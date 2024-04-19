---
tags: Physics/Mechanics/Quantum_mechanics, Maths/Algebra/Linear_Algebra 
---
# Spectral Theorem
There is a 1-to-1 correspondence between (possibly [unbounded](Linear%20map.md#^UnboundedOperator)) [[Linear map#^SelfAdjoint|self-adjoint operators]] $A:\H\to\H$ and [spectral measures](Measure.md#^SpectralMeasure) $\P^A:\B(\rr)\to \L(\H),$ given by the [integral](Measure.md#^PVMInt):
$$\bra{ψ}A\ket {φ} \equiv\int_{σ(A)} σ \ \bra{ψ}d\P^A(σ)\ket{φ} $$
where $\bra{ψ}d\P^A(σ)\ket{φ}:Σ\to \C$ is a [complex measure](Measure.md#^ComplexMeasure). We [[Measure#^PVMInt|rewrite]] this as the spectral decomposition:
$$A=\int_{σ(A)} σ\ d\P^A(σ)=\P^A[1]$$
We can use this to construct new unique closed operators $f(A)$ like so:
$$\begin{split}
\bra{ψ}f(A)\ket {φ} &\equiv\int_{X} f(σ) \ \bra{ψ}d\P^A(σ)\ket{φ}\\
f(A)&=\int_X f(σ)\ d\P^A(σ)
\end{split}$$
Where $f:X\to\C$ is a [Borel-measurable](Function.md#^MeasurableFunction) [function](Function.md#^Function) on the support of $\P^A,$ which is the [spectrum](Linear%20map.md#^Spectrum) $σ(A).$
$f(A)$ is [self-adjoint](Linear%20map.md#^SelfAdjoint) if $f(σ)\in\rr$
$f(A)$ is [positive-semidefinite](Linear%20map.md#^SemiPositiveOperator) if $f(σ)\ge 0$
Working with these is called *functional calculus for self-adjoint operators*.


