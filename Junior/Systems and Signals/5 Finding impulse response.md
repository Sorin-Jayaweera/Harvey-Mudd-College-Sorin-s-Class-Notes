Note: From now on, I'll write convolution with $*$.

Say we have a system
$$
\begin{align}
y[n] = b_{0}x[n] + b_{1}x[n-1] - ay[n-1] 
\end{align}
$$
This system is causal, only depending on previous values.

$h[n]$, the impulse response, is $y[n]$ when $x[n]=\delta[n]$.

We have initial conditions, where for n<0, $h[n]=0$.

$h[n] = -a_{1}h[n-1]+b_{0}\delta[n]+b_{1}\delta[n-1]$

We can solve this iteratively and make a table

| n   | h[n]                    |
| --- | ----------------------- |
| <0  | 0                       |
| 0   | $b_{0}$                 |
| 1   | $b_{0}-a_{1}b_{0}$      |
| 2   | $a_{1}b_{1}-a^{2}b_{0}$ |
| ... |                         |
The pattern for this is
$$
\begin{align}
h[n] = \begin{cases}
0 & n < 0 \\
b_{0} & n = 0 \\
(a_{1})^{n-1}b_{1}+(-a_{1})^{n}b_{0} & n\geq 1
\end{cases}
\end{align}
$$
Which we can write with step functions
$$
\begin{align}
h[n] = b_{0} \delta[n] + \left((-a_{1})^{n-1}b_{1}+(-a_{1})^{n}b_{0}\right) u[n]
\end{align}
$$


There is a better way to do this though.


We can consider periodic functions $x(t)$

If we can write it as a Fourier series, like:
$$
\begin{align}
x(t) = x(t+T_{0}) = \sum_{k=-\infty}^{\infty} a_{k} e^{jk\omega_{k} t}, \text{ where } \omega_{0} = \frac{1\pi}{T_{0} }
\end{align}
$$

I.e., $y(t)= \cos(\omega t) * h(t)$
$$
\begin{align}
\frac{1}{2}(e^{j\omega t}+ e^{-j\omega t})
\end{align}
$$
$H(j\omega) = \frac{1}{1+j\omega}$
So we get
$$
\begin{align}
H(j\omega)  \frac{1}{2}e^{j\omega t} + \frac{H(-j\omega)1}{2}e^{-j\omega t}
\end{align}
$$


We take the continuous time Fourier series, where
$$
\begin{align}
a_{k} = \frac{1}{T_{0}} \int_{\frac{-T_{0}}{2}}^{\frac{T_{0}}{2}} x(t)e^{-jk\omega_{0}t}dt 
\end{align}
$$

