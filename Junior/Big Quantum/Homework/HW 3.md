![[Pasted image 20260210202430.png]]


In the spin $J_{z}$ spin $\frac{1}{2}$ basis, we can find the representation of $\hat{J}_{+}$ and $\hat{J}_{-}$, then use the fact that 
$$
\begin{align}
\hat{S}_{x} = \frac{\hat{J}_{+}+ \hat{J}_{-}  }{2} \\
\hat{S}_{y} = \frac{\hat{J}_{+}- \hat{J}_{-}  }{2i} \\
 
\end{align}
$$
$$
\begin{align}
S_{z} = \frac{\hbar}{2} \begin{pmatrix}
1  & 0\\ 0 & -1
\end{pmatrix} 
\end{align}
$$
The basis states are 
$\ket{\frac{1}{2},-\frac{1}{2}}$ which I write as $\begin{pmatrix}0 \\ 1\end{pmatrix}$ 
and 
$\ket{\frac{1}{2},\frac{1}{2}}$ which I write as $\begin{pmatrix}1\\0\end{pmatrix}$

$$
\begin{align}
 & \hat{J}_{+}\ket{\frac{1}{2}, \frac{1}{2}}  & & =0  \\
 & \hat{J}_{+}\ket{\frac{1}{2},-\frac{1}{2}}   & & = \hbar\sqrt[]{j(j+1)- m(m+  1)  } \ket{\frac{1}{2}, \frac{1}{2}}    \\
  &  & & = \hbar \sqrt[]{ \frac{1}{2} \frac{3}{2} + \frac{1}{2}\left( \frac{1}{2} \right)} \ket{\frac{1}{2},\frac{1}{2}} \\
 & &  &  = \hbar   
\end{align}
$$

We can now find the matrix for $\hat{J}_{+}$ as
$$
\begin{align}
\hat{J}_{+}= \hbar \begin{bmatrix}
0 & 1 \\
0 & 0
\end{bmatrix}
\end{align}
$$
This gives $\hat{J}_{-}$ as 
$$
\begin{align}
\hat{J}_{-} = \hbar \begin{bmatrix}
0 & 0 \\
1 & 0
\end{bmatrix}
\end{align}
$$

$$
\begin{align}
\hat{S}_{x} &  = \frac{\hat{J}_{+}+ \hat{J}_{-}  }{2}  \\
 & = \frac{\hbar}{2} \begin{bmatrix}
0 & 1\\1 & 0
\end{bmatrix} \\
\hat{S}_{y}  & = \frac{\hat{J}_{+}- \hat{J}_{-}  }{2i} \\
 & = \frac{\hbar}{2}\begin{bmatrix}
0 & -i \\
i & 0
\end{bmatrix}
\end{align}
$$

The three spin matrices are mutually orthogonal, so we can take the dot product by simply separating out and adding terms

$$
\begin{align}
\hat{S}_{z}  & = \frac{\hbar}{2} \begin{pmatrix}
1 & 0 \\ 0  & -1
\end{pmatrix}  \\
\hat{S}_{x} &  = \frac{\hbar}{2} \begin{pmatrix}
0 & 1\\ 1 & 0
\end{pmatrix} \\
\hat{S}_{y}  & = \frac{\hbar}{2} \begin{pmatrix}
0 & -i\\i & 0
\end{pmatrix}  
\end{align}
$$
![[Pasted image 20260211090631.png]]
$$
\begin{align}
\hat{S}_{x}\hat{i}\cdot n  & = \sin\theta \cos \phi \frac{ \hbar}{2} \begin{pmatrix}
 0 & 1 \\ 1 & 0
\end{pmatrix}  \\
\hat{S}_{y} \hat{j} \cdot n  & = \sin\theta \sin\phi \frac{ \hbar}{2} \begin{pmatrix}
0 & -i \\ i & 0
\end{pmatrix} \\
\hat{S}_{z} \hat{k} \cdot n  & = \frac{\hbar}{2} \cos \theta  \begin{pmatrix}
1 & 0 \\ 0 & -1
\end{pmatrix}
\end{align}
$$

Eigenstates of $\hat{S}$ satisfy
$$
\begin{align}
\hat{S}\vec{n}= s \vec{n}
\end{align}
$$

