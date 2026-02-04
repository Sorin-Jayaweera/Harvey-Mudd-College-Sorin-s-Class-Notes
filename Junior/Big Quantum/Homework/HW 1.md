![[Pasted image 20260120115739.png]]
$$
\begin{align}
n = \sin\theta \cos \phi \hat{i} + \sin\theta \sin \phi \hat{j} + \cos \theta \hat{k}
\end{align}
$$
## A
The state $\ket{+x}$ corresponds to the vector $\begin{bmatrix}1\\0\\0\end{bmatrix}$, and $\ket{+y}$ to $\begin{bmatrix}0\\1\\0\end{bmatrix}$.
To get only $x$, $\theta=\frac{\pi}{2}$ and $\phi=0$.
$$
\begin{align}
\ket{+x}   &  \stackrel{?}{=}   \cos \frac{\pi}{4}\ket{+z} + \sin \frac{\pi}{4} \ket{-z}   \\
\ket{+x}  & \stackrel{?}{=}   \frac{\sqrt[]{ 2 }}{2}(\ket{+z} + \ket{-z} )
\end{align}
$$

Only $y$ has $\theta=\frac{\pi}{2},\phi=\frac{\pi}{2}$.
$$
\begin{align}
\ket{+y}  & \stackrel{?}{=}  \cos \frac{\pi}{4}\ket{+z}  + e^{\frac{i\pi}{2}}\sin \frac{\pi}{4} \ket{-z}  \\
\ket{+y} &  = \frac{\sqrt[]{ 2 }}{2} (\ket{+z} + i \ket{-z} )  \\
 & = \sqrt[]{ \frac{1}{2 } } (\ket{+z } + i \ket{-z} )
\end{align}
$$

## B
![[Pasted image 20260125192559.png]]
![[Pasted image 20260125192612.png]]

$P\left( \frac{\hbar}{2} \right) = \cos^{2} \frac{\theta}{2}$
$P\left( -\frac{\hbar}{2} \right) = \sin ^{2}\left( \frac{\theta}{2} \right)$

## C
![[Pasted image 20260125192643.png]]

![[Pasted image 20260125192612.png]]

$$
\begin{align}
\Delta S_{z} &  = \sqrt[]{ \left< S_{z} ^{2} \right> - \left< S_{z}  \right>^{2} }  \\
\end{align}
$$

We can find $\left< S_{z} \right>^{2}$
$$
\begin{align}
\left< S_{z} \right>  & = \frac{\hbar}{2}  (\left| \braket{ +z | +n } \right|^{2} -\left| \braket{ -z | +n } \right|)  \\
\left< S_{z}  \right>  & = \frac{\hbar}{2} \left(\cos ^{2} \frac{\theta}{2} - \sin ^{2} \frac{\theta}{2} \right) \\
\left< S_{z}  \right> ^{2}  & = \frac{\hbar^{2}}{4} \left( \cos ^{4} \frac{\theta}{2} + \sin ^{4} \frac{\theta}{2} - \cos ^{2} \frac{\theta}{2} \sin ^{2} \frac{\theta}{2} \right) 
\end{align}
$$
We can also find $\left< S_{z}^{2} \right>$
$$
\begin{align}
\left< S_{z}^{2} \right> = \left| \braket{ +z | +n } \right|^{2} \left( \frac{\hbar}{2} \right)^{2} + \left( \frac{\hbar}{2} \right)^{2}\left| \braket{ -z | +n } \right| ^{2}\\
= \frac{\hbar^{2}}{4}\left( \cos ^{2} \frac{\theta}{2} + \sin ^{2} \frac{\theta}{2} \right)
\end{align}
$$


This gives us
$$
\begin{align}
\Delta S_{z}   & = \frac{\hbar}{2} \sqrt[]{ \cos ^{2} \frac{\theta}{2} + \sin ^{2} \frac{\theta}{2 } - \left( \cos ^{4} \frac{\theta}{2} + \sin ^{4} \frac{\theta}{2} - \cos ^{2} \frac{\theta}{2} \sin ^{2} \frac{\theta}{2} \right)}   \\
 & = \frac{\hbar}{2} \sqrt[]{ 1 - \left( \cos ^{4} \frac{\theta}{2} + \sin ^{4} \frac{\theta}{2} - \cos ^{2} \frac{\theta}{2} \sin ^{2} \frac{\theta}{2} \right)}
\end{align}
$$

I don't want to further simplify this, but I am sure there exist trig identities to do so.
 ![[Pasted image 20260120115746.png]]
