---
layout:       post
title:        An Exploration of Some Simple RL Algorithms
summary:      Exploring three simple algorithms to solve the Open AI Gym Cartpole environment.
categories:   
---

After looking into various ways to get started in machine learning research,
OpenAI's [Requests for Research](https://openai.com/requests-for-research/)
seemed like the perfect way to learn more about the field and how to do research
within it. I'm starting off with the warmup challenge which explores three
different algorithms to solve the OpenAI Gym
[Cartpole](https://gym.openai.com/envs/CartPole-v0/) environment. All code can
be found on my [github](https://github.com/jacobjinkelly/cartpole).

Some of the resources I used includes David Silver's
[RL course](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/pg.pdf),
Roger Grosse's
[CSC321](http://www.cs.toronto.edu/~rgrosse/courses/csc321_2018/slides/lec21.pdf),
Andrej Karpathy's RL [blog post](http://karpathy.github.io/2016/05/31/rl/),
Chapter 13 of _Reinforcement Learning: An Introduction_ by Sutton and Barto, and
last, the original place I heard about OpenAI's Requests for Research, Kevin Frans'
[blog post](http://kvfrans.com/simple-algoritms-for-solving-cartpole/).
In fact, I will be following Kevin's method pretty closely, so definitely check
it out.

# The Environment

The Cartpole environment consists of a cart supporting a pole on an axis. The
goal in this environment is to balance the pole by moving the cart side to side,
as seen in the GIF below.

<p style="text-align: center;">
  <img src="/images/an-exploration-of-some-simple-rl-algorithms/cartpole.gif" alt="Cartpole">
</p>

At each time step, we receive a four-dimensional observation vector[^1], and the
agent must then decide whether to move the cart left or right. A failure in this
environment is when the cart moves off screen, or the pole tips more than 12
degrees. Last, the environment automatically stops after 200 time steps. Our
reward in this environment is simply the number of time steps we last in the
environment before one of the above occurs. Success in this environment is
defined as achieving an average reward of at least 195 over 100 episodes in the
environment.

As suggested in the challenge, our RL agent will have a simple linear model of
the environment. That is, our agent's model will have 4 parameters, and upon
each observation, the agent will move the cart in one direction or the other
based on the sign of the dot product of its four parameters with the
four-dimensional observation[^2].

# Algorithms

## Random

For this algorithm, we'll make 10,000 guesses as to what a good set of parameters
are, and pick the best one.

First, it's important to consider the distribution over which we make our guesses.
We'd like our distribution to align as closely as possible with the region in
parameter space corresponding to good models; we'll use this as a rough
intuitive guideline for finding a good distribution.

First, we can guess that all four of the parameters should come from the same
distribution (and obviously they should be independent). As a default,
I'm going to try a Gaussian distribution. We have no *a priori*
reason to believe any of the parameters will be more important, thus the
standard deviations will be the same; likewise, we'll use a mean of 0, since we
have no reason to bias the parameters away from zero. We could tune the standard
deviation and fiddle with our distribution to get something that aligns even
more closely with ideal parameters, but this would basically amount to manually
learning good parameters for the model, which is not really the point of this
exercise.

It's also important to consider what we mean by the best agent of 10,000. In
the challenge, OpenAI defines this as being the agent which receives the most
reward over one episode. What happens if we instead evaluate agents over
several episodes? In particular, how much more likely are we to have found an
agent which solves the environment? After some initial experiments, using more
than one episode didn't significantly improve performance, especially compared
to the additional run time. In fact, the additional run time made it difficult
to run any extensive experiments, so I'll leave this to potential future
investigations.

## Hill Climbing

The hill climbing algorithm begins with a random set of weights. At each step,
it adds a small perturbation to the weights, and sees if this model is better.
If so, the algorithm updates the model to these new weights.

This algorithm is clearly an improvement over the last one. In particular, this
algorithm has an internal state, which it can build on top of to find an even
better model. In contrast, the random guessing algorithm is no more likely to find
a good model, no matter which iteration (guess) it is on[^3].

It's important for this algorithm to consider the distribution from which we sample
our perturbation of the weights. We'll use a Gaussian; the mean should be 0
(there's no reason to bias our updates towards increasing or decreasing the
parameters) and we'll have to tune standard deviation (akin to a step size).

## Policy Gradient

For this algorithm, we're going to need to modify our agent's policy to be stochastic.
Instead of choosing an action based on the sign of the dot product of the model
parameters and the observation vector, we'll consider the sigmoid applied to the
dot product, and interpret the result as the probability that the agent will
choose a particular action[^4]. In other words, the agent will pick actions by
sampling from a distribution parameterized by the model weights and conditioned
on the observation vector.

There are a few reasons why a stochastic policy is a good idea. First, it
improves the exploration behaviour of the algorithm, i.e. it makes the algorithm
less likely to prematurely optimize over the information it has gained so far about
the environment having not yet sufficiently explored the various states in the
environment. A simpler alternative to encourage exploration behaviour is known
as an $$\epsilon$$-greedy strategy: at each time step the agent will take a
random action with probability $$\epsilon$$. This can sometimes work for simple
problems, but the epsilon parameter is quite difficult to tune, and if our
algorithm is to converge, we would have to decay $$\epsilon$$ over time.
Having a stochastic policy on the other hand solves this problem; a stochastic
policy can converge to a deterministic policy (by making the correct choice
very probable and the other options vanishingly improbable), which is
essentially automatically decaying the exploration behaviour of our algorithm.

Second, introducing stochasticity makes our function smooth and continuously
differentiable. Intuitively, what this means is that a small change to the
parameters will result in some proportional change in the "output" of the model.
In the reinforcement learning setting, what we mean by output here is the agent's
expected behaviour in the environment; perturbing the parameters makes some
actions slightly more likely, and others slightly less likely. If, on the other
hand, our policy was deterministic, a small perturbation of the parameters would
either do nothing, or make our agent switch from making one action all the time
to making a different action all the time (in a certain state), because the
ordering of our preferences for actions changed. We can easily visualize this in
the two-dimensional case (e.g. for our current cartpole problem with two actions)

<p style="text-align: center;">
  <img src="/images/an-exploration-of-some-simple-rl-algorithms/step and sigmoid.png" alt="step and sigmoid functions">
</p>

The orange curve corresponds to a deterministic policy. Small changes to the
parameters result in no change to the actions of our agent, unless they switch
the output of our model from positive to negative (or vice versa). The blue curve,
on the other hand, represents the stochastic policy, where a small change to the
parameters results in a correspondingly small change to the output. In other words,
stochasticity gives us a smooth function, allowing us to use gradient-based optimization.

Last, stochasticity allows us to do better in environments where a deterministic
policy would fail; either due to inherent stochasticity in the environment, or
partial-observability. A deterministic policy would be sub-optimal as the
same observation (according to the agent) might have different optimal behaviour,
depending on the state we are in within the environment. A better (stochastic)
policy would attempt to model the distribution over possible states it might be in,
and act accordingly. In other words, stochasticity essentially expands the class
of possible models our algorithm might learn.

At last, we arrive at the policy gradient algorithm itself. In particular, we'll
use the simplest instantiation of the policy gradient algorithm, called REINFORCE.
Essentially the algorithm is the simplest approach one could take in reinforcement
learning: it amounts to a slightly sophisticated form of trial and error. An update
in the inner loop makes each action that caused a good outcome (i.e. a large reward)
more likely, and each action that caused a bad outcome less likely. It makes outcomes
more or less likely via gradient based optimization: the parameters are wiggled
in the direction that would make a particular outcome more likely (hence the need
for our model to have a smooth stochastic output).

# Experiments

We'd like to understand how these algorithms perform. In this case, since we
already have a very concrete definition of solving this environment, what's left
to analyze is how efficiently our three algorithms converge to a solution; in
other words, we'll look at how many episodes of experience it takes each of
our three algorithms to find an agent which solves the environment.



# Conclusion

There were a lot of things I learned in this project, most importantly was the
difficulty in designing experiments. This is something I'd put relatively
thought into, and is definitely something I've under appreciated in papers
I've seen. There's definitely a lot for me to improve in the way of making
my results more reproducible (e.g. see here and here on reproducing results
in reinforcement learning).

---
[^1]: The meaning of each entry in the vector is described in the Cartpole environment [wiki](https://github.com/openai/gym/wiki/CartPole-v0), however our goal here is to learn a good model regardless of the actual meaning of the observation. Of course, in certain scenarios it might also be interesting to consider ways of somehow encoding the semantics of this observation vector into the model, but I leave this question unexplored.
[^2]: Technically, we'll use the logistic function (squishing the dot product onto the interval [0, 1]), and round the answer. This only really matters for our third algorithm, the policy gradient (where we don't round).
[^3]: I recently discovered what MCMC methods were, and both the random and hill-climbing algorithms, at least on a surface level, have some similarities. There is at least an analogy here between finding an independent sample from a distribution and an agent which performs well according to some criteria in an environment.
[^4]: Read this great [distill article](https://distill.pub/2016/augmented-rnns/) to learn more about how we can make smooth differentiable functions out of choosing amongst a finite set of options. The distill article primarily discusses the attention trick, but also relates this trick to what is used in RL (as we'll explore further now).
