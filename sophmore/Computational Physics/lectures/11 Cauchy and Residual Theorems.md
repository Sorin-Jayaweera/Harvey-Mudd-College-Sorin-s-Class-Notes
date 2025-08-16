Recall:
$f(z=x+iy)=u(x,y)+i\nu(x,y)$

$$
\begin{align}
\lim_{ dx,dy \to 0 } \frac{f(x+\delta x,y+\delta y)-f(x,y)}{i\delta y+\delta x}
\end{align}
$$
We have the Cauchy Riemann condition:
$$
\begin{align}
\frac{ \partial u }{ \partial x } = \frac{ \partial \nu }{ \partial y }   \\
\frac{ \partial \nu }{ \partial x }  = - \frac{ \partial u }{ \partial y } 
\end{align}
$$

$$
\begin{align}
\frac{d}{dz} (z^{n}) =nz^{n-1} \\
\frac{ d \sin(z)}{d z } = \cos(z) \\
\frac{ d }{d z } (z^{*}) \text{ doesn't exist } 
\end{align}
$$
If a function $f(z)$ is differentiable in a region of the complex plane, we say it is analytic. 

E&M aside: We have a long wire coming out of the board with a current I flowing out of the board. Suppose we integrate $\oint_{c}\vec{B}\cdot \vec{dl}$ for a section that doesn't have $i$. $\mu_{0}I_{enc}=0$, so we get 0. If instead we had the current included, we would get $$
\begin{align}
\oint _{c'}\vec{B}\vec{dl} =\mu_{0}I
\end{align}
$$
This is a prelude to remind us of stokes theorem:
$$
\begin{align}
\iint (\vec{\nabla}\cdot \vec{B})\cdot \vec{dA} = \oint \vec{B}\cdot d\vec{l}
\end{align}
$$
This is breaking up the area inside the shape into a bunch of circling areas, which cancel out contributions form everywhere except at the boundary.  

Consider the $\hat{z}$ component of $\vec{\nabla}\times \vec{B}$:
$$
\begin{align}
\left( \vec{\nabla}\vec{x}\vec{B} \right) _{z} = \frac{ \partial  }{ \partial x } B_{y} - \frac{ \partial  }{ \partial y } B_{x} \\
\iint (\vec{\nabla}\times  \vec{B})_{z}dxdy=\oint \vec{B}\cdot \vec{dl}  \\
= \oint b_{x}dx+B_{y}dy \\
\iint \left( \frac{ \partial B_{y} }{ \partial x } -\frac{ \partial B_{x} }{ \partial y }  \right)dxdy = \oint (B_{x}dx+B_{y}dy)
\end{align}
$$
Cauchy's Theorem:
$$
\begin{align}  \\
\oint_{c}f(z)dz = 0 \text{ if } f(z) \text{ is analydic and in } \mathbb{C} \\
\oint _{c}\left[ u(x,y)+i\nu(x,y) \right] (dx+idy) = \oint _{c}\left[ udx-vdy \right] + i[udy+\nu dx]
\end{align}
$$
Use stokes theorem:
Let $B_{x}=U$, $B_{y}=-\nu$

$$
\begin{align}
\oint _{c} \left[ udx-\nu dy \right] = \iint \underbrace{ \left( \frac{d(-\nu)}{dx}  - \frac{du }{dy} \right) }_{ \frac{ \partial u }{ \partial x } =-\frac{ \partial u }{ \partial y } } dxdy = \iint 0 dxdy
\end{align}
$$
So we have the real part.

We can do the imaginary part:
let $u=B_{y},\nu=B_{x}$
$$
\begin{align}
\oint _{c}\left[ udy+\nu dx \right] = \iint \left(\underbrace{  \frac{ \partial u }{ \partial x }- \frac{ \partial \nu }{ \partial y }  }_{ 0 \text{ by Cauchy Riemann } } \right)dxdy
\end{align}
$$

We see that if we have nothing inside our surface, then we get nothing. But what happens if we have a point inside that is not analytic, where the function blows up - where we have 'current'?

$$
\begin{align}
\oint _{c} \frac{f(z)dz}{z-z_{0}}
\end{align}
$$
We can keep morphing our path by getting rid of anywhere that doesn't have the discontinuity (anywhere without just goes to zero, so we can chop away those paths and get down to just the path around the point we care about).

We get 
$$
\begin{align}
\oint _{c'} \frac{f(z)dz}{z-z_{0}}, \text{ where } z=z_{0}+\epsilon e^{i\phi}
\end{align}
$$
This gets us in a circle around the point.
$$
\begin{align}
I=\int_{0}^{2\pi} \frac{f(z_{0}+\epsilon e^{i\phi})}{\epsilon e^{i\phi}} dz, dz = \epsilon ie^{i\phi}d\phi \\
I=i\int_{0}^{2\pi} f(z_{0}+\epsilon e^{i\phi}) \, ~  d\phi \\
I = 2\pi f(z_{0})
\end{align}
$$

We have therefore have Cauchy's integral formula:
$$
\begin{align}
f(z_{0})= \frac{1}{2\pi i}\oint _{c} \frac{f(z)}{z-z_{0}}dz, \text{ f(z) } \text{ is analytic on and in  } \mathbb{C}
\end{align}
$$
This is funny - we can pick out the value of the function at a point by integrating that function around a discontinuity.

Lets do an easy example, then generalize to a hard one:

$$
\begin{align}
I = \int_{-\infty}^{\infty}  \frac{dx}{x^{2}+1}, 
\end{align}
$$
Where $x=\tan \phi, dx = \sec ^{2}\phi d\phi$.
$$
\begin{align}
\sec ^{2}=1+\tan ^{2}\phi
\end{align}
$$
$$
\begin{align}
I = \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \frac{\sec ^{2}\phi d\phi}{\sec ^{2}\phi} = \pi
\end{align}
$$
Can we use complex variables to get the same value?
Consider we use Cauchy to get this result?
$$
\begin{align}
\int \frac{dz}{1+z^{2}}
\end{align}
$$
We need to make a closed path to use the Cauchy stuff. But we are integrating along the x axis from $-\infty$ to $\infty$. Can we get away with closing at a big radius?
![[Pasted image 20250225103710.png|300]]
Wouldn't it be swell if we say that the integral along the path is zero? Then we just have to integrate along the real line. We'll have to justify this in a bit.

$$
\begin{align}
I=\oint_{c} \frac{dz}{1+z^{2}} \\
= \int_{-\infty}^{\infty} \frac{dx}{1+x^{2}}+ \int_{\text{ loop }} \frac{dz}{z^{2}+1}
\end{align}
$$
Can we show this second loop part goes to zero?
On that loop,
$$
\begin{align}
z=re^{i\phi} \\
dz = rie^{i\phi}
\end{align}
$$
We get
$$
\begin{align}
\int_{0}^{\pi } \frac{re^{i\phi}d\phi}{r^{2}e^{2i\phi}+1} \\
= \int \frac{id\phi}{re^{ i\phi }+\frac{1}{r}e^{ -i\phi }} \\
\frac{1}{r} \int_{0}^{\pi} \frac{id\phi}{e^{ i\phi }+\frac{1}{r^{2}}e^{ -i\phi }}
\end{align}
$$
This is just algebra so far, but lets analyze: R is really big, so the bottom term becomes just $e^{i\phi}$, so the internal part of the integral won't explode. As $r$ goes to infinity, then the integral must go to zero. This means that we can just take the integral that we want, on the real axis. 

Now we have to worry about where the function blows up on the interior: where are the poles of $\frac{1}{z^{2}+1}$? $z=\pm i$

$$
\begin{align}
\frac{1}{z^{2}+1} = \frac{1}{(z+i)(z-i)} \\
\oint \frac{1}{(z+i)(z-i)} dz \\
\end{align}
$$
We can partial fractions decompose:
$$
\begin{align}
\frac{a}{z+i}+\frac{b}{z-i}=\frac{1}{(z+i)(z-i)} \\
a+b=0 ~ -ai+bi=1,  \\
\implies b = \frac{1}{2i}, a= -\frac{1}{2i}
\end{align}
$$
So the integral becomes
$$
\begin{align}
\oint \left( \frac{-\frac{1}{2i}}{z+i} + \frac{\frac{1}{2i}}{z-i}\right) dz 
\end{align}
$$
According to our theorems before, we get the left bit is $0$ by the fact that it is analytic, and the right bit becomes $(2\pi i)\left(  \frac{1}{2i} \right)$ by the Cauchy integral formula.

Lets consider something new
$$
\begin{align}
J = \int_{-\infty}^{\infty} \frac{dx}{1+x^{4}}
\end{align}
$$
We'll have poles at $x^{4}=-1$
The value of the integral is just $2\pi i \text{ times the value of the function at those two poles }$

The residue theorem says that the integral of a closed contour on the complex plane is $2\pi i$ times the values of the residues, which are the values of the function at each place where it explodes.


Are there ways of making the function not analytic except for having poles?
They have to satisfy the Cauchy Riemann conditions. There are issues with things like the square root of $z$.