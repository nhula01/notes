+++
title = "QuantumBits"
author = ["DESKTOP-PNLN52S"]
date = 2024-02-27T00:00:00-07:00
lastmod = 2024-02-27T00:00:00-07:00
tags = ["noexport"]
draft = false
+++

**Link**: [MathforQuantumInformation]({{< relref "mathforquantuminformation.md" >}})


## Quick Look at Important Information: {#quick-look-at-important-information}

\\[
\ket{\psi} = \cos{\frac{\theta}{2}} \ket{0} + e^{i\phi} \sin{\frac{\theta}{2}} \ket{1}
\\]


## Details {#details}

Qubits can be in states different than $ \ket{0}$ and $ \ket{1}$.

For example, the qubit could be in the superposition state:
\\[ \ket{\psi} = \alpha \ket{0} + \beta \ket{1} \\].

The states \\[ \ket{0} \\] and  \\[ \ket{1} \\] form a [complete]({{< relref "mathforquantuminformation.md#complete" >}})
and [orthonormal basis]({{< relref "mathforquantuminformation.md#orthonormal-basis" >}}). These states are also called the computational
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

Reference: EEE 492, Quantum Computation and Quantum Information
