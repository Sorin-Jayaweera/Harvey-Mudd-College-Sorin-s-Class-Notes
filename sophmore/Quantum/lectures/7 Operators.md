
Recall:

Energy expectation value.
We have to calculate $c_{n}'s$. 
$$
\begin{align}
c_{n}=\int_{-\infty}^{\infty} \psi^{*} _{n}\Psi(x,0)dx
\end{align}
$$
Where the expectation value for energy is given by
$$
\begin{align}
\left< E \right> = \sum_{n}^{}\left| c_{n} \right| ^{2}E_{n} 
\end{align}
$$
For other expectation values,
$$
\begin{align}
\left< x^{\alpha} \right> = \int_{-\infty}^{\infty} \Psi^{*} x^{\alpha}\Psi\\
\left< P_{x} \right> =\int_{-\infty}^{\infty} \Psi^{*} \frac{\hbar}{i}\frac{d}{dx} \Psi dx
\end{align}
$$


Continuing on to the lecture
We have these things called "operators". We can compute the expectation values by doing this integral with the operator corresponding to that value.

The momentum operator $P_{op}=\left( \frac{i}{\hbar}\frac{ \partial  }{ \partial x } \right)$
This means that $\left< P_{x} \right> = \int_{-\infty}^{\infty}\Psi^{*}p_{op}\Psi dx$

Instead of feeding numbers into functions to spit out a number, we can spit in a vector to a function to spit out a vector, etc. We have operators from linear algebra in rotation matrices, transforms, everywhere.

## Energy Operator
Other operators we've seen are 
$x_{op}=x$
$P_{op}=\frac{\hbar}{i}\frac{d}{dx}$
$P_{op}^{2}=-\hbar ^{2}\frac{d ^{2}}{dx^{2}}$

We can write down energy as 
$E=\frac{p^{2}}{2m}+V(x)$.
We turn everything that we can into an operator. 
$H_{op}=\frac{P_{op}^{2}}{2m}+V(x_{op})$
We can plug in, 
$H_{op}=-\frac{\hbar^{2}}{2m}\frac{ \partial^{2} }{ \partial x^{2} }+V(x)$. This is the Hamiltonian operator. We can use this operator to simplify the time independent Schrödinger equation down to the...

## Energy Eigenvalue Equation
First, conceptually.
Linear Algebra. We draw the $XY$ plane. We take the equation $A\mathbf{ X}=\lambda \mathbf{X}$.
This Operator $A$ would take $\mathbf{X}$ and stretch it along a line. $A$ is the operator, $\lambda$ is the eigenvalue, and $\mathbf{X}$ is the eigenvector.

With quantum mechanics, let's make a coordinate basis of $\psi_{1} \text{ and } \psi_{2}$ (orthogonal). These two $\psi's$ are the basis for the Hamiltonian operator. This gets us the energy eigenvalue equation. We take an input vector $\psi_{1}$ and apply $H_{op}$. If that vector is only scaled, not rotated, we have
$H_{op}\psi_{1}=E_{1}\psi_{1}$.
$E_{1}$ is the energy eigenvalue, $\psi_{1}$ is the eigen vector.

Lets write this out
$$
\begin{align}
\left[ -\frac{\hbar^{2}}{2m}\frac{ \partial^{2} }{ \partial x^{2} } +V(x) \right] \psi_{n}=E_{n}\psi_{n}
\end{align}
$$
This is the time independent Schrödinger equation!

Note, we are using a linear algebra abstraction where $\psi_{1}\text{ and } \psi_{2}$ are any functions of x. 

We'll also have $Z_{op}$ that tells us about its angular momentum, etc. Any value that we could measure has an associated operator. These are all Hermitian operators, so $H=H^{\dagger}$, which grantees that they have real eigenvalues. 

The possible outcomes of measurements are the eigenvalues of that operator. There can be a continuum of eigenvalues, as in the case for position and momentum.

For example: 
Let 
$$
\begin{align}
\Psi(x,0)=\begin{cases}
\sqrt{ \frac{30}{L^{5}} }x(L-x) & 0\leq x\leq L \\
0 & \text{else }
\end{cases}
\end{align}
$$
This is in a box, so we have
$$
\begin{align}
V(x)=\begin{cases}
0 & 0\leq x\leq L \\
\infty & \text{ else }
\end{cases}
\end{align}
$$
the eigenfunctions are sin waves that end at 0 at each boundary. This $\psi$ looks like the first, sin1. 

$\left< E \right> \approx E_{1}$ but bigger.
We can find with
$$
\begin{align}
\left< E \right> =\int_{-\infty}^{\infty} \Psi^{*}H_{op}  \Psi dx
  \\
= \int_{0}^{\infty} \left[ -\frac{\hbar^{2}}{2m}\frac{ \partial^{2} }{ \partial x^{2} }  \right] \sqrt{ \frac{30}{L^{5}} }x(l-x)dx \\
\dots \\
\left< E \right> = \frac{5\hbar^{2}}{mL^{2}}
\end{align}
$$
We compare this with $E_{1}$.
$E_{n}=\frac{n^{2}\pi^{2}\hbar^{2}}{2mL^{2}}$.

## Momentum Eigenfunctions
$p_{op}=\frac{\hbar}{i}\frac{ \partial  }{ \partial x }$
$p_{op}\psi_{k}(x)=\hbar k\psi_{k}(x)$
The momentum eigenvalue is $\hbar k$.
(this $K$ is the wavenumber $\frac{2\pi}{\lambda}$)
$\psi_{k}(x)$ is the $kth$ momentum eigenfunction.
We know already that $p_{x,op}=\frac{\hbar}{i}\frac{d}{dx}\psi_{k}=\hbar k\psi_{k}$
The solution to this has the form
$\psi_{k}=e^{ikx}$.
We can really think of this as a function along a continuum.
$\psi(k)=e^{ikx}$ 

Remember wavepackets:
$\underbrace{ \Psi(x,0) }_{ \text{ wavepacket } }=\int_{-\infty}^{\infty}A(k)e^{ikx}dk$
This is a super position of momentum eigenstates. 



