Man, they should learn how to make nicer figures... I'm for hire.

Suspicious claim (by Aharonov&Susskind): We may "classicalify away" the position/momentum uncertainty relation by setting $Δx\approx 0$ and having the system's mass $M$ be very large, so that we have $Δp=MΔv$ very large, but $Δv\approx 0,$ so it doesn't matter.
This kind of "cancelling zeroes with infinities" business is suspicious without saying under which conditions it holds.
Anyway, seems unimportant to the big points of the paper.
Later on, they put specific numbers in that operation and it checks out.

Fig. 2, p. 7: What is that "effective wavefunction" for the composite system? Why did they fuse together in a single lump? How does that work? Ohhh I get it! You can't just do the center of mass of a wavefunction and be done with it. Each of those points has a probability, and so the center of mass also has a probability distribution. The effective wavefunction of the composite system is the wavefunction of the system's center of mass.

Big main point of the paper:  Relational coordinates by themselves are, in general, *not* enough to fully describe a physical system! Center-of-mass information needs to be taken into account!
These quantities are not directly observable, but they do have physical consequences e.g. in the uncertainty relations. Throwing out this information is valid classically, but not quantumly. So by claiming that only relational quantities matter, you are being a classicalist!

I'm not sure this logic is watertight: The Born rule implies the existence of a classical $\mathbb{E}^3$ background space, which implies the existence of CRFs. Sure in the case of Flaminia's formalism this is true, but can we steelman it? Couldn't there be a Born rule that does not require such a classical background space? Do we even *have* any formalisms that have quantum space? Spin networks I guess. Do they have a Born rule? If so, I don't think this logic works too well. It could just say "This is for the case in which space-time is classical. Noone has yet investigated the non-classical space-time version yet because it's hard." and it would be fine, no need to obscure that.

Fig. 3, p. 16: Shouldn't O as seen by A be in a superposition of states, i.e. a blob?

Typo in Eq. 3.20: The $p_B$ should be a $\mathbf{p}_B.$

Typo in p.25 beginning: "the former is determined by the the"

Typo in p.29: Missing a dot before "Once her displacement..."

BIG typo in Eq. 3.64: 

# Bipartite system - 2 QRFs 1 CRF

The 2 QRFs are $A$ and $B.$ The CRF is $O.$
$O$ uses $(\mathbf{r},\mathbf{κ})$ coordinates.
$A$ uses $(\mathbf{x},\mathbf{p})$ coordinates.
$B$ uses $(\mathbf{q},\mathbf{π})$ coordinates.
I think what they call $d^3P(\mathbf{x}_B),$ is a trace of what we call $d\P^Q(\mathbf{x}_B).$ 

