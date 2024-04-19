---
tags:  Physics/Mechanics/Quantum_mechanics, Maths/Analysis
---

Let $(X,Σ)$ be a [measurable space](#^MeasurableSpace). A *measure* is a [[Function#^PositiveSemidefiniteFunc|positive-semidefinite]] [function](Function#^Function) $μ:Σ\to \rr_{\geq 0}$ such that for all [[Set#^Disjoint|disjoint]] $σ_{i}\in Σ:$
$$μ(\cup_i σ_i) = \sum_i μ(σ_i)$$
An important consequence is $μ(\varnothing)=0.$ ^Measure

Let $Σ$ be a [[σ-algebra#$σ$-algebra|$σ$-algebra]] of a set $X.$ A *signed measure* is a [function](Function#^Function) $μ:Σ\to \rr$ such that for all [[Set#^Disjoint|disjoint]] $σ_{i}\in Σ:$
$$μ(\cup_i σ_i) = \sum_i μ(σ_i)$$ 
An important consequence is $μ(\varnothing)=0.$ ^SignedMeasure

Let $Σ$ be a [[σ-algebra#$σ$-algebra|$σ$-algebra]] of a set $X.$ A *complex measure* is a [function](Function#^Function) $μ:Σ\to \C$ such that for all [[Set#^Disjoint|disjoint]] $σ_{i}\in Σ:$
$$μ(\cup_i σ_i) = \sum_i μ(σ_i)$$ 
An important consequence is $μ(\varnothing)=0.$ ^ComplexMeasure

A *probability measure* is a [measure](#^Measure) $p:Σ\to[0,1]$ such that $p(X)=1.$ ^ProbabilityMeasure

A *Haar measure* is a [measure](#^Measure) $μ:\B(G)\to \rr_{\geq0}$ on the [[σ-algebra#^BorelSet|Borel sets]] of a [[Algebraic structure#^LocCompTopoGroup|locally compact]] [[Algebraic structure#^TopoGroup|topological group]] $G$ that is invariant under the [[Action#^GroupAction|actions]] of $G.$ 
I.e. $μ(gA)=μ(A)$ for all $g\in G$ and $A\in\B(G)$ (left-invariant) ^HaarMeasure

A *Dirac measure* is a [measure](#^Measure) $δ_x:\mathcal P(X)\to \{0,1\}$ on the [[Set#^PowerSet|power set]] of a set $X,$ given by $$\d_x(A)=χ_A(x)=\begin{cases}
1 & \text{ if } x\in     A\\
0 & \text{ if } x\notin A\end{cases}$$where $x\in X,$ and $A\subseteq X,$ and $χ$ is the [indicator function](Function.md#^IndicatorFunction). ^DiracMeasure

A [measure](#^Measure) $μ$ is *absolutely continuous* with respect to a measure $ν$ on the same [measurable space](Measure.md#^MeasurableSpace) $(X,Σ)$ if$$\big(ν(σ)=0\big)\implies \big(μ(σ)=0\big)$$for all $σ\in Σ.$ It is usually denoted by $μ\ll ν.$ ^AbsolutelyContinuousMeasure

A *measurable space* (or *Borel space*) is a pair $(X,Σ)$, where $Σ$ is a [[σ-algebra#$σ$-algebra|$σ$-algebra]] over $X.$ ^MeasurableSpace

A *measure space* is a triple $(X,Σ,μ),$ where $μ$ is a [measure](#^Measure) on the [[Measure#^MeasurableSpace|measurable space]] $(X,Σ).$ ^MeasureSpace

The *image measure*, or *pushforward* $f_*(μ):Σ_2\to\rr_{\geq 0}$ of a [measure](Measure.md#^Measure) $μ:Σ_1\to\rr_{\geq 0}$ in a [measurable space](#^MeasurableSpace) $(X_1,Σ_1),$ is a measure in a measurable space $(X_2,Σ_2)$ given by$$f_*(μ)(σ_2)=μ(f^{-1}(σ_2))$$where $σ_2\in Σ_2,$ and $f:X_1\to X_2$ is a [measurable function](Function.md#^MeasurableFunction).
Intuitively, you want to measure a subset that has been transformed by $f.$ So you just undo that transformation and measure it. ^ImageMeasure

A *product measure* $μ\times ν$ of two [measures](#^Measure) $μ,ν$ on the [measurable spaces](#^MeasurableSpace) $(X_μ,Σ_μ)$ and $(X_ν,Σ_ν),$ is a measure on the measurable space $(X_μ\times X_ν\,, Σ_μ\otimes Σ_ν)$ such that$$(μ\times ν)(A\times B)=μ(A)ν(B)$$for all $A\in Σ_μ,\ B\in Σ_ν.$ The product measure is unique if $μ,ν$ are $σ$-finite. ^ProductMeasure

The *[convolution](Function.md#^Convolution)* of two complex [measures](#^Measure) $μ,ν:\B(\rr)\to\C$ is the measure $μ*ν:\B(\rr)\to\C$ such that$$\begin{split}
(μ*ν)(X)&=(μ\times ν)\left(\{  (x\times y)\ |\ x+y\in X \}\right)
\\&=\int_{\rr} μ(x)ν(X-x) \, dx 
\end{split}$$where $X\in\B(\rr),$ and $μ\times ν:\B(\rr^2)\to\C$ is the [product measure](#^ProductMeasure). ^MeasureConvolution

The *overall width* $W_ε(μ)$ of a [probability measure](#^ProbabilityMeasure) $μ:\B(\rr)\to[0,1]$ is the length of the smallest interval $X\in\mathcal{I}$ whose measure is no smaller than $1-ε:$$$W_ε(μ)=\inf_{X\in\mathcal{I}}\{|X| : μ(X)\ge 1-ε\}$$Properties: $$\begin{split}
W_ε(μ*ν)&\ge\max\{W_ε(μ),W_ε(ν)\}\\
W_ε(μ)&\le 2ε^{-1/α}\, σ_α(μ)
\end{split}$$ ^OverallWidth

The *$α$-deviation* $σ_α(μ,δ_y)$ of a [probability measure](#^ProbabilityMeasure) $μ:\B(\rr)\to[0,1]$ from a point $y\in\rr$ is given by$$\begin{split}
σ_α(μ,δ_y)&=\l\int |x-y|^α\, dμ(x)\r^{\frac1α}
\end{split}$$for $1\le α<\infty.$
 ^AlphaDeviation

The *$α$-spread*, or *minimal $α$-deviation* $σ_α(μ)$ of a [probability measure](#^ProbabilityMeasure) $μ:\B(\rr)\to[0,1]$ is the smallest $α$[-deviation](#^AlphaDeviation) $σ_α(μ,δ_y)$ for all $y:$$$\begin{split}
σ_α(μ)&=\inf_{y\in\rr}\l σ_α(μ,δ_y)\r
&=\inf_{y\in\rr}\l\int |x-y|^α\, dμ(x)\r^{\frac1α}\\
\end{split}$$for $1\le α<\infty.$
The value of $y$ where $σ_α(μ)=σ_α(μ,δ_y)$ depends on $α:$ For the absolute deviation $(α=2),$ it is the [median](Probability%20theory.md#^Median). For the [standard deviation](Probability%20theory.md#^StandardDeviation) $(α=2),$ it is the [mean](Probability%20theory.md#^MeanExpectation).
 ^AlphaSpread

---
# PVM

Let $(X,Σ)$ be a [[#^MeasurableSpace|measurable space]], and $\H$ a complex [[Vector space#^Hilbert|Hilbert space]].
A *projection-valued measure*, or *PVM*, is a [function](Function#^Function) $\P:Σ\to B(\H)$ whose values are [[Linear map#^BoundedOperator|bounded]] [[Linear map#^ProjectionOperator|projections]], such that for all [[Set#^Disjoint|disjoint]] $σ_i\in Σ:$
- $\P(\cup_iσ_i) = \sum_i \P(σ_i)$
- $\P(σ_i)$ and $\P(σ_j)$ are [[Linear map#^OrthogonalProjection|orthogonal]] if $i\neq j$

A PVM is a [POVM](#^POVM) whose values are [[Linear map#^ProjectionOperator|projection operators]], which happens iff $\E$ is multiplicative: $\E(σ_i\cap σ_j) =\E(σ_i)\E(σ_j)\iff \E(σ_i)^2=\E(σ_i)$

A *spectral measure*, or *normalized PVM* $\P,$ is a [PVM](#PVM) such that$$\P(X)=I_\H$$ Most people just call this a PVM. ^SpectralMeasure

Definition of orthogonality, check for equivalence between [orthogonality of projections](Linear%20map.md#^OrthogonalProjection) vs. [orthogonality of subspaces](Vector%20space.md#^OrthogonalSubspace).

# POVM

Let $(X,Σ)$ be a [[#^MeasurableSpace|measurable space]], and $\H$ a complex [[Vector space#^Hilbert|Hilbert space]].
A *positive operator-valued measure*, or *POVM*, is a [function](Function#^Function) $\E:Σ\to B(\H)$ whose values are [[Linear map#^SemiPositiveOperator|positive semidefinite operators]], such that for all [[Set#^Disjoint|disjoint]] $σ_i\in Σ,$ and all $ρ\in\S(\H):$$$\begin{split}
\E(\cup_iσ_i) &= \sum_i \E(σ_i)\\
\tr(ρ\,\E(σ))&\geq0
\end{split}$$The last expression is a regular [measure](#^Measure). In standard QM, it is the [probability measure](#^ProbabilityMeasure) that measuring the [observable](Quantum%20mechanics.md#^Observable) $\E$ of a [system](Quantum%20mechanics.md#^System) in [[Quantum mechanics#^State|state]] $ρ$ will yield outcome $σ.$ These operators are [[Linear map#^BoundedOperator|bounded]] and [[Linear map#^SelfAdjoint|self-adjoint]]. ^POVM

A *semispectral measure*, or *normalized POVM* $\E,$ is a [POVM](#^POVM) such that$$\E(X)=I_\H$$ Most people just call this a POVM. ^SemispectralMeasure
  
In finite-dimensional QM with usual measurement operators $M_m,$ the POVM elements are $\E_m\equiv M_m^\dagger M_m,$ so $P(m) = \bra ψ \E_m \ket ψ.$


A [POVM](#^POVM) is *localizable*, or *norm-1*, if the [[Function#^Norm|norm]] $\lvert \E(σ) \rvert$ is either 0 or 1 for all $σ\in Σ.$ ^LocalizablePOVM

A [POVM](#^POVM) $\E$ is *covariant* if it is part of a [[Quantum reference frames#System of covariance|system of covariance]] $(U,\E,\H).$ ^CovariantPOVM

The *effects* of a [POVM](#^POVM) $\E:Σ\to B(\H)$ are the [operators](Linear%20map.md#^LinearOperator) $A\in B(\H)$ in its [image](Function.md#^RangeImage).
The space of effects on $\H$ is written as $\mathcal{E}(\H).$ ^Effects

A *localizing sequence* $ω_n(x)$ centered at $x\in Σ$ for metrizable [*G*-space](Action.md#^G-space) $Σ$, is a [[Function#^Sequence|sequence]] of [[Quantum mechanics#^PureState|pure states]] $ω_n$ that allows us to approximate a [[#^DiracMeasure|Dirac measure]] $δ_x$ with the [[#^ProbabilityMeasure|probability measures]] 
$$μ^\E_{ω_n}(X)=\tr\l \E(X)ω_n(x) \r$$
for $\E$ [[#^LocalizablePOVM|localizable]], for all $X\in\B(Σ)$ with negligible boundary $(δ_x(\p X)=0),$ such that $\lim_{ n \to \infty }μ^\E_{ω_n}(X)=δ_x(X).$ ^LocalizingSequence

A [POVM](#^POVM) $\E_\P$ can arise from a [PVM](#PVM) $\P$ via *smearing*:$$\E_\P(X)=\int _\rr k(λ,X) \, d\P(λ) $$where $k:\rr\times\B(\rr)\to[0,1]$ is a [Markov kernel](Probability%20theory.md#^MarkovKernel). We usually only consider [confidence functions](Probability%20theory.md#^ConfidenceFunction) $k(λ,X)=e(X-λ),$ though. In that case, we get the form$$\E(X)=(e*\P)(X)=\int _\rr e(X-λ) \, d\P(λ)$$which is a [measure convolution](#^MeasureConvolution). The smearing goes away when $e$ is a delta function.
 ^Smearing



---
# Calculus with measures

The *Lebesgue integral* of a [simple](Function.md#^SimpleFunction), [measurable function](Function.md#^MeasurableFunction) $f= \sum_{k}a_{k}χ_{σ_{k}}:X\to\mathbb K$ on a [measure space](Measure.md#^MeasureSpace) $(X,Σ,μ)$ is given by
$$\int_S f\ dμ\equiv\sum_k a_k μ(σ_k \cap S)$$ ^LebesgueSimpleInt

An integral $\int_Ω f (σ)\ d\P(σ)$ with respect to a [PVM](#PVM) $\P:Σ\to B(\H)$ is defined from the [integral](#^LebesgueSimpleInt) with respect to the [measure](#^Measure) $\tr(ρ\,\P(σ)):$
$$\tr\l ρ\int_Ω f(σ)\ d\P(σ)\r\equiv\int_Ω f(σ)\ d\l\tr(ρ\,\P(σ))\r $$This integral is [[Linear map#^LinearOperator|operator]]-valued, and the [[Spectral theorem]] says that for all states $ρ,$ this correspondence between PVM and operator is 1-to-1. ^PVMInt

An integral $\int_Ω f (σ)\ d\E(σ)$ of a [measurable function](Function.md#^MeasurableFunction) $f:(X,Σ)\to \C$ with respect to a [POVM](#POVM) $\E:Σ\to B(\H)$ is defined from the [integral](#^LebesgueSimpleInt) with respect to the [complex measure](#^ComplexMeasure) $\tr(ρ\,\E(σ)):$
$$\tr\l ρ\int_Ω f(σ)\ d\P(σ)\r\equiv\int_Ω f(σ)\ d\l\tr(ρ\,\P(σ))\r $$This integral is [[Linear map#^LinearOperator|operator]]-valued, this correspondence between POVM and operator is 1-to-1. ^POVMInt

The *Fourier transform* $\widetilde{\E}$ of a [POVM](#POVM) $\E:Σ\to B(\H)$ is given by$$\widetilde \E(x)\equiv \int_\rr e^{ixt} \, d\E(t)$$(using $e^{ixt}$ or $e^{-ixt}$ is a matter of convention).

The *Radon-Nikodym derivative* $\dv{μ}{ν}$ of two finite [measures](#^Measure) such that [*μ<<ν*](#^AbsolutelyContinuousMeasure), is a [nonnegative](Function.md#^PositiveSemidefiniteFunc) [measurable function](Function.md#^MeasurableFunction) given by$$μ(σ)=\int_σ \dv{μ}{ν}dν$$The *Radon-Nikodym theorem* asserts that this derivative exists and is unique. ^RadonNikodymDerivative

Properties of the Radon-Nikodym derivative:$$\begin{split}
\dv{(μ+ν)}{λ}&=\dv{μ}{λ}+\dv{ν}{λ}\\
\dv{μ}{λ}&=\dv{μ}{ν}\dv{ν}{λ}\\
\int_σ g\, dμ &=\int_σ g\dv{μ}{λ}dλ \quad\text{ if $g$ is a $μ$-integrable function}  \\
\dv{μ}{ν}&=\left(\dv{ν}{μ}\right)^{-1}\\
\end{split}$$ ^RadonNikodymProperties

  Integration by change of variables:$$\int_a^b f(g(x))\dv{g(x)}{x} dx = \int_{g(a)}^{g(b)} f(g)\, dg$$Useful properties:$$\begin{split}
\int_a^b f(x\pm c)dx &= \int_{a\pm c}^{b\pm c} f(x)\, dx\\
\int_a^b f(kx)dx &= \frac{1}{k}\int_{ka}^{kc} f(x)\, dx
\end{split}$$
 ^ChangeOfVariables