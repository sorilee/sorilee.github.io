---
layout: post
date: 2020-07-17 KST
author: Sori Lee
---

# The lambda terms

**Definition.** Fix a set of *variables*. The *λ-terms* are defined by induction as follows.

   1. Each variable is a λ-term, called an *atom*.

   2. If $$M$$ and $$N$$ are λ-terms, then the pair written $$MN$$ is a λ-term called an *application*.

   3. If $$x$$ is a variable and $$M$$ is a λ-term, then the pair written $$\lambda x . M$$ is a λ-term called an *abstract* or *λ-abstract*.

A *composite* λ-term is a λ-term that is not an atom.

**Notation.** The triple bar sign ($$\equiv$$) is used to denote so-called *syntactic equality* of λ-terms in literature ([Hindley], p.~xx; [BDS], p.~1).

For example, the left-associative convention for applications may be examplified by writing:
\\[
LMN \equiv (LM)N.
\\]
