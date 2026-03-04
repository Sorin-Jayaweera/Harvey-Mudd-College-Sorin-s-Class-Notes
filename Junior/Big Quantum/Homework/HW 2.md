Collaborators: Annika Larson

![[Pasted image 20260202162016.png]]

The state $\ket{y}$ has the matrix representation in the z basis
$$
\begin{align}
\ket{\vec{y}}  & = \frac{1}{\sqrt[]{ 2 } }\begin{pmatrix}
1\\ i
\end{pmatrix} \\
\ket{-\vec{y}}  & =  \frac{1}{\sqrt[]{ 2 } }\begin{pmatrix}
1\\ -i
\end{pmatrix}
\end{align}
$$
Or in the $\ket{\vec{y}}$ basis, just the identities 
$$
\begin{align}
\ket{+y} & = \begin{pmatrix}
1\\0
\end{pmatrix} \\
\ket{-y}  & = \begin{pmatrix}
0\\1
\end{pmatrix}
\end{align}
$$

The rotator $\hat{J}_{z}$ in the $\ket{\vec{z}}$ basis is 
$$
\begin{align}
\begin{pmatrix}
\frac{\hbar}{2 } & 0 \\
0 & -\frac{\hbar}{2}
\end{pmatrix} \begin{pmatrix}
 \ket{+z}\\ \ket{-z}  
\end{pmatrix}
\end{align}
$$

We can project to the $\ket{\vec{y}}$ basis by using the rotation matrix
$$
\begin{align}
\mathbb{S}  & = \begin{pmatrix}
\braket{ +z | +y }  & \braket{ +z  | -y }  \\
\braket{ -z | +y }  & \braket{ -z | -y }  
\end{pmatrix} \\
 & = \frac{1}{\sqrt[]{ 2 } }\begin{bmatrix}
1 & 1 \\
i & -i
\end{bmatrix}
\end{align}
$$
We can now compute
$$
\begin{align}
J_{z} & \xrightarrow {S_{y} \text{ basis }} \frac{1}{2} \begin{bmatrix}
1 & -i \\
1 &  i \\ 
\end{bmatrix} \frac{\hbar}{2} \begin{bmatrix}
1 & 0 \\ 0  & -1
\end{bmatrix}\begin{bmatrix}
1 & 1 \\
i & -i
\end{bmatrix} \\
 & = \frac{\hbar}{4}\begin{bmatrix}
1 & -i \\ 1 & i
\end{bmatrix} \begin{bmatrix}
1 & 1 \\
-i & i
\end{bmatrix} \\
 & = \frac{\hbar}{4} \begin{bmatrix}
0 & 2 \\ 2 & 0
\end{bmatrix} \\
 & = \frac{\hbar}{2} \begin{bmatrix}
0 & 1\\1 & 0
\end{bmatrix}
\end{align}
$$

We can now evaluate $\left< S_{z} \right>$ for particles in the $\ket{-y}$ state as
$$
\begin{align}
\bra{-y} J_{z}\ket{-y}  & = [0 \,\, \,   1] \frac{\hbar}{2} \begin{bmatrix}
0 & 1 \\ 1 & 0
\end{bmatrix} \begin{bmatrix}
0\\ 1
\end{bmatrix}  \\
 & =[0\, \, \, 1] \frac{\hbar}{2} \begin{bmatrix}
1 \\ 0
\end{bmatrix} \\
 \left< S_{z}  \right> & =0
\end{align}
$$


![[Pasted image 20260202162024.png]]
We can take the vector $\ket{+z}$ to the $\ket{\vec{y}}$ basis with the $\mathbb{S}$ rotation matrix

$R\left( \frac{\pi}{2}j \right) = e^{-i \hat{J}_{y} \frac{\pi}{2 \hbar}}$

$$
\begin{align}
 \begin{bmatrix}
\braket{ +y | +z }  & \braket{ +y | -z}  \\
\braket{ -y | +z }  & \braket{ -y | -z }  
\end{bmatrix} \\
\end{align}
$$


$$
\begin{align}
\mathbb{S}  & = \frac{1}{\sqrt[]{ 2 } } \begin{bmatrix}
1 & -i \\
1 & i
\end{bmatrix}
\end{align}
$$