$$
\begin{align}
\ket{+y} =  \sqrt[]{ \frac{1}{2} } \ket{+z} + e^{\frac{i\pi}{2}} \sqrt[]{ \frac{1}{2 } } \ket{-z}  \\
\implies \bra{+y}  = \sqrt[]{ \frac{1}{2} } \bra{+z} + e^-\frac{i \pi}{2}\sqrt[]{ \frac{1}{2 } } \bra{-z} 
\end{align}
$$

$$
\begin{align}
\braket{ +n | +y }  &  \\
 & = \left( \cos \frac{\theta}{2}\ket{+z  }+ e^{i\phi}\sin \frac{\theta}{2}\ket{-z}  \right) \left( \sqrt[]{ \frac{1}{2} } \bra{+z} + e^\frac{-i \pi}{2}\sqrt[]{ \frac{1}{2 } } \bra{-z}  \right) \\
\text{ because }  & \braket{ +z | -z }=0 \\
 \braket{ +n | +y } & = \sqrt[]{ \frac{1}{2} } \cos \frac{\theta}{2} + e^{i\left( \phi-\frac{\pi}{2} \right)}\sqrt[]{ \frac{1}{2} } \sin \frac{\theta}{2}
\end{align}
$$
The probability of this is 
$$
\begin{align}
\left| \braket{ +z | +y } \right|  ^{2} = \frac{1}{2} \sin ^{2} \frac{\theta}{2} + \frac{1}{2} \cos^{2} \frac{\theta}{2} + \frac{1}{2}\sin \frac{\theta}{2} \cos \frac{\theta}{2} \\
= \frac{1}{2}\left( 1+ \sin \frac{\theta}{2}\cos \frac{\theta}{2} \right)
\end{align}
$$



We can check this with the test case state $\ket{+n}=\ket{+y}$ to see if we get $\braket{ +y | +y }=1$.
$\phi = \frac{\pi}{2}, \theta  = \frac{\pi}{2}$
This becomes

$$
\begin{align}
\sqrt[]{ \frac{1}{2} } \sqrt[]{ \frac{1}{2} } + \sqrt[]{ \frac{1}{2} }\sqrt[]{ \frac{1}{2} }    \\
=1
\end{align}
$$
So the equality holds for the test case. 

###  b)
![[Pasted image 20260125192612.png]]
We can write

$$
\begin{align}
\braket{ +y | +n }  &  \\
 & = \left( \sqrt[]{ \frac{1}{2} } \bra{+z} + e^\frac{-i \pi}{2}\sqrt[]{ \frac{1}{2 } } \bra{-z}  \right)\left( \cos \frac{\theta}{2}\ket{+z  }+ e^{i\phi}\sin \frac{\theta}{2}\ket{-z}  \right)  \\
\text{ because }  & \braket{ +z | -z }=0 \\
 \braket{ +y | +n } & = \sqrt[]{ \frac{1}{2} } \cos \frac{\theta}{2} + e^{i\left( \phi-\frac{\pi}{2} \right)}\sqrt[]{ \frac{1}{2} } \sin \frac{\theta}{2}
\end{align}
$$
This is the amplitude of getting $\ket{+y}$ given $\ket{+n}$. The probability is
$$
\begin{align} \\
\left| \braket{ +y | +n  }  \right| ^{2}  = \frac{1}{2}\left( 1+ \sin \frac{\theta}{2} \cos \frac{\theta}{2} \right)
\end{align}
$$


We can check this with $\ket{+n}=\ket{+y}$ to see if we get $\braket{ +y | +y }=1$.
$\phi = \frac{\pi}{2}, \theta  = \frac{\pi}{2}$
This becomes

$$
\begin{align}
\sqrt[]{ \frac{1}{2} } \sqrt[]{ \frac{1}{2} } + \sqrt[]{ \frac{1}{2} }\sqrt[]{ \frac{1}{2} }    \\
=1
\end{align}
$$
So the equality holds for the test case. 

### b
![[Pasted image 20260126191947.png]]
![[Pasted image 20260125192612.png]]
$$
\begin{align}
\ket{+y} =  \sqrt[]{ \frac{1}{2} } \ket{+z} + e^{\frac{i\pi}{2}} \sqrt[]{ \frac{1}{2 } } \ket{-z} 
\end{align}
$$
This is exactly the same as pt a, since multiplication is commutative and the conjugate transpose acts on the same product:

$$
\begin{align}
\braket{ +n | +y }  &  \\
 & = \left( \cos \frac{\theta}{2}\ket{+z  }+ e^{-i\phi}\sin \frac{\theta}{2}\ket{-z}  \right)\left( \sqrt[]{ \frac{1}{2} } \bra{+z} + e^\frac{i \pi}{2}\sqrt[]{ \frac{1}{2 } } \bra{-z}  \right)  \\
