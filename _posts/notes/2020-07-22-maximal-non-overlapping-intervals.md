---
layout: post
date: 2020-07-22 KST
date created: 2020-07-22 KST
author: Sori Lee
---

# An algorithm for finding a coverage-maximal set of non-overlapping intervals

**Definition.** In what follow, a 'natural number' shall refer to a non-negative integer.

- Let $$S$$ be a natural number.[^1] An *interval* in $$S$$ is a pair $$(i,j)$$ of natural numbers with $$i \leq j < S$$.

[^1]: For ㅎㅊ: this is the number is words in your given sentence.

For what follow, we fix the $$S$$, and an 'interval' without further elaboration shall refer to an interval in $$S$$.

- Intervals $$(i,j)$$ and $$(k,l)$$ are *non-overlapping* if $$[i,j] \cap [k,l] = \emptyset$$.

- By a *set of non-overlapping intervals* we mean a set of pairwise non-overlapping intervals.

- Let $$X$$ be a set of intervals. The *coverage* of $$X$$ is the set
\\[
C_X := \\{n \in \mathbf{N} \mid i \leq n \leq j,\ (i,j) \in X\\}.
\\]
The *coverage size* of $$X$$ is the cardinality $$|C_X|$$.

- Let $$X$$ be a (finite) set of intervals. A *coverage-maximal* set of non-overlapping intervals from $$X$$ refers to a set of non-overlapping intervals in $$X$$ whose coverage size is maximal.

**Problem.** Given a set $$I$$ of intervals in $$S$$, find a coverage-maximal set of non-overlapping intervals from $$I$$.

<!-- Here is the idea behind the algorithm to be presented.

**Algorithm.** TBC -->
