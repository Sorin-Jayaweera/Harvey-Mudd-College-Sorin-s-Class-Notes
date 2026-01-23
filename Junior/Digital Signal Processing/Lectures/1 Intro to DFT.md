
Music Information Retrieval lies in the union of Music, Signal Processing, and Machine Learning. 

Course goals:
Discrete Fourier Transform, Short Time Fourier Transform, Hidden Markov models,  Probability and Random Variables, Dynamic Time Warping, phase vocoder, instantaneous frequency estimation, Nonnegative Matrix Factorization. 

## Discrete Fourier Transform

Set up Jupyter notebook, virtual environment. 


|            | periodic                                                              | aperiodic                                                                                          |
| ---------- | --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| continuous | Fourier Series                                                        | Fourier Transform                                                                                  |
| discrete   | Discrete Fourier Transform (FFT is an efficient implementation of it) | Discrete Time Fourier Transform (needs infinite memory because it is $-\infty \text{ to } \infty$) |

Polar to coordinate
$$
\begin{align}
re^{i\theta} = \sqrt[]{ x_{r}^{2}+ x_{i}^{2} } e^{i \tan ^{-1}(\frac{x_{i}}{x_{r}})} 
\end{align}
$$
### Definition of the Discrete Fourier Transform
$$
\boxed{
\begin{align}
 & \text{Time to Frequency: } & X[k] = \sum_{n=0}^{N-1} x[n]e^{-j \frac{2\pi}{N}k_{n}} \\
 & \text{Frequency to Time: } & x[n] = \frac{1}{N} \sum_{k=0}^{N-1} X[k]e^{j\frac{ 2\pi}{N}k_{n}}
\end{align}
}
$$


### Intuition to the Discrete Fourier Transform

We have 4 views of the DFT:

#### CS View

``` python
function x=dft(x)
```
You don't need to know the internals, just the inputs and outputs.
The inputs are a set of $N$ complex numbers,
$$
\begin{align}
 & \text{ input: } & x \in \mathbb{C}^{n} &  \leftarrow \text{ vector sequence of N complex numbers } \\
 & \text{ output: } & X \in \mathbb{C}^{n} & 
\end{align}
$$
The dimensionality coming in is the same as coming out.

For instance, numpy has

``` python
X = np.fft.fft(x)
x = np.fft.iffy(X)
```

#### Math View

We can write the DFT equations as a single matrix operation. 

we have
$$
\begin{align} \\
X[0]  & = x[0] e^{-j \frac{2\pi}{N} \cdot 0} + x[1]e^{-j \frac{2\pi}{N}\cdot0 } + x[2] e^{-j \frac{2\pi}{N}\cdot 0}\dots x[n-1]  \\ 
X[1]  & = x[0] e^{-j \frac{2\pi}{N} \cdot 0} + x[1]e^{-j \frac{2\pi}{N}\cdot 1 } + x[2] e^{-j \frac{2\pi}{N}\cdot 2}\dots \\
X[2]  & = x[0] e^{-j \frac{2\pi}{N} \cdot 0} + x[1]e^{-j \frac{2\pi}{N}\cdot 2 } + x[2] e^{-j \frac{2\pi}{N}\cdot 4}\dots x[n-1]  \\

\vdots & 
\end{align}
$$
We can write this as an $n\times n$ matrix times an $n\times 1$.

$$
\begin{align}
\underbrace{ \begin{bmatrix}
X[0] \\
X[1] \\
\vdots \\
x[n-1]
\end{bmatrix} }_{ \bar{X} } = \underbrace{ \begin{bmatrix}
e^{-j \frac{2\pi}{N}} & e^{-j \frac{2\pi}{N}} &  \dots  & e^{-j \frac{2\pi}{N}(N-1)} \\
e^{-j \frac{2\pi}{N}\cdot0} & e^{-j \frac{2\pi}{N}\cdot 1}  & \dots  & e^{-j \frac{2\pi}{N}(N-1)}  \\
\vdots \\
e^{-j \frac{2\pi}{N}} & e^{-j \frac{2\pi}{N}1 \cdot(N-1)} & \dots &  e^{-j \frac{2\pi}{N}(N-1)^{2} }
\end{bmatrix} }_{ \mathcal{A}  }\underbrace{  \begin{bmatrix}
x[0]\\ x[1] \\ \vdots \\ x[n-1]
\end{bmatrix} }_{ \bar{x} }
\end{align}
$$

Note that $\mathcal{A}$ is totally fixed for an input of size $N$. The DFT can be summarized by $\bar{X}=\mathcal{A}\bar{x}$.

Similarly, we have the inverse DFT
$$
\begin{align}
\frac{1}{N} \begin{bmatrix}
e^{j \frac{2\pi}{N} \cdot 0}  & e^{j \frac{2\pi}{N} \cdot 0} &  e^{j \frac{2\pi}{N} \cdot 0} &  \dots &  e^{j \frac{2\pi}{N}\cdot 0} \\
e^{j \frac{2\pi}{N}\cdot 0} & e^{j \frac{2\pi}{N} \cdot 1}  &  e^{j \frac{2\pi}{N} \cdot 2}  & \dots  &  e^{j \frac{2\pi}{N} \cdot (N-1)} \\
e^{j \frac{2\pi}{N}\cdot 0} & e^{j \frac{2\pi}{N} \cdot 2}  &  e^{j \frac{2\pi}{N} \cdot 3}  & \dots &   e^{j \frac{2\pi}{N} \cdot 2(N-1)} \\ \\
\vdots \\
e^{j \frac{2\pi}{N}\cdot 0} & e^{j \frac{2\pi}{N} \cdot (N-1)}  &  e^{j \frac{2\pi}{N} \cdot 2(N-1)}  & \dots &   e^{j \frac{2\pi}{N}  \cdot  (N-1)^{2}}
\end{bmatrix}
\end{align}
$$

