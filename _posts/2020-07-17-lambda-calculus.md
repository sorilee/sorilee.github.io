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

   1. Each variable $$x$$ induces a λ-term just written $$x$$, an *atom*.

   2. Each pair of λ-terms $$M$$ and $$N$$ induces a λ-term written $$MN$$, an *application*.

   3. Each pair of a variable $$x$$ and a λ-term $$M$$ induces a λ-term written $$\lambda x{.}M$$, an *abstract* or *λ-abstract*.[^2]

[^2]: I took this terminology from [H97], Definition 1A1, (iii).

**Note.** Church [C36] originally stipulates that the infinite set of variables be countable. Some authors, including [H97] and [BDS13], are more explicit than others, such as [B84], in requiring the countability. Some author, [S13], simply doesn't require it.

All notable references I know, including [C36], [B84], [H97], [BDS13] and [S13], give virtually the above as the inducing clauses of a λ-term. Authors just differ over whether or not to identify the α-convertibles: in [C36], [H97] and [S13] a λ-term is just a 'raw' λ-term, whereas in [BDS13] and less explicitly in [B84] it is an equivalence class under α-conversion.
*Personalia:* I'm inclined to the former choice (whence the definition above), particularly for the sake of not lessening the simplicity of the notion.

Regardless of this fine difference in the notion, a notable notation is used in a common way across modern literature:

**Notation.** The equality of λ-terms is denoted by the triple bar '$$\equiv$$' (instead of the usual double bar '$$=$$'), and may be referred to as their *syntactic* equality.[^3]

[^3]: [B84], Notation 2.1.2(iv); [H97], Notation 1A1.1; [BDS13], p. xx and Remark 1A.7; [S13], p. 13.

As an example of the use of this notation, the left-associative convention of the applicative juxtaposition can be examplified as:
\\[
LMN \equiv (LM)N.
\\]

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
