![[Pasted image 20250212175015.png]]
A) The particle can be spin up or spin down along z, so we have a two dimensional space. We have a linear combination of the two states, spin up or down, to represent the actual spin in $\mathbb{R}^{2}$.
$\begin{pmatrix}1\\0\end{pmatrix}$ means spin up along z, $\begin{pmatrix}0\\1\end{pmatrix}$ is spin down along z, with the levels of each vector being determined by $\phi$.

B) We know that

$$
\begin{align}
e^{x}\approx 1+\frac{x}{1} + \frac{x^{2}}{2!}+\frac{x^{3}}{3!}+\dots
\end{align}
$$
We can write this for the matrix as an argument. 

Simplifying the exponent first
$$
\begin{align}
e^{\frac{i\hat{S}_{x}\phi}{\hbar}} & = e^{\frac{i\phi}{2}x}\\
 & = 1+\frac{i\phi x}{2} + \frac{\left( \frac{i\phi x}{2} \right)^{2}}{2} + \frac{\left( \frac{i\phi x}{2} \right) ^{3}}{3!}+\dots
\end{align}
$$
We can simplify this out to be
$$
\begin{align}
=1+\frac{i\phi}{2} \begin{bmatrix}
0 & 1 \\ 1 & 0
\end{bmatrix} + \frac{i^{2}\phi^{2}}{2^{2}} \begin{bmatrix}
1 & 0\\0 & 1
\end{bmatrix}\frac{1}{2} + \frac{i^{3}\phi^{3}}{2^{3}} \begin{bmatrix}
0 & 1\\1 & 0
\end{bmatrix} \frac{1}{6} +\dots
\end{align}
$$
This gives us the series expression
$$
\begin{align}
e^{\frac{i\hat{S}_{x}\phi}{\hbar}}= \sum_{n=0 }^{\infty} \left( \frac{i\phi}{2} \right) ^{2n+1} \frac{1}{(2n+1)!} \begin{bmatrix}
0 & 1\\1 & 0
\end{bmatrix} + \sum_{n=0}^{\infty} \left( \frac{i\phi}{2} \right) ^{2n} \frac{1}{(2n)!} \begin{bmatrix}
1 & 0\\0 & 1
\end{bmatrix}
\end{align}
$$
We can express the second term as
$$
\begin{align}
\begin{bmatrix}
1 & 0  \\
0 & 1
\end{bmatrix} \left( 1- \frac{\left( \frac{\phi}{2} \right)^{2}}{2!}+\frac{\left( \frac{\phi}{2} \right)^{3} }{3!} -\dots \right) 
\end{align}
$$
We see that this looks like cos, so this term becomes
$$
\begin{align}
\begin{bmatrix}
1 & 0\\0 & 1
\end{bmatrix} \cos \left( \frac{\phi}{2} \right) 
\end{align}
$$
The other term similarly looks like $-i\sin\left( \frac{\phi}{2} \right)$

This gives us 
$$
\boxed{
\begin{align}
\hat{R}_{x}(\phi) = \cos \left( \frac{\phi}{2} \right) \hat{\mathbb{I}} - i\sin\left( \frac{\phi}{2} \right) \mathbb{\hat{X}}
\end{align}
}
$$
We can now show that
$$
\begin{align}
\hat{R}_{x}(\phi)\hat{R}_{x}(\phi)^{\dagger}=\hat{\mathbb{I}} \\
\end{align}
$$
First, we must find $\hat{R}_{x}(\phi)^{\dagger}$

$$
\begin{align}
\hat{R}_{x}(\phi)=\begin{bmatrix}
\cos\left( \frac{i\phi}{2} \right) & -i\sin\left( \frac{\phi}{2} \right)\\  -i\sin\left( \frac{\phi}{2} \right) & \cos\left( \frac{i\phi}{2} \right) 
\end{bmatrix}
\end{align}
$$
We see that this is symmetric, so 
$$
\begin{align}
\hat{R}_{x}(\phi)^{T} = \hat{R}_{x}(\phi)
\end{align}
$$
We take the conjugate to get
$$
\begin{align}
\hat{R}_{x}(\phi)^{\dagger} = 
\begin{bmatrix}
\cos\left( -\frac{i\phi}{2} \right) & i\sin\left( \frac{\phi}{2} \right) \\
i\sin\left( \frac{\phi}{2} \right) & \cos\left( -\frac{i\phi}{2} \right)
\end{bmatrix}
\end{align}
$$
We can now multiply these two to find


