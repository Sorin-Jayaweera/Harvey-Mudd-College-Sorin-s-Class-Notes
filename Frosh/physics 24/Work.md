#work = $\text{ Force }\cdot \text{ displacement }$

We can write generally that 
$$
\begin{align}
W=\int_{c_{1}}^{} \vec{F}\cdot d\vec{R}_{cm}  \\
\text{ for a constant force and straight line path: } \\
W_{g}=\vec{F}_{g}\cdot(\vec{R}_{cm,f}-\vec{R}_{cm,i})  \\
= \left| \vec{F}_{g} \right|\left| \vec{D} \right|\cos(90-\theta) \\
\text{ If displacement is only in the }\hat{x}\text{ direction, } \\
= \vec{F}_{g}\cdot(D\hat{x}) \\
\text{ so for a block on a ramp, gravity does work equal to } \\
W_{g}=mg\sin \theta 
\end{align}
$$
Work done by gravity is $E_{g,i}-E_{g,f}$ (gravitational potential energy initial and final). Work is really just change in energy.

Work done by gravity is generally always the difference in gravitational potential energy. Work is $\Delta E$! We can write this for springs:
$W_{sp}=E_{s p,i}-E_{s p,f}$
$W_{sp}=\frac{1}{2}k(x_{i}-x_{0})^{2}-\frac{1}{2}k(X_{f}-x_{0})^{2}$

However this is a little different if we are thinking of friction. Friction works opposite to the direction of motion, so work done is negative. In both a block siding up and a block sliding down, friction does negative work. This means we always have to do $F\cdot D$ instead of simplifying to $E_{i}-E_{f}$. Most forces are like this.

However, if we have a conservative vector field, then we can do the subtraction. 

We call $\vec{F}$ a #conservative_field (or gradient field) if $\vec{F}=\nabla f$ for some scalar function F.
The fundamental theorem of line integrals:
If c is a path from A to B, and $\vec{F}$ = grad f, then
$$
\int_{c_{1}}^{} \vec{F}\cdot \vec{ds} = f(B)-f(A)
$$
Conservative forces are either constant or depend on position.
Non-conservative forces depend on velocity, ie direction and speed. 

A conservative force $\vec{F}$ is the negative gradient of its potential energy. $\vec{F}=-\nabla U$. 

$$
\begin{align}
U_{g}=mgY \\
\vec{F}_{g} = -\nabla E_{g} \\
= -\left( \frac{ \partial E_{g} }{ \partial x }\hat{X} + \frac{ \partial E_{g} }{ \partial y }\hat{Y} + \frac{ \partial E_{g} }{ \partial z }\hat{Z}  \right)  \\
= -\left( 0 + \frac{ \partial F_{g} }{ \partial y } + 0 \right)\\
\vec{F}_{g}=-mg\hat{Y}
\end{align}
$$


Let $K = E_{k}, U_{g} = E_{g}, \text{ and }  U_{s pr} = K_{ s pr}$. If we take
$$
\begin{align}
E_{k,i}+W_{tot}=E_{k,f} \\
K_{i} + W_{g}+W_{sp} + W_{other} = K_{f} \\
(K_{i}+U_{g,i}+U_{s p,i})+W_{other}=(K_{f}+U_{g,f}+U_{s pr}) \\
E_{i}+W_{other}=E_{f}
\end{align}
$$
In order to say that energy is conserved, ie $E_{i}=E_{f}$, then the net work by external forces is zero. 

$$
\begin{align}
F_{s p,x} &= -\nabla U_{s p} \\
&= -\frac{dU_{ s p}}{dx}\left( \frac{1}{2}k(x-x_{0})^{2} \right) \\
&=-k(x-x_{0})
\end{align}
$$
Force on a spring is negative slope of the energy function. 

![[Pasted image 20240220102249.png|300]]

