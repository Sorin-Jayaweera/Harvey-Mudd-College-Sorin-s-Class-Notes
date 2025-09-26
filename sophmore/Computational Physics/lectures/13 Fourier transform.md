We have
$$
\begin{align}
\tilde{f}= \int_{-\infty}^{\infty} e^{-i\omega t}f(t)dt \\
f(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty} e^{i\omega t}\tilde{f}(\omega)d\omega
\end{align}
$$
Suppose $f(t)=A\cos\Omega t$
$$
\begin{align}
\tilde{f}(\omega)= \int_{-\infty}^{\infty} e^{i\omega t}A \frac{\left( e^{i\Omega t}+e^{-i\Omega t} \right)}{2} dt \\
= \frac{A}{2 }\int_{-\infty}^{\infty} e^{i(\Omega-\omega) t}+e^{-i(\Omega-\omega) t} dt\\
\frac{A}{2}\left[ e^{i\Omega t}-e^{-i\Omega t} \right] =\frac{1}{2\pi} \int_{-\infty}^{\infty} e^{i\omega t}\tilde{f}(\omega)d\omega \\
\text{ this works if } \\
\frac{1}{2\pi}\int_{-\infty}^{\infty} e^{i\omega t}d\omega=\delta(t)
\end{align}
$$

Therefore,
$$
\begin{align}
\frac{1}{2\pi}\tilde{f}= \frac{1}{2}\left[ \delta(\omega-\Omega)+\delta(\omega+\Omega) \right]  \\
\end{align}
$$

To show that $\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{i\omega t}d\omega=\delta(t)$, consider 
$$
\begin{align}
\int_{a}^{b} \delta(t)dt = \int_{a}^{b} dt \frac{1}{2\pi}\int_{-\infty}^{\infty} e^{i\omega t} d\omega
\end{align}
$$
We know that we need to get $1$ if $b>0,a<0$ (or $-1$ if its reversed, or 0 if 0 is not captured in the range).

We can simplify this by reversing the order of integration:
$$
\begin{align}
= \frac{1}{2\pi} \int_{-\infty}^{\infty} d\omega \int_{a}^{b} e^{i\omega t}dt \\
= \frac{1}{2\pi}\int_{-\infty}^{\infty} \frac{e^{i\omega t}}{i\omega}\bigg|_{a}^{b}   \\
= \frac{1}{2\pi i} \int_{-\infty}^{\infty} \frac{e^{i\omega b}-e^{i\omega a}}{\omega}
\end{align}
$$
Oh boy, this has a pole right at $0$, and were integrating straight through it. We want to use contour integration. We can rewrite the integral (both of the components look the same, so well make a dummy variable $c$ that can be $a$ or $b$).
$$
\begin{align}
\int_{-\infty}^{\infty} \frac{i\omega c}{\omega}d\omega
\end{align}
$$
We're only going to go halfway around the pole when we integrate, so we'll only get half of the contribution (this is the Cauchy principle value).

We can do the contour integral. Along the semicircle, 
$$
\begin{align}
e^{i\omega c}= e^{ic(R\cos\theta+Ri\sin\theta)}
\end{align}
$$
As $r\to \infty$, $\frac{e^{i\omega c}}{\omega}d\omega\to 0$.
We therefore get
$$
\begin{align}
\oint \frac{e^{i\omega c}}{\omega}d\omega=I(c) \\
I(c)=\int_{-\infty}^{-\epsilon} \frac{e^{i\omega t}}{\omega}d\omega+\int_{\pi}^{2\pi} \frac{e^{ic\epsilon e^{i\theta}}\epsilon ie^{i\theta}}{\epsilon e^{i\theta}} d\theta + \int_{\epsilon}^{\infty} \frac{e^{i\omega c}}{\omega}d\omega
\end{align}
$$