So the eigenvalue problem is
$$
\begin{align}
\frac{\hbar}{2} \bigg[ \begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix} \sin\theta \cos \phi + \begin{pmatrix}
0 & -i \\ i & 0
\end{pmatrix} \sin\theta \sin \phi + \begin{pmatrix}
1 & 0\\0 & -1
\end{pmatrix} \cos \theta\bigg] \begin{pmatrix}
\braket{ +z | +n } \\ \braket{ -z | +n } 
\end{pmatrix}  = \frac{\hbar}{2}n  \begin{pmatrix}
\braket{ +z | +n } \\ \braket{ -z | +n } 
\end{pmatrix} 
\end{align}
$$


We can simplify this monstrous equation
$$
\begin{align}
 \begin{pmatrix}
\cos\theta & \sin\theta \cos \phi - i \sin\theta \sin \phi \\
 \sin\theta \cos \phi + i \sin\theta \sin \phi&- \cos \theta
\end{pmatrix} \begin{pmatrix}
\braket{ +z | +n } \\ \braket{ -z | +n } 
\end{pmatrix}  & = n \begin{pmatrix}
\braket{ +z | +n } \\ \braket{ -z | +n } 
\end{pmatrix}  \\
\begin{pmatrix}
\cos \theta - n &  \sin\theta \cos \phi - i \sin \theta \sin \phi \\
\sin \theta \cos \phi + i \sin \theta \sin \phi & -\cos \theta - n
\end{pmatrix}\begin{pmatrix}
\braket{ +z | +n } \\ \braket{ -z | +n } 
\end{pmatrix}   & = 0 \\
\begin{pmatrix}
\cos\theta-n & \sin\theta(\cos \phi-i\sin \phi) \\
\sin\theta(\cos \phi+i\sin \phi) & -\cos\theta-n 
\end{pmatrix} & =0 \\
\begin{pmatrix}
\cos\theta-n & \sin \phi e^{-i\phi} \\
\sin\theta e^{i\phi} & -\cos\theta-n 
\end{pmatrix} & =0
\end{align}
$$


This can be solved by setting the determinant to zero.

We have
$$
\begin{align}
(\cos\theta-n)(-\cos\theta-n)-\sin ^{2}\theta = 0 \\
-\cos ^{2}\theta - \cos \theta n+\cos\theta n + n^{2} - \sin ^{2} \theta= 0 \\
-\cos ^{2} \theta + n^{2} - \sin ^{2} \theta = 0 \\
-(\cos\theta ^{2}+\sin\theta ^{2}) + n^{2} = 0 \\
n^{2} = 1 \\
n = \pm 1 
\end{align}
$$
We can plug this eigenvalue to find the eigenstates.

$$
\begin{align} \\
\begin{pmatrix}
\cos\theta-n & \sin \phi e^{-i\phi} \\
\sin\theta e^{i\phi} & -\cos\theta-n 
\end{pmatrix}  & = 0 \\
\end{align}
$$

### $n = 1$
$$
\begin{align}
\begin{pmatrix}
\cos\theta - 1  &  \sin\theta e^{-i\phi} \\
\sin\theta e^{i\phi} & -\cos\theta-1
\end{pmatrix} \begin{pmatrix}
\braket{ +z | +n }  \\
\braket{ -z | +n } 
\end{pmatrix} = \vec{0} \\
\end{align}
$$
We have two equations from this
$$
\begin{align}
(\cos\theta -1) \braket{ +z | +n   } + \sin\theta e^{-i\phi} \braket{ -z | +n }  & = 0 \\
\sin\theta e^{i\phi}\braket{ +z | +n }  - (\cos\theta-1) \braket{ -z | +n }  & = 0 
\end{align}
$$
These two equations provide the same information, I'll use the first arbitrarily.
We can use the half angle identities to simplify.

