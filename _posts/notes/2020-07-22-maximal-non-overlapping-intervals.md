---
layout: post
date: 2020-07-22 15:30 KST
date created: 2020-07-22 KST
author: Sori Lee
---

# An algorithm for finding a coverage-maximal set of non-overlapping intervals

*I was given a programming problem by a colleague today. Below are a precise formulation and a linear-time solution that I suggested.*

**Definition.** In what follow, a 'natural number' shall mean a non-negative integer.

1. An *interval* is a pair $$(i,j)$$ of natural numbers such that $$i \leq j$$.

2. Intervals $$(i,j)$$ and $$(k,l)$$ are *non-overlapping* if $$[i,j] \cap [k,l] = \emptyset$$.

3. By a *set of non-overlapping intervals* we shall mean a set of pairwise non-overlapping intervals.

4. Let $$X$$ be a finite[^1] set of intervals. The *coverage* of $$X$$ is the set
\\[
C_X := \\{n \in \mathbf{N} \mid i \leq n \leq j,\ (i,j) \in X\\}.
\\]
The *coverage size* of $$X$$ is the cardinality $$\lvert C_X \rvert$$.

5. Let $$I$$ be a finite set of intervals. A *coverage-maximal* set of non-overlapping intervals from $$I$$ refers to a set of non-overlapping intervals from $$I$$ whose coverage size is maximal.

6. Let $$S$$ be a natural number.[^2]
An interval *in* $$S$$ shall mean an interval $$(i,j)$$ with $$j < S$$.

[^1]: This restriction is of course unnecessary for this definition itself, but I have asserted it since infinite cases are irrelevant for our purposes.

**Problem.** Given a natural number $$S$$ and a non-empty finite set $$I$$ of *input* intervals in $$S$$, find a coverage-maximal set of non-overlapping intervals from $$I$$.

I will first summarise the idea behind the algorithm in a proposition.

Some notations will be useful.
Let $$n \in \mathbf{N}$$.
Write

- $$I_{=n} := \{(n,j) \in I\}\ (= \{(i,j) \in I \mid i = n\})$$, and

- $$I_{\geq n} := \{(i,j) \in I \mid i \geq n\}$$.

We further denote by $$M_n$$ an arbitrary coverage-maximal set of non-overlapping intervals from $$I_{\geq n}$$. This is an algorithm for the above Problem:

<!--
Now the idea behind the algorithm to be presented is summarised in:
-->

<!--
**Proposition.**
Let $$0 \leq n < S-1$$.
Write
\\[
(n,m) = \mathop{argmax}_{(n,j) \in I_{=n}} |C_{\\{(n,j)\\} \cup M_{j+1}}|.
\\]
Then $$\{(n,m)\} \cup M_{j+1}$$ is a coverage-maximal set of non-overlapping intervals from $$I_{\geq n}$$.
-->

**Proposition 1.** Let $$0 \leq n < S-1$$.

1. If $$I_{=n} = \emptyset$$, then $$M_{n+1}$$ is a coverage-maximal set of non-overlapping intervals from $$I_{\geq n}$$.

2. Otherwise, any set of the form
\\[
\\{(n,j)\\} \cup M_{j+1}
\\]
with $$(n,j) \in I_{=n}$$ whose coverage size is maximal, is a coverage-maximal set of non-overlapping intervals from $$I_{\geq n}$$. ∎

**Algorithm.**

1. For each $$n = 0, \ldots, S-1$$, compute $$I_{=n}$$ say as a list.[^2]

2. For each $$n = S-1, \ldots, 0$$ (in that order), compute an $$M_n$$ using Proposition 1.[^3]

3. Report the $$M_0$$ as the answer.

[^2]: This step should be implemented to take $$O(S + \lvert I \rvert)$$ time.

[^3]: This step takes $$O(S + \lvert I \rvert)$$ time, since $$\lvert I \rvert = \lvert I_{=0} \rvert + \ldots + \lvert I_{=S-1} \rvert$$.

**Proposition 2.** This algorithm terminates, is correct and runs in $$O(S + \lvert I \rvert)$$ time. ∎

*I thanks colleague J. Yim for careful reading and pointing out that the complexity is $$O(S + \lvert I \rvert)$$ instead of $$O(\lvert I \rvert)$$, and colleague H. Noh for the problem and discussions.*

*Footnotes.*
