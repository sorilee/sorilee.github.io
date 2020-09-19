---
layout: post
date: 2020-07-22 KST
date created: 2020-07-22 KST
author: Sori Lee
---

# Computational linguistics terminologies

**Supertagging, supertags.**

In the context of CCG, Lewis *et al.* [LLZ16] writes:

> The process of assigning CCG categories to words is called *supertagging*. All supertaggers used in practice are probabilistic, providing a distribution over possible tags for each word. Parsing models either use these scores directly (Auli and Lopez, 2011b), or as a form of beam search (Clark and Curran, 2007), typically in conjunction with models of the dependencies or derivation.

In a like context, [Clark](https://www.cl.cam.ac.uk/teaching/1011/L107/clark-lecture7.pdf) writes:

> The first stage in the CCG parsing pipeline is to assign CCG lexical categories to the words in the sentence. This process is known as *supertagging*, since the labels being assigned are detailed syntactic structures.

In general, I will understand *supertagging* as the process of assigning [syntactic categories](https://en.wikipedia.org/wiki/Syntactic_category) to words (in a sentence), with respect to the grammatical theory in consideration.

## References

- [LLZ16]: Mike Lewis, Kenton Lee, Luke Zettlemoyer. *LSTM CCG Parsing*. NAACL 2016, http://dx.doi.org/10.18653/v1/N16-1026
