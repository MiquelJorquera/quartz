---
tags:  Maths/Algebra/Group_theory, Maths/Geometry/Differential_geometry
---
# Group action

A _(left) group action_ of the [group](Algebraic%20structure.md#^Group) $G$ on the set $X$ is a [binary operation](Operation.md#^Operation2) $·:G\times X\to X$ such that for all $g,h\in G,\ x\in X:$$$\begin{split}
I_G·x&=x\\
g(h·x)&=(gh)·x
\end{split}$$ ^GroupAction

A [group action](#^GroupAction) $·$ on $X$ is *faithful* if $g·x=x$ for all $x\in X$ implies $g=g_e.$  ^FaithfulAction

A [group action](#^GroupAction) $·$ on $X$ is *free* if $g·x=x$ for any $x\in X$ implies $g=g_e.$ I.e. only the identity element fixes points. ^FreeAction


A $G$*-space* $(X,·)_G$ is a set $X$  equipped with a [group action](#^GroupAction) $·$ of   $G$ on $X.$ ^G-space

A [G-space](#^G-space) $X$ is *homogeneous* if $G$   acts [transitively](Relation.md#^BinaryRelTransitive) on it.
I.e. any two points can be connected by a single action of $g\in G.$ ^HomogeneousG-space

A [G-space](#^G-space) $X$ is a *torsor*, or a *principal homogeneous space*, if $G$   acts [freely](#^FreeAction) and [transitively](Relation.md#^BinaryRelTransitive) on it.
I.e. any two points in $X$ are connected by a unique action of $g\in G.$ ^Torsor

The *$G$-orbit* $G·x$ of an element $x$ of a [G-space](#^G-space) $X$ is the set of elements in $X$ that can be reached by acting with $G$ on $x.$
The set of $G$-orbits of $X$ is written as $X/G$ ^G-orbit

---
# Ring action

A _(left) ring action_ of the [ring](Algebraic%20structure.md#^Ring) $(R,+_R,\times)$ on the [commutative](Algebraic%20structure.md#^CommGroup) [group](Algebraic%20structure.md#^Group) $(G,+)$ is a [binary operation](Operation.md#^Operation2) $·:R\times G\to G$ such that:$$\begin{split}
r·(g+ h)&=r·g+ r·h\\
(r+_R s)·g&=r·g+ s·g\\
(r\times s)·g&=r·(s·g)\\
I_R·g&=g
\end{split}$$
These axioms are mixed analogues of [distributivity](Operation.md#^Distributive) and [associativity](Operation.md#^Associativity). ^RingAction

An *$R$-module* $(M,+,·)_R$ is a [commutative](Algebraic%20structure.md#^CommGroup) [group](Algebraic%20structure.md#^Group) $(M,+)$ equipped with a [ring action](#^RingAction) $·$ of $R$ on $M.$ ^Module