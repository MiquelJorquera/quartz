---
tags:  Physics/Mechanics/Quantum_mechanics/Quantum_reference_frames
---
# System of covariance
A *system of covariance* $(U,\E,\H)$ based on a [[Action#^HomogeneousG-space|homogeneous]] [[Action#^G-space|G-space]] $(Σ,·)_G$ consists of:
- $\H,$ a complex, [separable](Quantum%20mechanics.md#^Separable) [[Vector space#^Hilbert|Hilbert space]].
- $U:G\to B(\H),$ a [[Function#^StronglyContinuousFunction|strongly continuous]], [[Linear map#^ProjectionOperator|projective]] [[Linear representation#^UnitaryRep|unitary representation]] of a [[Algebraic structure#^LocCompTopoGroup|locally compact]], [second-countable](Topology.md#^SecondCountable) [[Algebraic structure#^TopoGroup|topological group]] $G.$
- $\E:\B(Σ)\to B(\H),$ a [[Measure#^POVM|POVM]].
Such that it obeys the *covariance condition*$$\E(g·X)=U(g)\E(X)U^{\dagger}(g)$$$B(\H)$ is the space of [[Linear map#^BoundedOperator|bounded operators]] in $\H$.
$\B(Σ)$ is the [[σ-algebra#^BorelAlgebra|Borel algebra]] of $Σ.$

# System of imprimitivity

A *system of imprimitivity* is a [[Quantum reference frames]] $(U,\P,\H)$ in which the [[Measure#^CovariantPOVM|covariant]] [[Measure#^POVM|POVM]] $\P$ is a [[Measure#PVM|PVM]]. ^SOI

---
# Quantum reference frames

A *quantum reference frame* $\R$ for $G$ is a [[#System of covariance|system of covariance]]  $\R=(U_\R,\E_\R,\H_\R)$ on $(Σ_\R,α)_G,$ where$$\begin{alignat}{3}
g·A&\equiv U_\R(g)AU_\R(g)^{\dagger} &&\ \ \text{ for }\ A\in B(\H_\R)\\
g·ρ&\equiv U_\R(g)^{\dagger}ρ\, U_\R(g) &&\ \ \text{ for }\  ρ\in \S(\H_\R)\\
g·X&\equiv α(g,X) &&\ \ \text{ for }\  X\in\B(Σ_\R).
\end{alignat}$$ ^QRF

A [QRF](#^QRF) $\R$ is *principal* if $Σ_\R$ is a [[Action#^Torsor|torsor]] (a.k.a. a principal homogeneous space), and *non-principal* otherwise. ^PrincipalQRF

A [QRF](#^QRF) $\R$ is *sharp* if $\E_\R$ is sharp (i.e. a [[Measure#PVM|PVM]]), and *unsharp* otherwise. ^SharpQRF

A [QRF](#^QRF) is *ideal* if it is [[#^PrincipalQRF|principal]] and [[#^SharpQRF|sharp]]. ^IdealQRF

A [QRF](#^QRF) $\R$ is *localizable* if $\E_\R$ is [[Measure#^LocalizablePOVM|localizable]]. ^LocalizableQRF

A [QRF](#^QRF) $\R$ is *complete* if there is no (non-[trivial](Algebraic%20structure.md#^TrivialSubgroup)) [subgroup](Algebraic%20structure.md#^Subgroup) $H_{0} ⊆ G$ acting trivially on all the [[Measure#^Effects|effects]] of $\E_\R,$ and *incomplete* otherwise.
$H_{0}$ is called an *isotropy subgroup* for $\E_\R.$ ^CompleteQRF

A [QRF](#^QRF) $\R$ is *informationally complete* if $\E_\R$ is informationally complete. ^InfoCompleteQRF

A [QRF](#^QRF) $\R$ is called a *coherent state frame* if $\E_\R$ is constructed from a system of coherent states. ^CoherentStateFrame

Two [QRFs](#^QRF) $\R_1,\R_2$ on the same value space $Σ_\R$ are *(unitarily) equivalent* if there is a [unitary](Linear%20map.md#^UnitaryOperator) map $U:\H_{\R_1}\to\H_{\R_2}$ such that$$\E_{\R_2}(X)=U\E_{\R_1}(X)U^{\dagger}$$ for all $X\in\B(Σ_\R).$ ^EquivalentQRFs

## Framed things

The space of *$\E_\R$-framed effects* $\mathcal{E}(\H_\R\otimes\H_\S)^{\E_\R}$ of a frame-system Hilbert space $\H_\R\otimes\H_\S$ is given by$$\mathcal{E}(\H_\R\otimes \H_\S)^{\E_\R}\equiv \mathrm{conv}\{ \E_\R(X)\otimes \mathsf{F}_\S \}^\mathrm{cl}$$for all $X\in\B(Σ_\R),$ and where $\mathsf{F}_\S\in\mathcal{E}(\H_\S)$ are [effects](Measure.md#^Effects) of the system. $\mathrm{conv}(·)^\mathrm{cl}$ denotes the [closed](Topology.md#^Closure) [convex hull](Set.md#^ConvexHull). ^FramedEffects

The space of *$\E_\R$-framed operators* $B(\H_\R\otimes\H_\S)^{\E_\R}$ of a frame-system Hilbert space $\H_\R\otimes\H_\S$ is the [closed](Topology.md#^Closure) [span](Vector%20space.md#^Span) of the $\E_\R$[-framed effects](#^FramedEffects) of the same space:$$B(\H_\R\otimes \H_\S)^{\E_\R}\equiv \mathrm{span}\{ \mathcal{E}(\H_\R\otimes \H_\S)^{\E_\R}\}^\mathrm{cl}$$ ^FramedOperators

The space of *$\E_\R$-framed trace-class operators* $B(\H_\R\otimes\H_\S)^{\E_\R}$ of a frame-system Hilbert space $\H_\R\otimes\H_\S$ is given by:$$\T(\H_\S)_{\E_\R}\equiv\T(\H_\R\otimes \H_\S)\,/\sim_{\E_\R}$$where $\sim_{\E_\R}$ is the [operational](Quantum%20mechanics.md#^OpEquivStates) [equivalence relation](Relation.md#Equivalence%20relation) with respect to the $\E_\R$[-framed effects](#^FramedEffects).  ^FramedTraceClassOperators

The space of *$\E_\R$-framed states* $B(\H_\R\otimes\H_\S)^{\E_\R}$ of a frame-system Hilbert space $\H_\R\otimes\H_\S$ is given by:$$\S(\H_\S)_{\E_\R}\equiv\S(\H_\R\otimes \H_\S)\,/\sim_{\E_\R}$$where $\sim_{\E_\R}$ is the operational [equivalence relation](Relation.md#Equivalence%20relation) with respect to the $\E_\R$[-framed effects](#^FramedEffects).  ^FramedStates

# Relativization map

The *relativization map* $\yen^\R:B(\H_\S)\to B(\H_\R\otimes\H_\S)^G$  is a [linear map](Linear%20map.md#^LinearMap) between [bounded operators](Linear%20map.md#^BoundedOperator) given by $$
\yen^\R(A_\S)\equiv\int_G d\E_\R(g)\otimes g·A_\S
$$where $\R$ is a [[Quantum reference frames#^PrincipalQRF|principal frame]] and $g·A_\S\equiv U(g)A\,U^{\dagger}(g),$ where $U_\S$ is any [[Function#^StronglyContinuousFunction|strongly continuous]], [[Linear representation#^UnitaryRep|unitary representation]] of $G$ on $\H_\S.$
It maps operators into $\E_\R$-[framed](Quantum%20reference%20frames.md#^FramedOperators), $G$[-invariant](Quantum%20mechanics.md#^InvariantOperator) operators. ^RelMap

The *restriction map* $Γ_ω:B(\H_{\R}\otimes\H_{\S})\to B(\H_\S)$ with respect to a [state](#^State) $ω\in\S(\H_\R)$ is a map between [bounded](Linear%20map.md#^BoundedOperator) operators given by the [trace](Linear%20map.md#^Trace)$$Γ_ω(A\otimes  B)=A\,\mathrm{Tr}(ω B)$$It is [linear](Linear%20map.md#^LinearMap), [unital](Linear%20map.md#^UnitalMap), and [adjoint](Linear%20map.md#^Adjoint)-preserving. It describes the system contingent on a particular state of the frame.
 ^RestrictionMap

The *$ω$-conditioned $\R$-relativization map* $\yen^\R_ω\equiv Γ_ω\circ\yen^\R:B(\H_\S)\to B(\H_\S)$ is given by$$\begin{split}
\yen^\R_ω(A_\S)&\equiv Γ_ω(\yen^\R(A_\S))\\
&=\int_G g·A_\S\, dp^{\E_\R}_ω(g)
\end{split}$$

For a pair of [principal frames](Quantum%20reference%20frames.md#^PrincipalQRF) $\R_1,\R_2,$ the *relative orientation observable* of $\R_2$ with respect to $\R_1$ is $$(\E_{\R_2}*\E_{\R_1})(X)=\yen^{\R_1}(\E_{\R_2}(X))=\int_G  d\E_{\R_1} \otimes g·\E_{\R_2}(X)$$ ^RelativeOrientation

---

The $G$*-twirl* is a map $\mathcal{G}:B(\H)\to B(\H)$ given by$$\mathcal{G}(A)\equiv\int_{G}dμ(g)\ g·A$$where $A\in B(\H)$, $g\in G$, and $μ$ is a normalized [[Measure#^HaarMeasure|Haar measure]]. It constrains the system into the [[Linear representation#^UnitaryRep|unitary representation]] of the [[Topology#^Compact|compact]] group $G.$
It is a special case of the [[#^RelMap|relativization map]] with $\H_\R=\C$ and trivial $G$ [[Action#^GroupAction|action]], so a covariant POVM is a Haar measure. ^G-twirl