We have been thinking about functions of a complex variable and derived the Cauchy Riemann conditions, which tell us if a function is differentiable if the derivative continuous from every direction. We checked by taking orthogonal directions to get the limit. 

We also found the residue theorem. To integrate a function that is analytic except for some countable number of spots in the interior:
$$
\begin{align}
\oint_{c}f(z)dz = 2\pi i \sum_{}^{} \text{ residues enclosed}
\end{align}
$$

Lets consider a test problem:
$$
\begin{align}
\int_{-\infty}^{\infty} \frac{dx}{1+x^{4}}
\end{align}
$$
The poles satisfy
$$
\begin{align}
x^{4}=-1 = e^{i\pi}=e^{i\pi}e^{2n\pi i} \\
x=e^{\frac{i\pi}{4}}e^{\frac{in\pi}{2}} \\
\end{align}
$$
So we have
$$
\begin{align}
e^{\frac{i\pi}{4},}e^{\frac{3i\pi}{4}}, e^{\frac{5\pi}{4}}, e^{\frac{7\pi}{4}}
\end{align}
$$

Last time we saw that we could make a closed path and integrate the x axis from $-\infty \text{ to } \infty$, and made a semicircle that came back. The integral along this semicircle went to zero because we have $r\to \infty$, and it was in the denominator. 

In this case, the integral along the arc would have
$$
\begin{align}
z=Re^{i\phi}, dz=Rie^{i\phi}d\phi \\
\int_{\text{ arc }}^{} \frac{Rie^{i\phi}d\phi}{R^{4}e^{ri\phi}+1} = \frac{1}{R^{3}}\int_{\text{ arc }} \frac{e^{i\phi}d\phi}{e^{4i\phi}+R^{-4}}
\end{align}
$$
As $R$ go to infinity, this clearly goes to zero * some crummy small complex number (the integral bit its just some multiple of unity). 
The contribution of this semicircular path goes to zero. 

We want the straight part but we need to close, and we can use the residue theorem.

We can now evaluate:
$\oint=\int_{-\infty}^{\infty} \text{ real axis }$
We can cut away everywhere except the discontinuities, since the closed path of an analytic function is zero. So we have
$$
\begin{align}
z\to  z_{0}=e^{\frac{i\pi}{4}}
\end{align}
$$
We evaluate the integral as $z\to z_{0}$.
$$
\begin{align}
\frac{1}{z^{4}+1}
\end{align}
$$
Lets imagine that $z=z_{0}+\delta z=e^{\frac{i\pi}{4}}+\delta z$
If we stuff that in, we get the integrand look like
$$
\begin{align}
\frac{1}{(e^{\frac{i\pi}{4}}+\delta z)^{4}+1}
\end{align}
$$

We can use the binomial expansion
$$
\begin{align}
(a+b)^{4}=a^{4}+ {4\choose  1} a^{3}b+{4\choose  2}a^{2}b^{2}+\dots
\end{align}
$$


$$
\begin{align}
\frac{1}{e^{i\pi}+4\delta ze^{\frac{3i\pi}{4}}+6(\delta z)^{2}e^\frac{2i\pi}{4}+4(\delta z)^{3}e^\frac{i\pi}{4}+(\delta z)^{4}+1}
\end{align}
$$
We get
$$
\begin{align}
4e^{\frac{\pi i}{4}}(\delta z)\underbrace{ (1+\dots) }_{ O(\delta z) }
\end{align}
$$


The residue at $a$ is
$$
\begin{align}
\frac{1}{4e^{\pi \frac{i}{4}}}
\end{align}
$$
At $b$, we have
$$
\begin{align}
\frac{1}{4e^{9\pi \frac{i}{4}}}
\end{align}
$$
(note, its just $e^{3 (\text{ stuff })}$)
Anyways, we write out our integral now as
$$
\begin{align}
\oint =I=2\pi i\left[ \frac{e^{-3\pi \frac{i}{4}}}{4}+ \frac{e^{-9\pi \frac{i}{4}}}{4} \right] 
\end{align}
$$

We can simplify this down to
$$
\begin{align}
\frac{\pi i}{2}\left[ -\frac{i}{\sqrt{ 2 }}2 \right] \\
= \frac{\pi}{\sqrt{ 2 }}
\end{align}
$$



Near a first order pole at $z_{0}$
$$
\begin{align}
f(z)\approx \frac{a_{-1}}{(z-z_{0})} + a_{0} + a_{1}(z-z_{0})+ \frac{a_{2}}{2!}(z-z_{0})^{2}+\dots
\end{align}
$$
This is called a Laurent series.
So 
$$
\begin{align}
\lim_{ z\to  z_{0} } \left[ (z-z_{0}) f(z) \right]   \\
\lim_{ z \to e^{\frac{i\pi}{4}} }  \frac{(z-e^{\frac{i\pi}{4}})}{z^{4}+1}
\end{align}
$$
which we can use $l'hopital$ to get
$$
\begin{align}
\frac{1}{4z^{3}}=\frac{1}{4e^{3\pi \frac{i}{4}}}
\end{align}
$$
For a second order pole (where the leading dependence goes to zero quadratically)
$$
\begin{align}
f(z) \approx \frac{1}{2!} \frac{a_{-2}}{(z-z_{0})^{2}} + \frac{a_{-1}}{(z-z_{0})} + a_{0} + \dots
\end{align}
$$
(We're just writing out the expansion of our function).
We want to take the circles around each of these singularities, so we'll do the loop:

$$
\begin{align}
z-z_{0}=\epsilon e^{i\phi} \\
\int_{0}^{2\pi} \frac{\frac{a_{-2}}{2!}\epsilon ie^{i\phi}d\phi}{\epsilon^{2}e^{2i\phi}} \\
=\frac{a_{-2}}{2!}\epsilon^{-1}\int_{0}^{2\pi} e^{-i\phi}d\phi \\
= -\frac{1}{i}e^{i\phi}\bigg|_{0}^{2\pi}  
\end{align}
$$
We get back to the same spot we started, so this is $0$. This is true for every power of $n$ except $n=-1$, which integrates to log. It is only the terms that have $\frac{1}{z-z_{0}}$ contribute something. 
Similar to what we did in the first order pole, we can multiply by $(z-z_{0})^{2}$
$(z-z_{0})^{2}f(z)= \frac{a_{-2}}{2!}+a_{-1}(z-z_{0})+a_{0}(z-z_{0})^{2}$
We want the term $a_{-1}$, so we take a derivative with respect to $z$:

$$
\begin{align}
\lim_{ z \to z_{0} } \frac{ d }{d z } \left[ (z-z_{0})^{2}f(z) \right] = \lim_{ z \to z_{0} } a_{-1}+2a_{0}(z-z_{0})+\dots
\end{align}
$$

When were doing the integral of the first order term, however, we'll get
$$
\begin{align}
z=\epsilon e^{i\phi}, \delta z=i\epsilon e^{ i\phi }
\end{align}
$$

$$
\begin{align} \\
\int_{0}^{2\pi} \frac{1}{(z-z_{0})}dz \\
=\int_{0}^{2\pi} \frac{1}{\epsilon e^{i\phi}}\epsilon e^{i\phi}d\phi \\
= 2\pi i
\end{align}
$$
$ln(re^{i\phi})=ln(r)+i\phi$
The logarithm function changes its phase as it goes around the origin. 
