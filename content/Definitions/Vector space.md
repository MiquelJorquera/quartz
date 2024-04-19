---
tags:  Maths/Algebra/Linear_Algebra
---
# Vector space

^9474c0

[[Algebraic structure#^Module|Module]] $(V,+,\frown)_F$, the elements of which are called *vectors*, over a [[Algebraic structure#^Field|field]] $(F,+_F,\times),$ the elements of which are called *scalars*.
Set $V$ with two [[Operation#^Operation|operations]] $+:V\times V\to V$ (addition), and $\frown:F\times V\to V$ (scaling) such that:
- $(V,+)$ is a [[Algebraic structure#^CommGroup|commutative]] [[Algebraic structure#^Group|group]]
- $\exists$ a multiplicative [[Operation#^Inverse|identity]] $1v=v$
- Compatibility: $\begin{split}(a\times b)v &= a(bv)\\ (a+_F b)v &= av + bv\end{split}$
- Distributivity: $a(v + w) = av + aw$ 

$F$ is an $F$-vector space, so the two pairs of operations coincide.  
Note that that scaling is a [[Linear map#^BilinearMap|bilinear map]].

---
# Affine spaces

An *affine space* associated with the [vector space](#Vector%20space) $\vec{A}\equiv(A,+,\frown)_F$ is a [torsor](Action.md#^Torsor) $(A,+)_{\vec{A}}.$
Essentially, a vector space without an origin. ^AffineSpace

An *affine combination* of [vectors](#^Vector) $v_i\in V$ is a [linear combination](#^LinearCombination) $\sum_i k_i v_i$ such that $\sum_i k_i=1.$ ^AffineCombination

A *convex combination* of [vectors](#^Vector) $v_i\in V$ is an [affine combination](#^AffineCombination) $\sum_i k_i v_i$ such that $k_i$ are non-negative. ^ConvexCombination

---
# Types of vector spaces

A *coordinate space* is an $F$-[[#Vector space|vector space]] $F^n,$ whose [[Vector space#^Vector|vectors]] are $n$-tuples of [[Vector space#^Scalar|scalars]] in $F$ ^CoordinateSpace

A *symplectic space* $(V,ω)$ is an $F$-[[#Vector space|vector space]] $V$ equipped with a [[Linear map#^SymplecticForm|symplectic form]] $ω:V\times V\to F.$ ^SymplecticSpace

A *linear subspace* of a [[#Vector space|vector space]] $(V,+,\frown)_F,$  is a vector space $(W,+,\frown)_F$ such that $W\subseteq V,$ and which is [[Operation#^Closed|closed]] under $+$ and $\frown.$ ^Subspace

A *vector line* is a 1D [vector subspace](#^Subspace). ^VectorLine

An *invariant subspace* of an [[Morphisms#^Endomorphism|endomorphism]] $T:V\to V$ on a [[#Vector space|vector space]] $V$ is a [[#^Subspace|subspace]] $V'\subseteq V$ which is preserved by $T$:  
$$T(V')\subseteq V'$$ ^InvariantSubspace
## Normed spaces

A *normed space* is a $\mathbb K$-[[#Vector space|vector space]] equipped with a [[Function#^Norm|norm]]. ^Normed

The *parallelogram law* states that in a [[#^Normed|normed space]],$$|x+y|^2+|x-y|^2=2|x|+2|y|$$ ^ParallelogramLaw
### Inner product spaces

An *inner product space*, or *pre-Hilbert space*, is a $\mathbb K$-[[#Vector space|vector space]] equipped with an [[Linear map#^InnerProduct|inner product]]. ^InnerProd

Two [[#^Subspace|subspaces]] $V_1,V_2\subseteq V$ of an [[Vector space#^InnerProd|inner product space]] $V$ are *orthogonal* if all their vectors $v_1\in V_1$ and $v_2\in V_2$ are [[#^Orthogonal|orthogonal]]. ^OrthogonalSubspace

#### Hilbert spaces

A *Hilbert space* is a [[Metric#^Complete|complete]] [[Vector space#^InnerProd|inner product space]]. ^Hilbert

Every Hilbert space is a [[Vector space#^Banach|Banach space]].
Completeness is not strictly necessary for QM: Instead of working with square-integrable functions, you'd work with [[Function#^ContinuousFunction|continuous functions]] (which is nicer), but then limits of solutions may not live in the same space (which is annoying).

A *Banach space* $(B,\lvert ·\rvert)$ is a [[Metric#^Complete|complete]] [[Function#^Norm|normed space]]. ^Banach

An *$L^p$-space* is a space of [[Function#^Function|functions]] with finite [[Function#^LpNorm|$L^p$-norm]].
$(L^p,\|·\|_p)$ is a [[#^Banach|Banach space]]. For $p=2,$ it is a [[#^Hilbert|Hilbert space]]. ^LpSpace

---
# Vector space accessories

A *vector* is an element of a [[#Vector space|vector space]]. ^Vector

A *scalar* of an $F$-[[#Vector space|vector space]] is an element of the [[Algebraic structure#^Field|field]] $F.$ ^Scalar

A *linear combination* of [vectors](#^Vector) $v_i\in V$ in an $F$-[vector space](#Vector%20space) $V$ is a vector given by $\sum_i k_iv_i,$ where $k_i\in F.$ ^LinearCombination

A set $v_i$ of [[#^Vector|vectors]] is *linearly independent* if the only [[#^LinearCombination|linear combination]] to result in the zero vector, $\sum_ik_iv_i=\vec{0},$ is given by $k_i=0.$ ^LinearIndependence

A *(Hamel) basis* of a [[#Vector space|vector space]] $V$ is a [[Set#^Subset|subset]] $B\subseteq V$ of [[#^LinearIndependence|linearly independent]] [[#^Vector|vectors]] which [[#^Span|span]] $V.$ I.e. $\text{span}(B)=V.$ ^Basis

The *span* $\text{span}(S)$ of a [[Set#^Subset|subset]] $S\subseteq V$ of [[#^Vector|vectors]] of a [[#Vector space|vector space]] $V$ is the [[Set#^Intersection|intersection]] of all [[#^Subspace|subspaces]] of $V$ that contain $S.$ ^Span

A *unit vector* is a [[#^Vector|vector]] whose [[Function#^Norm|norm]] is 1. ^UnitVector

Two [[#^Vector|vectors]] $u,v$ in an [[#^InnerProd|inner product space]] are *orthogonal* if $\langle u,v \rangle=0.$ ^Orthogonal

Two [[#^Vector|vectors]] $u,v$ are *orthonormal* if they are [[#^Orthogonal|orthogonal]] [[#^UnitVector|unit vectors]]. ^Orthonormal

An *orthonormal basis* for an [[#^InnerProd|inner product space]] $V$ with finite dimension is a [[#^Basis|basis]] for $V$ whose [[#^Vector|vectors]] are mutually [[#^Orthonormal|orthonormal]].
For infinite-dimensional $V,$ it is a set $B$ of vectors such that every $v\in V$ can be written as an infinite [[#^LinearCombination|linear combination]] of vectors in $B.$ It is not a Hamel basis, because $\text{span}(B)$ may not be $V,$ but a dense [[Vector space#^Subspace|subspace]] of $V.$ ^OthonormalBasis

The *(algebraic) dual space* of a [[#Vector space|vector space]] $(V,+,\frown)_F$ is a vector space $(V^*,+,\frown)_F$ where $V^*$ is the set of all [[Linear map#^LinearForm|linear forms]] on $V.$ ^DualSpace

The *(algebraic) predual space* of a [[#Vector space|vector space]] $V$ is a vector space $W$ whose [[#^DualSpace|dual space]] is $W^*=V.$ ^PredualSpace

The *projective space* $PV$ of a $F-$[vector space](#Vector%20space) $V$ is the [set](Set.md#Set) of [equivalence classes](Relation.md#^EquivalenceClass)
$$(V-\{0\})/\sim$$
where $v\sim w$ if $v=λw$ for some $λ\in F.$
If $V$ is a [coordinate space](#^CoordinateSpace) $F^n,$ the notation usually becomes $FP^n,$ as in $\rr P^3.$ ^ProjectiveSpace