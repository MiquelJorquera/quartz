---
tags:  Maths/Logic/Set_theory 
---
# Set
A set is a formalization of the intuitive notion of a collection of *elements*, that are usually assumed to also be sets. If $x$ is an element of the set $X,$ we write it as $x\in X.$ Many such formalizations exist, based on first-order logic, and since I don't have opinions on it, I'll just stick with the most popular one, the ZFC axioms:
- **Extensionality:** Two sets are equal iff they have the same elements.
- **Regularity:** Every non-empty set $X$ contains a member $y$ such that $X$ and $y$ are [[#^Disjoint|disjoint]].
- **Axiom schema of specification:** There exists a [[#^Subset|subset]] of $X$ that can be specified as $\{ x\in X\ |\ φ(x) \},$ the set of elements of $X$ that obey a formula $φ(x)$ in the language of ZFC.
- **Pairing:** If $X$ and $Y$ are sets, there exists a set which contains $X$ and $Y$ as elements.
- **Union:** For any set of sets $\mathcal F,$ the [[#^Union|union]] $\cup\mathcal F$ exists.
- **Axiom schema of replacement:** The [[Function#^RangeImage|image]] of a set under any definable [[Function#^Function|function]] will be a [[#^Subset|subset]] of some set.
- **Infinity:** there exists a set with infinitely many members, all different from each other.
- **Power set**: The [[#^PowerSet|power set]] exists for every set.
- **Well-ordering:** Any set can be [[Relation#^WellOrdered|well-ordered]].

---
# Set theoretical definitions

A [set](#Set) $X$ is a *subset* of a set $Y$ iff every element of $X$ is an element of $Y.$ This is written $X\subseteq Y.$ ^Subset

A [[#^Subset|subset]] $X\subseteq Y$ is a *proper subset* if $X\neq Y.$ This is written $X\subset Y.$ ^ProperSubset

The *power set* $\mathcal P(X)$ of a [set](#Set) $X$ is the set of all [[#^Subset|subsets]] of $X.$ ^PowerSet

Two [sets](#Set) are *disjoint* if they share no elements. ^Disjoint

The *union* $\cup\mathcal F$ of a [set](#Set) of sets $\mathcal F$ is a set that contains every element of the members $X_i$ of $\mathcal F,$ and no other elements. We may also write $X_i\cup X_j,$ or $\bigcup_i X_i.$ ^Union

The *intersection* $\cap\mathcal F$ of a [set](#Set) of sets $\mathcal F$ is a set that contains all elements that are in every member $X_i$ of $\mathcal F,$ and no other elements. We may also write $X_i\cap X_j,$ or $\bigcap_i X_i.$ ^Intersection

The *complement* $X\backslash S$ of a [[#^Subset|subset]] $S\subseteq X$ of a [set](#Set) $X,$ is the set of elements of $X$ not in $S.$
If $X$ is known, we may write $\bar{S}.$ ^Complement

A *convex set* is a [[#^Subset|subset]] $C$ of a [[Vector space#Vector space|vector]]/[[Vector space#Affine spaces|affine]] space such that for any two points in $C,$ their [convex combination](Vector%20space.md#^ConvexCombination) (i.e. the straight line joining them) belongs to $C.$ ^ConvexSet

An element $c$ of a [convex set](#^ConvexSet) $C$ is *extremal* if it cannot be written as a non-trivial [convex combination](Vector%20space.md#^ConvexCombination) of some other elements. ^ExtremalElement

The *convex hull* $\mathrm{conv}(X)$ of a [set](#Set) $X$ is the smallest [[#^ConvexSet|convex set]] that contains it. ^ConvexHull

The *cardinality* $|A|$ of a [[#Set|set]] $A$ measures its number of elements.
$|A|=|B|$ if there is a [bijection](Function.md#^BijectiveFunc) $A\hooktwoheadrightarrow B.$
$|A|\leq|B|$ if there is an [injection](Function.md#^InjectiveFunc) $A\hookrightarrow B.$
$|A|<|B|$ if there is an [injection](Function.md#^InjectiveFunc) $A\hookrightarrow B$ and there is no [surjection](Function.md#^SurjectiveFunc) $A\twoheadrightarrow B.$ ^Cardinality

A [set](#Set) $A$ is *finite* if its [cardinality](#^Cardinality) is less than that of the natural numbers, $|A|<|\mathbb{N}|.$ ^FiniteSet

A [set](#Set) $A$ is *countably infinite* if its [cardinality](#^Cardinality) is equal to that of the natural numbers, $|A|=|\mathbb{N}|=\aleph_0.$ ^CountablyInfiniteSet

A [set](#Set) $A$ is *countable* if it is either [finite](#^FiniteSet) or [countably infinite](#^CountablyInfiniteSet), $|A|\le|\mathbb{N}|.$ ^CountableSet

A [set](#Set) $A$ is *uncountably infinite* if its [cardinality](#^Cardinality) is greater than that of the natural numbers, $|A|>|\mathbb{N}|.$ ^UncountablyInfiniteSet

The *Cartesian product* $A\times B$ of two [sets](#Set) $A$ and $B$ is the set of all ordered pairs $(a,b),$ where $a\in A$ and $b\in B.$ ^CartesianProduct