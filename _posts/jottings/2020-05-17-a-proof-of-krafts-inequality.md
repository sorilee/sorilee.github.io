---
layout: post
date: 2020-05-17 13:23 KST
author: Sori Lee
---

# A proof of Kraft's inequality

In coding theory, Kraft's inequality is a fundamental (in fact, characterising)
property of prefix codes. The theorem in fact generalises to uniquely decodable
codes, in which case it goes by the name of Kraft-McMillan inequality. In what
follow, I work out a proof of the inequality for prefix codes.

**Definition.** Let $$
\newcommand{\:}{\colon}
\newcommand{\abs}[1]{\left\lvert#1\right\rvert}
\newcommand{\LHS}{\text{LHS}}
\newcommand{\RHS}{\text{RHS}}
\newcommand{\im}{\mathop{\rm im}\nolimits}
S$$ and $$T$$ be finite sets (alphabets). A *prefix code* is a function
$$C\: S \to T^*$$ such that for $$s,s' \in S$$, if $$C(s) \preceq C(s')$$ then
$$s = s'$$.[^1]

[^1]: Here, $$T^*$$ is the Kleene star (i.e. the set of strings in $$T$$), and
      $$C(s) \preceq C(s')$$ denotes that $$C(s)$$ is an initial segment (or
      *prefix*) of $$C(s')$$.

Let $$C\: S \to T^*$$ be a prefix code. Kraft's inequality states:

**Theorem (Kraft's inequality, the forward direction[^2]).**
\\[ \sum_{s \in S} \abs{T}^{-\abs{C(s)}} \leq 1. \\]

[^2]: There is a converse to this statement, which I'm not bothered with today.

I'll just prove this for case $$\abs{T} = 2$$, for the sake of imaginational[^3]
and notational simplicity. The proof readily adapts to general $$\abs{T}$$.

[^3]: For $$\abs{T} = 2$$, $$\im(C)$$ is a binary tree, which I find easier to
      visualise.

My strategy is a "stateful induction"[^4], as manifested in the following
statement.

[^4]: There must be a more established term for this, but I can't recall one
      now.

**Lemma.** Let $$d \geq 0$$ and $$\iota \in T^d$$. Then
\\[ \sum_{\iota \preceq S(s)} 2^{-\abs{C(s)}} \leq 2^{-d}. \\]

Note that the Theorem is just a special case of the Lemma for $$\iota = ()$$.

*Proof.* By reverse induction on $$d$$.

Case $$d > \max_{s \in S} \abs{C(s)}$$. Then $$\LHS = 0 < \RHS$$, as desired.

Case $$d \leq \max_{s \in S} \abs{C(s)}$$. I'll analyse this case into three
exhaustive subcases.

Subcase 1: there is no $$s \in S$$ with $$\iota \preceq C(s)$$. Then
$$\LHS = 0 < \RHS$$, as desired.

Subcase 2: there is an $$s \in S$$ with $$\iota = C(s)$$. Since $$C$$ is a
prefix code, $$s$$ is in fact the only element in $$S$$ with
$$\iota \preceq C(s)$$. Therefore $$\LHS = 2^{-\abs{C(s)}} = \RHS$$, as desired.

Subcase 3: there are $$s \in S$$ with $$\iota ⪱ C(s)$$. Note that this case is
disjoint from Subcase 3, because $$C$$ is a prefix code. Thus
\\[
\\{s \in S \mid \iota \preceq C(s)\\}
=
\\{s \in S \mid \iota \preceq C(s){:}0 \\}
\cup
\\{s \in S \mid \iota \preceq C(s){:}1 \\},
\\]
where the colon ($$:$$) denotes concatenation and wherein the union, note, is
disjoint. Therefore, by induction, we have
\\[
\LHS
=    \sum_{
       \substack{s \in S, \\\\ \iota{:}0 \preceq C(s)}
     } 2^{-\abs{C(s)}}
     +
     \sum_{
       \substack{s \in S, \\\\ \iota{:}1 \preceq C(s)}
     } 2^{-\abs{C(s)}}
\leq 2^{-(d+1)} + 2^{-(d+1)}
=    \RHS.
\\]
This completes the proof. ∎
