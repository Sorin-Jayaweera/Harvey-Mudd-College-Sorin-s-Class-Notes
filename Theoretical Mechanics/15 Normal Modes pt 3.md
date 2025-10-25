## Review
For any conservative system with $N$ degrees of freedom, we can write the Lagrangian as
$$
\begin{align}
\mathscr{L}= \frac{1}{2} \dot{\mathbb{X}}^{T}\mathbb{M}\dot{\mathbb{X}} - \frac{1}{2}\mathbb{X}^{T} \mathbb{K}\mathbb{X} 
\end{align}
$$
Where
![[Pasted image 20251022145020.png]]
where 
$$
\begin{align}
\mathbb{M}_{ij}  = \frac{ \partial T }{ \partial \dot{q}_{1} \partial \dot{q}_{j}  }  \bigg|_{\text{ equilibrium }}^{}   \\
\mathbb{K}_{ij}  = \frac{ \partial U }{ \partial q_{1} \partial q_{j}  }  \bigg|_{\text{ equilibrium}}^{}
\end{align}
$$

These matrices should be symmetric, since the derivatives commute. Note that we're expanding around the equilibrium when evaluating each of these partials. 

For example, the Lagrangian 
$$
\begin{align}
\mathscr{L}= \frac{M}{2}(\dot{x}_{1} ^{2}+\dot{x}_{3} ^{2}) + \frac{m}{2}\dot{x}_{2} ^{2} - \frac{k}{2}(x_{3}-x_{2})^{2}-\frac{k}{2}(x_{2}-x_{1})^{2}
\end{align}
$$

Here,
$$
\begin{align}
\mathbb{M} = \begin{bmatrix}
M & 0 & 0 \\
0 & m & 0 \\
0 & 0 & M
\end{bmatrix}
\end{align}
$$
and
$$
\begin{align}
\mathbb{K}= \begin{bmatrix}
k & -k & 0 \\
-k & 2k & -k \\
0 & -k & k
\end{bmatrix}
\end{align}
$$
Note that this is not $-2k$ in two of the entries - when we foil the (stuff)^2 we go really fast and combine terms, but here we're leaving them uncombined because its helpful to be symmetric. Upper triangular is technically right, but who cares. 

Our $\mathbb{X}=\begin{pmatrix}x_{1}\\x_{2}\\x_{3}\end{pmatrix}$.

## Lecture
We will prove that this matrix Lagrangian yields a differential equation which looks like
$$
\begin{align}
\mathbb{M}\ddot{\mathbb{X}}=\mathbb{K}\mathbb{X}
\end{align}
$$

In index notation,
$$
\begin{align}
\mathscr{L} = \frac{1}{2}\sum_{i,j}^{} \dot{q}_{i} M_{ij} \dot{q}_{j}  - \frac{1}{2}\sum_{i,j}^{} q_{i} K_{ij} q_{j} 
\end{align}
$$
We can write down the Euler Lagrange equation for the $n^{th}$ coordinate. Note that $M_{ij}\text{ and } K_{ij}$ are both scalers, not matrices - they are the values in the $ij^{th}$ entry of their respective $\mathbb{M},\mathbb{K}$.
$$
\begin{align} \\
\frac{d}{dt} \left( \frac{ \partial \mathscr{L} }{ \partial \dot{q}_{n}  }  \right) = \frac{ \partial \mathscr{L} }{ \partial q_{n}  } 
\end{align}
$$
The right side:
$$
\begin{align}
\frac{ \partial \mathscr{L} }{ \partial q_{n}  } = -\frac{1}{2}\sum_{i,j}^{} K_{ij} \frac{ \partial  }{ \partial q_{n}  } (q_{i}q_{j}  )
\end{align}
$$
We can break this out into two sums
$$
\begin{align}
-\frac{1}{2}\sum_{ij}^{} K_{ij} \left( \frac{ \partial q_{i}  }{ \partial q_{n}  } q_{j} +q_{i} \frac{ \partial q_{j}  }{ \partial q_{n}  }  \right)
\end{align}
$$
Note that this term inside acts like the Kronecker delta - its going to be a 1 if $q_{i}=q_{n}$, and $0$ otherwise. 
This isolates out terms where $i=n$ or $j=n$. We have
$$
\begin{align}
-\frac{1}{2}\sum_{ij}^{} K_{ij} \left( \frac{ \partial q_{i}  }{ \partial q_{n}  } q_{j} \right) -\frac{1}{2} \sum_{ij}^{} \left( q_{i} \frac{ \partial q_{j}  }{ \partial q_{n}  }  \right)
\end{align}
$$
Which becomes
$$
\begin{align}
-\frac{1}{2} \sum_{ij}^{} K_{ij} \delta_{in}q_{j} - \frac{1}{2} \sum_{ij}^{} K_{ij} \delta_{jn} q_{i}  
\end{align}
$$

