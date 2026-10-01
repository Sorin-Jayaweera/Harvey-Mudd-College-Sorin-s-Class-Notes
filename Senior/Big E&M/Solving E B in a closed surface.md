

We have the electrostatics problem, and we want to solve the Poisson equation.

Given $\rho$ and boundary conditions,
$$
\begin{align}
\vec{\nabla}^{2} \phi = - 4\pi \rho  & &  \text{ Poisson }\\ \\
\vec{\nabla}^{2}\phi=0  &  & \text{ Laplace }
\end{align}
$$

--- 

We know that in three D,

$$
\begin{align}
\vec{\nabla}^{2} \left( \frac{1}{\left| \vec{x}-x' \right| }\right) = \delta^{3} (x-x) 
\end{align}
$$

We could easily say space is $\infty$ and there is no potential at $\infty$.
$$
\begin{align}
\phi(x) = \int dV' \frac{\rho(x')}{\left| \vec{x}-x' \right| }\\
\end{align}
$$


More practically though, we only have a contained area where we know $\rho(\vec{x})$ and want to find the electric scaler potential $\phi$ (or $\vec{\nabla}\phi=-\vec{E}$).

We have a second order differential equation, so we need the gradient of the potential at the boundaries to make something continuous. 

Lets set up some framework.


>[!abstract]+ Divergence Theorem
>$$\int\vec{\nabla}\cdot \vec{G} dv = \oint  \vec{G}\cdot d\vec{A}$$


Lets take
$$
\begin{align}
\vec{G} &  = \phi \vec{\nabla}\psi \\
\int\vec{\nabla} (\phi \vec{\nabla}\psi)dV   & =  \int \vec{\nabla} \phi \cdot \vec{\nabla} \psi + \phi \vec{\nabla}^{2} \psi  \\
 & = \oint  \phi \vec{\nabla}\psi \cdot d\vec{A} 
\end{align}
$$
You can write out a different $\vec{G}$ where you swap the order of $\phi$ and $\psi$, and take the difference between those two equations of the divergence theorem for the left and right side, and end up with

>[!abstract]+ Green's theorem
>$$
\begin{align}
\int (\phi \vec{\nabla}^{2} \psi - \psi \vec{\nabla}^{2} \phi)dV = \oint (\phi \vec{\nabla}\psi - \psi \vec{\nabla} \phi) \cdot d\vec{A}
\end{align}
$$



Back to the electrostatics. Lets call
$$
\begin{align}
G(x,x') \text{ a Green's function } \\
\vec{\nabla}^{2} G(x,x') = -4\pi \delta^{3} (x-x')
\end{align}
$$
$G$ is only defined within the finite region we are looking for. We are looking for Electric Potential ($G$) in a finite region with a finite charge. To define the problem, we need to say what $G$ is at the boundaries. 

There are two methods to solve for this Green's function for this - the left side

Dirichlet $G_{D}\to 0$ at boundary
Newman $$
\begin{align}
\frac{ \partial G_{n}  }{ \partial \vec{n} } = \frac{-4\pi}{S}
\end{align}
$$
where $S$ is the surface area at the boundary, and $\vec{n}$ is perpendicular to the surface boundary at every area.

$$
\begin{align}
\int d^{3}x  \vec{\nabla}^{2} G(x,x')  & = - 4\pi \int \delta^{3} (x-x') d^{3}x \\
\int d^{3}x \vec{\nabla}\cdot \vec{\nabla}G  \\
\oint  d\vec{A} \cdot \vec{\nabla}G \\
\oint dA \underbrace{ \hat{n} \vec{\nabla}G }_{ \frac{ \partial G }{ \partial n }  }
\end{align}
$$
if we had let $\frac{ \partial G }{ \partial n }=0$ than we would violate the setup that we have. 


$$
\begin{align}
\phi = \text{ electrostatic potential } \\
\psi = G(x,x') \text{ green's function that solves the immediately earlier eqn }
\end{align}
$$
$$
\begin{align}
\int(\phi \vec{\nabla}^{2} G - G\vec{\nabla}^{2} \phi)dV' = \oint (\phi\underbrace{  \vec{\nabla}G  }_{ - 4\pi \delta^{3}(x-x')  }- G \underbrace{ \vec{\nabla}^{2}\phi) }_{ - 4\pi \rho }\cdot d\vec{A}' \\
   \\
