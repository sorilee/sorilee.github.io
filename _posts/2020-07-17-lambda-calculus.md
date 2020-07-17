---
layout: post
date: 2020-07-17 KST
author: Sori Lee
---

# The lambda calculus: how authors define it

### Lambda terms

**Definition.** Fix a set of *variables*. The *λ-terms* are defined by induction as follows.

   1. Each variable is a λ-term, called an *atom*.

   2. If $$M$$ and $$N$$ are λ-terms, then the pair written $$MN$$ is a λ-term called an *application*.

   3. If $$x$$ is a variable and $$M$$ is a λ-term, then the pair written $$\lambda x . M$$ is a λ-term called an *abstract* or *λ-abstract*.

<!-- A *composite* λ-term is a λ-term that is not an atom. -->

All major references I know, in particular [B1984], [Hindley] and [BDS], virtually give the above as the definition of a λ-term[^1] *per se*. By *per se* I mean without regard to which λ-terms to identify as the same, that is, how to define their *syntactic equality*.

[^1]: that is, a term in the (untyped) lambda calculus

**Notation.** The triple bar sign ($$\equiv$$) is used to denote the syntactic equality of λ-terms in literature ([B1984], Notation 2.1.2(iv); [Hindley], p. xx; [BDS], p. 1).

For example, the left-associative convention of the applicative notation may be examplified as:
\\[
LMN \equiv (LM)N.
\\]

**Remark.** Some authors, notably [B1984] (Convention 2.1.12) and [BDS] (Remark 1A.7), adopt the position that α-conversion is part of the syntactic equality of λ-terms. 

### Beta and eta in equational lambda calculus

When one is to regard the lambda calculus as an equational theory, the beta and eta conversions are taken as axioms:

- The *beta* axiom:
  \\[
  (\lambda x . M)N = M[N/x]
  \\]
  for all $$x$$, $$M$$ and $$N$$.
 
- The *eta* axiom:
  \\[
  \lambda x . Mx = M
  \\]
  if $$x \notin \textrm{FV}(M)$$ for all $$x$$ and $$M$$.

Reference: [BDS], Definition 1A.4.