$$
\begin{align}
\sin\left( \frac{\theta}{2} \right) = \sqrt[]{ \frac{1-\cos\theta}{2} } \\
\to   1-\cos\theta = 2\sin ^{2} \frac{\theta}{2} \\
\to   \cos\theta-1 = -2 \sin ^{2} \frac{\theta}{2}
\end{align}
$$
This becomes
$$
\begin{align}
-2 \sin ^{2} \frac{\theta}{2} \braket{ +z | +n } =- \sin\theta e^{i\phi} \braket{ -z | +n } 
\end{align}
$$
We also have the trig identity (RAAGH THIS TOOK SO LONG TO REALIZE AAAA, WHOOPS)
$$
\begin{align}
\sin \theta = 2 \sin \frac{\theta}{2} \cos \frac{\theta}{2}
\end{align}
$$
$$
\begin{align}
-2 \sin ^{2} \frac{\theta}{2} \braket{ +z | +n } =- 2 \sin \frac{\theta}{2} \cos \frac{\theta}{2}e^{i\phi} \braket{ -z | +n } 
\end{align}
$$

$$
\begin{align} 
 \braket{ +z | +n }  & = \frac{\cos \frac{\theta}{2}}{\sin \frac{\theta}{2}} e^{i\phi} \braket{ -z |+n  }   \\
{\tan \frac{\theta}{2}} e^{-i\phi}  \braket{ +z | +n }  & = \braket{ -z | +n } 
\end{align}
$$

We have to satisfy the condition that
$$
\begin{align}
\left| \braket{ +z | +n } \right| ^{2*} + \left| \braket{ -z | +n } \right| ^{2*} = 1
\end{align}
$$
so
$$
\begin{align}
\left| \braket{ +z | +n }  \right| ^{2} + \tan ^{2} \frac{\theta}{2} \left| \braket{ +z | +n }   \right|^{2}  & = 1 \\
\left| \braket{ +z | +n } \right| ^{2}\left( 1+ \tan ^{2} \frac{\theta}{2} \right)  & = 1    \\
\left| \braket{ +z | +n }  \right| ^{2}\left( \frac{1}{\cos ^{2} \frac{\theta}{2} } \right) & =1 \\
\braket{ +z | +n }  & = \pm  \cos \frac{\theta}{2}
\end{align}
$$
We can plug this in to the equation for the two states (assuming +), the cosine will cancel, and we will get
$$
\begin{align}
\braket{ -z | +n } = \sin \frac{\theta}{2} e^{i\phi} 
\end{align}
$$

Thus,
$$
\boxed{
\begin{align}
\ket{+n} = \cos \frac{\theta}{2} + \sin \frac{\theta}{2} e^{i\phi} \ket{-z} 
\end{align}
}
$$


### n= -1
$$\begin{align}
\begin{pmatrix}
\cos\theta + 1  &  \sin\theta e^{-i\phi} \\
\sin\theta e^{i\phi} & -\cos\theta+1
\end{pmatrix} \begin{pmatrix}
\braket{ +z | -n }  \\
\braket{ -z | -n } 
\end{pmatrix} = \vec{0} \\
\end{align}
$$


The equation is
$$
\begin{align}
(\cos \theta+1) \braket{ +z | -n } = - \sin \theta e^{-i\phi} \braket{ -z | -n } \\ 
\end{align}
$$



We have similar trig identities

$$
\begin{align}
\cos \frac{\theta}{2} = \sqrt[]{  \frac{1+\cos\theta}{2} }  \\
1+\cos\theta = 2\cos ^{2} \frac{\theta}{2} \\
\sin \theta = 2 \sin \frac{\theta}{2} \cos \frac{\theta}{2}

\end{align}
$$
This gets
$$
\begin{align}
2 \cos ^{2} \frac{\theta}{2} \braket{ +z | -n }  &= - 2\sin \frac{\theta}{2} \cos \frac{\theta}{2}e^{i-\phi} \braket{ -z | -n }  
\end{align}
$$


We can now divide to get
$$
\begin{align}
\braket{ +z | -n } = -2 \frac{\sin \frac{\theta}{2}}{\cos \frac{\theta}{2}}e^{-i\phi} \braket{ -z | -n } 
\end{align}
$$