\text{ because }  & \braket{ +z | -z }=0 \\
 \braket{ +n | +y } & = \sqrt[]{ \frac{1}{2} } \cos \frac{\theta}{2} + e^{i\left( \phi-\frac{\pi}{2} \right)}\sqrt[]{ \frac{1}{2} } \sin \frac{\theta}{2}
\end{align}
$$
The probability is
$$
\begin{align}
\frac{1}{2}\left(  1 + \cos \frac{\theta}{2} \sin \frac{\theta}{2} \right)
\end{align}
$$


![[Pasted image 20260120115755.png]]
### a)
![[Pasted image 20260125192612.png]]
We can check this by rotating only $\theta$ (the angle down from $+\vec{z}$) by $\frac{\pi}{2}$. Any change to $\phi$ would not reflect the vector properly. 

We see that $\cos \theta=\sin\theta+\frac{\pi}{2}$, so this holds.
### b)
$$
\begin{align}
\bra{-n} = \sin \frac{\theta}{2} \bra{+z} - e^{-i\phi}  \cos \frac{\theta}{2}\bra{-z}  
\end{align}
$$
We can check normalizaiton
$$
\begin{align}
\braket{ -n | -n }  & = \left(\sin \frac{\theta}{2} \bra{+z} - e^{-i\phi}  \cos \frac{\theta}{2}\bra{-z}  \right)\left(\sin \frac{\theta}{2} \ket{+z} -e^{i\phi}  \cos \frac{\theta}{2}\ket{-z}  \right) \\
 & = \left| \sin ^{2} \frac{\theta}{2} + e^{2i\phi}\cos ^{2} \frac{\theta}{2} \right|  \\
 & = \sin ^{2} \omega + \cos ^{2} \omega \\
 & = 1
\end{align}
$$
So this is properly normalized.

### c)
$$
\begin{align}
\bra{-n}= \sin \frac{\theta}{2} \bra{+z} - e^{-i\phi}  \cos \frac{\theta}{2}\bra{-z}   \\
\ket{+n} = \cos \frac{\theta}{2} \ket{+z}  + e^{i\phi} \sin \frac{\theta}{2} \ket{-z} 
\end{align}
$$

We can check orthogonality:
$$
\begin{align}
\braket{ -n |+n  }  &  \\
 & = \left( \sin \frac{\theta}{2} \cos \frac{\theta}{2} \right)- \left( \cos \frac{\theta}{2} \sin \frac{\theta}{2} \right)  \\
 & =0
\end{align}
$$

So orthogonality holds

### d)
Written component wise as a three vector,
$$
\begin{align}
n = \sin\theta \cos \phi \hat{i} + \sin\theta \sin \phi \hat{j} + \cos \theta \hat{k}
\end{align}
$$
We can check the dot product $-n\cdot n$ by multiplying component wise (square each term, multiply each term by $-1$):
$$
\begin{align}
-n\cdot n & =-(\sin\theta \cos \phi)^{2} - \sin ^{2}\theta \sin ^{2}\phi - \cos ^{2}\theta \\
 & =-\sin ^{2}\theta(\cos ^{2}\phi+\sin ^{2}\phi)-\cos ^{2}\theta \\
 & = -\sin ^{2}\theta(1)-\cos ^{2}\theta \\
 & = -(\sin ^{2}\theta+\cos ^{2}\theta) \\
 & =-1
\end{align}
$$
Thus,  their orthogonality in Hilbert space has been shown.


![[Pasted image 20260120115809.png]]
### a)
Because $\phi=0$, the states $\ket{+n}$ can be written succinctly as
$\ket{+n} = \cos \frac{\theta}{2} \ket{+z}+ \sin \frac{\theta}{2}\ket{-z}$

![[Pasted image 20260126200106.png]]

The number of particles in the $\ket{+n}$ state after the second SG device is 
$\frac{N_{0}}{2} \braket{ +n | +z }$

This is
$$
\begin{align}
\braket{ +n | +z } = \cos \frac{\theta}{2}
\end{align}
$$
We can now multiply this with the probability $\braket{ -z | +n }$
Which is $\sin \frac{\theta}{2}$. Therefore, the fraction of particles measured in the $-\frac{\hbar}{2}$ state after the third SG device is simply
$$
\begin{align}
\frac{1}{2}\cos\frac{\theta}{2} \sin \frac{\theta}{2}
\end{align}
$$

### B)
The angle which maximizes the function
$\cos \frac{\theta}{2} \sin \frac{\theta}{2}$ is $\frac{\pi}{2}$. 
$$
\begin{align}
\cos \frac{\pi}{4} \sin \frac{\pi}{4} = 0.5
\end{align}
$$
For this angle, there would be $0.25$ particles after the third SG device (half through the first, then $\sqrt[]{ \frac{1}{2} }$ for the next two).


### C)