$$
\begin{align}
\hat{R}_{x}(\phi)\hat{R}_{x}(\phi)^{\dagger} =\begin{bmatrix}
\cos\left( \frac{i\phi}{2} \right) & -i\sin\left( \frac{\phi}{2} \right)\\  -i\sin\left( \frac{\phi}{2} \right) & \cos\left( \frac{i\phi}{2} \right) 
\end{bmatrix} 
\begin{bmatrix}
\cos\left( -\frac{i\phi}{2} \right) & i\sin\left( \frac{\phi}{2} \right) \\
i\sin\left( \frac{\phi}{2} \right) & \cos\left( -\frac{i\phi}{2} \right)
\end{bmatrix}

\end{align}
$$

$$
\begin{align}
= \begin{bmatrix}
\cos\left( \frac{i\phi}{2} \right)\cos\left( -\frac{i\phi}{2} \right)+\sin ^{2}\left( \frac{\phi}{2} \right) & i\sin\left( \frac{\phi}{2} \right)\cos\left( \frac{\phi}{2} \right)-i\sin\left( \frac{\phi}{2} \right)\cos\left( \frac{\phi}{2} \right) \\
-i\sin\left( \frac{\phi}{2} \right)\cos\left( -\frac{i\phi}{2} \right)+i\sin\left( \frac{\phi}{2} \right)\cos\left( -\frac{i\phi}{2} \right) & \sin ^{2}\left( \frac{\phi}{2} \right)+\cos\left( \frac{i\phi}{2} \right)\cos\left( -\frac{i\phi}{2} \right)
\end{bmatrix}
\end{align}
$$
$$
\begin{align}
= \begin{bmatrix}
\cos\left( \frac{i\phi}{2} \right)\cos\left( -\frac{i\phi}{2} \right)+\sin ^{2}\left( \frac{\phi}{2} \right) & 0 \\
0 & \sin ^{2}\left( \frac{\phi}{2} \right)+\cos\left( \frac{i\phi}{2} \right)\cos\left( -\frac{i\phi}{2} \right)
\end{bmatrix}
\end{align}
$$

Because cosine is symmetric, this reduces to have each term as
$$
\begin{align}
\cos ^{2}\left( i\frac{\phi}{2} \right)+\sin ^{2}\left( \frac{i\phi}{2} \right) = 1
\end{align}
$$
So the matrix becomes
$$
\begin{align}
\begin{bmatrix}
1 & 0\\0 & 1
\end{bmatrix}
\end{align}
$$
Therefore,
$$
\begin{align}
\hat{S}_{x}(\phi)\hat{S}_{x}(\phi)^{\dagger} = \hat{\mathbb{I}}
\end{align}
$$

![[Pasted image 20250212175028.png]]
We have the relationship
$$
\begin{align}
\Delta t=\frac{1}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}\Delta \tau
\end{align}
$$

This factor $\gamma$ is the ratio between $\Delta \tau \text{ and } \Delta t$
$$
\begin{align}
\gamma = \frac{\Delta t}{\Delta \tau}= \frac{1}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}
\end{align}
$$
$dt=\gamma d\tau$
$$
\begin{align}
\sqrt{ 1-\phi^{2} }dt = d\tau
\end{align}
$$


![[Pasted image 20250212175047.png]]
$V$ is velocity of the $s'$ frame relative to the s frame, $v'$ is the velocity in that $s'$ frame.


In the ship's local frame, with acceleration $g$, we would observe (for small $\Delta \tau$) that $\Delta v'=g\Delta \tau$
$$
\begin{align}
dv'=gd \tau
\end{align}
$$

