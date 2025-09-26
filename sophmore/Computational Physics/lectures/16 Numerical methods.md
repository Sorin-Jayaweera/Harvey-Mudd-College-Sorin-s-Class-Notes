We can try to solve the Laplacian of some thing in cylindrical coordinates.
$$
\begin{align}
\nabla^{2}\Psi =0 \\
= \vec{\nabla} \cdot (\vec{\nabla} \Psi )
\end{align}
$$

In cartesian, its just $\left( \frac{ \partial^{2} }{ \partial x^{2} }+\frac{ \partial^{2} }{ \partial y^{2} }+\frac{ \partial^{2} }{ \partial z^{2} } \right)\Psi=0$
The Laplacian is the divergence of the gradient. 


In spherical, $\vec{\nabla}\Psi= \left( \hat{s} \frac{ \partial \\Psi }{ \partial s }+ \hat{\phi} \frac{1}{s}\frac{ \partial \Psi }{ \partial \phi }+ \hat{z} \frac{ \partial \Psi }{ \partial z } \right)\Psi$
$$
\begin{align}
\vec{\nabla}\cdot \vec{A}= \frac{1}{s} \frac{ \partial  }{ \partial s } (SA_{s} ) + \frac{1}{s} \frac{ \partial  }{ \partial \phi } (A\phi) + \frac{ \partial A_{z}  }{ \partial z }  \\
\end{align}
$$

Can we make sense of this $\frac{1}{s}$ term?
![[Pasted image 20250403094353.png|300]]


Anyways, now lets write our Laplacian Operator, with the equation we want to solve for $\Psi(x,y,z)$.
Let $\Psi(s,\phi,z)=S(s)\Phi(\phi)Z(z)$
$$
\begin{align}
\frac{1}{s} \frac{ d }{d s } \left( s \frac{ d S}{d s }  \right)\Phi Z + \frac{1}{s^{2}} \left( \frac{ d ^{2}\Phi}{d \phi^{2} }SZ + \frac{ d^{2} Z}{d z^{2} } S\Phi \right) 
\end{align}
$$
We're gonna do some work on this:
$$
\begin{align}
\frac{\left[\frac{1}{s} \frac{ d }{d s } \left( s \frac{ d S}{d s }  \right)\Phi Z + \frac{1}{s^{2}} \left( \frac{ d ^{2}\Phi}{d \phi^{2} }SZ + \frac{ d^{2} Z}{d z^{2} } S\Phi \right)\right]}{S\Phi Z} \\
= \frac{\frac{1}{s}\frac{ d }{d s } \left( s \frac{ d S}{d s }  \right)}{S} + \frac{1}{s^{2}} \frac{\Phi''}{\Phi} + \underbrace{ \frac{Z''}{Z} }_{ \alpha^{2} } = 0 
\end{align}
$$
We can argue that these have to be a constant. 

Because the function $\Phi$ must be single valued if we wrap around a circle, 
$$
\begin{align}
\frac{\Phi ''}{\Phi} = -n^{2}  \\
\Phi''+n^{2}\Phi=0\\
\text{ which has solutions } \\
\Phi(\phi) = \begin{cases}
\cos(n\phi)\\ \sin(n\phi)
\end{cases}
\end{align}
$$
Now we'll go back to the Laplacian:
$$
\begin{align}
\frac{1}{s} \frac{ d }{d s } \left( s \frac{ d S}{d s }  \right)= \left( \frac{n^{2}}{s^{2}} - \alpha^{2} \right)S \\
S'' + \frac{1}{s}S' + \left( \alpha^{2}-\frac{n^{2}}{s^{2}} \right)S = 0 \\
s^{2}S'' + sS' + (\alpha^{2}s^{2}-n^{2})S = 0
\end{align}
$$
That's (basically) Bessel's equation.

We want to simplify the $\alpha$ bit.

Let $\rho=\alpha s$
$\frac{ d }{d s }= \alpha\frac{ d }{d \rho }$

$$
\begin{align}
\alpha^{2}s^{2} \frac{ d ^{2}S}{d \rho^{2} }  + \frac{\rho}{\alpha}\alpha \frac{ d S}{d \rho } + \left( \rho^{2}-n^{2} \right) S=0 \\
\rho^{2} \frac{ d ^{2}}{d \rho^{2} }  + \rho \frac{ d S}{d \rho } + (\rho^{2}-n^{2})S=0
\end{align}
$$
When orbital angular momentum is 1, we can have $\phi$ dependence. We could have the ones running around the z axis, etc. Here $n$ is the same as the spherical harmonic $m_{l}$. 

How are we going to solve this equation?

This is has a regular singular  point.

Lets use the *Frobenius* solution. 
We guess
$$
\begin{align}
S(\rho) = \sum_{k=0}^{\infty}  a_{k} \rho^{k+l}
\end{align}
$$

Lets play around
$$
\begin{align}
\rho S' = \sum_{k=0}^{\infty} a_{k} (k+l)\rho^{k+l} \\
\rho^{2} s'' = \sum_{k=0}^{\infty} a_{k} (k+l)(k+l-1)\rho^{k+l}
\end{align}
$$
The $(-n^{2})S$ is going to look the same as a constant, but we have an odd duck -  $\rho^{2}S$.
$$
\begin{align}
\rho^{2}S= \sum_{k=0}^{\infty} a_{k} \rho^{k+l+2}
\end{align}
$$
Well... we can make a $k'=k+2$.
So we have 
$$
\begin{align}
\sum_{k'=2}^{\infty} a_{k'-2} \rho^{k'+l}
\end{align}
$$
$k'$ is a dummy index, so as long as we don't cheat and make our $a_{k'-2}$ be negative, we can substitute everything into the differential equation.

$$
\begin{align}
0 = \sum_{k=0}^{\infty}\underbrace{ \left[  a_{k} \left\{ (k+l)(k+l-1)+(k+1) - n^{2} \right\} + a_{k-2} \right] }_{ 0 } \rho^{k+l} 
\end{align}
$$
We just, again, have to be careful about the $a_{k-2}$. This is a power series for the variable $\rho$. All the rest are constants, which have to go to zero for this to be true.

We have a recurrence relation!
Lets solve when $n=0$ for the Bessel function, $[J_{0}(\rho)]$. These converge at the origin, but we could also look at Neuemann $[Y_{0}(\rho)]$ functions instead.

We pick $a_{0}=1$. We have terms in the series that are separated by two, and say nothing about the odds. We choose for the odds $a_{1}=0$, which will keep us at 0 for all odd numbers.

$$
\begin{align}
a_{k} \left[ (k+l^{2}) - \cancelto{ 0 }{ n^{2} }\right] + a_{k-2} =0 \\
\end{align}
$$
This says $(k+l)^{2}-n^{2}$ must be equal to $0$. When $k=0, l^{2}=n^{2}$, so 
$l=\pm n$.

$$
\begin{align}
a_{k}  = -\frac{a_{k-2}}{(k+l)^{2}}  \\
a_{k} = -\frac{a_{k-2}}{k^{2}} 
\end{align}
$$



