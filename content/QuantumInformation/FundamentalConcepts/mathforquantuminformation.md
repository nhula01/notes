+++
title = "MathforQuantumInformation"
author = ["DESKTOP-PNLN52S"]
date = 2024-02-27T00:00:00-07:00
lastmod = 2024-02-27T00:00:00-07:00
tags = ["noexport"]
draft = false
+++

**Link**:


## Complete {#complete}

some


## Orthonormal Basis {#orthonormal-basis}


## Tensor Product {#tensor-product}


## Single Qubit Gates {#single-qubit-gates}

Also add eigen values and eigenfunctions
\\[
X = \left(\begin{array}{cc}
0 & 1 \\\\
1 & 0
\end{array}\right)
\\]

\\[
Y
\\]

\\[
Z = \left(\begin{array}{cc}
1 & 0 \\\\
0 & -1
\end{array}\right)
\\]

\\[
H = \frac{1}{\sqrt{2}}\left(\begin{array}{cc}
1 & 1 \\\\
1 & -1
\end{array}\right)
\\]


## Operator {#operator}

An operator is a linear map taking vectors to vectors
\\[ \mathbf{A}: \ket{\psi} \mapsto \mathbf{A} \ket{\psi}\\]


## Adjoint {#adjoint}

The adjoint \\[ \mathbf{A}^{\dagger}\\] is defined by

\\[ \braket{\phi|A\psi} = \braket{A^{\dagger}\phi|\psi}\\]


## Self-Adjoint {#self-adjoint}

It is self-adjoint if \\[ \mathbf{A} = \mathbf{A^{\dagger}}\\] such that
\\[ \bra{\phi} \mathbf{A} \ket{A} = \bra{\psi} \mathbf{A} \ket{\phi}^{\\\\*} \\]

Some properties that we want to know given that we know \\[ \mathbf{A}\\] and \\[ \mathbf{B}\\] self adjoints are:

-   \\[ \mathbf{A} + \mathbf{B}\\] are also self adjoint
-   \\[ ( \mathbf{A} + \mathbf{B})^{\dagger} = \mathbf{A}^{\dagger} + \mathbf{B}^{\dagger} \\] is self adjoint
-   \\[ ( \mathbf{AB})^{\dagger} = \mathbf{B}^{\dagger} \mathbf{A}^{\dagger}\\] is self adjoint
-   \\[ \mathbf{A} \mathbf{B}\\] is self adjoint if the two commute
-   \\[ \mathbf{A} \mathbf{B} + \mathbf{B} \mathbf{A}\\] is self adjoint
-   \\[ i(\mathbf{AB}-\mathbf{BA})\\] is self adjoint

The self adjoint operators have a spectral representation (its eigenstates form a complete and orthonormal basis) such that

\\[
\mathbf{A} = \sum\_n a\_n \mathbf{E\_n}
\\]

where a_n is the eigenvalue with the orthogonal projection \\[ \mathbf{E\_n}\\]. Because it is orthonoral, we also have

\\[
\mathbf{E\_n E\_m} = \delta\_{n,m} \mathbf{E\_n} \\
\mathbf{E^{\dagger}} = \mathbf{E\_n}
\\]

Another way to write the self-adjoint matrix is through the representation of the outer product

\\[
\mathbf{A} = \sum\_n \bra{n}a\_n \ket{a\_n}
\\]

where \\[ \ket{n}\\] are the eigenstates from \\[ \mathbf{A}\ket{n} = a\_n \ket{n}\\]. In this sense,
the outer production is the projection.
