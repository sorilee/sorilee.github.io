---
layout: post
date: 2020-07-19 KST
date created: 2020-07-17 KST
author: Sori Lee
---

# The lambda calculus: how authors define it

<!--
### A note on its origin: Church 1932 vs Church 1936

A lambda-calculus formalism makes its first appearance in Church [C32].
......
-->

### Lambda terms and their identity

The lambda calculus is a formal system with a single "kind" of expressions, unlike for instance predicate logics in which there are two kinds -- terms and formulas. The expressions of the lambda calculus are commonly called λ-terms.[^1]

[^1]: Church [C36] originally called them formulas.

**Definition.** Choose a denumerable set of *variables*. A *λ-term* is defined inductively as follows.

   1. Each variable is a λ-term, called an *atom*.

   2. If $$M$$ and $$N$$ are λ-terms, then the pair written $$MN$$ is a λ-term called an *application*.

   3. If $$x$$ is a variable and $$M$$ is a λ-term, then the pair written $$\lambda x{.}M$$ is a λ-term called an *abstract* or *λ-abstract*.

<!-- A *composite* λ-term is a λ-term that is not an atom. -->

<!-- Note. Took brief looks at Church 1932 and Church 1936 too, but couldn't quickly discern whether those definitions (esp. the 1936 one which is said to be the untyped lambda calculus) agree with the above as well. -->

<!-- All major (modern) references I know, in particular [B84], [H94] and [BDS13], virtually give the above as the definition of a λ-term[^1] *per se*. By *per se* I mean without regard to which λ-terms to identify as the same, that is, how to define their *syntactic equality*. -->

**Note.** Church [C36] originally stipulates that the infinite set of variables be countable. Some authors, including [H97] and [BDS13], are more explicit than others, such as [B84], in requiring the countability. Some author, [S13], simply doesn't require it.

All notable references I know, including [C36], [B84], [H97], [BDS13] and [S13], give virtually the above as the defining clauses of a λ-term. However, authors differ over whether or not <!--/ how--> to identify some of these inductively introduced objects as the same λ-terms.



......

<!-- People nevertheless seem to agree over the notation. -->

**Notation.** The triple bar sign ($$\equiv$$) is used to denote the syntactic equality of λ-terms in literature ([B84], Notation 2.1.2(iv); [H97], p. xx; [BDS13], p. 1).

For example, the left-associative convention of the applicative notation may be examplified as:
\\[
LMN \equiv (LM)N.
\\]

**Remark.** Some authors, notably [B84] (Convention 2.1.12) and [BDS13] (Remark 1A.7), adopt the position that α-conversion is part of the syntactic equality of λ-terms. 

### Beta and eta in equational lambda calculus

When one is to regard the lambda calculus as an equational theory, the beta and eta conversions are taken as axioms:

- The *beta* axiom:
  \\[
  (\lambda x{.}M)N = M[N/x]
  \\]
  for all $$x$$, $$M$$ and $$N$$.
 
- The *eta* axiom:
  \\[
  \lambda x{.}Mx = M
  \\]
  if $$x \notin \textrm{FV}(M)$$ for all $$x$$ and $$M$$.

Reference: [BDS13], Definition 1A.4.

### References

- [B84]
- [H97]
- [BDS13]
