In CT, for periodic $x(t)$, you first need $a_{k}$ (The Fourier Series coefficient).

In DT, it will be the same - you need the Fourier coefficients for the transform. 

Lets assume some periodic $x[n]$
$$
\begin{align}
x[n] = \sum_{k= <n>}^{} a_{k} e^{jk \hat{\omega}_{0} n}
\end{align}
$$
(this is just the Fourier series).

If $x[n]$ is periodic and has a Fourier series representation in terms of $a_{k}$, then
$$
\begin{align}
X(e^{j \hat{\omega}}) = \sum_{k=-\infty}^{\infty} 2\pi a_{k} \delta\left( \hat{\omega}- \frac{2\pi}{N} \right)
\end{align}
$$
where $x[n]$ has period $N$.

This is an impulse train repeating forever.

Recall
$$
\begin{align}
e^{j \hat{\omega}'n}\leftrightarrow  \sum_{l=-\infty}^{\infty} 2\pi \delta( \hat{\omega} - \hat{\omega}'-2\pi l)
\end{align}
$$
What does this look like?

For $l=0$, we'll have $0* 2\pi\delta(\hat{\omega}-\hat{\omega}')$
For $l=1$, we'll have $1* 2\pi\delta(\hat{\omega}-\hat{\omega}')$
For $l=-1$, we'll have $-2\pi\delta(\hat{\omega}-\hat{\omega}')$
![[Pasted image 20251023094729.png|500]]

How is this useful?

## Example
Take $x[n]= \cos\left( \frac{\pi}{2}n \right)$, so $\hat{\omega}_{0}= \frac{\pi}{2}$, $N=4$.
We can write out Euler's identity

$$
\begin{align}
x[n] = \frac{1}{2} e^{j(1)\frac{\pi}{2}n} + \frac{1}{2}e^{j(-1)\frac{\pi}{2}n}
\end{align}
$$
This gives us $a_{1}=a_{-1}=\frac{1}{2}$.

The Fourier series expansion involves terms of the form $e^{j \hat{\omega}n}$.
for each $e^{j\text{ stuff }}$. For the $e^{1}$ term only, we can make an $X(j\omega)$ - we have $\pi$ high spikes at $-\frac{3\pi}{2},\frac{\pi}{2}, \frac{5\pi}{2},\dots$
For the $e^{-1}$ term, we have $\pi$ high spikes at $=\frac{5\pi}{2}, -\frac{\pi}{2}, \frac{3\pi}{2},\dots$

The two of them combine by just putting together their individual frequency components.

This gives us the Fourier transform for the periodic function as
$$
\begin{align}
X(e^{j\omega}) = \sum_{k=-\infty}^{\infty} 2\pi a_{k} \delta\left( \hat{\omega}-\frac{2\pi k}{N} \right)
\end{align}
$$

## Summary
If you have a periodic $x[n]$ and want the DTFT,
1) Take the Fourier series, find $a_{k}$
2) To make it "math":
$$
\begin{align}
x(e^{j \hat{\omega}}) = \sum_{k=-\infty}^{\infty} 2\pi a_{k} \delta\left( \hat{\omega}- \frac{2\pi}{N}k \right) 
\end{align}
$$
To make it "plot" (be lazy):
Multiply the $x$ ax is by $\frac{2\pi}{N}$ (or $\hat{\omega}_{0}$), and change the label to $\hat{\omega}$.
Turn the stems into arrows (continuous)
Multiply everything by $2\pi$.



### Properties of the Discrete Time Fourier Transform
1) Linearity
$$
\begin{align}
\text{ if } x[n]  & \leftrightarrow  X(e^{j\omega}) \\
y[n]  & \leftrightarrow  Y(e^{j\omega}) \\
a x[n] + by[n]  & = aX(e^{e^{j\omega}}) + bY(e^{j\omega})
\end{align}
$$
2) Time Shifting

$$
\begin{align}
x[n] \Leftrightarrow  X(e^{j\hat{\omega}}) \\
x[n-n_{0}] \leftrightarrow  e^{-j \hat{\omega}n_{0}}X(e^{j\hat{\omega}})
\end{align}
$$

3) Convolutions and Multiplication

What about
$$
\begin{align}
x[n] \to  (H[n])\to  y[n]= x[n]*h[n]
\end{align}
$$
The DTFT gets
$$
\begin{align}
X(e^{j\hat{\omega}})\to  H(e^{j\hat{\omega}})\to  Y(e^{j\hat{\omega}})
\end{align}
$$
What is $Y(e^{j\hat{\omega}})$?

