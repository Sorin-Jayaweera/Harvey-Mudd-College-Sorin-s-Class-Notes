There are three (main) types of operators:
## Unitary
These operators are reversable (time manipulation???), and correspond to things that you can physically do to spin $\frac{1}{2}$ systems. 
$$
\begin{align}
\hat{U}^{\dagger} \hat{U}=1 \implies \hat{U}^{-1}=\hat{U}^{\dagger}
\end{align}
$$
For example, $\hat{R}(\theta \vec{n}),\hat{T}(\vec{a}),\hat{U}(t)$. 

The preserve probabilities adding to 1 (aka, the norm of states)
$$
\begin{align}
\underbrace{ \bra{\psi} \hat{U}^{\dagger} }_{\text{ transpose of origional thing } }  & \underbrace{ \hat{U} \ket{\psi}  }_{ \text{ unitary operator on a state } } \\
 \bra{\psi} \hat{U}^{\dagger}  \hat{U} \ket{\psi}  &  =1
\end{align}
$$


## Projection Operators
These physically correspond to measurements - when you take a measurement, you have projected the state into that basis that you measured in.

This projects a state onto a new representation. Doing it again doesn't change anything, since it is now in that new representation - so things in that basis are Eigenstuff.

$$
\begin{align}
\hat{P}^{2} = \hat{P}
\end{align}
$$
For example,
$$
\begin{align}
\hat{P}_{\perp} = \ket{+\vec{z}} \bra{+\vec{z}}  
\end{align}
$$
This doesn't always preserve the norm. 

## Hermitian Operators
There are two forms: 
1) These are measurable quantities. What do they actually do to a quantum state? They take in $\ket{}s$ and give new $\ket{}s$, but what does that mean?
2) Generators for interesting unitary operators

$$
\begin{align}
\hat{A}^{\dagger}=\hat{A}
\end{align}
$$
For measurable quantities:
States of definite $A$ are eigenstates of $\hat{A}$ with some eigenvalue $a$ that is what you would measure for that state. 



The expected value of A is just
$$
\begin{align}
\left< A \right> = \bra{\psi} \hat{A}\ket{\psi} 
\end{align}
$$
This is just a weighted average $\sum_{i}^{}\text{ Prob}_{i} A_{i}$

$\hat{J}_{x}$ is generic angular momentum (total sometimes?).
$\hat{L}_{x}$ is orbital angular momentum.
$\hat{S}_{x}$ is spin angular momentum.
We also have 
$\hat{x}$ position
$\hat{p}$ momentum
$\hat{H}$ energy

As generators:

$$
\begin{align}
\hat{R}(\phi \vec{k}) & = e^{\frac{-i}{\hbar}\hat{J}_{z} \phi} \\
\hat{T}_{x}(a)  & = e^{\frac{-i}{\hbar}\hat{p}a} \\
\hat{U}(t)  & =e^{\frac{-i}{\hbar}\hat{H}t} 
\end{align}
$$


## The identity operator
$1= \sum_{k}^{} \ket{k}\bra{k}$
What does this get us? It'll be really important.
$$
\begin{align}
\bra{i} \hat{A} \left( \sum_{k}^{} \ket{k} \bra{k}  \right) \hat{B} \ket{j} 
\end{align}
$$
This is equivalent to
$$
\begin{align}
\sum_{k}^{} \bra{i} \hat{A}\ket{k} \bra{k} \hat{B} \ket{j} 
\end{align}
$$
Lets draw this in matrix form
![[Pasted image 20260202114722.png|500]]


## Change of Basis
(passive rotation: not changing the thing were measuring, changing the basis that we're representing it in).

We can do this by tossing in a bunch of identity operators. For example
$$
\begin{align}
1  & = \ket{+\vec{z}} \bra{+\vec{z}} + \ket{-\vec{z}} \bra{-\vec{z}}  \\
 & = \ket{+\vec{x}} \bra{+\vec{x}}+ \ket{-\vec{x}} \bra{-\vec{x}}  
\end{align}
$$
Lets call these the identity in the ___ basis, i.e. $\mathbb{1}_{x}$ or $\mathbb{1}_{z}$.

Lets take
$$
\begin{align}
\bra{\phi} \hat{A} \ket{\psi} 
\end{align}
$$
We can insert the $z$ identity

$$
\begin{align} 
\bra{\phi}  \mathbb{1}_{z} \hat{A}\mathbb{1}_{z}\ket{\psi}  & =(\braket{ \phi | +\vec{z} } \braket{ \phi | -\vec{z} }  )
\begin{pmatrix}
\bra{+\vec{z}} \hat{A}\ket{+\vec{z}}  & \bra{+\vec{z}} \hat{A}\ket{-\vec{z}} \\
\bra{-\vec{z}} \hat{A} \ket{\vec{z}} & \bra{-\vec{z}} \hat{A}\ket{-\vec{z}}   
\end{pmatrix}\begin{pmatrix}
\braket{ +\vec{z} | \psi } \\ \braket{ -\vec{z} | \psi } 
\end{pmatrix}
\end{align}
$$

This is just writing things in a new basis.
We could also do
$$
\begin{align}
\bra{\phi} \mathbb{1}_{x}\mathbb{1}_{z}\hat{A}\mathbb{1}_{z}\mathbb{1}_{x}\ket{\psi}     
\end{align}
$$
This will be a matrix-y thing.

## Photon Polarization

Photon polarization going through filters / mirrors have the same behaviors as the electrons for the Stern Gerlach. 
If we measure one basis, we can predict how much goes through a rotated polarizer
Rotation matrix
$$
\begin{align} \begin{pmatrix}
\ket{x'} \\ \ket{y'} 
\end{pmatrix}=
\begin{bmatrix}
\cos \phi & \sin \phi \\
-\sin \phi & \cos \phi
\end{bmatrix} \begin{pmatrix}
\ket{x} \\ \ket{y} 
\end{pmatrix}
\end{align}
$$

Is equivalent to 
$$
\begin{align}
\ket{x'}   & = \hat{R}(\phi \vec{k})\ket{x}  \\
\ket{y'}  & = \hat{R}(\phi \vec{k})\ket{y}  \\
\ket{R}  & = \sqrt[]{ \frac{1}{2} } \ket{x} + i\sqrt[]{ \frac{1}{2} } \ket{y} \\
\hat{R}(\phi \vec{k})\ket{R}  & = e^{-i\phi}\ket{R}  
\end{align}
$$

We also have an $\ket{L}$
$$
\begin{align}
\hat{J}_{z}\ket{R} = + \hbar \ket{R}
\hat{J}_{z}\ket{L} = - \hbar \ket{L}  
\end{align}
$$
R and L are circular polarizations of light.