AGAIN (why is this problem so lonnnggg TT)
$$
\begin{align}
\left| \braket{ +z | +n } \right| ^{2*} + \left| \braket{ -z | +n } \right| ^{2*} = 1
\end{align}
$$
So we have
$$
\begin{align}
\left| \braket{ -z | -n } \right|^{2}\left( 1 +  \tan ^{2} \frac{\theta}{2}  \right) = 1 \\
\left| \braket{ -z | -n }  \right| ^{2}\left( \frac{1}{\cos ^{2} \frac{\theta}{2}} \right)=1 \\
\left| \braket{ -z | -n }  \right| ^{2} = \cos ^{2} \frac{\theta}{2}
\end{align}
$$
We can plug that in to the equation relating the amplitudes to get
$$
\begin{align}
\braket{ +z | -n } = - \sin \frac{\theta}{2} e^{-i\phi}
\end{align}
$$
The position of the overall phase doesn't matter, so I'll move it to the $-z$ position
Therefore, we have
$$
\boxed{
\begin{align}
\ket{n}  & =  \sin \frac{\theta}{2} \ket{+z} + \cos \frac{\theta}{2}e^{i\phi} \ket{-z} 
\end{align}
}
$$




![[Pasted image 20260210202445.png]]

$$
\begin{align}
\hat{S}_{y}  & = \frac{\hbar}{2}\begin{pmatrix}
0 & -i \\
i & 0
\end{pmatrix} \\
\hat{S}_{y}^{2}  & = \frac{\hbar^{2}}{4} \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}  \\
\hat{S}_{y}^{3} & =\hat{S}_{y}  \\
\vdots
\end{align}
$$

We can Taylor expand:
$$
\begin{align}
e^{\frac{-i \hat{S}_{y} \theta}{\hbar} }& =1 - \frac{i^{2}}{\hbar} \frac{\hbar}{2}\begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix} \theta + \frac{1}{2!}   \left(\frac{i}{\hbar} \hat{S}_{y} \theta\right)^{2} + \dots
\end{align}
$$
Reduce the terms to either the identity or $\hat{S}_{y}$ for all powers of $n$. Take note of the terms $\frac{\hbar}{2}$ as a constant for each $\hat{S}_{y}$ matrix - this cancels the $\hbar$ from the perfector terms. 
$$
\begin{align}
\hat{R}(\theta \mathbf{j}) = - \underbrace{ \frac{i}{\hbar}\hat{S}_{y} }_{ \text{ odd, sin } }\theta  + \frac{1}{2!}\left(  \frac{i}{\hbar}\underbrace{\frac{\hbar}{2}\frac{2}{\hbar} \hat{S}_{y} }_{ \mathbf{I} }\theta  \right)^{2}+ \dots   
\end{align}
$$

All the even power terms of $\hat{S}_{y}^{2n}$ are the identity, and all the odd terms are just $\hat{S}_{y}^{2n+1}=\hat{S}_{y}$. We can therefore separate out this expression to be

We can pull out the $\frac{i}{\hbar}$ 

Taking note of the Euler's identity that $e^{i\theta}=\cos\theta+i\sin\theta$. We have the Taylor series for $\cos \theta$. This becomes the Taylor expansion of
$$
\begin{align}
e^{-i \hat{S}_{y} \frac{\theta}{2} }= \cos\left( \frac{\theta}{\hbar}  \right)\mathbf{I} + \frac{2i}{\hbar} \hat{S}_{y} \sin \left( \frac{\theta }{2}  \right)
\end{align}
$$

QED.

## B
We can apply this matrix representation to $\ket{+z}$
$$
\begin{align}
 R (\theta \mathbf{J}) & =\begin{bmatrix}
\cos \frac{\theta}{2} & 0 \\
0 & \cos \frac{\theta}{2} 
\end{bmatrix} - \frac{2i}{\hbar}\begin{bmatrix}
0 & -i \\
i & 0
\end{bmatrix} \\
 & = \begin{bmatrix}
\cos \frac{\theta}{2}  & \frac{2}{\hbar} \sin \frac{\theta}{2} \\
\frac{-2}{\hbar} \sin \frac{\theta}{2}& \cos \frac{\theta}{2}
\end{bmatrix}
\end{align}
$$
applying this on $\ket{+z}$ by multiplying this matrix on the left side of
$$
\begin{align}
\vec{R}(\theta \mathbf{J})\begin{pmatrix}
\ket{+z} \\ \ket{-z} 
\end{pmatrix}
\end{align}
$$
The top row is the $\ket{+n}$ vector, and the bottom row is the $\ket{-n}$ vector:
$$
\begin{align}
\ket{+n} & = \cos \frac{\theta}{2} \ket{+z} + \frac{2}{\hbar} \sin \frac{\theta}{2} \ket{-z}  \\
\ket{-n} & =\frac{\hbar}{2} \sin \frac{\theta}{2} - \frac{2}{\hbar} \sin \frac{\theta}{2} \ket{-z}  
\end{align}
$$

