---
layout: post
author: Sori Lee
---

# Unification algorithm

I describe a unification algorithm for first-order languages.

To unify two terms $$t_1$$ and $$t_2$$ is to find a unifier $$\sigma$$ such that $$t_1 \sigma = t_2 \sigma$$. In the light of the last equation, let us refer to the pair $$(t_1, t_2)$$ as a *term equation*.

**Algorithm (Unification).**

Input: a set $$\{(t_1, u_1), \ldots, (t_n, u_n)\} of term equations, $$n \geq 0$$.

Output: 
