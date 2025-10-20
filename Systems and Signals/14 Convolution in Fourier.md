## Continuous
![[20251016_095116.jpg|500]]

![[20251016_095132.jpg|500]]

Then we get $H(j\omega)= \frac{Y(j\omega)}{X(j\omega)} = \frac{j\omega+2}{(j\omega)^{2}+4j\omega+3}$

The inverse Fourier transform of this is $h(t)$. This is most easily done with the Fourier transform pairs that we derived. 

We use partial fractions to separate out
$$
\begin{align}
H(j\omega) = \frac{\frac{1}{2}}{j\omega+1}+ \frac{\frac{1}{2}}{j\omega+3}
\end{align}
$$
Recall
$e^{-\alpha t}u(t)\leftrightarrow \frac{1}{\alpha+j\omega}$
so $h(t)= \frac{1}{2}e^{-t}u(t)+\frac{1}{2}e^{-3t}u(t)$

Lets take an arbitrary input $x(t)=e^{-4t}$. The Fourier transform is $X(j\omega)=\frac{1}{4+j\omega}$

Then we have
$Y(j\omega)=H(j\omega)X(j\omega)$

and then go back to the time domain with the Fourier pairs.

One more interesting proprety:
Multiplication and convolution are DUALS
$$
\boxed{
\begin{align}
x(t)*y(t)\leftrightarrow X(j\omega)Y(j\omega)\\
x(t)y(t)\leftrightarrow \frac{1}{2\pi}X(j\omega)*Y(j\omega)
\end{align}
}
$$

Note that if the Fourier domain is a bunch of delta functions that are far enough apart, then we just get multiple copies of the original function.

## Discrete

Lets take an  aperiodic signal $x[n]$

We truncate it to only exist over one period $N_{1}$, and zero elsewhere, then make it a periodic function by making copies at a period N > $2*N$

call this $\tilde{x}[n]$ with period $N$ and $\hat{\omega}_{0}=\frac{2\pi}{N}$.

We now have the Fourier series representation 
$a_{k}= \frac{1}{N}\sum_{N}^{}\tilde{x}[n]e^{-jk(\frac{2\pi}{N})n}$ and $\tilde{x}= \sum_{N}^{}a_{k}e^{jk(\frac{2\pi}{N})n}$.


