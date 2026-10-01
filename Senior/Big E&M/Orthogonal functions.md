
## Key takeaways

Using Method of images. 
Using Green's function.


## Orthogonal functions


$$
\begin{align}
f(x) \text{ for } a<x<b \\
\end{align}
$$

Orthogonal functions $U_{n}(x)$ in $a<x<b\,\,\forall_{n}$ are such that
$$
\begin{align}
f(x) = \sum_{n=1}^{\infty} a_{n} U_{n}(x)  
\end{align}
$$

Where
$$
\begin{align}
\int_{a}^{b} U_{n} (x)U^{*}_{m}(x) = \delta _{nm} 
\end{align}
$$

We have
$$
\begin{align}
\int_{a}^{b} U^{*}_{m} (x)f(x)dx = \sum_{n=1}^{\infty} \int_{a}^{b} U^{*}_{m} (x)a_{n} U_{n} (x)dx \\
= a_{m} 
\end{align}
$$
This tells us how to find $a_{m}$ given $f$, or we have a decomposition of the function $f$ in terms of these $a_{m}$.


For $-\pi \leq x \leq \pi$, 
$$
\begin{align}
U_{n} (x) = \frac{1}{\sqrt[]{ \pi } } \sin(nx)
\end{align}
$$
For periodic, $x \to  x + 2\pi$

$f(x)$ for periodic,
$$
\begin{align}
\frac{-d}{2} \leq  x \leq \frac{d}{2}
\end{align}
$$
$$
\begin{align}
U_{n} = \sqrt[]{ \frac{2}{d} } \sin \left(  \frac{2\pi nx}{d} \right)
\end{align}
$$
and $V_{n}=\sqrt[]{ \frac{2}{d} }\cos\left( \frac{2\pi nx}{d} \right)$

---
We have the non periodic doubling trick.

We can take a non periodic function that lives from $0\to d$
We can mirror and shift it from $d\to 2d$, extending it to look periodic.

$$
\begin{align}
f(x+d)=f(d-x)
\end{align}
$$
---
We can go to the complex plane and use the basis $e^{\pm ikx }$

We have the most famous example, the Fourier transform (infinite, not countable because it is a continuum)
$$
\begin{align}
f(x) = \int_{-\infty}^{\infty} A(x) \frac{e^{ikx}}{\sqrt[]{ 2\pi } } dk 
\end{align}
$$

