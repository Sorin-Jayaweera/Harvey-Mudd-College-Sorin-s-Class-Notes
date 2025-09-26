
Time invariance:

$$
\begin{align}
y(t) = \sin(t)x(t)
\end{align}
$$

is not time invariant. If $x(t)\to x(t-t_{0})$, then we would have
$$
\begin{align}
y(t) = \sin(t)x(t-t_{0})
\end{align}
$$
however, 
$$
\begin{align}
y(t-t_{0})= \sin(t-t_{0})x(t-t_{0})
\end{align}
$$
which is not the same.

We define a convolution
$$
\begin{align}
x[n]\circledast h[n] = \sum_{k=-\infty}^{\infty} x[k]h[n-k] = y[n] 
\end{align}
$$



In continuous time
$$
\begin{align}
x \circledast h = \int_{-\infty}^{\infty} x(\tau)h(t-\tau)d \tau 
\end{align}
$$
