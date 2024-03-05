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


## Orthonormal Basis {#orthonormal-basis}


## Tensor Product {#tensor-product}


## Single Qubit Gates {#single-qubit-gates}

\left(\begin{array}{cc}
0 &amp; 1 <br />
1 &amp; 0
\end{array}\right)


## Operator {#operator}

An operator is a linear map taking vectors to vectors
\\[ \mathbf{A}: \ket{\psi} \mapsto \mathbf{A} \ket{\psi} \\]


## Adjoint {#adjoint} {#adjoint-adjoint}

The adjoint \\[ \mathbf{A}^{\dagger} \\] is defined by

\\[ \braket{\phi|A\psi} = \braket{A^{\dagger}\phi|\psi} \\]


## Self-Adjoint {#self-adjoint}

It is self-adjoint if \\[ \mathbf{A} = \mathbf{A^{\dagger}} \\] such that
\\[ \bra{\phi} \mathbf{A} \ket{A} = \bra{\psi} \mathbf{A} \ket{\phi}^{\\\\\\*}  \\]

Some properties that we want to know given that we know \\[ \mathbf{A}\\]  and \\[  \mathbf{B}\\]  self adjoints are:

-   \\[  \mathbf{A} + \mathbf{B}\\]  are also self adjoint
-   \\[  ( \mathbf{A} + \mathbf{B})^{\dagger} = \mathbf{A}^{\dagger} + \mathbf{B}^{\dagger} \\]  is self adjoint
-   \\[  ( \mathbf{AB})^{\dagger} = \mathbf{B}^{\dagger} \mathbf{A}^{\dagger}\\]  is self adjoint
-   \\[  \mathbf{A} \mathbf{B}\\]  is self adjoint if the two commute
-   \\[  \mathbf{A} \mathbf{B} + \mathbf{B} \mathbf{A}\\]  is self adjoint
-   \\[  i(\mathbf{AB}-\mathbf{BA})\\]  is self adjoint

The self adjoint operators have a spectral representation (its eigenstates form a complete and orthonormal basis) such that

\\[
\mathbf{A} = \sum\\\_n a\\\_n \mathbf{E\\\_n}
\\]

where a_n is the eigenvalue with the orthogonal projection \\[  \mathbf{E\\\_n}\\] . Because it is orthonoral, we also have

\\[
\mathbf{E\\\_n E\\\_m} = \delta\\\_{n,m} \mathbf{E\\\_n} \\\\
\mathbf{E^{\dagger}} = \mathbf{E\\\_n}
\\]

Another way to write the self-adjoint matrix is through the representation of the outer product

\\[
\mathbf{A} = \sum\\\_n \bra{n}a\\\_n \ket{a\\\_n}
\\]

where \\[  \ket{n}\\]  are the eigenstates from \\[  \mathbf{A}\ket{n} = a\\\_n \ket{n}\\] . In this sense,
the outer production is the projection.


## Symmetry {#symmetry}

A symmetry is a transformation that acts on a state of a system, yet leaves
all observable properties of the system unchanged. Thus,

\\[
\ket{\psi} \mapsto \ket{\psi'} = \mathbf{U} \ket{\psi}
\\]

preserves\\[||\braket{\psi|\phi}|| =||\braket{\psi'|\phi'}    ||\\]

Symmetries form a group:

-   Each transformation can be inverted

<!--listend-->

-   Two symmetries form another symmetry

<!--listend-->

-   For any symmetry operation R, there exists a unitary \\[ \mathbf{U( R)}\\]

$$

  \begin{aligned}
  \mathbf{U}(R\_1) \mathbf{U}(R\_2) = phase(R\_1,R\_2) \mathbf{U}(R\_1 R\_2)
\end{aligned}

$$

Symmetry is cummutative with the system. Meaning: transform and then evolve is the same
as to evolve and then transform.

$$

\begin{aligned}
	\mathbf{U}( R) e^{-it \mathbf{H}} = e^{-it \mathbf{H}} \mathbf{U}( R) (2)
\end{aligned}

$$

Expanding the evolution in taylor series:
$$

\begin{aligned}
	e^{-it \mathbf{H}} = \mathbf{I}- i \mathbf{H} t + ..
\end{aligned}

$$

Up to first order, we obtain:

$$

\begin{aligned}
	\mathbf{U}( R) \mathbf{H} = \mathbf{H} \mathbf{U}( R)
\end{aligned}

$$


## Generator of symmetry {#generator-of-symmetry}

Let \\[ R = I + \epsilon T\\] such as it is so close to identiyy, then our unitary
operation is also close to identity.

$$

\begin{aligned}
\mathbf{U}(I+\epsilon T) = \mathbf{I} - i\epsilon \mathbf{Q} + O(\epsilon^2)
\end{aligned}

$$

where \\[ Q\\] is an operator determined by R and is an observable \\[ \mathbf{Q} = \mathbf{Q}^{\dagger}\\].
We could see that up to order \\[ \epsilon\\].

$$

\begin{aligned}
	\mathbf{U}( R) \mathbf{H} &= \mathbf{H} \mathbf{U}( R) \\
(\mathbf{I} - i\epsilon \mathbf{Q}) \mathbf{H} &= \mathbf{H} (\mathbf{I} - i\epsilon \mathbf{Q})
\end{aligned}

$$

leads to

$$

\begin{aligned}
	\mathbf{QH} = \mathbf{HQ}
\end{aligned}

$$

which shows that the observable \\[ \mathbf{Q}\\] commutes with the Hamiltonian

\\[
[\mathbf{Q,H}] = 0
\\]

The equation above is the conservation law. The eigenstates of \\[ \mathbf{Q}\\] is preserved
by the evolution by \\[ \mathbf{H}\\].

By repeating applying the continuous/infinitesimal symmetry like below when  \\[ N \to \infty\\], we have a finite transformation on the system.
$$

\begin{aligned}
	R = (1+ \frac{\theta}{N}T)^N \to
\mathbf{U}( R) = (\mathbf{I} + i \frac{\theta}{N} \mathbf{Q})^N \to e^{i \theta \mathbf{Q}}
\end{aligned}

$$

(q ehere)

We say that \\[ \mathbf{Q}\\] is the generator of the symmetry.
