
In continuous time we summed over infinite basis functions, but in discrete we have a limited number N.

We can reconstruct a function from Fourier coefficients with
$$
\begin{align}
x[n] = \sum_{k=\left< N \right>  }^{} a_{k} e^{jk \hat{\omega_{0}}n}
\end{align}
$$
Or find the coefficients  as
$$
\begin{align}
a_{k} = \frac{1}{N}\sum_{n=\left< N \right>  }^{} x[n]e^{-jk \hat{\omega_{0}}n}
\end{align}
$$
As long as the range in the sum spans the full period. i.e. if N=5 then
$$
\begin{align}
\sum_{0}^{4} \text{ or } \sum_{10}^{14} etc
\end{align}
$$


We define the period as $N$ that satisfies
$$
\begin{align}
x[n] = x[n+N]
\end{align}
$$
$$
\begin{align}
\hat{\omega}_{0} = \frac{2\pi}{N}
\end{align}
$$
## Example 1
Lets do an example.
![[Pasted image 20250923100624.png]]

$N=4, \hat{\omega}_{0}=\frac{\pi}{2}$

Let's pick a naive range bc it doesn't matter
$$
\begin{align}
a_{k} = \frac{1}{4} \sum_{n=0}^{3} x[n] e^{-jk \hat{\omega_{0}}n} 
\end{align}
$$
We define 
$$
\begin{align}
a_{0} = \frac{1}{4} [x[0] e^{-j\underbrace{ (0) }_{ k }\hat{\omega_{0}}\underbrace{ (0) }_{ n }}] + \frac{1}{4}x[1]e^{-j(0)\hat{\omega_{0}}\underbrace{ (1) }_{ n }}+ \frac{1}{4}x[2]e^{-j(0)\hat{\omega_{0}}\underbrace{ (2) }_{ n }} \dots \\
a_{0} = \frac{1}{4}(24 + 8 + 12 + 16) = 15
\end{align}
$$
Now we can find 

$$
\begin{align}
a_{1} = \frac{1}{4} [x[0] e^{-j\underbrace{ (1) }_{ k }\hat{\omega_{0}}\underbrace{ (0) }_{ n }}] + \frac{1}{4}x[1]e^{-j(1)\hat{\omega_{0}}\underbrace{ (1) }_{ n }}+ \frac{1}{4}x[2]e^{-j(1)\hat{\omega_{0}}\underbrace{ (2) }_{ n }} \dots \\
a_{0} = \frac{1}{4}(24-8j-12+16j) = 3+2j
\end{align}
$$
$$
\begin{align}
a_{2}  = \frac{1}{4}[x[0] + x[1]e^{-j\pi}+x[2]e^{-2\pi j} + x[3]e^{-3\pi j}]  \\
= \frac{1}{4}(24-8+12-16) = 3
\end{align}
$$
$$
\begin{align}
a_{3} = \frac{1}{4}\left[ x_{0}+x[1]e^{\frac{-3\pi}{2}j} + x[2] e^{-3\pi j} + x[3]e^{\frac{-9\pi}{2}j} \right] \\
= \frac{1}{4}[24 + 8j - 12 - 16j] = 3-2j
\end{align}
$$

This gives us
$$
\begin{align}
\begin{bmatrix}
a_{0}  & =& 15 \\
a_{1} & =& 3+2j  \\
a_{2} & =& 3 \\
a_{3} & =& 3-2j
\end{bmatrix}
\end{align}
$$
Because it doesn't depend on what starting indices,  we have more Fourier coefficients (which don't contribute anything new)
$$
\begin{align}
a_{k}  & = a_{k+N}  \\
a_{k}  & = 0 \text{ otherwise }
\end{align}
$$
We can check that we'll recover our original signal
$$
\begin{align}
x[n]  & = \sum_{k=0}^{3} a_{k} e^{jk \hat{\omega_{0}}n} \\
 & = 15 e^{0} + 3.6e^{0.59j}e^{\frac{\pi}{2}j} + 3e^{\pi nj} + 3.6e^{-0.59j}e^{\frac{3\pi}{2}nj}
\end{align}
$$
We can simplify this with sin and cos
For example,
$$
\begin{align}
3e^{j\pi n} = \cos(\pi n) \cancelto{ 0 }{ + j\sin(\pi n) }
\end{align}
$$
also,
$$
\begin{align}
e^{\frac{3\pi}{2}n j } = e^{j(\frac{4\pi}{2}- \frac{\pi}{2})n}= e^{2\pi nj} e^{\frac{-j\pi}{2}n}= e^{\frac{-\pi}{2}nj}
\end{align}
$$
This just leaves the two gross terms
$$
\begin{align}
3.6e^{j(\frac{\pi}{2}n + 0.59)} + 3.6e^{-j(\frac{\pi}{2}n + 0.59)}
\end{align}
$$
which just looks like the identity
$$
\begin{align}
\cos(\theta) = \frac{1}{2} (e^{j\theta}+e^{-j\theta})
\end{align}
$$


## Example 2
Lets do another example

Lets take a simple thing
$$
\begin{align}
x[n] = \cos\left( \frac{\pi}{2}n \right)
\end{align}
$$
$N = 4$
$$
\begin{align}
x[n] = \frac{1}{2}[e^{j \frac{\pi}{2}n}+ e^{\frac{-j\pi}{2}n}]
\end{align}
$$
We can solve by inspection,
$$
\begin{align}
a_{1}= \frac{1}{2}, a_{-1} = \frac{1}{2} 
\end{align}
$$
Remember that the span is 4, so
$$
\begin{align}
a_{1}=a_{5}=a_{9} \dots\\
a_{-1}= a_{3}=a_{-5}\dots  
\end{align}
$$