$$
\begin{align}
A(k) = \int_{-\infty}^{\infty} f(x) \frac{e^{-ikx}}{\sqrt[]{ 2\pi } }dx
\end{align}
$$
We have orthonormality as
$$
\begin{align}
\int_{-\infty}^{\infty} \frac{e^{-ikx}}{\sqrt[]{ 2\pi } } \frac{e^{ik'x}}{\sqrt[]{ 2\pi } } = \delta(k-k')
\end{align}
$$


We normally see this as

$$
\begin{align}
\frac{1}{2\pi} \int_{-\infty}^{\infty} e^{i(k-k')x}dx = \delta(k-k')
\end{align}
$$
This is a definition of the $\delta$ function, we can plug it in to
$$
\begin{align}
\int_{-\infty}^{\infty} f(x)\delta(x-a)dx = f(a)
\end{align}
$$
to show that it still works.


## Poisson Equation in Spherical Coordinates

We can circumvent the green's function when we have spherical symmetry. 

Lets take a sphere of radius $R$ that is grounded, so $\phi=0$ on it's surface. Lets solve for the region outside the sphere, where $r>R$. At $\infty$ we expect $\phi=0$. Lets put a charge $q$ at a distance $a$ from the origin of the sphere (the charge is outside the sphere). Lets call that the $z$ axis.

Point charge outside a grounded spherical conductor.
$$
\begin{align}
\vec{\nabla}^{2}=-4\pi \rho &  & r>R
\end{align}
$$

We *could* write the green's function, and we will do that in a bit (yippee spherical harmonics), but lets try method of images. Lets guess that we can put a negative imaginary charge $q'$ on the $z$ axis inside the grounded ball at some radius $a'$. We have two variables: $\left| q' \right|$ and the location $a'$ of this imaginary fake image charge. 

We want the charge such that the sum of potential vanishes at the surface of the sphere. 

$$
\begin{align}
\phi = \underbrace{ \frac{q}{\left| a\hat{z}-\vec{r} \right| } }_{ -4\pi q\delta^{3}(\vec{r}-a\hat{z}) } + \underbrace{ \frac{q'}{\left| a'\hat{z}-\vec{r} \right| } }_{ -4\pi q' \delta^{3} (\vec{r}-a'\hat{z}) }
\end{align}
$$

where this position vector $\vec{r}$ is outside the sphere always, and $a'$ is always inside the sphere. Therefore, the deltafunction never has an argument that hits $0$, so it will never have a value in the region of interest. Therefore, it still works for $\vec{\nabla}^{2}\phi=-4\pi \rho \,\,\forall r>R$.

We can simplify the first and second terms by doing $\sqrt[]{ val^{2} }$
$$
\begin{align}
\phi  & = \frac{q}{((a\hat{z}-\vec{r})\cdot(a\hat{z}-\vec{r}))^{1}{2}} + \frac{q'}{((a'\hat{z}-\vec{r})\cdot(a'\hat{z}-\vec{r}))^{1}{2}} \\
 & = \frac{q}{(r^{2}+a^{2}-2ar\cos\theta)^{\frac{1}{2}}} + \frac{q'}{(r^{2}+a'^{2}-2a'r\cos\theta)^{\frac{1}{2}}}
\end{align}
$$

We want 
$$
\begin{align}
 & \phi(r=R) =0  \\
 & = \frac{q}{(R^{2}+a^{2}-2aR\cos\theta)^{\frac{1}{2}}} + \frac{q'}{(R^{2}+a'^{2}-2a' R\cos\theta)^{\frac{1}{2}}}   &  &  \forall \theta
\end{align}
$$
We have two variables, $q'$ and $a'$. 

We can't just set $q'=-q$, because it wouldn't solve the denominator. Lets try to factor out an $a'$ maybe?

$$
\begin{align}
 & = \frac{q}{a^{2}\left( \frac{R^{2}}{a^{2}}+1-\frac{2R}{a}\cos\theta \right)^{\frac{1}{2}}} + \frac{q'}{a'\left( \frac{R^{2}}{a'^{2}}+1-2 \frac{R}{a'} \cos\theta \right)^{\frac{1}{2}}}  
\end{align}
$$

What if we say $\frac{R}{a'}=\frac{R}{a}$? Eh, we don't really see how we would set a condition on $q$. Lets try factoring out $R$ on one and just $a'$ on the other - now we can set a relationship between $q$ and $q'$ with the constants, and we have an expression on the inside to relate $R$ and $a'$.

$$
\begin{align}
 & = \frac{q}{R\left( 1+\frac{a^{2}}{R^{2}}-\frac{2a}{R}\cos\theta \right)^{\frac{1}{2}}} + \frac{q'}{a'\left( \frac{R^{2}}{a'^{2}}+1-\frac{2R}{a'}\cos\theta \right)^{\frac{1}{2}}}   &  &  \forall \theta
\end{align}
$$


The conditions for this are
$$
\begin{align}
\frac{a}{R}= \frac{R}{a'} \\
\frac{q}{R}=-\frac{q'}{a'} \\
 \\
a' = \frac{R^{2}}{a} \\
q' = -q \frac{a'}{R} = -q \frac{R^{2}}{a} \frac{1}{R}
\end{align}
$$

If we choose
$$
\begin{align}
q' = -q \frac{R}{a} \\
a' = \frac{R^{2}}{a}
\end{align}
$$
then we are guaranteed to have $\phi=0$ for all $\theta$ around the sphere. 


The electric field is
$$
\begin{align}
\vec{E} = -\vec{\nabla}\phi \\
E_{r} = \frac{-\partial \phi}{\partial r} = 4\pi \sigma \\
\end{align}
$$
Just outside, at $r = R+\epsilon$, just barely outside, we see that the field lines are all perpendicular to the conductor. 

If we look at the total charge,
$$
\begin{align}
\int_{0}^{\pi} \sigma 2\pi R^{2} \sin\theta d\theta = -q \frac{R}{a}
\end{align}
$$
--- 

Lets try the same problem, but instead of grounded we have a charge $Q$ on the conducting sphere. 

If it were grounded, we would have the charge $q'$ on the surface. If we disconnect it and make the total charge $Q$, we have added charge $Q-q'$, which will distribute uniformly. By superposition, 
$$
\begin{align}
\phi= \phi_{\text{ grounded }} + \frac{Q-q'}{r} 
\end{align}
$$
because this acts like a point charge at the origin. Quick and dirty. 

--- 

Lets take a sphere that is not grounded, connected to a battery. The voltage is $\phi_{0}$ on the surface. We put a charge $q$ above it. 

$$
\begin{align}
\phi=\phi_{\text{ grounded }} + \frac{\phi_{0}R}{r}
\end{align}
$$
at $r=R$, we have potential $\phi_{0}$ so we have solved the boundary condition. Existence uniqueness, we're done. 

--- 

Lets take the same damn sphere. We ground it, and put an electric field $\vec{E}_{0}$ externally that goes through all of space. What is $\phi$ everywhere?

We replace the electric field with two charges, $q$ and $-q$ (a dipole) which are $b$ from the origin each. This is NOT $\vec{E}_{0}$, which is a uniform electric field. But! We can take $b\to \infty$ and $q\to \infty$, but keeping the dipole fixed. The electric field at the origin is $E_{0} = \frac{2q}{b^{2}}$. We keep that fixed. We can put two charges inside the sphere $-q'$ and $q'$. 


## Greens function

 Lets do Green's function with spherical symmetry. 

We have a sphere with a charge outside of it, (by definition, we have to have $G_{d}=0$ on the boundary of the sphere for us to do the Dirichlet method). Let $q=1$. 
$$
\begin{align}
\vec{\nabla}^{2} G_{D} (x,x') = -4\pi \delta^{3} (x-x')
\end{align}
$$

We should get 
$$
\begin{align}
\vec{\nabla}^{2} \phi = -4\pi \rho \\
\phi = \phi_{0}
\end{align}
$$
We already solved this problem.

The green's function
$$
\begin{align}
G_{D} (\vec{r},\vec{r}') = \frac{1}{\left| \vec{r}-\vec{r}' \right| }  - \frac{R}{r' } \frac{1}{\left|  \frac{R^{2}}{r'^{2}}\vec{r}' - \vec{r} \right| }
\end{align}
$$
Because we aren't forcing the charge to be on the z axis, there is an angle $\alpha$ between $\vec{r}'$ and $\vec{r}$ . We expand the $\left|  \right|$ bits by doing $\sqrt[]{ x \cdot x }$.

We have

$$
\begin{align}
G_{D} = \frac{1}{(r^{2}+r'^{2}- 2rr'\cos\alpha)^{\frac{1}{2}} } - \frac{1}{(\frac{r^{2}r'^{2}}{R^{2}}+ R^{2} - 2rr' \cos \alpha)^\frac{1}{2}}
\end{align}
$$
Ignoring some algebra because who has time

$$
\begin{align}
\frac{ \partial G_{D}  }{ \partial r' } \bigg|_{r'=R}^{} = \frac{r^{2}-R^{2}}{R(r^{2}+R^{2}-2Rr\cos \alpha)^{3/2}} \\
\phi(\vec{r}) = \int G_{D}(\vec{r},\vec{r}')\rho(\vec{r}')dV' + \frac{1}{4\pi} \oint  \phi(R,\theta',\phi') \frac{(r^{2}-R^{2} )R^{2}\sin\theta' d\theta' d\phi'}{R(r^{2}+R^{2}-2Rr\cos\alpha)^{3/2}}  
\end{align}
$$


$$
\begin{align}
\cos\alpha &  = \frac{\vec{r}\cdot \vec{r}'}{rr'} \\
 & = \cos\theta \cos \theta' + \sin\theta \sin \theta' \cos(\phi-\phi')
\end{align}
$$


This is pretty general (compared to method of images), but not general enough. We haven't done Neumann, nor have we done inside the sphere. 

## General Green's Function Method in Spherical Coordinates

$$
\begin{align}
G(\vec{x},\vec{x}') = \frac{1}{\left| \vec{x}-\vec{x}' \right| } + F(\vec{x},\vec{x}')
\end{align}
$$
We will first find the most general $F$ in spherical coordinates (spherical harmonics!).

