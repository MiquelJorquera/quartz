---
tags: Physics/Mechanics/Quantum_mechanics 
---


***Axiom 1:*** The set $\mathbf{S}$ of all [states](#^State) in a [statistical duality](#^StatisticalDuality) $(\mathbf{S},\mathbf{O},p)$ forms a [convex subset](Set.md#^ConvexSet) of an $\rr$-[vector space](Vector%20space.md#Vector%20space). ^Axiom1

***Axiom 2:*** The experimental functions $f_{|(\E,X)|}:ρ\mapsto p^\E_ρ(X)$ of a [statistical duality](#^StatisticalDuality) $(\mathbf{S},\mathbf{O},p)$ are affine. ^Axiom2



In quantum mechanics, *physical systems* are associated to [Hilbert spaces](Vector%20space.md#^Hilbert) $\H.$ ^System

# General probabilistic theories

*States* $φ\in\mathbf{S}$ are [equivalence classes](Relation.md#^EquivalenceClass) of preparations $π$ of a [physical system](#^System): $$φ\equiv [π] = \{ π'| p^M_{π'}=p^M_{π}\}$$ for all measurements $M\in\E\in\mathbf{O}.$ I.e. an [ensemble](Probability%20theory.md#^Ensemble) of the system. The state space $\mathbf{S}$ has a [convex](Vector%20space.md#^ConvexCombination) structure, reflecting the fact that you can statistically mix several preparations into a new preparation.
In Hilbert space QM, they are identified with [positive](Linear%20map.md#^PositiveOperator) [operators](Linear%20map.md#^LinearOperator) of [trace](Linear%20map.md#^Trace) 1. 
The [convex set](Set.md#^ConvexSet) of all states in $\H$ is denoted by $\S(\H).$ ^State

*Observables* $\E\in\mathbf{O}$ are [equivalence classes](Relation.md#^EquivalenceClass) of measurements $M$ performed on a [physical system](#^System): $$\E\equiv[M] = \{M'\ | \ p_π^{M'}=p_π^M\}$$ for all preparations $π\in ρ\in\mathbf{S}.$ 
They assign measurement outcomes $ω\in\F$ in the ([measurable](Measure.md#^MeasurableSpace)) outcome space $(Ω,\F)$ to [effect operators](#^Effect): $\E:\F\to B(\H),$ or $\E:ω\mapsto \E(ω).$
If we demand the composite map $ω\mapsto \E(ω)\mapsto \tr(ρ\,\E(ω))=p^\E_ρ(ω)$ to be a [probability measure](Measure.md#^ProbabilityMeasure) for all [states](#^State) $ρ,$ it can be shown that $\E(ω)$ is an [operator](Linear%20map.md#^LinearOperator), so $\E$ is a [POVM](Measure.md#^POVM). ^Observable

$ω\mapsto \E_ω\mapsto \E_ω(ρ)=p^\E_ρ(ω)$ 
$ω\mapsto \E(ω)\mapsto \tr(ρ\,\E(ω))=p^\E_ρ(ω)$ 

*Effects* $\E_ω:\mathbf{S}\to [0,1]$ are equivalence classes of *measurement registrations*, or *events,* i.e. [observable](#^Observable)-outcome pairs $(\E,ω):$ $$\E_ω\equiv [(\E,ω)]=\{(\mathsf F,ω')\ |\ p_ρ^\mathsf F(ω') = p_ρ^\E(ω)\}$$ for all states $ρ\in\mathbf{S}.$ They are [affine](Vector%20space.md#^AffineSpace) [functionals](Linear%20map.md#^LinearForm) that map [states](#^State) to outcome probabilities: $\E_ω(ρ)=p^\E_ρ(ω).$ 
It can be shown[^(1)] that they can be realised as unique [bounded operators](Linear%20map.md#^BoundedOperator) $\E(ω)\in B(\H)$ such that the [Born formula](#^BornFormula) is obeyed: $\E_ω(ρ)=\tr(ρ\,\E(ω)) = p^{\E}_ρ(ω).$ This is the link to the related notion of the [effects](Measure.md#^Effects) of a POVM. ^Effect

[^(1)]: *The Mathematical Language of Quantum Theory*, pp. 68-70, or *Quantum Measurement*, p. 196


*Statistical causality* is the claim that a [state](#^State) $ρ$ and an [observable](#^Observable) $\E:\F\to\E_\F$ determine a [probability measure](Measure.md#^ProbabilityMeasure) $p_ρ^\E:\F\to[0,1]$ on the measurement outcome space $(Ω,\mathcal F),$ such that $p^\E_ρ(X)$ is the probability that measuring $\E$ on a system prepared in state $ρ$ will give an outcome in $X\in\F.$ ^StatisticalCausality

A *statistical duality* $(\mathbf{S},\mathbf{O},p)$ consists of all the [states](#^State) $ρ\in\mathbf{S}$ and [observables](#^Observable) $\E\in\mathbf{O}$ of a [system](#^System), together with the [probability function](#^StatisticalCausality) $p:(ρ,\E)\mapsto p_ρ^\E.$ ^StatisticalDuality

The *Born formula* specifies the [statistical causality](#^StatisticalCausality) Hilbert space QM: It specifies a [probability function](#^StatisticalDuality) $p:(ρ,\E)\mapsto p_ρ^\E$ that gives the [probability measure](Measure.md#^ProbabilityMeasure) $p_ρ^\E:\F\to[0,1]$ that measuring [observable](#^Observable) $\E:\F\to\E_\F$ in [state](#^State) $ρ$ will have an outcome in $ω\in \mathcal{F}:$
$$\tr(ρ\,\E(ω))=p_ρ^\E(ω)$$
If $\E=\P$ is a [PVM](Measure.md#PVM), there is a state $ω$ such that $p_ρ^\P(ω)=1$ iff $\P(ω)\neq 0$ ^BornFormula


Statistical duality $\to$ Fix observable $\to$ Observable $\to$ Fix outcome $\to$ Effect $\to$ Fix state $\to$ Probability
## Systems properties

*Composite systems* are [systems](#^System) associated to a [Hilbert space](Vector%20space.md#^Hilbert) which is the tensor product of two or more Hilbert spaces $\H=\H_1\otimes\H_2\otimes\dots \otimes\H_n.$ ^CompositeSystem

An *invariant operator algebra* $B(\H)^G$ consists of operators $A\in B(\H)$ that are invariant under $U:G\to B(\H),$ a [strongly continuous](Function.md#^StronglyContinuousFunction), [unitary representation](Linear%20representation.md#^UnitaryRep) of a [locally compact](Algebraic%20structure.md#^LocCompTopoGroup) [group](Algebraic%20structure.md#^Group) $G:$ $$B(\H)^G\equiv \{ A \ |\ U(g)A\,U^{\dagger}(g) = A\}$$ An invariant algebra is a [frame](Quantum%20reference%20frames.md#^QRF)-independent description, because [relativization](Relativization%20map.md#^RelMap) becomes trivial for all frames: $\yen^\R(A_\S)=I_\R\otimes A_\S.$ ^InvariantOperator

## States properties

A *pure state* is a [state](#^State) which is a [rank](Linear%20map.md#^Rank)-1 [projection](Linear%20map.md#^ProjectionOperator).
It is a minor sin, but it is usually said that pure states are states that can be written as $\ket{φ}\bra{φ}$ for some unit vector $φ\in\H$ (which can be called *vector states*).
Equivalently, it is an [extremal](Set.md#^ExtremalElement) state, i.e. not a [convex combination](Vector%20space.md#^ConvexCombination) of other states.
The set of all pure states is written as $\mathcal{P}(\H).$ ^PureState

A [state](#^State) is *mixed* if it is not [pure](#^PureState). ^MixedState

A *reduced state* $ρ_1\in\S(\H_1)$ in a [composite system](#^CompositeSystem) $\H_1\otimes\H_2$ is obtained from a regular [state](#^State) $ρ\in\S(\H_1\otimes\H_2)$ from the [partial trace](Linear%20map.md#^PartialTrace): $ρ_1=\mathrm{Tr}_{\H_2}(ρ).$
It is the state of the first component of the system, considered in isolation. ^ReducedState

A [vector state](#^PureState) $ψ$ in a [composite system](#^CompositeSystem) $\H_1\otimes\H_2$ is *separable* if it can be written as $ψ=φ_1\otimes φ_2$ for some $φ_1\in\H_1,\ φ_2\in\H_2.$
A [state](#^State) $ρ$ is *separable* if it isn't a [convex combination](Vector%20space.md#^ConvexCombination) of separable states. ^Separable

A [state](#^State) $ρ$ in a [composite system](#^CompositeSystem) is *entangled* if it is not [separable](#^Separable). ^Entangled


Two states $ρ,ω$ are *operationally equivalent* with respect to a collection of [effects](Measure.md#^Effects) $\mathcal{O}$ if $\tr(ρ\mathsf{F}) = \tr(ω\mathsf{F})$ for all $\mathsf{F}\in\mathcal{O}.$ ^OpEquivStates

---

## Observables properties

An [observable](#^Observable) is *sharp* if it is a [PVM](Measure.md#PVM) (which corresponds to a [self-adjoint operator](Linear%20map.md#^SelfAdjoint) by the [spectral theorem](Spectral%20theorem.md)).
If an observable is not sharp, it is *unsharp*. ^SharpObservable

A collection of [observables](#^Observable) $\E_i:\F_i\to B(\H)$ are *coexistent* if there exists an observable $\E:\F\to B(\H)$ such that $$\bigcup_i\text{ran}(\E_i)\subseteq \text{ran}(\E)$$ for all $X_i\in\F_i.$ ^Coexistence

A collection of ([coexistent](#^Coexistence)) [observables](#^Observable) $\E_i:\F_i\to B(\H)$ are *functionally coexistent* if there exists an observable $\E:\F\to B(\H)$ and [measurable functions](Function.md#^MeasurableFunction) $f_i:Ω\to Ω_i$ such that $$\E_i(X_i)=\E(f_i^{-1}(X_i))$$ for all $X_i\in\F_i.$ ^FunctionalCoexistence

Two [observables](#^Observable) $\E_1, \E_2$ on the outcome spaces $(\mathcal{F}_1,Ω_1),(\mathcal{F}_2,Ω_2)$ are *compatible*, or *jointly measurable*, if there exists an observable $\E$ on the outcome space $(\mathcal{F}_1\times \mathcal{F}_2, Ω_1\times Ω_2)$ such that for all $X\in\mathcal{F}_1,\, Y\in\mathcal{F}_2:$ $$\begin{split}
\E_1(X)&=\E(X\times Ω_2)\\
\E_2(Y)&=\E(Ω_1\times Y)
\end{split}$$ If either of them is [sharp](#^SharpObservable), then they are joint if they [commute](Operation.md#^Commutativity), and then $\E(X\times Y)=\E_1(X)\E_2(Y).$ This definition can be applied recursively for $n>2$ joint observables. ^JointObservables

The *marginal observables* of an [observable](#^Observable) $\E$ are [joint observables](#^JointObservables) $\E_1,\E_2$ that can be obtained from $\E.$ ^MarginalObservable

The *error* $\mathcal{W}_{ε,δ}(\E,\P)$ of an [observable](#^Observable) $\E:\rr\to B(\H)$ relative to a [sharp](#^SharpObservable) observable $\P:\rr\to B(\H),$ is the smallest interval length $w\ge0$ such that if $\P$ is localised within $x\pm δ/2,$ then the probability of $\E$ outcoming into $x\pm w/2$ is no smaller than $1-ε,$ where $ε\in(0,1):$ $$\mathcal{W}_{ε,δ}(\E,\P)\equiv\inf\Big\{w\ \Big|\ \forall x\forall ρ : \big(\P_ρ(J_{x,δ})=1\big)\implies \big(\E_ρ(J_{x,w})\ge1-ε\big)\Big\}$$ It describes the range within which the input values can be inferred from the output distributions, with confidence level $1 −ε,$ given initial localisations within $δ.$ So if $w$ is small for a small $ε,$ we can be quite sure that the outcome probabilities of $\E$ will be quite similar to those of $\P.$ (Shouldn't $w\ge δ?)$ ^Error

The *(gross) error bar width* $\mathcal{W}_ε(\E,\P)$ of an [observable](#^Observable) $\E$ relative to $\P,$ is the smallest [error](#^Error) $\mathcal{W}_{ε,δ}(\E,\P)$ at a fixed $ε$ and varying $δ:$ $$\mathcal{W}_ε(\E,\P)\equiv\inf_δ\mathcal{W}_{ε,δ}(\E,\P)=\lim_{ δ \to 0} \mathcal{W}_{ε,δ}(\E,\P)$$ The second equality is because the error is an increasing function of $δ.$ ^ErrorBarWidth

An [observable](#^Observable) $\E:\rr\to B(\H)$ is an *$ε$-approximation* to a [sharp](#^SharpObservable) observable $\P:\rr\to B(\H),$ if its [error](#^Error) $\mathcal{W}_{ε,δ}(\E,\P)$ is finite for all $δ.$ ^eApproximation

An [observable](#^Observable) $\E:\rr\to B(\H)$ is an *approximation* to a [sharp](#^SharpObservable) observable $\P:\rr\to B(\H),$ if its [error bar width](#^ErrorBarWidth) $\mathcal{W}_ε(\E,\P)$ is finite for all $ε\in(0,1/2)$ (because a "good" approximation should have confidence levels greater than $\frac12).$ ^Approximation

Two effects $\mathsf{F},\mathsf{G}$ are *operationally equivalent* with respect to a collection of [states](#^State) $\S$ if $\tr(ρ\mathsf{F}) = \tr(ρ\mathsf{G})$ for all $\mathsf{ρ}\in\mathcal{S}.$ ^OpEquivEffects

---
# Random identities

$\braket{x}{p} = \frac1{\sqrt{\tau}}e^{ipx}$ ([proof](https://www.youtube.com/watch?v=98jMwN6MYy8))

---
# Commutators

The *canonical commutation relation* between two [[canonical conjugates]] $\hat x$ and $\hat p$ is$$[\hat x,\hat p]=i\hat I$$ ^CanCommRel
## Commutator properties
$$\begin{split}
[\hat{x},\hat{p}^n]&=\sum_{k=0}^{n-1}\hat{p}^k[\hat{x},\hat{p}]\hat{p}^{n-k-1}=in\hat{p}^{n-1}\\
[\hat{x}^n,\hat{p}]&=\sum_{k=0}^{n-1}\hat{x}^k[\hat{x},\hat{p}]\hat{x}^{n-k-1}=in\hat{x}^{n-1}
\end{split}$$

^CommPwr

$$\begin{split}
[\hat{x},e^{iq\hat{p}}]&=
\sum_{n=0}^\infty\frac{(iq)^n[\hat{x},\hat{p}^n]}{n!}=
-qe^{iq\hat{p}}\\
[e^{iq\hat{x}},\hat{p}]&=
\sum_{n=0}^\infty\frac{(iq)^n[\hat{x}^n,\hat{p}]}{n!}=
-qe^{iq\hat{x}}
\end{split}$$

^CommExp

---
# Weyl operator/transform

The *Weyl operator* $W:\rr^2\to B(\H)$ in [[canonical coordinates]] $(q,p)\in\rr^2$ is given by $$\begin{split}
W(q,p)&= 
 e^{i(p\hat{Q}-q\hat{P})}
\\&= e^{\frac i2 qp}e^{-iq\hat{P}}e^{ip\hat{Q}}
\\&= e^{\frac i2 qp}\, U(q)V(p)
\end{split}$$ It is [unitary](Linear%20map.md#^UnitaryOperator). ^WeylOperator

The *Weyl transform*, or *Weyl quantization* $W:\L^2(Γ)\to \L(\H),$ is an [invertible](Operation.md#^Inverse) map from square-integrable phase space [functions](Function.md#^Function) $f(q,p)\in\L^2(Γ)$ into [Hilbert space](Vector%20space.md#^Hilbert) [operators](Linear%20map.md#^LinearOperator): $$\begin{split}
W(f) &= \frac1{τ^2}\iint\tilde f(a,b)e^{i(a\hat Q + b\hat P)}\, da\, db\\
&= \frac1{τ^2}\iint\tilde f(a,b)W(-b,a)\, da\, db\\
&= \iint f(q,p)W(q,p)\, Π \, W^{\dagger}(q,p)\, dq\, dp\\
\end{split}$$
where $\tilde f(a,b)=\iint_{\rr^2} f(q,p) e^{i(bp-aq)}\,dq\,dp$ is the [Fourier transform](Function.md#^Fourier) of $f(q,p)$, the operators $\hat{P}$ and $\hat{Q}$ are satisfy the [canonical commutation relation](#^CanCommRel), and $W(q,p)$ is the [Weyl operator](#^WeylOperator). Written in full: $$W(f) = \frac1{τ^2}\iiiint f(q,p)e^{i\left( a(\hat Q-q) + b(\hat P-p)\right)}\, dq\, dp\, da\, db $$ ^WeylTransform

The *Wigner transform* $\mathcal{W}:B(\H)\to\L^2(Γ)$ of a [trace-class operator](Linear%20map.md#^TraceClass) operator $T\in\T(\H)$ is a [continuous](Function.md#^ContinuousFunction), square-integrable phase space function given by $$\begin{split}
\mathcal{W}_T(q,p)&=2\int_{\rr} \bra{q+x} T\ket{q-x} e^{2ipx}dx
\\&=\frac1π\mathrm{Tr}(T\,W(q,p)\, Π \, W^{\dagger}(q,p))
\\&=\frac1π\mathrm{Tr}(W(2q,2p)\, Π \, T)
\end{split}$$ where $W(q,p)$ is the [Weyl operator](#^WeylOperator) and $Π$ is the [parity operator](Linear%20map.md#^ParityOperator) ^WignerTransform

[Trace properties](Linear%20map.md#Trace%20properties)

## Wigner-Weyl properties:

The Wigner and Weyl transforms are dual to each other: $$\tr(TW(f))=\int_Γ \mathcal{W}_T(q,p)\, f(q,p)\, dq\,dp$$ And inverses:$$\begin{split}
W(\mathcal{W}_T) &= T\\
\mathcal{W}_{W(f)} &= 
\end{split}$$
- If $f$ is real, $W(f)$ is [self-adjoint](Linear%20map.md#^SelfAdjoint).
- If $f$ is a Schwartz function, $W(f)$ is [trace-class](Linear%20map.md#^TraceClass).
- $W(f)$ is a densely defined [unbounded operator](Linear%20map.md#^UnboundedOperator).
- $W(f)$ is 1-to-1 on the Schwartz space (as a subspace of the square-integrable functions).


Cool QM book by Frank Schroeck "QM in phase space" or similar title

The *Weyl form* of the [canonical commutation relation](#^CanCommRel) is given by$$e^{it\hat{p}}e^{is\hat{x}}=e^{is\hat{x}}e^{it\hat{p}}e^{-ist}$$It is calculated using the Weyl form of the operators and the [Baker-Campbell-Hausdorff formula](Algebraic%20structure.md#^BCH-Formula) for a operators that [commute](Operation.md#^Commutativity) with its commutator: $$\begin{split}
 e^{it\hat{p}}e^{is\hat{x}}& =e^{it\hat{p}+is\hat{x}+\frac12[it\hat{p},is\hat{x}]}\\
 & =e^{(is\hat{x}+it\hat{p}+\frac12[is\hat{x},it\hat{p}])-\frac12[is\hat{x},it\hat{p}]+\frac12[it\hat{p},is\hat{x}]}\\
 & =e^{is\hat{x}}e^{it\hat{p}}e^{\frac{st}{2}\left([\hat{p},\hat{x}]-[\hat{x},\hat{p}]\right)}\\
 & =e^{is\hat{x}}e^{it\hat{p}}e^{-ist}
\end{split}$$ ^WeylRelation

## Weyl operator properties

$$\begin{split}
 e^{\frac i2qp}e^{-iq\hat{P}}e^{ip\hat{Q}}& =e^{\frac i2qp-iq\hat{P}+ip\hat{Q}+\frac12[-iq\hat{P},ip\hat{Q}]}\\
 & =e^{\frac i2qp-iq\hat{P}+ip\hat{Q}-\frac i2qp}\\
 & =e^{i(p\hat{Q}-q\hat{P})}\\
\end{split}$$

Weyl product 1 $$\begin{split}
W(q,p)W(q',p') &=
e^{\frac i2qp}V(q)U(p)\quad
e^{\frac i2q'p'}V(q')U(p')
\\&=
e^{\frac i2(qp+q'p')}
V(q)\big(e^{iq'p}V(q')
U(p)\big)U(p')
\\& =
e^{\frac i2(qp+2q'p+q'p')}
V(q+q')U(p+p')
\\& =
e^{\frac i2((q+q')(p+p')+(q'p-p'q))}
V(q+q')U(p+p')
 \\W(q,p)W(q',p')&=
 e^{\frac i2(q'p-qp')}W(p+p',q+q')
\end{split}$$ 
^WeylProd1

Weyl product 2 $$\begin{split}
W(q,p)W(q',p') &=
e^{i(p\hat{Q}-q\hat{P})}e^{i(p'\hat{Q}-q'\hat{P})}
\\&=
e^{i(p\hat{Q}-q\hat{P}+p'\hat{Q}-q'\hat{P})-\frac12[(p\hat{Q}-q\hat{P}),(p'\hat{Q}-q'\hat{P})]}
\\&=
e^{i((p+p')\hat{Q}-(q+q')\hat{P})
+\frac{q'p}2[\hat{Q},\hat{P}]
+\frac{qp'}2[\hat{P},\hat{Q}]}
\\&=
e^{i(p+p')\hat{Q}-i(q+q')\hat{P}}\
e^{\frac i2(q'p-qp')}
\\W(q,p)W(q',p')&=
e^{\frac i2(q'p-qp')}W(p+p',q+q')
\end{split}$$ ^WeylProd2

---
# Channels

A *channel* $Λ:B(\H_1)\to B(\H_2)$ is a [unital](Linear%20map.md#^UnitalMap), [normal](Linear%20map.md#^NormalMap), [completely positive](Linear%20map.md#^CompletelyPositiveMap) [linear map](Linear%20map.md#^LinearMap).
They are used to describe quantum evolution, because they map [observables](#^Observable) into observables. ^Channel

A [channel](#^Channel) $Λ$ is *incompatibility-breaking* for a set of [incompatible](#^JointObservables) [observables](#^Observable) $\E_i,$ if the observables $Λ(\E_i)$ are compatible.
It is simply *incompatibility-breaking* if it breaks the incompatibility of all observables in its Hilbert space. ^IncompatibilityBreakingChannel

The *predual map* is a [completely positive](Linear%20map.md#^CompletelyPositiveMap), [trace](Linear%20map.md#^Trace)-preserving map 
$Λ_*:\T(\H_1)\to\T(\H_2)$ between [trace classes](Linear%20map.md#^TraceClass), defined by $$\tr(TΛ(A))=\tr(Λ_*(T)A)$$ where $Λ$ is a [channel](#^Channel), $T\in\T(\H_2),$ and $A\in B(\H_1).$ [NORMAL](Linear%20map.md#^NormalMap)?? ^PredualMap

---
# Measurement model

A *measurement model* of an [observable](#^Observable) $\E$ on a [system](#^System) $\S$ associated to $\H_\S$ is a quadruple $(\H_\A, ρ^\A, \mathcal{V}, \E_\A),$ where our "probe" or "apparatus" system $\A$ is associated to $\H_\A$ and starts in [state](#^State) $ρ^\A.$ 
The [channel](#^Channel) $\mathcal{V}:\T(\H_\S\otimes \H_\A)\to \T(\H_\S\otimes \H_\A)$ describes the measurement interaction between $\S$ and $\A.$
The *pointer observable* $\E_\A$ on the probe system has the same outcome space $(Ω,\mathcal{F})$ as $\E.$
A measurement model must satisfy the *probability reproducibility condition* $$\tr(ρ\E(X)) = \tr\l\mathcal{V}(ρ\otimes ρ_\A)(\hat{I}\otimes \E_\A)\r$$ for all $X\in\B(Ω)$ and $ρ\in\S(\H_\S).$ This ensures that measurements of $\E_\A$ have the same probabilities as measurements of $\E.$

[composite system](#^CompositeSystem) is associated to $\H_\S\otimes \H_\A.$ In our case, we want to measure the position $Q$ of a particle.

# Von Neumann position measurement scheme

We wish to couple our "object" [system](#^System) $\S$ associated to $\H_\S=L^2(\rr)$ with our "probe" or "apparatus" system $\A$ associated to $\H_\A.$ The [composite system](#^CompositeSystem) is associated to $\H_\S\otimes \H_\A.$ In our case, we want to measure the position $Q$ of a particle.

The probe is first prepared in a ([pure](#^PureState), for simplicity) initial state $ρ^\A.$
Then, the system is allowed to interact and evolve unitarily via a [channel](#^Channel) $\mathcal{V}:\T(\H_\S\otimes \H_\A)\to \T(\H_\S\otimes \H_\A)$ which describes the measurement interaction between object and probe.
Finally, the system is separated and the probabilities recorded.

The pointer [observable](#^Observable) is associated to the [semispectral measure](Measure.md#^SemispectralMeasure) $\E^{Q_\A}:\mathcal{F}_\A\to B(\H_\A),$ where $Q_\A$ is a [self-adjoint operator](Linear%20map.md#^SelfAdjoint) on $\H_\A.$ The notation $\E^A$ indicates that the first moment $\E^A[1]=A.$ [effect](#^Effect)

The system starts in the [vector state](#^PureState) $P_φ,$ and it is made to unitarily interact with the probe via the [unitary operator](Linear%20map.md#^UnitaryOperator) $U=e^{-iλ(Q\otimes P_\A)}$, resulting in the composite system to be in state $U(P_φ\otimes ρ^\A)U^{\dagger}.$

Want an identity, composition, reversibility, and time is a single parameter

Where does the idea of time-evolution via unitary operators with interaction Hamiltonians come from? I see that $U$ generates shifts that are parametrized by $λ,$ but how do we know that these are the shifts that are happening in our system?

The probe is now entangled with the system. Next, we want to assign [probabilities](#^Effect) to each possible state of our probe. We're interested in the [reduced state](#^ReducedState) $ρ_φ^\A=\tr_{\H_\A}(U(P_φ\otimes ρ^\A)U^{\dagger})$ of the probe after the measurement interaction. We demand it to satisfy the calibration condition $$\begin{split}
p_φ^{\E^{Q_\S}}(X)&=p_{ρ_φ^\A}^{\E^{Q_\A}}(f^{-1}(X))\\
\tr\left(\E^{Q_\S}(X)P_φ\right)&=\tr\left(\E^{Q_\A}\left(f^{-1}(X)\right)ρ_φ^\A\right)
\end{split}$$ for all $φ\in\H$ and $X\in\B(\rr),$ and where $f:Ω_\A\to Ω$ is a [measurable](Function.md#^MeasurableFunction) [bijection](Function.md#^BijectiveFunc) called the *pointer function*, which accounts for the system and probe having different scales.
$U$ is of the form $$\begin{split}
U&=e^{-iλ(Q\otimes P_\A)}
\\&=e^{-iλ(\int_\rr x d\E^Q(x)\otimes P_\A)}
\\&\text{Wrong! Need functional calculus, or just explicitly write the exponential sum}
\\&=\int_\rr  e^{d\E^Q(x)\otimes -iλxP_\A}
\\&=\int_\rr  d\E^Q(x)\otimes e^{-ixλP_\A}
\\&=\int_\rr dx \ket{x}\bra{x}\otimes e^{-ixλP_\A}
\end{split}$$ I'm not convinced about the $e^{d\E^Q(x)}=d\E^Q(x)$ step, because I have used the "dirty" trick of setting $d\E^Q(x)=\ket{x}\bra{x}\ dx$ and so $(d\E^Q(x)^n)=d\E^Q(x).$ I could also handwave that "differentials squared vanish", but those are rationalizations for the fact that I only arrived to this result because I already knew it.
We choose $ρ^\A=P_\f=\ket{\f}\bra{\f}:$ $$\begin{split}
\tr\left(\E^{Q_\S}(X)P_φ\right)&=\tr\left(\E^{Q_\A}\left(f^{-1}(X)\right)ρ_φ^\A\right)\\
\bra{φ}\E^{Q_\S}(X)\ket{φ}
&= \bra{φ\otimes \f}U^{\dagger}(\hat{I}_\S\otimes \E^{Q_\A}(f^{-1}(X)))U\ket{φ\otimes \f}\\
&= \iint_{\rr^2}dx\, dx' \braket{φ}{x}\braket{x}{x'}\braket{x'}{φ} \otimes \bra{\f}e^{ixλP_\A} \E^{Q_\A}(f^{-1}(X))e^{ix'λP_\A}\ket{\f}\\
&= \iint_{\rr^2}dx\braket{φ}{x}\braket{x}{φ} \otimes  \int_{f^{-1}(X)}  d\bra{\f}\E^{Q_\A}(x''-λx)\ket{\f}\\
&= \iint_{\rr^2}dx\ dx''\ |φ(x)|^2 \otimes  χ_{f^{-1}(X)}(x'')\ |\f(x''-λx)|^2\\
&= \bra{φ}\left(\iint_{\rr^2}dx\ dx''\ \ket{x}\bra{x} \otimes  χ_X(f(x''))\ |\f(x''-λx)|^2\right)\ket{φ}\\
\end{split}$$ Therefore: $$\begin{split}
\E^{Q_\S}(X)&= \iint_{\rr^2}dx\ dx''\ \ket{x}\bra{x}\otimes χ_X(f(x''))\ |\f(x''-λx)|^2
\\&= \iint_{\rr^2}d\E^Q(x) \otimes χ_X(f(x''))e^{(λ)}(x-x''/λ)\ \frac{dx''}{λ}
\end{split}$$ where $e^{(λ)}(x)=λ|\f(-λx)|^2.$ So if we choose $f(x)=x/λ$ and change the variable to $x'\equiv \frac{x''}{λ}:$
$$\begin{split}
\E^{Q_\S}(X)
&=\int_{\rr}d\E^Q(x) \otimes (χ_X*e^{(λ)})(x)
\\&=(χ_X*e^{(λ)})(Q)
\end{split}$$
Now, if we choose $X=\rr$ and $λ=1:$ $$\begin{split}
\bra{φ}\E^{Q_\S}(\rr)\ket{φ} 
&=\iint_{\rr^2}dx\ dx''\  x''\ |φ(x)|^2 |\f(x''-x)|^2
\\&=\int_\rr dx''\,   x''(|φ|^2*|\f|^2)(x'')
\end{split}$$ If the probe has a brain, that brain will perceive itself to be in one of the "base states" $φ(x) = δ(x-x_0),$ so the expected value of a position measurement is: $$\begin{split}
\bra{x_0}\E^{Q_\S}(\rr)\ket{x_0} 
&=\int_{\rr}dx''\  x''\ |\f(x''-x_0)|^2
\end{split}$$ which is the usual result. And if the system were able to have a sharp position, we would get: $$\begin{split}
\bra{x_0}\E^{Q_\S}(\rr)\ket{x_0} 
&=\int_{\rr}dx''\  x''δ(x''-x_0-x_0')
\\&=x_0+x_0'
\end{split}$$

---
# Pictures of quantum mechanics

- Schrödinger picture: $$|\psi(t)\rangle = e^{-i\hat H t}|\psi\rangle,\qquad \hat{\mathcal O}(t) = \hat{\mathcal O}$$
- Heisenberg picture (nice for SR): $$|\psi(t)\rangle = |\psi\rangle,\qquad \hat{\mathcal O}(t) = e^{i\hat H t}\hat{\mathcal O}e^{-i\hat H t}$$
- Dirac/Interaction picture ([nice](Haag's%20theorem.md) for QFT): $$|\psi(t)\rangle = e^{-i\hat H_0 t}|\psi\rangle,\qquad \hat{\mathcal O}(t) = e^{i\hat H_0 t}\hat{\mathcal O}e^{-i\hat H_0 t}$$ where   $\hat{H}_0$ is the free part of the Hamiltonian, without an interaction term.