Note that $\mathbb{S}^{-1}=\mathbb{S}^{\dagger}$, so
$$
\begin{align}
\mathbb{S}^{-1} 
& = \frac{1}{\sqrt[]{ 2 } }\begin{bmatrix}
1 & 1 \\
i & -i
\end{bmatrix}
\end{align}
$$


We can now write the matrix from $\ket{+z}$ in the z basis to the $\ket{y}$ basis.


$$
\begin{align}
\ket{+z}_{y}  & = \frac{1}{\sqrt[]{ 2 } } \begin{bmatrix}
1 & -i \\ 1 & i
\end{bmatrix}  \begin{bmatrix}
1 \\0
\end{bmatrix}  \\
\ket{+z}_{y}  & =  \frac{1}{\sqrt[]{ 2 } }  \begin{bmatrix}
1 \\ 1
\end{bmatrix}
\end{align}
$$


We can also take the vector $\ket{+x}$ to the $\ket{\vec{y}}$ basis
$$
\begin{align}
\ket{+x} _{y}  & = \frac{1}{\sqrt[]{ 2 } }\frac{1}{\sqrt[]{ 2 } }\begin{bmatrix}
1 & -i \\ 1 & i
\end{bmatrix} \begin{bmatrix}
1 \\ 1
\end{bmatrix} \\
 & =\frac{1}{2} \begin{bmatrix}
1-i \\ 1+i
\end{bmatrix}
\end{align}
$$
We can now see how the $\hat{R}\left( \frac{\pi}{2}j \right)$ rotator acts, since this is now expressed in the Eigenbasis. 
We know that $\hat{J}_{y}\ket{\pm y}=\pm \frac{\hbar}{2} \ket{\pm y}$, which makes the matrix representation for the operator in the $S_{y}$ basis: 


$$
\begin{align}
\hat{J}_{y}  & \xrightarrow {S_{y} \text{ basis }}  \begin{pmatrix}
\bra{+y} \hat{J}_{y}  \ket{+y} & 
\bra{-y} \hat{J}_{y}  \ket{+y} \\
\bra{+y} \hat{J}_{y}  \ket{-y} & 
\bra{-y} \hat{J}_{y}  \ket{-y} 
\end{pmatrix}   \\
 & = \begin{pmatrix}
\frac{\hbar}{2} & 0 \\
0 & -\frac{\hbar}{2}
\end{pmatrix}
\end{align}
$$
$R\left( \frac{\pi}{2}j \right) = e^{-i \hat{J}_{y} \frac{\pi}{2 \hbar}}$, so this becomes

$$
\begin{align}
\hat{R}(\phi \hat{J})  & = \begin{pmatrix}
e^{\frac{-i\phi}{2}} & 0 \\ 0 & e^{\frac{i\phi}{2}}
\end{pmatrix} \\
\implies R\left( \frac{\pi}{2} \hat{J} \right) & =\begin{pmatrix}
e^{\frac{-i\pi}{4}} & 0 \\ 0 & e^{\frac{i\pi}{4}} \\
\end{pmatrix} \\
\end{align}
$$


We can now finally compute $\hat{R}\left( \frac{\pi}{2} \hat{J} \right)\ket{+z}$ nicely in the $\ket{y}$ basis
$$
\begin{align}
\ket{+z}_{y}  & =  \frac{1}{\sqrt[]{ 2 } }  \begin{bmatrix}
1 \\ 1
\end{bmatrix} \\
\hat{R}\left( \frac{\pi}{2 } \hat{J} \right) \ket{+z}_{y}  & = \frac{1}{2} \begin{pmatrix}
e^{\frac{-i\pi}{4}}  & 0 \\ 0  & e^{\frac{i\pi}{4}}
\end{pmatrix} \begin{bmatrix}
1\\1
\end{bmatrix} \\
 & =\frac{1}{2} \begin{bmatrix}
e^{\frac{-i\pi}{4}} \\ e^{\frac{i\pi}{4}}
\end{bmatrix} \\
 & =\frac{1}{2} \sqrt[]{ \frac{1}{2} } \begin{bmatrix}
1+i \\ 1-i
\end{bmatrix}
\end{align}
$$
We can see that this is the same as out $\ket{+x}_{y}$, so rotating $\ket{+z}$ by $\frac{\pi}{2}$ around the $\ket{\vec{y}}$ axis yields $\ket{x}$, as geometry demands. 