- 4\pi \phi(x) + 4\pi \int G \rho dV' = \oint  \phi \frac{ \partial G }{ \partial n } dA' - \oint  G \frac{ \partial \phi }{ \partial n } dA'
\end{align}
$$
$$
\begin{align}
\phi(x) = \int G(x,x') \rho(x') dV' + \frac{1}{4\pi} \oint G(x,x') \frac{ \partial \phi }{ \partial n' } dA' - \frac{1}{4\pi} \oint \phi(x') \frac{ \partial G }{ \partial n' } dA' 
\end{align}
$$

We need to know $G$, so we have to solve the Green's function problem.

We are solving the inhomogeneous equation (that's what we're doing with $\vec{\nabla}^{2} \phi = -4\pi \rho$)

Two cases: 

If we solve the Dirichlet problem, $G_{D}=0$ at boundary. We are left with the term that has $\phi$ on the boundary, $-\frac{1}{4\pi}\oint \phi(x') \frac{ \partial G }{ \partial n' }dA'$

If we do the Newman, we need
$$
\begin{align}
\frac{ d \phi}{d n } \text{ as the boundary }
\end{align}
$$
We still have a $\frac{ \partial G }{ \partial n' }$, which is a constant in the Newman case. The $4\pi$'s cancel, we have $\frac{1}{S}$ out front the integral. We then integrate $\phi$ over the boundary, so this ends up as $\phi_{avg}$ over the boundary (which we also need to know).

The most general strategy:
Given a boundary value problem with a cavity, where we want to find $\phi$ given $\rho$ in the cavity. We need to know $\phi$ at the boundary, then we solve the Green's function problem with $G_{D}=0$ at the boundary. 

If instead we know the electric field at the boundary, so we try to solve the Green's function problem with
$$
\begin{align}
\frac{ \partial G_{n}  }{ \partial n }  = \frac{-4\pi}{S}
\end{align}
$$

These both reduce to just finding the Green's function. 

$$
\begin{align}
G(x,x') = \frac{1}{\left| \vec{x}-\vec{x}' \right| } +\underbrace{  F(x,x') }_{ \text{ for B.C. Solve with Laplace equations } }
\end{align}
$$

The green's functions will always have this $\frac{1}{\left| \vec{x}-\vec{x}' \right|}$ term, so we only have to solve for $F$. 

We have simplified solving an homogeneous differential equation to just a Laplace equation (where if we have symmetry, we are happy).

![[20260917_103228.jpg]]

We have

$$
\begin{align}
\frac{1}{r} \frac{ \partial  }{ \partial r } \left(  r \frac{ \partial  }{ \partial r }  \right)G = 0 \\
\frac{ \partial G }{ \partial r } + r \frac{ \partial^{2} G }{ \partial r^{2} } = 0
\end{align}
$$

The solution is $G \propto \ln r$, i.e.
$$
\begin{align}
G= C \ln r \\
\frac{C}{r} - \frac{rC}{r^{2}} = 0
\end{align}
$$
We take $\lim_{ r \to 0 }$, make a circle around the origin, use Stoke's theorem (instead of the divergence theorem), and do the same stuff we did before (look back a lecture or so). 

The Green's function in the general function is
$$
\begin{align}
G^{2D}= C \ln (\vec{x}-\vec{x}') + F(x,x')
\end{align}
$$
$$
\begin{align}
\phi(x) = \int G(x,x')\rho(x')da' + \frac{1}{4\pi}\oint  \left(  G(x,x')\frac{ \partial \phi }{ \partial n' } - \phi(x')\frac{ \partial G }{ \partial n' }  \right)dS'
\end{align}
$$


---



