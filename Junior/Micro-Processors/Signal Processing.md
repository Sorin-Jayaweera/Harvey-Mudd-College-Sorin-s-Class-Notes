Imagine a sound source going to a microphone, which outputs $\pm 10mV$. This is usually fed to a pre-amplifier, which would make it $\pm 1V$. This then would have to be shifted up 2 volts to be usable by the analog to digital converter of the MCU. 

This is the receive chain - gain, and offset. 

Audio is usually sampled at 44.1 kilo-samples per second, because our ears cap out at 20khz and Nyquist. It is useful to think of the Fourier representation of the continuous time signal sampled with a bunch of delta functions. For in depth, see [[Application.pdf]].

Note that you might accidentally sample things that you don't mean to.
We handle this by putting an anti-aliasing filter (low pass) before the analog to digital filter. 

Lets consider a situation where we have the following:
A signal of interest as a 10 Khz tone (sin)
Sampling at 100 KSps (kilo samples per second) (so max representable signal is 50 Khz).
The anti aliasing filter is a first order RC, with a corner at 10 Khz. 

How much rejection in DB do we get from 100 Khz Blocker? 

The RC falls with 20 dB per decade, so a 20 dB reduction. 


| Reconstruction loss | $\frac{f_{sig}}{fs}$ |
| ------------------- | -------------------- |
| 1db                 | 40%                  |
| 3db                 | 60%                  |
| 6db                 | 80%                  |
| 10db                | 90%                  |

When we go to the real world, the voltage that comes out has all the high and low frequency copies, which are called "images". We address that by attaching the DAC to a low-pass filter - "Reconstruction Filter".

## Digital Filters
FIR filter:
We can take an impulse response and convolve it with any input and find how a system will respond to the new input. 

We can do that in a digital system, programming an arbitrary impulse response and kick it with a digital signal. 

We have a digitized signal, which we want to delay to get multiple copies (put a chain of registers). Each of those copies will go down to a multiplier, which has a coefficient attached, and then added together. This is hardware convolution, aka the Finite Impulse Response Filter.

How do we pick the tap weights (coefficients that multiply each time sample)? 
Lets say we want a perfect low pass filter, a first order low pass, a high pass, and a linear phase (delayed).

![[Pasted image 20251028141343.png|500]]![[Pasted image 20251028141355.png|500]]
![[Pasted image 20251028141414.png|500]]
![[Pasted image 20251028141428.png|500]]
![[Pasted image 20251028141437.png|500]]


We can make an infinite impulse response filter to implement the first order low pass filter.
$$
\begin{align}
a_{0}=1 \\
a_{1}=e^{\frac{-t}{\tau }} \\
a_{2}=e^{\frac{-2t}{\tau }} \\
a_{3}=e^{\frac{-3t}{\tau }} \\
\end{align}
$$
This could be implemented as a feedback, where the signal is the current + the previous $e^{\frac{-t}{\tau}}$. Note that anytime you see feedback, you should be worried about stability.

![[Pasted image 20251028142312.png|500]]

## Cross correlation
We define this as
$$
\begin{align}
\sum_{}^{} x[n]y[n]
\end{align}
$$
Let $x[n]\text{ and } y[n]$ be sampled $\cos(\omega_{1} t)\text{ and } \cos (\omega_{2} t)$.

If we let $y[n]=e^{jk \frac{2\pi}{N}n}$, then it would be exactly the discrete Fourier Series.
$\vec{S_{p}}$

