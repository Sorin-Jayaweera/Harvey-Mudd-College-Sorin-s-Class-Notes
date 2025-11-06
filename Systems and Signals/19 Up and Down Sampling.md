
Lets think about continuous to digital converters some more.

If we have an $X(j\omega)$ in continuous time (i.e. for example a box $u(\omega-\omega_{0})u(-\omega-\omega_{0})$,) then we can take it to discrete time Fourier representation by rescaling it: divide the height by $T$, stretch the frequency axis so that $\omega_{0}$ maps to $\omega_{0}T$,  and tile it to be periodic every $2\pi$.

This applies for any signal. To go from discrete time to continuous, we just do the inverse - keep only the representation from $-\pi$ to $\pi$ squish the frequency axis to map $\omega_{0}T$ to $\omega_{0}$, divide the amplitude by $T$.

Side note:
If you have high frequency data, that's good for bandwidth and time resolution in the frequency domain. However, it takes a lot of resources to store all that data, so we really only want to sample as fast as useful. 

## Down Sampling
Decreasing your sample rate by an integer factor $N$. We are keeping every N'th data point when down sampling, squishing all N-1 inbetween them. 

We have a discrete time signal, multiply by a discrete time pulse train, pass it through a "decimation block" of a factor $N$, and take out our new $x_{b}$ signal.

The pulse train $p[n]$ is a delta every $N$ samples, and zero everywhere else. This keeps only time indices that are integer multiples of $N$. 

The decimation block discards the zeros in between. We take every $n^{th}$ sample, and make them adjacent to each other in the signal. 

What is happening in the frequency domain when we do this?



| Time       |                               | Frequency                  |                                                                                                                                  |
| ---------- | ----------------------------- | -------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| $p[n]$     | $\sum_{k}^{}\delta[n-kN]$     | $P(e^{j\hat{\omega}})$     | $\sum_{k=0}^{N-1} \frac{2\pi}{N}\delta\left( \omega-k \frac{2\pi}{N} \right)$                                                    |
| $x_{p}[n]$ | $x[n]p[n]$                    | $X_{p}(e^{j\hat{\omega}})$ | $\frac{1}{N} \sum_{k=0}^{N-1} X(e^{j(\omega-\frac{2\pi}{N}k)})$<br>and<br>$\sum_{k=-\infty}^{\infty} x_{p}[kN]  e^{-jk\omega N}$ |
| $x_{b}[n]$ | $x_{p}[Nn]$<br>and<br>$x[Nn]$ | $X_{b}(e^{j\hat{\omega}})$ | $X_{p}(e^{j \frac{\hat{\omega}}{N}})$                                                                                            |
The key take away: When down sampling in software, we have to filter and then decimate. Otherwise, we'll have aliasing.

The derivation of this table is found below.
Lets do the time domain analytical expression first:

$p[n] = \sum_{k}^{}\delta[n-kN]$

### $P[n]$
The discrete Fourier series
$$
\begin{align}
p[n]  & = \sum_{k=0}^{N-1} a_{k} e^{j \frac{2\pi}{N}kn} \\
a_{k}  & = \frac{1}{N} \sum_{n=0}^{N-1} p[n]e^{-j \frac{2\pi}{N}kn} \\
 & = \frac{1}{N} \forall k
\end{align}
$$
The discrete time Fourier transform
$$
\begin{align}
e^{j\omega_{0}n}  & \leftrightarrow  2\pi \delta(\omega-\omega_{0}) \\
e^{j \frac{2\pi}{N}kn}  & \leftrightarrow  2\pi \delta\left( \omega- \frac{2\pi}{N}k \right) \\
\sum_{k=0}^{N-1} a_{k}e^{j \frac{2\pi}{N}kn}  & \leftrightarrow  2\pi \sum_{k=0}^{N-1} a_{k} \delta\left( \omega- \frac{2\pi}{N}k \right)
\end{align}
$$
so
$$
\begin{align}
p[n] = \sum_{k=0}^{N-1} \frac{1}{N} e^{j \frac{2\pi}{N}kn}\leftrightarrow  \sum_{k=0}^{N-1} \frac{2\pi}{N}\delta\left( \omega-k \frac{2\pi}{N} \right) 
\end{align}
$$
So the frequency domain of our pulse chain is deltas of height $\frac{2\pi}{N}$ spaced every $\frac{2\pi}{N}$.

### $x_{p}$
There are two approaches we could do. 
#### Approach 1, convolution
$x_{p}=x[n]p[n] \leftrightarrow X_{p}(e^{j\hat{\omega}})$

