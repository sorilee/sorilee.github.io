---
layout: post
date: 2020-07-22 15:30 KST
date created: 2020-07-22 KST
author: Sori Lee
---

# An algorithm for finding a maximally covering set of disjoint intervals

*I was spoken to about a programming problem by a colleague today. Below are a precise formulation and a linear-time solution that I proposed.*

**Definition.**

1. An *interval* is a pair $$(i,j)$$ of non-negative integers such that $$i \leq j$$.

2. Intervals $$(i,j)$$ and $$(k,l)$$ are *disjoint* if $$\{i, \ldots, j\} \cap \{k, \ldots, l\} = \emptyset$$.

3. A *set of disjoint intervals* means a set of pairwise disjoint intervals.

4. Let $$X$$ be a finite[^1] set of intervals. The *coverage* of $$X$$ is the set
\\[
C_X := \\{n \in \mathbf{Z}_{\geq 0} \mid i \leq n \leq j,\ (i,j) \in X\\}.
\\]
The *coverage size* of $$X$$ is the cardinality $$\lvert C_X \rvert$$.

5. Let $$I$$ be a finite set of intervals. A *maximally covering* set of disjoint intervals from $$I$$ refers to a set of disjoint intervals from $$I$$ whose coverage size is maximal.

6. Let $$S$$ be a non-negative integer.
An interval *below* $$S$$ means an interval $$(i,j)$$ with $$j < S$$.

[^1]: These finiteness restrictions are of course unnecessary for the definitions themselves, yet I assert them since infinite cases are irrelevant for our purposes.

**Problem.** Given a non-negative integer $$S$$ and a non-empty[^4] finite set $$I$$ of *input* intervals below $$S$$, find a maximally covering set of disjoint intervals from $$I$$.

[^4]: I assert this so that there is at least one maximally covering set of disjoint intervals from $$I$$, as that simplifies the formulations of both the problem and the algorithm.

Before giving an algorithm for this problem, I will first summarise the idea behind it in a proposition.

Some notations will be useful.
Let $$n \in \mathbf{Z}_{\geq 0}$$.
Write

- $$I_{=n} := \{(n,j) \in I\}\ (= \{(i,j) \in I \mid i = n\})$$, and

- $$I_{\geq n} := \{(i,j) \in I \mid i \geq n\}$$.

We further denote by $$M_n$$ an arbitrary maximally covering set of disjoint intervals from $$I_{\geq n}$$.

<!--
**Proposition.**
Let $$0 \leq n < S-1$$.
Write
\\[
(n,m) = \mathop{argmax}_{(n,j) \in I_{=n}} |C_{\\{(n,j)\\} \cup M_{j+1}}|.
\\]
Then $$\{(n,m)\} \cup M_{j+1}$$ is a maximally covering set of disjoint intervals from $$I_{\geq n}$$.
-->

**Proposition 1.** Let $$0 \leq n < S$$.

1. If $$I_{=n} = \emptyset$$, then $$M_{n+1}$$ is a maximally covering set of disjoint intervals from $$I_{\geq n}$$.

2. Otherwise, any set of the form
\\[
\\{(n,j)\\} \cup M_{j+1}
\\]
with $$(n,j) \in I_{=n}$$ whose coverage size is maximal, is a maximally covering set of disjoint intervals from $$I_{\geq n}$$. ∎

**Algorithm.**

1. For each $$n = 0, \ldots, S-1$$, compute $$I_{=n}$$ say as a list.[^2]

2. For each $$n = S-1, \ldots, 0$$, in that order, compute an $$M_n$$ using Proposition 1.[^3]

3. Report the $$M_0$$ as an answer.

[^2]: This step should be implemented to take $$O(S + \lvert I \rvert)$$ time.

[^3]: This step takes $$O(S + \lvert I \rvert)$$ time, since $$\lvert I \rvert = \lvert I_{=S-1} \rvert + \ldots + \lvert I_{=0} \rvert$$.

**Proposition 2.** This algorithm terminates, is correct and runs in $$O(S + \lvert I \rvert)$$ time. ∎

*I thank J. Yim for careful reading and correcting that the complexity should be $$O(S + \lvert I \rvert)$$ instead of $$O(\lvert I \rvert)$$, and H. Noh for the problem and discussions.*

*Footnotes.*
