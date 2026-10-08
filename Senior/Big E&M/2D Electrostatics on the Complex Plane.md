
on $\mathbb{C}^{2}$

Lets take a number $z=x+iy$, with angle (argument) $\alpha$ and length $\left| z \right|= (z^{*}z)^{\frac{1}{2}}$, and $z^{*} = x-iy$. 

We can have functions of complex variables, so we think of functions $\Omega(z,z^{*})$. Something magical happens when we think of functions which only depend on z -$\Omega(z)$.
$$
\begin{align}
\frac{ d \Omega}{d z^{*} } = & 0
\end{align}
$$


if we have 
$$
\begin{align}
\Omega = u + i \nu \\
\frac{ \partial \Omega }{ \partial z^{*} } = 0  \\
\implies \left( \frac{ \partial  }{ \partial x } + i \frac{ \partial  }{ \partial y }  \right)(u + i\nu) = 0
\end{align}
$$
This is the chain rule. We therefore have
$$
\begin{align}
\frac{ \partial  }{ \partial z^{*} } = \frac{ \partial x }{ \partial z^{*} } \frac{ \partial  }{ \partial x } + \frac{ \partial y }{ \partial z^{*} } \frac{ \partial  }{ \partial y } 
\end{align}
$$

The inverse relationships of $x$ and $y$ for $z$ and $z^{*}$ are
$$
\begin{align}
x = \frac{z+z^{*}}{2}, y = \frac{z-z^{*}}{2i}
\end{align}
$$
Using this, we have
$$
\begin{align}
\frac{ \partial  }{ \partial z^{*} } = \frac{1}{2}\frac{ \partial  }{ \partial x } + \frac{i}{2} \frac{ \partial  }{ \partial y } 
\end{align}
$$
We have two things that should sum to zero seperately:
$$
\begin{align}
\frac{ \partial u }{ \partial x } + i \frac{ \partial \nu }{ \partial x } + i \frac{ \partial u }{ \partial y } - \frac{ \partial \nu }{ \partial y } =0 \\
\frac{ \partial u }{ \partial x } = \frac{ \partial \nu }{ \partial y } \text{ and } \frac{ \partial \nu }{ \partial x } = - \frac{ \partial u }{ \partial y }   
\end{align}
$$

Lets take a derivative of each of these terms
$$
\begin{align}
\frac{ \partial^{2}u }{ \partial x^{2} } = \frac{ \partial^{2}\nu }{ \partial x\partial y } \\
\frac{ \partial^{2}\nu }{ \partial y\partial x } = - \frac{ \partial^{2}u }{ \partial y^{2} }   
\end{align}
$$
That means that
$$
\begin{align}
\frac{\partial^{2}\nu}{\partial x^{2}}+ \frac{\partial^{2}u}{\partial y^{2}} = 0
\end{align}
$$
This is laplaces equation! The Laplaces equation that we have been solving before is just the real part of this holomorphic function! 

On the complex plane, differential equations become algebraic equations.


If we say that $\phi=\mathrm{Re}(\Omega)$, we can use holomorphic equations. We don't need to solve the PDE, and just have an algebraic problem for boundary conditions. 

I was too lazy to tex up contour integration again, see Phys 64 notes if you care. Also photos: 
![[20261008_100540.jpg]]

![[Pasted image 20261008100715.png]]


![[Pasted image 20261008100754.png]]



Now on to physics


We have a domain on the $Z$ plane with some arbitrary contour and a region $D$. We want to solve
$$
\begin{align}
\vec{\nabla}\phi=0
\end{align}
$$
with some arbitrary boundary condition
![[20261008_100844.jpg]]

The general boundary condition can be written
$$
\begin{align}
A(t)\phi(t) + B(t) \frac{ \partial \phi }{ \partial n } (t)= C(t)
\end{align}
$$

If we have $B=0$, Dirichlet. If $A=0$, Neumann. 

Lets define a box with grounded sides, an open top, and a potential at the bottom. The sides are
$$
\begin{align}
\Gamma_{1}  & &  z= iy,  & &  y>0 \\
\Gamma_{2}  & &  z= b+iy &  & y>0 \\
\Gamma_{3}  &  & z=x  & & 0<x<b
\end{align}
$$

We want the potential to be 0 at $\Gamma_{1}\text{ and } \Gamma_{2}$, and $\phi_{0}$ at $\Gamma_{3}$.

