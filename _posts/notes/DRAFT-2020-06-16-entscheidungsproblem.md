---
layout: post
date: 2020-06-16 10:00 KST
author: Sori Lee
---

# Entscheidungsproblem

## Undecidability of the halting problem

The \emph{halting problem} is a decision problem that, as a mathematical function, assigns to each computer program $$e$$ and input data $$x$$ a truth value $$H(e, x)$$ telling whether or not $$e$$ terminates.

Turing, in his Entscheidungsproblem paper (1936), proved that the halting problem was undecidable. It was one of the first problems to be proved undecidable; Alonzo Church too proved, in *his* Entscheidungsproblem paper (1936), undecidability results in terms of lambda calculus.

The undecidability of the halting problem has a simple proof, which I will now outline.

Notations:
- Let $f\: X \pto Y$ be a partial function, and let $x \in X$. We write $f(x)\up$ if $f$ is undefined on $x$, and write $f(x)\down$ if $f$ is defined on $x$.
- Le

Let $$D\: \N \to \N$$ be a function that satisfies
\\[
    D(e) = true if H(e, e) = false, false otherwise
\\]

If $$H$$ were computable, then we could surely construct a computer program $$d$$ that computed $$D$$. Asking the question whether $$d$$ terminates on $$d$$ leads us to a contradiction:
\\[
d \down d \Leftrightarrow \neg H(d,d) \Leftrightarrow d \up d.
\\]
It follows that $$H$$ is not computable. ∎

## Undecidability of the Entscheidungsproblem

**Corollary (Undecidability of the Entscheidungsproblem).** The logical consequence relation of first-order logic is undecidable.

Here's a proof outline. 

The idea 

the formula

"The program e terminates on input x" or "$$H(e,x) = \true$$"

"this 