If the $SG_{n}$ device is removed, then we are measuring in the same basis twice in a row. The particles do not "reset" their spin measurements. 
We are asking the question $\braket{ -z | +z }$ which is $0$, because the two bases are orthogonal.

![[Pasted image 20260120115819.png]]
We can write out the information as
$$
\begin{align}
\left| \braket{ +z | +n } \right|^{2}  = \frac{9}{10} \\
\left| \braket{ +y | +n } \right|^{2}  = \frac{1}{5}  
\end{align}
$$

This becomes a system of equations, and we can solve for $\ket{+n}$.
$$
\begin{align}
\ket{+n} = \cos \frac{\theta}{2} \ket{+z}  + e^{i\phi} \sin \frac{\theta}{2} \ket{-z} 
\end{align}
$$
$$
\begin{align}
\braket{ +z | +n }= \frac{9}{10}= \cos^{2} \frac{\theta}{2} \\
2 \arccos(\sqrt[]{ \frac{9}{10} } ) = \theta
\end{align}
$$

$\theta \approx 0.6435$

Similarly, 
$$
\begin{align}
\left| \braket{ +y | +n }  \right|^{2}  & = \left| \left( \sqrt[]{  \frac{1}{2}  }\bra{+z}  + \sqrt[]{ \frac{1}{2 } } \bra{-z}   \right)\left( \cos \frac{\theta}{2} \ket{+z} + e^{i\phi} \sin \frac{\theta}{2} \ket{ -z}  \right) \right|^{2}  \\
 \frac{1}{5} & = \left( \sqrt[]{ \frac{1}{2} } \cos \frac{\theta}{2}  + \sqrt[]{ \frac{1}{2} }e^{i\phi} \sin \frac{\theta}{2} \right)^{2}  \\ \\
\frac{1}{\sqrt[]{ 5 } } &  = \sqrt[]{ \frac{1}{2} }(\cos 0.32 + \sin(0.32)e^{i\phi})  \\
-1  & =\frac{\sqrt[]{ \frac{2}{5} - \cos(0.32) }}{\sin(0.32)}  = e^{i\phi}\\ \\
\phi = \frac{\pi}{2}
\end{align}
$$

$$
\begin{align}
\ket{+n}  = \cos \left(0.32 \right)\ket{+z} + e^{i \frac{\pi}{2} } \sin\left( 0.32 \right) \ket{-z} 
\end{align}
$$

Because $\phi\approx \frac{\pi}{2}$, $\braket{ +z | +n }\approx \frac{1}{2}$.


![[Pasted image 20260120115831.png]]

### Normalized?
We can check
$$
\begin{align}
\braket{ \psi | \psi  }  & \stackrel{?}{=}    \\
\frac{1}{5}[-i , 2] \begin{bmatrix}
i \\ 2
\end{bmatrix}    & =\frac{1}{5} 1+4 \\
 & =1
\end{align}
$$
We can see that this is indeed normalized.
### $\frac{\hbar}{2}$?
$$
\begin{align}
\ket{x}  & = \frac{1}{\sqrt[]{ 2 } } \begin{pmatrix}
1\\1
\end{pmatrix} \\
\ket{+y}  & = \frac{1}{\sqrt[]{ 2 } } \begin{pmatrix}
1 \\ -i 
\end{pmatrix}  \\
\ket{\psi}  & = \frac{1}{\sqrt[]{ 5 } } \begin{bmatrix}
i \\ 2
\end{bmatrix}
\end{align}
$$

#### Probability of getting $Y$ as $\frac{\hbar}{2}$
$$
\begin{align}
\left| \braket{ +y | \psi }  \right| ^{2} &  = \left| \frac{1}{\sqrt[]{ 2 } }(1, -i) \frac{1}{\sqrt[]{ 5 } } \begin{pmatrix}
i\\2
\end{pmatrix}\right| ^{2} \\
 & = \left| \frac{1}{\sqrt[]{ 10 } }( i-2i )\right| \left| \frac{1}{\sqrt[]{ 10 } } (-i+2i) \right|  \\
 & =\frac{1}{10}
\end{align}
$$

#### Probability of getting $X$ as $\frac{\hbar}{2}$
$$
\begin{align}
(\braket{ +x | \psi })^{2}  & = \left| \sqrt[]{ \frac{1}{2} } \begin{bmatrix}
1 & 1
\end{bmatrix}  \frac{1}{\sqrt[]{ 5 } } \begin{bmatrix}
i\\ 2
\end{bmatrix}\right| ^{2} \\
 & = \left| 
\sqrt[]{ \frac{1}{10}  }(i + 2) 
\right| ^{2}  \\
 & =\frac{1}{10} (i+2)(-i+2) \\
 & =\frac{1}{10} 5 \\
= \frac{1}{2}
\end{align}
$$