![[Pasted image 20260202162039.png]]
## A
$\text{ Prob (y) = }\left| \left( \frac{i}{\sqrt[]{ 3 }} \right)^{2} \right|$
more formally: $\left| \braket{ +y | \psi } \right|^{2}$ 
Which is $\frac{1}{3}$.
## B
We can write the general state of the photon in terms of the new axis of the polarizer
$$
\begin{align}
\ket{x'} & = \cos \phi \ket{x}+ \sin \phi \ket{y} \\
\ket{y'}  & = -\sin \phi \ket{x} + \cos \phi \ket{y} 
\end{align}
$$


This question reduces to the statement
$$
\begin{align}
\left| \braket{ y' | \psi }   \right|^{2}  & =\left| \left(  (-\sin \phi \bra{x} + \cos \phi \bra{y} )\left( \sqrt[]{ \frac{2}{3} } \ket{x} + \frac{i}{\sqrt[]{ 3 } }\ket{y}  \right)   \right) \right|^{2} \\
 & = \left| \left( -\sin \phi \sqrt[]{ \frac{2}{3} }  + \cos \phi    \frac{i}{\sqrt[]{ 3 } } \right) \right| ^{2} \\
 & \sin ^{2}\phi  \frac{2}{3} + \cos ^{2} \phi  \frac{1}{3}
\end{align}
$$


## C
The total angular momentum imparted per second  will be roughly 
$N_{L} \hbar - N_{R} \hbar$

We can find $N_{L}$ and $N_{R}$.
$N_{L}=N-N_{R}$

$$
\begin{align}
\ket{R}  & = \frac{1}{\sqrt[]{ 2 } }(\ket{x} +i \ket{y} ) \\
\ket{L}  & = \frac{1}{\sqrt[]{ 2 } }(\ket{x} -i\ket{y} ) 
\end{align}
$$
We know that 
$$
\begin{align}
\ket{\psi}   & = \sqrt[]{ \frac{2}{3} } \ket{x} + \frac{i}{\sqrt[]{ 3 } }\ket{y} 
\end{align}
$$
We can thus find 
$$
\begin{align}
\left| \braket{ R | \psi } \right| ^{2}  & = \left( \frac{1}{\sqrt[]{ 2 } }\left( \bra{x} -i \bra{y} \right)   \left(\sqrt[]{ \frac{2}{3} } \ket{x} + \frac{i}{\sqrt[]{ 3 } }\ket{y}  \right) \right)^{2} \\
	 & =\left( \frac{1}{\sqrt[]{ 2 } } \sqrt[]{ \frac{2}{3} } + \frac{1}{\sqrt[]{ 6 } }  \right)^{2}\\
	 & = \left( \frac{1}{\sqrt[]{ 6 } }(\sqrt[]{ 2 } + 1 ) \right)^{2} \\
	 & = \frac{1}{6}(3 +2\sqrt[]{ 2 } )
\end{align}
$$

This gives that there are $\sim0.97 N$ right circularly polarized photons, and $\sim0.03N$ Left circularly polarized. 

The momentum change per second would thus be $(0.97-0.03)N \hbar = 0.94N \hbar$

## D

Every calculation here uses the complex magnitude, so any $i$ factor cancels out with a $-i$ to be the same. We don't have any terms which would change with the overall phase difference between $1 \text{ and }  i$.  A,B, and C would have identical resulting probabilities.



![[Pasted image 20260202162054.png]]

result is counterintuitive, no sense classically. 
The probability of passing through the first polarizer from a state $\ket{+y}$ would be the same as the probability of passing from the first through the second, since we assume that all the offset angles are the exact same. Thus the chance of passing through $N$ polarizers is
$$
\begin{align}
\bigg(\braket{ y' | +y } \bigg)^{N}
\end{align}
$$
We can evaluate this initially in the $\ket{y}$ basis, and this assumes that each successive probability is in its own $y\underbrace{n' }_{ \text{ some number } }$ basis - i.e.  $\braket{ y'' | y' }, \braket{ y''' | y'' }$, where each has the same probability of occurrence as the previous event. 

$$
\begin{align}
 \bra{y'} = -\sin \theta \bra{x}  + \cos \theta \bra{y} 
\end{align}
$$
This means that 
$$
\begin{align}
\braket{ y' | y } =  \cos \frac{\phi}{N}
\end{align}
$$
So the chance of going through the series of polarizers is 
$$
\begin{align}
\cos ^{N} \frac{\phi}{N}
\end{align}
$$
For $\phi=\frac{\pi}{2}$,
$$
\begin{align}
\text{ Probability of passing } &   \\
 & = \lim_{ n \to \infty } \cos ^{N} \frac{\pi}{2N}
\end{align}
$$
To sketch the argument in words:
$\lim_{ N \to \infty } \frac{\pi}{2N} = 0$, and $\cos(0)=1$
So as $N\to \infty$, the probability of transmission through each successive filter approaches $1$. Thus, the probability through all filters approaches $1$.  

We can prove this by Taylor expanding and using the binomial theorem.
$$
\begin{align}
\cos ^{N} \frac{\pi}{2} = \left( \sum_{k=0}^{\infty} \frac{(-1)^{k}\left( \frac{\pi}{2} \right)^{2k}}{2k!} \right)^{N}
\end{align}
$$
If we only keep up to second order terms of $\cos$, this becomes
$$
\begin{align}
\cos ^{N}(x) \approx \left(  1 - \frac{x^{2}}{2} + \mathscr{O}(x^{3})  \right)^{N}
\end{align}
$$
We can simplify this with the binomial expansion

$$
\begin{align}
\lim_{ n \to \infty } \cos ^{n} \frac{\pi}{2n}   & \approx \lim_{ n \to \infty }  \left(1-  \frac{\pi^{2}}{4n^{2}} \right)^{N} \\ \\
 & = \lim_{ n \to \infty } 1 \cancelto{ 0 }{ + \frac{\pi^{2}}{4n^{2}} + } \cancelto{ 0 }{ \mathscr{O} \left( \left( \frac{\pi^{2}}{4n^{2}} \right)^{2} \right) } \\
 & = 1
\end{align}
$$
Thus, there is a 100% chance that a photon will pass through infinite polarizers that are offset by infinitely small angles all the way down to $\frac{\pi}{2}$.

$\braket{ x | y }=0$ means that a particle in state $y$ has no chance of being in state $x$. However, this isn't going between those two - it is between adjacent states of polarization $\braket{ y' | y }$, for which there is a finite chance. As $\theta\to 0$, $\cos\theta=1$.  




![[Pasted image 20260202162107.png]]
referencing pg 63 of Townsend

The initial state is $\ket{\psi} = \frac{1}{\sqrt[]{ 2 }} (\ket{x} + \ket{y})$
Light parallel to the x axis will pick up a phase $n_{x} \frac{\omega}{c} z$ traveling a distance $z$. 
in the y axis, $n_{y \frac{\omega}{c}}z$.

At 45 degrees, there is a phase difference $\left[ (n_{x}-n_{y}) \frac{\omega}{c} \right]z$ between $x$ and $y$.
If the phase difference is $\frac{\pi}{2}$, then circularly polarized light will be emitted. 

$\lambda= 5890 \dot{A}$.
$\omega=2\pi\nu= 2\pi\frac{c}{\lambda}$
$\frac{\omega}{c} = \frac{2\pi}{\lambda}$
Thus we can simplify
 $$
\begin{align}
 \theta & = \frac{[n_{y}-n_{x}]\omega}{c} z \\
 & = [-0.17] \frac{2\pi}{5890 \dot{A}} 100 \mu m \\
 & = -0.17 \cdot 2\pi \cdot 58.9 \\
\theta & = 62.9135
\end{align}
$$

This means that $\ket{\psi'}= \frac{1}{\sqrt[]{ 2 }}(\ket{x} + e^{62.9135} \ket{y})$
We know the state
$$
\begin{align}
\ket{R}  & = \frac{1}{\sqrt[]{ 2 } }(\ket{x} +i \ket{y} ) \\
\end{align}
$$
So we can find
$$
\begin{align}
\bra{R}  & = \frac{1}{\sqrt[]{ 2 } }(\bra{x} -   \bra{y} ) \\
\braket{ R | \psi' }^{2}  & = \left| \frac{1}{2} -\frac{1}{2}ie^{-63i}  \right|^{2}  \\
 & =\frac{1}{4} \left| 1 - ie^{-63i} \right|^{2} \\
 & = \frac{1}{4} \left| 1  +ie^{63i}-ie^{63i} \right| \\
 & = \frac{1}{4} \left| 1 + \sin 63 \right|  \text{ (radians) } \\
 & \approx 30 \% \text{ chance }
\end{align}
$$





