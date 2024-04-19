---
width: "1920"
height: "1080"
enableLinks: "true"
theme: my theme
transition: none
timeForPresentation: "600"
---
<!-- slide bg="[[Meta hole.png]]" -->
<grid drag="90 20" drop="5 13">
# Designing an optical black hole using Transformation Optics without infinite parameters <!-- element style="color:beige" -->
</grid>

<grid drag="90 20" drop="5 -12">
Miguel Jorquera

Supervised by Jonathan Gratus

2018
<!-- element style="color:beige" -->
</grid>

note: Hello, my name is Miguel Jorquera and I will be presenting my Master's project that I did at Lancaster University. This is actually old work for me, from 5 years ago, and it doesn't have that much to do with my current interest, which are quantum foundations, and mainly quantum reference frames, but I think it's still a really cool project. It consisted on designing an optical black hole, which is a material, or more likely metamaterial, that as far as light is concerned, has the same properties as a black hole, so if we built one, it would look like a black hole. It all starts with the field of Transformation optics.

---

# Transformation optics

Designing the optical properties of a medium to match those of a space-time transformation.

Cloaking devices!
Perfect lenses!
History rewriters!

![[Transpormation optics.png|1024]]

Desired transformed space $\longleftrightarrow$ Real space with a medium

note: Transformation optics consists of equating the effects of a space-time transformation to the effects of an optical medium in the non-transformed space-time, to build a device that mimics the space-time transformation for light. You can use it to build all sorts of crazy devices. This here would be a cloaking device.

Except for history rewriters, most of these devices have been actually built. Here are two examples:

---

<grid drag="50 90" drop="left" justify-content="space-between">
## Omnidirectional absorber

![[Real hole.png|800]]

Qiang Cheng *et al* 2010 *New J. Phys.* **12** 063006
</grid>

<grid drag="50 90" drop="right" justify-content="space-between">
## Negative-index superlens

![[Negative-index superlens.png|512]]

K. Aydın 2008, doctoral dissertation, Bilkent U.
</grid>

note: Left is almost a real-life optical black hole. It absorbs light coming from all directions. If we had microwave vision it would look amazing. For years thought impossible, that TO was a mathematical curiosity, because you need negative refraction.

But that is precisely what you see on the left. This is a superlens, which can resolve things with wavelengths much smaller than the diffraction limit allows for regular lenses.

I said "almost" because it doesn't simulate a gravitational black hole, it just absorbs light. This is because, as you will see later, simulating a black hole in the naïve way would require some of the optical parameters to become infinite at the horizon.

This was my job to fix during my Master's. I was to design an optical black hole without these infinite parameters.

Usually I try putting only the simplest equations, but with this audience, I think it will be fun to get our hands dirty.

---

## Tricking light into thinking it's in a black hole


The constitutive relations relate $F$ (contains $\vec{E}$ and $\vec{B}$) to $G$ (contains $\vec{D}$ and $\vec{H}$):

$$\begin{split}
G &= \star χ F\\\\
G_{μν} &= {{\star_{μν}}}^{αβ} {χ_{αβ}}^{γδ} F_{γδ}
\end{split}$$

Optical properties of the medium are in the **constitutive tensor** $χ.$ 

Optical properties of space-time are in the **Hodge star operator** $\star.$

EM fields can't distinguish $\star$ and $χ:$

$$\begin{split}
\star_\mathrm{lab}\ χ_\mathrm{lab} &= \star_\mathrm{black\ hole}\ χ_\mathrm{vacuum}\\\\
χ_\mathrm{lab}&= -\star_\mathrm{lab}\ \star_\mathrm{black\ hole} \\\\
\end{split}$$

This is **Plebanski's formula**, the cornerstone of this work. With indices:

$$\boxed{{χ_{αβ}}^{γδ}=
-{\star_{αβ}}^{μν}\ {\hat\star_{μν}}^{γδ}}$$


note: Start with the constitutive relations, which relate the EM tensor *F* to the excitation tensor *G*. Or the *E* and *B* to the *D* and *H* fields. Simpler to work with the full tensorial equation.