$AB$ system seen by $O:$$$\ket{Ψ_{AB}^{(O)}}_{AB} = \iint ψ_A(\mathbf{r}_A)\f_B(\mathbf{r}_B)\ \ket{\mathbf{r}_A}_A \ket{\mathbf{r}_B}_B\ d^3r_A\, d^3r_B$$
$OB$ system seen by $A$ (bad choice, one of Flaminia's):$$\begin{split}
\ket{Ψ_{OB}^{\prime(A)}}_{OB}
&= \iint ψ_O(-\mathbf{x}_O)\f_B(\mathbf{x}_B-\mathbf{x}_O)\ \ket{\mathbf{x}_O}_O \ket{\mathbf{x}_B}_B\ d^3x_O\, d^3x_B\\
&= \iint ψ_O(\mathbf{r}_A)\f_B(\mathbf{r}_B)\ \ket{-\mathbf{r}_A}_O \ket{\mathbf{r}_B-\mathbf{r}_A}_B\ d^3r_A\, d^3r_B\\
\end{split}$$
$OB$ system seen by $A$ (good choice):$$\begin{split}
\ket{Ψ_{OB}^{(A)}}_{OB}
&= \iint ψ_O(-\mathbf{x}_O)\f_B(\mathbf{x}_B-\mathbf{x}_O)\ \ket{\mathbf{x}_O}_O \ket{\mathbf{x}_B-\mathbf{x}_O}_B\ d^3x_O\, d^3x_B\\
&= \iint ψ_O(\mathbf{r}_A)\f_B(\mathbf{r}_B)\ \ket{-\mathbf{r}_A}_O \ket{\mathbf{r}_B}_B\ d^3r_A\, d^3r_B\\
\end{split}$$


"The predictions of our QRF model depend on the chosen projector $\hat{Π}_{\ket{\text{Bob}=φ^{(A)}_B}_{OB}},$ but not on the basis used to express the ‘objective’ state, $\ket{Ψ^{(O)}_{AB}}_{AB}$. This is as it should be, since the former is determined by the measurements we choose, whereas the latter is not. For position measurements, we project onto the basis ${|\mathbf{x}_O⟩_O |\mathbf{x}_B − \mathbf{x}_O⟩_B},$ whereas for momentum measurements, we project onto the basis ${|\mathbf{p}_O⟩_O |\mathbf{p}_B − \mathbf{p}_O⟩_B}.$ Crucially, we see that these are not mutually exclusive. There exists a single bipartite state, $|Ψ^{(A)}_{OB}⟩_{OB} := \hat{P}_{O↔A} |Ψ^{(O)}_{AB}⟩_{AB}$ (3.46), that is compatible with both transformations."
(I have no idea what $\hat{P}_{O\leftrightarrow A}$ is. A typo for the parity-swap operator? They start by calling it $\mathcal{P}_{O\leftrightarrow A},$ but then they switch)

They define what is probably akin to the [restriction map](Quantum%20mechanics.md#^RestrictionMap), but with a [partial trace](Linear%20map.md#^PartialTrace):$$\hat{ρ}^{(A)}_B :=\int\tr_{O}\l\ket{\mathbf{x}_O}\bra{\mathbf{x}_O}_O \otimes  \hat{U}_B(\mathbf{x}_O) \hat{ρ}_{OB}^{(A)}\r \, d^3x_O$$

# Uncertainty relations

I didn't check the maths in detail, I'm sure they're correct. Uncertainty relations of Bob, as seen by Alice:$$\begin{split}
(Δ_ρx^i_B)(Δ_ρ p_{Bj})
%&=
 % (Δ_ψr^i_A)^2(Δ_ρp_{Bj})^2
%+(Δ_ρx^i_B)^2(Δ_ψ κ_{Aj})^2
%+(Δ_ψ r^i_B)^2(Δ_ψ κ_{Aj})^2
%-(Δ_\f r^i_B)^2(Δ_\f κ_{Bj})^2\\
&\ge \hbar δ^i_{\,j}
\end{split}$$This is compatible with my finding that the UR of a relativized+restricted system should be twice that of the system alone. My result says $2\hbar,$ but that's because their observables are sharp and mine are smeared, which doubles the UR yet again.


"The important point is that, *if* a real physical observer could be embodied as a classical object - that is, as a material body that is perfectly well localised in both position and momentum space - they would be able to measure not only the relative position and momentum of Alice and Bob, but also their ‘objective’ positions and momenta, relative to a classical frame of reference defined with respect to the background geometry."
Meaning not a sharp position/momentum measurement, just that the 4 degrees of freedom are accessible, which Flaminia makes impossible in her formalism.

"By combining her data on both position and momentum measurements, and using these relations, Alice is, at least in principle, able to determine her own position and momentum uncertainties, albeit *indirectly*, via their effect on the uncertainty relations she attributes to Bob. If the latter are found to deviate from the canonical Heisenberg form, according to Eqs. (3.64), then Alice is able to determine that both she and Bob are quantum mechanical in nature."
They go on to say that a similar effect could be used to detect space-time quantization.

This is *weird*. If true, it would imply that we can, at least in a limited way, detect our own decoherence. Is this not a *huge* deal? Is this not the same as saying that we can detect the effects of different MWI branches?
