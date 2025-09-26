Review
in a general potential well, the nth excited state has n nodes
there are inflection points at $E=V(x)$

$E>v(x)$ is wiggly, The bigger $E-V(x)$, the lower the wavelength and lower the amplitude.

$E<V(x)$ decays. The greater the difference, the shorter the decay length.


## Classic Harmonic Oscillator
"Everything looks like a simple harmonic oscillator"
- literally every physicist, ever

At equilibrium, $F_{x}=-\frac{dV}{dx}=0$
![[Pasted image 20250212101144.png|300]]

![[Pasted image 20250212101158.png|300]]

![[Pasted image 20250212101231.png|300]]


$\left< X \right>=$ 0 by symmetry of $V(X)$
$\left< P \right> =0$ (stationary state)
$$
\begin{align}
\left< p^{2} \right> =\Delta p^{2} \\
\left< x^{2} \right> = \Delta x^{2} \\
\Delta x\Delta p \geq \hbar_{2} \text{ At a minimum }, \Delta p=\frac{\hbar}{2\Delta x} \\
\left< E \right> _{\text{ min uncertainty }} = \frac{\hbar^{2}}{8m\Delta x^{2}}+\frac{1}{2}m\omega_{0}^{2}\Delta x^{2} 
\end{align}
$$

Lets try to find the minimum possible energy by finding where $\frac{d \left< E \right>}{dx}=0$
$$
\begin{align}
0=-\frac{\hbar^{2}}{4m\Delta x_{*}^{3}}+m\omega_{0}^{2}\Delta x_{*} \\
\Delta x_{*} = \left( \frac{\hbar^{2}}{4m^{2}\omega_{0}^{2}} \right) 
\end{align}
$$
This tells us the absolutely smallest energy that we could get, if we have our uncertainty in x and p at $\frac{\hbar}{2}$.
We can find $\left< E \right>_{\Delta x_{*}}=\hbar \frac{\omega}{2}$

## Ground state

$\psi_{0}(x)=A_{0}e^{ \frac{-m\omega}{2\hbar}x^{2}}$
We plug in and find $E_{0}=\frac{\hbar \omega}{2}$

Lets normalize $A_{0}$
$$
\begin{align}
1-\int_{-\infty}^{\infty} \lvert \psi_{0} \rvert ^{2}dx \\
= A_{0}^{2} \int_{-\infty}^{\infty} e^{\frac{-m\omega}{\hbar}x^{2}}dx \\
\text{ let } \xi \equiv \int_{-\infty}^{\infty} e^{\frac{-m \omega_{0}}{\hbar}x^{2}}dx \\
\left| A_{0} \right| ^{2}=\frac{1}{\xi} 
\end{align}
$$
We find $\xi$ by doing
$$
\begin{align}
\xi^{2} = \int_{-\infty}^{\infty} e^{\frac{-m\omega_{0}}{\hbar}x^{2}}dx \int_{-\infty}^{\infty} e^{-\frac{m\omega_{0}}{\hbar}y^{2}}dy \\
= \iint_{-\infty}^{\infty} e^{-(\frac{m\omega}{\hbar}(x^{2}+y^{2}))}dxdy
\end{align}
$$
We can change this into polar coordinates
$$
\begin{align}
\xi^{2}=\iint e^{-\left( \frac{m\omega_{0}}{\hbar} \right)r^{2}}rdrd\phi \\
\text{ we can take } \\
\frac{d}{dr}\left( e^{\frac{-m\omega_{0}}{\hbar}r^{2}} \right)  \\
d(e^{\frac{-m\omega_{0}}{\hbar}r^{2}})= -\frac{m\omega_{0}}{\hbar}2\mathrm{Re}^{-(\frac{m\omega_{0}}{\hbar)r^{2}}dr} \\
\text{ mathematicians avert your eyes } 
\end{align}
$$
We can simplify $\xi$ to 
$$
\begin{align}
\xi^{2}=-\frac{\hbar}{2m\omega_{0}}e^{\frac{-m\omega_{0}}{\hbar}r^{2}}\bigg|_{0}^{\infty} 2\pi \\
\xi=\sqrt{ \frac{\pi \hbar}{m\omega_{0}} } 
\end{align}
$$
This gives us our normalization factor
$A_{0}=\left( \frac{m\omega_{0}}{\pi \hbar} \right)^{\frac{1}{4}}$

![[Pasted image 20250212103745.png|300]]
Note that we index from 0 not from 1 as we do in particle in a box.
![[Pasted image 20250212104110.png|300]]

ENERGY EIGENSTATES DO NOT GIVE US TIME VARYING POSITION, THEY ARE STATIONARY STATES.


### fun side notes

we can solve differential equations using power series equations.
Lets call
$$
\begin{align}
y\equiv \sqrt{ \frac{m\omega_{0}}{\hbar } }x
\end{align}
$$
We can make a guess that
$$
\begin{align}
\psi(y)=\sum_{m=0}^{\infty} c_{m}y^{m}
\end{align}
$$
This is a power series, an infinite sum. 
We guess that solution and plug it into the time independent Schrödinger equation.

We can rearrange it, and get
$$
\begin{align}
\frac{ \partial^{2} }{ \partial y^{2} } H - 2y \frac{ \partial  }{ \partial y } H + \left( \frac{2E}{\hbar \omega_{0}}-1 \right) H(y)=0
\end{align}
$$
We can relate the $m+1$th coefficient to the $mth$. 

We already know how it is supposed to look asymptotically. We know that it has to look like 
$$
\begin{align}
\psi(y)=H(y)e^{\frac{-y^{2}}{2}}
\end{align}
$$
We can factor out the asymptotic behavior. We still have to find the recursion relation.

$$
\begin{align}
\sum_{l=0}^{\infty} \left[ (l+2)(l+1)-2la_{l}+\left( \frac{2E}{\hbar \omega}-1 \right) a_{l} \right] y^{l}=0
\end{align}
$$
Each term has to vanish individually, so all coefficients must satisfy
$$
\begin{align}
\frac{a_{l+2}}{a_{l}} = \frac{2l+1-\frac{2E}{\hbar}\omega_{0}}{(l+2)(l+1)}
\end{align}
$$
This is shrinking barely fast enough to converge to $e^{y^{2}}$. With our asymptotic behavior, we have $e^{-y^{2}}$. We know that this would not be normalizable, so the series must stop at some point. That means the ratio must go to zero. We can do that by making the top zero.

$$
\begin{align}
2n+1-\frac{2E}{\hbar \omega_{0}}=0 \to   E = \left( n+\frac{1}{2} \right)\hbar \omega_{0}
\end{align}
$$
This gives us energy quantization. We chop off the polynomial, and this gets us the Hermet that we have for the SHO that we saw before!