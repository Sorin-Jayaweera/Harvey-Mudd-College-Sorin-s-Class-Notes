## Matrix representations
We have representations of bras and kets in matrices, where you choose a coordinate axis. 

for instance, 
$$
\begin{align}
\ket{+x}  & \xrightarrow {\text{ x basis }}  \begin{pmatrix}
1 \\ 0
\end{pmatrix}     \\
\ket{+x} &  \xrightarrow {\text{ z basis }}   \sqrt[]{ \frac{1}{2} } \begin{pmatrix}
1\\1
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
\braket{ \phi | \psi } = \begin{pmatrix}
\phi_{1}^{*} & \phi_{2}^{*}
\end{pmatrix} \begin{pmatrix}
\psi_{1}\\\psi 2
\end{pmatrix} = \phi_{1}^{*}\psi_{1} + \phi_{2}^{*}\psi_{2}
\end{align}
$$


We have operators (i.e. rotate a thing with spin in magnetic fields). We can physically enact these operators.

An operator takes $\hat{R}(\theta \vec{n})\ket{+n}\to \ket{+m}$
$\hat{\text{ hat }}$ is reserved for operators. Unit vectors have $\vec{\text{ vec }}$.

## Rotation Operator
For instance, lets rotate a vector around the $\vec{j}$ axis by $\frac{\pi}{2}$ (z axis). This would take something along the $z$ direction down to the $x$ direction. 

$$
\begin{align}
\hat{R}\left( \frac{\pi}{2 } \vec{j}\right) \ket{+z} = \ket{+x}\\
\hat{R}\left( \frac{\pi}{2 } \vec{j}\right) \ket{-z} = \ket{-x} 
\end{align}
$$
What if we have a random ket?
$$
\begin{align}
\ket{\psi}   & = C_{+} \ket{+\vec{z}} + C_{-} \ket{-\vec{z}} \\
R\left(  \frac{\pi}{2} \vec{j} \right)\psi  & = C_{+} \ket{+\vec{x}} + C_{-}  \ket{-\vec{x}}  
\end{align}
$$
These operators have Eigenkets, i.e.
$R\left( \frac{\pi}{2} \vec{j} \right)\ket{+y}=e^{i \text{ phase }}\ket{+y}$
but the phase doesn't change the probability. 

## Adjoint Operator (don't forget bras)
### WRONG
$$
\begin{align}
\bra{+\vec{x}} = \bra{+\vec{z}} \hat{R}\left( \frac{\pi}{2}\vec{j} \right)
\end{align}
$$
This is wrong, because we need to hold
$$
\begin{align}
1 = \braket{ +x | +x }   & = \braket{ +z | \hat{R}\left( \frac{\pi}{2} \vec{j}\right) \hat{R}\left( \frac{\pi}{2}\vec{j} \right)|+\vec{z} }  \\
 & = \braket{ +\vec{z} | -\vec{z} }  \\
 & =0 
\end{align}
$$
So we need a new version of $\hat{R}$ called $\hat{R}^{\dagger}$.

$$
\begin{align}
\bra{+x}  & = \bra{+z} \hat{R}^{\dagger}\left( \frac{\pi}{2} \vec{j} \right)  \\
\braket{ +\vec{x} | +\vec{x} }   & = \underbrace{ 1 }_{ \text{ want } } = \bra{+\vec{z}} \underbrace{\hat{R}^{\dagger}\left( \frac{\pi}{2}\vec{j} \right) \hat{R}\left( \frac{\pi}{2}\vec{j} \right) }_{ \mathbf{\hat{I}}=1 }\ket{+\vec{z}}     \\
\hat{R}^{\dagger}(\theta \vec{n}) & = \hat{R}^{-1}(\theta \vec{n}) \\
\hat{R}^{\dagger}(\theta \vec{n})  & = \hat{R}^{-1}(\theta \vec{n})
\end{align}
$$
If $\vec{U}^{\dagger}=\vec{U}^{-1}$, or equivalently $\hat{U}^{\dagger}\hat{U}=1$, then $\hat{U}$ is "Unitary".

## Generators of Rotations

We have a Hermitian operator, where the conjugate transpose is the same as the thing itself, instead of its inverse.
$$
\begin{align}
\hat{J}_{z}^{\dagger} = \hat{J}_{z} 
\end{align}
$$
$$
\begin{align}
\hat{R}(d\phi \vec{k}) & = 1+ \hat{r}_{z} d\phi \\
 & = 1 - \frac{i}{\hbar} \hat{J}_{z} d\phi \\
 \hat{R}^{\dagger}(d\phi \vec{k}) & = 1 + \frac{i}{\hbar} \hat{J}_{z} ^{\dagger} d\phi
\end{align}
$$
$$
\begin{align}
\hat{R}^{\dagger}(d\phi \vec{k})\hat{R}(d\phi \vec{k})  & = \left( 1+ \frac{i}{\hbar}\hat{J}_{z}d\phi  \right) \left( 1 - \frac{i}{\hbar} \hat{J}_{z} d\phi \right) \\
1 & = 1 + \frac{i}{\hbar} (\hat{J}_{z}^{\dagger} - \hat{J}_{z} )d\phi + \underbrace{ \mathscr{O} (d\phi^{2}) }_{ \to  0 } \\
\hat{J}^{\dagger}_{z}  & = \hat{J}_{z} 
\end{align}
$$

