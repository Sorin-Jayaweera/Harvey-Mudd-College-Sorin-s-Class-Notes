$H_{2}^{+}:$ 2 protons, 1 electron. These two protons share the electron, and have coulomb potential between them.
![[Pasted image 20250214100551.png]]
We can model this with Dirac delta functions. We will find today that the double Dirac is more stable for the electron than if it were just bonded to one proton.

Recall:

Dirac Delta function is defined as
$$
\begin{align}
\delta(x-x_{0})=\begin{cases}
0 & x\neq x_{0} \\
\infty & x=x_{0}
\end{cases}
\end{align}
$$
Such that
$$
\begin{align}
\int_{x_{0}-\epsilon}^{x_{0}+\epsilon} f(x)\delta(x-x_{0})dx = f(x_{0}) 
\end{align}
$$

We can have a brief aside about the position operator:
We know that we should have
$$
\begin{align}
x_{op}  \psi_{\text{ position }} = x_{0}\psi_{\text{ position }}
\end{align}
$$
But $x$ could be any value, so how can we get it to a constant?
We can say $\psi_{\text{ positoin }}=\delta(x-x_{0})$ so that it would just pull out this $x_{0}$. 

It is impossible for a particle to be in this eigenstate unless we have an $\infty$ momentum uncertainty. Any position we could actually measure we will have some $dx$, so we can't ever collapse something into an actual delta function. When we measure, we initialize particles in a really narrow gaussian.
## Modeling a Sticky Point

What if we have a single point in space that is very sticky? We can model the potential energy for this point with a delta function. 

$$
\begin{align}
V(x) = \begin{cases}
0, & x\neq x_{0} \\
-V_{0}, & x=x_{0}
\end{cases}
\end{align}
$$
We can write out the Time Independent Schrödinger equation
$$
\begin{align}
-\frac{\hbar^{2}}{2m}\psi''+V(x)\psi=E\psi \\
\psi''= -\frac{2m}{\hbar^{2}}\left( E-V(x) \right)\\ 
\end{align}
$$
We also know that we have boundary conditions: $\psi$ has to be continuous everywhere, and $\psi'$ has to be continuous everywhere except where there is an infinite barrier (where the potential diverges). We should formalize this concept.

$$
\begin{align}
\int_{x_{0}-\epsilon}^{x+\epsilon} \psi''dx= -\frac{2m}{\hbar^{2}}\int_{x_{0}-\epsilon}^{x_{0}+\epsilon} (E-V(x))\psi dx
\end{align}
$$
At the discontinuity of the slope, we have
$$
\begin{align}
\lim_{ \epsilon \to 0 } \psi'(x_{0}+\epsilon)-\psi'(x_{0}-\epsilon)=  \\
-\frac{2m}{\hbar^{2}}(E-V(x_{0}))\psi(x_{0})\underbrace{ \int_{x_{0}-\epsilon}^{x_{0}+\epsilon}dx }_{ 2\epsilon }  \\
\end{align}
$$

We evaluate this for $\psi'(x_{0}^{+})-\psi'(x_{0}^{-})=0$

While the second derivative at that point is discontinuous at $x_{0}$, $\psi \text{ and } \psi'$ are still unchanged. We have to pull this value down to $-\infty$ to have an effect, a finite value won't cut it. 





## Single Delta function potential well
$$
\begin{align}
V(x)=-\frac{\hbar^{2}\alpha}{2ma}\delta(x) 
\end{align}
$$
Let's have $\alpha$ be a dimensionless number that represents the strength of $V(x)$, and $a$ is the length.


What should our potential look like here? We'll have some decay constants, and a slope. Lets make an initial guess:
![[Pasted image 20250214103308.png|300]]
For all positions $x\neq x_{0},$
$$
\begin{align}
\psi''=\underbrace{ \frac{2m}{\hbar^{2}} }_{ \kappa^{2} }(-E)\psi \, \, \, \, \, \, \, \, \, \, \, \, \, & (V = 0)
\end{align}
$$
We can write out our typical psi and get rid of values that wouldn't be bounded. $Y$ is continuous at $x=0\implies A=B$, so we can jump straight to
$$
\begin{align}
\psi(x) = \begin{cases}
Ae^{\kappa x},  & x<0 \\
Ae^{-\kappa x}, x>0
\end{cases} \\

\end{align}
$$

We can write out the Schrödinger equation with our energy function
$$
\begin{align}
\psi''(x)=-\frac{2m}{\hbar^{2}}\left( E+\frac{\hbar^{2}\alpha}{2ma}\delta(x) \right) \psi
\end{align}
$$
We can look on both sides to show the discontinuity of the slope:
$$
\begin{align}
\psi'(\epsilon)-\psi'(-\epsilon)=\int_{-\epsilon}^{\epsilon}-\frac{2m}{\hbar^{2}}\left( E+ \frac{\hbar \alpha}{2ma}\delta(x) \right)\psi dx  
\end{align}
$$

We have
$$
\begin{align}
\lim_{ \epsilon \to 0 } \psi'(\epsilon)-\psi'(-\epsilon) & = \\
 & =-\frac{2mE}{\hbar^{2}}\int_{-\epsilon}^{\epsilon}\psi dx - \frac{\alpha}{a}\int_{-\epsilon}^{\epsilon} \delta(x)\psi dx \\
 & = - \frac{\alpha}{a} \psi(0) 
\end{align}
$$
We can write out 
$$
\begin{align}
\psi'(0^{+})-\psi'(0^{-})=-\frac{\alpha}{a}\psi(0) \\
-\kappa Ae^{-\kappa(0)}-\kappa Ae^{\kappa(0)}= \frac{-\alpha}{a}A \\
\kappa= \frac{\alpha}{2a}
\end{align}
$$
We already had a definition of $\kappa$ before, so we get
$$
\begin{align}
\frac{\alpha^{2}}{4a^{2}} = \frac{2m}{\hbar^{2}}(-E)\psi
\end{align}
$$
This gets us 
$$
\begin{align}
E=-\frac{\hbar^{2}}{2m} \frac{\alpha^{2}}{4a^{2}} = -\frac{\hbar^{2}\alpha^{2}}{8ma^{2}}=E
\end{align}
$$
There is only one energy that is possible, there are no excited states. There is only the ground state. 
## Double delta functions

![[Pasted image 20250214105211.png|400]]
![[Pasted image 20250214105237.png|400]]
![[Pasted image 20250214105251.png|400]]
![[Pasted image 20250214105305.png|400]]