So, *G* is the Hodge dual of the constitutive tensor *χ* contracted with *F*. It encodes the information about the space-time shape because only it contains the metric, and *χ* encodes the information about the optical medium. Some conventions don't include ★ here, and place it in Maxwell's eqs, and there may be good reasons, but this will make things more clear.

Now, the key thing to notice is that ★ and *χ* always appear together, so electromagnetic fields can't really tell the difference between them. We can take ★*χ* as one. If we take the same ★*χ*, make one side be a black hole in vacuum and the other flat space, whatever *χ* remains, will be our desired optical black hole! Plebanski's formula, cornerstone of TO.

---

${χ_{αβ}}^{γδ}$ has $4^4=256$ elements.

Antisymmetry ${χ_{[αβ]}}^{[γδ]}$ makes only $((4^2-4)/2)^2=36$ be independent.

Easier to translate $χ$ into four $3\times 3$ matrices $ζ:$

$$\begin{split}
\vec{D}=ζ^{DE}\ \vec{E}+ζ^{DB}\ \vec{B}\\\\
\vec{H}=ζ^{HB}\ \vec{B}+ζ^{HE}\ \vec{E}
\end{split}$$

note: Before we go on, a technical issue: the χ tensor is too unwieldy for humans, but by exploiting its symmetries we can get it down to a more manageable set of four 3x3 matrices, each of which transforms one field component into another. So for example ζDE gives the contribution of the E field to the D field. Much simpler to understand.

---

# 
<grid drag="100 20" drop= "0 10" justify-content="start">
## Calculation sample for the simplest black hole metric (Schwarzschild, 6 non-zero numbers to calculate):
</grid>


<font size=4>

<grid drag="20 65" drop="0 -3" justify-content="start" align="left">
We start with Plebanski's formula with $\text g=\eta$ being the flat lab metric and $\hat{\text{g}}$ being the optical Schwarzschild metric:

$$
χ\_{αβ}^{\ \ γδ}
=-\frac{\sqrt{|\eta||\hat{\text{g}}|}}{4}
\epsilon\_{\alpha\beta\rho\sigma}\eta^{\rho\mu}\eta^{\sigma\nu}
\epsilon\_{\mu\nu\tau\eta}\hat{\text{g}}^{\tau\gamma}\hat{\text{g}}^{\eta\delta}.
$$

We use our formulas for the $ζ$ matrices:

$$\begin{split}
{(ζ^{DE})\_b}^{a}&=2\chi\_{b0}^{\ \ a 0}\\\\
&=-\frac{\sqrt{|\hat{\text g}||\eta|}}{2}
\epsilon\_{b0\rho\sigma}\eta^{\rho\mu}\eta^{\sigma\nu}
\epsilon\_{\mu\nu\tau\eta}\hat{\text g}^{\tau a}\hat{\text g}^{\eta 0}.
\end{split}$$

Focus only on the non-zero elements. g and $\hat{\text g}$ are diagonal (i.e. g$^{\alpha\beta}= 0$ if $\alpha\neq\beta$):

$$
{(ζ^{DE})\_b}\^{a}
=-\frac{\sqrt{|\hat{\text g}||\eta|}}{2}
\epsilon\_{b0cd}\eta\^{c\bar c }\text g\^{d\bar d }
\epsilon\_{\bar c\bar d  \bar a  0}\hat{\text g}\^{\bar a a}\hat{\text g}\^{0 0},
$$
</grid>

<grid drag="20 65" drop= "25 -5" justify-content="start" align="left">
where the value of $a$ must be the same as the value of $\bar a$ for the corresponding term to be non-zero.
We know that $\epsilon_{cda 0}=\epsilon_{a0cd}=-\epsilon_{0acd}$, so:

$${(ζ^{DE})\_b}^{a}
=-\frac{\sqrt{|\hat{\text g}||\eta|}}{2}
\epsilon_{0bcd}\epsilon_{0\bar a\bar c\bar d}
\eta^{c\bar c}\eta^{d\bar d}
\hat{\text g}^{\bar a a}\hat{\text g}^{00}.$$