We can see that 
$B = A^{H}$

$H$ means Hermitian, aka Conjugate Transpose. The transpose doesn't matter because of symmetry, but is a fact that exists. 

$$
\begin{align}
\bar{X} = \mathcal{A} \bar{x} \\
\bar{x} = \frac{1}{N} B \bar{X}  \\
\bar{X} = \frac{1}{N}B A \bar{x} \\
\frac{1}{N}BA = I \\
\frac{1}{N}B = A^{-1}
\end{align}
$$

The speed up from the FFT algorithm is because of how fast it is to compute matrix multiplication. 
#### Art View (math but pretty)

We can draw a picture for what is happening. In 2D we have the projections of a vector onto the basis functions. 

If we have a vector $X$ with basis functions $v_{1}\text{ and } v_{2}$, then we have
$x = av_{1}+bv_{2}$, where 

$a= \frac{V_{1}^{T}x}{v_{1}^{T}v_{1}}$  and $b= \frac{v_{2}^{T}x}{v_{2}^{T}v_{2}}$.


This is just taking the inner product. i.e.$v_{1}^{T}v_{1}$ is the Euclidian distance squared.
To handle complex numbers, instead of just taking the transpose we take the Conjugate transpose, aka Hermitian$^{\dagger}$ 

If you have a different basis, then you can still represent the vector by projecting it onto the new vectors. It is still the inner product normalized by the length of the vectors. 

The fact that in 2D the two basis vectors are orthogonal is pivotal - otherwise, there would be components that are double counted (projected onto both basis vectors). 

$X = av_{1}+bv_{2}$ is only true when the $v_{1}^{H}v_{2}=0$. There is still a way of representing the vector with non orthogonal basis vectors, but this specific approach doesn't change. 

In multiple dimensions, you can still do the decomposition in the exact same way.

Lets look at the DFT now.

$$
\begin{align}
\begin{bmatrix}
X[0] \\ X[1] \\ \vdots \\ X[n-1]
\end{bmatrix} = \begin{bmatrix}
-- v_{0}^{H} -- \\
- - v_{1}^{H} - - \\ 
\vdots  \\
- -v_{n-1}^{H} - - 
\end{bmatrix} \begin{bmatrix}
x[0] \\ x[1] \\ \vdots \\ x[n-1]
\end{bmatrix} \\
\end{align}
$$

$a = \frac{v_{0}^{H}x}{v_{0}^{H}v_{0}}$. If $v_{0} \text{ is all 1, then the product } v_{0}^{H}v_{0}=N$. 

We get
$$
\begin{align}
X[0] = v_{0}^{H}x = Na \\
X[1] = v_{1}^{H}x = Nb
\end{align}
$$
So the DFT coefficients are the length of the projection on a different vector set. Its a new coordinate system where the basis set is orthogonal, breaking down each point into an $N$ dimensional space. The length of each vector is the coefficient.
$$
\begin{align}
x = av_{0} + bv_{1} \\
= \frac{1}{N}(x[0]v_{0} + x[1]v_{1} + \dots)
\end{align}
$$
Are $v_{0},v_{1},\dots,v_{n-1}$ orthogonal? Yes! 

The DFT coefficients are projections onto the basis vectors of sine waves.  


#### Humanities View

Projecting a discrete, periodic signal onto discrete, complex exponentials.

* "Projecting onto": inner product 
	* $X[k]=\bar{v}_{k}^{H}\bar{x}$ is the projection onto $\bar{v}_{k}$.
* "discrete, periodic signal": 
	* DFT assumes $x[n]$ is $N-\text{ periodic }$.
* "discrete, complex exponentials"
	* $\bar{v}_{k}= \begin{bmatrix}e^{j \frac{e\pi}{N}0} \\ e^{j \frac{2\pi}{N}k} \\ e^{j \frac{2\pi}{N}}2k \\ \dots\\ e^\frac{j 2\pi}{N}(N-1)k\end{bmatrix}$

>[!abstract]+ Exersize:
> For N = 8, draw each element of $\bar{V}_{0}$ on the complex plane.
> Repeat for $\bar{v}_{1}, \bar{v}_{2}, \text{ and }  \bar{v}_{3}$
> We have a unit circle.
>  For k=0 All $N$ points are sitting at the same point, at $\phi=0$ on the unit circle
>  for K=1, the points are separated by $\frac{\pi}{4}$, and wind around the unit circle once.
>  for K=2, it winds around twice. K=3 jumps $\frac{3}{8}^{\text{ ths }}$ of the circle. At $k=4$ it jumps back and forth between $0$ and $\pi$, at $k=7$ we move $\frac{7}{8}^{ths}$ which is just *back once*, and at $k=8$ we don't move at all. 

The highest frequency is $\frac{N}{2}$. 



 