This gives us the change in the ship's velocity in the Earth's frame as the difference between the new velocity and the velocity of the stationary frame (i.e. if the ship weren't accelerating)

$$
\begin{align}
\Delta v = \frac{V+g\Delta \tau}{1+\frac{V g\Delta \tau}{c^{2}}}-V
\end{align}
$$
$$
\begin{align}
\Delta v = \frac{Vc^{2}+g\Delta \tau c^{2}}{c^{2}+Vg\Delta \tau}-\frac{Vc^{2}+V^{2}g\Delta \tau}{c^{2}+Vg\Delta \tau} \\
\Delta V = \frac{g\Delta \tau c^{2}-V^{2}g\Delta \tau}{c^{2}+Vg\Delta \tau} \\
\Delta V = \frac{\Delta \tau(gc^{2}-V^{2}g)}{c^{2}+Vg\Delta \tau}
\end{align}
$$
4
$$
\begin{align}
\Delta v = \frac{\Delta \tau(gc^{2}-V^{2}g)}{c^{2}+Vg\Delta \tau} \\
\Delta v(c^{2}+Vg\Delta \tau) =  \Delta \tau\left( gc^{2} -V^{2}g\right) \\
\end{align}
$$

We can take the limit as $\Delta V\text{ and } \Delta T$ become very small, so that many of these terms will disappear magically:
$$
\begin{align}
\frac{dv}{d \tau}  =g\left( 1-\frac{V^{2}}{c^{2}} \right) \\

\frac{dv}{d \tau}  =g\left( 1- \tanh^{2}(\phi) \right)
\end{align}
$$


![[Pasted image 20250212175058.png]]
We can do this in steps: 
1) $dt\leftrightarrow d \tau$
2) $dv\leftrightarrow d \tau$
3) $\phi \leftrightarrow v$
4) $d\phi \leftrightarrow dv$
5) using 1,2 we can get $dt\leftrightarrow dV$
6) using 2 and 4, we can get $d\phi \leftrightarrow d \tau$
7) We can integrate that to get $\phi \leftrightarrow \tau$
We can separate out our expression from (B)
$$
\begin{align}
dv= g\left( 1-\frac{v^{2}}{c^{2}}\right)d \tau
\end{align}
$$


We know $\tanh \phi=\frac{V}{c}$
$$
\begin{align}
dv = c sech^{2}\phi ~ d\phi = g~sech ^{2}\phi ~ d\tau \\
d\phi = \frac{g}{c}d\tau
\end{align}
$$
We see that this grows linearly in time. 

We can integrate,
$$
\boxed{
\begin{align}
\phi= \frac{g}{c}\tau
\end{align}
}
$$
We also have 
$$
\begin{align}
dt = \frac{d\tau}{\sqrt{ 1-tanh(\phi)^{2} }}\\
dt = \frac{d\tau}{\sqrt{ 1-tanh\left( \frac{g\tau}{c} \right)^{2} }}
\end{align}
$$

We can integrate that
$$
\begin{align}
dt  & = \frac{d\tau}{sech\left( \frac{g\tau}{c} \right) } \\
T  & = \int \cosh\left( \frac{g\tau}{c} \right)d\tau \\
T  & = \sinh\left( \frac{g\tau}{c} \right) \frac{c}{g} \\
\end{align}
$$

![[Pasted image 20250212175110.png]]

The time to get to the first half was 45 months, $= 1.183*10^{8}$ seconds in the ships frame.

We have that 
$$
\begin{align}
dv= g~sech ^{2}\phi ~ d\tau
\end{align}
$$
We can rearrange and integrate this to get velocity with respect to ship's time:

$$
\begin{align}
dv  & = g ~ sech^{2}\phi ~ d \tau \\
\int dv  & = \int g ~ sech ^{2}\left( \frac{g}{c} \tau \right) d\tau \\
v  & = c \tanh ^{2}\left( \frac{g}{c}\tau \right)
\end{align}
$$
We can integrate this velocity over the half - traveling time to get the half distance.
$$
\begin{align}
d = \int_{0}^{\frac{\tau}{2}} c \tanh ^{2}\left( \frac{g}{c}\tau \right)d\tau 
\end{align}
$$
$$
\begin{align}
d = c\tau - \frac{c\tau}{g}\tanh\left( \frac{g}{c}\tau \right)
\end{align}
$$
We can plug in these values
$$
\begin{align}
\frac{d}{2} = 3.312 \times  10^{16} \text{ meters }
\end{align}
$$
This gets us the distance, in light years, as
$7$ light years.

![[Pasted image 20250212175119.png]]

We can transform the time from $\tau$ Ceti to earth with:

$$
\begin{align}
T  & = \sinh\left( \frac{g\tau}{c} \right) \frac{c}{g}  \\
T  & = 3.705*10^{9} \text{ seconds } \\
 & = 117.5 \text{ years in earths frame}