By looking at $\epsilon_{0bcd}\epsilon_{0\bar a\bar c\bar d}$, we can see that this expression will only be non-zero if $\bar a=b\neq 0$.
So there are 3 non-zero terms:
$$\begin{split}
(\zeta^{DE})^1\_1
&=-\frac{\sqrt{|\hat{\text g}||\eta|}}{2}
\epsilon\_{01cd}\epsilon\_{01\bar c\bar d}
\eta^{c\bar c}\eta^{d\bar d}
\hat{\text g}^{11}\hat{\text g}^{0 0}\\\\
&=-\frac{\sqrt{|\hat{\text g}||\eta|}}{2}
(\epsilon_{0123}\epsilon\_{0123}
\eta^{22}\eta^{33}+\epsilon\_{0132}\epsilon\_{0132}
\eta^{33}\eta^{22})
\hat{\text g}^{11}\hat{\text g}^{0 0}\\\\
&=-\frac{r^4\sin^2\theta}{2}
(\eta^{22}\eta^{33}+\eta^{33}\eta^{22})
\hat{\text g}^{11}\hat{\text g}^{0 0}\\\\
&=-\frac{r^4\sin^2\theta}{2}\frac{2}{r^4\sin^2\theta}
1(-1)\\\\
&=1.
\end{split}
$$
</grid>

<grid drag="20 65" drop= "50 -5" justify-content="start" align="left">
$$
\begin{split}
(\zeta^{DE})^2\_2
&=-\frac{\sqrt{|\hat{\text g}||\eta|}}{2}
\epsilon_{02cd}\epsilon_{02\bar c\bar d}
\eta^{c\bar c}\eta^{d\bar d}
\hat{\text g}^{22}\hat{\text g}^{0 0}\\\\
&=-\frac{\sqrt{|\hat{\text g}||\eta|}}{2}
(\eta^{11}\eta^{33}+\eta^{33}\eta^{11})
\hat{\text g}^{22}\hat{\text g}^{0 0}\\\\
&=-\frac{r^4\sin^2\theta}{2}
(2(-1)\frac{1}{r^2\sin\theta})
\frac{1}{r^2}(1-\frac{R}{r})^{-1}\\\\
&=(1-\frac{R}{r})^{-1}.
\end{split}$$

$$
\begin{split}
(\zeta^{DE})^{3}\_{3}
&=-\frac{\sqrt{|\hat{\text g}||\eta|}}{2}
\epsilon\_{03cd}\epsilon_{03\bar c\bar d}
\eta^{c\bar c}\eta^{d\bar d}
\hat{\text g}^{33}\hat{\text g}^{0 0}\\\\
&=-\frac{\sqrt{|\hat{\text g}||\text{g}|}}{2}
(\eta^{11}\eta^{22}+\eta^{22}\eta^{11})
\hat{\text g}^{33}\hat{\text g}^{0 0}\\\\
&=-\frac{r^4\sin^2\theta}{2}
(2(-1)\frac{1}{r^2})
\frac{1}{r^2\sin\theta}(1-\frac{R}{r})^{-1}\\\\
&=(1-\frac{R}{r})^{-1}.
\end{split}
$$

 Therefore:
 $$\boxed{
 \zeta^{DE}=\begin{bmatrix}
 1 & 0 & 0\\\\
 0 & (1-\frac{R}{r})^{-1} & 0\\\\
 0 & 0 & (1-\frac{R}{r})^{-1}
 \end{bmatrix}}$$
</grid>

<grid drag="20 65" drop="75 -5" justify-content="start" align="left">
$$\begin{split}
{(ζ\^{HB})\_b}^{a} &= 2\hat{\star}\^{\ \ μν}\_{0b}\star_{μν}\^{\ \ a 0}
\\\\
&= \frac{\sqrt{|\hat{\text{g}}||\text{g}|}}{2}\epsilon\_{0bρσ}\hat{\text{g}}\^{ρμ}\hat{\text{g}}\^{ρν}
\epsilon\_{μνκλ}η\^{κa}η\^{λ0}
\\\\
&= \frac{r\^4\sin\^2\theta}{2}
\epsilon\_{0bcd}\hat{\text{g}}\^{c\bar c}\hat{\text{g}}\^{d\bar d}
\epsilon\_{\bar c\bar d\bar a0}η\^{\bar aa}η\^{00}
\\\\
&=\frac{r^4\sin^2\theta}{2}
\epsilon_{0bcd}\hat{\text{g}}^{c\bar c}\hat{\text{g}}^{d\bar d}
\epsilon_{\bar c\bar d\bar a0}\eta^{\bar aa}\eta^{00}
\end{split}$$

