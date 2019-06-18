---
layout:       post
title:        Boyer-Moore
summary:      Finding substring alignments in linear time.
categories:   
---




# Motivation


## A (very brief) crash course in genomics

What does it mean to sequence someone's genome? We'd like to figure out the string
of nucleotides (Adenine, Thymine, Guanine, and Cytosine) which make up their DNA.
A string of human DNA is over 3 billion nucleotides long, how do we do this in a
cost-efficient, timely manner? We make the sequencing massively parallel. We accomplish this
by splitting up a sample of DNA into small chunks (called shotgun sequencing), attaching each
of these chunks to one large grid, then sequencing each nucleotide one at a time.

Given this data, how do we get back someone's genome? Most human genomes are very alike, and so
we can use what is called a *reference genome* to *align* sequenced DNA to the reference genome,
and thus infer their entire genome. This brings us to the problem of alignment.

# Alignment

Thus, we've abstracted away the biology for now, and we're left with the computer science
problem of aligning a short-read to a reference genome. That is, we're left with finding ocurrences
of a substring in larger corpus. This is a classic problem in Computer Science, with applications in
other areas as well (e.g. search engines). Let's first consider a naive approach to this problem.

## Naive Algorithm

## Boyer-Moore Algorithm

There are two inefficiencies we might notice in the naive algorithm. That is, the naive algorithm checks
for alignments that are bound to fail. These two inefficiencies can be turned into heuristics (rules)
for deriving a better string-matching algorithm.

### Heuristics

#### The Bad Character Rule


#### The Good Suffix Rule


Why these heuristics? I'm not entirely sure, but I speculate:
- They're intuitive.
- They're sufficient for making the algorithm run in linear time (assuming the rules
    can be evaluated in linear time)
- *Indexes* for the rules can be constructed in linear time.

### Boyer-Moore in Linear Time

There's a great series of notes describing how to implement Boyer-Moore in linear time.
I really wanted to try and do this, and so I spent quite a few weeks implementing this, getting
stuck on some annoying bugs (the notes used 1-based indexing, and I 0-based indexing; it was nontrivial
to translate it and get it right). Implementing the construction of the good suffix rule index
in linear time was quite challenging, and rather unintuitive, requiring several steps, but the notes
provide a quite detailed explanation.

## Comparison
A short comparison between the naive and string matching algorithms

## Indexes

What do I mean by an index? It's essentially the same as a book index, or maybe a
"inverted" index. Boyer-Moore can be viewed as an algorithm which *indexes* the
query substring. Many algorithms instead will index the string to be queried (the reference genome).
This is more practical as we may have to do many queries all on the same reference genome. Construction of
an index for each query, though linear in the query, can take up more time than necessary as it must be done for each query (we also have to allocate extra memory for each query, which may cause issues if we're querying many at once).
Indexing the reference is easier since we do it once, and its cost can be amortized over all queries. In a future post I hope to dive into an algorithm which indexes the reference genome instead.

## Alternatives
Other popular string matching algorithms include KMP and Rabin-Karp. Apparently Boyer-Moore is more efficient for genomics, but I'm not sure why. At a minimum, it appears to be a very common algorithm introduced early on in a course on algorithms for genomic sequencing.

# Abstraction
Recall that early on in the post we made the abstraction that sequencing a genome involves aligning short reads to a reference genome. We ignored an important detail in that example: sequencing is *noisy*, and we don't always correctly read a sequence. Furthermore, the reference genome is not going to match exactly due to mutations. How do we account for this? It turns out we can do approximate matching using algorithms for exact matching with a few tricks on top, which I will detail in a future post.

# Acknowledgements
Ben Langmead's course and Jared Simpson's version of it.
