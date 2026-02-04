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
## a
$\text{ Prop (y) = }\left| \left( \frac{i}{\sqrt[]{ 3 }} \right)^{2} \right|$
more formally: $\left| \braket{ +y | \psi } \right|^{2}$ 
Which is $\frac{1}{3}$.
## b
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
The total momentum imparted will be roughly 
$N_{L} \hbar - N_{R} \hbar$

We can find $N_{L}$ and $N_{R}$.
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
\left| \braket{ R | \psi } \right| ^{2}  & = \frac{1}{\sqrt[]{ 2 } }\left( \bra{x} -i \bra{y} \right)   \left(\sqrt[]{ \frac{2}{3} } \ket{x} + \frac{i}{\sqrt[]{ 3 } }\ket{y}  \right) \\
	 & =\frac{1}{\sqrt[]{ 2 } } \sqrt[]{ \frac{2}{3} } + \frac{1}{\sqrt[]{ 6 } } \\
	 & = \left( \frac{1}{\sqrt[]{ 6 } }(\sqrt[]{ 2 } + 1 ) \right)^{2} \\
	 & = \frac{1}{6}(5 +2\sqrt[]{ 2 } )

\end{align}
$$
# NOT YET GOOD



# KEEP GOING YUOU GOT THIS



![[Pasted image 20260202162054.png]]

result is counterintuitive, no sense classically. 



![[Pasted image 20260202162107.png]]

magic formula pg 63
There will be a phase difference $\frac{[n_{x}-n_{y}]\omega}{c} z$

