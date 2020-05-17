---
layout: post
date: 2020-05-17 13:23 KST
author: Sori Lee
---

# Kraft's Inequality

**Definition.** Let $$\newcommand{\:}{\colon}
\newcommand{\abs}[1]{\left\lvert#1\right\rvert}
S$$ and $$T$$ be finite sets (alphabets). A
*prefix code* is a function $$C\: S \to T^*$$ such that for
$$s,s' \in S$$, if $$C(s) \preceq C(s')$$[^1] then $$s = s'$$.

[^1]: This notation means: $$C(s)$$ is an initial segment of
$$C(s')$$.

Let $$C\: S \to T^*$$ be a prefix code. Kraft's inequality states:

**Theorem (Kraft's Inequality, the inequality part).**
\\[ \sum_{s \in S} |T|^{-\abs{C(s)}} \leq 1. \\]

For ostensive simplicity, I'll just prove this for case $$\abs{T} = 2$$. (The proof readily applies to general $$\abs{T}$$.)

My approach is a "stateful induction"[^2], manifested as the following
statement.

[^2]: There must be a more established term for this, but it doesn't occur to me now.

**Lemma.** Let $$d \geq 0$$. Let $$\iota \in T^d$$. Then
\\[ \sum_{\iota \preceq S(s)} |T|^{-|C(s)|} \leq 1. \]]

*Proof.* By reverse induction on $$d$$.

Case $$d > \max_{s \in S} |C(s)|$$. Then $$\text{LHS} = 0 < \text{RHS}$$, as is sufficient.

Case $$d \leq \max_{s \in S} |C(s)|$$. I'll analyse this case into three
exhaustive subcases.

Subcase 1: there is no $$s \in S$$ with $$\iota \preceq C(s)$$. Then
$$LHS = 0 < RHS$$, as is sufficient.

Subcase 2: there is an $$s \in S$$ with $$\iota = C(s)$$. Since $$C$$ is a
prefix code, $$s$$ is in fact the only element in $$S$$ with
$$\iota \preceq C(s)$$. Therefore $$LHS = 2^{-|C(s)} = RHS$$, as is sufficient.

Subcase 3: there are $$s \in S$$ with $$\iota \precneq C(s)$$. Note
that this case is disjoint from Subcase 3, because $$C$$ is a prefix
code. Thus
\\[
\{s \in S \mid \iota \preceq C(s)\}
=
\{s \in S \mid \iota \preceq C(s){:}0 \}
\cup
\{s \in S \mid \iota \preceq C(s){:}1 \},
\\]
where the $$\cup$$ is a disjoint union.
Therefore, by induction, we have
\\[
\text{LHS}
=    sum_{s \in S, \iota{:}0 \preceq C(s)} 2^{-|C(s)|} +
     sum_{s \in S, \iota{:}1 \preceq C(s)} 2^{-|C(s)|}
\leq 2^{-(d+1)} + 2^{-(d+1)}
=    2^{-d}
=    \text{RHS}.
\\]
This completes the proof. □