We have gotten the result for $\phi=0$

![[Pasted image 20260212210637.png]]





![[Pasted image 20260210202459.png]]

## 3.8
If a matrix $\hat{A}$ is Hermitian, then $\hat{A}=\hat{A}^{\dagger}$
We can expand out
$$
\begin{align}
[\hat{A}, \hat{B}]  & = \hat{A}\hat{B} - \hat{B}\hat{A} \\
 & =A^{\dagger}B^{\dagger}-B^{\dagger}A^{\dagger} \\
 & =[\hat{A}^{\dagger},\hat{B}^{\dagger}]
\end{align}
$$
Therefore, 
$$
\begin{align}
i\hat{C}= i\hat{C}^{\dagger}
\end{align}
$$
so $\hat{C}$ is Hermitian.
## 3.12
### $\hat{S}_{z}$
$$
\begin{align}
\hat{S}_{z}\ket{+z}  & = \frac{\hbar}{2} \ket{+z} \bra{+z}\ket{+z} - 0 \\
 & = \frac{\hbar}{2} \ket{z} \\
\hat{S}_{z} \ket{-z}  & = 0 - \frac{\hbar}{2} \ket{-z} \\
 & = -\frac{\hbar}{2}\ket{-z}     
\end{align}
$$
This validates the $\hat{S}_{z}$ expression.

We can check the raising and lowering operators now
### $\hat{S}_{+}$
$\hbar \ket{+z}\bra{-z}$

$$
\begin{align}
\hat{S}_{+}\ket{-z}  & = \hbar \ket{+z} \\
\hat{S}_{+}\ket{+z}  & = 0 \\
\end{align}
$$
### $\hat{S}_{-}$
$\hbar \ket{-z}\bra{+z}$
$$
\begin{align}
\hat{S}_{-}\ket{+z}  & = \hbar \ket{-z} \\
\hat{S}_{-}\ket{-z}  & = 0     
\end{align}
$$


![[Pasted image 20260210202526.png]]

## A

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

The eigenvalues are $\hbar,0,-\hbar$. We can now solve for the vectors
### $\lambda=\hbar$
$$
\begin{align} \frac{1}{\sqrt[]{ 2 } }
\begin{bmatrix}
-\sqrt[]{ 2 }  & 1 & 0 \\
1 & -\sqrt[]{ 2 }  & 1 \\
0 & 1 & -\sqrt[]{ 2 } 
\end{bmatrix} \begin{bmatrix}
a\\ b\\ c
\end{bmatrix} & =0
\end{align}
$$

We get
$$
\begin{align}
-\sqrt[]{ 2 } a+b=0 \\
a-\sqrt[]{ 2 } b+c=0 \\
b-\sqrt[]{ 2 } c=0
\end{align}
$$

This has $a=c$ and $2a=\sqrt[]{ 2 }b$

so the eigenvector is 
$$
\begin{align}
\frac{1}{2 }\begin{bmatrix}
1\\\sqrt[]{ 2 } \\1
\end{bmatrix}
\end{align}
$$


### $\lambda=0$

The matrix is

$$
\begin{align} \frac{1}{\sqrt[]{ 2 } }
\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 0
\end{bmatrix} \begin{bmatrix}
a\\ b\\ c
\end{bmatrix} & =0
\end{align}
$$
This gives
$$
\begin{align}
b=0 \\
a=-c \\
b=0
\end{align}
$$
That gives
$$
\begin{align}
\frac{1}{\sqrt[]{ 2 } }\begin{bmatrix}
1\\0\\-1
\end{bmatrix}
\end{align}
$$