$$
\begin{align}
X_{p} (e^{j\omega})  & = \frac{1}{2\pi} P(e^{j\hat{\omega}})*X(e^{j\hat{\omega}}) \\
 & = \frac{1}{2\pi} \int_{2\pi}^{} P(e^{j\theta})X(e^{j(\omega-\theta )})d\theta \\
 & =\frac{1}{2\pi}\int_{2\pi} \frac{2\pi}{N} \sum_{k=0}^{N-1} \delta\left( \theta-\frac{2\pi}{N}k \right)X(e^{j(\omega-\theta)})d\theta \\
 & = \frac{1}{N} \sum_{k=0}^{N-1} \int_{0}^{2\pi} \delta\left( \theta-\frac{2\pi}{N}k \right)X(e^{j(\omega-\theta)})d\theta \\
 & \text{ this is the sifting proerty } \\
 & =\frac{1}{N} \sum_{k=0}^{N-1} X(e^{j(\omega-\frac{2\pi}{N}k)})
\end{align}
$$
We are scaling by $\frac{1}{N}$ and have a bunch of copies of our $X(e^{j\hat{\omega}})$ centered at integer multiples of $\frac{2\pi}{N}$. 

The $x_{p}(e^{j\hat{\omega}})$ is periodic every $\frac{2\pi}{N}$ with a height $\frac{1}{N}$ of our $X(e^{j\hat{\omega}})$
If we have aliasing, then the boundaries between these would overlap - so the width of the new version would be enough to touch from either side. Aliasing can happen not only when we go from continuous to discrete time, but any time that we change our sampling rate. 

#### Approach 2: Definition of DTFT

$$
\begin{align}
x_{p} [n] = \sum_{k}^{} x[kN]\delta[n-kN]\leftrightarrow  X_{p} (e^{j\hat{\omega}})
\end{align}
$$
$$
\begin{align}
\delta(n-kN) & \leftrightarrow  \sum_{n=-\infty}^{\infty} \delta[n-kN]e^{-j\omega n} \\
 & =e^{-j\omega kN}
\end{align}
$$
This is a linear operator, so we have
$$
\begin{align} \\
x_{p} [kN]  & \leftrightarrow  X_{p} (e^{j\hat{\omega}}) \\
\sum_{k=-\infty}^{\infty} x[kN]\delta(n-kN)  & \leftrightarrow   \sum_{k=-\infty}^{\infty} x_{p}[kN]  e^{-jk\omega N}
\end{align}
$$

### $x_{b}[n]$
$$
\begin{align}
X_{b} (e^{j\hat{\omega}})  & = \sum_{k}^{} x_{b} [k]e^{-j\omega k} \\
 & = x_{p} [kN]e^{-j\omega k} \\
 & = \sum_{n=\text{ integer multiple of N }}^{} x_{p} [n] e^{-j\omega \frac{n}{N}}  \\
 &  \text{ because } x_{p} [n]=0 \text{ when } n \neq  kN, k \in \mathbb{Z} \\
 & = \sum_{n=-\infty}^{\infty} x_{p} [n]e^{-j\omega \frac{n}{N}} \\
  & = X_{p} (e^\frac{j \omega}{N})
\end{align}
$$
So we're only stretching the frequency axis by a factor of $N$. When in $X_{p}(e^{j\hat{\omega}})$ having a width $\omega_{0}$, the width becomes $N\omega_{0}$. Instead of being centered at $\frac{2\pi}{N}$, now they are centered at $2\pi$. The height is the same as before, $\frac{1}{N}$. 

Our results are analogous to continuous time. Aliasing occurs if $\omega_{0}> \frac{\pi}{N}$. If we will have aliasing, we'll have to apply an anti-aliasing filter before down-sampling. 


## Up-sampling
Increasing the sampling rate by integer factor $N$. 
We do this by padding zeros and interpolating. 
$$
\begin{align}
x_{b} [n] \to  \text{ zero padding } \to  x_{p} [n] \to  \text{ interpolation envolope } \to   x[n]
\end{align}
$$
We're doing the same operation as before, but in the reverse. 



![[Pasted image 20251104105024.png]]

The ideal filter in the time domain is the sinc function (it is zero at each data point, and smoothly interpolating between points), which looks like a box in the frequency domain. However, its hard to do that in practice. Its easy to have a zero order hold in the time domain, which is a sinc in the frequency domain.

'When upsampling, we use an interpolation filter that is a box that holds data (as a low pass filter). In reality we can't be perfect, so we could have a box that approximates the zeroth order hold but has slightly curved sides.

