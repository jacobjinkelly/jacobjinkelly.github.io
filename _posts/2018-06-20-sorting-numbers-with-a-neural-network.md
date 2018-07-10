---
layout:       post
title:        Learning to Sort with a Neural Network
date:         2018-06-20
summary:      Exploring how one might teach a neural net to sort numbers.
categories:   
---

I recently came across an interesting challenge: sorting numbers with a neural
network[^1]. In contrast to other machine learning problems, this one is already
solved by classical methods (e.g. quicksort). And of course, the data we could
generate to feed to a machine learning model to learn how to sort is endless, so
what makes this problem interesting is how *little* data a machine learning
model would need to learn how to sort.

## Generalization to Longer Sequences
One of the most useful properties we could have would be for the model to learn
an algorithm which generalizes to longer input sequences. In particular, the
actual model architecture would readily need to have the capacity to generalize
to longer sequences, and the learning algorithm which trains it would have to
regularize appropriately so that the model does not overfit to the shorter
sequences it sees during training.

## A Naive Approach
This problem obviously requires us to learn a function which maps sequences to
sequences, and an obvious way to perform this will be using an encoder-decoder
RNN architecture, as used for translation problems. One can do better by using
a common variant of this architecture: augmentation via an attention mechanism.
But can we do even better?

# An Improvement

## Outputs correspond directly to inputs
In contrast to many sequence to sequence problems, the output of the model
will in fact be elements of the input. Many sequence to sequence problems are
some sort of translation between domains, and hence, obviously, outputs will
correspond to inputs *roughly* in a one-to-one manner, depending on the domain.
But in sorting, outputs correspond to inputs *precisely* in a one-to-one manner,
i.e. the output is a permutation of the input.

## Pointer Networks
The issue with returning a prediction corresponding to one of the input elements
is that the there are a *variable number* of them depending on the specific
example. However, it turns out we can use a simple trick to modify our attention
mechanism slightly so that we can get a prediction over the input elements. This
architecture, called a Pointer Network, is described in much more detail in the
[original paper](https://arxiv.org/pdf/1506.03134.pdf).

# Additional Observations
There are in fact a lot of other interesting ideas one might apply to this
problem. Here are some speculations and ideas that I had that I haven't yet
gotten the chance to try out.

## Invariance to Permutation
One crucial invariance in the sorting problem, in contrast to most other
sequence to sequence problems (e.g. translation), is
that the order of the inputs does not affect the outcome. Or, as
[FastML writes](http://fastml.com/introduction-to-pointer-networks/)

> In essence we’re dealing with sets, not sequences, as input. Sets don’t have
inherent order, so how elements are permuted ideally shouldn’t affect the
outcome.

So, my comment earlier about us wanting to learn a function mapping from
sequence to sequence is actually not quite true. One approach to fixing this
problem might be including all possible permutations of a sequence, along with
the (same) output in the training set, essentially "emphasizing"[^2] to the model
that the output should be invariant to permutation. However, this would be
extremely expensive (factorial growth with the length of the sequence) and might
not even work (i.e. "emphasize" to the model that order doesn't matter).
Instead, it'd be much better if we could encode this invariance in the design of
the architecture itself. This is what the original authors of the Pointer
Network did, and you can read more about it
[here](https://arxiv.org/pdf/1511.06391.pdf).

## Elastic Weight Consolidation
I recently read the paper describing
[this method](https://arxiv.org/pdf/1612.00796.pdf) to do incremental
learning[^3], and I thought I might use it to try to help the network generalize
to longer sequences. In particular, one could use a form of curriculum learning:
incrementally teach the model to sort longer and longer sequences, (using EWC to
"overcome catastrophic forgetting") and this might lead the network to better
generalization (unfortunately I haven't been able to do any experiments yet).

## Amount of computation at each step
A sequence to sequence model will, at each step, perform the same number of
operations. Even simple sorting algorithms like insertion sort perform different
amounts of computation at each step. It seems unreasonable for the decoder in
our architecture to perform the same amount of steps whether it's supposed to
spit out 100 more numbers or 5. Once again, it turns out someone has already
thought of this: it's called
[Adaptive Computation Time](https://arxiv.org/pdf/1603.08983.pdf)
and you can read more about it on
[distill](https://distill.pub/2016/augmented-rnns/#adaptive-computation-time) as
well.

# Conclusion

There is still plenty of potential future work to be done. More experiments
should be performed looking at generalization to longer sequences, the
performance of the models against the permutation metric and the nondecreasing
metric[^4], and coming up with other metrics and visualizations to better
understand how to further improve these models.

Even a simple toy problem like sorting turns out to spark a lot of interesting
intuitions, and led me to discover a lot of cool new architectures and
optimization schemes.

---
[^1]: In particular sorting a finite set of integers. (Or, if one wanted to be really pedantic, an arbitrary totally ordered finite set)
[^2]: It turns out there's actually a name for this intuition of hand crafting the examples one feeds to a model: curriculum learning.
[^3]: Continually learning new tasks without forgetting old ones.
[^4]: i.e. permutation metric being whether or not the network's output is permutation of the input, and nondecreasing metric being whether or not the network's output is nondecreasing sequence (i.e. "sorted")