$$\begin{split}
(\zeta^{HB})^1_1&=\frac{r^4\sin^2\theta}{2}(
\epsilon_{0123}\hat{\text{g}}^{22}\hat{\text{g}}^{33}
\epsilon_{2310}\eta^{11}\eta^{00}+
\epsilon_{0132}\hat{\text{g}}^{33}\hat{\text{g}}^{22}
\epsilon_{3210}\eta^{11}\eta^{00}
)
\\\\&=-\eta^{11}\eta^{00}\\\\
&=1.
\end{split}
$$

$$\begin{split}
(\zeta^{HB})^2_2&=\frac{r^4\sin^2\theta}{2}(
\epsilon_{0213}\hat{\text{g}}^{11}\hat{\text{g}}^{33}
\epsilon_{1320}\eta^{22}\eta^{00}+
\epsilon_{0231}\hat{\text{g}}^{33}\hat{\text{g}}^{11}
\epsilon_{3120}\eta^{22}\eta^{00}
)
\\\\&
=-\hat{\text{g}}^{11}\\\\
&=-\big(1-\frac{R}{r}\big)
\end{split}$$

$$\begin{split}
(\zeta^{HB})^3_3&=\frac{r^4\sin^2\theta}{2}(
\epsilon_{0312}\hat{\text{g}}^{11}\hat{\text{g}}^{22}
\epsilon_{1320}\eta^{33}\eta^{00}+
\epsilon_{0321}\hat{\text{g}}^{22}\hat{\text{g}}^{11}
\epsilon_{2130}\eta^{33}\eta^{00}
)\\\\
&=-\hat{\text{g}}^{11}
\\\\&
=\big(1-\frac{R}{r}\big).
\end{split}$$

Therefore:
$$
\boxed{\zeta^{HB}=\begin{bmatrix}
 1 & 0 & 0\\\\
 0 & (1-\frac{R}{r}) & 0\\\\
 0 & 0 & (1-\frac{R}{r})\\\\
 \end{bmatrix}}
 $$
</font>
</grid>

# 

note: Now, a more difficult technical issue is this right here. Don't even try to read it, this is just to show you how long it takes. This is the simplest calculation required for the simplest Schwarzschild black hole, which only requires you to calculate 6 numbers out of the 36 possible ones. And this is the polished version, this is not what it will look like when you try to do it for the first time. It will be at least 5 times longer.

---
<grid drag="50 65" drop="0 5" justify-content="start">
# Problem:

Metric tensor

$$\bigg\downarrow$$

1-3 hours of work

$$\bigg\downarrow$$

Result
</grid>

<grid drag="50 65" drop="50 5" justify-content="start"> <!-- element class="fragment" data-fragment-index="1" -->

# My solution: 

Metric tensor

$$\bigg\downarrow$$

200-500 hours of work

$$\bigg\downarrow$$

Computer program

$$\bigg\downarrow$$

Result
</grid>

note: So it's a few hours of work per calculation, which is a bit annoying, but I guess this is reasonable for a Master's project, I will need to do it a few dozen times, but after that I will have my result, and my Master's degree.

OR! What I could do instead, is to write an entire computer program that will calculate the result for me, and not only my result for a simple black hole, but for for any metric tensor that you can write! Let me show you.


---

# Summary

- Goal: Design an optical black hole with finite optical parameters
- Python program automates the calculation
- Works for any metric tensor
- Achieve the goal by using Eddington-Finkelstein coordinates
- Bonus: We can now design a Kerr-Newman black hole
- Building a real one is trivial and left as an exercise for the reader
