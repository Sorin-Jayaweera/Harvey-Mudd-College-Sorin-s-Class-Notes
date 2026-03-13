To the grader:
I'm dropping this homework, I did some of the problems but no where near all. 

![[Pasted image 20260303164134.png]]

## A

# TODO

## b



![[Pasted image 20260303164151.png]]

$$
\begin{align}
\left< S_{y}  \right> = tr(\hat{S}_{y} \hat{p}) \\
p _{ij}= \braket{ i | \psi } \braket{ \psi | j } 
\end{align}
$$

## A
$\frac{3}{4}$ - the trace has to add to $1$ for any ensemble. 

## B


We know that for a pure state, $\hat{\rho}^{2}=\hat{\rho}$.
$$
\begin{align}
\rho=\rho \rho & = \begin{pmatrix}
\frac{1}{4} & n \\
n^{*} & \frac{3}{4}
\end{pmatrix}\begin{pmatrix}
\frac{1}{4} & n \\
n^{*} & \frac{3}{4}
\end{pmatrix} \\ 
 & =\begin{pmatrix}
\frac{1}{16}+ n^{*}n & n \\
n^{*} & n^{*}n + \frac{9}{16}
\end{pmatrix}
\end{align}
$$
This tells us that $n^{*}n = \frac{3}{16}$

with any complex phase, so
$$
\begin{align}
n = \frac{\sqrt[]{ 3 }}{4}e^{i\phi} 
\end{align}
$$
The density matrix is now
$$
\begin{align}
\begin{bmatrix}
\frac{1}{4} & \frac{\sqrt[]{ 3 }}{4}e^{i\phi} \\
\frac{\sqrt[]{ 3 }}{4}e^{-i\phi} & \frac{3}{4} 
\end{bmatrix}
\end{align}
$$

## C

The maximum possible real value is $n= \frac{\sqrt[]{ 3 }}{4}$
We know that a general state
$$
\begin{align}
\ket{n} = \cos \frac{\theta}{2} \ket{+z} + e^{i\phi}\sin \frac{\theta}{2}\ket{-z} 
\end{align}
$$

We can compare this with 
$$
\begin{align}
\begin{bmatrix}
\frac{1}{4} & \frac{\sqrt[]{ 3 }}{4}e^{i\phi} \\
\frac{\sqrt[]{ 3 }}{4}e^{-i\phi} & \frac{3}{4} 
\end{bmatrix}
\end{align}
$$
The diagonal terms of the density matrix with $\ket{n}$ are $\ket{+z}\bra{+z}$, so we just have the elements squared. 
$$
\begin{align}
\cos ^{2} \frac{\theta}{2}= \frac{1}{4} \\
\cos \theta = \frac{1}{2} \\ \\
\sin ^{2} \frac{\theta}{2} = \frac{3}{4} \\
\sin \frac{\theta}{2} = \frac{\sqrt[]{ 3 }}{2} 
\end{align}
$$


because we have the largest real value, $\phi=0$, so we have the state
$$
\begin{align}
\ket{n}= \frac{1}{2}\ket{+z} + \frac{\sqrt[]{ 3 }}{2} \ket{-z} 
\end{align}
$$




![[Pasted image 20260303164219.png]]

We have the elements of the density matrix as
$$
\begin{align}
\begin{bmatrix}
\ket{x,x} \bra{x,x}   & 
\ket{x,x} \bra{y,y}  \\
\ket{y,y} \bra{x,x}   & 
\ket{y,y} \bra{y,y} 
\end{bmatrix}
\end{align}
$$
Or is it
$$
\boxed{
\begin{align}
\begin{bmatrix}
\ket{x,x} \bra{x,x}   & 
\ket{x,x} \bra{y,y}   & 
\ket{y,y} \bra{x,x}   & 
\ket{y,y} \bra{y,y}  &  \\
\text{ stuff } \\
\dots
\end{bmatrix}
\end{align}
}
$$
Or do we have
$$
\begin{align}
\begin{bmatrix}
\ket{x}\bra{x} \ket{x} \bra{x}  & \ket{x} \bra{x} \ket{x} \bra{y} & \ket{x} \bra{y} \ket{x} \bra{x}  & \ket{x} \bra{y} \ket{x} \bra{y}  \\
etc
\end{bmatrix} 
\end{align}
$$


# TODO




![[Pasted image 20260303164235.png]]

## a
We have $\frac{1}{2}$ of each state, so
$$
\begin{align}
\rho = \frac{1}{2} \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
\end{align}
$$
## b
We have the exact scenario in the $\ket{n}$ basis, since $\rho = \sum_{i}^{}p_{i}\ket{\psi _{i}}\bra{\psi _{i}}$
So it looks the same,
$$
\begin{align}
\rho = \frac{1}{2}\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
\end{align}
$$
## C

I don't think we would be able to tell, since we could measure in any basis and these two mixes look the exact same. 

