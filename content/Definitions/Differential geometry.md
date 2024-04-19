---
tags:
  - Maths/Geometry/Differential_geometry
---
# Differential geometry
Differential geometry studies differentiable manifolds.
## Differentiable manifolds

A *differentiable manifold* is a [second-countable](Topology.md#^SecondCountable) [topological manifold](Topology.md#^TopoManifold) with a [differential structure](#^DiffStructure). ^DiffManifold

A *smooth manifold* is a [second-countable](Topology.md#^SecondCountable) [topological manifold](Topology.md#^TopoManifold) with a [smooth structure](#^SmoothStructure). ^SmoothManifold

A *complex manifold* is a [second-countable](Topology.md#^SecondCountable) [topological manifold](Topology.md#^TopoManifold) with a [complex structure](#^ComplexStructure). ^ComplexManifold

A *symplectic manifold* is a [smooth manifold](#^SmoothManifold) equipped with a [symplectic form](Linear%20map.md#^SymplecticForm) (i.e. with a [symplectic structure](#^SymplecticStructure)) ^SymplecticManifold

A *Riemannian manifold* is a [smooth manifold](#^SmoothManifold) equipped with a [Riemannian metric](Metric.md#^RiemannianMetric) (i.e. with a [Riemannian structure](#^RiemannianStructure)) ^RiemannianManifold

A *Kähler manifold* is a [manifold](Topology.md#^TopoManifold) with a [symplectic structure](#^SymplecticStructure), a [complex structure](#^ComplexStructure), and a [Riemannian structure](#^RiemannianStructure). ^KahlerManifold

---
### Differential structures

A *differential structure* is an [equivalence class](Relation.md#^EquivalenceClass) of [differentiably equivalent](#^AtlasEquivalence) [atlases](#^DiffAtlas) or, equivalently, a unique [maximal atlas](#^MaximalAtlas). ^DiffStructure

A *smooth structure* is an [equivalence class](Relation.md#^EquivalenceClass) of [smoothly equivalent](#^AtlasSmoothEquivalence) [atlases](#^DiffAtlas) or, equivalently, a unique [maximal](#^MaximalAtlas) [smooth](#^SmoothAtlas) atlas. ^SmoothStructure

A *complex structure* is an [equivalence class](Relation.md#^EquivalenceClass) of [holomorphically equivalent](#^AtlasEquivalence) [atlases](#^DiffAtlas) or, equivalently, a unique [maximal](#^MaximalAtlas) [holomorphic](#^HolomorphicAtlas) atlas. ^ComplexStructure

A *symplectic structure* is an assignment of a [symplectic form](Linear%20map.md#^SymplecticForm) to a [smooth manifold](#^SmoothManifold). ^SymplecticStructure

A *Riemannian structure* is an assignment of a [Riemannian metric](Metric.md#^RiemannianMetric) to a [smooth manifold](#^SmoothManifold). ^RiemannianStructure

---
### Differentiable atlases

A *differentiable atlas* is either a $C^k$[-atlas](#^CkAtlas), a [smooth atlas](#^SmoothAtlas), an [analytic atlas](#^AnalAtlas), or a [holomorphic atlas](#^HolomorphicAtlas). ^DiffAtlas

A *$C^k$-atlas* is an [atlas](Topology.md#^Atlas) whose [transition functions](Topology.md#^TransitionFunction) are $C^k$[-differentiable](Function.md#^DifferentiabilityClass). ^CkAtlas

A *smooth atlas* is an an [atlas](Topology.md#^Atlas) whose [transition functions](Topology.md#^TransitionFunction) are [smooth](Function.md#^DifferentiabilityClass). ^SmoothAtlas

An *analytic atlas* is an an [atlas](Topology.md#^Atlas) whose [transition functions](Topology.md#^TransitionFunction) are [analytic](Function.md#^DifferentiabilityClass). ^AnalAtlas

A *holomorphic atlas* is an an [atlas](Topology.md#^Atlas) whose [transition functions](Topology.md#^TransitionFunction) are holomorphic. ^HolomorphicAtlas

---
#### Atlas equivalence

Two [atlases](Topology.md#^Atlas) $φ_i,ψ_j$ are *differentiably [equivalent](Relation.md#^EquivalenceClass)* if their union $φ_i\cup ψ_j$ forms a [differentiable atlas](#^DiffAtlas) of the same [differentiability class](Function.md#^DifferentiabilityClass) (this requires the [transition functions](Topology.md#^TransitionFunction) to be [differentiably compatible](#^ChartCompatibility)). ^AtlasEquivalence

Two [atlases](Topology.md#^Atlas) $φ_i,ψ_j$ are *$C^k$[-equivalent](Relation.md#^EquivalenceClass)* if their union $φ_i\cup ψ_j$ forms a $C^k$[-atlas](#^CkAtlas) (this requires the [transition functions](Topology.md#^TransitionFunction) to be $C^k$[-compatible](#^ChartCkCompatibility)). ^AtlasCkEquivalence

Two [atlases](Topology.md#^Atlas) $φ_i,ψ_j$ are *[smoothly equivalent](Relation.md#^EquivalenceClass)* if their union $φ_i\cup ψ_j$ forms a [smooth atlas](#^SmoothAtlas) (this requires the [transition functions](Topology.md#^TransitionFunction) to be [smoothly compatible](#^ChartSmoothCompatibility)). ^AtlasSmoothEquivalence

Two [atlases](Topology.md#^Atlas) $φ_i,ψ_j$ are *[holomorphically equivalent](Relation.md#^EquivalenceClass)* if their union $φ_i\cup ψ_j$ forms a [holomorphic atlas](#^HolomorphicAtlas) (this requires the [transition functions](Topology.md#^TransitionFunction) to be [holomorphically compatible](#^ChartHolomorphicCompatibility)). ^AtlasHolomorphicEquivalence

A *maximal differentiable atlas* is the union of all [differentiably equivalent](#^AtlasEquivalence) [atlases](Topology.md#^Atlas) of one [differentiability class](Function.md#^DifferentiabilityClass).. ^MaximalAtlas

---
#### Chart compatibility

Two [charts](Topology.md#^Chart) $φ:U\to φ(U)$ and $ψ\to ψ(W)$ are *differentiably compatible* if their images $φ(U),ψ(W)$ are [open](Topology.md#^OpenSet), and their [transition functions](Topology.md#^TransitionFunction) $ψφ^{-1}, φψ^{-1}$ share a [differentiability class](Function.md#^DifferentiabilityClass). ^ChartCompatibility

Two [charts](Topology.md#^Chart) $φ:U\to φ(U)$ and $ψ\to ψ(W)$ are *$C^k$-compatible* if their images $φ(U),ψ(W)$ are [open](Topology.md#^OpenSet), and their [transition functions](Topology.md#^TransitionFunction) $ψφ^{-1}, φψ^{-1}$ are  $C^k$[-differentiable](Function.md#^DifferentiabilityClass). ^ChartCkCompatibility

Two [charts](Topology.md#^Chart) $φ:U\to φ(U)$ and $ψ\to ψ(W)$ are *smoothly compatible* if their images $φ(U),ψ(W)$ are [open](Topology.md#^OpenSet), and their [transition functions](Topology.md#^TransitionFunction) $ψφ^{-1}, φψ^{-1}$ are [smooth](Function.md#^DifferentiabilityClass). ^ChartSmoothCompatibility

Two [charts](Topology.md#^Chart) $φ:U\to φ(U)$ and $ψ\to ψ(W)$ are *holomorphically compatible* if their images $φ(U),ψ(W)$ are [open](Topology.md#^OpenSet), and their [transition functions](Topology.md#^TransitionFunction) $ψφ^{-1}, φψ^{-1}$ are [holomorphic](Function.md#^DifferentiabilityClass). ^ChartHolomorphicCompatibility

---
### Manifold accessories

The *cotangent space* $T_x^*\M$ of a [smooth manifold](#^SmoothManifold) $\M$ at a point $x\in \M,$ is the [quotient space](Topology.md#^QuotientSpace) $I_x/I_x^2,$ where $I_x$ is the [ideal](Algebraic%20structure.md#^Ideal) of all [smooth functions](Function.md#^DifferentiabilityClass) $f\in C^\infty(\M):\M\to\rr$ such that $f(x)=0,$ and $I_x^2$ is the ideal of all functions $\sum_if_ig_i$ where $f_i,g_i\in I_x$. Both $I_x$ and $I_x^2$ are $\rr$[-vector spaces](Vector%20space.md#Vector%20space).
More intuitively, it is the [dual](Vector%20space.md#^DualSpace) of the [tangent space](#^TangentSpace) at $x,$ i.e. the space of cotangent [linear forms](Linear%20map.md#^LinearForm) at $x.$ ^CotangentSpace
 
The *tangent space* $T_x\M$ of a [smooth manifold](#^SmoothManifold) $\M$ at a point $x\in \M,$ is the [dual](Vector%20space.md#^DualSpace) of the [cotangent space](#^CotangentSpace) at $x.$
More intuitively, it is the [vector space](Vector%20space.md#Vector%20space) of tangent vectors at $x,$ which are [equivalence classes](Relation.md#^EquivalenceClass) of [paths](Topology.md#^TopoPath) that pass through $x,$ where paths $γ_1,γ_2$ are equivalent iff $(φ\circ γ_1)'=(φ\circγ_2)'$ for any [chart](Topology.md#^Chart) $φ.$ ^TangentSpace
 
A [function](Function.md#^Function) $f:\M\to\rr$ *belongs to $C^\infty(\M)$* if for every [chart](Topology.md#^Chart) $φ:U\to φ(U)$ for $U\subseteq\M,$ the map $f\circ φ^{-1}:φ(U)\to\rr,$ is [smooth](Function.md#^DifferentiabilityClass).
Note that $C^\infty(\M)$ is an [associative algebra](Algebraic%20structure.md#^AssAlgebra) over $\rr$ w.r.t. function sum, scalar multiplication, and function pointwise product. ^CooM