## Big ideas for today
* How to find $\vec{E}$ outside sphere with uniform $\rho$
* Introducing flux
	* how much vector field passes through an area
* Find flux of $\vec{E}$ through a sphere surrounding a point charge
* Gauss's law: 
	* Always true, sometimes useful for finding $\vec{E}$. $$
\begin{align}
∯\vec{E}\cdot d\vec{A}=\frac{q_{enc}}{\epsilon_{0}}
\end{align}
$$
## Gauss's law
$$
\begin{align}
∯\vec{E}\cdot d\vec{A}=\frac{q_{enc}}{\epsilon_{0}}
\end{align}
$$
If we have a closed surface, (i.e. a bubble that fully encloses a volume), the flux $\Phi_{E}$ of $\vec{E}$ out through the closed surface is equal to the charge enclosed divided by $\epsilon_{0}$

We can use gauss's law ONLY if we have cylindrical, spherical, or planar symmetry around an object. We use that to reduce the number of unknowns, then pull out the $\vec{E}$ from the surface integral and solve. 

$$
\begin{align} \\
\text{ let $\vec{c}$ be a generic vector field}\\
 \text{ flux ($\Phi_{c}$)} = \iint\vec{c}\cdot d\vec{A}
\end{align}
$$


if $\vec{c}$ is constant and the area is flat, then $\Phi=\vec{c}\cdot \vec{A}$
Lets do a quick example. Imagine water flowing through a pipe. The flux is $$
\begin{align}
\Phi=\vec{v}\cdot \vec{A}=va\cos\theta
\end{align}
$$
![[Pasted image 20240903095546.png]]
We can cut a different surface for the pipe.
![[Pasted image 20240903095646.png]]

Lets try a more electric-y example of a sphere. Remember, the flux is the OUTWARD normal, not the inwards.
![[Pasted image 20240903100234.png]]
This verifies (for this case) Gauss's law.
Lets see if we can prove that it holds for any point charge, we can prove that it works for any superposition of many point charges.
![[Pasted image 20240903102113.png]]
![[Pasted image 20240903101614.png]]
This is a rough proof that we can deform any shape and find the flux through that area. 

Lets do Gauss's law for $\vec{E}$ of a line charge. 
$$
\begin{align}
\vec{E}=\frac{\lambda}{2\pi \epsilon_{0}r}\hat{r}
\end{align}
$$
Lets use cylindrical coordinates $r \phi z$.
![[Pasted image 20240903104108.png]]

We have shown a fast way of finding the field using Gauss's law.
Now lets try $\vec{E}$ of an $\begin{align}\infty\end{align}$  plane of charge.
$E=\frac{\sigma}{2\epsilon_{0}}$

See previous: [[Lecture 2 Electric Field]]
See next: [[Lecture 3 Gauss's law]]
