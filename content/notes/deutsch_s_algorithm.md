+++
title = "Deutsch's Algorithm"
author = ["DESKTOP-PNLN52S"]
date = 2024-02-26T00:00:00-07:00
lastmod = 2024-02-26T00:00:00-07:00
tags = ["moc"]
draft = false
+++

**Link**:

Built as: [Query Problem]({{< relref "query_problem.md" >}})

<div class="LaTeX">

\section{Introduction}
This is LaTeX content directly within Org mode. You can write your LaTeX code here.

\begin{equation}
E = mc^2
\end{equation}

</div>

Learn about the query here:
Deustch's algorithm solves the parity problem for \\(n=1\\).

Deutsch's problem:

Input: a function \\( f:\\{0,1\\} \to \\{0,1\\} \\)

Output: 0 if f is constant, 1 if f is balanced

The quantum circuit looks like this :

...

The initial state is \\(\ket{0}\ket{1}\\), by applying two hadamard gates:

\begin{align\*}
	H \otimes H \ket{1} \ket{0} &= \ket{-} \ket{+} \\\\
&= \frac{1}{\sqrt{2}}(\ket{0} + \ket{1}) \frac{1}{2}(\ket{0} - \ket{1}) \\\\
&= \frac{1}{2}(\ket{0} - \ket{1}) \ket{0} + \frac{1}{2}(\ket{0} - \ket{1})\ket{1}
&= \ket{\psi\_1}
\end{align\*}

$ \ket{\psi\_1} \ket{\psi\_2}$

Next, we apply the \\(U\_f\\) gate:
and we can as well utilize this expression
$ \ket{0 \otimes a} - \ket{1 \otimes a} = (-1)^a (\ket{0} - \ket{1})$

\begin{align\*}
	U\_f  \ket{\psi\_1}
&= \frac{1}{2}(\ket{0 \otimes f(0)} - \ket{1 \otimes f(0)})\ket{0}
+ \frac{1}{2}(\ket{0 \otimes f(0) - \ket{1 \otimes f(1)}})\ket{1} \\\\
&= \frac{1}{2}(-1)^{f(0)}(\ket{0} - \ket{1})\ket{0}
+ \frac{1}{2}(-1)^{f(1)}(\ket{0} - \ket{1})\ket{1} \\\\
&= \ket{-} \left( \frac{(-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}}{\sqrt{2}} \right)
\end{align\*}

A phase kickback happened here: learn more at

So finally, we obtained

\begin{align\*}
	\ket{\psi\_2} &= (-1)^{f(0)}\ket{-} \left( \frac{\ket{0} + (-1)^{f(0) \otimes f(1)}\ket{1}}{\sqrt{2}} \right) \\\\
&=
   \begin{cases}
        (-1)^{f(0)} \ket{-} \ket{+} \quad \text{if} f(0) \otimes f(1) = 0\\\\
        (-1)^{f(0)} \ket{-} \ket{-} \quad \text{if} f(0) \otimes f(1) = 1
   \end{cases}
\end{align\*}

After applying the hadamard again, we obtain the final solution:

\begin{align\*}
	\ket{\psi\_3} &=
\begin{cases}
   (-1)^{f(0)} \ket{-} \ket{0} \quad \text{if} f(0) \otimes f(1) = 0\\\\
   (-1)^{f(0)} \ket{-} \ket{1} \quad \text{if} f(0) \otimes f(1) = 1
\end{cases}
\end{align\*}