$$
\begin{align}
e^{i\pi \frac{z}{b}} \in  \mathbb{R}^{} \text{ on } \Gamma_{1} \text{ and } \Gamma_{2} 
\end{align}
$$

On $\mathbb{C}$, 
$$
\begin{align}
\ln (z) = \ln \left| z \right|  + i \, \mathrm{arg}(z) \\
\end{align}
$$

For $\Gamma_{1}\text{ and } \Gamma_{2}$, we need something real. We can define 
$$
\begin{align}
\Omega = i \ln e^{i\pi z/b}
\end{align}
$$
The imaginary part is zero, so the $\Omega$ as defined vanishes at $\Gamma_{1}$ and $\Gamma_{2}$.

On $\Gamma_{3}$, we set $z=x$ (so real). 
$$
\begin{align}
\mathrm{Re}\Omega = \mathbb{R} i\ln e^{i\pi x/b} \\
= \mathrm{Re} i\left( \cancelto{ 0 }{ \ln 1 } + \frac{i\pi x}{b} \right) = -\frac{\pi x}{b} ?????\to   \phi_{0}????
\end{align}
$$
UH OH. We satisfied only two of the three boundary conditions - we can't have $\phi_{0}$ the boundary as a function of $x$. Therefore, bad. 


Lets look at something else.
$$
\begin{align}
\alpha \in \mathbb{R}^{}
\end{align}
$$
$$
\begin{align}
\frac{1+e^{i \alpha}}{1-e^{i \alpha}}  & = \frac{1+ e^{i \alpha}}{1-e^{i\alpha}} \frac{1-e^{-i \alpha}}{1- e^{-i\alpha}}  \\
 & = \frac{1-1 + e^{i\alpha}-e^{-i\alpha}}{1+1-e^{i\alpha}-e^{-i\alpha}} \\
 & = \frac{2i \sin\alpha}{2-2\cos\alpha}
\end{align}
$$
The denominator is real, the numerator has an $i$, so this is imaginary.

We have a trick: if you have a phase $e^{i \alpha}$, we can turn it purely imaginary with 
$$
\begin{align}
\frac{1+ e^{i \alpha}}{1-e^{i\alpha}}
\end{align}
$$


We can guess that
$$
\begin{align}
\Omega = -i \ln \frac{1+ e^{i\pi z/b}}{1-e^{i\pi z/b}}
\end{align}
$$

Lets check that we didn't ruin $\Gamma_{1}$ and $\Gamma_{2}$. We still get an angle zero when we take the real part of this, so yes. We are good. Evaluated on $\Gamma_{3}$, the real part of this is $\frac{\pi}{2}$. We want $\phi_{0}$, so we just modify it:
$$
\begin{align}
\Omega =- \phi_{0} \frac{2i}{\pi} \ln \frac{1+ e^{i\pi z/b}}{1-e^{i\pi z/b}}
\end{align}
$$
We have satisfied the boundary conditions. Remember how terrible this was in cartesian - we had an infinite series, which could sum exactly into a function? It would sum into this function. 

Lets look back. The way we solved this problem was by taking a region $D$  with a complicated problem, we found a mapping to a nice space $D'$ where we could solve the complex problem for $\chi(\xi)$, and then map back (where $z=f(\xi)$, $\chi(\xi)=\Omega(f(\xi))$).

Someone took an airplane wing shape, found a map to a circle, solved $\vec{\nabla}^{2}\phi=0$, and found the exact solution for fluid dynamics around the wing. 

We have really nice conformal mapping that preserve angles:
$$
\begin{align}
z = \frac{a\xi+b}{c\xi+d} &  & a,b,c,d \in \mathbb{R}^{} 
\end{align}
$$

Lets take a difficult problem: Two lengths of metal that are at 90 degrees to each other. Lets put $\Gamma_{1}$ at $\phi=\phi_{0}$ and $\Gamma_{2}$ at $\phi = \phi_{0}+k$.
![[Pasted image 20261008105008.png]]
We could have the nice conformal map to make this just look like parallel plates of a capacitor. The map is
$$
\begin{align}
\xi = \frac{2}{3\pi} \ln (z)
\end{align}
$$
The log of a real line is still real. $0\to \infty$ maps to $-\infty\to \infty$ in the complex plane.$\Gamma_{2}$ is the angle $\frac{3\pi}{2}$, the log will give $\frac{3\pi}{2}*\frac{2}{3\pi}$. We map boundaries to where they go, and the regions map in between those boundaries.

![[Pasted image 20261008105605.png]]