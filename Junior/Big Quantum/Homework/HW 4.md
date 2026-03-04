Collab:
Annika L

![[Pasted image 20260213121720.png]]
The Hamiltonian in a magnetic field is
$$
\begin{align}
\bar{H} = \omega_{0} \hat{S}_{x}
\end{align}
$$
It travels for a time $t=\frac{l_{0}}{v_{0}}$. The field is $B_{0} \hat{\mathbf{i}}$.

We need to find the time evolution from $\hat{H}$ on $\ket{-z}$. We have the representation of $\ket{-z}$ in the $S_{x}$ basis as:
$$
\begin{align}
\ket{-z} = \frac{1}{\sqrt[]{ 2 } }(\ket{+x} - \ket{-x} ) \\
\bra{+z} = \frac{1}{\sqrt[]{ 2 } } (\bra{+x}+\bra{-x}   ) 
\end{align}
$$


So we have 
$$
\begin{align}
U(t)\ket{-z}  &  = \frac{1}{\sqrt[]{ 2 } }e^{-i\omega_{0} \hat{S}_{x} \frac{t}{\hbar}t}  (\ket{+x} - \ket{-x} ) \\
 & = \frac{1}{\sqrt[]{ 2 } }\left( e^{\frac{-i\omega_{0}}{2}t} \ket{+x} - e^{\frac{i\omega_{0}}{2}}\ket{-x} \right)  \\
\end{align}
$$


We can now find
$$
\begin{align}
\braket{ +z |\hat{H} |-z }  & = \frac{1}{2}\left( e^{\frac{-i\omega_{0}}{2}t}- e^{\frac{i\omega_{0}}{2}t} \right) \\
 & = i\sin\left( \frac{\omega_{0}}{2}t \right)
\end{align}
$$
We need
$$
\begin{align}
\left| \braket{ +z | \hat{H}|\ket{-z}  }  \right|^{2} = \frac{1}{4} \\
\sin ^{2}\left( \frac{\omega_{0}}{2}t \right) = \frac{1}{4} \\
\sin\left( \frac{\omega_{0}}{2}t \right) = \frac{1}{2} \\
\frac{\omega_{0}}{2}t = \frac{\pi}{6} \\
t = \frac{\pi}{3 \omega_{0}}
\end{align}
$$
$$
\begin{align}
t=\frac{l_{0}}{v_{0}}
\end{align}
$$
We therefore have
$$
\begin{align}
l_{0} = \frac{v_{0}\pi}{3\omega_{0}}
\end{align}
$$


![[Pasted image 20260213121729.png]]

# Advice from annika
## My advice is "I think i mighta done it wrong" but i have an answer

don't find $\bra{+y}$, plug in +z and -z in terms of -n. We already found z in terms of the N kets, find -z in a similar way. Everything is real

# I decided to take the L, the warning scares me <3





![[Pasted image 20260213121740.png]]
The Hamiltonian for magnetic field $B=B_{0}\mathbf{K}$ is
$$
\begin{align}
\hat{H} = \frac{ge}{2mc}\hat{S}_{z}B_{0} = \omega_{0} \hat{S}_{z} 
\end{align}
$$
We know the eigenvalues for the magnetic field Hamiltonian
$$
\begin{align}
\hat{H}\ket{+z}  & = \omega_{0} \hat{S}_{z}\ket{+z}   & & = \hbar \frac{\omega_{0}}{2} \ket{+z} \\
\hat{H}\ket{-z}   &   = \omega_{0} \hat{S}_{z} \ket{-z}  &  &   = -\hbar \frac{\omega_{0}}{2} \ket{-z} 
\end{align}
$$
We also know that in the $z$ basis, 
$$
\begin{align}
\ket{n} = \cos \frac{\theta}{2}\ket{+z}  + e^{i\phi} \sin \frac{\theta}{2} \ket{-z}  
\end{align}
$$
Here $\phi=0$.
Therefore, we have
$$
\begin{align}
\ket{n(t)}  & = e^{-i\frac{\omega_{0}}{2}t} \cos \frac{\theta}{2} \ket{+z} + e^{\frac{i\omega_{0}}{2}t}\sin \frac{\theta}{2}\ket{-z} 
\end{align}
$$
Now we have to write out the operators in the $\ket{z}$ basis.
### $\left< S_{z} \right>$
$$
\begin{align}
S_{z} = \frac{\hbar}{2} \begin{bmatrix}
1 & 0\\0 & -1
\end{bmatrix} 
\end{align}
$$

