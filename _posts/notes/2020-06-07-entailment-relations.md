---
layout: post
date: 2020-06-07 04:30 KST
author: Sori Lee
---

# Entailment relations

*This is a piece on entailment relations that I prepared as a preliminary to an explanation of the propositional resolution.*

Central to the basic discussions of resolution are its soundness and completeness. Soundness and completeness are a recurring theme in logic, which in many cases are manifested as a comparison between two of so-called entailment relations.

I will first give (well, attempt) a general description of the concept of an entailment relation, then go definite and give standard examples in propositional/first-order logic.

Given a formal language, an *entailment relation* (or *consequence relation*) is a binary relation between a set of expressions (in the language) and an expression, that in one way or another models the notion that the latter expression is a logical consequence of the expressions in the former set.[^1]

[^1]: For a more comprehensive account of this concept, see e.g. [the IEP article](https://www.iep.utm.edu/logcon/).

Fix a propositional or first-order language. Recall that a set of formulas $$\Gamma$$ *proves* a formula $$\phi$$, or $$\Gamma \vdash \phi$$, if there exists a (say natural-deduction) proof whose conclusion is $$\phi$$ and all of whose hypotheses are from $$\Gamma$$. This is the archetypical example of a "syntactic" entailment relation.

On the other hand, recall that $$\phi$$ is *(semantically) valid* in $$\Gamma$$, or $$\Gamma \models \phi$$, if $$M \models \phi$$ (i.e. $$\phi$$ is true in $$M$$) for every model $$M$$ of $$\Gamma$$.[^2] This, in turn, is the archetypical example of a "semantic" entailment relation.

[^2]: Note the two distinct uses of the notation $$\models$$.

*The* soundness and completeness of propositional or first-order logic are the statements that simply compare these two entailment relations:

**Theorem (Soundness).** If $$\Gamma \vdash \phi$$, then $$\Gamma \models \phi$$.

It is called soundness in that the deductive apparatus (e.g. natural deduction, yielding $$\vdash$$) of the logic is 'sound' with respect to its standard semantics (which yields the $$\models$$).

**Theorem (Completeness).** If $$\Gamma \models \phi$$, then $$\Gamma \vdash \phi$$.

Similarly, this is called completeness in that the deductive apparatus is 'complete' with respect to the standard semantics.

In general, logicians speak of soundness when a syntactic entailment relation implies a semantic entailment relation, and of completeness for the converse.

Propositional resolution, the subject of our discussions today, gives rise to another entailment relation of syntactic nature for propositional logic. A natural question henceforth to ask is whether it is also sound and complete with respect to the standard semantics, and it will turn out to be so.
