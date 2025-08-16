## Review
The wave function tells us the probability of detecting the particle in a small detector $dP(x,t)=\left| \Psi(x,t) \right|^{2}dx$

If the wave function is governed by the Schrödinger equation, the total probability is preserved. $j_{x}$ is the rate that probability is flowing in the x direction at a place x at time t.


## Uncertainty
We define an expectation value $\left< n \right> = \sum_{n=0}^{\infty}nP(n)$, and is a constant value for a sum.
$\left< f \right>=\sum_{0}^{\infty}P_{n}f(n)$
n is the number of "occurrences" of a thing,
$\Delta n$ is the standard deviation.
$\Delta n^{2}$ is the variance.



$$
\begin{align}
\Delta n^{2}=\left< (n-\left< n \right>^{2}) \right> \\
=\sum_{n=0}^{\infty}P(n)(n-\left< n \right> )^{2} \\
= \sum_{n=0}^{\infty}P(n)n^{2}-\sum_{n=0}^{\infty}P(n)2n\left< n \right> +\sum_{n=0}^{\infty}P(n)\left< n \right> ^{2} \\
= \left< n \right> ^{2}-2\left< n \right> \sum_{n=0}^{\infty}P(n)n+\left< n \right> ^{2}\sum_{n=0}^{\infty}P(n) \\
\Delta n^{2}=\left< n^{2} \right> -2\left< n \right> ^{2}+\left< n \right> ^{2} \\
\Delta n= \left< n^{2} \right> -\left< n \right> ^{2}
\end{align}
$$
This is how we will typically calculate the variance
$$
\boxed{
\begin{align}
\Delta n^{2}=\left< n^{2} \right> -\left< n \right> ^{2}
\end{align}
}
$$
this is the weighted average of the expectation value.

We can now do this for continuous variables.
$$
\begin{align}
\left< x^{\alpha} \right> =\int_{-\infty}^{\infty} x^{\alpha}dP(x)
\end{align}
$$

Now lets tie in some quantum mechanics. Let's use the borne rule to calculate $\left< x^{\alpha} \right>=\int_{-\infty}^{\infty}x^{\alpha}\left| \Psi \right|^{2}dx$

![[Pasted image 20250129102915.png|300]]


Lets do a practice problem: What is the uncertainty of
$$
\begin{align}
\Psi(x,0)=\left\{ \sqrt{ \frac{30}{L^{5}} }x(l-x) \right\} \, 0<x<L
\end{align}
$$
$\left< x \right> =\frac{L}{2}$
$\Delta x=?$

$$
\begin{align}
\Delta x^{2} & = \left< x^{2} \right> -\left< x \right> ^{2}\\
\left< x^{2} \right>  & = \int_{0}^{L}x^{2} \frac{30}{L^{5}}(L-x)^{2}dx = \frac{2}{7}L^{2} 
\end{align}
$$
$$
\begin{align}
\Delta x=\sqrt{ (x^{2}) -\left< x \right> ^{2}} \\
= \sqrt{ \frac{2}{7}L^{2}-\frac{L^{2}}{4} } \\
\Delta x=\frac{L}{2\sqrt{ 7 }}
\end{align}
$$

We can also do this for momentum:

$$
\begin{align}
\left< P_{x} \right> = \int_{-\infty}^{\infty} \frac{\Psi^{*}\hbar}{i} \frac{d\Psi}{dx}dx \\
\left< P_{x}^{2} \right> =\int_{-\infty}^{\infty} \Psi^{*}(-\hbar) \frac{d^{2}\Psi}{dx^{2}}dx
\end{align}
$$
We'll derive these in big quantum but... not yet.
$$
\begin{align}
\left( \Delta P_{x} \right) ^{2}=\left< P_{x}^{2} \right> -\left< P_{x} \right> ^{2}
\end{align}
$$

The momentum expectation value of a $\Psi$ that is real (doesn't have a 'meaningful' i in it. There is always some $e^{i\phi}$ phase factor, but if it is a constant or not really a function than its basically real)
$$
\begin{align}
\left< P_{x} \right> =\int_{-\infty}^{\infty} \frac{\Psi \hbar}{i} \frac{d\Psi}{dx}dx \\
=\frac{1}{i}\int_{-\infty}^{\infty} \hbar \Psi \frac{d\Psi}{dx} dx
\end{align}
$$
We can't have an imaginary momentum, so $\int_{-\infty}^{\infty}\hbar \Psi \frac{d\Psi}{dx}dx=0$. 
If $\Psi$ is real, than $\left< P_{x} \right>=0$. (remember, P = momentum).
This means the distribution of momentum must be symmetric about 0. 

Because of this,
$$
\begin{align}
\Delta p^{2}=\left< P^{2} \right> =\left< P \right> ^{2} \\
=\left< P^{2} \right> \sim  \frac{ \partial^{2} \Psi}{ \partial x } 
\end{align}
$$
This means that $P$ depends only on the curvature of your wave function.  Lower curvature has a smaller uncertainty in momentum. Therefore the more kinetic energy, the greater the uncertainty in $P$. 


>[!abstract]+ Theorem: Ehrenfest's Theorem
>The correspondence principle tells us that we should expect
>$\frac{d\left< X \right>}{dt} = \frac{p_{x}}{m}$
>So then the time derivative $\frac{d\left< p_{x} \right>}{dt}=-\left< \frac{ \partial V }{ \partial x } \right>$

Newton's second law still holds in quantum mechanics.

