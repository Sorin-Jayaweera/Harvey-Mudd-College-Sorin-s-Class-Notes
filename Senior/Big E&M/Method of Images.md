
We left off with
$$
\begin{align}
\nabla^{2}\phi  & = -4\pi \rho + \text{ b.c. } \\
\phi(x)  & = \int G(x,x') \rho(x')d^{3}x' + \frac{1}{4\pi} \oint \left( G(x,x') \frac{ \partial  \phi(x') }{ \partial n' } - \phi(x) \frac{ \partial G(x,x') }{ \partial n' }  \right)da
\end{align}
$$



## Method of Images

Lets start with Planer symmetry.


Take an infinite planer conductor which is grounded ($\phi=0$).

What if we want to solve the Laplace equation 
$$
\begin{align}
\nabla^{2} \phi=0
\end{align}
$$
The potential is just zero everywhere - it solves the equation, existence uniqueness, we're done.


What if instead we are solving
$$
\begin{align}
\nabla^{2}\phi = -4\pi q \delta(z-a)\delta(x)\delta(y)
\end{align}
$$
This is a point charge height $a$ above the plane. Lets NOT pull out the big guns (green's theorem). 
Lets put a random point $\vec{x}$ and try to solve for the potential there.
The solution has
$$
\begin{align}
\phi = \frac{q}{\left| a\hat{z}-\vec{x} \right| }
\end{align}
$$
This solves the Laplace equation, but it doesn't solve the boundary conditions (zero at the infinite plane).

We add to this $F$, where $F$ satisfies
$$
\begin{align}
\vec{\nabla}^{2}\phi = 0 \text{ AT } z>0
\end{align}
$$
We can add on
$$
\begin{align}
\phi = \frac{q}{\left| a\hat{z} - \vec{x} \right| } + \underbrace{ F }
\end{align}
$$
because $F$ doesn't change anything when we plug it into the laplace equation.

We need an $F$ such that the potential $\phi(x,y,z=0)=0$.

We can put a copy of the particle (an image charge) at $a$ below the axis, with charge $-q$. The charge isn't there, its in a region where we aren't even considering solving for $\phi$. Because the laplacian has a $\delta(z-a)$, and this charge is at a position $\delta(z+a)$, we don't see it.

$$
\begin{align}
\phi(x) = \frac{q}{\left| a\hat{z}-\vec{x} \right| } - \frac{q}{\left| -a\hat{z}-\vec{x} \right| }
\end{align}
$$
where this second term is the "image charge". 

We can strategically place charges outside the boundary to add something that solves the Laplaces equaiton, but where the position and value set the boundary conditions that we want. 

$$
\begin{align}
\phi(x) = \frac{q}{\underbrace{ \sqrt[]{ x^{2}+y^{2}+(z-a)^{2}U } }_{ r } } - \frac{q}{\underbrace{ \sqrt[]{ x^{2}+y^{2}+(z+a)^{2} } }_{ r' } }
\end{align}
$$
and $\vec{E} = -\vec{\nabla}\phi$

So we have
$$
\begin{align}
\vec{E} = \left(  \frac{qx}{r^{3}}- \frac{qx}{r'^{3}}, \frac{qy}{r^{3}} - \frac{qy}{r'^{3}}, \frac{q(z-a)}{r^{3}} - \frac{q(z+a)}{r'^{3}} \right)
\end{align}
$$


at $z=0$,
$$
\begin{align}
\left( 0,0, \frac{q(z-a)}{r^{3}}- \frac{q (z+a)}{r'^{3}} \right) \\
= \left( 0,0, \frac{-2qa}{r^{3}} \right)
\end{align}
$$
--- 


We have from gauss's law
$$
\begin{align}
E_{2n} - E_{1n} = 4\pi \sigma  
\end{align}
$$

Region two is inside the grounded conductor, so we just have
$$
\begin{align}
\frac{2qa}{r^{3}}= 4\pi \sigma \\
\sigma = -\frac{qa}{2\pi r^{3}}
\end{align}
$$

We have accumulated a charge density on the grounded wire to cancel out the charge. How much total charge do we have on the grounded plane?

$$
\begin{align}
Q_{tot} = \iint_{-\infty}^{\infty} \sigma dqdy = -q 
\end{align}
$$
The fictitious image charge $-q$ is physically distributed across the boundary, and solves the boundary conditions. 

--- 

Lets do a function where method of images isn't sufficient, but Green's method is still overkill.

Lets make a two D enclosure - a semi infinite rectangle. The two sides are grounded, the bottom has $\phi=\phi_{0}$, some finite potential, and the top is open.

![[Pasted image 20260922100717.png]]

This has planer symmetry. 

Lets write out
$$
\begin{align}
\nabla^{2}\phi  & = 0 \\
\frac{ \partial^{2}\phi }{ \partial x^{2} } + \frac{ \partial^{2}\phi }{ \partial y^{2} } + \frac{ \partial^{2}\phi }{ \partial z^{2} } & =0 \\
\phi(x,y,z)  & = X(z)Y(y)Z(z) \\
YZ \frac{ \partial^{2}X }{ \partial x^{2} } + XZ \frac{ \partial^{2}Y }{ \partial y^{2} } + XY \frac{ \partial^{2}Z }{ \partial z^{2} }  & =0 \\
\frac{1}{X} \frac{ \partial^{2}X }{ \partial x^{2} } + \frac{1}{Y} \frac{ \partial^{2}Y }{ \partial y^{2} } + \frac{1}{Z} \frac{ \partial^{2}Z }{ \partial z^{2} }  & = 0
\end{align}
$$

Because we have three separate derivatives with different variables that have to cancel out, they have to be constants.

$$
\begin{align}
\frac{1}{X} \frac{ d ^{2}X}{d x^{2} } = -\alpha^{2}  \\
\frac{1}{Y} \frac{ d ^{2}Y}{d y^{2} } = -\beta^{2} \\
\frac{1}{Z} \frac{ d ^{2}Z}{d z^{2} } = + \gamma^{2}
\end{align}
$$
$$
\begin{align}
\alpha^{2}+\beta^{2} = \gamma^{2}
\end{align}
$$

The solutions to the first two are sine and cos, because it looks like a spring force ($\frac{ d ^{2}X}{d x^{2} }=-kX$).

We really only have two constants, because two define the third. 
We put the $\sin$ and $\cos$ solutions going across $x$ because we need to match the boundary condition. We don't care about $y$, there should be no $y$ dependence - the box extends infinitely in $y$. No $y-dep$ because translational symmetry in $y$. 

We can't have three of the same signs, the three constants have to sum to $0$. 

The third, $\gamma$, has exponential solutions $e^{\pm \gamma z}$. We want this to die off to infinity, to have $0$ potential at $z\to \infty$. 


The boundary condition needs $\phi(x=0)=\phi(x=b)=0$. 

We can write linear combinations of $\sin$ to fit this, but we can't have $\cos$ because it won't be $0$ at $0$.
$$
\boxed{
\begin{align}
\sin(\alpha b)= 0 \\
\alpha= \frac{n\pi}{b} \\
\implies X(x) = \sin \left(  \frac{n\pi x}{b} \right)
\end{align}
}
$$
We have an infinite set of possibilities, and can have sums of any sine with these n's. 

We have
$$
\begin{align}
\alpha^{2} + \cancelto{ 0 }{ \beta^{2} } = \gamma^{2} \\
\end{align}
$$
This sets $\gamma$, so the $z$ solutions are
$$
\begin{align}
e^{\pm \frac{n\pi}{b}z }
\end{align}
$$
For this to die off at $z\to \infty$, we need the negative solution. 
$$
\boxed{
\begin{align}
Z(z) = e^{\frac{-n\pi}{b}z}
\end{align}
}
$$



This gives us the solution
$$
\begin{align}
\phi(x,y,z) = \sum_{n=1}^{\infty} A_{n} \sin\left( \frac{n\pi x}{b} \right) e^{ \frac{-n\pi z}{b}}
\end{align}
$$
OOOH we have anything! But we still have to solve for $A_{n}$ to satisfy the bottom boundary condition. At $z=0$, we need
$$
\begin{align} \\
\phi(x,y,z=0) & =\phi_{0}\\
 & = \sum_{n=1}^{\infty} A_{n} \sin\left( \frac{\pi nx}{b} \right)
\end{align}
$$
We are trying to solve for all the constants $A_{n}$. We can use the orthogonality of the Fourier nodes. 

$$
\begin{align}
\frac{2}{b}\int_{0}^{b}  \sin\left( \frac{n\pi x}{b} \right)\sin\left( \frac{m\pi x}{b} \right)= \delta_{nm} 
\end{align}
$$

Lets try to manipulate our function with this. 
$$
\begin{align}
\frac{2}{b}\int_{0} ^{b} dx \phi_{0} \sin\left( \frac{m\pi x}{b} \right)  & = \sum_{n=1}^{\infty} \frac{2}{b}\int_{0}^{b} A_{n} \sin\left( \frac{n\pi x}{b} \right)\sin\left( \frac{m\pi x}{b} \right)  \\
 & = A_{n} \delta_{nm} = A_{m} \\
A_{m} = \frac{2}{b}\phi_{0} \int_{0}^{b} dx \sin\left( \frac{m\pi x}{b} \right)  \\
A_{m} = \frac{2}{b}\phi_{0} \left( -\cos\left( \frac{m\pi x}{b} \right)\bigg|_{0}^{b} \frac{b}{m\pi}  \right) \\
A_{m} = \frac{2}{b}\phi_{0} \frac{b}{m\pi} (1-\cos(m\pi)) \\
\end{align}
$$
Any time $m$ is even we get 0, and when it is odd we get $2$.

$$
\begin{align}
A_{m} = \begin{cases}
0 & \text{ m is even} \\
\frac{4\pi_{0}}{m\pi} & \text{ m is odd }
\end{cases}
\end{align}
$$

So we have
$$
\begin{align}
\phi(x,y,z) = \sum_{n=1}^{\infty} \frac{4\phi_{0}}{2n\pi} \sin\left( \frac{2\pi nx}{b} \right)e^{-\frac{2n\pi z}{b}}
\end{align}
$$
(i added a $2$ in front of every $n$, or we could just specify the sum is only for $n$ odd)

Lets sum this exactly. 

We know that $\sin$ is the imaginary part of
$$
\begin{align}
e^{i\phi}= \cos\theta + i\sin\theta
\end{align}
$$
So we can rewrite the sin part as
$$
\begin{align}
Im e^{i \pi \frac{x}{b}n}
\end{align}
$$

Therefore, we have
$$
\begin{align}
\phi = \mathbf{Im} \sum_{n=1, odd}^{\infty} \frac{4\phi_{0}}{n \pi} e^{ \frac{i\pi x}{b}n}e^{-\frac{\pi z}{b}n}
\end{align}
$$
Lets call the exponentials
$$
\begin{align}
e^{\left( \frac{i\pi x}{b}- \frac{\pi z}{b} \right)n}= \xi
\end{align}
$$
We have
$$
\begin{align}
Im \sum_{n \text{ odd }}^{\infty} \frac{4 \phi_{0}}{\pi} \frac{\xi^{n}}{n}
\end{align}
$$

We have 
$$
\begin{align}
\phi = Im \sum_{n \text{ odd }}^{\infty} \frac{4\phi_{0}}{\pi} \frac{\xi^{n}}{n} \\
= \frac{2 \phi_{0}}{\pi} \mathbf{Im} \ln  \frac{1+\xi}{1-\xi}
\end{align}
$$

We know this because
$$
\begin{align}
\ln  \frac{1+\xi}{1-\xi} = \ln (1+\xi) - \ln  (1-\xi) \\
= \int \frac{1}{1+\xi}d\xi + \int \frac{1}{1-\xi} d\xi
\end{align}
$$
which we can substitute into the geometric series, integrate, and get back.

We can continue as
$$
\begin{align}
\frac{2\phi_{0}}{\pi} \tan ^{-1} \frac{\left( \sin\left( \frac{\pi x}{b} \right) \right)}{\left( \sinh \left( \frac{\pi z}{b} \right) \right)}
\end{align}
$$

This is really cool. Why? 

This is a two $D$ problem, because we can complexify things, and $2D$ has a 1-1 correspondence to the complex plane. We'll use complex analysis to look at the problem and write this solution in only two lines. 
