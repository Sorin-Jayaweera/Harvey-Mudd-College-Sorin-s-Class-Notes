ADCs have input Impedance that moves around, and if you have a high impedance input then things get messed up. Put a unity gain 3.3v op amp before ADCs to protect the ADC and to fix your signal. 


We can make a discrete Fourier transform by using the signal processing block from before - a bunch of shift registers, each multiplied by an $a_{k}$ and added. If we make the $a_{k}$ follow a sin wave of a particular frequency, then we find how much of that frequency is in $x$. If we make many of these auto correlators, then we have the DFT!

## Fast Fourier Transform
The DFT takes $N^{2}$ multipliers to impliment - 4 data points means 4 multipliers, and 4 frequencies to compare (so 16 multipliers).

The FFT is a mathematical trick
$$
\begin{align} \\
\text{ let } \omega = e^{\frac{-2\pi}{n}jkN}\\
x[n] = \sum_{n=0}^{N} x[n]w^{kn}\\
\end{align}
$$
We can break apart the summation into halfes, i.e.
$$
\begin{align}
\sum_{n=0}^{\frac{N-1}{2}} x[2n]w^{2nk} + \left( \sum_{n=0}^{\frac{N-1}{2}} x[2n+1]\omega^{2nk}  \right)\omega k 
\end{align}
$$
This is the Codey Tukey algorithm, or fast Fourier: Each of these little sums is faster to compute. Lets think of this as a matrix. $\omega$ is periodic over $\frac{N}{2}$ - 
$\omega^{\frac{N}{2}}=-\omega^{\frac{N}{2}}$

$$
\begin{align}
\begin{bmatrix}
X[0] \\
X[1] \\
X[2] \\
X[3] \\
\end{bmatrix} = \begin{bmatrix}
1 & 1 & 1 & 1 \\
1 & \omega & \omega^{2} & \omega^{3} \\
1 & \omega^{2} & \omega^{4} & \omega^{6} \\
1 & \omega^{3} & \omega^{6} & \omega^{9}
\end{bmatrix} \begin{bmatrix}
x[0] \\
x[1] \\
x[2] \\
x[3] \\
\end{bmatrix}
\end{align}
$$

This becomes the nicer object
$$
\begin{align}
\begin{bmatrix}
X[0] \\
X[1] \\
X[2] \\
X[3] \\
\end{bmatrix} = \begin{bmatrix}
1 & 1 & 1 & 1 \\
1 & \omega & \omega^{2} & \omega^{3} \\
1 & \omega^{2} & 1 & -1 \\
1 & \omega^{3} & -1& \omega
\end{bmatrix} \begin{bmatrix}
x[0] \\
x[1] \\
x[2] \\
x[3] \\
\end{bmatrix}
\end{align}
$$

The fundamental unit of the FFT is called the Butterfly Unit.

