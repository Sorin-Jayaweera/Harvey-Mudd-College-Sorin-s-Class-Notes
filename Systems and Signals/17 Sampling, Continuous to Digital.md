
The discrete time Fourier series is the only useful one in practice. When we sample data, it is inherently discrete. With an aperiodic signal, the definition goes from -infinity to +infinity, and we can't do that. The discrete series has a finite definition which we could compute in real life.
The only one with real data is the DFS. We take a chunk of data, pretend it is one period, and chug ahead. The other three tools are useful in theory. If we want to design a communication system, for example, we will need to use those. But for interpreting data read from a sensor, we need the discrete Fourier series.

### Aside
This is a transform that represents the exact same thing in different forms. Similar to the transform pairs from polar to rectangular coordinates - just different representations that have a linear map.
$$
\begin{align}
re^{j\theta} = \sqrt[]{ x_{i}^{2}+x_{r} ^{2}  }e^{j \tan ^{-1}(\frac{x_{i} }{x_{r} })}  \\
x_{r} +jx_{i} = r\cos\theta +j r \sin\theta 
\end{align}
$$
Imagine we called these the polar transform and inverse polar transform. If all you knew was polar form, it would be hard to add complex numbers. But if we knew the rectangular form, that would be easy. The point is - having two equivalent representations that are different allows you to do far more complex operations.

We are taking a whole signal and representing it in a different way, and then manipulating it.


## The Fast Fourier Transform
This is an efficient Implementation of the Discrete Fourier Transform (for some reason the exact same thing as the Discrete Fourier Series - why the transform vs series naming mix?).

The information that you are looking for is hard to see in the time domain, but very clear in frequency. 
In speech recognition, we look at the spectrogram of a voice to recognize things (which is the same as how our brains do it - different frequencies travel different depths in our ears, and we have receptors at each depth).

Looking at radio, you'll have a terrible mess in time but neatly sectioned off bands in frequency. 

Audio and image compression relies on Fourier compression of pixel data. 

Take a sequence of data, take the DFT, cut out frequencies that you don't care about - and you have a much smaller representation. Its a little grainy when you go back to time, but still contains a lot of the data quality.

## Sampling

Why do we need sampling?
If we replace a continuous time analog circuit with a digital system that has analog to digital and digital to analog converters, then we'll be able to do more manipulations with the data - logging, controlling, updating system behavior without manually replacing op amps, etc.


In the time domain, sampling a signal is just saying
$$
\begin{align}
x[n] = x(nT)
\end{align}
$$
In the frequency domain, however, this is harder.

What we are really doing is making a delta function pulse train at $0,T,2T...$. We are multiplying this by $x(t)$ to get a continuous time signal but that only has the values at multiples of $T$. 
$$
\begin{align} 
p(t) = \sum_{k=-\infty}^{\infty} \delta(t-kT)\\
x_{P}(t) = x(t)p(t) \\
= \sum_{k}^{} x(t)\delta (t-kT) \\
= \sum_{k}^{} x(kT)\delta(t-lT)
\end{align}
$$

We can write $x[n]$ as either a scalar or as a signal, 
$$
\begin{align}
x[n]=x(nT) \\
= \sum_{k}^{} \delta(n-k)
\end{align}
$$

Lets do these steps in Fourier now.
We have an impulse train $p(t)$, lets get the frequency domain for that. 
Lets take the Fourier series.
We find $a_{k}$:
$$
\begin{align}
p(t)  & = \sum_{k}^{} a_{k} e^{jk\omega_{0}t}
\end{align}
$$
$$
\begin{align}
a_{k}  & = \frac{1}{T} \int_{-\frac{T}{2}}^{\frac{T}{2}} (t)e^{-jk\omega_{0}t}dt
\end{align}
$$
This is just a single impulse at zero.
$$
\begin{align}
a_{k}  & = \frac{1}{T} \int_{-\frac{T}{2}}^{\frac{T}{2} } \delta(t)e^{-jk\omega_{0}t}dt
\end{align}
$$
This just pulls out
$$
\begin{align}
a_{k}  & = \frac{1}{T}e^{-jk\omega_{0}(0)} \\
a_{k}  & = 1\\ 
\end{align}
$$
We know that $e^{j\omega_{0}t}\leftrightarrow 2\pi\delta(\omega-\omega_{0})$,
so
$$
\begin{align}
e^{j \frac{2\pi}{T}kt}\leftrightarrow  2\pi\delta\left( \omega- \frac{2\pi}{T}k \right)
\end{align}
$$
$$
\begin{align}
\sum_{}^{} a_{k} e^{j \frac{2\pi}{T}kt} \leftrightarrow  \sum_{k}^{} 2\pi a_{k} \delta\left( \omega-\frac{2\pi}{T}k \right) \\
p(t) = \sum_{k}^{} \frac{1}{T}e^{j \frac{2\pi}{T}kt} \leftrightarrow  \underbrace{ \sum_{k}^{} \frac{2\pi}{T}\delta\left( \omega-\frac{2\pi}{T}k \right) }_{ P(j\omega) }
\end{align}
$$
At integer multiples of $\frac{2\pi}{T}$ we have a sequence of impulses, with magnitude $\frac{2\pi}{T}$.

