# Quantum reference frames

For our [[Quantum reference frames#^QRF|quantum reference frame]], we choose
$$\begin{split}
\H&=\H_A\otimes \H_B\otimes \H_C\\
(Σ,·)_G &=(\rr,+)_\rr\\
g&=x\\
α(g,X)&=X-x\\
\end{split}$$
such that $U(x)\E(X)U(x)^*=\E(X-x)$ for all $X\in\B(\rr).$

$B(\H)^G\coloneqq\left\{ A\in B(\H)\ |\ g·A=A\right\}$ is the space of **gauge-invariant operators** (analogous to $\H_{\rm{phys}}$ in PN). 
***Hint***: We want these types of operators, and $\H$ is not invariant under the action of $G.$

$\S(\H)_{G}\equiv\S(\H)/\sim_{G}$, but $\S^G(\H)\equiv\{ρ\in\S(\H)\ |\ g· ρ=ρ\}$ do not confuse.

$B(\H)$ is the [[Vector space#^DualSpace|dual]] of $\mathcal{T}(\H).$

---
# Quantum reference frame jumping

This is achieved through the [[Relativization map#^RelMap|relativization map]] $\yen^C:B(\H_A\otimes \H_B)\to B(\H_A\otimes \H_B\otimes \H_C).$
We know that
$$\hat{x}=\int _{\rr}x\ket{x}\bra{x}   \ dx $$
which should be better written as
$$\hat{Q}=\int _{\rr}x\ d\P^Q(x)=\P^Q[1]$$
so when translated to usual physicist notation, our PVM obeys 
$$d\P^Q(x)=\ket{x}\bra{x}\ dx$$
$$\begin{split}
Q_\S&=\int _\rr xd\P^{Q_\S}(x) \\
Q_\S-Q_\R &=Q_\S\otimes I_\R-I_\S\otimes Q_\R=\int _\rr xd\P^{Q_\S}(x) - \int_\rr y \ d\P^{Q_\R}(y)  \\
\end{split}$$
$$\begin{split}
\P^{Q_\S}(X)&=\int_X d\P^{Q_\S}(x)=\int _\rr  χ_X(x) d\P^{Q_\S}(x)\equiv χ_X(Q_\S)\\
\P^{-Q_\S}(X)&=\P^{Q_\S}(-X)=\int_{-X} d\P^{Q_\S}(x)=\int _\rr  χ_{-X}(x) d\P^{Q_\S}(x)=\int _\rr  χ_{X}(-x) d\P^{Q_\S}(x)=χ_X(-Q_\S)\\
\P^{Q_\S-Q_\R}(X)&=\int_X d\P^{Q_\S}(x)\otimes \int_{-X} d\P^{Q_\R}(y)=\int_X d\P^{Q_\S}(x)\otimes d\P^{Q_\R}(-x) =χ_X(Q_\S-Q_\R)\\
\end{split}$$

where $χ_X$ is the [[Function#^IndicatorFunction|indicator function]]. It satisfies $χ_X(x+y)=χ_{X-y}(x)=χ_{X-x}(y).$ 
$\P$ satisfies $U(y)\P^{Q_\S}(X)U^{\dagger}(y)=\P^{Q_\S}(X-y)$ for $U(y)=e^{iyP_\S}$ iff $Q_\S,P_\S$ are canonically conjugate. 

**Exercise:** Show that $(\yen\circ\P^{Q_\S})(X)=\P^{Q_\S-Q_\R}(X).$ 
$$\begin{split}
\bra{ ψ} \yen(\P^{Q_\S}(X))\ket{ψ} &=\bra{ψ}\P^{Q_\S-Q_\R}(X)\ket{ψ}\\
\int_\rr U_\S(x)\P^{Q_\S}(X)U_\S^*(x)\otimes d\P^{Q_\R}(x)&=\int_X d\P^{Q_\S}(x)\otimes \int_{-X} d\P^{Q_\R}(y)
\\
\int_\rr U_\S(x)\l\int_X d\P^{Q_\S}(y)\r U_\S^*(x)\otimes d\P^{Q_\R}(x)&=\iint_{X^2}\l d\P^{Q_\S}(x)\otimes d\P^{Q_\R}(-y)\r
\\
\int_\rr \int_X d\P^{Q_\S}(y\pm x) \otimes d\P^{Q_\R}(x)&=\int_X d\bra{ψ}\P^{Q_\S}\ket{ψ}(x)\otimes d\bra{ψ}\P^{Q_\R}(-x)\ket{ψ}
\\
\iint_\rr χ_X(y) d\bra{ψ} \P^{Q_\S}(y\pm x)\ket{ψ}  \otimes d\bra{ψ} \P^{Q_\R}(x)\ket{ψ} &=
\\
\iint_\rr χ_X(y) |  ψ(y\pm x)|^2 dy \otimes  |  ψ(x)|^2 dx &=\int_\rr χ_X(x) |  ψ(x)|^2 dx\otimes |  ψ(-x)|^2 dx
\end{split}$$
Sanity check: $\yen(\P^{Q_\S}(\rr))=\yen(I_\S)=I_\S\otimes I_\R.$ 

$$\begin{split}
\yen(\P^{Q_\S}(X))&=\P^{Q_\S-Q_\R}(X)\\
(\P^{Q_\S}*\P^{Q_\R})(X)&=\int_X d\P^{Q_\S}(x)\otimes \int_{-X} d\P^{Q_\R}(y)
\\
\int_\rr \P^{Q_\S}(X-x)\otimes d\P^{Q_\R}(x)&= \iint_{\rr^2}\l χ_X(x) d\P^{Q_\S}(x)\otimes χ_X(-y)d\P^{Q_\R}(y)\r
\\
\int_\rr \int _{X} d\P^{Q_\S}(y-x)\otimes d\P^{Q_\R}(x)&=\int_X d\P^{Q_\S}(x)\otimes d\P^{Q_\R}(-x)
\\
\iint _\rr χ_{X-x}(y) d\P^{Q_\S}(y)\otimes d\P^{Q_\R}(x)&=\\
\iint _\rr χ_{X}(y+x)  d\P^{Q_\S}(y)\otimes d\P^{Q_\R}(x)&=\\
\iint _\rr χ_{X}(y+x)  d\P^{Q_\S}(y)\otimes χ_{X}(y+x) d\P^{Q_\R}(x)&=\\
\iint _\rr χ_{X-x}(y)  d\P^{Q_\S}(y)\otimes χ_{X-y}(x) d\P^{Q_\R}(x)&=\\
\iint _\rr \P^{Q_\S}(X-x)\otimes \P^{Q_\R}(X-y)&=\\
\end{split}$$
Change of variable $x\mapsto y/2-x/2$

The operator $Q_\S\otimes I_\R-I_\S\otimes Q_\R$ is self-adjoint, so it has a spectral measure $\P^{Q_\S-Q_\R}.$
This is a rigorous way to show $\yen(Q_\S)=Q_\S-Q_\R.$ 

$χ_{X-x}(y)=1$ if $y\in X-x,$ or $y+x\in X.$ So $χ_X(x+y)=χ_{X-y}(x)χ_{X-x}(y).$ 

We must define our states $ψ\coloneqq\ket{ψ}\bra{ψ}$ so that
$$\begin{split}
\bra{ψ}ψ\ket{ψ}&=\int_\rr |ψ(x)|^2 \ d\bra{ψ}\P(x)\ket{ψ}\\
\braket{ψ}{ψ}\braket{ψ}{ψ}  &=\int_\rr |ψ(x)|^2 \ |ψ(x)|^2\ dx \\
1&=1 \\
\end{split}$$

$$\psi_{AB}(x)\coloneqq\int_{\mathbb{R}}\,\psi(x_{A},x_{B})\begin{vmatrix}\ket{x_{A}+x}\bra{x_{A}+x}\\
\otimes\\
\ket{x_{B}+x}\bra{x_{B}+x}
\end{vmatrix}dx_{A}dx_{B}
$$


$$\begin{split}
\yen^\R(Q_\S) &= \int_\rr U(x)Q_\S U^*(x)\otimes d\P^{Q_\R}(x)
\\&=
\int_\rr U(x)\int _\rr\l y\ d\P^{Q_\S}(y)\r U^*(x)\otimes d\P^{Q_\R}(x)
\\&=
\iint _\rr y\ d\P^{Q_\S}(y\pm x)\otimes d\P^{Q_\R}(x)
\\&=
\iint _\rr \l (y\pm x\mp x)\ d\P^{Q_\S}(y\pm x)\r\otimes d\P^{Q_\R}(x)
\\&=
\iint _\rr (y\pm x)\ d\P^{Q_\S}(y\pm x)\otimes d\P^{Q_\R}(x)\mp\iint _\rr \ d\P^{Q_\S}(y\pm x)\otimes x\ d\P^{Q_\R}(x)
\\&=
\iint _\rr (y+x)\ d\P^{Q_\S}(y+x)\otimes d\P^{Q_\R}(\mp x) - \iint _\rr \ d\P^{Q_\S}(y+x)\otimes x\ d\P^{Q_\R}(\mp x)
\\&=
\mp Q_\S\otimes \hat{I} \pm \hat{I}\otimes Q_\R
\end{split}$$

$$\begin{split}
\yen^{C}(\hat{x}_A)
&= \int_\rr dx
\begin{vmatrix}
x_A\ket{x_A+x}\bra{x_A+x}\\
\otimes\\
\ket x\bra x
\end{vmatrix}
\\&= \int_\rr dx
\begin{vmatrix}
(x_A+x)\ket{x_A+x}\bra{x_A+x}-x\ket{x_A+x}\bra{x_A+x}\\
\otimes\\
\ket x\bra x
\end{vmatrix}
\\&=
\begin{vmatrix}
\hat{x}_A\\
\otimes\\ \hat{I}_C \end{vmatrix}
-
\begin{vmatrix}
\hat{I}_A\\
\otimes\\ \hat{x}_C \end{vmatrix}
\end{split}$$
$$\begin{split}
\yen^{C}(\hat{x}_A\otimes \hat{x}_B)
&= \int_\rr dx
\begin{vmatrix}
x_A\ket{x_A+x}\bra{x_A+x}\\
\otimes\\
x_B\ket{x_B+x}\bra{x_B+x}\\
\otimes\\
\ket x\bra x
\end{vmatrix}
\\&= \int_\rr dx
\begin{vmatrix}
(x_A+x)\ket{x_A+x}\bra{x_A+x}-x\ket{x_A+x}\bra{x_A+x}\\
\otimes\\
(x_B+x)\ket{x_B+x}\bra{x_B+x}-x\ket{x_B+x}\bra{x_B+x}\\
\otimes\\
\ket x\bra x
\end{vmatrix}
\\&=
\begin{vmatrix}
\hat{x}_A\\ \otimes\\ \hat{x}_B\\
\otimes\\ \hat{I}_C \end{vmatrix}
-
\begin{vmatrix}
\hat{x}_A\\ \otimes\\ \hat{I}_B\\
\otimes\\ \hat{x}_C \end{vmatrix}
-
\begin{vmatrix}
\hat{I}_A\\ \otimes\\ \hat{x}_B\\
\otimes\\ \hat{x}_C \end{vmatrix}
+
\begin{vmatrix}
\hat{I}_A\\ \otimes\\ \hat{I}_B\\
\otimes\\ \hat{x}_C^2 \end{vmatrix}
\end{split}$$

---
# Quantum reference frame changing

Like in the perspective-neutral approach, there is a "global'' description of the system. Our [[Vector space#^Hilbert|Hilbert space]] decomposes as $\H_\mathcal{T}\cong\H_1\otimes\H_2\otimes\H_\S$, and $U_\mathcal{T}=U_1\otimes U_2\otimes U_\S$. We assume that $\R_1$ is [[Quantum reference frames#^LocalizableQRF|localizable]].

Ultimately, what we want is a map
$$Φ_{1\to2}:\S(\H_{\R_2}\otimes\H_\S)_{\E_2}^{\R_1}\to\S(\H_{\R_1}\otimes\H_\S)_{\E_1}^{\R_2}$$
where the $\E_{2}$-framed, $\R_{1}$-relative states are
$$\S(\H_{\R_{2}}\otimes\H_\S)_{\E_2}^{\R_1}=\S(\H_{\R_2}\otimes\H_\S)^{\R_1}/\sim_{\E_2}$$
where
$$\begin{align*}
\S(\H)^\R & \coloneqq\S(\H\otimes\H_C)/\sim_C\\
 & \cong\yen_*^{\R}(\S(\H\otimes\H_{C}))
\end{align*}$$
where $\yen_{*}^\R:\S(\H\otimes\H_\R)\to\S(\H)^\R$ is the predual of $\yen^\R.$

This is done using the $ω$-lifting map $\L_ω^\R:\mathcal{T}(\H_\S)^\R\to\mathcal{T}(\H_\R\otimes\H_\S)_G,$ where $ω\in\S(\H_\R)$ is a state.
$$\L_ω^\R\coloneqq(Γ_ω^\R)_*$$
which is the predual of the relativized $\omega$-restriction map $Γ_ω^\R:B(\H_\R\otimes\H_\S)^{G}\to B(\H_\R\otimes\H_\S)$
$$Γ_ω^\R\coloneqq\yen^\R\circ Γ_ω$$
where $Γ_ω:B(\H_\R\otimes\H_\S)\to B(\H_\S)$ is the restriction map
$$Γ_ω(\hat{X}_\R\otimes\hat{Y}_\S)\coloneqq\hat{Y}_\S\ {\tr}(ω\hat{X}_\R)$$
In our case, $Γ_ω:B(\H_C\otimes\H_B)\to B(\H_B)$ is the restriction map
$$Γ_ω(\hat{x}_C\otimes\hat{x}_B)\coloneqq\hat{x}_B\ \tr(ω\hat{x}_C)$$
$\tr(ω\hat{x}_C)$ is mathematician's notation for the expectation value of $\hat{x}_C$ in state $ω,$ where we assume that it is a pure state. So:
$$\begin{split}
\tr(ω\hat{x}_C)&=\bra{ω}\hat{x}_C\ket{ω}\\
&=\int_\R x_{C} \ d\bra{ω}\P(x)\ket{ω}\\
&=\int_\R x_{C}|ω(x_C)|^2 \ dx_C 
\end{split}$$
For Flaminia with no superposition, I think it's reasonable to set $\tr(ω\hat{x}_C)=x_C.$ (maybe make clear that this should be state-dependent in general)
$$Γ_ω(\hat{x}_C\otimes\hat{x}_B)=x_C\ \hat{x}_B$$
$$\begin{split}
Γ_ω^C(\hat{x}_A\otimes\hat{x}_B\otimes\hat{x}_C)&=\yen^C(\hat{x}_A\otimes\hat{x}_B)\ x_C\ \hat{x}_B
\\&= x_C\l
\begin{vmatrix}
\hat{x}_A\\ \otimes\\ \hat{x}_B^2\\
\otimes\\ \hat{I}_C \end{vmatrix}
-
\begin{vmatrix}
\hat{x}_A\\ \otimes\\ \hat{x}_B\\
\otimes\\ \hat{x}_C \end{vmatrix}
-
\begin{vmatrix}
\hat{I}_A\\ \otimes\\ \hat{x}_B^2\\
\otimes\\ \hat{x}_C \end{vmatrix}
+
\begin{vmatrix}
\hat{I}_A\\ \otimes\\ \hat{x}_B\\
\otimes\\ \hat{x}_C^2 \end{vmatrix}\r
\end{split}$$

Since $ω\hat{x}_C\in \mathcal{T}(\H)$ (lie: needs to be bounded), we have $$Γ_ω(\hat{x}_{A}\otimes\hat{x}_{B}\otimes\hat{x}_{C})=\hat{x}_{A}\otimes\hat{x}_{B}\langle\hat{x}_C\rangle_ω .$$ Lie: just use the trace, check how to write that correctly. So $$Γ_ω^{C}(\hat{x}_{A}\otimes\hat{x}_{B}\otimes\hat{x}_{C})=\yen^{C}(\hat{x}_{A}\otimes\hat{x}_{B})\ \tr(ω\hat{x}_{C})$$ for all $ω.$ Now, what is the predual of this?


In Galley, Eq. (25) doesn't make sense:
$$\int _{g\in G} \ket{g}\bra{g}\otimes \hat{I}_0 \otimes U_{R}(g)    \ dg $$
I can see the physicist's notation, which we established should be written as
$$\int _{g\in G} d\P(g)\otimes \hat{I}_0 \otimes U_{R}(g)    \  $$

---
# Questions

> [!question]-  Are $\sim_G$ the [[Action#^G-orbit|G-orbits]]?
> No, but they contain them

 > [!question]-  What is $Ω?$
> Any state in $\H_\R\otimes\H_\S.$

 > [!question]-  How to compute preduals?
> Defined though the [[Linear map#^Trace|trace]] formula, top of page 3, $\tr(TΛ(A))=\tr(Λ_*(T)A)$
