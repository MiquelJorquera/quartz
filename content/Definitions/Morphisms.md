---
tags:  Maths/Algebra
---
A *morphism* is a structure-preserving map $f$ from one mathematical structure $X$ to another $Y$ of the same type (i.e. name).
It is usually written $f:X\to Y.$ When several are involved, it can be written as $X\xrightarrow{f}Y.$ If only one is involved and doesn't need to be referred to again, we may simply write $X\to Y.$ ^Morphism
 
An *endomorphism* is a [[#^Morphism|morphism]] $f:X\to X$ from a mathematical structure to itself. ^Endomorphism

An *isomorphism* is a [[#^Morphism|morphism]] $f$ with a (two-sided) [inverse](Function.md#^InvertibleFunc) $f^{-1}$ that is also a morphism. ^Isomorphism

An *automorphism* is an [[#^Endomorphism|endomorphism]] that is also an [[#^Isomorphism|isomorphism]]. ^Automorphism

A *homomorphism* is a [[#^Morphism|morphism]] $f:X\to Y$ between [[Algebraic structure#Algebraic structure|algebraic structures]], that preserves all [[Operation#^Operation|operations]]: $f(a*b)=f(a)*f(b).$ ^Homomorphism

An *embedding, or* *monomorphism*, $X\hookrightarrow Y$ is an injective [[#^Homomorphism|homomorphism]].
This describes a mathematical structure being contained in another (e.g. [[Algebraic structure^Subgroup|subgroups]] are [[Algebraic structure#^Group|groups]] in groups).
Different embeddings are possible for the same two structures (e.g. depending on how you embed the $\mathbb Z$ into $\rr,$ you get $\mathbb Z$ or $2\mathbb Z$) ^Monomorphism

An *epimorphism* $X\twoheadrightarrow Y$ is an surjective [[#^Homomorphism|homomorphism]]. ^Epimorphism

An *bimorphism* $X\hooktwoheadrightarrow Y$ is a bijective [[#^Homomorphism|homomorphism]]. ^Bimorphism

The *kernel* of a [[#^Homomorphism|homomorphism]] is the pre-[[Function#^RangeImage|image]] of the [[Operation#^Identity|identity]]. ^Kernel

A *homeomorphism* is an [[#^Isomorphism|isomorphism]] of [[Topology#^TopoSpace|topological spaces]].
Equivalently, it is a [continuous](Function.md#^ContinuousFunction) [bijection](Function.md#^BijectiveFunc) with a continuous [inverse](Function.md#^InvertibleFunc).
It preserves [[Topology#^OpenSet|open]]/[[Topology#^ClosedSet|closed]] sets. ^Homeomorphism

An *isometry* $f:M\to N$ is a [bijection](Function.md#^BijectiveFunc) of [[Metric#^MetricSpace|metric spaces]] $(M,g)$ and $(N,h)$ that preserves distances:$$g(x,y)=h(f(x),f(y))$$for all $x,y\in M.$
Isometries are [homeomorphisms](Morphisms.md#^Homeomorphism).  ^Isometry

A *derivation* $D:X\to X$ is an [[#^Endomorphism|endomorphsim]] that obeys Leibniz's rule: $D(xy)=D(x)y+xD(y).$ ^Derivation

A *Lie derivative* $\L_X(T)$ is a [derivation](#^Derivation) of the [tensor algebra](Algebraic%20structure.md#^TensorAlgebra) $T,$ with respect to a vector field $X.$ Its axioms are:
$$\begin{split}
\L_X(f)&=X(f)=X^μ\p_μ f\\
\L_X(T\otimes S)&=(\L_X T)\otimes S + T\otimes (\L_X S)\\
\L_X(T(V)) &= (\L_X T)(V) + T(\L_X V)\\
[\L_X,d]&=0
\end{split}$$
In index notation:
$$\L_X(T^a_b) = X^c\p_c T^a_b - T^c_b\p_c X^a + T^a_c\p_b X^c$$ ^LieDerivative

A *diffeomorphism* is an [[#^Isomorphism|isomorphism]] of [[|differentiable manifolds]]. ^Diffeomorphism