The operator $\hat{J}z$ generates a rotation, because
$$
\begin{align}
\hat{R}(\phi \vec{k}) & = \lim_{ N \to \infty } \hat{R}\left( \frac{\phi}{N}\vec{k} \right)^{N} \\
 & = \left[ 1- \frac{i}{\hbar}\hat{J}_{z} \frac{\phi}{N} \right]^{N} \\
 & = e^{-\frac{1}{\hbar} \hat{J}_{z} \phi }
\end{align}
$$
This is like Noethers theorem - operators correspond to conservation laws. 

This is an angular momentum operator. 

If I want to translate a particle in space by some amount $a$, I would use the linear momentum generator
$$
\begin{align}
\hat{T}(a) = e^{- \frac{i}{\hbar} \hat{p}a  }
\end{align}
$$
Or if we wanted to time evolve something by a time $t$, we could use the energy operator:
$$
\begin{align}
\hat{U}(t) = e^{- \frac{i}{\hbar}\hat{H}t}
\end{align}
$$

The fact that $\hbar$ shows up is a consequence of these three places that we insert it. 

## Eigenstates and Eigenvalues

Lets go back to thinking about Eigenkets. 
For instance,
$$
\begin{align}
R(\phi \vec{k})\ket{+\vec{z}}  = e^{i\phi}\ket{+\vec{z}}  \\
R(\phi \vec{k})\ket{-\vec{z}} = e^{i\phi'}\ket{-\vec{z}}  \\
\end{align}
$$
Lets look at the rotation generator
$$
\begin{align}
\hat{R}(\phi \vec{k})\ket{+z}  = e^{-\frac{i}{\hbar} \hat{J}_{z} \phi}\ket{+z} 
\end{align}
$$
Because we have a matrix in the exponent, lets do a Taylor series thing
$$
\begin{align}
\left[ 1 - \frac{i}{\hbar} \hat{J}_{z} \phi + \frac{1}{2!}\left( - \frac{i}{\hbar} \hat{J}_{z} \phi \right)^{2} + \dots \right]
\end{align}
$$

$$
\begin{align}
\hat{J}_{z} \ket{+\vec{z}} = \text{ const } \ket{+\vec{z}}  \\
\hat{J}_{z} \ket{-\vec{z}} = \text{ const }' \ket{-\vec{z}}  
\end{align}
$$
Lets say we want to rotate some finite amount around $\ket{+x}$

$$
\begin{align}
\hat{R}(\phi \vec{k})\ket{+\vec{x}} \\
\hat{J}_{z}^{2} \ket{+z} = \left( \frac{\hbar}{2} \right)^{2} \ket{+\vec{z}} \\
\hat{J}_{z}^{n}\ket{+z} = \left( \frac{\hbar}{2} \right)^{n}\ket{+\vec{z}} \\
\hat{J}_{z}^{n}\ket{-z} = \left( \frac{\hbar}{2} \right)^{n}\ket{-\vec{z}} \\
\end{align}
$$
We can write the operator as the Taylor expansion of $e^{ - \frac{i}{\hbar}\hat{J}_{z}\phi}$

$$
\begin{align}
\hat{R}(\phi \vec{k})\ket{+z}  & = \left[ 1 - \frac{i}{\hbar}\hat{J}_{z} \phi + \frac{1}{2 }\left( \frac{i}{\hbar}\hat{J}_{z} \phi \right)^{2}+\dots \right] \\
 & = \left[ 1- \frac{i}{\hbar} \frac{\hbar}{2} \phi + \frac{1}{2} \left( \frac{i}{\hbar}\frac{\hbar}{2} \phi\right)^{2}+\dots \right] \\
 & = e^{ -i \frac{\phi}{2}} \ket{+\vec{z}} \\ 
\end{align}
$$
$$
\begin{align}
\hat{R}(\phi \vec{k})\ket{-\vec{z}}  & = e^{ i \frac{\phi}{2}}\ket{-\vec{z}} \\
\hat{R}(\phi \vec{k})\ket{+z} &  = \hat{R}\left( \sqrt[]{ \frac{1}{2} } \ket{+z} + \sqrt[]{ \frac{1}{2} } \ket{-\vec{z}}    \right)    \\
 & = \sqrt[]{ \frac{1}{2} } e^{-i \frac{\phi}{2} }\ket{+\vec{z}} + \sqrt[]{ \frac{1}{2} } e^{i\phi}\ket{-\vec{z}}  \\
 & = e^{-i \frac{\phi}{2}}\left[  \sqrt[]{ \frac{1}{2} } \ket{+z} + \sqrt[]{ \frac{1}{2 } } e^{i\phi}\ket{-z}   \right]
\end{align}
$$
So
$$
\begin{align}
\hat{J}_{z}\ket{+z}   & =+ \frac{\hbar}{2} \ket{+\vec{z}}\\
\hat{J}_{z}\ket{-z}   & =  - \frac{\hbar}{2} \ket{-\vec{z}}   
\end{align}
$$



