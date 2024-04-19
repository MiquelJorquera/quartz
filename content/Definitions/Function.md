---
tags:  Maths/Logic/Set_theory
---
A *function* is a [[Relation#^BinaryRelation|binary relation]] $f:X\to Y$ that is *functional*, a.k.a. *right-unique*:
Each element of the [[Function#^NaturalDomainOfDefinition|domain of definition]] $S\subseteq X$ goes to one element of $Y.$ 
It is usual to call a [[#^TotalFunction|total function]] a "function". ^Function

The *domain* of a [[#^Function|function]] $f:X\to Y$ is the [set](Set.md#Set) $X\equiv\mathrm{Dom}(f).$ ^Domain

The *codomain* of a [[#^Function|function]] $f:X\to Y$ is the [set](Set.md#Set) $Y.$ ^Codomain

The *natural domain*, or *domain of definition*, of a [[#^Function|function]] $f:X\to Y$ is the [subset](Set.md#^Subset) $S\subseteq X$ of the [[#^Domain|domain]] consisting of the elements at which $f$ can be evaluated. ^NaturalDomainOfDefinition

The *range*, or *image*, of a [[#^Function|function]] $f:X\to Y$ is the [subset](Set.md#^Subset) $f(X)\subseteq Y$ of the [[#^Codomain|codomain]] to which $f$ actually outputs values. ^RangeImage

The *preimage* $f^{-1}(B)$ of a [set](Set.md#Set) $B\subseteq Y$ under a [[#^Function|function]] $f:X\to Y,$ is the [subset](Set.md#^Subset) of elements $x\in X$ that get evaluated to $B:$$$f^{-1}(B)\equiv\{x\ |\ f(x)\in B\}$$ ^Preimage

---
# Function types

A *partial function* is a [[#^Function|function]] in which $S\subset X.$
I.e. the [[#^NaturalDomainOfDefinition|domain of definition]] is a [[Set#^ProperSubset|proper subset]] of the [[#^Domain|domain]]. ^PartialFunction

A *total function*  is a *serial*, or *left-total*, [[#^Function|function]], in which $S=X.$
I.e. the [[#^NaturalDomainOfDefinition|domain of definition]] is the [[#^Domain|domain]]. ^TotalFunction

A [[#^Function|function]] $f:(X\times \dots\times Y)\to Z$ of several variables is *symmetric* if it is independent of the order of the arguments. E.g, $f(x,y)=f(y,x).$ ^Symmetric

A [[#^Function|function]] $f:(X\times \dots\times Y)\to Z$ of several variables is *antisymmetric* if it changes sign under permutation of two arguments. E.g, $f(x,y)=-f(y,x).$ ^Antisymmetric

A [function](#^Function) $f:X\to Y$ is *invertible* if there exists a function $f^{-1}:Y\to X$ such that$$\begin{split}
f^{-1}(f(x)) &= 1_X\\
f(f^{-1}(y)) &= 1_Y
\end{split}$$for all $x\in X$ and $y\in Y.$
$f^{-1}$ is called the *inverse function* of $f,$ and it is unique.
Invertible functions are [bijective](#^BijectiveFunc), and vice versa. ^InvertibleFunc

An *involution* $f=f^{-1}$ is a self-[inverse](#^InvertibleFunc) ([[#^BijectiveFunc|bijective]]) [[#^Function|function]]: $f(f(x))=x.$ ^Involution

A [[#^Function|function]] $f:X\to Y$ between [[Topology#^TopoSpace|topological spaces]] is *continuous* if the pre-[[#^RangeImage|image]] $f^{-1}(V)$ of every [[Topology#^OpenSet|open]] $V\subseteq Y,$ is open.
I.e. open subsets come from open subsets. ^ContinuousFunction

A [[#^ContinuousFunction|continuous function]] $f:X\to Y$ between [[Topology#^TopoSpace|topological spaces]] is *strongly continuous* if the [[#^RangeImage|image]] $f(U)$ of every [[Topology#^OpenSet|open]] $U\subseteq X,$ is open.
I.e. open subsets $\longleftrightarrow$ open subsets. ^StronglyContinuousFunction

Let $f,g:X\to Y$ be [continuous functions](#^ContinuousFunction). A *homotopy* is a continuous function $F:X\times[0,1]\to Y,$ written as $F_s(x),$ such that$$\begin{split}
F_0(x)&=f(x)\\
F_1(x)&=g(x)
\end{split}$$A homotopy is more relaxed than a homeomorphism, allowing to compress large spaces into points. ^Homotopy

A [[#^Function|function]] $f:(X,Σ)\to(Y,\mathrm{Τ})$ between [[Measure#^MeasurableSpace|measurable spaces]] (often abbreviated as $f:X\to Y)$ is *measurable* if the pre-[[#^RangeImage|image]] of every $τ\in \mathrm{Τ}$ is in $Σ:$$$f^{-1}(τ)\in Σ$$This condition can also be written as $f^{-1}(\mathrm{Τ})\subseteq Σ.$  ^MeasurableFunction

A [function](#^Function) $f:X\to\mathbb K$ is *simple* if it can be written as $f=\sum_k c_k χ_{A_k},$ where $c_k\in\mathbb K,$ and $χ_A$ is the [indicator function](#^IndicatorFunction) of $A,$ which is a [measurable](Measure.md#^MeasurableSpace) set of $X,$ and where the different $A_k$ are [disjoint](Set.md#^Disjoint). ^SimpleFunction

(MY OWN DEFINITION!) A *positive-semidefinite function* is a [[#^Function|function]] $f:X\to\rr_{\geq 0}$ for any set $X.$ ^PositiveSemidefiniteFunc

(MY OWN DEFINITION!) A *positive-definite function* is a [[#^PositiveSemidefiniteFunc|positive-semidefinite]] [[#^Function|function]] $f:X\to\rr_{\geq 0}$ such that
$$\big(f(x)=0\big)\iff\big(x=\varnothing\big)$$ ^PositiveDefiniteFunc

The *smoothness*, or *differentiability class,* of a real [function](#^Function) $f:U\to\rr$ is a measure of the highest order of derivative that $f$ has and is continuous on its ([open](Topology.md#^OpenSet)) domain $U\subseteq\rr .$
A $C^k$ function has continuous derivatives up to order $k\in\mathbb{Z}.$
A $C^\infty,$ or *smooth,* function has continuous derivatives of all orders.
A $C^ω,$ or *analytic* function is smooth and its Taylor expansion around a point converges to $f$ at that point. ^DifferentiabilityClass

## Sequences

A *sequence* is a [[#^Function|function]] $f:\mathbb Z\to X$ whose [[#^NaturalDomainOfDefinition|domain of definition]] is an interval of integers.
Intuitively, it's just an ordered set of mathematical objects.
The output is usually written $f_n$, rather than $f(n).$ ^Sequence

An *exact sequence* is a [[#^Sequence|sequence]] of [morphisms](Morphisms.md#^Morphism) between objects of an commutative category such that the [[#^RangeImage|image]] of one morphism equals the [[Morphisms#^Kernel|kernel]] of the next. ^ExactSequence

A *short exact sequence* is an [[#^ExactSequence|exact sequence]] of the form $0\to A\xrightarrow{f}B\xrightarrow{g}C\to 0$. 0 does *not* go to $A.$ Rather, 0 goes to the identity of $A.$ It can be equivalently written as $A\xhookrightarrow{f}B\xtwoheadrightarrow{f} C$ can be shown that the first two maps are injections, and the last two are surjections. ^ShortExactSequence

A *Cauchy sequence* $f$ is a [[#^Sequence|sequence]] whose [[#^Codomain|codomain]] is a [[Metric#^MetricSpace|metric space]] $(M,g),$ such that for every $\e\in\rr^+,$ there is an integer $N$ such that $g(f_a,f_b)<\e$ for all integers $a,b>N.$ 
I.e. the points get closer and closer together, and converge to a limit. ^CauchySequence

A [sequence](#^Sequence) $x_n$ in a [complete](Metric.md#^Complete) [metric space](Metric.md#^MetricSpace) $(M,g)$ is *convergent* to $x\in X$ if$$\lim_{ n \to \infty } g(x_n,x)=0$$ ^Convergence

A [sequence](#^Sequence) $x_n$ in a [Banach space](Vector%20space.md#^Banach) $B$ is *strongly convergent* to $x\in X$ if$$\lim_{ n \to \infty } |x_n-x|=0$$ ^StrongConvergence

A [sequence](#^Sequence) $x_n$ in a [Banach space](Vector%20space.md#^Banach) $B$ is *weakly convergent* to $x\in B$ if$$\lim_{n\to \infty } f(x_n) = f(x) $$for any [linear functional](Linear%20map.md#^LinearForm) $f\in B^*.$ If $B$ is a [Hilbert space](Vector%20space.md#^Hilbert), the condition becomes$$\lim_{ n \to \infty } \langle x_n,y \rangle =\langle x,y \rangle $$for all $y\in B.$ ^WeakConvergence

## Forms

A *form* is a [[#^Function|function]] $f:(V\times V\times\dots\times V)\to K$ for a $K$-[[Vector space#Vector space|vector space]] $V.$ ^Form

A *positive-semidefinite form* for an $\rr$-[[Vector space#Vector space|vector space]] $V$ is a [[#^Form|form]] $f:(V\times V\times\dots\times V)\to \rr_{\geq 0}.$ ^PositiveSemidefinite

A *positive-definite form* is a [[#^PositiveSemidefinite|positive-semidefinite]] [[#^Form|form]] $f:(V\times V\times\dots\times V)\to \rr_{\geq 0}$ for an $\rr$-[[Vector space#Vector space|vector space]] $V$ such that$$
\big(f(v,v,...,v)=0\big)\implies \big(v=\vec{0}\big)$$ ^PositiveDefiniteForm

A *top-form* is an $n$-[form](#^Form) in an $n$-dimensional manifold. ^TopForm

An *exact form* $α$ is a [form](#^Form) that obeys $α=dβ.$ ^ExactForm

An *closed form* $α$ is a [form](#^Form) that obeys $dα=0.$ ^ClosedForm

## Jectivity

A [[#^Function|function]] $f$ is *injective* (written $f:X\hookrightarrow Y$) if it preserves distinctness:
$$\big( f(a)=f(b)\big)\implies(a=b)$$
![Picture|500](Jectivity.png)
 ^InjectiveFunc

A [[#^Function|function]] $f$ is *surjective* (written $f:X\twoheadrightarrow Y$) if its [[#^RangeImage|image]] equals its [[#^Codomain|codomain]] (it paints the whole canvas):
$$f(X)=Y$$
![Picture|500](Jectivity.png) ^SurjectiveFunc

A [[#^Function|function]] $f$ is *bijective* (written $f:X\hooktwoheadrightarrow Y$) if it is [[#^InjectiveFunc|injective]] and [[#^SurjectiveFunc|surjective]].
![Picture|500](Jectivity.png)
Bijective functions are [invertible](#^InvertibleFunc), and vice versa. ^BijectiveFunc

---

# Specific functions

The *indicator function* $χ_X:S\to \{0,1\}$, where $X\subseteq S,$ is a [[#^Function|function]] given by$$χ_X(x)=\begin{cases}
1 \quad \text{if } x\in     X\\
0 \quad \text{if } x\notin X
\end{cases}$$Useful properties:$$χ_X(x+y)=χ_{X-y}(x)=χ_{X-x}(y).$$
 ^IndicatorFunction

A *norm* is a [positive-definite form](#^PositiveDefiniteForm) $\lvert ·\rvert:V\to \rr_{\ge0}$ on a $\mathbb K$-[[Vector space#Vector space|vector space]] $V$ such that:$$\begin{split}
|u+v|&\leq|u|+|v|\\
|kv|&=|k||v|
\end{split}$$It induces a canonical [[Metric#^Metric|metric]] $g(v,w)\equiv\lvert w-v \rvert.$ ^Norm



A *seminorm* is a [[#^PositiveSemidefinite|positive-semidefinite]] [[Function#^Form|form]] $p:V\to \mathbb{R}$ on a $\mathbb K$-[[Vector space#Vector space|vector space]] $V$ such that:$$\begin{split}
p(u+v)&\leq(u)+(v)\\
p(kv)&=|k|p(v)
\end{split}$$ ^Seminorm

The *$L^p$-norm* $\|·\|_p$ of a [[#^MeasurableFunction|measurable function]] $f:X\to\mathbb K$ on the [[Measure#^MeasureSpace|measure space]] $(X,Σ,μ)$ is given by$$\|f\|_p\equiv\left(\int_X |f|^p \, dμ \right)^{\frac1p}$$ for $0<p<\infty.$ It can also be defined for $p=\infty.$ ^LpNorm

The *Fourier transform* $\tilde{f}:\rr\to\C$ of the [integrable](Measure.md#^LebesgueSimpleInt) [[#^Function|function]] $f:\rr\to\C$ is given by$$\tilde f(k) = \int_{\rr^n}f(x)e^{-ik·x}dx^n$$ and its inverse is $$f(x) = \int_{\rr^n}\tilde f(k) e^{ik·x}\frac{dk^n}{τ^n}$$ ^Fourier

The *convolution* $f*g$ of two [integrable](Measure.md#^LebesgueSimpleInt) [functions](#^Function) $f$ and $g$ is a function given by summing all $f(y)g(z)$ as $x=y+z$ remains fixed:$$\begin{split}
 (f*g)(x)
 &\equiv\int_\rr f(y)g(x-y)  \, dy\\
 &\equiv\int_\rr f(x-y)g(y)  \, dy\\
\end{split}$$ Convolutions [commute](Operation.md#^Commutativity): $(f*g=g*f),$ [associate](Operation.md#^Associativity): $(f*(g*h)=(f*g)*h),$ and [distribute](Operation.md#^Distributive) over $+:$ $(f*(g+h)=(f*g)+(f*h)).$ ^Convolution

Convolution properties:$$\begin{split}
\int_\rr (f*g)(x) \, dx &= \l\int_\rr f(x) \, dx \r\l\int_\rr g(x) \, dx \r
\end{split}$$