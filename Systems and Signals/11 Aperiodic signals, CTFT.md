
Today we'll learn how to represent signals that *don't* repeat.
Continuous time Fourier Series only represent periodic signals, since they integrate over one period. 

Can we consider a function over a finite duration, and write it as a sum of $e^{j\omega t}$? 

We can copy-paste our signal, and make an envelope so that the front and end agree(don't jump)!. 


We look at $x(t)$ and tile it to have period over $T$, (such that they don't overlap).

$$
\begin{align}
\tilde{x}(t) = \sum_{k=-\infty}^{\infty} a_{k} e^{jk\omega_{0}t}
\end{align}
$$
where
$\omega_{0}= \frac{2\pi}{T}$

$$
\begin{align}
a_{k} = \frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}} \tilde{x}(t)e^{-jk\omega_{0}}dt 
\end{align}
$$

We note that this looks the same as only our original function, since its just over the length that our function exists (its zero everywhere else)

$$
\begin{align}
a_{k}  = \int_{-\infty}^{\infty} x(t)e^{-jk\omega_{0}t}
\end{align}
$$
We define a new thing
$$
\begin{align}
\mathbf{X}(j\omega ) = \int_{-\infty}^{\infty} x(t)e^{-j\omega t}dt 
\end{align}
$$
and say that the thing in our $a_{k}$ is just $\mathbf{X}(jk\omega_{0})$

Since $\omega_{0}=\frac{2\pi}{T}$, $\frac{1}{T}=\frac{\omega_{0}}{2\pi}$
$a_{k}=\frac{1}{T}\mathbf{X}(jk\omega_{0})$

so we can sub into the synthesis equation
$$
\begin{align}
\tilde{x}(t) = \sum_{k=-\infty}^{\infty} a_{k} e^{jk\omega_{0}t} \\
= \sum_{k=-\infty}^{\infty} \frac{1}{T}\mathbf{X}(jk\omega_{0}t)\omega_{0}
\end{align}
$$

Lets take $T\to \infty$


We now have 
$$
\begin{align}
\tilde{x}(t) = \frac{1}{2\pi} \sum_{k=-\infty}^{\infty} \mathbf{x}(jk\omega_{0})e^{jk\omega_{0}t}\omega_{0} 
\end{align}
$$

Lets define another new object
$$
\begin{align}
x(jk\omega_{0})e^{jk\omega_{0}t} \equiv g(k\omega_{0},t)
\end{align}
$$
$$
\begin{align}
\tilde{x}(t) = \frac{1}{2\pi} \sum_{k=-\infty}^{\infty} g(k\omega,t)\omega_{0}
\end{align}
$$
As $T\to \infty$, $\omega=\frac{2\pi}{T}\to \text{ small }$




## Result
$$
\begin{align}
x(t) = \frac{1}{2\pi} \int_{w=-\infty}^{\infty} \mathbf{X}(j\omega)e^{j\omega t}d\omega \\
\end{align}
$$
We Because $\tilde{x}(t)\leftarrow x(t)$ as $T\to \infty$.
This looks "like" the CTFS synthesis. This is the inverse Fourier transform.


$$
\begin{align}
\mathbf{X}(j\omega) = \int_{-\infty}^{\infty} x(t)e^{-j\omega t}dt
\end{align}
$$
This is the continuous time Fourier Transform.

For periodic signals, we used $e^{jk\omega_{0}}t$, which is countably infinite basis functions - we only have integer $k$.

For aperiodic signals, The Fourier Transform uses $\omega$ everywhere - uncountably infinite basis functions.



Note, our signal has to have finite power, the integrals must converge.
$$
\begin{align}
\int_{-\infty}^{\infty} \left| x(t) \right| dt < \infty
\end{align}
$$


1) $H(j\omega)$ is the CTFT of $h(t)$, an aperiodic function.
2) If $x_1(t) = x_{2}(t)$, then $x_{1}(j\omega)=x_{2}(j\omega)$
3) 