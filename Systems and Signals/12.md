## Periodic Signals
### Analysis
$$
\begin{align}
a_{k} = \frac{1}{T}\int_{T} x(t)e^{-jk\omega_{0}t}
\end{align}
$$
### Synthesis
$$
\begin{align}
x(t)=\sum_{k=-\infty}^{\infty} a_{k} e^{jk \omega_{0}t}
\end{align}
$$

## Aperiodic Signals
### Analysis
Fourier transform
$$
\begin{align}
x(j\omega) = \int_{t=-\infty}^{\infty} x(t)e^{-j\omega t}dt
\end{align}
$$
This is making the basis functions.

### Synthesis
Inverse Fourier Transform
$$
\begin{align}
x(t) = \frac{1}{2\pi} \int_{\omega=-\infty}^{\infty} x(j\omega)e^{j\omega t} d\omega
\end{align}
$$
Note that this synthesis uses all $w$, not just $k \omega_{0}$.


*Both* techniques allow us to express $x(t)$ in terms of $e^{j\omega t}$ basis functions. 

The main difference is that for periodic functions, we only consider a small set of frequencies $\omega=k\omega_{0}, \,k \in \mathbb{\mathbb{Z}}$
For aperiodic functions, we consider all frequencies. 

For periodic we have an amplitude at each $k$, which just maps to $\omega$ by $\omega=k\omega_{0}$.
![[Pasted image 20251007095146.png|500]]

In continuous, we have everything
![[Pasted image 20251007095225.png|500]]


$x(j\omega)$ is related to how much $e^{j\omega t}$ is in $x(t)$. 

For example,
$$
\begin{align}
x(t) = e^{-\alpha t}u(t)
\end{align}
$$
where $a$ is real, $a > 0$.
This is an exponential decay starting somewhere, and is definitely aperiodic.
![[Pasted image 20251007095424.png|500]]


We want to find $x(j\omega)$
$$
\begin{align}
x(j\omega) = \int_{t=-\infty}^{\infty} e^{-\alpha t}u(t)e^{-j\omega t}dt \\
= \int_{0}^{\infty} e^{-\alpha t}e^{-j\omega t}dt \\
= \int_{0}^{\infty} e^{-(\alpha+ j\omega)t} dt \\
= \frac{-1}{\alpha+ j\omega} e^{-(\alpha+j\omega)t } \bigg|_{0}^{\infty}  \\ 
\end{align}
$$

$$
\begin{align}
x(j\omega) = -\frac{1}{\alpha+j\omega}( ?-1)
\end{align}
$$
Its easy to have the 0 bound, but how do we find this value at $\infty$?

$$
\begin{align}
-\frac{1}{\alpha+j\omega} ( \underbrace{ e^{-\alpha t} }_{ \text{ goes to 0 } }\underbrace{ e^{-j\omega t} }_{ \text{ magnitude 1 but oscillating } })
\end{align}
$$
This will look like something slowly spiraling into zero.
![[Pasted image 20251007095811.png|300]]
This converges to zero, but only because $a>0$.
$$
\begin{align}
a=0 \text{ then we would spin around } \\
a<0 \text{ we spiral out. BAD BAD  }
\end{align}
$$
 So this question mark bit
 $$
\begin{align}
? = 0 \text{ for } a > 0 \\
x(j\omega) = \frac{1}{\alpha+ j\omega}
\end{align}
$$
While it worked in this case, the continuous time Fourier transform doesn't always converge. If that is the case, then we'd have to use the Laplace Transform.

As sets for how broad they are:
![[Pasted image 20251007100131.png|500]]

We have the first Fourier transform pair.
$$
\boxed{
\begin{align} \\
\text{ time domain }  & \Leftrightarrow   \text{ frequency domain }\\
e^{-\alpha t}u(t) &  \Leftrightarrow  \frac{1}{\alpha+ j\omega}
\end{align}
}
$$
We can hop back and forth using these.
$$
\begin{align}
x(t) \Leftrightarrow  x(j\omega)
\end{align}
$$
How about another?

$$
\begin{align}
x(t) = \int_{t=-\infty}^{\infty} \delta(t-t_{0}) e^{-j\omega t}dt  \\
= e^{-j\omega t_{0}}
\end{align}
$$
By the sifting property!
So
$$
\boxed{
\begin{align}
\delta(t-t_{0}) \leftrightarrow  e^{-j\omega t_{0}}
\end{align}
}
$$