### $-\hbar$
Finally, 
$$
\begin{align} \frac{1}{\sqrt[]{ 2 } }
\begin{bmatrix}
\sqrt[]{ 2 }  & 1 & 0 \\
1 & \sqrt[]{ 2 }  & 1 \\
0 & 1 & \sqrt[]{ 2 } 
\end{bmatrix} \begin{bmatrix}
a\\ b\\ c
\end{bmatrix} & =0
\end{align}
$$

This gives
$$
\begin{align}
\frac{1}{2 }\begin{bmatrix}
1\\-\sqrt[]{ 2 } \\1
\end{bmatrix}
\end{align}
$$


## B
![[Pasted image 20260212214419.png]]

The particle is in the state $\ket{+z}$. This is asking
$$
\begin{align}
\braket{ S_{x}=0 \text{ state }  | 1,1_{z}   } 
\end{align}
$$

We know that the eigenvector corresponding to $S_{x}\ket{z}=0$ has the form 
$$
\begin{align}
\begin{bmatrix}
1\\0\\-1
\end{bmatrix}
\end{align}
$$
from above. Therefore, we can write this as
$$
\begin{align}
\braket{ 1,0_{x}  |+z  } & = \frac{1}{\sqrt[]{ 2 } } [1,0,-1] \begin{bmatrix}
1\\0\\0
\end{bmatrix} \\
 & =\frac{1}{\sqrt[]{ 2 } }
\end{align}
$$
Thus,
$$
\begin{align}
\left| \braket{ 1,0_{x}  | +z }  \right| ^{2} = \frac{1}{2}
\end{align}
$$



![[Pasted image 20260210202541.png]]

## a) 
$\hbar: \frac{1}{14}$
$0: \frac{2}{7}$
$-\hbar: \frac{9}{14}$

$$
\begin{align}
\left< S_{z}  \right>  & = \frac{\hbar}{14} - \frac{9\hbar}{14} \\
 & = \frac{-8\hbar}{14} \\
 & = -\frac{4}{7}\hbar
\end{align}
$$


## b)
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

Where 
$$
\begin{align}
\ket{1,1} = \begin{pmatrix}
1 \\ 0 \\ 0
\end{pmatrix}  \\
\ket{1,0}  = \begin{pmatrix}
0 \\ 1 \\ 0
\end{pmatrix} \\
\ket{1,-1} = \begin{pmatrix}
0 \\0\\1
\end{pmatrix}
\end{align}
$$

We know that 
$$
\begin{align}
\left< S_{x}  \right>= \bra{\psi} S_{x} \ket{\psi}  
\end{align}
$$
Therefore, we can compute
$$
\begin{align}
\psi & = \frac{1}{\sqrt[]{ 14 } }\begin{pmatrix}
1\\2\\3i
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
\psi' = \frac{1}{\sqrt[]{ 14 } }(1,2,-3i)
\end{align}
$$


This just becomes
$$
\begin{align} 
\left< S_{x}  \right> & = \frac{1}{14}(1,2,-3i) \frac{\hbar}{\sqrt[]{ 2 } }\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 0
\end{bmatrix}\begin{pmatrix}
1\\2\\3i
\end{pmatrix} \\
 & = \frac{1}{14}(1,2,-3i) \frac{\hbar}{\sqrt[]{ 2 } } \begin{bmatrix}
2 \\1+3i\\2
\end{bmatrix} \\
 & =\frac{\hbar}{14\sqrt[]{ 2 } }( 2 + 2 + 6i - 6i) \\
 & = \frac{4\hbar}{14\sqrt[]{ 2 } }
\end{align}
$$

## C
The state for $\hat{S}_{x}=\hbar$ has the matrix representation
$$
\begin{align} \ket{\hat{S}_{x}=\hbar }= \frac{1} {2} 
\begin{bmatrix}
1\\\sqrt[]{ 2 } \\1
\end{bmatrix}
\end{align}
$$


We can write this now as
$$
\begin{align}
\braket{ +x | \psi}  & =\frac{1}{2} [1,\sqrt[]{ 2 } ,-1]\frac{1}{\sqrt[]{ 14 } }\begin{pmatrix}
1\\2\\3i
\end{pmatrix} \\
 & = \frac{1}{2\sqrt[]{ 14 } }(1+2\sqrt[]{ 2 } -3i)
