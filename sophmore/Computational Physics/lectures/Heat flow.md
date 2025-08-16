
Lets take the heat flow equation
$$
\begin{align}
c\rho u_{t} - k u_{xx} = g(x,t) 
\end{align}
$$

Lets imagine a brief impulse of input temperature, then see the time evolution.
$$
\begin{align}
c\rho u_{t} - k u_{xx} = \delta(x-x_{0})\delta(t-t_{0}) \\
c\rho G_{t} (x,t,x_{0},t_{0}) - k G_{xx}(x,t,x_{0},t_{0}) =  \delta(x-x_{0})\delta(t-t_{0}) \\
\end{align}
$$
Lets take the Fourier transform to find a representation of our function over time:
$$
\begin{align}
\int_{-\infty}^{\infty} e^{ikx}dx \int_{-\infty}^{\infty} e^{i\omega t}dt \left\{ c\rho G_{t} - k G_{x x} = \underbrace{ \delta(x-x_{0})\delta(t-t_{0}) }_{ e^{ikx_{0}-i\omega t_{0}} } \right\}
\end{align}
$$

Lets consider the left side first. Integrating by parts:
$$
\begin{align}
c\rho \int_{-\infty}^{\infty} e^{-i\omega t} \frac{ \partial G }{ \partial t } dt \\ 
= c\rho \left\{ e^{-i\omega t}G \bigg|_{-\infty}^{\infty} - \int_{-\infty}^{\infty} (-i\omega)e^{-i\omega t}G dt \right\} \\
\text{ assume } G\to  0 \text{ as  } \left| t \right| \to  \infty \\
c\rho i\omega \tilde{G}
\end{align}
$$
We can now write out the left part of our Fourier as

$$
\begin{align}
c\rho(i\omega) \tilde{G}(k,\omega,x_{0},t_{0}) - \kappa(ik)^{2} \tilde{g}(k,\omega,x_{0},t_{0}) = e^{ikx_{0}+i\omega t_{0}}
\end{align}
$$

$$
\begin{align}
\tilde{G}(k, \omega,x_{0},t_{0}) = \frac{e^{i(kx_{0} + \omega t_{0})}}{\kappa k^{2}- i\omega c\rho}
\end{align}
$$
Now, to find $G(x,t)$:
$$
\begin{align}
G(x,t,x_{0},t_{0}) = \frac{1}{2\pi} \int_{-\infty}^{\infty} d\omega e^{-i\omega t} \frac{1}{2\pi} \int_{-\infty}^{\infty} d \kappa e^{-ika x} \frac{e^{i(\kappa x_{0} + \omega t_{0})}}{\kappa k^{2}-i\omega c\rho}
\end{align}
$$
Lets to the time part first. We can factor out the constants $-ic\rho$ from the right side as well as $e^{ika x_{0}}$. 
$$
\begin{align}
\frac{1}{2\pi} \int_{-\infty}^{\infty} dk e^{ik(x_{0}-x)} \frac{i}{2\pi \rho c} \int_{-\infty}^{\infty} \frac{d\omega e^{i\omega(t_{0}-t)}}{\omega + \frac{ika k^{2}}{c\rho}}
\end{align}
$$


We can evaluate this with the residue theorem. 

![[Pasted image 20250429101553.png]]

$$
\begin{align}
\int_{-\infty}^{\infty} \frac{e^{-i\omega(t-t_{0})}}{\omega + i \frac{\kappa k^{2}}{c\rho} } \\
\omega = - \frac{i \kappa k^{2}}{c\rho} \\
= -2\pi i e^{-i(-i \kappa \frac{k^{2}}{c\rho})(t-t_{0})}
\end{align}
$$
We can now go back and write
$$
\begin{align}
G(x,t,x_{0},t_{0}) = \frac{1}{2\pi} \int_{-\infty}^{\infty} e^{ik(x-x_{0})} \frac{i}{2\pi \rho c}(-2\pi i)e^{- \frac{\kappa k^{2}}{c\rho}(t-t_{0})}d \kappa \, \,( t>t_{0})  \\
= \frac{1}{2\pi \rho c}\int_{-\infty}^{\infty} e^{-\frac{\kappa k^{2}}{\rho c}(t-t_{0})+ik(x_{0}-x) }d \kappa
\end{align}
$$
We can solve this like a gaussian:
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-\alpha x^{2}-bx-\gamma} = \sqrt[]{ \frac{\pi}{\alpha} } e^{ \frac{\beta^{2}}{4\alpha}-\gamma}
\end{align}
$$
Visually, we can say that
$$
\begin{align}
\alpha= \frac{k}{\rho c}(t-t_{0}) \\
\beta= i(x-x_{0}) \\
G(x,t,x_{0},t_{0}) = \frac{1}{2\pi \rho c} \sqrt[]{ \frac{\pi \rho c}{\kappa(t-t_{0})} } \exp\left( \frac{-(x-x_{0})^{2}\rho c}{4\kappa (t-t_{0})} \right)
\end{align}
$$
Lets call $D=\frac{\kappa}{\rho c}$
We simplify this to be
$$
\begin{align}
G(x,t,x_{0},t_{0}) =\begin{cases}
 \frac{1}{4\pi \rho c \kappa (t-t_{0})}  \exp \left[ \frac{-(x-x_{0})^{2}}{4D(t-t_{0})} \right]  &  t > t_{0} \\
0  & t<t_{0} \\
\end{cases}
\end{align}
$$

This just describes a gaussian that spreads out over time, more and more slowly. 