$$
\begin{align}
Y(e^{j\hat{\omega}}) = \sum_{n=-\infty}^{\infty} y[n]e^{-j \hat{\omega}n} = \sum_{n=-\infty}^{\infty} (x[n]*h[n])e^{-j\hat{\omega}n}
\end{align}
$$
$$
\begin{align}
Y(e^{j\hat{\omega}}) = \sum_{n=-\infty}^{\infty} \left( \sum_{k=-\infty}^{\infty} x[k]h[n-k] \right) e^{-j \hat{\omega}n}
\end{align}
$$
We can switch the order of the sum
$$
\begin{align}
= \sum_{k=-\infty}^{\infty} x[k] \left( \sum_{n=-\infty}^{\infty} h[n-k]e^{-j \hat{\omega}n} \right)
\end{align}
$$
Remember:
$$
\begin{align}
h[n] \leftrightarrow    H(e^{j\omega}) \\
h[n-k] \leftrightarrow  e^{-j \hat{\omega}k}H(e^{j\hat{\omega}})
\end{align}
$$
We get
$$
\begin{align}
Y(e^{j\hat{\omega}}) = \sum_{k=-\infty}^{\infty} x[k]e^{-j \hat{\omega}k}H(e^{j\omega}) \\
= H(e^{j\hat{\omega}})\sum_{k=-\infty}^{\infty} x[k]e^{-j \hat{\omega}k}
\end{align}
$$
$$
\begin{align}
Y(e^{j\hat{\omega}})= H(e^{j\hat{\omega}})X(e^{j\hat{\omega}})
\end{align}
$$
This is the same as in continuous time!
$$
\begin{align}
H(e^{j\hat{\omega}}) = \frac{Y(e^{j\hat{\omega}})}{X(e^{j\hat{\omega}})}
\end{align}
$$




4) Multiplication Property

$$
\begin{align}
\text{ if  }x[n] \leftrightarrow  X(e^{j\hat{\omega}}) \\
y[n] \leftrightarrow  Y(e^{j\hat{\omega}})
\end{align}
$$
Then
$$
\begin{align}
x[n]y[n] \leftrightarrow   \frac{1}{2\pi} \int_{\theta= <2\pi>} Y(e^{j\theta})X(e^{j(\hat{\omega}-\theta)})d\theta 
\end{align}
$$

So if we have 
$$
\begin{align}
y[n] = \frac{1}{2\pi} \int_{2\pi}^{} Y(e^{j\hat{\omega}})e^{j\hat{\omega}n}d\hat{\omega}  \\
\end{align}
$$
then we also have
$$
\begin{align}
y[n] = \frac{1}{2\pi} \int_{2\pi}^{} X(e^{j\hat{\omega}})H(e^{j\hat{\omega}})e^{j\hat{\omega}n}d\hat{\omega}
\end{align}
$$


## Example
Lets take a difference equation
$$
\begin{align}
y[n] - \frac{1}{2}y[n-1] = x[n]
\end{align}
$$
The time shifting property takes
$$
\begin{align}
x[n-n_{0}] \leftrightarrow  e^{-j \hat{\omega}n_{0}}X(e^{j\hat{\omega}}) \\
\end{align}
$$
Taking the DTFT of the difference equation:
$$
\begin{align}
Y(e^{j\hat{\omega}}) - \frac{1}{2} e^{-j\hat{\omega}(1)}Y(e^{j\hat{\omega}}) = X(e^{j\hat{\omega}})
\end{align}
$$
Rearranging,
$$
\begin{align}
H(e^{j\hat{\omega}}) = \frac{Y(e^{j\hat{\omega}})}{X(e^{j\hat{\omega}})} = \frac{1}{1-\frac{1}{2}e^{-j\hat{\omega}}}
\end{align}
$$

## Example
If we had an input $x[n]= \left( \frac{1}{6} \right)^{n}u[n]$
We know
$$
\begin{align}
Y(e^{j\hat{\omega}}) = X(e^{j\hat{\omega}})H(e^{j\hat{\omega}})
\end{align}
$$
and we can find that $X(e^{j\hat{\omega}})=\frac{1}{1-\frac{1}{6}e^{-j\hat{\omega}}}$.
Therefore,
$$
\begin{align}
Y(e^{j\hat{\omega}}) = \frac{1}{1-\frac{1}{2}e^{-j\hat{\omega}}} \frac{1}{\left( 1-\frac{1}{6}e^{-j\hat{\omega}} \right)}
\end{align}
$$
We have two approaches from here. We could either use the raw integral, or we could expand and use transform pairs. First the easy way (pairs):
We can do partial fraction expansion here,
$$
\begin{align}
Y(e^{j\hat{\omega}}) = \frac{\frac{3}{2}}{\left( 1-\frac{1}{2}e^{-j\hat{\omega}} \right)} - \frac{\frac{1}{2}}{\left( 1-\frac{1}{6}e^{-j\hat{\omega}} \right)}
\end{align}
$$
This gives us
$$
\begin{align}
y[n] = \frac{3}{2} \left( \frac{1}{2} \right)^{n}u[n] - \frac{1}{2}\left( \frac{1}{6} \right)^{n} u[n]
\end{align}
$$

OR do the actual integral (annoying but general)
$$
\begin{align}
y[n] = \frac{1}{2\pi} \int_{2\pi}^{} Y(e^{j\hat{\omega}})e^{j\hat{\omega}n}d\hat{\omega}
\end{align}
$$


|        | Periodic          | Aperiodic OR Periodic |
| ------ | ----------------- | --------------------- |
| $x[n]$ | DT Fourier Series | DT Fourier Transform  |
| $x(t)$ | CT Fourier Series | CT Fourier Transform  |

