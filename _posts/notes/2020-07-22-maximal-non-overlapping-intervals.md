---
layout: post
date: 2020-07-22 KST
date created: 2020-07-22 KST
author: Sori Lee
---

# An algorithm for finding a coverage-maximal set of non-overlapping intervals

**Definition.** In what follow, a 'natural number' shall refer to a non-negative integer.

1. Let $$S$$ be a natural number. An *interval* in $$N$$ is a pair $$(i,j)$$ of natural numbers with $$i \leq j < S$$.

For what follow, we fix the $$S$$, and an 'interval' without further elaboration shall refer to an interval in $$S$$.

2. Intervals $$(i,j)$$ and $$(k,l)$$ are *non-overlapping* if $$[i,j] \cap [k,l] = \emptyset$$.

3. By a *set of non-overlapping intervals* we mean a set of pairwise non-overlapping intervals.

4. Let $$X$$ be a set of intervals. The *coverage* of $$X$$ is the set
\\[
C_X := \{n \in \mathbf{N} \mid i \leq m \leq j,\ (i,j) \in X\}.
\\]
The *coverage size* of $$X$$ is the natural number $$|C_X| \leq X$$.

- A *coverage-maximal* set of non-overlapping intervals refers to a set of non-overlapping intervals whose coverage size is maximal.

**Problem.** Given a set of intervals in $$S$$, find a coverage-maximal set of non-overlapping intervals.

**Algorithm.** TBC