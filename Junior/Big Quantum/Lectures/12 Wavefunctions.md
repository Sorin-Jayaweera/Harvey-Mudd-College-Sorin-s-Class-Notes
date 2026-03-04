We will now have position and momentum as the basis.

In spin, we had $\ket{+z},\ket{-z},\ket{-\vec{n}}$

Now we have
$$
\begin{align}
\ket{x} \text{ which returns something like } \ket{3.98 _{cm} } 
\end{align}
$$

We think of the thing in the ket as something definite. 

We have operators which act as a function, so
$$
\begin{align}
\hat{x} \ket{x} = x \ket{x} 
\end{align}
$$
Where the $\hat{x}$ position operator grabbing the $x$ position eigenvalue from the eigenket $\ket{x}$ returns the eigenvalue $x$. 

We'll have to be careful for superpositions though. In the spin state, we had
$$
\begin{align}
\ket{\psi} = a\ket{+\vec{z}} + b\ket{-\vec{z}} 
\end{align}
$$
Now, however, we have a continuous, infinite number of positions. 
$$
\begin{align}
\ket{\psi} = \int_{-\infty}^{\infty} dx\, \,  \psi(x)\ket{x} 
\end{align}
$$

Where $\psi(x)$ is just the weight that gets applied to each individual $\ket{x}$. 
It is an amplitude corresponding the state vector of each position.

We have the identity operator
$$
\begin{align}
1 = \int_{-\infty}^{\infty} dx \,  \ket{x} \bra{x} 
\end{align}
$$
For instance,
$$
\begin{align}
1\ket{\psi} = \int_{-\infty}^{\infty} dx \, \ket{x} \braket{ x|  \psi}  
\end{align}
$$
This is an amplitude for every $x$, $\braket{ x | \psi }=\psi(x)$.

