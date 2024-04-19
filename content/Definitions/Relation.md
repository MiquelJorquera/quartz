---
tags:  Maths/Logic/Set_theory
---
An $n$-ary *relation* over the [sets](Set.md#Set) $X_1,...,X_n$ is a [subset](Set.md#^Subset) of $X_1×...×X_n.$ ^Relation

A *binary relation* over the [sets](Set.md#Set) $A,B$ is a [subset](Set.md#^Subset) of $A×B.$ ^BinaryRelation

Example: $A$ are people, $B$ are objects. The relation "owns" (different from "is owned by") is defined by the list of pairs $(a,b)$ that satisfy "$a$ owns $b$".

A *homogeneous relation* is a [[#^BinaryRelation|binary relation]] over the same [sets](Set.md#Set) $X,X.$ ^BinaryRelHomogeneous

A [[#^BinaryRelHomogeneous|homogeneous relation]] over $X$ is *reflexive* if it contains $(x,x)$ for all $x\in X.$ ^BinaryRelReflexive

A [[#^BinaryRelHomogeneous|homogeneous relation]] over $X$ is *irreflexive* if it does not contain $(x,x)$ for any $x\in X.$ ^BinaryRelIrreflexive

A [[#^BinaryRelHomogeneous|homogeneous relation]] over $X$ is *symmetric* if $(x,y)\iff(y,x)$ for all $x,y\in X.$ ^BinaryRelSymmetry

A [[#^BinaryRelHomogeneous|homogeneous relation]] over $X$ is *asymmetric* if $(x,y)\implies\cancel{(y,x)}$ for all $x,y\in X.$ ^BinaryRelAsymmetry

A [[#^BinaryRelHomogeneous|homogeneous relation]] over $X$ is *antisymmetric* if $(x,y)\wedge(y,x)\implies (x=y).$  ^BinaryRelAntisymmetry

A [[#^BinaryRelHomogeneous|homogeneous relation]] over $X$ is *transitive* if $(x,y)\wedge(y,z)\implies(x,z)$ for all $x,y,z\in X.$ ^BinaryRelTransitive

An [[Relation#Equivalence relation|equivalence relation]] $\sim$ on a [set](Set.md#Set) $X$ splits $X$ into *equivalence classes* $[x]=\{x_i\in X\ |\ x_i\sim x\}.$ ^EquivalenceClass

A *total order* is a [[#Partial order|partial order]] on a [set](Set.md#Set) $X$ in which any two elements are comparable, i.e. $x\leq y$ or $y\leq x$ for all $x,y\in X.$
Every non-empty totally ordered set is a [directed set](#^DirectedSet) ^TotalOrder

A [totally ordered](#^TotalOrder) [set](Set.md#Set) $X$ is *well-ordered* if every non-empty subset of $X$ has a least element. ^WellOrdered

A *directed set* $D$ is a [preordered](#Preorder) [set](Set.md#Set) in which every [finite](Set.md#^FiniteSet) subset $A\subseteq D$ has an upper bound, i.e. a $c\in D$ such that $c\geq a$ for all $a\in A.$ ^DirectedSet

A *causal set*, or *locally finite poset* $C$, is a [set](Set.md#Set) with a [partial order](#Partial%20order) $\preceq$ such that $$\{y\in C\ |\ x\preceq y \preceq z  \}$$ is [finite](Set.md#^FiniteSet) for all $x,z\in C.$ ^CausalSet

---
# Equivalence relation
[[#^BinaryRelHomogeneous|Homogeneous relation]] $\sim$ that is:
- [[Relation#^BinaryRelReflexive|Reflexive]]: $a\sim a$
- [[Relation#^BinaryRelTransitive|Transitive]]: $a\sim b\sim c\implies a\sim c$
- [[Relation#^BinaryRelSymmetry|Symmetric]]: $a\sim b\iff b\sim a$

# Preorder
[[#^BinaryRelHomogeneous|Homogeneous relation]] $\lesssim$ that is:
- [[Relation#^BinaryRelReflexive|Reflexive]]: $a\lesssim a$
- [[Relation#^BinaryRelTransitive|Transitive]]: $a\lesssim b\lesssim c\implies a\lesssim c$ 

# Partial order
[[#^BinaryRelHomogeneous|Homogeneous relation]] $\leq$ that is:
- [[Relation#^BinaryRelReflexive|Reflexive]]: $a\leq a$
- [[Relation#^BinaryRelTransitive|Transitive]]: $a\leq b\leq c\implies a\leq c$ 
- [[Relation#^BinaryRelAntisymmetry|Antisymmetric]]: $(a\leq b)\wedge (b\leq a)\implies (a=b).$

# Strict partial order/Strict preorder
[[#^BinaryRelHomogeneous|Homogeneous relation]] $<$ that is:
- [[Relation#^BinaryRelReflexive|Irreflexive]]: $a\nless a$
- [[Relation#^BinaryRelTransitive|Transitive]]: $a\leq b\leq c\implies a\leq c$ 
As a consequence, it is [[Relation#^BinaryRelAsymmetry|asymmetric]]: $a< b\implies b\nless a.$
