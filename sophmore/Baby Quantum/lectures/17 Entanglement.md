Involved in everything cool, quantum computing, quantum cryptography, quantum gravity, and the foundations of quantum mechanics.

We will talk about the state of more than 1 particles.

## Two particle states
we have particle $A: x_{a}$ and $B: x_{b}$, given by $\Psi(x_{a},x_{b},t)$
We have $dP(x_{a},x_{b})=\left| \Psi(x_{a},x_{b},t) \right|^{2}dx_{a}dx_{b}$
The overall wavefunction has dimensions $\frac{1}{\text{ length }}$, whereas before it had to have dimensions $\frac{1}{\text{ length }^{1/2}}$

## Unentangled states
(I'm going to now write the $t$ for all wavefunctions from here on out, but they all have).
$$
\begin{align}
\Psi (x_{a},x_{b})=\underbrace{ f(x_{a})g(x_{b}) }_{ \text{ product of single particle states } }
\end{align}
$$
We have a wavefunction that is the probability density function for $a$ and one for $b$, and they interact by multiplying. Changing $x_{b}$ only affects $g$, aka the multiplicative factor (or scale) of $f$.

For example: 
$A$ in $\psi_{1}$ of an infinite square well, length $L$
$B$ is $\psi_{4}$ of the well.
$$
\begin{align}
\Psi (x_{a},x_{b})=\sqrt{ \frac{2}{L}}\sin\left( \frac{\pi x_{a}}{L} \right)\sqrt{ \frac{2}{L} }\sin\left( \frac{4\pi x_{b}}{L} \right)
\end{align}
$$
We think of this as the probability that $A$ is in $\psi_{1}$ AND that $B$ is in $\psi_{4}$

## Entangled states
However, if we aren't able to separate out the function as an independent product of $x_{a}\text{ and } x_{b}$, then we are entangled.
For example: 
$$
\begin{align}
\Psi (x_{a},x_{b}) & = \alpha(x_{a}-x_{b}) \\
\left| \Psi (x_{a},x_{b}) \right|^{2}  & = \left| \alpha \right| ^{2}(x_{a}^{2}-2x_{a}x_{b}+x_{b}^{2})
\end{align}
$$

Consider a particle of mass $m$ in the 5th excited state of an infinite square well,
$$
\begin{align}
E_{5}= \frac{25\pi^{2}\hbar^{2}}{2mL^{2}}
\end{align}
$$
It can decay into two particles, $A\text{ and } B$ with $m_{a}=\frac{m}{5}\text{ and } m_{b}=\frac{4m}{5}$
We have energy conservation
![[Pasted image 20250228102310.png|300]]
The particles are in a superposition of the two states with some probability (we are saying 50% chance of each but it could be anything)
![[Pasted image 20250228102334.png|300]]


Now things are going to get weird. Instead of thinking of these in the same well, they're in different wells. We can move those wells apart. We can measure the state of $A$, and instantaneously collapse $B$ down to a wave function, even if its nowhere nearby. 

This is weird. What if the particles have a definite energy and state when the particle decays, and quantum mechanics is just encoding our ignorance of the world? This nonlocality is just so weird and wrong.

Lets imagine we have two particles that are fully entangled with position and momentum: $\left[ x_{op},p_{op} \right]=i\hbar$. 
If $x_{a} =x_{0}, \text{ then } x_{b}=-x_{0}$.
If $p_{x_{a}}=p_{0}, p_{x_{b}}=-p_{0}$

The wavefunctions are built off of delta functions.
$$
\begin{align}
\Psi (x_{a},x_{b})= \delta(x_{a}-x_{0})\delta(x_{b}+x_{0})
\end{align}
$$
We can write the entangled position state 
$$
\begin{align}
\Psi (x_{a},x_{b})= \int_{-\infty}^{\infty}  C(x_{0}) \delta(x_{a}-x_{0})\delta(x_{b}+x_{0}) dx_{0}
\end{align}
$$
We can also write out the momentum measurement
![[Pasted image 20250228104253.png|500]]
![[Pasted image 20250228104328.png|500]]

So both are definitely defined, but but just have uncertainty in our ability to measure (was the thought).

But we can test this:
We can have linearly polarized light going through 3 polarizers. 

We need an operator that doesn't commute - which is true about polarization measurements (we can have vertically polarized light be blocked by 1 sheet, but if we have a 45 degree one before than light can pass. The order of the sheets matters).

It is possible to initialize photons in a superposition of states. 