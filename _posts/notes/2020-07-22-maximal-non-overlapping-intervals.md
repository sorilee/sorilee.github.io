---
layout: post
date: 2020-07-22 KST
date created: 2020-07-22 KST
author: Sori Lee
---

# An algorithm for finding a coverage-maximal set of non-overlapping intervals

**Definition.** In what follow, a 'natural number' shall refer to a non-negative integer.

1. An *interval* is a pair $$(i,j)$$ of natural numbers such that $$i \leq j$$.

2. Intervals $$(i,j)$$ and $$(k,l)$$ are *non-overlapping* if $$[i,j] \cap [k,l] = \emptyset$$.

3. By a *set of non-overlapping intervals* we shall mean a set of pairwise non-overlapping intervals.

4. Let $$X$$ be a finite[^1] set of intervals. The *coverage* of $$X$$ is the set
\\[
C_X := \\{n \in \mathbf{N} \mid i \leq n \leq j,\ (i,j) \in X\\}.
\\]
The *coverage size* of $$X$$ is the cardinality $$|C_X|$$.

5. Let $$I$$ be a finite set of intervals. A *coverage-maximal* set of non-overlapping intervals from $$I$$ refers to a set of non-overlapping intervals from $$I$$ whose coverage size is maximal.

6. Let $$S$$ be a natural number.[^2]
An *interval* in $$S$$ shall mean an interval $$(i,j)$$ with $$j < S$$.

[^1]: This restriction is of course unnecessary for these definitions, but I have asserted it since infinite cases are irrelevant for our purposes.

[^2]: For ㅎㅊ: this is the number is words in your given sentence.

**Problem.** Given a natural number $$S$$ and a set $$I$$ of intervals in $$S$$, find a coverage-maximal set of non-overlapping intervals from $$I$$.

<!-- Here is the idea behind the algorithm to be presented.
Let -->

**Proposition.**

<!-- **Algorithm.** TBC -->