also note that we have the Dirac delta
$$
\begin{align}
\braket{ x' | x } =0 \\
\braket{ x | x } =1
\end{align}
$$

We have the normalizaiton condition
$$
\begin{align}
1  & = \braket{ \psi | \psi } \\
 &  = \left( \int_{-\infty}^{\infty} dx' \braket{ \psi | x' } \bra{x}   \right)\left( \int_{-\infty}^{\infty} dx \braket{ \psi | x } \bra{x}   \right) \\
 & = \int_{-\infty}^{\infty} dx' \int_{-\infty}^{\infty} dx \underbrace{ \braket{ \psi | x' }  }_{ \psi ^{*}(x') } \underbrace{ \braket{ x' | x } }_{ \delta(x-x') } \underbrace{ \braket{ x | \psi }  }_{ \psi(x) } \\
 & = \int_{-\infty}^{\infty} dx \psi ^{*}(x)\psi(x)  \\
 & = \int_{-\infty}^{\infty} dx \, \left| \psi(x) \right| ^{2}
\end{align}
$$
This is just the regular normalization condition.


## Rotations and Translation

in spin, we had
$$
\begin{align}
\hat{R}(\phi \vec{k})\ket{\vec{n}} = \ket{\vec{n}'} 
\end{align}
$$
Now we have translation
$$
\begin{align}
\hat{T}(a)\ket{x} = \ket{x+a} 
\end{align}
$$

We have the Hermitian properties, i.e.
$$
\begin{align}
\hat{R}^{\dagger}\hat{R}=1 \\
\end{align}
$$
We want
$$
\begin{align}

\hat{T}^{\dagger}\hat{T}=1
\end{align}
$$
$$
\begin{align}
\hat{T}^{\dagger}(a) =\hat{T}^{-1}(a)=\hat{T}(-a)
\end{align}
$$


$$
\begin{align}
\psi(x) = \braket{ x | \psi } 
\end{align}
$$
For $\ket{\psi'}= \hat{T}(a)\ket{\psi}$, what is the wave function?
$$
\begin{align}
\braket{ x | \psi' }  & = \braket{ x} (\hat{T}(a)\ket{\psi} ) \\
 & = (\bra{x} \hat{T}(a))\ket{\psi}  \\
 & = \braket{x-a  |  \psi}  \\
 & = \psi(x-a)
\end{align}
$$

If we go to a ket $\ket{x+a}$ then we are grabbing the wave function given by $\psi(x-a)$ (because it's a function of x, not writing out the state).


## Commutation relations.
Translation doesn't depend on order, neither does momentum, but the two don't commute:
$$
\begin{align}
[\hat{x},\hat{p}_{x} ] = i\hbar
\end{align}
$$
We see this because
$$
\begin{align}
 & \hat{x} \hat{T}(\delta x)- \hat{T}(\delta x)\hat{x} \\
 & = \hat{x} \left[ 1- \frac{i}{\hbar}\hat{p}_{x} \delta x  \right] - \left[ 1- \frac{i}{\hbar}\hat{p}_{x}\delta x  \right] \hat{x} \\
 & = -\frac{i}{\hbar}(\hat{x}\hat{p}_{x} -\hat{p}_{x} \hat{x})\delta x \\
 & = -\frac{i}{\hbar}[\hat{x},\hat{p}_{x} ]\delta x
\end{align}
$$
If we apply both sides to some generic state $\psi$
$$
\begin{align}
(\hat{x}\hat{T}(\delta x)- \hat{T}(\delta x)\hat{x})\ket{\psi}  & = - \frac{i}{\hbar}[\hat{x},\hat{p}_{x} ]\delta x \ket{\psi} 
\end{align}
$$
When in doubt, insert the identity operator
$$
\begin{align}
1 = \int_{-\infty}^{\infty} dx \, \ket{x} \bra{x} 
\end{align}
$$
$$
\begin{align}
 & \, \, \, \, \, \, \, \, \, \int_{-\infty}^{\infty} dx \, (\hat{x}\hat{T}(\delta x)\ket{x} - \hat{T}(\delta x)\hat{x}\ket{x} )\braket{ x | \psi }  \\
 & =  \int_{-\infty}^{\infty} dx \, (\hat{x}\ket{x+\delta x} - \hat{T}(\delta x)x \ket{x} )\braket{ x | \psi }  \\
 & = \int_{-\infty}^{\infty} dx\,  ((x+\delta x )\ket{x+\delta x} - x\ket{x+\delta x} )\braket{ x | \psi }  \\
 & = \delta x\int_{-\infty}^{\infty} dx \,   \ket{x+\delta x} \braket{ x | \psi } 
\end{align}
$$
Because the approximation that $\hat{T}(\delta x)= 1- \frac{i}{\hbar}\hat{P}_{x}\delta x$ is already to first order (otherwise we would have to use the full series of $e^{\frac{-i}{\hbar}\hat{P}_{x}a}$), we only need to keep up to first order in the integral. Therefore, we get
$$
\begin{align}
 & \delta x \int_{-\infty}^{\infty} \ket{x} \braket{ x | \psi } + \mathscr{O}(\delta x^{2})  \\
 & = \delta_{x} \ket{\psi} + \mathscr{O} (\delta x^{2}) 
\end{align}
$$


## Hamiltonians
$$
\begin{align}
\hat{H}  & = -\hat{\vec{\mu}}\cdot \vec{B} \\
\hat{H}  & = \frac{\hat{p}^{2}_{x} }{2m} + V(\hat{x})
\end{align}
$$

We also have the momentum operator
$$
\begin{align}
\hat{P}_{x} \xrightarrow {\text{ x basis }} \frac{\hbar}{i} \frac{ \partial  }{ \partial x } 
\end{align}
$$
Which we called the $P_{op}$ in baby quantum.

$$
\begin{align} 
\ket{\psi} = \int_{-\infty}^{\infty} dx \, \psi(x)\ket{x} \to  \begin{pmatrix}
\vdots \\ \psi(x) \\ \vdots
\end{pmatrix}
\end{align}
$$
We have
$$
\begin{align}
\bra{\psi} \to  [\dots\,  \psi ^{*}(x)\, \dots]
\end{align}
$$
$$
\begin{align}
\hat{P}_{x} \xrightarrow {x} \begin{pmatrix}
\text{ mushy matrix }\\\text{ takes column vec } \\
\text{ to column vec }
\end{pmatrix}
\end{align}
$$
which gets some complex function. We'll talk about change of basis next time (the Fourier transform). 


$$
\begin{align}
\hat{T}(\delta x)\ket{\psi} &  = \int_{-\infty}^{\infty} dx' \ket{x'} \left( \braket{ x' | \psi } - \delta x \frac{ \partial  }{ \partial x' } \braket{ x' | \psi }  \right)+\dots \\
 & = \ket{\psi} - \delta x \int_{}^{} dx' \ket{x'} \frac{ \partial  }{ \partial x' } \braket{ x' | \psi } 
\end{align}
$$
We can write out with the generator way instead of applying the $\hat{T}$ to the kets,
$$
\begin{align}
\left( 1- \frac{i}{\hbar} \hat{p}_{x} \delta x \right)\ket{\psi}  \\
\end{align}
$$
Looking at first order, we see
$$
\begin{align}
\hat{P}_{x} \ket{\psi} = \frac{\hbar}{i}\int_{-\infty}^{\infty} dx' \ket{x'} \frac{ \partial  }{ \partial x' } \braket{ x' | \psi } 
\end{align}
$$
We can inner product it with a definite particular position
$$
\begin{align}
\bra{x}  & \left( \hat{P}_{x} \ket{\psi} = \frac{\hbar}{i}\int_{-\infty}^{\infty} dx' \ket{x'} \frac{ \partial  }{ \partial x' } \braket{ x' | \psi }  \right) \\
 & = \bra{x} \hat{P}_{x} \ket{\psi} = \frac{\hbar}{i} \int_{-\infty}^{\infty} dx' \braket{ x | x' } \frac{ \partial  }{ \partial x' } \braket{ x' | \psi }  \\
 & = \frac{\hbar}{i} \frac{ \partial  }{ \partial x } \braket{ x | \psi } 
\end{align}
$$