\end{align}
$$
The probability is this squared, so
$$
\begin{align}
\left| \braket{ +x | \psi }  \right|^{2} &  =\frac{1}{56} ((1 + 2 \sqrt[]{ 2 } )^{2} +9) \\
 & = \frac{1}{56} (18+ 4 \sqrt[]{ 2 } )
\end{align}
$$

This feels like a weird number, but okay??? I can do algebra I think?


![[Pasted image 20260210202554.png]]

### A
The rotation matrix is given by
$$
\begin{align}
\hat{R}(\theta J) = \begin{pmatrix}
\frac{1+\cos \theta}{2} & - \frac{\sin\theta}{\sqrt[]{ 2 } } & \frac{1- \cos\theta}{2} \\
\frac{\sin \theta}{\sqrt[]{ 2 } } & \cos\theta & \frac{-\sin \theta}{\sqrt[]{ 2 } } \\
\frac{1- \cos\theta}{2} & \frac{\sin\theta}{\sqrt[]{ 2 } }   &  \frac{1 + \cos\theta}{2}
\end{pmatrix} 
\end{align}
$$

This tells us that
$$
\begin{align}
\ket{n}=  \hat{R}(\theta J) \ket{z} 
\end{align}
$$
For $\ket{S_{n}=\hbar}$, we multiply by the basis vector
$$
\begin{align}
\begin{pmatrix}
1\\0\\0
\end{pmatrix}
\end{align}
$$
This gets
$$
\begin{align}
\ket{+n}= \begin{pmatrix}
\frac{1+\cos\theta}{2} \\\frac{ \sin \theta}{\sqrt[]{ 2 } } \\ \frac{1- \cos \theta}{2}
\end{pmatrix} 
\end{align}
$$


We can now find 
$$
\begin{align}
\left| \braket{ +n | +z } \right| ^{2} &  =  \left[\frac{1+\cos\theta}{2},\frac{ \sin \theta}{\sqrt[]{ 2 } }, \frac{1- \cos \theta}{2}\right]\begin{pmatrix}
1\\0\\0
\end{pmatrix} \\
 & = \left( \frac{1+\cos \theta}{2} \right)^{2}
\end{align}
$$
We have the next step as
$$
\begin{align}
\left| \braket{ -z | +n }  \right| ^{2}   & =\left( \left[0,0,1\right]\begin{pmatrix}
\frac{1+\cos\theta}{2}\\\frac{ \sin \theta}{\sqrt[]{ 2 } }\\\frac{1- \cos \theta}{2}
\end{pmatrix} \\ \right)^{2} \\
 & =\left( \frac{1-\cos\theta}{2} \right)^{2}
\end{align}
$$

So the odds of going through both are
$$
\begin{align}
\left( \frac{1-\cos\theta}{2} \right)^{2}\left( \frac{1+\cos\theta}{2} \right)^{2} \\
=\left( \frac{1+\cos ^{2}\theta}{4} \right)^{2}
\end{align}
$$

### B
at $\theta=\pi$. The arguments are maximized by $\cos ^{2}\theta$ 


### C
None would pass through, since $\ket{S_{z}=\hbar}$ has no transition and can't be immediately in the state $\ket{S_{z}=-\hbar}$ or $\ket{S_{z}=0}$.

### D?


#### A
We would now have 
$\ket{S_{z}=0,+n}$ 
$$
\begin{align}
\ket{+n}= \begin{pmatrix}
\frac{1+\cos\theta}{2} \\\frac{ \sin \theta}{\sqrt[]{ 2 } } \\ \frac{1- \cos \theta}{2}
\end{pmatrix} 
\end{align}
$$
So this would be $\left( \frac{\sin\theta}{\sqrt[]{ 2 }} \right)^{2}$

this gets
$$
\begin{align}
\left( \frac{1+\cos\theta}{2} \right)^{2} \cdot \left( \frac{\sin\theta}{\sqrt[]{ 2 } } \right)^{2}
\end{align}
$$

#### B
this is maximized at
$\theta=\frac{\pi}{3}$ 
![[Pasted image 20260213085233.png]]

#### C
This would stay the same - we don't have any $S_{z}=0$ if we have just enforced $S_{z}=\hbar$.






# Extra work that I didn't want to delete because I was proud but it was useless

## a

