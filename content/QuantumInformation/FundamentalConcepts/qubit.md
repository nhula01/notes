+++
title = "qubit"
author = ["DESKTOP-PNLN52S"]
date = 2024-02-29T00:00:00-07:00
lastmod = 2024-02-29T00:00:00-07:00
tags = ["moc"]
draft = false
+++

**Link**:


## Quick Look at Important Information: {#quick-look-at-important-information}

\\[
\ket{\psi} = \cos{\frac{\theta}{2}} \ket{0} + e^{i\phi} \sin{\frac{\theta}{2}} \ket{1}
\\]


## Details {#details}

Qubits can be in states different than $ \ket{0}$ and $ \ket{1}$.

For example, the qubit could be in the superposition state:
\\[ \ket{\psi} = \alpha \ket{0} + \beta \ket{1} \\].

The states \\[ \ket{0} \\] and  \\[ \ket{1} \\] form a complete [Complete]({{< relref "math-for-qis.md#complete" >}})
and [orthonormal basis]({{< relref "math-for-qis.md#orthonormal-basis" >}}). These states are also called the computationaal
bases.

When we measure this qubit in computational basis, the result we get
is either \\[ \ket{0}\\] or \\[ \ket{1}\\] with the probability of \\[|\alpha|^2\\]
or \\[|\beta|^2\\] respectively.

We can write the general state \\[ \ket{\psi}\\] in terms of a global phase and a relative phase. Assume:

$$

\begin{aligned}
	\alpha &= \cos{\frac{\theta}{2}} e^{i \phi\_\alpha} \\
\beta &= \sin{\frac{\theta}{2}} e^{i\phi\_\beta}
\end{aligned}

$$

where \\[0 \leq \theta \leq \pi\\] around the Z axis and \\[0 \leq \phi\_\alpha \phi\_\beta < 2\pi\\] spanding the XY plane

Therefore, the general state is given:

$$

\begin{aligned}
	\ket{\psi} &= \alpha \ket{0} + \beta \ket{1} \\
&= \cos{\frac{\theta}{2}} e^{i\phi\_\alpha}\ket{0} + \sin{\frac{\theta}{2}} e^{i\phi\_\beta} \ket{1}  \\
&= e^{i\phi\_\alpha} (\cos{\frac{\theta}{2}} \ket{0} + e^{i(\phi\_\beta - \phi\_\alpha)} \sin{\frac{\theta}{2}} \ket{1})
\end{aligned}

$$

The global phase will collapse after measurement without any observable effects. However,
the relative phase \\[e^{i\phi}\\] plays a very important role. (Note: \\[e^{i(\phi\_\beta-\phi\_\alpha)}\\])

One might wonder how much information the qubit could store. Before the measurement, the qubit superposition seems
to cover all the space. However, the information only collapses to 1 bit at the end.


## Spin 1/2 representation {#spin-1-2-representation}

From the definition of [symmetry]({{< relref "math-for-qis.md#symmetry" >}}) and [generator]({{< relref "math-for-qis.md#generator-of-symmetry" >}})
Let's now apply to rotations! An infinitestimal rotation counterclockwise about
\\[ \hat{n} = (n\_1,n\_2,n\_3)\\] is expressed as:

\\[
R(\hat{n},\theta) = I - i d\theta \hat{n} \cdot \vec{J}
\\]

Thus, a finite rotation is:

\\[
R(\hat{n},\theta) = e^{-i \theta \hat{n} \cdot \vec{J}}
\\]

Rotation of distinct axis dont commute since the relations is.
\\[
[J\_k,J\_l] = i \epsilon\_{klm} J\_m
\\]

Now, we find the unitary version of rotations \\[ \mathbf{J}\\]

continue nextime here

Reference: EEE 492, Quantum Computation and Quantum Information, Preskill's Lecture