We're basically going from $-\infty$ to some small $\epsilon$ near the point at zero, doing a quick semicircle around it, then continuing on to $\infty$. On the semicircle, we are saying $\omega=\epsilon e^{i\omega},d\omega=\epsilon ie^{i\theta}d\theta$
This gross semicircle integral becomes
$$
\begin{align}
\int_{\pi}^{2\pi} i d\theta =i\pi
\end{align}
$$
$$
\begin{align}
I(c)=\begin{cases}
-i\pi & c<0 \\
i\pi & c>0
\end{cases}
\end{align}
$$
We can rewrite the earlier integral now as
$$
\begin{align}
\frac{1}{2\pi i}\left[ I(b)-I(a)\right] 
\end{align}
$$
if $b>0,a<0$ then
$$
\begin{align}
\frac{1}{2\pi i}\left[ i\pi- \, -i\pi \right] =1
\end{align}
$$
$$
\begin{align}
\int_{a}^{b} \delta(t)dt=\frac{1}{2\pi i}\left[ i\pi \text{ sign(b)- }\text{ sign }(b) \right]  \\
= \frac{1}{2} \left[ \text{ sign(b) }-\text{ sign(a) } \right] 
\end{align}
$$

Finally we can go back to our tilde functions:
$$
\begin{align}
\tilde{f}(\omega)= \int_{-\infty}^{\infty} dt \frac{e^{-i\omega t}1}{2\pi}\int_{-\infty}^{\infty} d\omega'e^{i\omega't}\tilde{f}(\omega')
\end{align}
$$
We have an omega prime because we'll have a function of t and can't use the same omega that we have earlier in the function. $\omega'$ is a dummy variable of integration. 

Anyways, this says
$$
\begin{align}
\int_{-\infty}^{\infty} d\omega'\tilde{f}(\omega') \underbrace{ \frac{1}{2\pi}\int_{-\infty}^{\infty} dt e^{i(\omega'-\omega)t} }_{ \delta(\omega'-\omega) }
\end{align}
$$

Therefore when we integrate over all frequencies possible, we get a delta function for only the frequency that we feed in. 

Lets do a fourier transform.
Suppose $f(t)=\begin{cases}1& |t|<\tau \\ 0 & |t|<\tau\end{cases}$
This is a square from $-\tau \text{ to }\tau$

$$
\begin{align}
\tilde{f}(\omega)= \int_{-\infty}^{\infty} e^{-i\omega t}f(t)dt \\
= \int_{-\tau}^{\tau} e^{-i\omega t}dt  \\
= \frac{e^{-i\omega t}}{-i\omega}\bigg|_{-\tau}^{\tau}  \\
= \frac{-e^{-i\omega \tau}+e^{i\omega \tau}}{i\omega} \\
= \frac{e^{i\omega \tau}-e^{-i\omega \tau}}{2i} \frac{2}{\omega} \\
= \frac{2\sin(\omega \tau) }{i\omega} \\
 = \frac{2\tau \sin(\omega \tau)}{\omega \tau}
\end{align}
$$
$\lim_{ x \to 0 }\frac{\sin(x)}{x}\to 1$, so we don't have a pole.

At $\omega\to 0, \text{ we get }2\tau$. Its an even function (odd function over odd function falls off the same way).
At $\omega=\frac{\pi}{\tau}$, we go to zero, and at $2\pi$ we come back, so we end up with an oscillation that has an amplitude that falls off by $\frac{1}{\omega}$.

![[Pasted image 20250304104645.png|300]]

Where does this come up in physics? If we shine light at a narrow slit, it can go through the small area. The function we just drew looks like the electric field. Our eyes see intensity which is the square of the electric field, so we would see $I \propto \left| \tilde{f}(\omega) \right|^{2}$.


Can we go backwards?
$$
\begin{align}
f(t)\stackrel{?}{=}  \frac{1}{2\pi}\int_{-\infty}^{\infty} e^{i\omega t}2\tau \frac{\sin(\omega \tau)}{\omega \tau}d\omega
\end{align}
$$

$$
\begin{align}
= \frac{\tau}{\pi}\int_{-\infty}^{\infty} \frac{e^{i\omega \tau}-e^{-i\omega \tau}}{2i} \frac{e^{i\omega t}}{\omega \tau}d\omega \\
= \frac{1}{2\pi i}\int_{-\infty}^{\infty} \frac{\left[ e^{i\omega(t+\tau)}-e^{i\omega(t-\tau)} \right]}{\omega}d\omega 
\end{align}
$$
There is only one pole at $\omega=0$. Depending on the sign of $t+\tau$, we'll either have to enclose on the upper or lower half plane.

