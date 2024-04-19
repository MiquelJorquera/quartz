---
tags:  Maths/Algebra/Linear_Algebra
---
# Linear maps

A *linear map* is a [[Morphisms#^Homomorphism|homomorphism]] $f:V\to W$ between two $F$-[[Vector space#Vector space|vector spaces]] which preserves addition and scaling:$$\begin{split}
f(u+v)&=f(u)+f(v)\\
f(λv)&=λf(v)
\end{split}$$ ^LinearMap

A *bilinear map* is a [[Operation#^Operation2|binary operation]] $·:V\times W\to X$ for three $F$-[[Vector space#Vector space|vector spaces]], which is [[#^LinearMap|linear]] in both arguments:$$\begin{split}
(u+v)·(w+x)&=u·w+u·x+v·w+v·x\\
(λv)·(μw)&=λμ(v·w)
\end{split}$$^BilinearMap

A *multilinear map* is an $n$-ary [[Operation#^Operation|operation]] $f:V_1\times V_2\times\dots\times V_n\to W$ on $n$ [[Vector space#Vector space|vector spaces]] over the same field $F,$ which is [[#^LinearMap|linear]] in each argument. ^MultilinearMap

An *antilinear map*, or *conjugate linear map*, is a [[Morphisms#^Homomorphism|homomorphism]] $f:V\to W$ between two $\mathbb K$-[[Vector space#Vector space|vector spaces]]  such that:$$\begin{split}
f(u+v)&=f(u)+f(v)\\
f(kv)&=\bar{k}f(v)
\end{split}$$ If $\mathbb K=\rr$, then $\bar{k}=k$ so an antilinear map is a [[#^LinearMap|linear map]]. ^AntilinearMap

A [[#^MultilinearMap|multilinear map]] $f:V\times V\times\dots\times V\to W$ is *alternating* if it yields zero whenever two arguments are equal. 
For $f$ [[#^BilinearForm|bilinear]], $f(v,v)=0.$ ^Alternating

A *Lie bracket* is a [[Operation#^Closed|closed]], [[#^Alternating|alternating]] [[Linear map#^BilinearMap|bilinear map]] $[\cdot,\cdot]:\mathfrak{g\times g\rightarrow g}$ on a [[Vector space#Vector space|vector space]] $\mathfrak{g},$ that obeys the [[Operation#^Jacobi|Jacobi identity]]: $[x,[y,z]]+[y,[z,x]]+[z,[x,y]]=0.$
If $\mathfrak g$ is a [[Vector space#^VectorField|vector field]], then $[x,y] = \L_x\ y.$ ^LieBracket

The *Poisson bracket* $\{·,·\}$ of phase space (and time) [[Function#^Function|functions]] $f,g,h$ is a [[#^LieBracket|Lie bracket]] which obeys [[Morphisms#^Derivation|Leibniz's rule]] $\{fg,h\}=\{f,h\}g+f\{g,h\}$.
In [[canonical coordinates]], it takes the form $$\{f,g\} = \pdv{ f}{ q_i}\pdv{ g}{ p^i} - \pdv{ g}{ q_i}\pdv{ f}{ p^i}$$ ^PoissonBracket

A *linear isometry* is a [bijective](Function.md#^BijectiveFunc) [linear map](Linear%20map.md#^LinearMap) $A:V\to W$ between [inner product spaces](Vector%20space.md#^InnerProd) that preserves inner products:$$\langle A u, Av\rangle_V = \langle u,v\rangle_U$$for all $u,v\in V$. Equivalently, $A^{\dagger}A=I_V.$
For [normed spaces](Vector%20space.md#^Normed), it preserves norms: $|Av|=|v|.$ ^LinearIsometry

A *unitary transformation* is a [closed](Operation.md#^Closed) [linear isometry](#^LinearIsometry) $U:V\to V.$ ^UnitaryTransformation

The *rank* of a [linear map](#^LinearMap) $f:V\to W$ is the dimension of its [image](Function.md#^RangeImage):$$\mathrm{rank}(f)=\mathrm{dim}(f(V))$$Intuitively, it is the number of independent linear constrains imposed by $V.$ ^Rank

A [linear map](#^LinearMap) $\f:C\to C$ on a [C<sup>*</sup>-algebra](Algebraic%20structure.md#^CstarAlgebra) $C$ is *unital* if it preserves the [identity element](Operation.md#^Identity) $I_C:$$$\f(I_C)=I_C$$ ^UnitalMap

A [linear map](#^LinearMap) $\f:A\to B$  between [C<sup>*</sup>-algebras](Algebraic%20structure.md#^CstarAlgebra) $A,B$ is *positive* if it preserves [positive-semidefiniteness](#^SemiPositiveOperator):$$a\geq 0\implies\f(a)\geq 0$$ ^PositiveMap

A [positive map](#^PositiveMap) $\f:A\to B$ is *$k$-positive* if the linear map $I_{\C^{k\times k}}\otimes \f:A^{k\times k}\to B^{k\times k}$ between the C$^*$-algebras of complex $k\times k$ matrices with entries in $A$ and $B,$ is [positive](#^PositiveMap). ^kPositiveMap

A [k-positive](#^kPositiveMap) map is *completely positive* if it is [positive](#^PositiveMap) for all $k.$ ^CompletelyPositiveMap

A [linear map](#^LinearMap) $\f:B(\H_1)\to B(\H_2)$ between [bounded operators](#^BoundedOperator) is *normal* if there is a bounded linear map $ψ:\T(\H_2)\to\T(\H_1)$ between [trace classes](#^TraceClass) such that$$\tr(B_1ψ(T_2))=\tr(T_2\f(B_1))$$for all $B_1\in B(\H_1), T_2\in\T(\H_2).$ ^NormalMap







---
# Forms

A *linear form*, *linear functional*, *1-form*, or *covector* $f:V\to F$ on an $F$-[[Vector space#Vector space|vector space]] $V,$ is a [[Function#^Form|form]] that is [[#^LinearMap|linear]].
A linear form in $V$ lives in the [dual space](Vector%20space.md#^DualSpace): $f\in V^*.$ ^LinearForm

A *bilinear form* $f:V\times V\to F$ on an $F$-[[Vector space#Vector space|vector space]] $V,$ is a [[Function#^Form|form]] that is [[#^BilinearMap|bilinear]]. ^BilinearForm

A *multilinear form*, or *$n$-linear form*, $f:V\times V\times\dots\times V\to F$ is a [[Function#^Form|form]] which is [[#^LinearMap|linear]] in each argument. ^MultilinearForm

A bilinear form $f:V\times V\to F$ is *non-degenerate* if for all $v\in V,$$$\big(f(u,v)=0\big)\implies\big(u=\vec{0}\big)$$ ^Nondegenerate

A *sesquilinear form* is a [[Operation#^Operation2|binary operation]] $f:V\times V\to \mathbb K$ for a $\mathbb K$-[[Vector space#Vector space|vector space]] $V,$ which is [[#^LinearMap|linear]] in one argument, and [[#^AntilinearMap|antilinear]] in the other:$$\begin{split}
f(u+v,w+x)&=f(u,w)+f(u,x)+f(v,w)+f(v,x)\\
f(kv,\ell w)&=\bar{k}\ell f(v,w)
\end{split}$$
If $\mathbb K=\rr$, then $\bar{k}=k$ so a sesquilinear form is a [[#^BilinearForm|bilinear form]]. ^SesquilinearForm

A *symplectic form* is a [[#^Nondegenerate|non-degenerate]], [[#^Alternating|alternating]] [[#^BilinearForm|bilinear form]]. ^SymplecticForm

An *inner product* is a [[Function#^PositiveDefiniteForm|positive-definite]], [[Linear map#^SesquilinearForm|sesquilinear form]] $\langle ·,·\rangle:V\times V\to \rr_{\ge0}$ which is *conjugate-symmetric*, or *Hermitian*:$$\langle u,v\rangle=\overline{\langle v,u\rangle}$$
It induces a canonical [[Function#^Norm|norm]] $|v|\equiv \sqrt{\langle v,v \rangle}.$ ^InnerProduct

---
# Distributions

 A *distribution* $T:D(U)\to C$ is a [continuous](Function.md#^ContinuousFunction) [linear form](#^LinearForm) ^Distribution

---
# Operators

A *linear operator* is a [[#^LinearMap|linear map]] $A:V\to W,$ which may or may not obey additional conditions, such as $V=W,$ the [[Vector space#Vector space|vector spaces]] being real, being function spaces, or its domain being a [linear subspace](Vector%20space.md#^Subspace) of $V.$ ^LinearOperator

A *bounded operator*, or *bounded linear map*, is an [[#^LinearOperator|operator]] $B:V\to W$ between [[Vector space#^Normed|normed spaces]] such that there is a bound $|B(v)|\leq |B||v|=k|v|$ for all $v\in V$ and some finite $k>0.$
They form a [C<sup>*</sup>-algebra](Algebraic%20structure.md#^CstarAlgebra), usually denoted $B(V)$ or $\L(V).$
If $V=W,$ the condition becomes $|BC|\leq|B||C|$ for all $B,C\in B(V).$ ^BoundedOperator

An [operator](#^LinearOperator) is *unbounded* if it is not [bounded](#^BoundedOperator). ^UnboundedOperator

An [operator](#^LinearOperator) is *continuous* iff it is [bounded](#^BoundedOperator). ^ContinuousOperator

An [[#^LinearOperator|operator]] $A:V\to V$ on an [[Vector space#^InnerProd|inner product space]] $V$ is *symmetric* if $\langle u,Av \rangle=\langle Au,v \rangle$ for all $u,v\in \dom(A)\subseteq V$ ^SymmetricOperator

A *positive (-definite) operator* is an [[#^LinearOperator|operator]] on an [[Vector space#^InnerProd|inner product space]] such that $\langle Ax,x \rangle\in\mathbb{R}^+$ for all $x\in\dom(A).$ ^PositiveOperator

A *positive-semidefinite operator* is an [[#^LinearOperator|operator]] on an [[Vector space#^InnerProd|inner product space]] such that $\langle Ax,x \rangle\in\mathbb{R}^{\geq 0}$ for all $x\in\dom(A).$ ^SemiPositiveOperator

A *self-adjoint*, or *Hermitian, operator*, is an [[#^LinearOperator|operator]] $A$ that is its own [[#^Adjoint|adjoint]]: $A^{\dagger}=A.$
If $A$ is [unbounded](#^UnboundedOperator), we also require it to be [symmetric](#^SymmetricOperator) and [densely defined](Topology.md#^DenselyDefinedMap). ^SelfAdjoint

A *normal operator* is a [[#^BoundedOperator|bounded operator]] $U:\H\to\H$ on a [[Vector space#^Hilbert|Hilbert space]] $\H$ that obeys $$UU^{\dagger}=U^{\dagger}U$$ ^NormalOperator

A *unitary operator* is a [closed](Operation.md#^Closed) [linear isometry](#^LinearIsometry) $U:\H\to \H$ on a [[Vector space#^Hilbert|Hilbert space]] $\H$ that, in addition to $U^{\dagger}U=I,$ obeys $UU^{\dagger}=I.$ Equivalently, $U^{\dagger}=U^{-1}.$
It preserves norms: $|Uψ|=|ψ|$ for all $ψ\in\H,$ and is therefore [bounded](#^BoundedOperator) with $|U|=1.$ ^UnitaryOperator

The *(Hermitian) adjoint* $A^{\dagger}:V\to V$ of a [[Operation#^Closed|closed]], [bounded](#^BoundedOperator) [[#^LinearOperator|operator]] $A:V\to V$ on an [[Vector space#^InnerProd|inner product space]] $V$ is defined by $\langle u,Av \rangle=\langle A^{\dagger} u,v\rangle$ for all $u,v\in V.$ ^Adjoint

The *adjoint* $A^{\dagger}:V\to V$ of a [densely defined](Topology.md#^DenselyDefinedMap) (possibly [unbounded](Linear%20map.md#^UnboundedOperator)) [[#^LinearOperator|operator]] $A:V\to V$ on an [[Vector space#^InnerProd|inner product space]] $V$ is an operator whose domain is all $v\in V$ such that $v\mapsto\langle v,A v \rangle$ is a [distribution](#^Distribution) on $\dom(A),$ and $\langle u,Av \rangle=\langle A^{\dagger} u,v\rangle$ for all $u\in\dom(A^{\dagger}),v\in \dom(A).$
In general, $A^{\dagger}$ need not be densely defined. ^AdjointUnbounded

A *projection* is an [[#^LinearOperator|operator]] $P:W\to V,$ where $V\subseteq W$ is a [linear subspace](Vector%20space.md#^Subspace) of $W,$ such that $$P^2=P$$ ^ProjectionOperator

An *orthogonal projection* is a [[#^ProjectionOperator|projection]] $P:\H\to\H'$ between [[Vector space#^Hilbert|Hilbert spaces]] whose [[Function#^RangeImage|range]] $P(\H)$ and [[Morphisms#^Kernel|kernel]] $P^{-1}(I)$ are [[Vector space#^OrthogonalSubspace|orthogonal subspaces]]:
$$\braket{ψ}{Pφ}=\braket{Pψ}{Pφ}=\braket{Pψ}{φ}$$
Equivalently, $P$ is [[Linear map#^SelfAdjoint|self-adjoint]] ^OrthogonalProjection

Two [[#^LinearOperator|operators]] are *orthogonal* if their images are [[Vector space#^OrthogonalSubspace|orthogonal subspaces]]. ^OrthogonalOperator

The *spectrum* $σ(A)$ of a [bounded](#^BoundedOperator) [operator](#^LinearOperator) $A:B\to B$ acting on a $\C$-[Banach space](Vector%20space.md#^Banach) $B,$ is the set of $λ\in\C$ such that $A-λI$ does not have an [inverse](Operation.md#^Inverse). ^Spectrum

The *parity operator* $Π=U(π)$ is an [[Linear map#^LinearOperator|operator]] defined such that $Π\hat x Π^{-1}=-\hat{x}$ and $Π\hat{p}Π^{-1}=-\hat{p}.$ Equivalently:$$Πψ(x)=ψ(-x)$$$Π$ is [[Linear map#^UnitaryOperator|unitary]] and [[Linear map#^SelfAdjoint|self-adjoint]], so $Π^{\dagger}=Π^{-1}=Π$.
Useful property: $ΠU(x)=U(-x)Π$ ^ParityOperator

## Trace

The *trace* of a [[#^SemiPositiveOperator|positive-semidefinite]], [[#^SelfAdjoint|self-adjoint]] [[#^LinearOperator|linear operator]] $A:\H\to\H$ on a [[Vector space#^Hilbert|Hilbert space]] $\H$ is given by$$\tr(A)=\sum_i\bra{e_i}  A\ket{e_i} $$where $e_i\in\H$ form an [[Vector space#^OthonormalBasis|orthonormal basis]] for $\H.$ Its value does not depend on the choice of basis. ^Trace

The *partial trace* $\mathrm{Tr}_\K$ is a [linear map](#^LinearMap) $\mathrm{Tr}_\K:\T(\H\otimes\K)\to\T(\K)$ satisfying$$\mathrm{Tr}(\mathrm{Tr}_\K(A)B)=\mathrm{Tr}(AB\otimes \hat{I})$$for all $A\in\mathcal{T}(\H\otimes\K)$ and $B\in B(\H).$ With [[Vector space#^OthonormalBasis|orthonormal bases]] $\{e_i\}$ for $\H$ and $\{φ_i\}$ for $\K,$ the definition is$$\mathrm{Tr}_\K(A) = \sum_{i,j,k} \bra{e_i\otimes φ_j}A\ket{e_k\otimes φ_j}\ket{e_i}\bra{e_k}   $$ ^PartialTrace

A *trace-class operator* $T\in\T(\H)$ is an [[#^LinearOperator|operator]] that belongs to the *trace class* $\T(\H)$ (or $\L_1(\H)),$ for which a finite [[#^Trace|trace]] can be defined. The condition is $\tr(\sqrt{ T^{\dagger}T })<\infty.$
The [[Vector space#^DualSpace|dual]] of $\mathcal T(\H)$ are the [[#^BoundedOperator|bounded]] operators $B(\H).$ ^TraceClass

### Trace properties

- $\tr(U^\dagger A\, U)=\tr(A)$ ^TraceUnitaryInvariance
- $\tr(A\otimes B)=\tr(A)\tr(B)$ ^TraceTensor
- $\tr\left(\sum_i\ket{ψ_i}\bra{φ_i}\right)=\tr\left(\sum_i\braket{φ_i}{ψ_i}\right)$ ^TraceKetBra

