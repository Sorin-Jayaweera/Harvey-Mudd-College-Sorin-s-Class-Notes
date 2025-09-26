
## Review: The Schrödinger Equation
V(x) means potential energy, not potential.
![[Pasted image 20250124100835.png]]


## Interpretation of the wave function

Each atom is described by the wave function $\Psi$ which is continuous over all of space. Each helium atom hits the screen at 1 place at 1 time, but is described by a non local function?
### Recall 
For photons we found the probability amplitude Z, a complex number. The chance of measuring a photon was $ZZ^{*}$.

>[!abstract]+ Definition: The Born Rule
>Similarly, for matter we have $\Psi(x,t)$: a complex function that takes
>in real numbers and outputs a complex number. 
>The dimensions are $\frac{1}{L^{1/2}}$. 
>$dP= \Psi \Psi^{*}$ is the infitesimal probability that a particle
>described by $\Psi (x,t)$ is found between x and x+dx at time t. 
>$P(a\leq x \leq b,t)=\int_{a}^{b}\Psi^{*} (x,t)\Psi (x,t)dx$


We can think of $\Psi (x,t)\Psi^{*} (x,t)$ as the probability density, i.e. probability of finding something per unit length. 

The normalization of $\Psi (x,t)$ is
$$
\begin{align}
\int_{-\infty}^{\infty} \Psi^{*} (x,t)\Psi (x,t) dx=1 
\end{align}
$$ 
How do we really normalize?
I.e., let's take 
$$
\begin{align}
\Psi (x)=\Psi (x,t=0) = \left\{ Nx(l-x),0\leq x \leq l , 0 \text{ otherwise }\right\}   \\
\end{align}
$$
Lets plug in:
$$
\begin{align}
\int_{0}^{L} \mid N\mid ^{2} (L^{2}x^{2}-2x^{3}L+x^{4})dx = 1 \\
\mid N\mid^{2} L^{5 }\left(\underbrace{  \frac{1}{3}-\frac{2}{4}+\frac{1}{5} }_{ \frac{1}{30} } \right)U=1 \\
\end{align}
$$
$\mid N\mid^{2}=\frac{30}{L^{5}}\implies N=\sqrt{ \frac{30}{L^{5}} }e^{i\phi}$


The probability of finding a particle in a certain region is described by the wave function, and it extends widely through space. Upon observation, the wave function collapses to be sharply peaked - there could be a non zero probability far away enough that light could not travel from there to the place the function localized to!

## The probability current
Matter and energy are conserved, so at all time we should have
$$
\begin{align}
1=\int_{-\infty}^{\infty} \left| \Psi (x,t)  \right| ^{2}dx \\
0=\frac{d}{dt} \left[ \int_{-\infty}^{\infty} \left| \Psi (x,t)  \right| ^{2}dx \right] 
\end{align}
$$
Does the Schrödinger equation stay normalized for all future times t?
We have to look at $\frac{d}{dt}\left| \Psi (x,t) \right|^{2}=\frac{d}{dt}\left( \Psi^{*} (x,t)\Psi^{} (x,t) \right)=\Psi^{*}\frac{ \partial \Psi^{} (x,t) }{ \partial t }+\frac{ \partial \Psi^{*} (x,t) }{ \partial t }\Psi^{} (x,t)$

We can write out the Schrödinger equation for both $\Psi^{} (x,t)\text{ and } \Psi^{*} (x,t)$, multiply each equation by the opposite function, and add the two equations as above.

We get
$$
\begin{align}
\frac{ \partial  }{ \partial t } \left| \Psi^{} (x,t)  \right| ^{2}=-\frac{ \partial  }{ \partial x } \underbrace{ \left[ \frac{\hbar}{2mi}\left( \Psi^{*}\frac{ \partial \Psi  }{ \partial x } -\Psi \frac{ \partial \Psi^{*}}{ \partial x }   \right)  \right]  }_{ j_{x} }
\end{align}
$$
This $j_{x}$ is the Probability Current.
We get 
$$
\begin{align}
\frac{d}{dt} \left|\underbrace{  \Psi }_{ \text{ prob per unit length } } \right| ^{2}=-\frac{d}{dx} \underbrace{ j_{x} }_{ \text{ prob per time } }
\end{align}
$$
$-\frac{d}{dt}P=-\vec{\nabla}\cdot \vec{j}$
$j_{x}=\text{ the rate of probability flow in the +x direction }$
