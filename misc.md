---
layout: page
title: Misc.
permalink: /misc/
tags: misc
---

<style>
    ul {
      margin-bottom: 0;
    }
</style>


## Online Courses

Ones for which I've completed a significant portion and really enjoyed.

- [Algorithms for DNA Sequencing](https://www.coursera.org/learn/dna-sequencing)
([*Ben Langmead*](http://www.langmead-lab.org/))
    - This course begins by explaining how sequencing actually works. According to
    [James Somers](https://jsomers.net/i-should-have-loved-biology/),
    understanding the methods, like sequencing, used to study biology is a more
    effective way to acquire a "reading knowledge" of biology.
    - The course focuses on string algorithms. Presenting this content in the
    context of impacting genomics made it far more interesting than if it was
    presented abstractly.
- [Human Behavioural Biology](https://www.youtube.com/playlist?list=PL848F2368C90DDC3D&app=desktop)
([*Robert Sapolsky*](https://en.wikipedia.org/wiki/Robert_Sapolsky))
    - The best lecturer I've seen. He does an amazing job of crafting a narrative
    around the science.
- [Machine Learning](https://www.coursera.org/learn/machine-learning)
([*Andrew Ng*](https://www.andrewng.org/))
    - This course got me incredibly excited about machine learning.
    This course provided a solid foundation which I've relied on ever since to
    learn more about machine learning.
- [Learning How to Learn](https://www.coursera.org/learn/learning-how-to-learn)
([*Barbara Oakley*](https://barbaraoakley.com/))
    - I originally learned about this course from [this article](http://nautil.us/issue/17/big-bangs/how-i-rewired-my-brain-to-become-fluent-in-math) by the instructor.
- [Introduction to Mathematical Thinking](https://www.coursera.org/learn/mathematical-thinking)
([*Keith Devlin*](https://web.stanford.edu/~kdevlin/))
    - I was really curious about what it actually meant to prove something in math
    and this course was a great introduction that improved my logical thinking ability.
- [CS50: Introduction to Computer Science](https://online-learning.harvard.edu/course/cs50-introduction-computer-science)
([*David J. Malan*](https://cs.harvard.edu/malan/))
    - I loved the breadth of topics covered in this course; this was my first deep
    exposure to computer science and I got to learn about topics such as
    ciphers, sorting algorithms, hash tables, linked lists, and file I/O.
    The problem sets are excellent and give a sense of curious exploration.


## Courses

### Third Year
- STA347: Probability
([*David Brenner*](https://www.statistics.utoronto.ca/people/directories/all-faculty/david-brenner))
    - In this course we proved that you can uniformly sample a real number on an
    interval by uniformly sampling the bits of that number (or a digit in whichever base you like),
    to whatever precision you like.
    In other words, we constructed the continuous uniform distribution from the discrete uniform distribution.
    - Besides this result being beautiful in its own right, it suggests an implementation
    of uniform sampling on a computer (though I'm not sure if it's practical).
    - In general the theme of the course was constructing complex distributions from simpler ones and
    proving things "structurally" (instead of manually calculating expectations by integrating).
- STA447/2006: Stochastic Processes
([*Jeffrey Rosenthal*](http://probability.ca/jeff/))
    - The course focused on Markov chains. Many of the results  about convergence are subtle and
    hard to understand intuitively without a grasp of real analysis which I did not have.
    - We briefly talked about Brownian motion and other continuous time stochastic processes,
    but once again, these were hard to get a handle of without the proper background in analysis.
    - I need to take real analysis to understand these things!
- CSC258: Computer Organization
([*Maziar Goudarzi*](http://sharif.edu/~goudarzi/))
    - This course is an ECE course that CS students are required to take, and most dread it.
    While it has a heavy workload, I found the course fascinating.
    - Each week we would learn about the implementation of a circuit component, and the
    next week that circuit component would become a black box which we would use to construct the next circuit
    component. For example, we started with transistors and eventually learned about flip-flop circuits.
    - Programming in Verilog was unintuitive. It's a language that's basically HTML for circuits, but designed to
    have an imperative feel like C or Python. We also learned some Assembly which was cool in the way
    that all low-level programming languages are, but also not fun for the same reasons.
    Luckily we only wrote code snippets in this course so we just did the fun bits.
- CSC473: Advanced Algorithm Design
([*Aleksandar Nikolov*](http://www.cs.toronto.edu/~anikolov/))
    - One of the best courses I've taken.
    The focus is on randomized and approximation algorithms ([course website](http://www.cs.toronto.edu/~anikolov/CSC473W20/)). Such a breadth of topics is covered that it's hard to summarize.
    - One random cool thing I learned about was [reservoir sampling](https://en.wikipedia.org/wiki/Reservoir_sampling),
    though we didn't do much streaming algorithms in general. [Tim Vieira](https://timvieira.github.io/blog/post/2014/08/01/gumbel-max-trick-and-weighted-reservoir-sampling/) has a few posts about it.
    - Locality sensitive hashing is cool.
    - We learned some cool techniques like Chebyshev's inequality, Chernoff bounds, and complementary slackness in linear programming.
    - The algorithms we covered solve foundational problems in a general way. We understand how these algorithms work
    and their tradeoffs. They have at most a handful of parameters that need to be tuned according to the tradeoffs the user wants. Contrast this with machine learning, where often we want to solve a specific problem better than a general algorithm could by leveraging data. We don't understand a lot of machine learning algorithms nearly as well
    or their tradeoffs with different parameters. I wonder how much this has to do with the fields being fundamentally different versus one simply having better develped theory.
- APM462: Nonlinear Optimization
([*Jonathan Korman*](https://www.math.toronto.edu/jkorman/))
    - We learned some basics about convexity (zeroth, first, and second order conditions).
    I wish we'd done more, since it seems like it has the right tradeoff between being tractable and becoming useful
    (at least according to [Boyd and Vandenberghe](https://web.stanford.edu/~boyd/cvxbook/)).
    - We learned about variational optimization, which usually means minimizing an integral over
    a space of functions instead of over vectors. It seems cool but probably only useful for physics.
- BIO130: Molecular and Cell Biology
([*Melody Neumann*](https://csb.utoronto.ca/melody-neumann/) and
[*Daphne Goring*](http://labs.csb.utoronto.ca/goring/))
    - My first course in biology since the 10th grade. I went to [Con. Hall](https://en.wikipedia.org/wiki/Convocation_Hall_(University_of_Toronto)) for the first time for lectures for this class.
    - It was so much fun diving into the details and learning about biology. Surprisingly, I found the labs
    very useful. They gave me a taste of how knowledge is acquired in biology, which makes it much
    easier to understand what is known in biology.
- LIN101: Introduction to Linguistics: Sound Structure
([*Peter Jurgec*](http://www.jurgec.net/))
    - Peter Jurgec is a very engaging lecturer. This course was full of moments where we would
    learn a concept that formalized something we already had an intuitive feel for. One very simple
    example was that the only difference between the "s" and "z" sounds is that we engage our vocal chords
    to make the "z" sound.
- LIN102: Introduction to Linguistics: Sentence Structure and Meaning
([*Susana Bejar*](https://www.linguistics.utoronto.ca/people/directories/all-faculty/susana-b%C3%A9jar))
    - This course focused on mathematizing language, which I found not very exciting as the concepts
    were things that I'd already learned in my math and CS courses, whereas I was looking to learn things
    radically different from my normal coursework. But most people I know seemed to really enjoy this course!
- PHL271: Law and Morality
([*Sophia Moreau*](https://www.law.utoronto.ca/faculty-staff/full-time-faculty/sophia-reibetanz-moreau))
    - These lectures were amazing. I learned some new words in this course. It's also the first time
    I heard someone refer to "law" as "The Law", which makes it sound way cooler.
    - One thing I learned about was the difference between [positive freedom](https://en.wikipedia.org/wiki/Positive_liberty) and [negative freedom](https://en.wikipedia.org/wiki/Negative_liberty).

### Second Year
- MAT257: Analysis II
([*Edward Bierstone*](https://www.math.toronto.edu/bierston/))
    - Closely follows Michael Spivak's
    [Calculus on Manifolds](https://en.wikipedia.org/wiki/Calculus_on_Manifolds_(book)).
    Topics included topology, the implicit function theorem, measure theory, partitions of unity, differential forms, culminating in Stokes' Theorem on manifolds.
- MAT267: Advanced Ordinary Differential Equations
([*Mary Pugh*](http://www.math.toronto.edu/mpugh/))
    - Covered some analysis to show existence and uniqueness theorems for ODEs, then switched to a dynamical systems perspective including phase plots, Lyapunov functions, stability of solutions, and bifurcations.
- STA257: Probability and Statistics I
([*Mark Ebden*](http://www.mebden.com/))
- CSC209: C & Systems Programming
([*Michelle Craig*](https://michellecraig.github.io/))
- CSC265: Enriched Data Structures and Analysis
([*Aleksandar Nikolov*](http://www.cs.toronto.edu/~anikolov/))
    - In addition to standard data structures and algorithms, this course covered adversary arguments to prove lower bounds on problem complexity, and the [potential method](https://en.wikipedia.org/wiki/Potential_method) for analyzing amortized complexity.
- CSC373: Algorithm Design, Analysis & Complexity ([*François Pitt*](http://www.cs.toronto.edu/~fpitt/))
- CSC411/2515: [Machine Learning and Data Mining](http://www.cs.toronto.edu/~rgrosse/courses/csc411_f18/)
([*Roger Grosse*](http://www.cs.toronto.edu/~rgrosse/))
    - Focus on using a mathematical framework to understand classical algorithms leading to principled generalizations (e.g. k-means to EM algorithm, regularization as MAP estimation).
- CSC412/2506: [Probabilistic Learning and Reasoning](http://www.cs.toronto.edu/~jessebett/CSC412/)
([*Jesse Bettencourt*](http://www.jessebett.com/))
    - Independence relationships in Bayesian networks via d-separation, as well as inference and learning in other probabilistic graphical models. Focus on variational inference in latent variable models, in particular implementing a VAE from scratch.
- CSC421/2516: [Neural Networks and Deep Learning](http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/)
([*Roger Grosse*](http://www.cs.toronto.edu/~rgrosse/))
    - Modern deep learning research, in particular implementing attention mechanisms in a Transformer, and implementing a CycleGAN.
- CSC2541: [Machine Learning for Health](https://cs2541-ml4h2019.github.io/)
([*Marzyeh Ghassemi*](http://www.marzyehghassemi.com/))
    - A graduate seminar course looking at research into applying machine learning in the clinic, with major project and problem set components.

### First Year
- MAT240: Algebra I
([*Eckhard Meinrenken*](http://www.math.toronto.edu/mein/))
    - We used the book Linear Algebra by Insel, Spence, and Friedberg.
    - Proofs in linear algebra are all so clean. This was a great way to be introduced to proofs.
- MAT247: Algebra II
([*Stephen Kudla*](http://www.math.toronto.edu/~skudla/))
    - We used the book Linear Algebra by Insel, Spence, and Friedberg.
    - We learned about the [Jordan Canonical Form](https://en.wikipedia.org/wiki/Jordan_normal_form), which was
    super confusing and hard to compute. But then it came up later in my ODEs class which was cool.
    - We also learned the [Cayley-Hamilton theorem](https://en.wikipedia.org/wiki/Cayley%E2%80%93Hamilton_theorem),
    which was super weird. I think it has a lot of interesting applications but I haven't encountered one myself outside
    this class.
- MAT157: Analysis I
([*Joe Repka*](http://www.math.utoronto.ca/~repka/))
    - Closely follows Michael Spivak's Calculus. This course was my first introduction to
    pure math, and is particularly known for rigorously constructing
    the real numbers using [dedekind cuts](https://en.wikipedia.org/wiki/Dedekind_cut) in the first month.
- CSC148: Introduction to Computer Science
([*David Liu*](https://www.cs.toronto.edu/~david/))
- CSC165: Mathematical Expression and Reasoning for Computer Science
([*Danny Heap*](http://www.cs.toronto.edu/~heap/))
- CSC207: Software Design
([*Lindsey Shorser*](https://www.math.toronto.edu/cms/people/faculty/shorser-lindsey/) and
[*Jaisie Sin*](https://www.jaisiesin.com/))
- CSC240: Enriched Introduction to Theory of Computation
([*Faith Ellen*](http://www.cs.toronto.edu/~faith/))
    - The most challenging course I've taken. Heavy emphasis on problem-solving
    techniques and thinking deeply combined with rigorous proofs (including formal proofs.)
- CCR199: Common Humanity
([*John Noyes*](https://german.utoronto.ca/john-k-noyes/))
    - A small seminar course looking at the idea of common humanity throughout
    history, with a particular focus on Apartheid in South Africa.
- LTE199: Biotechnology and Society
([*John Coleman*](https://csb.utoronto.ca/john-coleman/))
    - A small seminar course looking at the potential impact of various
    biotechnologies such as CRISPR-Cas9 and paradigms such as personalized medicine.
