---
tags:
  - Maths/Algebra/Group_theory
---
# Lagrange's theorem

If $(H,·)$ is a [subgroup](Algebraic%20structure.md#^Subgroup) of $(G,·),$ then the [order](Algebraic%20structure.md#^GroupOrder) of $(H,·)$ divides the order of $(G,·):$
$$(H,·)\leq (G,·)\implies \frac{|G|}{|H|}\in\mathbb{N}$$
This holds for infinite groups.

This implies that $(G,·)$ gets divided into disjoint, equal-sized [cosets](Algebraic%20structure.md#^Coset) of $(H,·):$ [Picture](foo.png)

Multiplying by an element $g_i'\neq g_i$ in the coset $g_iH$ gives an element in $g_iH:$
$$\begin{split}
g_i'·h_j&=g_i·h_k\\
g_i'&=g_i·(h_k·h_j^{-1})\in g_1H\\
\end{split}$$