\end{align}
$$





![[Pasted image 20250212175130.png]]

## A
If $f(x)$ is odd, then we have the condition that $f(x)=-f(-x)$
We can write this out with the Fourier representation to show that
$$
\begin{align}  
 \sum_{n=-\infty}^{\infty} a_{n}e^{\frac{n\pi ix}{l}} = -\sum_{n=-\infty}^{\infty} a_{n}e^{\frac{-n\pi ix}{l}}
\end{align}
$$

We can define a new variable for this sum, $m=-n$

We can distribute the negative sign and set the insides equal to each other.
$$
\begin{align}  
 \sum_{n=-\infty}^{\infty} a_{n}e^{\frac{n\pi ix}{l}} = \sum_{m=\infty}^{-\infty} -a_{n}e^{\frac{m\pi ix}{l}}
\end{align}
$$

It is now apparent that, for $f$ to be odd, $a_{n}=-a_{-n}$.


## B
If $f(x)$ is even, then we have the condition that $f(x)=f(-x)$
We can write this out with the Fourier representation to show that
$$
\begin{align}  
 \sum_{n=-\infty}^{\infty} a_{n}e^{\frac{n\pi ix}{l}} = \sum_{n=-\infty}^{\infty} a_{n}e^{\frac{-n\pi ix}{l}}
\end{align}
$$

We can define a new variable for this sum, $m=-n$

We can distribute the negative sign and set the insides equal to each other.
$$
\begin{align}  
 \sum_{n=-\infty}^{\infty} a_{n}e^{\frac{n\pi ix}{l}} = \sum_{m=\infty}^{-\infty} a_{n}e^{\frac{m\pi ix}{l}}
\end{align}
$$
It is now apparent that, for $f$ to be even, $a_{n}=a_{-n}$.

## C

If $f(x)$ is real, then we have the condition that $f(x)^{2}=f(x)f^{*}(x)$
We can write this out with the Fourier representation to show that
$$
\begin{align}  
 \left( \sum_{n=-\infty}^{\infty} a_{n}e^{\frac{n\pi ix}{l}}  \right)^{2} = \left( \sum_{n=-\infty}^{\infty} a_{n}e^{\frac{n\pi ix}{l}}  \right)\left( \sum_{n=-\infty}^{\infty} a_{n}e^{\frac{n\pi ix}{l}}  \right)^{*} \\
\end{align}
$$
We can rewrite this second term as
$$
\begin{align}
\sum_{m=\infty}^{-\infty} a_{m}e^{n\pi ix}
\end{align}
$$
Where $m=-n$. The imaginary terms cancel, which gets us
$$
\begin{align}
\left( \sum_{n=-\infty}^{\infty} a_{n}^{2}  \right)^{2} = \left( \sum_{n=-\infty}^{\infty} a_{n}a_{-n}^{*}\right) \\
\end{align}
$$



We can see that this is only true if
$$
\begin{align}
a_{n}^{2}=a_{n}a_{-n}^{*}, \\
\text{ that is }, a_{n}=a_{-n}^{*}
\end{align}
$$

## D

We proved that if a function is even, then
$a_{n}=a_{-n}$.
We proved that if a function is real, then 
$a_{-n}=a_{n}^{*}$
Therefore, if a function is real and imaginary,
$$
\begin{align}
a_{n}=a_{-n}=a_{n}^{*}
\end{align}
$$

## E


We have proven that if the function is odd, then
$$
\begin{align}
a_{-n} = -a_{n}
\end{align}
$$
If a function is imaginary, then 
$$
\begin{align}
a_{n}^{*}=-a_{n}
\end{align}
$$
This gives us
$$
\begin{align}
a_{-n}=-a_{n}=a^{*}
\end{align}
$$

![[Pasted image 20250212175140.png]]

We can write out the generic Fourier series as

