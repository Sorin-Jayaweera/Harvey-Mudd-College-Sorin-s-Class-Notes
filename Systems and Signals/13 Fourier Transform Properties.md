Last time we talked about the Fourier transform for aperiodic signals.

For the periodic x(t), if we can do the Fourier series
$$
\begin{align}
x\left( t\right) = \sum_{k=-\infty}^{\infty} a_{k} e^{jk\omega_{0}t}  \\
\text{ (aka x(t)  is periodic)}
\end{align}
$$
Then 
$$
\begin{align}
x(j\omega) = \mathscr{F} \left\{ x(t) \right\} = \sum_{k=-\infty}^{\infty} 2\pi a_{k} \delta(\omega-\omega_{0}k)
\end{align}
$$

When you have a periodic $x(t)$, you both get to do this and HAVE to do this, as in this integral definition $x(j\omega)$ does not converge. 

For example,
$$
\begin{align}
x(t) = \cos(\omega_{0}t) \\
x(t) = \frac{1}{2}(e^{j\omega_{0}t}+e^{-j\omega_{0}t}) \\
\text{ Use the Fourier series } \\
x(t) = \sum_{k=-\infty}^{\infty} a_{k} e^{j\omega_{0}t}
\end{align}
$$
with $a_{\pm 1}$ and all other $a_{k}=0$
Then we just have to write
$$
\begin{align}
x(j\omega) = \sum_{k=-\infty}^{\infty} 2\pi a_{k} \delta\left( \omega-\underbrace{ \omega_{0}}_{ \frac{2\pi}{T} } k\right) \\
= 2\pi\underbrace{  \left( \frac{1}{2} \right) }_{ a_{1}  }\delta(\omega-\underbrace{ (1) }_{ k=1 }\omega_{0})+ 2\pi\underbrace{ \left( \frac{1}{2} \right) }_{ a_{-1}  }\delta(\omega-\underbrace{ (-1) }_{ -k }\omega_{0})
\end{align}
$$

The Fourier transform of a periodic signal is a train of impulses located at $k\omega_{0}$
The areas of these impulses are $2\pi a_{k}$.

$$
\begin{align}
x(j\omega) = \pi\delta(\omega-\omega_{0} ) + \pi\delta(\omega+\omega_{0})
\end{align}
$$

## Example
A periodic impulse train in the time, with a delta function at $0,T,2T,$ etc, but zero everywhere else. Not like discrete where it could be anything because we don't care - its zero. 

The period is $T$. 
$$
\begin{align}
a_{k} = \frac{1}{T}\int_{T}^{} x(t)e^{-jk\omega_{0}t}dt \\
= \frac{1}{T} \int_{-\frac{T}{2}}^{\frac{T}{2}} \delta(t)e^{-jk\omega_{0}t}dt \\
= \frac{1}{T} e^{-jk\omega_{0}(0)} = \frac{1}{T}
\end{align}
$$
so, $a_{k}=\frac{1}{T}$ for ALL $k$.

This makes
$$
\begin{align}
x(j\omega)= \mathscr{F }\left\{ x(t) \right\}  \\
= \sum_{k=-\infty}^{\infty} 2\pi a_{k} \delta\left( \omega-k\underbrace{ \omega_{0} }_{ \omega_{0}=\frac{2\pi}{T} } \right) \\
= \sum_{k=-\infty}^{\infty} \frac{2\pi}{T}\delta(\omega-k\omega_{0})
\end{align}
$$
This is a bunch of spikes that turn on at $\omega=\frac{2n\pi}{T}$ in the frequency domain. 

Note that in the time domain, as $T$ goes up the spikes go farther apart - but in the frequency domain, as $T$ increases the spikes get closer together!

## Properties of the Continuous Time Fourier Transform

### Linearity
If $x(t) \leftrightarrow  x(j\omega)$ and $y(t)\leftrightarrow y(j\omega)$
$$
\begin{align}
ax(t)+by(t) \leftrightarrow  ax(j\omega) + by(j\omega)
\end{align}
$$
Recall that $\cos(\omega t) = \frac{1}{2}(e^{j\omega_{0}t+e^{-j\omega_{0}t}})$
We derived that
$$
\begin{align}
e^{j\omega_{0}t} \leftrightarrow  2\pi\delta(\omega-\omega_{0}) \\
\text{ and } \\
e^{-j\omega t} \leftrightarrow  2\pi \delta(\omega_{\omega_{0}} )
\end{align}
$$
So we could have just broken up the cos into the $e^{j\omega t}$s and gotten the same result
$$
\begin{align}
\cos(\omega_{0}t) \leftrightarrow  \pi\delta(\omega+\omega_{0}) + \pi \delta(\omega-\omega_{0})
\end{align}
$$

### Time Shifting
if $x(t) \leftrightarrow x(j\omega)$
$x(t-t_{0})\leftrightarrow e^{-j\omega t_{0}}x(j\omega)$
Proof:
$$
\begin{align}
x(t) = \int_{\omega=-\infty}^{\infty} x(j\omega)e^{j\omega t}d\omega
\end{align}
$$
then
$$
\begin{align}
x(t-t_{0}) = \int_{\omega=-\infty}^{\infty} x(j\omega)e^{j\omega t-t_{0}}d\omega \\
x(t-t_{0}) = \int_{\omega=-\infty}^{\infty} (x(j\omega)e^{-j\omega t_{0}})e^{j\omega t}d\omega
\end{align}
$$
Which by definition is $\mathscr{F}\left\{ x(t-t_{0}) \right\}$.


