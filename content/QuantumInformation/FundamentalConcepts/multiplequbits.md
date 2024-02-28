+++
title = "MultipleQubits"
author = ["DESKTOP-PNLN52S"]
date = 2024-02-27T00:00:00-07:00
lastmod = 2024-02-27T00:00:00-07:00
tags = ["noexport"]
draft = false
+++

**Link**:


## Quick Information: {#quick-information}

The n-qubit system has \\(2^n\\) computational basis states.

The four EPR qubit states are:

\\[
\ket{\phi\_{\pm}} = \frac{1}{\sqrt{2} } (\ket{00} \pm \ket{11}) \\
\ket{\psi\_{\pm}} = \frac{1}{\sqrt{2} } (\ket{01} \pm \ket{10})
\\]


## Details {#details}

We can combine multiple single qubits together to create a bigger system. For example, we can combine:

\\[
\ket{\psi\_1} = \alpha\_1 \ket{0} + \beta\_1 \ket{1} \\
\ket{\psi\_2} = \alpha\_2 \ket{0} + \beta\_2 \ket{1} \\
\\]

through the [tensor product]({{< relref "mathforquantuminformation.md#tensor-product" >}}) to obtain:

$$

\begin{aligned}
	\ket{\psi} &= \ket{\psi\_1} \otimes \ket{\psi\_2} \\
&= (\alpha\_1 \ket{0} + \beta\_1 \ket{0}) \otimes (\alpha\_2 \ket{0} + \beta\_2 \ket{0}) \\
&= \alpha\_1 \alpha\_2 \ket{00} + \alpha\_1 \beta\_2 \ket{01}
+ \beta\_1 \alpha\_2 \ket{10} + \beta\_1 \beta\_2 \ket{11}
\end{aligned}

$$

Now, the new computational basis has \\(2^2\\) states \\[ \ket{00}, \ket{01}, \ket{10}, \ket{11}\\].

In this sense, we can create \\[n\\] qubit state system with \\[2^n\\] computational basis states.

Most notable two qubit states are the bell states (EPR). These states create the entanglement between two states
which have spooky action at a distance. The four EPR states are:

\\[
\ket{\phi\_{\pm}} = \frac{1}{\sqrt{2} } (\ket{00} \pm \ket{11}) \\
\ket{\psi\_{\pm}} = \frac{1}{\sqrt{2} } (\ket{01} \pm \ket{10})
\\]