We worked really hard to express functions in terms of sums of other functions - if we can do that, then we can take those results with the delta functions and decays etc. 


Lets start with an $x(j\omega)$ and find what $x(t)$ is?

Let $x(j\omega)= 2\pi\delta(\omega-\omega_{0})$
This is just a spike of height $2\pi$ at frequency $\omega_{0}$, and zero elsewhere.

$$
\begin{align}
\mathscr{F^{-1}}\{ 2\pi\delta(\omega-\omega_{0})\}
\end{align}
$$
$$
\begin{align}
x(t) = \frac{1}{2\pi} \int_{\omega=-\infty}^{\infty} x(j\omega)e^{j\omega t}d\omega \\
x(t) =\cancelto{  }{  \frac{1}{2\pi} }\int_{\omega^{-}\infty}^{\infty} \cancelto{  }{ 2\pi  }\delta(\omega-\omega_{0})e^{j\omega t}d\omega \\
\text{ which means } \\
e^{j\omega_{0}t} \Leftrightarrow  2\pi\delta(\omega-\omega_{0})
\end{align}
$$
note that this $\omega_{0}$ is anything - it isn't isn't the fundamental frequency . We're just considering a point to care about. This is just a location where we have a frequency and we're isolating it. It could be any frequency. 

If we set $\omega_{0}=0$,
$$
\begin{align}
\text{ time }  &\, \, \, \, |\,     \text{ frequency } \\
1 \, \, \, \,  & \Leftrightarrow  \, \, \, 2\pi\delta(\omega)
\end{align}
$$

This is duality.

![[Pasted image 20251007102422.png|500]]

Note that a delta function is the limit as a gaussian as its width goes to zero, and that a constant is the limit as a gaussian goes to infinite width.

The fact that these are gaussians goes to the uncertainty principle ( see quantum!)

$\boxed{\delta(t)\Leftrightarrow 1}$

Lets look at a function that is one from $-T$ to $T$, and zero elsewhere.
$$
\begin{align}
\mathscr{F}\left\{ x(t) \right\}  \\
x(j\omega) = \int_{t=-\infty}^{\infty} x(t)e^{-j\omega t}dt  \\
= \int_{-T}^{T} (1)e^{-j\omega t}dt \\
= \frac{1}{-j\omega} e^{-j\omega t}\bigg|_{-T}^{T} \\
= -\frac{1}{j\omega}\bigg[ e^{-j\omega T}-e^{j\omega T} \bigg]  \\
= \frac{2}{\omega}\sin(\omega T)  
\end{align}
$$


As an aside, a normalized $\text{ sinc }$ function
$$
\begin{align}
\sin(\theta) = \frac{\sin(\pi\theta)}{\pi\theta}
\end{align}
$$
So we get
$$
\begin{align}
x(j\omega) = 2T \text{ sinc }\left( \frac{\omega T}{\pi} \right)
\end{align}
$$

![[Pasted image 20251007103706.png|500]]


## FT of a periodic signal
For a periodic signal,
$$
\begin{align}
x_{t} = \sum_{k=-\infty}^{\infty} a_{k} e^{jk\omega_{0}t}
\end{align}
$$
What if we do the Fourier transform on this instead of the Fourier series?
$$
\begin{align}
\mathscr{F} \left\{ x(t) \right\}  & = \int_{t=-\infty}^{\infty} a_{k} e^{jk\omega_{0}t}e^{-j\omega t}dt \\
 x(j\omega) & =\sum_{k=-\infty}^{\infty} a_{k} \underbrace{ \int_{t=-\infty}^{\infty} e^{jk\omega_{0}t}e^{-j\omega t}dt }_{ \mathscr{F} \left\{ e^{jk\omega_{0}t} \right\} \text{ definitionally } }
\end{align}
$$
We already know that
$$
\begin{align}
e^{jk\omega_{0}t} \Leftrightarrow  2\pi\delta(\omega-k\omega_{0})
\end{align}
$$
So we can simplify this to be
$$
\begin{align}
x(j\omega)= \sum_{k=-\infty}^{\infty} a_{k}e^{jk\omega_{0}} 
\end{align}
$$
Which has recovered the Fourier Series!