We are computing here 
$$
\begin{align}
|\braket{ S_{n} =\hbar | S_{z}=\hbar  } |^{2} \cdot |\braket{ S_{z} =-\hbar | S_{n} =\hbar } |^{2}
\end{align}
$$
$\ket{1,1}_{z}= \begin{pmatrix}1\\0\\0\end{pmatrix}$
$$
\begin{align}
\braket{ 1 | 1 }_{n} = R(\theta J) \ket{1,1}_{z} \\
\end{align}
$$

$J_{y}= \frac{1}{2i}(J_{+}-J_{-})$
Lets use the basis
$$
\begin{align}
\ket{1,+1} \to   \begin{pmatrix}
1\\0\\0
\end{pmatrix} \\
\ket{1,0} \to   \begin{pmatrix}
0\\1\\0
\end{pmatrix} \\
\ket{1,-1} \to   \begin{pmatrix}
0\\0\\1
\end{pmatrix} 
\end{align}
$$

$J_{+}\ket{j,m}=\hbar \sqrt[]{ j(j+1)-m(m+1) }\ket{j,m+1}$
$$
\begin{align}
J_{+}\ket{1,1}=0 \\
J_{+}\ket{1,0} = h  \sqrt[]{ 2} \ket{1,1} \\
J_{+}\ket{1,-1} = \hbar\sqrt[]{ 2 } \ket{1,0} 
\end{align}
$$

So we can make the $J_{+}$ matrix:
$$
\begin{align}
J_{+}= \hbar\begin{bmatrix}
0 & \sqrt[]{ 2 }  & 0 \\
0 & 0 & \sqrt[]{ 2 }   \\
0 & 0 & 0
\end{bmatrix} 
\end{align}
$$
$$
\begin{align}
\hat{J}_{-}= \hbar \begin{pmatrix}
0 & 0 & 0 \\
\sqrt[]{ 2 }  & 0 & 0 \\
0 & \sqrt[]{ 2 }  & 0
\end{pmatrix}
\end{align}
$$

$$
\begin{align}
\hat{J}_{y}=\frac{1}{2i} \begin{bmatrix}
0 & \sqrt[]{ 2 }  & 0 \\
-\sqrt[]{ 2 }  & 0 & \sqrt[]{ 2 }  \\
0 & -\sqrt[]{ 2 }  & 0
\end{bmatrix}
\end{align}
$$
This gives us the generator of rotations, that
$$
\begin{align}
\ket{+n}= e^{\frac{-i}{\hbar}\hat{J}_{y}\theta } \ket{+z}  
\end{align}
$$
The pavlovian urge is to ~~~integrate~~~ taylor expand

$$
\begin{align}
e^{\frac{-i}{\hbar}\hat{J}_{y}\theta } = 1-
\end{align}
$$




# a different question
We can write the $\hat{S}_{x}$ operator in the spin 1 $\ket{+z}$ basis
$$
\begin{align} 
\hat{S}_{x} = \frac{\hbar}{2}\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 0
\end{bmatrix}
\end{align}
$$
This gives us that
$$
\begin{align}
\frac{\hbar}{2} \begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 0
\end{bmatrix} \begin{pmatrix}
1\\0\\0
\end{pmatrix}  & = \begin{bmatrix}
0\\1\\0
\end{bmatrix} \\
\frac{\hbar}{2} \begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 0
\end{bmatrix} \begin{pmatrix}
0\\1\\0
\end{pmatrix}  & = \begin{bmatrix}
1\\0\\1
\end{bmatrix} \\
\frac{\hbar}{2} \begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 0
\end{bmatrix} \begin{pmatrix}
0\\0\\1
\end{pmatrix}  & = \begin{bmatrix}
0\\1\\0
\end{bmatrix} \\
\end{align}
$$

Summarized, 
$$
\begin{align}
\hat{S}_{x}\ket{1,1} &  = \frac{\hbar}{2} \ket{1,0} \\
\hat{S}_{x}\ket{1,0} &  = \frac{\hbar}{2}(\ket{1,1} + \ket{1,-1}  )    \\
\hat{S}_{x}\ket{1,-1}  & = \frac{\hbar}{2} \ket{1,0} \\  
\end{align}
$$

