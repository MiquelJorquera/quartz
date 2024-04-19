---
tags:  Maths/Algebra/Linear_Algebra
---
# Metric

A *metric* is a [positive-semidefinite](Function.md#^PositiveSemidefiniteFunc), [symmetric function](Function.md#^Symmetric) $g:M\times M\to \mathbb{R}_{\geq 0}$ on a set $M$ such that for all $x,y\in M:$$$\begin{split}
g(x,y)&=0\implies (x=y)\\
g(x,z)&\leq g(x,y)+g(y,z)
\end{split}$$ ^Metric

A *metric space* is an ordered pair $(M,g)$ of a set $M$ and a [metric](#^Metric) $g$ on it.
It is usually endowed with the [metric topology](#^MetricTopology), making it a [topological space](Topology.md#^TopoSpace). ^MetricSpace

A [[Metric#^MetricSpace|metric space]] $(M,g)$ is *complete* if every [[Function#^CauchySequence|Cauchy sequence]] in $M$ has a limit in $M$. ^Complete

The *open ball* $B_r(x)$ of radius $r\in\rr^+$ centered at $x\in M$ in a [[#^MetricSpace|metric space]] $(M,g)$ is the set of points $y\in M$ whose distance from $x$ is less than $r:$$$B_r(x)\equiv \{ x\ |\ g(x,y)<r\}$$ ^OpenBall

The *metric topology* induced by a metric space is the [topology](Topology.md#Topology) consisting of all unions of its [open balls](#^OpenBall). ^MetricTopology

A *Riemannian metric* $g:T\M\times T\M\to\rr$ in a [smooth manifold](Differential%20geometry.md#^SmoothManifold) $\M,$ is the [metric](#^Metric) induced by assigning an [inner product](Linear%20map.md#^InnerProduct) $g_x:T_x\M\times T_x\M\to\rr$ to the [tangent space](Differential%20geometry.md#^TangentSpace) $T_x\M$ at every $x\in\M.$ ^RiemannianMetric