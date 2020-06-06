---
layout: post
date: 2020-06-03 14:36 KST
author: Sori Lee
---

# Resolution in First-Order Logic

## Entailment relations

First, I want to introduce by examples the concept of *entailment* (or *consequence*) relations.^[1] This is because central to what we shall do today are comparisons of entailment relations. 

[1]: For a deeper account of this concept, see e.g. [the IEP article](https://www.iep.utm.edu/logcon/).

Given a formal language, an entailment relation for us is a binary relation between a set of expressions (in the language) and an expression, that in one way or another models the notion that the latter expression is a logical consequence of the expressions in the former set.

Examples. In propositional or first-order logic, a notion of a proof (such as natural deduction) defines the 'provability' relation $$\vdash$$, the prototypical example of a 'syntactic' entailment relation. On the other hand, a semantics for such a logic defines the semantic entailment relation $$\models$$, given by: $$\Gamma \models \phi$$ if and only if $$M \models \phi$$ for all models $$M$$ of $$\Gamma$$.

These examples are also the environment for the prototypical example of a comparison of entailment relations: soundness and completeness. A formal language endowed with a deductive apparatus may be referred to as a *deductive system*.^[2] A semantics for the underlying language of 


Of caution is the fact that there are two concepts of 'semantics' afloat that be better distinguished. One is the negative sense: semantics is something non-syntactic. Another is..... interpre ...




$$
\newcommand{\:}{\colon}
\newcommand{\abs}[1]{\left\lvert#1\right\rvert}
\newcommand{\LHS}{\text{LHS}}
\newcommand{\RHS}{\text{RHS}}
\newcommand{\im}{\mathop{\rm im}\nolimits}
S$$

## Refutation-completeness

A "formal system" $$S$$ is *(strongly) complete* if
\\[
\Gamma \models_S \varphi \text{ implies } \Gamma \vdash_S \varphi.
\\]
for all theories $$\Gamma$$ and formulas $$\varphi$$ in $$S$$.

A "formal system" $$S$$ is *refutationally complete* if
\\[
\Gamma \models_S \bot \text{ implies } \Gamma \vdash_S \bot.
\\]
for all theories $$\Gamma$$ in $$S$$.

When explaining the refutational completeness, people often remark along the
following lines:

> ... strong completeness means that, given a formula set $$\Gamma$$, it is
> possible to compute every semantical consequence $$\varphi$$ of $$\Gamma$$,
> while refutation completeness means that, given a formula set $$\Gamma$$ and
> $$\varphi$$, it is possible to check whether $$\varphi$$ is a semantical
> consequence of $$\Gamma$$.
>
> https://en.wikipedia.org/wiki/Completeness_(logic)#Refutation_completeness

I construe this as saying the following. First, an implicit assumption they are
making is that $$S$$ is a sound system. Now, since $$\im(\Gamma \vdash)$$ is
(obviously) c.e., if $$S$$ is (strongly) complete, then
$$\Thm_S(\Gamma) = \im(\Gamma \vdash)$$ is c.e.. However, when $$S$$ is merely
refutationally complete, then that conclusion cannot be drawn. Nevertheless, for
a given formula $$\phi$$, since $$\Gamma, \neg \varphi \vdash_S \bot$$ can
always be decided, 


when a "formal system" is strongly complete, then
$$\Thm(\Gamma) $$ 

