
In review of last time for a bit.

Remember that we can represent $x(t)$ with the Fourier series as
$$
\begin{align}
x(t) = \sum_{k=-\infty}^{\infty} a_{k} e^{jk\omega_{0}t}
\end{align}
$$
The response through a LTI system is
$$
\begin{align}
y(t) = \sum_{k=-\infty}^{\infty} H(jk\omega_{0})a_{k} e^{jk\omega_{0}t}
\end{align}
$$
Where $H(jk\omega_{0})$ is the frequency response function, i.e.
$$
\begin{align}
\frac{1}{1+j\omega}
\end{align}
$$

OR, more clearly
$$
\begin{align}
y(t) = \sum_{k=-\infty}^{\infty} b_{k} e^{jk\omega_{0}t}
\end{align}
$$
where
$$
\begin{align}
b_{k} = H(jk\omega_{0})a_{k} 
\end{align}
$$

### For example:

$$
\begin{align}
x = \cos(10t)
\end{align}
$$

$$
\begin{align}
a_{\pm 1} = \frac{1}{2} 
\end{align}
$$
We know
$$
\begin{align}
b_{1} = a_{1} \frac{1}{1+10j} = 0.05e^{-1.47 j} \\
b_{2} = a_{2} \frac{1}{1-10j}f= 0.05 e^{1.47 j}
\end{align}
$$
The phase 
$$
\begin{align}
\measuredangle  = \tan ^{-1}\left( \frac{0}{1} \right) - \tan ^{-1}\left( \frac{20}{2} \right)
\end{align}
$$
$$
\begin{align}
\tan ^{-1}\left( \frac{\text{ top imaginary }}{\text{top real }}  \right) - \tan ^{-1}\left( \frac{\text{ bot imaginary }}{\text{ bot real }} \right)
\end{align}
$$

## Discrete time
if we can come up with a representation of $x[n]$ in the form
$$
\begin{align}
x[n] = \sum_{k= <N>}^{} a_{k} e^{jk \hat{\omega_{0}}n} 
\end{align}
$$

then we have 
$$
\begin{align}
y[n] = \sum_{k= <N>}^{} H(e^{jk \hat{\omega}_{0} })e^{jk \hat{\omega}_{0} n} 
\end{align}
$$
Or similarly,
$$
\begin{align}
\text{ let } b_{k} = H(e^{jk \hat{\omega}_{0} })a_{k}  \\
y[n] = \sum_{k= <N>}^{} b_{k} e^{jk \hat{\omega}_{0} n} 
\end{align}
$$
### For Example:
$$
\begin{align}
x[n] = \cos\left( \frac{\pi}{2}n \right). N=4,  \hat{\omega}_{0} = \frac{\pi}{2} \\
a_{\pm1} = \frac{1}{2}, & a_{k} = a_{k+N}  
\end{align}
$$
If 
$$
\begin{align}
H(e^{j\hat{\omega}}) = \frac{1}{2} (1+e^{-j \hat{\omega}})
\end{align}
$$
then
$$
\begin{align}
b_{1} = \frac{1}{2} \left( \frac{1}{2}\left( 1+e^{-j \frac{\pi}{2}} \right) \right) = \frac{\sqrt[]{ 2 }}{4} e^{-j \frac{\pi}{4}}\\
b_{2} = \frac{1}{2} \left( \frac{1}{2}\left( 1+e^{j \frac{\pi}{2}} \right) \right) =\frac{\sqrt[]{ 2 }}{4} e^{j \frac{\pi}{4}} \\
\end{align}
$$

So
$$
\begin{align}
y = \frac{\sqrt[]{ 2 }}{2} \cos\left( \frac{\pi}{2}n - \frac{\pi}{4} \right) 
\end{align}
$$


