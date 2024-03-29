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

### Fourth Year
- ECE1502: Information Theory ([*Frank Kschischang*](https://www.comm.utoronto.ca/frank/))
    - This was the only engineering course I took during my undergrad.
    While this was essentially a math course, I think engineering takes a unique perspective distinct from what I've seen in other math courses.
    For example, many of the homework problems had unstated assumptions you needed to use in your solution. 
    This made it feel like solving a research problem, in that all the contraints weren't clear from the start.
- MAT1841: Mathematics of Massive Data Analysis ([*Yun William Yu*](https://yunwilliamyu.net/content/))
    - This was a small seminar class I took. It covered a bunch of different disciplines that have cool math as a foundation for methods they used to process large amounts of data.
    This course was a lot of fun, and very challenging. We covered such a wide breadth of mathematical areas, many of which I was surprised had practical applications.
- MAT1850: Linear Algebra and Optimization ([*Mary Pugh*](http://www.math.toronto.edu/mpugh/))
    - This course taught me a lot of math I've seen in ML papers, but hadn't deeply understood until now.
    It goes beyond what you learn in standard undergraduate linear algebra courses, and gives you a basic foundation in optimization.
- CSC495: Research Project in Computer Science ([*Roger Grosse*](https://www.cs.toronto.edu/~rgrosse/))
    - This course allowed me to do a research project for course credit. 
    I worked with Guodong Zhang, Vardan Papyan, and Roger Grosse on a project related to [KFAC](https://arxiv.org/abs/1503.05671).
    This was a fun project because it tied math and code together very closely. 
    There were many times we had to do some math to properly understand the result of an experiment, or develop a new hypothesis.
- CSC2321: Matrix Calculations ([*Christina Christara*](https://www.cs.toronto.edu/~ccc/))
    - This was a numerical methods course. I wrote more MATLAB code for this course than I ever wrote before.
    I learned that you can precisely test the correctness of a numerical method implementation.
    It's very easy to write buggy numerical code that still converges most of the time, and this course taught me how to find those subtle bugs.
    The professor listed a bunch of numerical methods textbooks for this course, and it was really cool reading through them and finding cool and very useful tricks that 
    you really wouldn't be able to find anywhere else online.
- CSC369: Operating Systems ([*Angela Demke Brown*](https://www.cs.toronto.edu/~demke/))
    - I really enjoyed this course. It was fascinating to hear about all the engineering tricks that go into making various parts of the OS work.
    The assignments were essentially just large C-programming assignments; it was a lot of fun writing a lot of code, and making it as clean as possible so that it was easy to debug.
    We used [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/) for this course, which is the most engaging textbook I've ever read.
- CSC317: Computer Graphics ([*David Levin*](http://142.93.146.228/researchdb/))
    - This was the best organized course I've taken. The assignments were a lot of fun because they involved writing code to make a pretty picture at the end.
    The assignments taught me to break down a large task into manageable parts, each of which could be tested on its own.
- MAT363: Curves and Surfaces ([*Alexander Nabutovsky*](http://www.math.toronto.edu/nabutovsky/))
    - I took this course purely for fun. I hadn't done any pure math courses in a while, so this was a nice change of pace.
- STA261: Probability and Statistics II ([*Mohammad Kaviul Anam Khan*](https://www.statistics.utoronto.ca/people/directories/all-faculty/mohammad-kaviul-anam-khan))
    - This course was extremely useful, and I wish I'd found the time to take it sooner. 
    We learned about hypothesis testing, and frequentist statistics more broadly, which is something that had been sorely lacking in my toolkit until this course.

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
    or their tradeoffs with different parameters. I wonder how much this has to do with the fields being fundamentally different versus one simply having better developed theory.
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
- CSC494: Research Project in Computer Science
    ([*David Duvenaud*](http://www.cs.toronto.edu/~duvenaud/))
    - This was a chance for me to do research for course credit. It gave me the extra time I needed to build
    a lot of necessary fundamental technical skills for running experiments. Eventually the work for this
    project turned into the paper [Learning Differential Equations that are Easy to Solve](https://arxiv.org/abs/2007.04504).

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
    - I learned how to compute covariance. I also learned the difference between mutually-independent and conditionally-independent. I also learned about [moment generating functions](https://en.wikipedia.org/wiki/Moment-generating_function).
- CSC209: C & Systems Programming
([*Michelle Craig*](https://michellecraig.github.io/))
    - I had a lot of fun in this course. It was my first chance to do some low-level programming. It can be very stressful and frustrating, but also rewarding.
    - I also learned to be comfortable in shell. I can't understate how useful this skill was.
- CSC265: Enriched Data Structures and Analysis
([*Aleksandar Nikolov*](http://www.cs.toronto.edu/~anikolov/))
    - In addition to standard data structures and algorithms, this course covered adversary arguments to prove lower bounds on problem complexity, and the [potential method](https://en.wikipedia.org/wiki/Potential_method) for analyzing amortized complexity.
- CSC373: Algorithm Design, Analysis & Complexity ([*François Pitt*](http://www.cs.toronto.edu/~fpitt/))
    - A great lecturer. This was another instance where I learned much better than when I had tried to teach myself.
    Preparing for tests in this course felt more useful than other courses, since in many ways it's similar to preparing
    for technical interviews.
    - We spent some time learning about P and NP. I feel like it's only worthwhile to
    learn that content if you spend an entire semester digging into the details. Instead,
    I wish we'd learned about something else like [FFT](https://en.wikipedia.org/wiki/Fast_Fourier_transform).
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
    - I had tried and failed to teach myself about recursion and binary trees before taking this course.
    This course taught me those concepts really well, and moreover I was surprised how easy it felt to learn them.
    - I meta-learned that learning new things is much more efficient when you can find a good resource to learn it from rather than just trying think really hard about it for a long time and getting frustrated.
- CSC165: Mathematical Expression and Reasoning for Computer Science
([*Danny Heap*](http://www.cs.toronto.edu/~heap/))
    - One cool thing we learned was connecting number theory concepts to applications to [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)) in cryptography.
- CSC207: Software Design
([*Lindsey Shorser*](https://www.math.toronto.edu/cms/people/faculty/shorser-lindsey/) and
[*Jaisie Sin*](https://www.jaisiesin.com/))
    - One random thing I learned in this course was about underflow and overflow in floating point.
    - Besides this, I think the course would have been more interesting if there was a larger project component.
- CSC240: Enriched Introduction to Theory of Computation
([*Faith Ellen*](http://www.cs.toronto.edu/~faith/))
    - The most challenging course I've taken. Heavy emphasis on problem-solving
    techniques and thinking deeply combined with rigorous proofs (including formal proofs.)
    - For one problem set we were given the
    [Boyer-Moore majority voting algorithm](https://en.wikipedia.org/wiki/Boyer%E2%80%93Moore_majority_vote_algorithm)
    and had to come up with and prove our own invariants to show correctness.
- CCR199: Common Humanity
([*John Noyes*](https://german.utoronto.ca/john-k-noyes/))
    - A small seminar course looking at the idea of common humanity throughout
    history, with a particular focus on Apartheid in South Africa.
- LTE199: Biotechnology and Society
([*John Coleman*](https://csb.utoronto.ca/john-coleman/))
    - A small seminar course looking at the potential impact of various
    biotechnologies such as CRISPR-Cas9 and paradigms such as personalized medicine.
