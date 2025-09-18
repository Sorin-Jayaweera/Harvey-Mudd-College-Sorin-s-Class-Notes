
Take a square wave from $-T_{0}$ to $T_{0}$

We can Fourier decompose this with
$$
\begin{align}
a_{x} = \frac{1}{T_{0}}\int_{T_{0}} x(t)e^{-jk\omega_{0}t} \\
\text{ where } \omega_{0} = \frac{2\pi}{T_{0}}
\end{align}
$$
$$
\begin{align}
A_{k} = \frac{1}{T_{0}} \bigg[ \int_{-\frac{T_{0}}{2}}^{0} (-1)e^{-jk\omega_{0}t}dt + \int_{0}^\frac{T_{0}}{2}(1)e^{-jk\omega_{0}t}dt   \bigg]  \\

\end{align}
$$
$$
\begin{align}
\frac{1}{T_{0}}\left[ \frac{-1}{-jk\omega_{0}}\underbrace{ e^{-jk\omega_{0}t} \bigg|_{-\frac{t_{0}}{2}}^{0} }_{ \left( 1-e^{jk \frac{2\pi}{T_{0}} \frac{T_{0}}{2}} \right) } + \frac{1}{-jk\omega_{0}}\underbrace{ e^{-jk\omega_{0}t}\bigg|_{0}^{\frac{T_{0}}{2}} }_{ e^{-jk 2\pi \frac{To}{2T_{0}}}-1 }\right] \\
   
\end{align}
$$
For which the e to the stuff collapse to
$$
\begin{align}
(1-e^{jk\pi}) \text{ and } (e^{-jk\pi} -1)
\end{align}
$$

We can fully unpack these to get
$$
\begin{align}
a_{k}= \frac{1}{jk\pi}(1-\cos(k\pi)) \\
= \frac{1}{jk\pi}[1-(-1)^{k}]
\end{align}
$$


## Properties of the  Fourier series
### Continuous time
Linearity
Coefficients are scaled with the function

Time shift: If we move a function by some amount, we multiply each coefficient by the complex exponential 
$$
\begin{align}
a(t) \to   a_{k} \\
b(t) \to   a(t-t_{0}) \\
b_{k} = e^{-j\omega_{0}kt_{0}}a_{k}  
\end{align}
$$
### Discrete time
$$
\begin{align}
x[n] = x[n+N], N \text{ is the fundamental period } \\
\hat{\omega_{0}} = \frac{2\pi}{N} \text{ is the fundamental frequency } \\
\end{align}
$$

This is conceptually similar but with a big wrinkle. 
$$
\begin{align}
\phi_{k} [w] = e^{jk \hat{\omega_{0}}n}, k = 0,\pm 1, \pm 2,\dots
\end{align}
$$
Instead of summing over all infinite frequencies, we have to limit ourselves. This is because the k's are no longer unique:
$$
\begin{align}
e^{jk \hat{\omega}_{0} n} = e^{jk \hat{\omega_{0}}n(k+rN)}
\end{align}
$$
where $r$ is an integer and $N$ is the fundamental period
$$
\begin{align}
= e^{jk \hat{\omega_{0}}n}e^{jrN \frac{2\pi}{N}n} \\
= e^{jk\hat{\omega}n}
\end{align}
$$
since 
$$
\begin{align}
e^{2\pi rjn} = \cos(2\pi \underbrace{ rm }_{ \text{ integer } }) + j\sin(2\pi \, \, r m)
\end{align} = 1
$$
If, for example, our signal is periodic over $n=4$, then we only have k from $-4$ to $4$, otherwise we would repeat. 

Wild thing: We can now use any range of $k$ for our basis functions, as long as there are all $N$ versions. 

Can we really reproduce a signal with such a tight limit of basis functions?

Lets take a vanilla range 
$$
\begin{align}
x[n] = \sum_{k=0}^{N-1} a_{k} e^{jk \hat{\omega_{0}}n} 
\end{align}
$$
Lets multiply each side by $e^{-jr \hat{\omega_{0}}n}$.
We now sum over n from 0 to $N-1$. 

We get
$$
\begin{align}
\sum_{n=0}^{N-1} x[n] e^{-jr \hat{\omega_{0}}n} = \sum_{n=0}^{N-1} \sum_{k=0}^{N-1} a_{k} e^{jk \hat{\omega_{0}}n}e^{-jr \hat{\omega_{0}}n}
\end{align}
$$
We can rewrite the right hand side:
$$
\begin{align}
\sum_{k=0}^{N-1} a_{k} \sum_{n=0}^{N-1} e^{j(k-r)\hat{\omega_{0}}n}
\end{align}
$$
There is a lemma that we can use
$$
\begin{align}
\sum_{n=0}^{N-1} e^{j m \hat{\omega_{0}}n} = \begin{cases}
N &  m = 0, \pm  N, \pm  2N \\
0 & \text{ otherwise }
\end{cases}  
\end{align}
$$
For our cases, this is
$$
\begin{align}
\sum_{n=0}^{N-1} e^{j(k-r)\hat{\omega_{0}}n} = \begin{cases}
N  & k=r  \\
0 & k\neq  r
\end{cases}
\end{align}
$$
Note that this is because we chose to start at 0 instead of any of the arbitrary set of consecutive numbers of length N that we could have used. We would have a different constraint of $k-r= Mn$ $(\text{ or } k-r)$ is an integer multiple of n. We don't span the range between each of the solutions $0,\pm N,\pm 2C$ etc. So we only need one - and we chose the simplest, which was zero. 

$$
\begin{align}
a_{r} = \frac{1}{N} \sum_{n=0}^{N-1} x[n] e^{-jr \hat{\omega_{0}}n}
\end{align}
$$
