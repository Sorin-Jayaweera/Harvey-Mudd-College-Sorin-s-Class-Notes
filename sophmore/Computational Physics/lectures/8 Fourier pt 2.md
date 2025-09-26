
What if we want to represent a periodic function instead?

We could use a sum of periodic functions to make the true function. Instead of expanding a series with $x^{n}$s., could we use $A\sin(kx)$s?

Lets imagine we want to represent a square wave?
![[Pasted image 20250213095216.png|300]]

We want to make the period T so that it fits with this square wave.

We can make an initial guess:
$f(t)=a_{0}+\sum_{n=1}^{\infty}a_{n}\cos\left( \frac{2\pi nt}{T}  \right) +b_{n}\sin\left( \frac{2\pi nt}{T}  \right)$

This looks like a vector space - we have a linear combination of two basis. 
It would be nice if these were orthogonal, so we define an inner product that would make these two yield zero. 

If our function has a non zero average, then we know that has to come from $a_{0}$, since that is the only function with a non zero average in our guess.

We can write out:
$$
\begin{align}
\int_{0}^{T} \cos\left( \frac{2\pi nt}{T} \right)\cos\left( \frac{2\pi mt}{T} \right)dt = \begin{cases}
0 & n \neq m \\
\_\_ &n=m\neq 0  \\
T &n=m=0 
\end{cases}
\end{align}
$$
only when $m=n$ we will get something that doesn't average to zero over a full period. All the others oscillate around zero. 

We know that we can represent
$$
\begin{align}
\cos(\omega t)=\frac{e^{i\omega t}+e^{-i\omega t}}{2} \\
\sin(\omega t) = \frac{e^{i\omega t}-e^{-i\omega t}}{2i}
\end{align}
$$
Consider the following integral:
$$
\begin{align}
 & \int_{0}^{T}  e^{in\omega t}e^{-im\omega t}dt, &  \omega=\frac{2\pi}{T} \\
 & =\int_{0}^{T} e^{i(n-m)\omega t}dt\\
 & =\frac{e^{i(n-m)\omega t}}{i(n-m)\omega}\bigg|_{0}^{T}   \\
\end{align}
$$
If n = m, this explodes to infinity, so we would have to go back and integrate $\int_{0}^{T}1$. Otherwise, we have this thing. 
$$
\begin{align}
\frac{e^{i(n-m)\omega T}-1}{i(n-m)\omega} \\
= \frac{e^{i(n-m)2\pi}-1}{i(n-m)\omega}=0
\end{align}
$$

Lets use what we just developed and go back to 
$$
\begin{align}
\int_{0}^{T} \cos(n\omega t)\cos(m\omega t)dt \\
=\int_{0}^{T} \left( \frac{e^{in\omega t}+e^{-in\omega t}}{2} \right)  \left( \frac{e^{im\omega t}+e^{-im\omega t}}{2} \right) 
\end{align}
$$
We get
$$
\begin{align}
\frac{1}{4}\int_{0}^{T} \underbrace{ e^{i(n+m)\omega t} }_{ 0 }+\underbrace{ e^{-i(n+m)\omega t} }_{ 0 }+\underbrace{ e^{i(n-m)\omega t} }_{ T\delta_{nm} }+\underbrace{ e^{-i(n-m)\omega t}dt }_{ T \delta_{nm} }
\end{align}
$$
We know that were whipping around the unit circle some positive number of times, so the first two e's are 0. The next two are zero unless n=m, in which we get T.
This gets us
$$
\begin{align}
\frac{T}{2}\delta_{nm}
\end{align}
$$

So we have our basis functions that are orthogonal if we let the inner product be the integral over the period of the product of the vectors. Its zero everywhere except where $n=m$.

If we shift our frame to only look at the square wave from $-\frac{T}{2}\text{ to } \frac{T}{2}$, we see that the function looks odd.

We know that our $a_{n}\cos(n\omega t)$ has $a_{n}=0$,
$$
\begin{align}
f(t)=-f(-t), \text{ and }  \cos \text{ is even }
\end{align}
$$


![[Pasted image 20250213102437.png|300]]
If we have even n's, then we have equal contribution to the positive and negative regions, so they would integrate to 0. We can therefore only have odd integers that we can fit.

We multiply $f(t)=\dots$ by $\sin m\omega t$ and integrate from $-\frac{T}{2}\text{ to } \frac{T}{2}$
We get

$$
\begin{align}
 & \int_{-\frac{T}{2}}^{T/2} f(t)\ & sin(m\omega t)dt \\
= & \int_{-\frac{T}{2}}^{\frac{T}{2}} \left[ a_{0}+\sum_{n=1}^{\infty} a_{n}\cos n\omega t+b_{n}\sin(n\omega t) \right]  & \sin m\omega t ~ dt
\end{align}
$$
We can reduce this with what we learned (0 mean, so no $a_{0}$, no cosines, and only odd sines)
$$
\begin{align}
\int_{-\frac{T}{2}}^{\frac{T}{2}} \underbrace{ b_{n}\sin(n\omega t)\sin(m\omega t) }_{ \delta_{nm} \frac{T}{2} }dt 
\end{align}
$$
We therefore have
$$
\begin{align}
I_{nm}\equiv 2\int_{0}^{\frac{T}{2}} \sin(m\omega t)dt  \\
=2-\frac{\cos(m\omega t)}{m\omega}\bigg|_{0}^{\frac{T}{2}} \\
=-\frac{2}{m\omega}\left[ \cos\left( \frac{m\omega T}{2}\right) -1  \right]    \\
= -\frac{2}{m\omega}[\cos(m\pi)-1]
\end{align}
$$
$$
\begin{align}
=\frac{4}{m\omega}\text{ if m is odd } \\
= \frac{b_{m}T}{2}\text{ n=m }
\end{align}
$$
and we have nothing if $m$ is even.

We therefore get
$$
\begin{align}
b_{m}=\begin{cases}
\frac{2}{T} \frac{4}{m\omega}  & \text{ m odd } \\
0 & \text{ m even }
\end{cases} \\
b_{m}= \frac{4}{m\pi}~ ~\text{ m odd } \\
f(t)=\sum_{\text{ n odd }} \frac{4}{n\pi}\sin\left( \frac{2\pi nt}{T} \right) 
\end{align}
$$

