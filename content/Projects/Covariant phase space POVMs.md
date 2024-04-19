# Definitions

An *approximate joint position/momentum [observable](Quantum%20mechanics.md#^Observable)* is defined as:
$$\begin{split}
\P^{Q_{μ}}(X)&\equiv (μ*\P^Q)(X)=\int _\rr μ(X-q) \, d\P^Q(q)\\
\P^{P_ν}(Y)&\equiv (ν*\P^P)(Y)=\int _\rr ν(Y-p) \, d\P^P(p) \\
\end{split}$$
$$φ_μ(\P^Q(X))=(μ*\P^Q)(X)$$
$$φ_μ(a\P^Q(X)+b\P^Q(Y))=aφ_μ(\P^Q(X))+bφ_μ(\P^Q(Y))=a(μ*\P^Q)(X)+b(μ*\P^Q)(Y)$$

For $X\in\B(\rr),$ where $μ,ν$ are [probability measures](Measure.md#^ProbabilityMeasure) on $\rr.$ Sometimes we assume that its [Radon-Nikodym derivative](Measure.md#^RadonNikodymDerivative) are the [confidence functions](Probability%20theory.md#^ConfidenceFunction) $e\equiv\dv{μ}{x}$ exists so that $μ(X)=\int_{X}  e(x)\, dx=\int_\rr χ_X(x)  e(x)\, dx.$ The approximation becomes exact when $\mu$ or $\nu$ are [Dirac](Measure.md#^DiracMeasure). Note that some authors write $Q(dq)\equiv d\P^Q(q)$ and $Q\equiv\P^Q\equiv\mathsf Q.$

A *covariant phase space observable* is an [observable](Quantum%20mechanics.md#^Observable) $\G:\B(\rr^2)\to B(\H)$ which obeys the covariance condition $W(q,p)\G(Z)W(q,p)^{\dagger} = \G(Z - (q,p))$ for all [Borel sets](σ-algebra.md#^BorelSet) $Z \in \B(\rr^2),$ and $(q,p)\in\rr^2,$ where $W$ is the [Weyl operator](Quantum%20mechanics.md#^WeylOperator). This implies that its [marginals](Quantum%20mechanics.md#^MarginalObservable) are $\P^{Q_μ}(X), \P^{P_ν}(Y).$ ^CovarPhaseSpaceObs

Technically I should be writing $(q\times p),$ but that gets cumbersome on long expressions, so I will mostly stick with $(q,p)$ and sometimes $(X,Y)\equiv(X\times Y)$ (the choice based purely on what I think works better at the time).

It is necessarily of the form
$$
\G^T(Z)=\int _Z \, d\G^T(q,p) =\frac1τ\int _Z W(q,p)T\, W^{\dagger}(q,p) \, dq\ dp 
$$
for $Z\in\B(\rr^2),$ for some [state](Quantum%20mechanics.md#^State) $T$ such that $μ=μ_T\equiv p^{\P^Q}_{ΠTΠ^\dagger}$ and $ν=ν_T= p^{\P^P}_{ΠTΠ^\dagger}$, where $Πψ(q)=ψ(-q)$ is the [parity operator](Linear%20map.md#^ParityOperator), and the probability measure
$$\begin{split}
p^{\P^Q}_ρ(X)&=\int_X dp^{\P^Q}_ρ(q)=\text{Tr}(ρ\P^Q(X))=\int_X |ψ(q)|^2 \, dq=\bra ψ \P^Q(X)\ket ψ\\
p^{\P^P}_ρ(Y)&=\int_Y dp^{\P^P}_ρ(p)=\text{Tr}(ρ\P^P(Y))=\int_Y |\tilde ψ(p)|^2 \, dp=\bra ψ \P^P(Y)\ket ψ\\
\end{split}$$
for $X\in\B(\rr)$ and assuming $ρ=\ket ψ\bra ψ.$ It can be shown that $(T_1\neq T_2)\implies(\G^{T_1}\neq\G^{T_2}).$

Busch sometimes uses the notation $\P^Q_ρ\equiv p^{\P^Q}_ρ,$ which is shorter, but also more subtle. I'll use that one instead. So:$$\begin{split}
\G^T(X\times\rr)&=\P^{Q_{μ_T}}(X)\\
\int_X\int_\rr \, d\G^T(q,p)
&=\int _\rr μ_T(X-q) \, d\P^Q(q)\\
&=\int _\rr \P^Q_{ΠTΠ^\dagger}(X-q) \, d\P^Q(q)\\
&=\int _\rr \tr(ΠTΠ^\dagger\P^Q(X-q)) \, d\P^Q(q)\\
&=\int _\rr \tr(T\P^Q(q-X)) \, d\P^Q(q)\\
&=\int _\rr \P^Q_{T}(q-X) \, d\P^Q(q)\\
\end{split}$$and$$\begin{split}
\G^T_ρ(X\times\rr)
&=\P^{Q_{μ_T}}_ρ(X)
\end{split}$$Seemingly useful property:$$\begin{split}
\G^T_ρ(Z)
&=\G^ρ_T(-Z)\\
\P^{Q_{μ_T}}_ρ(X)
&=\P^{Q_{μ_ρ}}_T(-X)
\end{split}$$The measurement outcome ([joint](Probability%20theory.md#^JointPDF)) [probability density function](Probability%20theory.md#^pdf) (up to a factor of $\frac{1}{τ}$) is given by$$f_ρ(q,p)\equiv \mathrm{Tr}(ρ\, W(q,p)\, T\, W^{\dagger}(q,p))$$So if we push the integration inside the trace:$$\G^T_ρ(Z)=\mathrm{Tr}(ρ\, \G^T(Z))=\int_Z d\G^T_ρ(q,p)=\frac1τ\int_Z  f_ρ(q,p)\, dq\, dp $$These two quantities are related by marginalization, and the [Radon-Nikodym derivative](Measure.md#^RadonNikodymDerivative) (assuming $\P^Q_ρ\ll q,$ which I think is true):$$\begin{split}
\G^T_ρ(X\times\rr)=\P^{Q_μ}_ρ(X)&=\frac1τ\int_{(X,\rr)}  f_ρ(q,p)\, dq\, dp \\
 \dv{\P^{Q_μ}_ρ}{q}&= \frac1τ\int_\rr  f_ρ(q,p)\, dp
\end{split}$$
We want to use $\G^T$ as the [POVM](Measure.md#^POVM) of a [QRF](Quantum%20reference%20frames.md#^QRF), with $W$ being the [unitary operators](Linear%20map.md#^UnitaryOperator). The [group](Algebraic%20structure.md#^Group) is $(\rr^2,+)$ and the [action](Action.md#^GroupAction) is addition/subtraction (we can choose for convenience):
$$\begin{split}
\H&=\H_\R\otimes \H_\S\\
(Σ,·)_G &=(\rr^2,+)_{(\rr^2,+)}\\
g&=(q,p)\\
α(g,Z)&=Z-(q,p)\\
\end{split}$$

such that $W(q,p)\G^T(Z)W(q,p)^{\dagger}=\G^T(Z-(q,p))$ for all $Z\in\B(\rr^2).$ Smeared position/momentum are also covariant.
So we want to use $\G^T$ as the POVM in the [relativization map](Relativization%20map.md#^RelMap).
$$\begin{split}
\yen^T(A)&\equiv\int_{\rr^2} d\G^T(q,p)\otimes W_\S(q,p)\, A\, W_\S^{\dagger}(q,p)\\
&=\frac1τ\iint_{\rr^2} W(q,p)(T\otimes A)W^{\dagger}(q,p) \, dq\ dp\\
\end{split}$$
---
# Tasks

- [x] Check the $\frac1\tau$ factor
	Kiukas et al define $x=(q,p)$ and $dx=\frac{dq\, dp}{τ}.$ 
- [x] Show that the product of two [positive](Linear%20map.md#^PositiveOperator) operators is not necessarily positive (2x2 matrices work fine)
	I've found that for a $2\times 2$ matrix (that can be written as $vw^T)$ to be positive, i.e.:
	
	$\begin{split}\ml x^* & y^*\mr\ml a & b \\ c & d\mr\ml x \\ y\mr&= \ml x^*&y^*\mr\ml ax+by\\cx+dy \mr\\&= ax^*x+by^*x + cx^*y+dy^*y>0\end{split}$
	for all $x,y\in\C,$ the condition is $w=v^*,$ so:$$\begin{split}a&\ge 0\\d&\ge 0\\c&=b^*\\ ad&=|b|^2\end{split}$$so if we take a product
	$\ml a'a+b'b^*&a'b+b'd\\ b'^*a+d'b^*&b'^*b+d'd\mr$
	we see that there's no reason why $b'b^*\ge 0$ or $(a'b+b'd)=(b'^*a+d'b^*)^*.$ Or in vector form, $vv^{\dagger}ww^{\dagger},$ there is no reason why $w=\frac{v}{v^{\dagger} w},$ and I'd think that it is positive only in that case, up to scaling.
- [x] Look at the [variance](Probability%20theory.md#^Variance) of $\yen(\hat{Q}_\S)$ and see how that depends on $η.$ PVM ideally, but operator also nice.
- [x] Check that you didn't mix up system and frame $μ$'s. 
- [x] Check whether $Γ_ω\circ\yen$ is an [incompatibility-breaking](Quantum%20mechanics.md#^IncompatibilityBreakingChannel) channel for $\P^Q$ and $\P^P.$ [link](https://arxiv.org/pdf/1504.05768.pdf)
	It doesn't seem like there's any new information there. $Γ_ω\circ\yen$ being incompatibility-breaking for $\P^Q$ and $\P^P$ is almost the same question as the one about $\yen(\P^{Q_\S}(X))$ and $\yen(\P^{P_\S}(Y))$ being [jointly measurable](Quantum%20mechanics.md#^JointObservables).
- [x] Maybe check other measures of uncertainty, ([error bar widths](Quantum%20mechanics.md#^ErrorBarWidth), **[overall widths](Measure.md#^OverallWidth)**)
	Overall width uncertainty relation: $W_{ε_1}(\P^Q_ρ)·W_{ε_2}(\P^P_ρ)\geτ\hbar(1-ε_1-ε_2)^2$
	Error bar width uncertainty relation: $W_{ε_1}(\P^{Q_μ},\P^Q)·W_{ε_2}(\P^{P_ν},\P^P)\geτ\hbar(1-ε_1-ε_2)^2$
	**Calibration error, resolution**

---
# Relativization, marginalization, and restriction of $\G^T_\S(Z)$
## [Relativize](Relativization%20map.md#^RelMap)
$$\begin{split}
(\yen^T\circ\G^T_\S)(Z)&\equiv\iint_{\rr^2} d\G^T(q,p)\otimes W_\S(q,p) \G^T_\S(Z) W_\S^{\dagger}(q,p)\\
&=\iint_{\rr^2} d\G^T(q,p)\otimes \G^T_\S(Z-(q,p))\\
&=(\G^T*\G^T_\S)(Z)\\
&=(\G^T_\S*\G^T)(Z)\\
\end{split}$$
Where the last line refers to the [POVM convolution](#POVM%20[convolution](Measure.md%20MeasureConvolution)) defined below. In this case, $\G^T(Z)$ and $\G^T_\S(Z)$ commute because they are a shorthand for $\G^T(Z)\otimes\hat{I}_\S$ and $\hat{I}_\R\otimes\G^T_\S(Z)$ respectively. This would still apply if the $T$'s were not the same.

Next, we would like to [marginalize](Quantum%20mechanics.md#^MarginalObservable). But first, let us check whether the order of relativize-marginalize vs. marginalize-relativize affects the results.
### Check differences in order of operations
Be mindful of integration ranges: $\rr$ may not be the same as $\rr.$

Marginalize-then-relativize (remember that $\P^{Q_\R}_μ(X)$ is also covariant):$$\begin{split}
\yen^T(\G^T(X,\rr))&=\iint_{\rr^2} d\G^T(q,p)\otimes W_\S(q,p) \P^{Q_\S}_μ(X) W_\S^{\dagger}(q,p)\\
&=\iint_{\rr^2} d\G^T(q,p)\otimes \P^{Q_\S}_μ(X-q)\\
\end{split}$$Relativize-then-marginalize (be careful with that $\rr-p$):$$\begin{split}
(\yen^T\circ\G^T)(X,\rr)
&=\iint_{\rr^2} d\G^T(q,p)\otimes W(q,p) \G^T(X,\rr)W^{\dagger}(q,p)\\
&=\iint_{\rr^2} d\G^T(q,p)\otimes \G^T(X-q,\rr-p)\\
&=\iint_{\rr^2} d\G^T(q,p)\otimes \iint_{(X-q,\rr-p)} d\G^T(q',p')\\
&=\iint_{\rr^2} d\G^T(q,p)\otimes \iint_{(X,\rr)} d\G^T(q''-q,p''-q)\\
&=\iint_{\rr^2} d\G^T(q,p)\otimes \P^{Q_\S}_μ(X-q)\\
\end{split}$$
where $q''\equiv q'-q$, and $p''\equiv p'-p.$ I tried many (not shown) ways to trick the objects into showing any subtle differences between the approaches, but unless there is a fundamental mistake in some of my definitions, I'm very confident that the order of marginalization vs. relativization doesn't matter for $\G^T(Z).$

### An extra-detailed calculation of the $\rr-p$ thing

The trick is to pass the $\rr-p$ from the integration limits (which are mysterious and may raise concerns about how the limiting process is carried out) into the [indicator function](Function.md#^IndicatorFunction) $χ_X(x)$ (which has very clear properties and you can't really argue that $χ_{\rr-p}(p'')=χ_\rr(p''+p)=1$ is false):$$\begin{split}
(\yen^T\circ\G^T)(X\times\rr)&=\iint_{\rr^2} d\G^T(q,p)\otimes \G^T\big((X\times\rr)-(q\times p)\big)\\
&=\iint_{\rr^2} d\G^T(q,p)\otimes \G^T\big((X-q)\times(\rr-p)\big)\\
&=\iint_{\rr^2} d\G^T(q,p)\otimes \iint_{(X\times\rr)}d\G^T\big((q'-q)\times(p'-p)\big)\\
&=\iint_{\rr^2}d\G^T(q,p)\otimes\iint_{(X\times\rr-p)}  d\G^T\big((q'-q)\times p''\big)\\
&=\iint_{\rr^2}\iint_{\rr^2} χ_X(q')χ_{\rr-p}(p'') d\G^T(q,p)\otimes d\G^T\big((q'-q)\times p''\big)\\
&=\iint_{\rr^2}\iint_{\rr^2} χ_X(q')χ_{\rr}(p''+p) d\G^T(q,p)\otimes d\G^T\big((q'-q)\times p''\big)\\
&=\iint_{\rr^2}\iint_{\rr^2} χ_X(q') d\G^T(q,p)\otimes d\G^T\big((q'-q)\times p''\big)\\
&=\iint_{\rr^2}\iint_{(X\times\rr)} d\G^T(q,p)\otimes d\G^T\big((q'-q)\times p''\big)\\
\yen^T(\G^T(X\times\rr))
&=\iint_{\rr^2} d\G^T(q,p)\otimes \P^{Q_{\S,μ}}(X-q)\\
\end{split}$$

## [Marginalize](Quantum%20mechanics.md#^MarginalObservable)

Now we make sure to distinguish that the system $\S$ marginalizes into $\P^{Q_{\S,μ}}$ and $\P^{P_{\S,ν}},$ and the frame $\R$ marginalizes into $\P^{Q_{\R,η}}$ and $\P^{P_{\R,ι}}.$

Anyway, here's the marginalization into unsharp position:$$\begin{split}
(\yen^T\circ\G^T_\S)(X\times\rr)
&=\iint_{\rr^2} d\G^T(q,p)\otimes \P^{Q_{\S,μ_T}}(X-q)\\
\yen^T(\P^{Q_{\S,μ_T}}(X)) 
&=\iint_{\rr^2} d\G^T(q,p)\otimes (μ_T*\P^{Q_\S})(X-q)\\
&=\iiint_{\rr^3} μ_T(X-q-q')\,  d\G^T(q,p)\otimes  d\P^{Q_\S}(q')\\
&=\iiiint_{\rr^4} χ_X(x) e(x-q-q')\,  d\G^T(q,p)\otimes  d\P^{Q_\S}(q')\, dx\\
&=(\G^T*\G^T_\S)(X\times\rr)\\
&=(\G^T*\P^{Q_{\S,μ_T}})(X)\\
&=(\G^T*(μ_T*\P^{Q_\S}))(X)\\
\end{split}$$
Analogously for momentum:$$\yen^T(\P^{P_{\S,ν_T}}(Y)) =(\G^T*(ν_T*\P^{P_\S}))(Y)$$BUT! Remember that this [convolution](#POVM%20[convolution](Measure.md%20MeasureConvolution)) commutes, so the marginalization can be applied to the frame:$$\begin{split}
\yen^T(\P^{Q_{\S,μ_T}}(X)) 
&=(\G^T_\S*\G^T)(X\times\rr)\\
&=(\G^T_\S*\P^{Q_{\R,μ_T}})(X)\\
&=(\G^T_\S*(μ_T*\P^{Q_\R}))(X)\\
\end{split}$$which is weird and surprising, but seems useful if true.
## [Restrict](Quantum%20mechanics.md#^RestrictionMap)
Sections 5 and 6 of Leon's long paper. Definition of the restriction $Γ_ω$ of a relativized quantity $\yen(A):$
$$
(Γ_ω\circ\yen)(A)=\int_G U_\S(g)\, A\, U_\S^{\dagger}(g) \, d\mathsf F_ω(g)
$$
where $\mathsf F_ω\equiv ω\circ\mathsf F$ (or $\mathsf F_ρ(X)=\mathrm{Tr}(ρ\mathsf F(X))=\sum_n\bra{ψ_n}ρ\mathsf F(X)\ket{ψ_n}$ if $ρ$ is a density operator corresponding to $ω$) is a regular (probability?) [measure](Measure.md#^Measure) (we also have the notation $\mathsf p^{\mathsf F}_ω,$ and Leon calls it $μ^{\mathsf F}_ω$ elsewhere, but that's entirely too many notations for one thing, so I'll just pick the shortest one). So applying this definition:
$$\begin{split}
(Γ_ρ\circ\yen^T)(\P^{Q_{\S,μ}}(X))&=\iint_{\rr^2} \P^{Q_{\S,μ}}(X-q)\, d\G^T_ρ(q,p)\\
Γ_ρ(\yen^T(\P^{Q_{\S,μ}}(X)))&=(\G^T_ρ* \P^{Q_{\S,μ}})(X)\\
&=(\G^T_ρ* (μ*\P^{Q_\S}))(X)\\
\end{split}$$


**Theorem:** Let $\E$ be a [localizable POVM](Measure.md#^LocalizablePOVM), and let $(\f_n)\subset\H_\R$ be a [localizing sequence](Measure.md#^LocalizingSequence) of unit vectors such that $\lim_{ n \to \infty }\bra{\f_n}\E(X)\ket{\f_n}=1$ if $\E(X)\neq 0.$ Then, for all $A\in\L(\H_\S)$ and $φ\in\H_\S:$
$$\begin{split}
\lim_{ n \to \infty } \bra{φ\otimes \f_n}\yen(A)\ket{φ\otimes \f_n} &= \bra{φ}A\ket{φ}
\\\lim_{ n \to \infty } (Γ_{\f_n}\circ\yen)(A) &= A 
\end{split}$$


## Expectation values

We start with the expectation value of $\yen^T(\P^{Q_{\S,μ}}(X))$ (without restriction), and write $\ket{φ\f}\equiv \ket{φ}\otimes\ket{\f}$ to save some space:
$$\begin{split}
\bra{φ\f}\yen^T(\P^{Q_{\S,μ}}(X))\ket{φ\f}
&=\iiint_{\rr^3} \bra φ d\G^T(q,p)\ket{φ}\,   μ(X-q-q')  \bra\f d\P^{Q_\S}(q')\ket\f\\
\tr(\ket{φ\f}\bra{φ\f}\yen^T(\P^{Q_{\S,μ}}(X)))
&=\iiint_{\rr^3} d\G^T_φ(q,p)\,   μ(X-q-q') d\P^{Q_\S}_\f(q')
\\&=\iint_{\rr^2} d\G^T_φ(q,p)   (μ * \P^{Q_\S}_\f)(X-q)
\\&=\bra\f\l\G^T_φ*\P^{Q_{\S,μ}}\r(X)\ket\f
\\&=\l\G^T_φ* (μ * \P^{Q_\S}_\f)\r(X)
\end{split}$$
The last 3 lines could be both considered final results, this calculation has some branches, but I think it's all true. If we use the frame marginalization:$$\begin{split}
\bra{φ\f}\yen^T(\P^{Q_{\S,μ}}(X))\ket{φ\f}
&=(\G^T_{\S,\f}*(η*\P^{Q_\R}_φ))(X)\\
\end{split}$$

Now let's calculate the expectation value of its restriction $Γ_ρ(\yen^T(\P^{Q_{\S,μ}}(X)),$ which we calculated in the previous section:
$$\begin{split}
\bra\f Γ_ρ(\yen^T(\P^{Q_{\S,μ}}(X))\ket\f &=((μ * \P^{Q_\S}_\f)* \G^T_ρ)(X)\\
\end{split}$$
Both expectation values are the same if $ρ=\ket φ\bra φ,$ as would be expected intuitively.


NOW WAIT A MINUTE! $\tr(ρ\P(X))$ is a weird thing to call "expectation value": It is a probability, not a value. Busch just calls it something like "the statistic". Let's try Busch's approach:$$\begin{split}
\langle \yen^T\circ\P^{Q_{\S,μ}}\rangle_ρ 
&=\langle \G^T_ρ*\P^{Q_{\S,μ}} \rangle_ρ\\
&=\tr(ρ(\G^T*\P^{Q_{\S,μ}})[1])\\
&= \tr \l ρ\int_\rr q\, d(\G^T * \P^{Q_{\S,μ}})(q)\r\\
&=\tr\l ρ\int_\rr q\, \iint_{\rr^2}d\G^T(q',p) d\P^{Q_{\S,μ}}(q-q')\r\\
&=\int_\rr q\, \iint_{\rr^2}d\G^T_ρ(q',p) d(μ*\P^{Q_\S}_ρ)(q-q')\\
&=\int_\rr q\, \iint_{\rr^2}d\G^T_ρ(q',p)\int_\rr \, dμ_T(q''-q+q')d\P^{Q_\S}_ρ(q'')\\
\end{split}$$I'm pretty sure this is true, because $\tr(ρ\,\E(X))=\int_\rr χ_X(x) \, d\E_ρ(x),$ and $\langle \E \rangle_ρ\equiv \tr(ρ\E[1])= \int_\rr x \, d\E_ρ(x),$ which is exactly the comparison between what I had before and what I have now, if we compare the fully expanded parts (just substitute $q\mapsto χ_X(q)$ the first time $q$ appears in the integral). Also, maybe it's useful to note that $μ(X-q)=\int_\rr χ_X(x)  e(x-q)\, dx=\int_\rr χ_X(x)  dμ(x-q),$ so $dμ(x-q)=e(x-q)dx.$

So this is not very illuminating, but at least I found an expression for $d(\P_1*\P_2)(x),$ which is pretty neat.
### Momentum
The calculation for the momentum expectation values is completely analogous:
$$\begin{split}
\bra{φ\f}\yen^T(\P^{P_{\S,ν}}(Y))\ket{φ\f}
&=\iiint_{\rr^3} \bra φ d\G^T(q,p)\ket{φ}\, ν(Y-p-p') \bra\f d\P^{P_\S}(p')\ket\f
\\\tr(\yen^T(\P^{P_{\S,ν}}(Y))\ket{φ\f}\bra{φ\f})&=\iiint_{\rr^3} d\G^T_φ(q,p)\, ν(Y-p-p') d\P^{P_\S}_\f(p')
\\&=\iint_{\rr^2} \,  \G^T_φ(q,p)  (ν * \P^{P_\S}_\f)(Y-p)
\\&=\bra\f\l\P^{P_{\S,μ}}* \G^T_φ\r(Y)\ket\f
\\&=\l(ν * \P^{P_\S}_\f)*  \G^T_φ\r(Y)
\\&=\l(ν * \G^T_φ)* \P^{P_\S}_\f\r(Y)
\end{split}$$
$$\begin{split}
\bra\f Γ_ρ(\yen^T(\P^{P_{\S,ν}}(Y)))\ket\f &=((ν * \P^{P_\S}_\f)* \G^T_ρ)(Y)\\
\end{split}$$

## [Variance](Probability%20theory.md#^Variance)
Busch defines the variance of an [observable](Quantum%20mechanics.md#^Observable) as $σ^2(\P)_ρ\equiv \langle \P[2] \rangle-\langle \P \rangle_ρ^2=\int_\rr (x-\langle \P \rangle_ρ)^2\, d\P_ρ,$ and using $σ^2(\P_1*\P_2)=σ^2(\P_1)+σ^2(\P_2):$
$$\begin{split}
σ^2(\yen^T(\P^{Q_{\S,μ_T}}))_ρ 
&= σ^2(\G^T*((μ_T*\P^{Q_\S})))_ρ \\
σ^2(\langle  \yen^T\circ\P^{Q_{\S,μ_T}}_ρ \rangle) 
&= σ^2(\G^T_ρ)+σ^2(μ_T)+σ^2(\P^{Q_\S}_ρ)
\end{split}$$
And for the other marginalization:$$\begin{split}
σ^2(\yen^T(\P^{Q_{\S,μ_T}}))_ρ 
&= σ^2(\G^T_\S*((μ_T*\P^{Q_\R})))_ρ \\
σ^2(\langle  \yen^T\circ\P^{Q_{\S,μ_T}}_ρ \rangle) 
&= σ^2(\G^T_{\S,ρ})+σ^2(μ_T)+σ^2(\P^{Q_\R}_ρ)
\end{split}$$The fact that these two quantities are equal may be useful, or may be trivial.
$$\begin{split}
σ^2(\P^{Q_\S}_ρ)&=\P^{Q_\S}_ρ[2]-\langle \P^{Q_\S}_ρ \rangle^2
\\&=\int_\rr q^2\, d\P^{Q_\S}_ρ(q) -\l\int_\rr q\, d\P^{Q_\S}_ρ(q) \r^2
\\&=\int_\rr q^2\, d\P^{Q_\S}_ρ(q) -\mathrm{Tr}(ρ\,\hat{Q}_\S)^2
\end{split}$$
I need some way to calculate the variance of $\G^T_ρ,$ but is takes two variables, so I don't 
$$σ^2(\G^T_ρ)=\G^T_ρ[2]-\langle  \G^T_ρ\rangle^2=\iint_{\rr^2} q^2p^2\, d\G^T_ρ(q,p) -\l\iint_{\rr^2} qp\, d\G^T_ρ(q,p) \r^2$$

---

## Is $Γ_ρ\circ\yen^T$ [incompatibility-breaking](Quantum%20mechanics.md#^IncompatibilityBreakingChannel) for $\P^Q, \P^P?$

The convolution from $\yen^T$ should commute, but just in case I'll do it the long way:
$$\begin{split}
(Γ_ρ\circ\yen^T)(\P^{Q_\S}(X))
&= (\G_ρ^T*\P^{Q_\S})(X)\\
&= \iint_{\rr^2}\P^{Q_\S}(X-q)\, d\G^T_ρ(q,p)\\
&= \iiint_{\rr^3}χ_{X-q}(q')d\P^{Q_\S}(q')\, d\G^T_ρ(q,p)\\
&= \iiint_{\rr^3}χ_{X-q'}(q)d\P^{Q_\S}(q')\, d\G^T_ρ(q,p)\\
&= \iint_{\rr^2}d\P^{Q_\S}(q')\, \G^T_ρ(X-q',p)\\
&= (\P^{Q_\S}*\G_ρ^T)(X\times\rr)\\
&= (\P^{Q_\S}*\P^{Q_{\R,μ_T}}_ρ)(X)\\
\end{split}$$
This is a sharp position observable $\P^{Q_\S}$ convolved with the measure $\P^{Q_{\R,μ_T}}_ρ=(μ_T*\P^{Q_\R}_ρ)=(μ_T*μ_{Π^\dagger ρ Π}).$ Iff we could prove that this measure equals $μ_{T'}=\P^{Q_\S}_{ΠT'Π^{\dagger}}$ for some $T',$ we could prove that a joint p&m covariant phase space observable $\G^{T'}$ exists, so $(Γ_ρ\circ\yen^T)$ is incompatibility-breaking. Reasoning: If $(Γ_ρ\circ\yen^T)$ is incompatibility-breaking, then a covariant phase space observable $\G^{T'}$ exists, of which $(Γ_ρ\circ\yen^T)(\P^{Q_\S}(X))=(μ_{T'}*\P^{Q_\S})(X)=\G^{T'}(X\times\rr)$ is a marginal. The smearing measure must then obey $μ_{T'}=\P^{Q_\S}_{ΠT'Π^{\dagger}},$ which leaves us with the equation $\P^{Q_{\R,μ_T}}_ρ=\P^{Q_\S}_{ΠT'Π^{\dagger}}:$$$\begin{split}
\P^{Q_{\R,μ_T}}_ρ(X)
&=
\P^{Q_\S}_{ΠT'Π^{\dagger}}(X)\\
\tr(ρ\P^{Q_{\R,μ_T}}(X))
&=
\tr(T'\P^{Q_\S}(-X))\\
\tr(ρ(μ_T*\P^{Q_\R})(X))
&=
\tr(T'\P^{Q_\S}(-X))\\
(\P^{Q_\R}_{ΠTΠ^{\dagger}}* \P^{Q_\R}_ρ)(X)
&=
\P^{Q_\S}_{T'}(-X)\\
\int_\rr \P^{Q_\R}_{ΠTΠ^{\dagger}}(X-q)\, d\P^{Q_\R}_ρ(q)
&=
\tr\l T'\P^{Q_\S}(-X)\r\\
\int_{\rr}\int_X \tr\l Td\P^{Q_\R}(q-x)\r\, \tr\l ρd\P^{Q_\R}(q)\r\,dx
&=
\int_X \tr\l T' d\P^{Q_\S}(-x)\r\\
\int_{\rr}\tr\l Td\P^{Q_\R}(q-x)\r\, \tr\l ρd\P^{Q_\R}(q)\r
&=
\tr\l T' d\P^{Q_\S}(-x)\r\\
\int_{\rr}\bra{q-x} T\ket{q-x} \, \bra{q}ρ \ket{q}\,dq
&=
\bra{-x} T'\ket{-x}\\
\int_{\rr}t(q+x) \, ψ(q)\,dq
&=
t'(x)\\
\end{split}$$This seems very plausible, but I wonder what conditions must the states obey for this to be true. We know that [the pdf of a sum of random variables is given by the convolution of the single-variable pdfs](Probability%20theory.md#^PDFconvolution). Going back to the interpretation of operators as random variables, $ΠTΠ^{\dagger}(x)$ is the pdf of $\P^{Q_\S}(ω_1),$ the [effect operators](Quantum%20mechanics.md#^Effect) of the effects $\P^{Q_\S}_{ω_1}(ΠTΠ^{\dagger})$ of $\P^{Q_\S}$ in state $ΠTΠ^{\dagger},$ and $ρ(x)$ is the pdf of $\P^{Q_\S}(ω_2),$ the effect operators of the effects $\P^{Q_\S}_{ω_2}(ρ)$ of $\P^{Q_\S}$ in state $ρ.$ 
So $T'(x)$ is the pdf of $\P^{Q_\S}(ω_3),$ the effect operators of the effects $\P^{Q_\S}_{ω_3}(T')$ of $\P^{Q_\S}$ in state $T',$ which is also the pdf of... $\P^{Q_\S}(ω_1)+\P^{Q_\S}(ω_2)?$ which are... the effect operators of the effects $\P^{Q_\S}_{ω_1}(ΠTΠ^{\dagger})+\P^{Q_\S}_{ω_2}(ρ)=\P^{Q_\S}_{ω_3}(T')?$
$$\begin{split}
\tr(T'\P^{Q_\S}(ω_3))&= \tr(ΠTΠ^{\dagger}\P^{Q_\S}(ω_1)+ρ\P^{Q_\S}(ω_2))
\end{split}$$

Wigner function/**Husimi function**

Okay wait, so if we agree that $A = \int_\rr  A(x)\, d\P^Q(x)$ is the spectral decomposition of a state, then given any probability density function $f(x),$ the integral $\int_\rr f(x) \, d\P^Q(x)$ should be a state too. $f(x)$ is nonnegative everywhere, so the integral should be a [positive-semidefinite](Linear%20map.md#^SemiPositiveOperator) operator, and $\tr\left(\int_\rr f(x) \, d\P^Q(x) \right)=\int_\rr f(x) \, \tr\left(d\P^Q(x) \right)\dots$ wait, this is just the convex combination argument again. 

(The spectrum of a state is *always* discrete)

**GLEASON THEOREM**!!: Let $\H$ be a complex separable Hilbert space of $\dim(\H)\ge 3.$ If $f:\mathbf{P}(\H)\to[0,1]$ is a generalised probability measure on projections $P,$ then there is a unique state $ρ\in \S(\H)$ such that $f(P) = \tr(ρ P)$ for all $P.$


What if we have a map $h(f(q),g(p))=4f(q)\,g(p)$ such that $h(t',g)$ turns $t'$ into a phase space function for any pdf $g(p),$ and take the [Weyl transform](Quantum%20mechanics.md#^WeylTransform) $W(h)=4\iint_{\rr^2} t'(q)g(p)W(q,p)ΠW^{\dagger}(q,p)\,dq\,dp?$ In that case,$$\begin{split}
\tr(W(h))
&=4\iint_{\rr^2} t'(q)g(p)\tr(W(q,p)ΠW^{\dagger}(q,p))\,dq\,dp\\
&=4\iint_{\rr^2} t'(q)g(p)\iint_{\rr^2}\bra{q',p'} W(q,p)ΠW^{\dagger}(q,p))\ket{q',p'} \,dq'\,dp'\,dq\,dp\\
&=4\iint_{\rr^2} t'(q)g(p)\iint_{\rr^2}\braket{q',p'}{2q-q',2p-p'} \,dq'\,dp'\,dq\,dp\\
&=4\iint_{\rr^2} t'(q)g(p)δ(2q-2q')δ(2p-2p')\,dq\,dp \\
&= 1
\end{split}$$where we have used the property $δ(ax)=\frac{1}{|a|}δ(x)$ (this is the reason for the factor of 4), and if I can prove $W(h)$ is [positive-semidefinite](Linear%20map.md#^SemiPositiveOperator), I'll have proved my claim:
$$\begin{split}
\bra{x,k} W(q,p)ΠW^{\dagger}(q,p)\ket{x,k} &=\bra{x-q,k-p}Π\ket{x-q,k-p}\\
&=\braket{x-q,k-p}{q-x,p-k}\in\{ 0,1 \}\\
\end{split}$$
This seems easy enough. One last condition is that $h$ needs to be an element of Schwartz space (it should be, if both $t'$ and $g$ are, as they differentiate independently even inside $h$), and then we can conclude that $W(h)$ is indeed a state.

Check that we still obey our original requirement that $\tr(W(h)\, d\P^Q(x))=t'(x):$
$$\begin{split}
\tr(W(h)\, d\P^Q(x))
&=4\iint_{\rr^2}t'(q)g(p)\tr(W(q,p)ΠW^{\dagger}(q,p)\, d\P^Q(x))\,dq\,dp\\
&=4\iint_{\rr^2} t'(q)g(p)\iint_{\rr^2}\bra{q',p'} W(q,p)ΠW^{\dagger}(q,p)\, (d\P^Q(x)\otimes I_p) \ket{q',p'}\,dq'\,dp'\,dq\,dp\\
&=4\iint_{\rr^2} t'(q)g(p)\iint_{\rr^2}\bra{2q-q',2p-p'} (d\P^Q(x)\otimes I_p)) \ket{q',p'}\,dq'\,dp'\,dq\,dp\\
&=4\iint_{\rr^2} t'(q)g(p)\iint_{\rr^2}\braket{2q-q'}{x} \braket{x}{q'} \braket{2p-p'}{p'} \,dq'\,dp'\,dq\,dp\\
&=4\iint_{\rr^2}t'(q)δ(2q-2x)\int_\rr g(p)δ(2p-2p') \, dp'\,dq\,dp\\
&=4\frac{t'(x)}2\int_\rr \frac{g(p)}2 \,dp\\
&=t'(x)\\
\end{split}$$
The elegant thing about this is, we can use the same thing for the momentum pdf of the same state: $t'(k)=\int_{\rr}\bra{p-k} T\ket{p-k} \, \bra{p}ρ \ket{p}\,dp$ and both position and momentum bases should fit together nicely.


Bochner’s theorem for the Weyl transform: A function $g :\rr^2→\C$ is of the form $g(q, p) =\tr(K W(q, p))$ for some positive trace class operator $K$ iff $g$ is continuous, and has the property (18.5).

What if we write $d\P^Q(x)=\ket{x}\bra{x}\ dx$ In that case:
$$\begin{split}
\tr\l T' \P^{Q_\S}(-X)\r
&=
\int_{\rr}\tr\l T\P^{Q_\R}(q-X)\r\, \tr\l ρd\P^{Q_\R}(q)\r\\
\int_X \bra{-x} T'\ket{-x}\, dx
&=
\int_{\rr}\int_X\bra{q-x} T\ket{q-x} \, \bra{q}ρ \ket{q}\,dq\,dx\\
&=
\int_{\rr}\int_X\bra{-x}U(-q) T U(-x)\ket{q} \, \bra{q}ρ\, U(q+x)\ket{-x}\,dq\,dx\\
T'
&=
\int_{\rr}U(-q) TU(-x) d\P^{Q_\R}(q) ρ\, U(q+x)\\
&=
\int_{\rr}q· \l T d\P^{Q_\R}(q) (x·ρ)\r\\
\end{split}$$

Or use the definition of a [PVM integral](Measure.md#^PVMInt):$$\begin{split}
\tr\l T' \P^{Q_\S}(-X)\r
&=
\int_{\rr}\tr\l T\P^{Q_\R}(q-X)\r\, \tr\l ρ\,d\P^{Q_\R}(q)\r\\
&=
\tr\l ρ\int_{\rr}\tr\l T\,\P^{Q_\R}(q-X)\r\, d\P^{Q_\R}(q)\r\\
\int_X \tr\l T' d\P^{Q_\S}(-x)\r
&=
\tr\l ρ\int_{\rr}\int_X \tr\l T\,d\P^{Q_\R}(q-x)\r\, d\P^{Q_\R}(q)\r\\
\tr\l T' \int_X d\P^{Q_\S}(-x)\r
&=
\tr\l ρ\int_{\rr}d\P^{Q_\R}(q)\tr\l T\int_X \,d\P^{Q_\R}(q-x)\r\, \r\\
\int_X \bra{-x}  T' \ket{-x}dx
&=
\int_X \tr\l ρ\int_{\rr}\bra{q-x}  T\ket{q-x}\, d\P^{Q_\R}(q)\r dx\\
\end{split}$$

Sequential $q,p$ measurements: I don't see how they relate to this problem.

That's unclear. The more general question is: For any [state](Quantum%20mechanics.md#^State) and observable, we can find the corresponding pdf, but given a pdf, can we be sure that a corresponding state exists? Equivalently, are there preparations of a physical system whose probability densities are given by $μ_{T'}?$ This seems to be the assumption behind the [axiom](Quantum%20mechanics.md#^Axiom1) of [convex](Vector%20space.md#^ConvexCombination) structure of the state space $\mathbf{S}$ (See page 501 of Quantum Measurement), basically saying "A convex combination of states is a state". Both $T(x)$ and $ρ(x)$ can function as a "continuous" version of the convex coefficients $k_i,$ since they are nonnegative and their integral is 1. The only requirement seems to be that the integrals converge for all observables and $X.$ Busch writes that "it is a mathematically convenient idealisation to assume that the set of states is closed under $σ$-convex combinations".

More things that are true:
- $σ$-convexity means that if $\{ ρ_j\}$ is a [sequence](Function.md#^Sequence) of states, and $\{ λ_j \}$ is a sequence of positive numbers summing to 1,then $\sum_jλ_jρ_j$ converges in $\T(\H)$ and the limit belongs to $\S(\H).$
- These [convex combinations](Vector%20space.md#^ConvexCombination) are allowed to be infinite, but [countable](Set.md#^CountablyInfiniteSet) ([Cassinelli ,1997](https://pdf.sciencedirectassets.com/272578/1-s2.0-S0022247X00X01023/1-s2.0-S0022247X97954809/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjED0aCXVzLWVhc3QtMSJHMEUCIQC6s7gGvO58zp9IoP7vhxfZBk1IE8nm%2Fs0OtmeHrzLIYgIgeaScyeXwfPGqDno00V6JtEhxsSjS5qFPfDey59G8zvgqswUIRhAFGgwwNTkwMDM1NDY4NjUiDKpoUTJhHMQYn0%2FiwSqQBZ7vfWvaKfQqkvcG%2Buik%2B1uAZvdFtEeTNppTuoFWc58OgqLCHsarknNez7s9tzG3zmsUdvTl%2FS8zjdw9jq5k2tDC2qjBU3iMFX2A4RDM%2B0879lXro0mDnLz1oJW8TDBFwvVwONSIT8oPDZ%2BA%2FHMe9JIEA%2B5XGRxFa1jms4gY3Su9F%2FMqDdae6aStrCv2GPxIvb6%2Fs%2BuGh0l9dwZ%2B%2Fk7tFhOmGrGqQiIbMn87el8VM%2B%2BbuEuHeCvKUj64lRq1Iz4K5YP7roxPgp34GBm5nqSXMvkwD4hvNQPcFYMCOck3TEl%2Fndie2bwHS9xHyqaZrT%2FpaMILgNvquqlLmmfCCZWxxnsLTnaRa9fbQgtE5jOZ4BXpT3vUXfnh3bNkkbquBa1tjvn8aUYNFrPdxT%2BpekSMonxo7D2nKXSyiVFp0dZaZJyU%2BuvZfW4jz7hufPUs6IDOBwcSTL54VQm44qrblUZOka9fJSP6yoye23xZ1oIBmN8aoasvLIrewOVc%2Bnz53ZGVWw5f%2BaAwWX1fckwQNR558n91a44S8c4PYk68ZmxVfjLSYlCOQW58jWJ4qTPqYJIRNxUcuikAp3UNzV1hxTkLZkFBF9pSvvN2kGsY83hxTBBWSdqm%2BFSVp1dqKCjWApeP0cSmBfIm999%2By%2BKp4jP0k%2Bs3cU8KoCsyBex5Vkstju3n74UlQzGuOrUxWAIroNtMuRZHDc1aa6%2BYZj2kVAF2%2F6qc9Uu79bdl2wOaO%2BEVUES8Gh2oGftruugFrLUTzyPncH24nXaJrsR0kEagWqxgej9T80PrrTjkO08jontrU9UvJ8Xzc%2FhuCE0QKBCUrvxy%2BC98eK1eYxy44eF3oSp2gcWH4Sy9qybJPimX1lGGr93dMJmTwa8GOrEB3vI2zb6H8%2F2il%2FyOEQsDn7rczoSTJ1uQElnuLvU%2BBpqU5w9iL3wswGuiFFJsEMMKeBYN%2BwICdjpn%2FjgF5IXsOGUlt0wqVOwKQ7qyHl8OMkziD9Jo0HTa5nKHRoSdXCU9KUrtt3xqjxzcnX3gWpDPZr8B0BE3BdV74teHhya2etns9%2BY1v4I3rHPpFq19pz0Udkx4GaiDIqjlLt6Cc9EauEL2k%2FD9%2BtpWS3LZgggcWsES&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20240312T130941Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTY3SDC4GUU%2F20240312%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=90cd8d3dd35c99bc40be2064455e627cac80d5e9338868fbc5803c2ae9127d17&hash=40153fe76f5495a11045a6c71b4ffde230d9f67fd3f770a25b57e0ef7f083356&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S0022247X97954809&tid=spdf-8dff8ab8-e183-4cc7-957a-3000d38eeaf1&sid=70e03a5a11aff546b609b1752ae80c03ceabgxrqb&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=18015c535053565a5050&rr=86340527bfb72dd2&cc=be)). I can't find anything about uncountable dimensions.

If true, this would be a rigorous way to show that the smearing that comes from the choice of frame is equally good at breaking incompatibility as the smearing that comes from approximating $\P^Q$ and $\P^P.$


$$μ_T(X)=\P^Q_{ΠTΠ^{\dagger}}(X)=\int_X \, d\P^Q_{ΠTΠ^{\dagger}}(q)=\frac1τ\iint_{(X,\rr)}\tr\big(W(-q,-p)TW^{\dagger}(-q,-p)\big)\,dq\,dp=\P^Q_T(-X)$$


$ΠW(q,p)ψ(x,y)=Πψ(x\pm q)=ψ(\mp q-x,\mp p-y),$ so $ΠW(q,p)=W(-q,-p)Π$
[trace](Linear%20map.md#^Trace) [weyl](Quantum%20mechanics.md#^WeylOperator) [chov](Measure.md#^ChangeOfVariables) [ind](Function.md#^IndicatorFunction)
### [Compatibility](Quantum%20mechanics.md#^JointObservables) criteria

 [Sharp](Quantum%20mechanics.md#^SharpObservable) [observables](Quantum%20mechanics.md#^Observable): 
- Are compatible iff they commute.
- Any amount of pairwise-compatible sharp observables are all compatible together.

Observables defined on $\B(\rr)$ are compatible iff they are [functionally coexistent](Quantum%20mechanics.md#^FunctionalCoexistence).

An observable $\G:\B(\rr^2)\to B(\H)$ is a *joint position and momentum observable* iff it obeys the covariance conditions$$\begin{split}
W(q,p)\G(X\times\rr)W^{\dagger}(q,p) &= \G((X\times\rr)\pm(q,p))\\
W(q,p)\G(\rr\times Y)W^{\dagger}(q,p) &= \G((\rr\times Y)\pm(q,p))\\
\end{split}$$Apparently it is an open question whether these conditions imply $W(q,p)\G(X\times Y)W^{\dagger}(q,p) = \G((X\times Y)\pm(q,p))$

If a position observable and a momentum observable are joint, then they have a joint covariant phase space observable $\G^T.$

An uncertainty relation is necessary and sufficient for joint measurability (B+)

A non-trivial joint measurability structure is necessary and sufficient for a Bell violation.

Unitary [channels](Quantum%20mechanics.md#^Channel) $σ_U(T)\equiv UTU^{\dagger}$ are incompatibility-preserving.

### OLD: Are $\yen(\P^{Q_\S}(X))$ and $\yen(\P^{P_\S}(Y))$ [jointly measurable](Quantum%20mechanics.md#^JointObservables)?

We're looking for an [observable](Quantum%20mechanics.md#^Observable) $\E(X\times Y)$ such that $\E(X\times\rr)=\yen(\P^{Q_\S}(X))$ and $\E(\rr\times Y)=\yen(\P^{P_\S}(Y))$
$$\begin{split}
\yen(\P^{Q_\S}(X))&=\frac1τ\iint_{\rr^2} W(q,p)(T\otimes \P^{Q_\S}(X))W^{\dagger}(q,p) \, dq\ dp\\
\yen(\P^{P_\S}(X))&=\frac1τ\iint_{\rr^2} W(q,p)(T\otimes \P^{P_\S}(X))W^{\dagger}(q,p) \, dq\ dp\\
\end{split}$$

We should have $\yen(\P^{Q_\S}(\rr))=\yen(\P^{P_\S}(\rr))=\yen(I_\S)=I_\R\otimes I_\S,$ so naïvely, $\yen(\P^{Q_\S}(X))\ \yen(\P^{P_\S}(Y))$ could do the trick. This is the case when at least one observable is [sharp](Quantum%20mechanics.md#^SharpObservable) (in this case both are, since $\P$ is a [PVM](Measure.md#PVM)) and they commute, which is not the case here. So I don't think it will be that easy. Maybe:
$$\begin{split}
\yen(\P^{Q_\S}(X)\P^{P_\S}(Y))&=
\frac1τ\iint_{\rr^2} W(q,p)(T\otimes \P^{Q_\S}(X) \P^{P_\S}(Y))W^{\dagger}(q,p) \, dq\ dp\\
\end{split}$$
But symmetrized so that it is Hermitian:
$$\P^{\{Q_\S,P_\S\}}(X,Y)\equiv
\frac12\left(\P^{Q_\S}(X)\P^{P_\S}(Y)+\P^{P_\S}(Y)\P^{Q_\S}(X)\right)$$
$$\E(X\times Y)=\yen(\P^{\{Q_\S,P_\S\}}(X,Y))$$
The product of [effects](Measure.md#^Effects) might not be an [effect](Quantum%20mechanics.md#^Effect) if they don't commute.

#### Check that $\yen(\P^{\{Q_\S,P_\S\}}(X,Y))$ is an [effect](Measure.md#^Effects) of $\E$

We have checked that it is [self-adjoint](Linear%20map.md#^SelfAdjoint) and [normalized](Measure.md#^SemispectralMeasure).
It should be [positive](Linear%20map.md#^SemiPositiveOperator) if $\E(X\times Y),\P^{Q_\S}(X),$ and $\P^{P_\S}(Y)$ are positive (semidefinite) for all $X,Y$?
It should also be [bounded](Linear%20map.md#^BoundedOperator) and additive because $\P^{Q_\S}(X),\P^{P_\S}(Y)$ are bounded

So it definitely *could* be in the range of $\E,$ but how to check it actually is?

#### Check additivity of $\P^{\{Q_\S,P_\S\}}$

##### Take two disjoint $X\cap Y=\varnothing,$ put it into $\yen$ and check if that's additive:
 $$\P^A(X\cup Y)=\int_{X\cup Y} d\P^A(x)=\int_X d\P^A(x)+\int_Y d\P^A(x)=\P^A(X)+\P^A(Y)$$
$$\begin{split}
\yen(\P^{Q_\S}(X\cup Y))
&=\frac1τ\iint_{\rr^2} W(q,p)(T\otimes \P^{Q_\S}(X\cup Y))W^{\dagger}(q,p) \, dq\ dp\\
&=\frac1τ\iint_{\rr^2} W(q,p)(T\otimes \P^{Q_\S}(X)+\P^{Q_\S}(Y))W^{\dagger}(q,p) \, dq\ dp\\
&=\frac1τ\iint_{\rr^2} W(q,p)(T\otimes \P^{Q_\S}(X))W^{\dagger}(q,p) \, dq\ dp\\
&+\frac1τ\iint_{\rr^2} W(q,p)(T\otimes \P^{Q_\S}(Y))W^{\dagger}(q,p) \, dq\ dp\\
&=\yen(\P^{Q_\S}(X)) + \yen(\P^{Q_\S}(Y))
\end{split}$$
Yes, it is additive.
##### If yes, check additivity of $\yen(\P^{\{Q_\S,P_\S\}})$

$$\begin{split}
\P^{\{Q_\S,P_\S\}}(X_1\cup X_2, Y_1\cup Y_2)
&=
\frac12\left(\P^{Q_\S}(X_1\cup X_2)\P^{P_\S}(Y_1\cup Y_2)+\P^{P_\S}(Y_1\cup Y_2)\P^{Q_\S}(X_1\cup X_2)\right)
\\&=
\frac12\Big(\big(\P^{Q_\S}(X_1)+\P^{Q_\S}(X_2)\big)\big(\P^{P_\S}(Y_1)+\P^{P_\S}(Y_2)\big)\\
&\phantom{=\frac12}+\big(\P^{P_\S}(Y_1)+\P^{P_\S}(Y_2)\big)\big(\P^{Q_\S}(X_1)+\P^{Q_\S}(X_2)\big)\Big)
\\&=
\frac12\Big(\P^{Q_\S}(X_1)\P^{P_\S}(Y_1)+\P^{Q_\S}(X_2)\P^{P_\S}(Y_1)+\P^{Q_\S}(X_1)\P^{P_\S}(Y_2)+\P^{Q_\S}(X_2)\P^{P_\S}(Y_2)\\
&\phantom{=\frac12}+\P^{P_\S}(Y_1)\P^{Q_\S}(X_1)+\P^{P_\S}(Y_1)\P^{Q_\S}(X_2)+\P^{P_\S}(Y_2)\P^{Q_\S}(X_1)+\P^{P_\S}(Y_2)\P^{Q_\S}(X_2)\Big)
\\&=
\P^{\{Q_\S,P_\S\}}(X_1, Y_1)+\P^{\{Q_\S,P_\S\}}(X_2, Y_1)+
\P^{\{Q_\S,P_\S\}}(X_1, Y_2)+\P^{\{Q_\S,P_\S\}}(X_2, Y_2)
\end{split}$$


Wait, what exactly did I mean by "additivity of $\yen(\P^{\{Q_\S,P_\S\}})$"?

Whether $\yen(\P^{\{Q_\S,P_\S\}})=\frac12\yen(\left(\P^{Q_\S}(X)\P^{P_\S}(Y))+\frac12\yen(\P^{P_\S}(Y)\P^{Q_\S}(X)\right))?$ (This seems trivially true)

Whether $\yen(\P^{\{Q_\S,P_\S\}}+\P^{\{Q'_\S,P'_\S\}})=\yen(\P^{\{Q_\S,P_\S\}})+\yen(\P^{\{Q'_\S,P'_\S\}})?$

---

## POVM [convolution](Measure.md#^MeasureConvolution)

It is convenient to define something analogous to [measure convolution](Measure.md#^MeasureConvolution), and to $(μ*\P^Q)(X)=\int _\rr μ(X-q) \, d\P^Q(q).$ If $A, B:\B(\rr)\to B(\H)$ are commuting [POVMs](Measure.md#^POVM): and $X\in\B(\rr):$$$\begin{split}
(A*B)(X)&\equiv \int_\rr A(X-x)\, dB(x)
\\&=\int_{\rr}\int _X dA(x'-x) dB(x)
\\&=\iint_{\rr^2}χ_X(x')\, dA(x'-x)\, dB(x)
\\&=\iint_{\rr^2}χ_X(x')\, dA(x'')\, dB(x'-x'')
\\&=\int_{\rr}dA(x'')\int _X  dB(x'-x'')
\\&=\int_{\rr}dA(x)  B(X-x)
\\&= (B*A)(X)
\end{split}$$This could probably be defined for a more general [action](Action.md#^GroupAction) other than addition/subtraction, for a more general domain $Σ$ instead of $\B(\rr),$ but I just need this for now.

Sometimes we will also want$$\begin{split}
d(A*B)(x)
&=(dA * dB)(x)\\
&=\int_{\rr} dA(x-x') dB(x')\\
\end{split}$$Reminder: $μ(X-q)=\int_\rr χ_X(x)  e(x-q)\, dx$


## Do the $\yen$ commute?
$$\begin{split}
[\yen(\P^{Q_\S}(X)),\yen(\P^{P_\S}(Y))]=\frac1{τ^2}\bigg(\iiiint_{\rr^4}&W(q,p)(T\otimes \P^{Q_\S}(X))W^{\dagger}(q,p) \, dq\, dp\\
&W(q',p')(T\otimes \P^{P_\S}(Y))W^{\dagger}(q',p') \, dq' dp'\\
-\iiiint_{\rr^4}&W(q,p)(T\otimes \P^{P_\S}(Y))W^{\dagger}(q,p) \, dq\, dp\\
&W(q',p')(T\otimes \P^{Q_\S}(X))W^{\dagger}(q',p') \, dq'\ dp'\bigg)\\
=\frac1{τ^2}\bigg(\iiiint_{\rr^4}&
d\G^T(q,p)\,d\G^T(q',p')\otimes \P^{Q_\S}(X+q)\P^{P_\S}(Y+p') \, dq\, dp\, dq' dp'\\
-\iiiint_{\rr^4}&
d\G^T(q,p)\,d\G^T(q',p')\otimes  \P^{P_\S}(Y+p)\P^{Q_\S}(X+q')\, dq\, dp\, dq' dp'\bigg)\\
=\frac1{τ^2}\bigg(\iiiint_{\rr^4}&
d\G^T(q,p)\,d\G^T(q',p')\otimes\\
&\otimes\iint_{X,Y}\ket{x+q}\braket{x+q}{y+p'}\bra{y+p'}\, dx\, dy\, dq\, dp\, dq' dp'\\
-\iiiint_{\rr^4}&
d\G^T(q,p)\,d\G^T(q',p')\otimes\\
&\otimes\iint_{X,Y}\ket{y+p}\braket{y+p}{x+q'}\bra{x+q'}\, dx\, dy\, dq\, dp\, dq' dp'\bigg)\\
\end{split}$$


**Theorem:** Two self-adjoint operators commute iff their spectral projections commute.
**Proof:** In Chris Isham's QM book

---
# [Radon-Nikodym derivative](Measure.md#^RadonNikodymDerivative)

One of those things that once you know, you start seeing everywhere.
[RN derivative](Measure.md#^RadonNikodymDerivative) [properties](Measure.md#^c652f5)
[Definition of abolutely continuous measure](Measure.md#^AbsolutelyContinuousMeasure)
This was all to reproduce what Leon did in his head that one time (going from $\bra{\f} d\P^{Q_\R}(q)\ket{\f}$ to $|\f(q)|^2$ without doing the $d\P^{Q_{\R}}(q)=\ket{q}\bra{q}$ thing), but I still can't figure it out:$$\bra{\f} \P^{Q_\R}(X)\ket{\f}=\int_X \bra{\f} d\P^{Q_\R}(q')\ket{\f}=\int_X  \dv{\bra{\f} \P^{Q_\R}\ket{\f}}{q}\, dq $$

---

# Calculate $\yen(\hat{Q}_\S)$

$$\begin{split}
\yen(\hat{Q}_\S)&\equiv\iint_{\rr^2} d\G^T_\R(q,p)\otimes W_\S(q,p) \hat{Q}_\S W_\S^{\dagger}(q,p)\\
&=\iint_{\rr^2} d\G^T_\R(q,p)\otimes e^{-iq\hat{P}_\S}e^{ip\hat{Q}_\S} \hat{Q}_\S e^{-ip\hat{Q}_\S}e^{iq\hat{P}_\S} \\
&=\iint_{\rr^2} d\G^T_\R(q,p)\otimes e^{-iq\hat{P}_\S}\hat{Q}_\S e^{iq\hat{P}} \\
&=\iint_{\rr^2} \left(d\G^T_\R(q,p)\otimes e^{-iq\hat{P}_\S}\left(e^{iq\hat{P}}\hat{Q}_\S -[e^{iq\hat{P}_\S}, \hat{Q}_\S]\hat{I}_\S\right)\right) \\
&=\iint_{\rr^2} d\G^T_\R(q,p)\otimes (\hat{Q}_\S-q\hat{I}_\S) \\
&=\left(\iint_{\rr^2} d\G^T_\R(q,p)\right)\otimes \hat{Q}_\S-\iint_{\rr^2}q\, d\G^T_\R(q,p)\otimes\hat{I}_\S\\
&=\hat{I}_\R\otimes \hat{Q}_\S-\iint_{\rr^2}q\, d\G^T_\R(q,p)\otimes\hat{I}_\S\\
&=\hat{I}_\R\otimes \hat{Q}_\S-\int_{\rr}q\, d\P^{Q_{\R,η}}(q)\otimes\hat{I}_\S\\
&=\hat{I}_\R\otimes \hat{Q}_\S-\P^{Q_{\R,η}}[1]\otimes\hat{I}_\S\\
&=\hat{I}_\R\otimes \hat{Q}_\S-\hat{Q}_{\R,η}\otimes\hat{I}_\S\\
\end{split}$$

where we have used Busch's definition of first moment operator $\P[1]\equiv \int_\rr x\, d\P(x)$ and the definition $\hat{A}\equiv \int_\rr x \, d\P^A(x).$
## Expectation value of $\yen(\hat{Q}_\S)$
Now, to take the [expectation](Probability%20theory.md#^MeanExpectation) value $\langle \yen(\hat{Q}_\S) \rangle,$ we need to take the [trace](Linear%20map.md#^Trace) $\tr(ρ\yen(\hat{Q}_\S)),$ where $ρ$ has trace 1. We also know that $T$ has trace 1, the trace is [unitarily invariant](Linear%20map.md#^TraceUnitaryInvariance) and that [it multiplies tensor products](Linear%20map.md#^TraceTensor). Using Busch's definition of the expectation value $\langle \P_ρ \rangle\equiv \mathrm{Tr}(ρ\P[1]),$ where $\P_ρ(X)\equiv \mathrm{Tr}(ρ\P(X)):$$$\begin{split}
\tr(ρ\yen(\hat{Q}_\S))
&=\tr(ρ\hat{Q}_\S)-\tr\l ρ\P^{Q_{\R,η}}[1]\r\\
\langle \yen(\hat{Q}_\S) \rangle
&=\langle \hat{Q}_\S \rangle -\langle\P^{Q_{\R,η}}\rangle_ρ
\end{split}$$
(if $\P$ is a POVM and not a PVM, $\P[1]$ may be symmetric instead of self-adjoint, look a bit further into this)




*The following is now obsolete, but the reasoning was ultimately correct and may be useful in the future:*

To understand $\tr(ρ\yen(\hat{Q}_\S))=\tr(ρ\hat{Q}_\S)-\frac{1}{τ}\iint_{\rr^2}q\, f_ρ(q,p)\, dq\, dp,$ I will try to interpret it in terms of [random variables](Probability%20theory.md#^RandomVariable). If [states](Quantum%20mechanics.md#^State) are probability-measurable by the [effects](Quantum%20mechanics.md#^Effect) of some [observable](Quantum%20mechanics.md#^Observable) (as is assumed by [statistical causality](Quantum%20mechanics.md#^StatisticalCausality)), then operators, which map states to states, can be considered [measurable functions](Function.md#^MeasurableFunction), and so they are random variables.

Now, the expression $\frac{1}{τ}\iint_{\rr^2}q\, f_ρ(q,p)\, dq\, dp$ is the [expectation](Probability%20theory.md#^MeanExpectation) of some random variable with a [pdf](Probability%20theory.md#^pdf) $\frac{1}{τ}f_ρ$ that is [joint](Probability%20theory.md#^JointPDF) with another random variable. In our case, we know that $p_ρ^{\G^T}(X,Y)=\frac{1}{τ}\iint_{(X,Y)} f_ρ(q,p)\,dq\,dp$, so the operator is $\G^T(X,Y).$

This operator is now interpreted as a random variable, and given how it has $\P^{Q_{\R,η}}(X)$ and $\P^{P_{\R,ι}}(Y)$ as [marginals](Quantum%20mechanics.md#^MarginalObservable), we can conclude that these are the jointly distributed random variables corresponding to $f_ρ.$ So our mysterious quantity $\frac{1}{τ}\iint_{\rr^2}q\, f_ρ(q,p)\, dq\, dp$ is the expectation of $\P^{Q_{\R,η}}(X)$ (in state $ρ).$

## Variance of $\yen(\hat{Q}_\S)$
[Variance](Probability%20theory.md#^Variance) is defined as $σ^2(X)=\langle X^2 \rangle-\langle X \rangle^2,$ where $\langle  \rangle$ denotes the [expectation](Probability%20theory.md#^MeanExpectation). Busch defines the variance of an observable as $σ^2(\P_ρ)\equiv \langle \P[2] \rangle-\langle \P_ρ \rangle^2$
$$\begin{split}
σ^2(\yen(\hat{Q}_\S)) 
&= \langle \yen(\hat{Q}_\S)^2 \rangle - \langle \yen(\hat{Q}_\S) \rangle^2
\\&=\langle \hat{Q}_\S^2 \rangle - \langle (\P^{\hat{Q}_{\R,η}}[1])_ρ^2 \rangle
    -(\langle \hat{Q}_\S\rangle  -\langle\P^{Q_{\R,η}}_ρ\rangle)^2
\\&=σ^2(\hat{Q}_\S) - \langle (\P^{\hat{Q}_{\R,η}}[1])_ρ^2 \rangle
     - 2\langle \hat{Q}_\S\rangle\langle\P^{Q_{\R,η}}_ρ\rangle + \langle\P^{Q_{\R,η}}_ρ\rangle^2
\end{split}$$

Now, $\langle (\P^{\hat{Q}_{\R,η}}[1])_ρ^2 \rangle=\left( \int_\rr q\, d\P^{\hat{Q}_{\R,η}}_ρ \right)^2,$ but that's not very illuminating. Perhaps the intrinsic noise operator $N(\P)\equiv \P[2]-\P[1]^2$ has a nice interpretation, in which case we have and from Busch we find $\langle  (\P^{\hat{Q}_{\R,η}}[1])_ρ^2 \rangle =\langle (\P^{\hat{Q}_{\R,η}}[2])_ρ \rangle - \langle N(\P^{\hat{Q}_{\R,η}})  \rangle$
$$\begin{split}
σ^2(\yen(\hat{Q}_\S)) 
&=σ^2(\hat{Q}_\S) - σ^2(\P^{\hat{Q}_{\R,η}}_ρ) + \langle N(\P^{\hat{Q}_{\R,η}})_ρ  \rangle
     - 2\langle \hat{Q}_\S\rangle\langle\P^{Q_{\R,η}}_ρ\rangle
\end{split}$$
I'm not sure how illuminating this is, but it looks like the PVM version of this calculation will be nicer.

---
### Check whether $\yen(\hat{Q}_\S)$ and $\yen(\hat{P}_\S)$ commute

If they do, we can write a joint observable. We need to check whether $\hat{I}_\R\otimes \hat{Q}_\S-\P^{Q_{\R,μ}}[1]\otimes\hat{I}_\S$ commutes with $\hat{I}_\R\otimes \hat{P}_\S-\P^{P_{\R,ν}}[1]\otimes\hat{I}_\S.$ 

---
### Check that covariance holds

It does, just see the rule 

---
## Check that $\yen(\hat{A})$ is invariant under phase space shifts
$$\begin{split}
W(q',p')\yen(A) W^{\dagger}(q',p')&=
\frac1τ\iint_{\rr^2} W(q',p')W(q,p)(T\otimes A)W^{\dagger}(q,p) W^{\dagger}(q',p') \, dq\ dp
\\&=
\frac1τ\iint_{\rr^2} W(q+q',p+p')(T\otimes A)W^{\dagger}(q+q',p+p') \, dq\ dp
\\&=
\frac1τ\iint_{\rr^2}W(q'',p'')(T\otimes A)W^{\dagger}(q'',p'') \, dq''\ dp''
\\&=
\yen(A)\\
\end{split}$$
Where we have performed the change of variable $(q+q',p+p')\mapsto(q'',p'')$ such that $dq''\ dp''=d(q+q')\ d(p+p')=dq\ dp.$ 

[Also](Quantum%20mechanics.md#^WeylProd1), $W(q',p')W(q,p)=e^{\frac i2(qp+2q'p+q'p')}W(q+q',p+p'),$ but the adjoint cancels the exponential part out.

---


# Uncertainty relations
## [Variance](Probability%20theory.md#^Variance)
### Smeared position/momentum

The undergrad preparation uncertainty principle states $σ(A)σ(B)\ge\frac12|\langle[A,B]\rangle|,$ where $σ$ denotes the [standard deviation](Probability%20theory.md#^StandardDeviation). In our case, it is $σ(\hat{q},ρ)σ(\hat{p},ρ)\ge\frac \hbar2$ .
Busch's paper concludes that the equivalent preparation uncertainty relation for smeared position and momentum is given by $σ(\P^{Q_μ},ρ)σ(\P^{P_ν},ρ)\ge\hbar.$ He also notes that$$\begin{split}
σ^2(μ_T*\P^Q,ρ)&=σ^2(μ_T)+σ^2(\P^Q,ρ)\\
σ^2(μ_T)σ^2(ν_T)&\ge\frac{\hbar^2}{4}\\
σ(\P^Q,ρ)σ(\P^P,ρ)&\ge\frac{\hbar}{2}.\\
\end{split}$$
From that:$$\begin{split}
σ(\P^{Q_{\R,μ}},ρ)σ(\P^{P_{\R,ν}},ρ)&=\sqrt{\l σ^2(μ)+σ^2(\P^Q,ρ)\r \l σ^2(ν)+σ^2(\P^P,ρ)\r }\\
&=\sqrt{σ^2(μ) σ^2(ν)+σ^2(μ)σ^2(\P^P,ρ)+σ^2(\P^Q,ρ) σ^2(ν)+σ^2(\P^Q,ρ)σ^2(\P^P,ρ)}\\
&\ge\sqrt{\frac{\hbar^2}{2}+σ^2(μ)σ^2(\P^P,ρ)+σ^2(\P^Q,ρ) σ^2(ν)}\\
\end{split}$$
$σ^2(μ)σ^2(\P^P,ρ)σ^2(\P^Q,ρ) σ^2(ν) \ge (\hbar/2)^4,$ so whatever quantity $x=σ^2(μ)σ^2(\P^P,ρ)/(\hbar/2)^2$ is, the complementary quantity $x'=σ^2(\P^Q,ρ) σ^2(ν)/(\hbar/2)^2\ge\frac1{x},$ so $x+x'\ge x+\frac{1}{x}\ge 2,$ so:$$\begin{split}
σ(\P^{Q_{\R,μ}},ρ)σ(\P^{P_{\R,ν}},ρ)&\ge\sqrt{\frac{\hbar^2}{2}+ (x+x')\frac{\hbar^2}{4}}\\
&\ge\sqrt{\frac{\hbar^2}{2}+ \left( x+\frac{1}{x} \right)\frac{\hbar^2}{4}}\\
&\ge\sqrt{\frac{\hbar^2}{2}+\frac{\hbar^2}{2}}\\
&=\hbar\\
\end{split}$$
This works in general if we have $ab\ge x$ and $cd\ge y$ and we want to know $ac + bd$ or $ad+bc:$ We know that $abcd\ge xy$ (assuming $x,y>0),$ so we define a quantity $k\equiv \frac{ac}{\sqrt{xy}}$ and the complementary $k'\equiv \frac{bd}{\sqrt{xy}}$ so that $kk'\ge 1\implies k'\ge \frac{1}{k}$ and therefore $ac+bd=(k+k')\sqrt{xy}\ge \left( k+\frac{1}{k} \right)\sqrt{xy}\ge 2\sqrt{xy}.$

### Restricted relativized position/momentum

$σ^2(f*g)=σ^2(f)+σ^2(g)$ works for a general convolution, so we have $$\begin{split}
σ^2(Γ_φ(\yen(\P^{Q_{\R,μ}}_\f)))&=\l σ^2(μ)+σ^2(\P^Q_\f)+σ^2(\G^T_φ)\r\\
σ^2(Γ_φ(\yen(\P^{P_{\R,ν}}_\f)))&=\l σ^2(ν)+σ^2(\P^P_\f)+σ^2(\G^T_φ)\r\\
\end{split}$$and then$$\begin{split}
σ(Γ_φ(\yen(\P^{Q_{\R,μ}}_\f)))σ(Γ_φ(\yen(\P^{P_{\R,ν}}_\f)))
&=\sqrt{\l σ^2(\P^{Q_{\R,μ}}_\f)+σ^2(\G^T_φ)\r \l σ^2(\P^{P_{\R,ν}}_\f)+σ^2(\G^T_φ)\r }\\
&=\sqrt{
σ^2(\P^{Q_{\R,μ}}_\f)\l σ^2(\P^{P_{\R,ν}}_\f)+σ^2(\G^T_φ)\r+
σ^2(\G^T_φ)         \l σ^2(\P^{P_{\R,ν}}_\f)+σ^2(\G^T_φ)\r}\\
&\ge\sqrt{
\hbar^2+\lσ^2(\P^{Q_{\R,μ}}_\f)+σ^2(\P^{P_{\R,ν}}_\f)+σ^2(\G^T_φ)\r σ^2(\G^T_φ)
}\\
&\ge\sqrt{
\hbar^2+\l 2\hbar+σ^2(\G^T_φ)\r σ^2(\G^T_φ)
}\\
\end{split}$$
Last step: We have $ab\ge x$ and we want to know $a+b.$ We know that $b\ge \frac{x}{a},$ so $a+b\ge a+\frac{x}{a}=\sqrt{ x }\left( \frac{a}{\sqrt{ x }} +\frac{\sqrt{ x }}{a}\right)\ge 2\sqrt{ x }.$ It's the same inequality technique as before, with $c=d=y=1.$ I don't think the mean/expectation of a joint pdf has any definition other than listing the means of its marginals, so let's use our previous result $(Γ_φ\circ\yen^T)(\P^{Q_{\S,μ_T}}_\f(X))= (\P^{Q_{\S,μ_T}}_\f*\P^{Q_{\R,μ_T}}_φ)(X):$
$$\begin{split}
σ(Γ_φ(\yen^T(\P^{Q_{\S,μ_T}}_\f)))σ(Γ_φ(\yen^T(\P^{P_{\S,ν_T}}_\f)))
&=\sqrt{\l σ^2(\P^{Q_{\R,μ_T}}_\f)+σ^2(\P^{Q_{\S,μ_T}}_φ)\r \l σ^2(\P^{P_{\R,ν_T}}_\f)+σ^2(\P^{P_{\S,ν_T}}_φ)\r }\\
&=\sqrt{
σ^2(\P^{Q_{\R,μ_T}}_\f)\l σ^2(\P^{P_{\R,ν_T}}_\f)+σ^2(\P^{P_{\S,ν_T}}_φ)\r+
σ^2(\P^{Q_{\S,μ_T}}_φ) \l σ^2(\P^{P_{\R,ν_T}}_\f)+σ^2(\P^{P_{\S,ν_T}}_φ)\r}\\
&\ge\sqrt{
2\hbar^2+σ^2(\P^{Q_{\R,μ_T}}_\f)σ^2(\P^{P_{\S,ν_T}}_φ)+σ^2(\P^{Q_{\S,μ_T}}_φ) σ^2(\P^{P_{\R,ν_T}}_\f)}\\
&\ge\sqrt{4\hbar^2}\\
&=2\hbar
\end{split}$$Where for the second-to-last step we have used the same inequality technique as before.
$$σ(Γ_φ(\yen^T(\P^{Q_{\S,μ_T}}_\f)))σ(Γ_φ(\yen^T(\P^{P_{\S,ν_T}}_\f)))\ge2\hbar$$
This uncertainty relation is *not* necessarily saturated for whatever states $φ,\f,T$ saturate the uncertainty relations $σ(\P^{Q_{\R,μ_T}}_\f)σ(\P^{P_{\R,ν_T}}_\f)=\hbar$ and $σ(\P^{Q_{\S,μ_T}}_φ)σ(\P^{P_{\S,ν_T}}_φ)=\hbar.$ 
The 3rd line becomes an equality, but not the 4th: If $ab=x$ and $cd=x,$ then $abcd=x^2$ and so $ac+bd=ac+\frac{x^2}{ac}= x\l \frac{ac}{x}+\frac{x}{ac}\r\ge 2x.$ For this inequality to be saturated, we need the additional condition $ac=bd(=x).$
For our uncertainty relation $σ^2(\P^{Q_{\R,μ_T}}_\f)σ^2(\P^{P_{\S,ν_T}}_φ)+σ^2(\P^{Q_{\S,μ_T}}_φ) σ^2(\P^{P_{\R,ν_T}}_\f)\ge 2\hbar^2,$ this means $σ^2(\P^{Q_{\R,μ_T}}_\f)σ^2(\P^{P_{\S,ν_T}}_φ)=σ^2(\P^{Q_{\S,μ_T}}_φ) σ^2(\P^{P_{\R,ν_T}}_\f)(=\hbar^2).$ 
$$\begin{split}
σ^2(\P^{Q_{\R,μ_T}}_\f)σ^2(\P^{P_{\S,ν_T}}_φ)&=
σ^2(\P^{Q_{\S,μ_T}}_φ) σ^2(\P^{P_{\R,ν_T}}_\f)\\
(σ^2(μ_T)+σ^2(\P^{Q_\R}_\f))(σ^2(ν_T)+σ^2(\P^{P_\S}_φ))&=
(σ^2(μ_T)+σ^2(\P^{Q_\S}_φ))(σ^2(ν_T)+σ^2(\P^{P_\R}_\f))\\
σ^2(μ_T)σ^2(\P^{P_\S}_φ)+σ^2(\P^{Q_\R}_\f)(σ^2(ν_T)+σ^2(\P^{P_\S}_φ))&=
σ^2(μ_T)σ^2(\P^{P_\R}_\f)+σ^2(\P^{Q_\S}_φ)(σ^2(ν_T)+σ^2(\P^{P_\R}_\f))\\
\end{split}$$Simply doing $φ=\f$ is sufficient to accomplish this, but maybe not necessary. (SQUEEZED STATES! Balanced? 2-mode squeezing, gaussian states)

---

## [Overall width](Measure.md#^OverallWidth)
Overall width uncertainty relations: $$\begin{split}
W_{ε_1}(\P^Q_ρ)·W_{ε_2}(\P^P_ρ)&\ge τ\hbar(1-ε_1-ε_2)^2\\
W_{ε_1}(μ_T)·W_{ε_2}(ν_T)&\ge τ\hbar(1-ε_1-ε_2)^2\\
\end{split}$$

But how do overall widths act on convolutions? Well, if 

# Questions

> [!question]-  Why do we call "[effects](Quantum%20mechanics.md#^Effect)" both the affine functionals $\E_ω,$ and the effect operators $\E(ω)?$ It confuses me as to what [observables](Quantum%20mechanics.md#^Observable) are. Do they map outcomes to effects, or to effect operators? Is the identification of observables and POVMs exact, or indirect like for effects and effect operators?
> 

> [!question]-  How to find $T?$
> Unnecessary(?)

> [!question]-  PN uses $\E:\B(G)\to B(\H)$. Why use $\E:Σ\to B(\H)$? It seems more indirect. Sure, $(G,·)$ can act on itself so this is more general, but what value does this generalization add? We usually end up using $(Σ,·)=(G,·)$ anyway.
> Counterexample: Minkowski is $\rr^4$ but the Poincaré group acting on it is bigger. The frame should be a (tetrad) in $\rr^4.$ The POVM should not be on Poincaré, but on Minkowski.

> [!question]-  [Positive-semidefinite](Linear%20map.md#^SemiPositiveOperator|Positive-semidefinite) operators over $\C$ are [self-adjoint](Linear%20map.md#^SelfAdjoint|self-adjoint), but not over $\rr.$ Should we specify that $\H$ is always a complex Hilbert space? There are reasons why QM should not be done in a real $\H,$ but a [POVM](Measure.md#^POVM|POVM) may not necessarily be about QM. What about quaternionic?
> Just use complex, we don't know much about real or quaternionic $\H.$



