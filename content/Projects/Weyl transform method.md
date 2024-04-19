We want a state $T'$ that corresponds to the pdf $t'(x)=\int_{\rr}\bra{q-x} T\ket{q-x} \, \bra{q}ρ \ket{q}\,dq$ such that $\tr(T'd\P^Q(x))=t'(x).$

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