This gives us only the terms where $i=n$ or $j=n$.
$$
\begin{align}
-\frac{1}{2} \sum_{j}^{} K_{nj} q_{j} - \frac{1}{2} \sum_{i}^{} k_{in} q_{i}  
\end{align}
$$
(side note - this is symmetric because we have a symmetric matrix! One we're summing along rows, another along columns).

Because $K_{nj}=K_{jn}$, and because our labeling is arbitrary, we can just write this out
$$
\begin{align}
-\frac{1}{2}\sum_{j}^{} K_{nj} q_{j} -\frac{1}{2}\sum_{j}^{} k_{jn} q_{j}   \\
=-\frac{1}{2}\sum_{j}^{} K_{nj} q_{j} -\frac{1}{2}\sum_{j}^{} k_{nj} q_{j} \\
= - \sum_{j}^{} K_{nj} q_{j} 
\end{align}
$$
Remember, we can write out 
$$
\begin{align}
\mathbb{K}= \begin{bmatrix}
K_{11} & K_{1,2} & K_{1,3} \\
\vdots & \ddots & \vdots \\
K_{3,1}  & \dots & K_{3,3}    
\end{bmatrix}
\end{align}
$$
and
$$
\begin{align}
\mathbb{X} = \begin{pmatrix}
q_{1} \\ q_{2} \\ q_{3} 
\end{pmatrix}
\end{align}
$$

This means that the nth entry in our Lagrange equation will have a right side that looks like
$$
\begin{align}
(\mathbb{K}\mathbb{X})_{n} 
\end{align}
$$
(the nth entry down of this)

The left side of the Euler Lagrange equation is
$$
\begin{align}
\frac{ \partial \mathscr{L} }{ \partial \dot{q}_{n}  } = \sum_{j}^{} M_{n,j} \dot{q}_{j} = (\mathbb{M} \ddot{\mathbb{X}})_{n}  
\end{align}
$$

We now have a **generalized eigenvalue problem.** 

The strategy is similar to before - we'll move to complex variables, and guess that $\mathbb{Z}(t)$ looks like $\mathbb{Z}_{0}e^{i\omega t}$.

Lets see what parts are the same, and which are unique:

$$
\begin{align} 
\mathbb{M}\mathbb{Z}_{0} (-\omega^{2})e^{i\omega t}= -\mathbb{K}\mathbb{Z}_{0} e^{i\omega t} \\
(\mathbb{K}-\omega^{2}\mathbb{M})\mathbb{Z}_{0} =0 \\
\det{(\mathbb{K}-\omega^{2}\mathbb{M})} =0
\end{align}
$$
We can solve for the eigenvalues, and then get the corresponding eigen vectors that are the normal modes for our system, and then write a general solution as a sum over all the eigenmodes. 

We can show that the eigenvalues $\omega^{2}$ must be real and positive (no imaginary $\omega$), and that the eigenvectors are orthogonal, although with a slightly different definition of the inner product.
$$
\begin{align}
 \mathbb{Z}_{0} ^{(i)^{T} } \mathbb{M} \mathbb{Z}_{0} ^{(j)}  =0 \text{ (if i } \neq  \text{ j) }
\end{align}
$$



We can always write our general solution
$$
\begin{align}
\mathbb{Z}(t)= \sum_{i=1}^{N} C_{i}  \mathbb{Z}_{0} ^{i}e^{i\omega t}
\end{align}
$$
Where
* $N$ is number of of degrees of freedom, which is the same as the number of normal modes,
 * $C_{i}$ is the complex amplitude of mode i, amplitude and phase.
 * $\mathbb{Z}_{0}$ is the eigenvector that tells you how much of mode $i$ is in each $q_{i}$ (i.e. $\begin{pmatrix}1\\0\\-1\end{pmatrix}$)
 We are adding the contribution from all normal modes to all variables to find how they evolve over time. 

