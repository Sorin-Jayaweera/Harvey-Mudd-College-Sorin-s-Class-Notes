$$
\begin{align}
\hat{P} \xrightarrow {\text{ position }} \frac{\hbar}{i} \frac{ \partial  }{ \partial x }   \\
\braket{ x | p } = N e^{\frac{i p x}{\hbar}} = \sqrt[]{ \frac{1}{2\pi \hbar} } e^{\frac{ipx}{\hbar}}
\end{align}
$$

Position:
$$
\begin{align}
 & \ket{x}  \\
\hat{x}\ket{x}  & = x\ket{x} \\
\ket{\psi} & = \int_{-\infty}^{\infty} dx \, \ket{x} \underbrace{ \braket{ x | \psi } }_{ \psi(x) } \\
 & = \int_{-\infty}^{\infty} dx \, \psi(x)\ket{x} \\  
\end{align}
$$
We have the exact same for momentum
$$
\begin{align}
 & \ket{p}  \\
 \hat{p}\ket{p}  & = p\ket{p}  \\
\ket{\psi }  & = \int_{-\infty}^{\infty} dp \, \ket{p}\underbrace{  \braket{ p| \psi }  }_{ \tilde{\psi(p)} } \\
\end{align}
$$

Note the all powerful identity operator
$$
\begin{align}
1 = \int_{-\infty}^{\infty} dp \,  \ket{p} \bra{p} 
\end{align}
$$


## Find N
![[20260309_114557.jpg|600]]

For the same $\ket{\psi}$ we can write in two different ways and get the Fourier transform pairs
![[20260309_114610.jpg|600]]

![[20260309_114942.jpg]]



## Free Particles
$v(x)=0$
$$
\begin{align}
\hat{H} = \frac{\hat{p}^{2}}{2m}+ \cancelto{ 0 }{ V(\hat{x}) }
\end{align}
$$
Time evolution is
$$
\begin{align}
\hat{U}(t)= e^{-i \hat{H} \frac{t}{\hbar}}
\end{align}
$$
If we knew the eigenstates, the exponential would be really easy. 