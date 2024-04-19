---
tags:  Maths/Algebra/Group_theory
---
A *linear representation* $R$ of a [[Algebraic structure#^Group|group]] $G$ on an $F$-[[Vector space#Vector space|vector space]] $V$ is a [[Morphisms#^Homomorphism|homomorphism]]
$$R:G\to GL(V)$$
where $V$ is the *representation space* and $n=\dim V$ is the *dimension* of the representation.
It is common to choose a [[Vector space#^Basis|basis]] for $V$ and identify $GL(V)$ with $GL(n,F)$, the group of $n\times n$ [[Operation#^Inverse|invertible]] matrices on the [[Algebraic structure#^Field|field]] $F$. ^Rep

A [[Linear representation#^Rep|representation]] is *faithful* if it is [[Morphisms#^Monomorphism|injective]]. ^FaithfulRep

A [[Linear representation#^Rep|representation]] $R$ is *trivial* if $R(g) = I$ for all $g\in G.$ ^TrivialRep

A [[Linear representation#^Rep|representation]] $U:G\to GL(\H)$ on a complex [[Vector space#^Hilbert|Hilbert]] representation space $\H$ is *unitary* if $U(g)$ is a [[Linear map#^UnitaryOperator|unitary operator]] for all $g\in G.$
The theory is well-developed for [[Topology#^LocCompTopoGroup|locally compact]] [[Topology#^TopoGroup|topological groups]] $G$, and [[Function#^StronglyContinuousFunction|strongly continuous]] $U.$ ^UnitaryRep

A *subrepresentation* of a [[#^Rep|representation]] $R:G\to GL(V)$ is a representation $R':G\to GL(V')$ whose representation space $V'$ is a $G$-[[Vector space#^InvariantSubspace|invariant subspace]] of $V.$ ^Subrep

A [[Linear representation#^Rep|representation]] is *irreducible* if it is nonzero, and doesn't have any proper non-[[#^TrivialRep|trivial]] [[#^Subrep|subrepresentations]]. ^Irrep

The *adjoint representation*  $\operatorname{ad}$  of a finite-dimensional [Lie algebra](Algebraic%20structure.md#^LieAlgebra)  $\g$  with elements  $X,Y\in\g$  is defined by$$\begin{split}
\operatorname{ad}:\g&\to\mathfrak{gl}(\g)\\
X&\mapsto \operatorname{ad}_X\\
\operatorname{ad}_X(Y)&=[X,Y]
\end{split}$$ If  $\g$  is infinite-dimensional, then  $\operatorname{ad}:\g\to \mathrm{End}(\g)$.  ^AdjointRep

