
When a pair of operators does not commute, a particle cannot have definite values of both observables at the same time. This leads to an uncertainty principle. If $\left[ A_{op},B_{op} \right]=iC_{op}$, with all operators being Hermitian, then
$$
\begin{align}
\left< A_{op},B_{op}  \right>  =ic_{op} \to  \Delta A\Delta b \geq \frac{\left| \left< C \right>   \right| }{2}
\end{align}
$$
We have, for example,
$$
\begin{align}
\left[ x_{op} ,p_{xop} \right] = i\hbar, \\
\Delta x\Delta p_{x}\geq \frac{\hbar}{2} 
\end{align}
$$
We will encounter several more uncertainty principles. We have the above for 3 dimensions. We also have rules for uncertainties in orthogonal components of orbital and spin angular momentum. 

We have Energy-Time uncertainty, 
$$
\begin{align}
\Delta E\Delta t\geq \frac{\hbar}{2}
\end{align}
$$
Time is not an operator, time is a parameter that tells us how the wave function evolves. What do we mean by $\Delta t$ here?
We have
$$
\begin{align}
\Delta n^{2} -\left< n^{2} \right>  -\left< n \right>  ^{2}
\end{align}
$$
But we don't know what $\Delta t$ is at this point. 

Warning, sketchy heuristic argument ahead.
$$
\begin{align}
E=\hbar \omega \text{ applies to things with mass }
\end{align}
$$
We could imagine a signal as a function of time that is pure. A single energy corresponds to a single frequency. We've seen over again that for different eigenstates, $\frac{E}{i}=\frac{\hbar}{t}$
Suppose that we also create a wave packet where we plot vs time. Near the center, it can look just the same as the single frequency, but it decays and has different behavior elsewhere. If we only see a fraction of a second, we can't tell between these two very well.
$$
\begin{align}
\Delta x\Delta k \geq \frac{1}{2} \\
\Delta t\Delta \omega \geq \frac{1}{2} \text{ Fourier Analysis }
\end{align}
$$
If we add quantum mechanics, we get 
$$
\begin{align}
\Delta t\Delta(\hbar \omega)\geq \frac{\hbar}{2} \\
\Delta t\Delta E \geq \frac{\hbar}{2}
\end{align}
$$

What if we try to use a Special relativity approach instead of huristic?
$$
\begin{align}
p^{\mu}=\left( \frac{E}{c},p_{x},p_{y},p_{z} \right) 
\end{align}
$$
$$
\begin{align}
x^{\mu}=\left( ct,x,y,z \right) 
\end{align}
$$
Where $\mu$ is an index saying that these are 4-vectors $x^{0}=ct,x^{2}=y$, etc.

$\Delta x ~ct$
$\Delta p_{x} \frac{~E}{c}$
This gets us again
$\Delta t\Delta E\geq\frac{\hbar}{2}$

What about because Particle physics?
$z$ boson is a heavy elementary particle, mediates the weak force. 
$$
\begin{align}
E_{\text{ rest }}=M_{z}c^{2}=91GeV \\
\tau=3\times  10^{-25}s
\end{align}
$$
$\tau$ is the decay time.

$$
\begin{align}
\Delta E \geq \frac{\hbar}{2\tau}=1GeV
\end{align}
$$
This would give us an estimate of the spread in rest mass of the particle.
We can measure the mass of the $z$ boson, and measure the width of our measurements. Low and behold - we have a spread of $1GeV$! 

## Time evolution of Expectation Values
$H_{op}=\psi(x,t)=i\hbar \frac{ \partial \psi }{ \partial t }$.