If we can write some $f(t)$ in terms of $g(\omega)$ as
$$
\begin{align}
f(t) = \frac{1}{2\pi} \int_{\omega=-\infty}^{\infty} g(\omega)e^{j\omega t}d\omega 
\end{align}
$$
then $g(\omega)$ is $\mathscr{F}\left\{ f(t) \right\}$.


### Differentiation
if $x(t)\leftrightarrow x(j\omega)$
then
$$
\begin{align}
\frac{ d x(t)}{d t } \leftrightarrow  j\omega \,  x(j\omega)
\end{align}
$$

$x(t)=\frac{1}{2\pi}\int_{\omega=-\infty}^{\infty}x(j\omega)e^{j\omega t}d\omega$

Now we take the derivative
$$
\begin{align}
\frac{ d x(t)}{d t } = \frac{ d }{d t } \left\{  \frac{1}{2\pi}\int_{\omega=-\infty}^{\infty}x(j\omega)e^{j\omega t}d\omega\right\}  \\
= \frac{1}{2\pi} \int_{\omega=-\infty}^{\infty} x(j\omega) \frac{ d e^{j\omega t}}{d t } d\omega  \\
= \frac{1}{2\pi}\int_{\omega=-\omega}^{\infty} \underbrace{ j\omega x(j\omega) }_{ \mathscr{F} \left\{ \frac{ d x(t)}{d t }  \right\}  }\, \, e^{j\omega t}d\omega 
\end{align}
$$
Differentiation is like a high pass filter

### Convolution property
For LTI systems, where $x(t)\to \text{ LTI }\to y(t)$ 
where $y(t)= x(t)*h(t)=\int_{\tau=-\infty}^{\infty}x(\tau)h(t-\tau)d \tau$
What if we take $\mathscr{F}\left\{ \text{ this } \right\}$

 What if we can find  $x(j\omega)\to y(j\omega)$ without convolution?

$$
\begin{align}
y(j\omega) = \int_{t=-\infty}^{\infty} y(t)e^{-j\omega t}dt  \\
= \int_{t=-\infty}^{\infty} x(t)*h(t)e^{-j\omega t}dt \\
= \int_{t=-\infty}^{\infty} \left[ \int_{\tau=-\infty}^{\infty} x(\tau)h(t-\tau)d \tau \right]
\end{align}
$$
we can switch the order of integration
$$
\begin{align}
Y(j\omega) = \int_{\tau = -\infty}^{\infty} x(\tau) \bigg[ \int_{t=-\infty}^{\infty}h(t-\tau) e^{-j\omega t}dt  \bigg] d \tau
\end{align}
$$
We see that this inner integral part is the Fourier transform of $h(t-\tau)$ by definition.
We know from time shifting that $\mathscr{F}(h(t-\tau))=e^{-j\omega \tau}H(j\omega)$

We can plug that back in
$$
\begin{align}
Y(j\omega) = \int_{\tau=-\infty}^{\infty} x(\tau) e^{-j\omega \tau}H(j\omega)\Delta u \\
= H(j\omega)\int_{\tau=-\infty}^{\infty} x(\tau)e^{-j\omega \tau}d \tau \\
= H(j\omega)X(j\omega)
\end{align}
$$

WOOHOOO! 
A convolution in time domain is multiplication in frequency domain. 

$$
\begin{align}
Y(j\omega) = H(j\omega)X(j\omega) \\
y(t) = x(t)*h(t)
\end{align}
$$

Given any $x(t)$ and $h(t)$, we take the transform to get $H(j\omega)\text{ and } X(j\omega)$, multiply, and take the inverse. Nice.

## Example
take an LTI system
$$
\begin{align}
\ddot{y}(t) + 4 \dot{y}(t) + 3y(t) = \dot{x}(t)+2x(t)
\end{align}
$$
We take the Fourier of each side
$$
\begin{align}
\mathscr{F} \left\{ y(t) \right\}  = Y(j\omega) \\
\mathscr{F} \left\{ \dot{y}(t) \right\} = j\omega Y(j\omega) \\
\mathscr{F} \left\{ \ddot{y}(t) \right\} = (j\omega)^{2}Y(j\omega)
\end{align}
$$
So we can rewrite
$$
\begin{align}
(j\omega)^{2}Y(j\omega)+ 4j\omega Y(j\omega) + 3Y(j\omega) = j\omega X(j\omega)+2X(j\omega) \\
Y(j\omega) \bigg[ (j\omega)^{2}+4j\omega+3 \bigg] = x(j\omega)(j\omega+2)
\end{align}
$$
so 
$$
\begin{align}
H(j\omega) = \frac{Y(j\omega)}{H(j\omega)} = \frac{j\omega+2}{(j\omega)^{2}+4j\omega+3}
\end{align}
$$
And our Y is just
$$
\begin{align}
Y(j\omega) = H(j\omega)\underbrace{ X(j\omega) }_{ \mathscr{F} \left\{ x(t) \right\}  }
\end{align}
$$
