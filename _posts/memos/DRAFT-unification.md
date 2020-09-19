**Theorem (Soundness of Resolutional Refutation).** Let $$\Gamma$$ be a finite
set of formulas. If $$\Gamma$ is resolutionally refutable, then $\Gamma$ is
unsatisfiable.

Note that this is evidently 
Note that the statement is evidently equivalent to saying the 

**Proposition (Soundness of Resolutional Refutation).. 


- Let $$\Gamma$$ be a finite set of formulas and $$\phi$$ be a formula.

 If
  $$\Gamma \vdash^{\text{resolution}} \phi$$, then $$\Gamma \models \phi$$.



Let $$ $$

<indent>Given a formula </indent>

<center>$$\Gamma \vdash^{\text{res}} ,</center>
whence 

# Resolution in First-Order Logic



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
