---
tags:
  - Maths/Logic/Probability_theory
---
A *probability space*, or *probability triple*, $(Ω, \mathcal F, P)$ is a [measure space](Measure.md#^MeasureSpace) such that $P:\mathcal F\to[0,1]$ is a [probability measure](Measure.md#^ProbabilityMeasure). ^ProbabilitySpace

The set $Ω$ of possible outcomes in a [probability space](#^ProbabilitySpace) $(Ω, \mathcal F, P)$ is called the *sample space*. ^SampleSpace

The elements of the [$σ$-algebra](σ-algebra.md#$σ$-algebra) $\mathcal F$ of the [sample space](#^SampleSpace) $Ω$ in a [probability space](#^ProbabilitySpace) $(Ω, \mathcal F, P)$ are called *events*. ^EventsProbability

The [probability measure](Measure.md#^ProbabilityMeasure) $P$ of a [probability space](#^ProbabilitySpace) $(Ω, \mathcal F, P)$ is sometimes called a *probability function*. ^ProbabilityFunction

A *random variable* $X$ is a [measurable function](Function.md#^MeasurableFunction) $X:(Ω,\mathcal F,P)\to(E,\mathcal{E},X_*P)$ from a [probability space](#^ProbabilitySpace) to another with [measurable space](Measure.md#^MeasurableSpace) $(E,\mathcal E)$ and probability measure given by the [image measure](Measure.md#^ImageMeasure) of $P.$  
Intuitively, $X$ maps outcomes to measurable quantities with well-defined probabilities. ^RandomVariable

The *probability distribution* $X_*P:E\to[0,1]$ of a [random variable](#^RandomVariable) $X:(Ω,\mathcal F,P)\to(E,\mathcal{E},X_*P)$ is the [probability measure](Measure.md#^ProbabilityMeasure) given by the [image measure](Measure.md#^ImageMeasure) of $P:$ $$X_*P=PX^{-1}$$ ^ProbabilityDistribution

The *probability density function*, or *probability distribution function* (*pdf*) $f$ of a [random variable](#^RandomVariable) $X:(Ω,\mathcal{F},P)\to (E,\mathcal{E},X_*P)$ with respect to a measure $μ$ on $(E,\mathcal{E}),$ is a [nonnegative](Function.md#^PositiveSemidefiniteFunc) [measurable function](Function.md#^MeasurableFunction) given by the [Radon-Nikodym derivative](Measure.md#^RadonNikodymDerivative):$$f\equiv\dv{X_*P}{μ}$$such that for all $A\in\mathcal{E}:$$$X_*P(A)=\int_A f \, dμ=P(X^{-1}(A))=\int_{X^{-1}(A)}  dP$$ ^pdf

The *median* $m$ of a [random variable](#^RandomVariable) $X$ with [pdf](#^pdf) $f$ is defined from$$\int_{-\infty}^m xf(x) \, dx = \int _m^\infty xf(x) \, dx = \frac12  $$ ^Median

The *mean,* or *expectation* $\langle X\rangle$ of a [random variable](#^RandomVariable) $X$ with [pdf](#^pdf) $f,$ is given by$$\langle X\rangle=\int_\rr xf(x)  \, dx $$ ^MeanExpectation

The *covariance* of two [random variables](#^RandomVariable) $X,Y$ is a [function](Function.md#^Function) calculated from the [expectations](#^MeanExpectation):
$$\mathrm{Cov}(X,Y)\equiv\langle XY\rangle-\langle X\rangle\langle Y\rangle$$ ^Covariance

The *variance* $σ^2(X)$ of a [random variable](#^RandomVariable) $X$ is a [function](Function.md#^Function) calculated from the [expectations](#^MeanExpectation):
$$σ^2(X)\equiv\mathrm{Cov}(X,X)=\langle X^2\rangle-\langle X\rangle^2$$ ^Variance

The *standard deviation* $σ(X)$ of a [random variable](#^RandomVariable) $X$ is a [function](Function.md#^Function) given by the square root of the [variance](#^Variance):$$\begin{split}
σ(X)&\equiv\sqrt{σ^2(X)}\\
&=\sqrt{ \mathrm{Cov}(X,X) }\\
&=\sqrt{ \langle X^2\rangle-\langle X\rangle^2 }
\end{split}$$ ^StandardDeviation

The *correlation* of two [random variables](#^RandomVariable) $X,Y$ is a [function](Function.md#^Function) given by
$$\text{Corr}(X,Y) = \frac{\langle XY\rangle-\langle X\rangle\langle Y\rangle}{\sigma(X)\sigma(Y)} = \frac{\text{Cov}(X,Y)}{\sqrt{\text{Cov}(X,X)\text{Cov}(Y,Y)}} $$where $\text{Cov}(X,Y)$ is the [covariance](#^Covariance) of $X$ and $Y,$ and $σ(X)$ is the [standard deviation](#^StandardDeviation) of $X.$ ^Correlation

*Bayes rule* in odds form is given by
$$O(A|B) = O(A)\frac{O(B|A)}{O(B|\lnot A)}$$
$O(A)$ is called the *prior*, and $\frac{O(B|A)}{O(B|\lnot A)}$ is called the *Bayes factor*. ^BayesRuleOdds

An *ensemble* is a [probability distribution](#^ProbabilityDistribution) for the [state](Quantum%20mechanics.md#^State) of the system,
an infinite set of copies of the system whose initial microstates are determined by the [probability density function](#^pdf). ^Ensemble

The *binomial coefficient* ($n$ choose $k$) is given by$$\begin{pmatrix}n\\k\end{pmatrix}= \frac{n!}{k!(n-k)!}$$It gives the number of ways to choose an unordered subset of $k$ elements from a set of $n$  elements.
E.g. there are 6 ways of choosing 2 elements from the set $\{1,2,3,4\}.$
It also counts the number of $(k-1)$-simplices in an $(n-1)$-simplex. ^BinomialCoefficient

The *Boltzmann distribution* is the [probability distribution](#^ProbabilityDistribution) of a system to be in a [state](Quantum%20mechanics.md#^State) as a function of energy. Maximizes entropy. Describes the canonical  ($NVT$)  [ensemble](#^Ensemble).$$p_i=\frac{e^{-βE}}{Z(β)}$$where  $p_i$  is the probability of state  $i$  with energy  $E_i$ , and  $Z(β)$  is the [canonical partition function](#^CanonicalPartitionFunction). ^BoltzmannDistribution

The *canonical partition function* $Z(β)$ is the normalizing constant of the [Boltzmann distribution](#^BoltzmannDistribution):$$\begin{split}
\text{Discrete classical: }Z(β) &= \sum_i e^{-βE_i}\\
\text{Continuous classical: }Z(β) &= \int e^{-βE}dE\\
\text{Discrete quantum: }Z(β) &= \text{Tr}(e^{-β\hat H})\\
\text{Continuous quantum: }Z(β) &= \int\bra{p,q}e^{-β\hat H(p,q)}\ket{p,q}\ dp\ dq
\end{split}$$ ^CanonicalPartitionFunction

A *Markov kernel* between [measurable spaces](Measure.md#^MeasurableSpace) $(X,Σ)$ and $(Y,Θ),$ is a [function](Function.md#^Function) $k:X\times Θ\to[0,1]$ such that:
$k(x,·)$ is a [probability measure](Measure.md#^ProbabilityMeasure) in $(Y,Θ)$
$k(·,θ)$ is a [measurable function](Function.md#^MeasurableFunction) in $(X,Σ)$
for all $x\in X,$ and $θ\in Θ.$ ^MarkovKernel

A *confidence function* is a [Markov kernel](#^MarkovKernel) of the form $k(x,y)=e(x-y).$ It is a [measurable function](Function.md#^MeasurableFunction). ^ConfidenceFunction


## Multivariate probability theory

A *multivariate random variable,* or *random vector,* is a [vector](Vector%20space.md#^Vector) $(X_1,X_2,\dots,X_n)$ of [scalar](Vector%20space.md#^Scalar)-valued [random variables](#^RandomVariable) $X_i,$ all on the same [probability space](#^ProbabilitySpace). ^RandomVector

The *joint probability density function* $f_{X_1,X_2,\dots,X_n}$ of $n$ [random variables](#^RandomVariable) $X_1,X_2,\dots,X_n,$ all on the same [probability space](#^ProbabilitySpace) $(Ω,\mathcal{F},P),$ is a [nonnegative](Function.md#^PositiveSemidefiniteFunc) [measurable function](Function.md#^MeasurableFunction) such that they induce$$\int_{D}  f_{(X_1,X_2,\dots,X_n)}(x_1,x_2,\dots,x_n) \, dx_1\,dx_2\dots dx_n=\text{Prob}((X_1,X_2,\dots,X_n)\in D)$$where $D=(D_1,D_2,\dots,D_n)$ and $D_i\in\mathcal{F}.$ ^JointPDF

The *marginal* [probability density functions](#^pdf) $f_X,f_Y$ of a [joint pdf](#^JointPDF) $f_{XY}$ are given by$$\begin{split}
f_X(x)&=\int_\rr f_{X,Y}(x,y) \, dy\\
f_Y(y)&=\int_\rr f_{X,Y}(x,y) \, dx\\
\end{split}$$ ^Marginal

# Algebra of random variables
<iframe width="100%" height="320" src="https://en.wikipedia.org/wiki/Algebra_of_random_variables#Expectation_algebra_for_random_variables"></iframe>

^RandomAlgebraWiki

For two random variables $X$ and $Y:$$$\begin{split}
\langle X+Y\rangle &= \langle X\rangle  +\langle Y\rangle\\
\langle XY\rangle &= \langle X \rangle  \langle Y \rangle \text{ (if independent)}\\
\langle kX\rangle &= k\langle X \rangle\\
σ^2(X+Y) &= σ^2(X) + 2\mathrm{Cov}(X,Y) + σ^2(Y)\\
σ^2(XY) &= σ^2(X)\langle Y\rangle^2 + σ^2(X)σ^2(Y) + \langle X\rangle^2 σ^2(Y) \text{ (if independent)}\\
σ^2(kX) &= k^2σ^2(X)\\
\end{split}$$ ^RandomAlgebra

The [probability density function](#^pdf) $f_{X+Y}$ of the sum of two [random variables](#^RandomVariable) $X$ and $Y$ is given by the [convolution](Function.md#^Convolution)$$f_{X+Y}(x)=(f_X*f_Y)(x)=\int_\rr f_X(y)f_Y(x-y)\, dy$$ ^PDFconvolution