$$
\begin{align}
f(x) = \sum_{n=0}^{\infty} a_{n}\sin\left( \frac{n\pi x}{L} \right) \\
a_{0} = 0, \text{ since we don't have a constant } \\

\end{align}
$$
We can find each successive value of $a_{n}$ as

$x(L-x)=\sum_{n=1}^{\infty}a_{n}\sin\left( \frac{n\pi x}{L} \right)$
We want a method of getting a single one of these terms, so we multiply the whole thing by $\sin\left( \frac{m\pi x}{L} \right)$

We get 
$$
\begin{align}
\int_{0}^{L} [x(L-x)]\sin\left( \frac{m\pi x}{L} \right) = \int_{0}^{L} a_{m}\sin ^{2}\left( \frac{m\pi x}{L} \right) \\
\text{ integrate this by parts }=a_{m}\frac{L}{2} \\
\end{align}
$$
$$
\begin{align}
\int_{0}^{L} x(L-x)\sin \frac{m\pi x}{L} \\
= \underbrace{ -x(L-X) \frac{L}{m \pi}\cos }_{ 0 }\left( \frac{m\pi x}{L} \right) \bigg|_{0}^{L} + \int_{0}^{L} \frac{l}{m\pi}(L-2x)\cos\left( \frac{m\pi X}{L} \right)dx  \\
= \underbrace{ \frac{\frac{L}{m\pi}(L-2x)L}{m\pi}\sin\left( \frac{m\pi x}{L} \right) }_{ 0 }\bigg|_{0}^{L}  - \int_{0}^{L} -\frac{2L}{m\pi} \frac{L}{m\pi}\sin\left( \frac{m\pi x}{L} \right) dx \\
= 2\left( \frac{L}{m\pi} \right)^{3}\left( -\cos\left( \frac{m\pi x}{L} \right) \right)\int_{0}^{L}  \\
= 2 \left( \frac{L}{m\pi} \right)^{3} (1-\cos(m\pi)) \\
= 2 \left( \frac{L}{m\pi} \right)^{3} (1-(-1)^{m})
\end{align}
$$
We have now, that
$$
\begin{align}
\frac{a_{m}L}{2}= 2 \left( \frac{L}{m\pi} \right)^{3} (1-(-1)^{m}) \\
\implies a_{m} = \frac{4L^{2}}{(m\pi)^{3}} (1- (-1)^{m})
\end{align}
$$

We, therefore, have
$$
\begin{align}
f(x) = \sum_{n=1}^{\infty} a_{m}\sin\left( \frac{n\pi x}{L} \right) \\
\end{align}
$$
We can evaluate this at $x=\frac{L}{2}$
This gives us
$$
\begin{align}
f\left( \frac{L}{2} \right) = \sum_{n=1}^{\infty} \frac{4L^{2}}{\left( m\pi \right) ^{3}}(1-(-1)^{n}) \sin\left( \frac{n\pi}{2} \right)
\end{align}
$$
For values $n=0,2,4$ this will be zero, so we only have odd values of $n$.
Therefore, $\left( -1 \right)^{n}=-1$. The sin term will flip signs every other odd $n$.
We can evaluate $f\left( \frac{L}{2} \right)$

$$
\begin{align}
\frac{L}{2}\left( L-\frac{L}{2} \right) = \frac{L^{2}}{4}
\end{align}
$$

We have
$$
\begin{align}
\frac{L^{2}}{4} = \sum_{n=1, odd}^{\infty}- \frac{8L^{2}}{n^{3}\pi^{3}} (-1)^{n}\\
\pi^{3}=32\sum_{n=1,odd}^{\infty} \frac{(-1)^{n+1}}{n^{3}}
\end{align}
$$
$$
\begin{align}
\pi^{3}=32 \left( 1 - \frac{1}{27}+\frac{1}{125}\dots \right)
\end{align}
$$
![[Pasted image 20250217135150.png]]
$$
\begin{align}
\left< f\left( \frac{L}{2} \right),f\left( \frac{L}{2} \right) \right> \\ 
\end{align}
$$
We can first do this with the normal $F\left( \frac{L}{2} \right)^{2}$

$$
\begin{align}
f\left( \frac{L}{2} \right)^{2} = \sum_{n=1}^{\infty} \frac{32L^{4}}{\left( m\pi \right) ^{6}} \sin ^{2}\left( \frac{n\pi}{2} \right)
\end{align}
$$
This will always be positive.

$f\left( \frac{L}{2} \right)^{2} = \left( \frac{L}{2}\right)^{4}$
This gives us
$$
\begin{align}
\pi^{6}= \sum_{n=1,odd}^{\infty} \frac{512}{n^{6}} \\
\pi^{6} = 512\left( 1+\frac{1}{64}+ \frac{1}{729} + \dots\right)
\end{align}
$$

