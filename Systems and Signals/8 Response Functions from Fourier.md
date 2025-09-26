We have learned the Continuous time Fourier Series and Discrete Time Fourier Series.

The "Series" and for periodic signals.

We also have the Continuous and Discrete Fourier Transform, which are for Aperiodic signals.

Recall the eigenfunction property for a linear time invariant system:
We have an impulse response $H(s)$
$$
\begin{align}
H(s) = \int_{-\infty}^{\infty} h(t)e^{jt}dt \\
\text{ where } s \text{ is some complex \# } \\
\text{ if } x(t) = e^{st}, y(t) = H(s)e^{st}
\end{align}
$$

How do we actually use this?

Lets take a system:
$$
\begin{align}
\dot{y}(t) + ay(t) = x(t)
\end{align}
$$

Let $x(t) = e^{j\omega t}$ so that we can take advantage of the Eigenvalue property.

We know that
$$
\begin{align}
y(t) = H(j\omega)e^{j\omega t} \\
\dot{y}(t)= j\omega H(j\omega)e^{j\omega t}
\end{align}
$$
We can sum in, so
$$
\begin{align}
j\omega H(j\omega)e^{j\omega t} + aH(j\omega)e^{j\omega t} = e^{j\omega t} \\
H(j\omega)e^{j\omega t}(j\omega+a) = e^{j\omega t}
\end{align}
$$
Since $e^{j\omega t}$ is never zero, we have
$$
\begin{align}
H(j\omega)(j\omega+a)=1 \\
H(j\omega) = \frac{1}{(j\omega+a)}
\end{align}
$$


Lets do this on something crazier
$$
\begin{align}
x(t) = \sum_{k=-\infty}^{\infty} a_{k} e^{jk\omega_{0}t}
\end{align}
$$
Feeding this through an LTI system, we have
$$
\begin{align}
\sum_{k=-\infty}^{\infty} H(jk\omega_{0})a_{k} e^{jk\omega_{0}t}
\end{align}
$$
Woah! We don't have to perform the convolution between $x(t)$ and $H(t)$ to get the response - we can apply the eigenvalue property on x by decomposing it into a bunch of different frequencies of $e^{jk\omega_{0} t}$.

### Example Time!

$$
\begin{align}
x(t) = \cos(10t) \text{ for } H(j\omega) = \frac{1}{1+j\omega} \\
x(t) = \frac{1}{2}(e^{10jt} + e^{-10jt}) \\
\implies a_{\pm  1} = \frac{1}{2} \\
\omega_{0} = 10 \frac{\text{ rad }}{\text{ sec }}
\end{align}
$$
All other Fourier components are zero, because its just a single cos.

We can write the response as
$$
\begin{align}
y(t)  & = \sum_{k=-\infty}^{\infty} H(jk\omega_{0})a_{k} e^{jk\omega_{0}t} \\
 & = \frac{H(j(-1)\omega_{0})}{2}e^{(-1)10jt} + \frac{H(j(1)\omega_{0})}{2}e^{(1)10jt} \\
 & = \frac{1}{2} \left| (H(-j\omega_{0})) \right| e^{-10jt + j<H(-j\omega_{0})} + \frac{1}{2} \left| H(j\omega) \right| e^{10jt _{ <H(j\omega_{0})j} }
\end{align}
$$
So the magnitude is an even function

We can find 
$$
\begin{align}
\left| H(j\omega) \right| = \left| \frac{1}{j\omega+1} \right| \\
= \frac{1}{\sqrt[]{ 1 + \omega^{2} } } \\
= \left| H(-j\omega) \right|  \\
< H(j\omega) = - \tan ^{-1}\left( \frac{\omega}{1} \right) = - < H(-j\omega) 
\end{align}
$$
so the angle is an odd function.


$$
\begin{align}
y(t) = \frac{1}{2}\left| H(10j) \right| e^{-j(10+ <H(10j))} + \frac{1}{2} \left| H(j\omega) \right| e^{j(10t+<H(10))} \\
= \left| H(10j) \right| \cos(1-t+<H(10j)) \\
= \frac{1}{\sqrt[]{ 101 }} \cos(10t+1.47)
\end{align}
$$

The corner frequency of $\frac{1}{j\omega+1}$ is 1


We can now predict the output from ANY function. 
We find the Fourier representation and the impulse response - then we have truly the output (without having to compute any more convolutions)!



## Discrete time
We have a similar eigenfunction property
$$
\begin{align}
x[n] = z^{n} \to  \text{ LTI } \to   H(z)z^{n}
\end{align}
$$
Let $z$ be in the form $e^{j\hat{\omega}}$, with unit amplitude.
$H(z) = \sum_{k=-\infty}^{\infty} h[k]z^{-k}$

Feeding in $z^{n}= e^{j\hat{\omega}n}\to H(e^{j\hat{\omega}})e^{j\hat{\omega}n}$

Lets consider a function
$$
\begin{align}
y[n] = \frac{1}{2}[x[n]+x[n-1]] \text{ , a moving average of window 2 }
\end{align}
$$
Lets find our response $H(e^{j\hat{\omega}})$ for this function.
Lets take a special $x[n]= e^{j\hat{\omega}n}$
$$
\begin{align}
y[n]= H(e^{j\hat{\omega}})e^{j\hat{\omega}n} \\
H(e^{j\hat{\omega}} )e^{j\hat{\omega}n} = \frac{1}{2} e^{j\hat{\omega}n} + \frac{1}{2} e^{j\hat{\omega}(n-1)} \\
= \frac{1}{2}e^{j\hat{\omega}n}(1+e^{-j\hat{\omega}}) \\
H(e^{j\hat{\omega}}) = \frac{1}{2}(1+e^{-j\hat{\omega}})
\end{align}
$$

We can feed any $x[n]= \sum_{k= \left< n \right> }^{} a_{k}e^{jk\omega_{0}n}$
through the LTI to get
$$
\begin{align}
y[n] = \sum_{k=\left< n \right>  }^{} H(e^{jk \hat{\omega}}_{0} )a_{k} e^{jk \hat{\omega}_{0} n}
\end{align}
$$

### Example:

Lets take
$$
\begin{align}
x[n] = \cos\left( \frac{\pi}{2}n \right)
\end{align}
$$
$\hat{\omega}_{0}= \frac{\pi}{2}, N=4$

$$
\begin{align}
a_{1} = a_{-1} = \frac{1}{2} \\
\end{align}
$$
so
$$
\begin{align}
y[n] = \sum_{k=-1}^{2} H(e^{jk \hat{\omega}_{0} }) \frac{1}{2} e^{jk \hat{\omega}_{0} n}
\end{align}
$$

We can break this out and write the magnitude and phase of $H(e^{j \hat{\omega}})$

$$
\begin{align}
H(e^{j\omega}) = \frac{1}{2} (1+ e^{-j\omega}) = \frac{1}{2}(1+\cos(-\omega)+j\sin(-\omega))
\end{align}
$$

$$
\begin{align}
\left| H(e^{j \hat{\omega}}) \right| = \frac{1}{2} \sqrt[]{ (1+\cos(\omega))^{2} + (-\sin(\omega))^{2} }  \\
= \frac{\sqrt[]{ 2 }}{2}\sqrt[]{ 1+\cos(\omega) } 
\end{align}
$$
The angle
$$
\begin{align} \\
\measuredangle   H(e^{j \hat{\omega}}) = \measuredangle  \frac{1}{2}(1+\cos(\omega)- j\sin(\omega)) \\
= -\tan ^{-1}\left( \frac{\sin(\omega)}{1+\cos(\omega)} \right) \to  \frac{\sin(\omega)}{1+\cos(\omega)} = \tan\left( \frac{\omega}{2} \right)  \\ 
\end{align}
$$
$$
\begin{align}
\measuredangle  H(e^{j \hat{\omega}}) = -\tan ^{-1}\left( \tan\left( \frac{\omega}{2} \right) \right) = -\frac{\omega}{2}
\end{align}
$$
This is an odd function.

We can now write out
$$
\begin{align}
y[n] = \frac{1}{2} \left| H(e^\frac{j \pi}{2}) \right| (e^{-j(\frac{\pi}{2})n \measuredangle  H(e^{\frac{j\pi}{2})}}+ e^{j(\frac{\pi}{2})n+ \measuredangle  H(e^{\frac{jpi}{2}})}) \\
= \left| H(e^\frac{j \pi}{2}) \right| \cos(\frac{\pi}{2}n + \measuredangle  H(e^{j \frac{\pi}{2}}))
\end{align}
$$

Note that this response function is periodic:
$$
\begin{align}
\frac{1}{2}(1+e^{-j\hat{\omega}}) = \frac{1}{2}(1+e^{-j(\hat{\omega}+2\pi)})
\end{align}
$$
So for this function,
$$
\begin{align}
H(e^{j\hat{\omega}}) = H(e^{j(\hat{\omega}+2\pi)})
\end{align}
$$
This is GOOD!

We chose arbitrarily to construct the Fourier coefficients for the range -1 to 2, but could do any other range. We should still get the same answer no matter where!
