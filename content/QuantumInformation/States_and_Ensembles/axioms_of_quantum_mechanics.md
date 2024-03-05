+++
title = "axioms-of-quantum-mechanics"
author = ["DESKTOP-PNLN52S"]
date = 2024-02-28T00:00:00-07:00
lastmod = 2024-02-28T00:00:00-07:00
tags = ["noexport"]
draft = false
+++

**Link**:

We know that all quantum systems must essentially be open, but it is always good to study the system as
a closed system at first


## Axiom 1 States {#axiom-1-states}

A state is a complete description of a physical system. In quantum mechanics, a state is a ray (norm 1) in [Hilbert space]({{< relref "hilbert_space.md" >}}).

A ray is a state for which \\[ \braket{\psi|\psi} = 1\\]. The global phase could be ignored.

Given any two states, we can write as in the [qubit]({{< relref "qubit.md" >}})


## Axiom 2. Observables {#axiom-2-dot-observables}

An observable is a property of a physical system that in principle can be measured. In quantum mechanics, an
observable is a [self-adjoint]({{< relref "math-for-qis.md#self-adjoint" >}}) operator.


## Axiom 3. Measurement {#axiom-3-dot-measurement}

A measurement is a process in which the information about the state of a physical system is acquired by an observer.
In quantum mechanics, the measurement of an observable \\[ \mathbf{A}\\] prepares an eigenstate of \\[ \mathbf{A}\\]
and the observer learns the value of the corresponding eigenvalue. If the quatum state just prior to the measurement
is \\[ \ket{\psi}\\], then the outcome \\[ a\_n\\] is obtained with a prior probability of :

\\[
Prob(a\_n) = || \mathbf{E\_n} \ket{\psi}||^2 = \bra{\psi} \mathbf{E\_n} \ket{\psi}
\\]

If the outcome \\[ a\_n\\] is obtained, then the quatum state collapses to:

\\[
\frac{\mathbf{E\_n} \ket{\psi}}{||\mathbf{E\_n \ket{\psi}}||}
\\]

If we repeat this measurement on the same basis state again, we will obtain the probability of 1 getting \\[ a\_n\\]

By repeating measuring many identical qubits, the expectation outcome is

\\[
\langle a \rangle = \sum\_n a\_n \bra{\psi} \mathbf{E\_n} \ket{\psi} = \bra{\psi} \mathbf{A} \ket{\psi}
\\]


## Axiom 4. Dynamics {#axiom-4-dot-dynamics}

Dynamics describes how a state evolves over time. In quantum mechanics, the time evolution of a closed system is described by a unitary operator

Give a unitary operator \\[ U(t',t)\\], the evolution from \\[ t \mapsto t'\\] is:

\\[ \ket{\psi(t')} = U(t',t) \ket{\psi(t)}\\]

For infinitesimal time evolution, it is governed by the Schrodinger equation

\\[
\frac{d}{dt} \ket{\psi(t)} = -i \mathbf{H(t)} \ket{\psi(t)} \quad \textbf{(1)} \\
\ket{\psi(t)} = e^{-i \mathbf{H(t)}t} \ket{\psi(0)}
\\]

where \\[ \mathbf{H}\\] is the hamiltonian of the system. Note that we have assume the planck constant to be 1.
From (1), a change in wave \\[ d\ket{\psi}\\] after a \\[ dt\\] is:

\\[
d \ket{\psi(t)} = -i \mathbf{H} dt \ket{\psi(t)}
\\]

Therefore, the wave evolution after a small \\[ dt\\] is:

$$

\begin{aligned}
\ket{\psi(t)} + d \ket{\psi(t)} &= \ket{\psi(t)} -i \mathbf{H} dt \ket{\psi(t)}\\
\ket{\psi(t+dt)} &= (\mathbf{I}-i \mathbf{H(t)}dt) \ket{\psi(t)}
\end{aligned}

$$

We can note that, the operator \\[ U(t+dt,t) \equiv \mathbf{I} - i \mathbf{H(t)} dt\\] is unitary. and \\[ \mathbf{U U^{\dagger}}=1\\]
up to linear order \\[ dt\\].

If \\[  \mathbf{H}\\] is time independent, the solution to the schrodinger equation is

\\[
\mathbf{U(t',t)} = e^{-i(t'-t) \mathbf{H}}
\\]


## Axiom 5. Composite Systems. {#axiom-5-dot-composite-systems-dot}

If the Hilbert space of system \\[ A\\] is \\[ H\_A\\] and the Hilbert space of the system \\[ B\\] is \\[ H\_B\\], then
the composite system \\[ AB\\] is the tensor product \\[ H\_A \otimes H\_B\\]. If the system A is prepared
in \\[ \ket{\psi}\_A\\] and the syste, B is prepared in the state \\[ \ket{\phi}\_B\\], then the composite system state is \\[ \ket{\psi}\_A \otimes \ket{\phi}\_B\\]

Let \\[ \ket{i\_A}\\] forms an orthonormal basis for \\[ \mathbb{H\_A}\\] and
\\[ \ket{\mu\_B}\\] firns an orthonormal basis for \\[ \mathbb{H\_B}\\],
the new basis is in \\[ \mathbb{H\_A \otimes H\_B}\\] denoted as \\[\ket{i,\mu}\_{AB}\\].

Some good properties:
$$

\begin{aligned}
	\braket{i,\mu|j,\nu} &= \delta\_{ij} \delta\_{\mu \nu} \\
\mathbf{M\_A} \otimes \mathbf{N\_B} \ket{i,\mu} &= \mathbf{M\_A} \ket{i}\_A
\otimes \mathbf{N\_B} \ket{\mu}\_B =
\sum\_{j,\nu} \ket{j,\nu} (M\_A)\_{ji} (N\_B)\_{\nu \mu}
\end{aligned}

$$