$$
\begin{align}
\left< A \right>  =\int_{-\infty}^{\infty} \Psi ^{*}A_{op} \Psi dx \\
\frac{d \left< A \right>  }{dt} = \frac{d}{dt} \int_{-\infty}^{\infty} \Psi ^{*}A_{op} \Psi dx \\
\frac{d}{dt}\left< A \right>  = \int_{-\infty}^{\infty} \left\{ \frac{d}{dt} \Psi ^{*}A_{op} \Psi +\Psi ^{*}A_{op} \frac{d}{dt} \Psi  \right\} dx \\
\end{align}
$$
Recall the actual Schrödinger equation
$$
\begin{align}
H_{op} \Psi =i\hbar \frac{ \partial \Psi  }{ \partial t } 
\end{align}
$$
We can solve this with
$$
\begin{align}
\frac{ \partial \Psi  }{ \partial t } =-\frac{i}{\hbar}H_{op} \Psi  \\
\end{align}
$$
$$
\begin{align}
H_{op} ^{*} \Psi ^{*}=-i\hbar \frac{d}{dt} \Psi ^{*} \\
H_{op} \Psi ^{*}=-i\hbar \frac{d}{dt} \Psi ^{*} \\
\text{ which we can solve to get } \\
\frac{d}{dt} \Psi ^{*}=\frac{i}{\hbar}H_{op}\Psi ^{*} 
\end{align}
$$
We get
$$
\begin{align}
\frac{ d \left< A \right>  }{d t } =\frac{i}{\hbar}\int_{-\infty}^{\infty} \left( \underbrace{ H_{op} }_{ B_{op}  } \underbrace{ \Psi U }_{ \Phi } \right) ^{*}\underbrace{ A_{op} \Psi  }_{ \Theta }+\Psi ^{*}A_{op} (-H_{op} \Psi ) ~ ~ dx
\end{align}
$$


We can use the properties of hermitian operators that
$$
\begin{align}
\int_{-\infty}^{\infty} (B_{op} \Phi)^{*}\Theta dx = \int_{-\infty}^{\infty} \Phi ^{*}B_{op} \Theta dx
\end{align}
$$
We can relabel our expression and have the expression of a commutator:
$$
\begin{align}
\frac{ d \left< A \right>  }{d t }= \frac{i}{\hbar} \left[ \int_{-\infty}^{\infty} \Psi ^{*}H_{op} A_{op} \Psi dx \right] + \frac{i}{\hbar}\int_{-\infty}^{\infty} \Psi ^{*}(-A_{op} H_{op} )\Psi dx \\
= \frac{i}{\hbar }\int_{-\infty}^{\infty} \Psi ^{*} \left[ H_{op} ,A_{op}  \right] \Psi dx \\
\end{align}
$$
$$
\boxed{
\begin{align}
\frac{ d \left< A \right>  }{d t } = \frac{i}{\hbar}\left< \left[ H_{op} ,A_{op}  \right]  \right>  
\end{align}
}
$$
This is tremendous. If we have $H_{op}$ known and want to know if $A$ is 'conserved'?

If $A_{op}$ commutes with the Hamiltonian, then it is possible to find simultaneous eigenstates of both. 
We just have to check if $A_{op}$ commutes with $H_{op}$, aka
$$
\begin{align}
\left[ H_{op} ,A_{op}  \right] =0 \\  
\end{align}
$$
If so, $\frac{ d \left< A \right> }{d t }=0$
So the expectation value of $A$ doesn't change. 

This tells us stuff about the energy time uncertainty relation.

$$
\begin{align}
\left< H_{op} ,A_{op}  \right>  =iC_{op}  \implies \Delta A\Delta E\geq \frac{ \left| C \right| }{2} \\
\left< C \right>   = \left< \left[ H_{op} ,A_{op}  \right] = -\hbar \frac{ d \left< A \right>  }{d t }  \right>  
\end{align}
$$
These two together give us
$$
\begin{align}
\Delta A\Delta E\geq \frac{\hbar}{2} \frac{ d \left< A \right>  }{d t }  \\
\underbrace{ \frac{\Delta A}{\frac{ d A}{d t } } }_{ \Delta T }\Delta E\geq \frac{\hbar}{2}
\end{align}
$$
The uncertainty in quantity $A$ divided by the rate at which the quantity is changing. 
$\Delta T$ is how long it takes the wave function to change the quantity A (i.e. position) by an amount equal to that uncertainty. Aka, to change so much that we can tell that it changed. 