Maybe if time evolution were dependent on state polarization - like a magnetic field in some direction, but I don't think so since the states are identical. 
$$
\begin{align}
\frac{ d }{d t } \hat{\rho}(t)= \frac{1}{i\hbar}[\hat{H}(t),\rho(t)]
\end{align}
$$






![[Pasted image 20260311093217.png]]
## a
For $n=1$, we have
$$
\begin{align}
[\hat{x}^{1},\hat{p}_{x} ]= i\hbar
\end{align}
$$
For $n=2$, we have
$$
\begin{align} \\
[\hat{x}^{n},\hat{p}_{x} ] & = \\
[x x^{n-1},\hat{p}_{x} ] &  = \hat{x}[\hat{x}^{n-1},\hat{p}_{x} ]+ [\hat{x},\hat{p}_{x} ]x^{n-1} \\
 & = \hat{x}[\hat{x}^{1},\hat{p}_{x} ]+ [\hat{x},\hat{p}_{x} ] x^{1} \\
 & =2 i\hbar x
\end{align}
$$
for $n=3$
$$
\begin{align}
[xx^{n-1},\hat{p}_{x} ]  & = \hat{x}[\hat{x}^{n-1},\hat{p}_{x} ]+ [\hat{x},\hat{p}_{x} ]x^{n-1}  \\
 & = \hat{x}[\hat{x}^{2},\hat{p}_{x} ]+ [\hat{x},\hat{p}_{x} ]\hat{x}^{2}
\end{align}
$$
$$
\begin{align}
  \hat{x}(2i\hbar \hat{x}^{2}) + i\hbar \hat{x}^{2} \\
 = 3 i\hbar \hat{x}^{2}
\end{align}
$$
We can show that this result holds inductively
$$
\begin{align}
[xx^{n-1},\hat{p}_{x} ]  & = \hat{x}[\hat{x}^{n-1},\hat{p}_{x} ]+ [\hat{x},\hat{p}_{x} ]x^{n-1}   \\
 & = \hat{x} (\hat{x}[\hat{x}^{n-2},\hat{p}_{x} ]+ [\hat{x},\hat{p}_{x} ]x^{n-2} )+ [\hat{x},\hat{p}_{x} ]x^{n-1} \\
 & = \vdots
\end{align}
$$
Where for $n=1$, we get $2i\hbar x$ which propagates forwards.
For any $n$, we can plug in the result from the previous for the first term of the expansion, which will have the form
$$
\begin{align}
\hat{x}[\hat{x}^{n-1},\hat{p}_{x} ]= (n-1)i\hbar \hat{x}^{n-1}
\end{align}
$$
as well as 
$$
\begin{align}
[\hat{x},\hat{p}_{x} ]\hat{x}^{n-1} & =i\hbar \hat{x}^{n-1}
\end{align}
$$
The sum of these two is just
$$
\begin{align}
[\hat{x}^{n},\hat{p}_{x} ]=i\hbar nx^{n-1}
\end{align}
$$

## B
![[Pasted image 20260311093144.png]]
# TODO:
how do we know eigenvalues of $\hat{x}$ are being fed in? 
## C
![[Pasted image 20260311093201.png]]
We can rearrange the Hamiltonian, and have derivatives in space and derivatives in time with separation of variables. Those must be constant (because they aren't in terms of the other). We get
$$
\begin{align}
\frac{1}{2m} \frac{ d \hat{p}^{2}_{x} }{d t } = - \frac{ d V(\hat{x})}{d x }  \\
\end{align}
$$
# TODO




![[Pasted image 20260303164300.png]]




![[Pasted image 20260303164311.png]]
$$
\begin{align}
\braket{ x | \psi(t) } = \int dp\, e^{-i p^{2}t/2m\hbar}\braket{ x | p } \braket{ p | \psi(0) } 
\end{align}
$$
We can pull out constants and evaluate

$$
\begin{align}
\braket{ x | p } = N e^{\frac{i p x}{\hbar}} = \sqrt[]{ \frac{1}{2\pi \hbar} } e^{\frac{ipx}{\hbar}}
\end{align}
$$
![[Pasted image 20260311110133.png|300]]

$$
\begin{align}
\braket{ p | \psi(0) } &  = \tilde{\psi}(0)  \\
 & =\int \frac{1}{2\pi \hbar}e^{\frac{-ipx}{\hbar}}\braket{ x | \psi(0) } 
\end{align}
$$

$$
\begin{align}
\braket{ x | \psi(t) } = \frac{1}{\sqrt[]{ \sqrt[]{ \pi } a } } \int dp \sqrt[]{ \frac{1}{2\pi \hbar} } e^{\frac{ipx}{\hbar}}
\end{align}
$$
For reference:
![[Pasted image 20260310235718.png|500]]
![[Pasted image 20260310235835.png|500]]

## B
# TODO


![[Pasted image 20260303164331.png]]

## A



## B

# TODO


![[Pasted image 20260303164340.png]]

Infinitely high barriers, infinitely thin well. 
page 243






