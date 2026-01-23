
$$
\boxed{
\begin{align}
X(e^{j\omega})= \sum_{n=-\infty}^{\infty} x[n]e^{-j \hat{\omega}n}\\ 
x[n] = \frac{1}{2\pi} \int_{\hat{\omega}=2\pi}^{} X(e^{j \hat{\omega}})e^{j \hat{\omega}n}d \hat{\omega} \\
\end{align}
}
$$







We have the discrete time Fourier transform as
$$
\begin{align}
\tilde{x}[n] = x[n] = \frac{1}{2\pi} \int_{2\pi}  x(e^{j \hat{\omega}})e^{j \hat{\omega}n}d\omega
\end{align}
$$
(assuming that we go to really high $n$ samples, so that it is a Riemann sum that we're saying is an integral

where 
$$
\begin{align}
X(e^{j\hat{\omega}})= \sum_{n=-\infty}^{\infty} x[n]e^{-j \hat{\omega}n}
\end{align}
$$
and 
$$
\begin{align}
a_{k} = \frac{1}{N}X(e^{jk \hat{\omega}_{0}})
\end{align}
$$

This $X(e^{j \hat{\omega}})$ is continuous and periodic in $2\pi$, so $X(e^{j \hat{\omega}})=X(e^{j(\hat{\omega}+2\pi)})$

The DTFT converges for absolutely summable signals.

Note, our $X(e^{j\hat{\omega}})$ is a discrete signal for each input $\hat{\omega}$, but we have an infinite number of those $\hat{\omega}$ that we are considering. This is why we have to integrate over all of them.



Recall that if $\left| \alpha \right| <1$ then $\sum_{n=0}^{\infty}\alpha^{n}=\frac{1}{1-\alpha}$

The magnitude of $ae^{-j\hat{\omega}}<1$ since $\left| \alpha \right|<1$ and $\left| e^{-j\hat{\omega}} \right|=1$. This gives us nicely that
$$
\begin{align}
X(e^{j \hat{\omega}})= \frac{1}{1-ae^{-j\hat{\omega}}}
\end{align}
$$

Using Eulers identity $e^{j\hat{\omega}}=\cos(\hat{\omega})+j\sin(\hat{\omega})$, we have
$$
\begin{align}
\left| X(e^{j\hat{\omega}}) \right| = \frac{1}{\sqrt[]{ (1-a\cos(\hat{\omega}))^{2} + a\sin(\hat{\omega})^{2} } }
\end{align}
$$

## Ex 2

let $x[n]=\delta[n-n_{0}]$
$$
\begin{align}
X(e^{j\hat{\omega}})= \sum_{n=-\infty}^{\infty} \delta[n-n_{0}]e^{-j\hat{\omega}n} \\
=e^{-j\hat{\omega}n_{0}}
\end{align}
$$
So the Fourier transform pair 
$$
\begin{align}
\delta[n-n_{0}]\leftrightarrow  e^{-j\hat{\omega}n_{0}}
\end{align}
$$

## Ex 3
Lets take an $x[n]$ that is three spikes of height 1, at -1, 0, and 1.  We could use the $DTFS$ formula, or we can use the pairs.
$$
\begin{align}
\delta[n-1]\to  e^{j\hat{\omega}}\\
\delta[n]\to 1\\
\delta[n+1]\to  e^{-j\hat{\omega}}\\
\end{align}
$$
![[20251021_103510.jpg]]

Lets take a new slightly different function, that doesn't exactly land on every $2\pi$.
![[20251021_103519.jpg]]

$$
\begin{align}
2\pi \sum_{l=-\infty}^{\infty} \delta(\hat{\omega}-2\pi l-\hat{\omega}') \leftrightarrow  e^{-j\hat{\omega}'n}
\end{align}
$$


If we have a periodic signal, using the Fourier series we would have
$$
\begin{align}
x[n]= \sum_{k= <n>}^{} a_{k} e^{jk\hat{\omega}_{0} n}, \text{ where } \hat{\omega}_{0} =\frac{2\pi}{N}
\end{align}
$$

