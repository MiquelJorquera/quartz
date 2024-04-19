---
tags:
  - Maths/Topology
---
# Fiber bundle

A *fiber bundle* is a structure $(E,B,π ,F),$ where $E,B,F$ are [topological spaces](Topology.md#^TopoSpace), and $π :E\to B$ is a [continuous](Function.md#^ContinuousFunction) [surjection](Function.md#^SurjectiveFunc) satisfying the *local triviality* condition, which roughly says that $E$ must locally look like $B\times F.$

The [connected](Topology.md#^ConnectedTopoSpace) space $B$ is called the *base space* of the bundle, $E$ the *total space*, and $F$ the *fiber*. The map $π$ is called the *projection map*, or *bundle projection*.

For every [open neighbourhood](Topology.md#^OpenNeighbourhood) $U\subseteq B,$ there is a [homeomorphism](Morphisms.md#^Homeomorphism) $φ :π^{-1}(U)\to U\times F$ such that it composes with the *natural projection* $\text{proj}_1:U\times F\to U$ into the projection map: $φ\circ\text{proj}_1=π.$ More visually, this diagram commutes:
![](Local%20triviality.png)
So for all $b\in B,$ the [preimage](Function.md#^Preimage) $π^{-1}(b)$ is homeomorphic to $F$ (since this is true of $\operatorname {proj}_1^{-1}(b)$ )and is called the *fiber over* $b.$

The [set](Set.md#Set) of all $\{(U_i,φ_i)\}$ is called a *local trivialization* of the bundle.

# Types of fiber bundles

A *trivial bundle* is a [fiber bundle](#Fiber%20bundle) where $E=F\times B,$ and so $π=\text{proj}_1$ ^TrivialBundle

A $G$*-bundle* is a [fiber bundle](#Fiber%20bundle) with [structure group](#^StructureGroup) $G.$ ^GBundle

A *principal $G$-bundle* is a [fiber bundle](#Fiber%20bundle) whose fiber is a [principal homogeneous G-space](Action.md#^Torsor) (i.e. a $G$-torsor). ^PrincipalBundle

A *covering space* of a [topological space](Topology.md#^TopoSpace) $X$ is a [fiber bundle](#Fiber%20bundle) $(E,X,p,F)$ with discrete fibers, i.e. $p^{-1}(x)$ is a [discrete space](Topology.md#^DiscreteTopoSpace) for all $x\in X.$
$p$ is called the *covering map.* ^CoveringSpace

A *universal cover* is a cover whose [covering space](#^CoveringSpace) is [simply connected](Topology.md#^SimplyConnected). ^UniversalCover

The *tangent bundle* $T\M$ of a [differentiable manifold](Differential%20geometry.md#^DiffManifold) $\M$ is the disjoint union $\bigsqcup _{x\in M}T_x\M$ of all [tangent spaces](Differential%20geometry.md#^TangentSpace) of $\M.$
As a [fiber bundle](#Fiber%20bundle), it is a type of [vector bundle](#^VectorBundle) $(T\M,\M,π,V),$ where the projection map $π:T\M\to\M$ takes a tangent space $T_x\M$ and returns $x.$ ^TangentBundle

A *vector bundle* is a [fiber bundle](#Fiber%20bundle) in which the fibers $E_b\equiv π^{-1}(b)$ at every $b\in B$ are [isomorphic](Morphisms.md#^Isomorphism) to a [vector space](Vector%20space.md#Vector%20space) $V,$ such that the local triviality condition becomes$$φ_b: E_b\overset{φ_{E_b}}{\longrightarrow}\{b\}\times V\overset{\text{proj}_1}{\longrightarrow} V$$and preserves the vector structure of $E_b$ :$$φ_b(kv+_{E_b}\ell w)=kφ_b(v)+_Vφ_b(w)$$ (e.g. $φ_b(x)=x+1$ doesn't work) ^VectorBundle

# Fiber bundle accessories

The *structure group* $G$ of a [fiber bundle](#Fiber%20bundle) $(E,B,π,F)$ is a [topological group](Algebraic%20structure.md#^TopoGroup) which [acts](Action.md#^GroupAction) ([faithfully](Action.md#^FaithfulAction)) on the fiber $F,$ such that there exist [transition functions](#^TransitionFunctionBundle) $g_{ij}:U_i\cap U_j\to G.$
$G$ is always a [subgroup](Algebraic%20structure.md#^Subgroup) of $\operatorname{Homeo}(F).$ ^StructureGroup

*Transition functions* $g_{ij}:U_i\cap U_j\to G$ in a [fiber bundle](#Fiber%20bundle) are [continuous](Function.md#^ContinuousFunction) [invertible](Function.md#^InvertibleFunc) transformations of the fiber $F.$
For all fibers $e\in π^{-1}(U_i\cap U_j)$ they obey $g_{ij}(π(e))· φ_i(e)=φ_j(e).$
For all points $b\in U_i\cap U_j\cap U_k,$ they compose as $g_{ij}(b)g_{jk}(b)=g_{ik}(b)$ (*cocycle condition*). ^TransitionFunctionBundle

A *global section* of a [fiber bundle](#Fiber%20bundle) $(E,B,π,F)$ is a [continuous](Function.md#^ContinuousFunction) map $σ:B\to E,$ such that $π(σ(b))=b$ for all $b\in B.$ ^GlobalSectionBundle

A *local section* of a [fiber bundle](#Fiber%20bundle) $(E,B,π,F)$ is a [continuous](Function.md#^ContinuousFunction) map $σ:U\to E,$ where $U$ is an [open neighbourhood](Topology.md#^OpenNeighbourhood) of $B,$ such that $π(σ(b))=b$ for all $b\in U.$ ^LocalSectionBundle