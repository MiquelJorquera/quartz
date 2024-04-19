---
tags:  Maths/Topology
---
# Topology
A topology $τ$ on $X$ is a [[Set#Set|set]] of [[Set#^Subset|subsets]] of $X$ such that for all $τ_i\in τ:$$$\begin{split}
X,\varnothing&\in τ\\
\bigcup_{i}τ_i&\in τ\\
\bigcap_{i<\infty}τ_i &\in τ\\
\end{split}$$ ^Topology

*Open sets* in $(X,τ)$ are elements $τ_i\inτ$ of the [[#^Topology|topology]] on $X.$ ^OpenSet

*Closed sets* in $(X,τ)$ are the [[Set#^Complement|complements]] $X\setminus τ_i$ of [[#^OpenSet|open sets]] $τ_i.$ ^ClosedSet

*Clopen sets* in $(X,τ)$ are sets that are both [[#^OpenSet|open]] and [[#^ClosedSet|closed]] in $(X,τ).$
$\varnothing$ and $X$ are always clopen in $(τ,X).$ ^ClopenSet

---
# Topological space

A *topological space* $(X,τ)$ consists of a set $X$ and a [[#^Topology|topology]] $τ$ on $X.$
If $τ$ is unimportant or obvious, $X$ may be called the topological space. ^TopoSpace

A [[#^TopoSpace|topological space]] $X$ is *connected* iff it doesn't have any [[#^ClopenSet|clopen]] sets other than $\varnothing$ and $X.$ ^ConnectedTopoSpace

A [[#^TopoSpace|topological space]] is *path-connected* if any two points in it can be connected by a [paths](#^TopoPath). ^PathConnected

A [[#^TopoSpace|topological space]] is *simply connected* if it is [path-connected](#^PathConnected) and all [paths](#^TopoPath) are [homotopic](Function.md#^Homotopy). ^SimplyConnected

A [[#^TopoSpace|topological space]] $X$ is *discrete* iff every subset $x_i\subseteq X$ is [[#^ClopenSet|clopen]]. ^DiscreteTopoSpace

A [[#^TopoSpace|topological space]] $X$ is *Hausdorff* if every pair of points $x_1,x_2\in X$ have disjoint [[#^OpenSet|open]] [[#^Neighbourhood|neighbourhoods]]. ^Hausdorff

A [[#^TopoSpace|topological space]] $X$ is *(quasi)compact* if every [[#^OpenCover|open cover]] of $X$ has a finite [subcover](#^Subcover). ^Quasicompact

A [[#^TopoSpace|topological space]] is *compact* if it is [[#^Quasicompact|quasicompact]] and [[#^Hausdorff|Hausdorff]]. ^Compact

A [[#^TopoSpace|topological space]] $X$ is *locally compact* if every point $x\in X$ has a [[#^Quasicompact|quasicompact]] [[#^Neighbourhood|neighbourhood]]. ^LocallyCompact

A [[#^TopoSpace|topological space]] is *second-countable*, or *completely separable*, if it has a [countable](Set.md#^CountableSet) [base](#^Base). ^SecondCountable

A [topological space](#^TopoSpace) is *locally Euclidean* if every point has a [neighbourhood](#^Neighbourhood) which is [homeomorpic](Morphisms.md#^Homeomorphism) to $\rr^n$ or to an open ball in $\rr^n$ for some $n\in\mathbb{Z}^{\ge0}$ ^LocallyEuclideanTopoSpace

A *topological subspace* $(S,τ_S)$ is a subset $S\subseteq X$ of a [[Topology#^TopoSpace|topological space]] $(X,τ)$, equipped with the [[#^SubspaceTopo|subspace topology]] $τ_S.$ ^TopoSubspace

An $n$-dimensional *topological manifold* is a [locally Euclidean](#^LocallyEuclideanTopoSpace) (all points have a [neighborhood](#^Neighbourhood) homeomorphic ro $\rr^n)$ [Hausdorff space](#^Hausdorff). ^TopoManifold

## Topological space accessories

A *path* in a [[Topology#^TopoSpace|topological space]]  $X$ is a [[Function#^ContinuousFunction|continuous function]] $γ:[0,1]\to X.$ ^TopoPath

A *cover* of a [[Topology#^TopoSpace|topological space]]  $X$ is a set of subsets $\{U_α\subseteq X\}$ such that $\bigcup_α U_α=X.$ ^Cover

A *cover* of a [topological subspace](#^TopoSubspace)  $S\subseteq X$ is a set of subsets $\{U_α\subseteq X\}$ such that $S\subseteq\bigcup_α U_α.$ ^CoverSubspace

An *open cover* of a [[Topology#^TopoSpace|topological space]]  $(X,τ)$ is a set of [[Topology#^OpenSet|open subsets]] $\{U_α\in τ\}$ such that $\bigcup_α U_α=X.$ ^OpenCover

An *open cover* of a [topological subspace](#^TopoSubspace)  $(S,τ_S)\subseteq (X,τ)$ is a set of [[Topology#^OpenSet|open subsets]] $\{U_α\in τ\}$ such that $S\subseteq\bigcup_α U_α.$ ^OpenCoverSubspace

A *subcover* $\{U_β\}$ of a [cover](#^Cover) $\{U_α\}$ of $X$ is a subset $\{U_β\}\subseteq\{U_α\}$ that still covers $X:$ $\bigcup_β U_β=X.$ ^Subcover

A *quotient space* $X/{\sim},$ where $\sim$ is an [[Relation#Equivalence relation|equivalence relation]] on the [[Topology#^TopoSpace|topological space]] $(X,τ)$ is a topological space whose points are the [[Relation#^EquivalenceClass|equivalence classes]] $[x]$ of $X$, and whose sets are [[#^OpenSet|open]] iff they come from open sets in $X.$ $(U$ is open in $X/{\sim}$ iff $\{x\in τ\ |\ [x]\in U\}).$ ^QuotientSpace

A *neighbourhood* of a subset $S\subseteq X$ of a [[Topology#^TopoSpace|topological space]] $(X,τ)$ is a subset $V\subseteq X$ that contains an [[Topology#^OpenSet|open set]] $τ\ni U\subseteq V$ that contains $S:$
$$S\subseteq U\subseteq V\subseteq X$$ ^Neighbourhood

An *open neighbourhood* $V$ of a subset $S\subseteq X$ of a [[Topology#^TopoSpace|topological space]] $(X,τ)$ is an [[Topology#^OpenSet|open set]] $V\in τ$ that contains $S:$
$$S\subseteq V\subseteq X$$ ^OpenNeighbourhood

The *closure* $A^\mathrm{cl}$ of a [[Set#^Subset|subset]] $A\subseteq X$ of a [[Topology#^TopoSpace|topological space]] $X$ is the [[Set#^Intersection|intersection]] of all [[#^ClosedSet|closed sets]] of $X$ that contain $A.$ 
I.e. the smallest closed set that contains $A.$ ^Closure

A *dense subset* of a [[Topology#^TopoSpace|topological space]] $X$ is a [[Set#^Subset|subset]] whose [[#^Closure|closure]] is $X.$ ^DenseSubset

A *dense subspace* of a [[Topology#^TopoSpace|topological space]] $X$ is a [[#^TopoSubspace|topological subspace]] whose [[#^Closure|closure]] is $X.$ ^DenseSubspace

A map $f:X\to Y$ between [topological spaces](#^TopoSpace) is *densely defined* if $X$ is a [dense subset](#^DenseSubset) of $Y.$ ^DenselyDefinedMap

A *chart*, or *coordinate patch* $φ:U\toφ(U)$ for a [topological space](#^TopoSpace) $X$ is a [homeomorphism](Morphisms.md#^Homeomorphism) from an [open](#^OpenSet) subset $U\subseteq X$ into an open subset $φ(U)\subseteq\rr^n.$ ^Chart

A *transition function* $ψφ^{-1}:φ(U\cap V)\to ψ(U\cap V)$ between two [charts](#^Chart) $φ,ψ$ with overlapping [domains](Function.md#^Domain) $U,V$ is a [homeomorphism](Morphisms.md#^Homeomorphism) between open subsets of $\rr^n.$ ^TransitionFunction

An *atlas* of a [topological space](#^TopoSpace) $X$ is a collection of [charts](#^Chart) $φ_i$ that [covers](#^OpenCover) $X.$ ^Atlas

A *base*, or *basis* $\B$ for the [topology](#^Topology) $τ$ of a [topological space](#^TopoSpace) $(X,τ),$ is a subset $\B\subseteq τ$ such that every $τ_i\in τ$ is a union $τ_i=\bigcup_j B_j$ of some collection of *basic sets* $B_j\in\B.$ ^Base

# Specific topologies

The *subspace topology* $τ_S$ of a subset $S\subseteq X$ of a [[Topology#^TopoSpace|topological space]] $(X,τ)$ is the set of [open sets](#^OpenSet) in $τ$ that are also in $S:$$$τ_S\equiv \{ S\capτ_i\ |\ τ_i\in τ \}$$ ^SubspaceTopo

The *metric topology* on a [[Metric#^MetricSpace|metric space]] $(M,g)$ is the set of all [[Set#^Subset|subsets]] of $M$ that are the [[Set#^Union|union]] of [[Metric#^OpenBall|open balls]] in $M.$ ^MetricTopo

The *norm topology* on a [[Vector space#^Normed|normed space]] $V$ is the [[#^MetricTopo|metric topology]] induced by the [[Function#^Norm|induced]] [[Metric#^Metric|metric]] $g(u,v)\equiv|u-v|.$ ^NormedTopo

## Operator topologies

If we have a [sequence](Function.md#^Sequence) $T_n\in B(\B)$ of [operators](Linear%20map.md#^LinearOperator) on the [Banach space](Vector%20space.md#^Banach) $\B,$ the statement "$T_n$ converges to the operator $T\in\B$" will have different meanings depending on the chosen [topology](#^Topology).

A [topology](#^Topology) is usually called strong if it has many open sets, and weak if it has few, so that sequences will [strongly converge](Function.md#^StrongConvergence) or [weakly converge](Function.md#^WeakConvergence) respectively.

$T_n\to T$ in the uniform operator topology (a.k.a. norm topology, the strongest topology of them all) means that $T_n$ [strongly converges](Function.md#^StrongConvergence) to $T,$ i.e. $|T_n-T|\to 0.$

$T_n\to T$ in the strong operator topology means that $T_n x\to Tx$ for all $x\in\B.$ ^StrongOpTopo

$T_n\to T$ in the weak topology means that $F(T_n x)\to F(Tx)$ for all $x\in\B$ and all [distributions](Linear%20map.md#^Distribution) $F.$ ^WeakTopo

$T_n\to T$ in the ultraweak operator topology means that $\lim_{n \to 0}\tr(T_n t)\to \tr(Tt)$ for all [trace-class](Linear%20map.md#^TraceClass) $t\in\T(\B).$ ^UltraweakTopo