We will now take this result and use it to see how sampling effects our signal.

In continuous time we have a sequence of impulses but whose magnitudes are the value of the function at that spot. This is the $x_{p}(t)=x(t)p(t)$. 
We know that $x(t)p(t)\leftrightarrow X(j\omega)P(j\omega)=X_{p}(j\omega)$

We are defining the bandwidth of our generic $x(j\omega)$ as $\omega_{0}$.
$$
\begin{align}
x_{p} (j\omega)  & = \frac{1}{2\pi} \int_{-\infty}^{\infty} X(j\theta)P(j(\omega-\theta))d\theta \\
 & = \frac{1}{2\pi} \int_{-\infty}^{\infty} X(j\omega) \cdot \frac{2\pi}{T}\sum_{k=-\infty}^{\infty} \delta\left( \omega-\theta-\frac{2\pi}{T}k \right) d\theta \\
 & = \frac{1}{T} \sum_{k}^{} \int_{-\infty}^{\infty} X(j\theta)\delta\left(\omega-\theta-\frac{2\pi k}{T}\right)d\theta \\
\end{align}
$$
$$
\boxed{
\begin{align}
X_{p} (j\omega) & = \frac{1}{T} \sum_{k}^{} X\left( j \left( \omega- \frac{2\pi k}{T} \right) \right)
\end{align}
}
$$

This is an infinite sum of scaled and shifted versions of our $X(j\omega)$.  Here I draw an arbitrary $x(j\omega)$ that doesn't actually matter, just for graphical depiction.
![[Pasted image 20251028103810.png|500]]

We could have found $X_{p}(j\omega)$ in a different way (we'll call this approach 2), that will also be a useful representation of the same thing.
We could say
$$
\begin{align}
x_{p} (t) = \sum_{k}^{} x(kT)\delta(t-KT) \leftrightarrow  X_{p} (j\omega)
\end{align}
$$
$$
\begin{align}
\delta(t-kT) & \leftrightarrow  \int_{-\infty}^{\infty} \delta(t-kT)e^{-j\omega t}dt \\
 & = e^{-j\omega kT}
\end{align}
$$
If we have a whole bunch of these impulses and scale them by constant scaling factors, its just adding. Fourier analysis tools are just linear operators.

$$
\boxed{
\begin{align}
\sum_{k}^{} x(kT)\delta(t-kT) \leftrightarrow  \underbrace{ \sum_{k}^{} x(kT)e^{-jk\omega T} }_{ X_{p} (j\omega) }
\end{align}
}
$$
This is the other useful way of writing the exact same $X_{p}(j\omega)$.

Now we can move to the very last step: converting from these sequence of impulses of different magnitudes in continuous time to a discrete time.

$$
\begin{align}
x[n]\leftrightarrow  X(e^{j \hat{\omega}}) = ?
\end{align}
$$
Lets compare the definition of the DTFT.
$$
\begin{align}
x_{p} (j\omega)  & = \sum_{k}^{} x(kT)e^{-jk\omega T}  & \text{ From approach 2 } \\
X(e^{j\hat{\omega}})  & = \sum_{k}^{} x[k]e^{-j \hat{\omega}k}  & \text{ definition of DTFT }\\
 & = \sum_{k}^{} x(kT)e^{-j \hat{\omega}k}
\end{align}
$$

So  $X(e^{j \hat{\omega}})$ is just a frequency scaled version of $X_{p}(j\omega)$.
Since 
$$
\begin{align}
X_{p}(j\omega) & = \frac{1}{T}\sum_{k}^{}X\left( j\left( \omega-k \frac{2\pi}{T} \right) \right) & \text{ (from approach 1) } \\
X(e^{j\hat{\omega}})  & = X_{p} \left( j \frac{\hat{\omega}}{T} \right) \\
 & = \frac{1}{T} \sum_{k}^{} X\left( j\left(  \frac{\hat{\omega}-2\pi k}{T} \right) \right)
\end{align}
$$
This multiplies the location of peaks by $T$. So the peaks that used to be at $\frac{2\pi}{T}$ are moved to just $2\pi$.
![[Pasted image 20251028105336.png]]




In reality, we can't make perfect impulse trains, so instead we take a zeroth order hold. This acts like a hold, so we say that data is constant for each sampling period until the next sample. 
![[Pasted image 20251030102209.png]]