$$
\begin{align}
 & \bra{n(t)} S_{z}\ket{n(t)} \\
   & = \bra{n(t)} \left( \frac{\hbar}{2} e^{-i\omega_{0}t}\cos \frac{\theta}{2} \ket{ +z} - \frac{\hbar}{2}e^{\frac{i\omega_{0}}{2}t}\sin \frac{\theta}{2}  \ket{-z}  \right) \\
 \left< S_{z}  \right> & =\frac{\hbar}{2}\left( \cos ^{2}\left( \frac{\theta}{2} \right) - \sin ^{2} \left( \frac{\theta}{2} \right) \right)
\end{align}
$$


### $\left< S_{x} \right>$ and $\ket{S_{y}}$
We have to find this from the raising and lowering operators. 
$$
\begin{align}
S_{x} = \frac{\hat{S}_{+} +\hat{S}_{-} }{2}\\
S_{y} = \frac{\hat{S}_{+} - \hat{S}_{-} }{2i}
\end{align}
$$

We can find the time average of $\hat{S}_{+}$ and $\hat{S}_{-}$, then combine them to get the expectation values (that feels valid since we're just adding)

$$
\begin{align}
\hat{S}_{+} = \hbar \ket{+z} \bra{-z} \\
\hat{S}_{-} = \hbar \ket{-z} \bra{+z} \\
\end{align}
$$
$$
\begin{align}
\ket{n(t)}  & = e^{-i\frac{\omega_{0}}{2}t} \cos \frac{\theta}{2} \ket{+z} + e^{\frac{i\omega_{0}}{2}t}\sin \frac{\theta}{2}\ket{-z} 
\end{align}
$$
So we have
$$
\begin{align}
\left< \hat{S}_{+}  \right>  & = \bra{n} \hbar e^{\frac{i\omega_{0}}{2}t} \sin \frac{\theta}{2} \ket{ +z} \\
 & = \hbar e^{i\omega_{0} t} \cos \frac{\theta}{2} \sin \frac{\theta}{2} 
\end{align}
$$

We can do the same with $\hat{S}_{-}$:
$$
\begin{align}
\left< \hat{S}_{-}  \right> &  = \bra{n} \hbar e^{\frac{-i\omega_{0}}{2}}\cos \frac{\theta}{2} \ket{-z}  \\
 & = \hbar e^{-i\omega_{0}t}\cos \frac{\theta}{2} \sin \frac{\theta}{2}
\end{align}
$$
We can now find the last expectation values 
$$
\begin{align}
S_{x} &  = \frac{\hat{S}_{+} +\hat{S}_{-} }{2} \\
 & = \frac{\hbar}{2} \cos \frac{\theta}{2} \sin \frac{\theta}{2}(e^{i\omega_{0}t}+ e^{-i\omega_{0}t}) \\
 & = \hbar \cos \frac{\theta}{2} \sin \frac{\theta}{2} \cos(\omega_{0}t) \\

\end{align}
$$

And 
$$
\begin{align}
S_{y}  & = \frac{\hat{S}_{+} - \hat{S}_{-} }{2i} \\
 & = \hbar \cos \frac{\theta}{2} \sin \frac{\theta}{2} \sin(\omega_{0}t)
\end{align}
$$





![[Pasted image 20260213121752.png]]

We can write the $\hat{S}_{x}$ operator in the spin 1 $\ket{+z}$ basis
$$
\begin{align} 
\hat{S}_{x} = \frac{\hbar}{\sqrt[]{ 2 } }\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 0
\end{bmatrix}
\end{align}
$$

The eigenvalues are $\hbar,0,-\hbar$. We can now solve for the vectors, which I label in order as $\ket{1},\ket{2},\ket{3}$
$$
\begin{align}
\frac{1}{2  }\begin{bmatrix}
1\\\sqrt[]{ 2 } \\1
\end{bmatrix} ,
\frac{1}{\sqrt[]{ 2 } }\begin{bmatrix}
1\\0\\-1
\end{bmatrix},
\frac{1}{2 }\begin{bmatrix}
1\\-\sqrt[]{ 2 } \\1
\end{bmatrix}
\end{align}
$$

We can find the projection of $\ket{1,1}$ in the $S_{x}$ eigenstates, and do the same for the $\ket{1,-1}$ state. 
$$
\begin{align}
\bra{1,1}_{x}\ket{1,1}_{z} = \frac{1}{2} [1, \sqrt[]{ 2 } ,1]     \begin{bmatrix}
1\\0\\0
\end{bmatrix} = \frac{1}{2}
\end{align}
$$
Similarly, for others we are just keeping the first component and the amplitude. This gets us
$$
\begin{align}
\ket{1,1} _{z} = \frac{1}{2} \ket{1} + \frac{1}{\sqrt[]{ 2 } } \ket{2} + \frac{1}{2} \ket{3} 
\end{align}
$$
We can do the same for the final state, $\ket{1,-1}$
$$
\begin{align}
\ket{1,-1}_{z} = \frac{1}{2}\ket{1} - \frac{1}{\sqrt[]{ 2 }  }\ket{2} + \frac{1}{2}\ket{3} 
\end{align}
$$

We can now time evolve, with the individual eigenvalues for each basis ket
$$
\begin{align}
\ket{\psi(t)}_{z} =\hat{H}\ket{1,1} = e^{-i\omega_{0} t} \frac{1} {4}\begin{bmatrix} 1\\\sqrt[]{ 2}\\ -1
\end{bmatrix}+ \frac{1}{2 }e^{0} \begin{bmatrix}
1\\0\\-1
\end{bmatrix} + \frac{1}{4}e^{i\omega_{0}t} \begin{bmatrix}
1\\-\sqrt[]{ 2 } \\1
\end{bmatrix}
\end{align}
$$
This collapses down to
$$
\begin{align}
\ket{\psi(t)}_{z} = \begin{bmatrix}
\frac{e^{-i\omega_{0}t}}{4}+ \frac{1}{2}+ \frac{e^{i\omega_{0}t}}{4} \\ \, \sqrt[]{ 2 }  \frac{e^{-i\omega_{0}t}}{4} - \sqrt[]{ 2 } \frac{e^{i\omega_{0}t}}{4} \\
\frac{1}{4} ( -e^{-i\omega_{0}t}+e^{i\omega_{0}t})-\frac{1}{2}
\end{bmatrix}
\end{align}
$$
which further simplifies down to

$$
\begin{align}
\ket{\psi(t)}_{z} = \begin{bmatrix}
\frac{1}{2}(1 + \cos \omega_{0}t )   \\
\sqrt[]{ \frac{1}{2} }  (i\sin(\omega_{0}t) )  \\
\frac{1}{2}(\cos \omega_{0}t-1)
\end{bmatrix}  
\end{align}
$$


We are now asking the question
$$
\begin{align}
 & \left| \bra{1,-1} \hat{H} \ket{1,1} \right| ^{2} \\
 & = \left|[0,0,1]\begin{bmatrix}
\frac{1}{2}(1 + \cos \omega_{0}t )   \\
\sqrt[]{ \frac{1}{2} }  (i\sin(\omega_{0}t) )  \\
\frac{1}{2}(\cos \omega_{0}t-1)
\end{bmatrix}   \right| ^{2} \\
 & = \left| \frac{1}{2}(\cos \omega_{0}t-1) \right| ^{2} \\
 & = \frac{1}{4} (\cos ^{2}(\omega_{0}t)-2\cos \omega_{0}t +1 )
\end{align}
$$




![[Pasted image 20260213121800.png]]
First, we need to find the Eigenbasis for this system. Excluding the center row and column, the matrix looks symmetric as
$$
\begin{align}
\begin{bmatrix}
E_{0} & A \\
A & E_{0}
\end{bmatrix}
\end{align}
$$
This has the familiar eigenvectors 
$$
\begin{align}
\begin{pmatrix}
1\\1 
\end{pmatrix} \text{ and }   \begin{pmatrix}
1\\-1
\end{pmatrix}
\end{align}
$$
The third eigenvector has to be orthogonal as the set spans $\mathbb{R}^{3}$, so we have
$$
\begin{align}
\begin{pmatrix}
1\\0\\1
\end{pmatrix}, \begin{pmatrix}
0\\1\\0
\end{pmatrix}, \begin{pmatrix}
1\\0\\-1
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
H= \begin{bmatrix}
E_{0} & 0 & A \\
0 & E_{1} & 0 \\
A & 0 & E_{0}
\end{bmatrix}
\end{align}
$$

Applying each, we get the eigenvalues

$$
\begin{align}
(E_{0}+A )\begin{pmatrix}
1\\0\\1
\end{pmatrix}, E_{1} \begin{pmatrix}
0\\1\\0
\end{pmatrix},( E_{0}-A )\begin{pmatrix}
1\\0\\-1
\end{pmatrix}
\end{align}
$$


## A
$\ket{2}$ is an eigenstate because we have $\begin{pmatrix}0\\1\\0\end{pmatrix}$ already.

$$
\begin{align}
\psi(t) = e^{\frac{-i}{\hbar}E_{1}t} \ket{2} 
\end{align}
$$


## B
$$
\begin{align}
\ket{3} = \begin{pmatrix}
0\\0\\1
\end{pmatrix}
\end{align}
$$
This is the sum of the first and third eigenstates, so we have
$$
\begin{align}
\psi(t)  & = \frac{1}{2} \left( e^{\frac{-i}{\hbar} (E_{0}+A)t}(\ket{1} - \ket{3} ) - e^{\frac{-i}{\hbar}(E_{0}-A)t}(\ket{1} +\ket{3} ) \right) \\
 & =\frac{1}{2} e^{\frac{-i}{\hbar}E_{0}}  \left( e^{\frac{-i}{\hbar}At} (\ket{1}-\ket{3} ) - e^{\frac{i}{\hbar}At}(\ket{1} +\ket{3} ) \right) \\
 & = \frac{1}{2}e^{\frac{-i}{\hbar}E_{0}} \left( i\sin \frac{A}{\hbar } t\ket{1} +  \cos \frac{A}{\hbar }t\ket{3}  \right)
\end{align}
$$








# old work
We could use the equation
$$
\begin{align}
(E_{1}-\lambda)(E_{0}-\lambda)^{2} -A^{2}(E_{1}-\lambda) = 0 \\
\end{align}
$$
This has the solutions $E_{1}=\lambda$, and some quadratic thing. 
$$
\begin{align}
(E_{0}-\lambda)^{2} = A^{2} \\
E_{0}^{2} -2 E_{0} \lambda + \lambda^{2}- A^{2} = 0 \\
\lambda^{2} - 2E_{0} \lambda+(E_{0}^{2}-A^{2}) = 0 \\
\lambda= \sqrt[]{  } 
\end{align}
$$
 


# OLD WORK 2

given $\psi(0)=\ket{2}$, this becomes
$$
\begin{align}
 & \begin{pmatrix}
E_{0} & 0 & A \\
0 & E_{1} & 0 \\
A & 0 & E_{0}
\end{pmatrix} \begin{pmatrix}
0\\1\\0
\end{pmatrix} \\
 & = \begin{pmatrix}
0\\ E_{1}\\ 0
\end{pmatrix}
\end{align}
$$

This means that evolving in time is
$$
\begin{align}
\ket{\psi(t)} =e^{\frac{-i}{\hbar}E_{1}t} \ket{2} 
\end{align}
$$


## B
We get
$$
\begin{align}
H\ket{\psi}= \begin{pmatrix}
A\\0\\ E_{0}
\end{pmatrix}
\end{align}
$$

Therefore,
$$
\begin{align}
\ket{\psi(t)} = e^{-\frac{i}{\hbar}At}\ket{1} + e^{-\frac{i}{\hbar}E_{0}t}\ket{3}   
\end{align}
$$
