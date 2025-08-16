---
tags:
  - Phys51
---
### Definition:
A material in which free [[Electrons]] can flow throughout an object in response to [[special/FriendsNotes/Phys51/Electric Field|electric fields]]. Metals are the most common example.

In copper, there are about $8.5\times 10^{22}$ free electrons per cubic centimeter.

##### Defining Property:
In equilibrium, the electric field in a conductor is always$^{*}$ zero.

$^{*}$ minus the brief moment a field is applied

If there is an electric field, the charges will move until
a field is *induced* that is equal and opposite to the applied field.

The induced surface charge is given by $\pm\epsilon_{0}E_{0}$. $E_{ind}=\frac{\sigma_{ind}}{\epsilon_{0}}=E_{0}$


#### In an External Field:
1. Inside the conductor, $\vec{E}=0$.
2. Inside the conductor, $q=0$.
	By [[Gauss's Law]]: No electric field in conductor $\implies$ $\Phi_{E}=0 \implies q_{enc}=0$.
3. Net charge or induced charge reside on the conductor surface.
	$q_{enc}=0\implies$ charge all on surface.
4. $\vec{E}$ is perpendicular to the conductor surface everywhere and $E=\frac{\sigma}{\epsilon_{0}}$ ($E$ : field at surface).



#### Example:
A charge inside a neural hollow metal sphere.




## Grounding
Connecting a conductor by wire to a huge infinitely* distant object. Ensures that the [[special/FriendsNotes/Phys51/Electrostatic Potential|potential]] of whatever is connect is always equal to zero.

A point charge $+q$ placed inside a hollow conductor causes negative charges on the inside of the conductor and positive charges on the outside.

Grounding the conductor makes the potential zero, which means the electric field outside of the conductor is zero (field is only between the point charge and inner conductor face).



### Laplacian

Since $\begin{matrix}\vec{\nabla}\cdot \vec{E}=\frac{\rho}{\epsilon_{0}} & \text{and}& \vec{E}=-\vec{\nabla}V \end{matrix}$, $\implies -\vec{\nabla}\cdot(\vec{\nabla}V)=\frac{\rho}{\epsilon_{0}}$
or
$$
\nabla^{2}V = \frac{ \partial ^{2}V }{ \partial x^{2} }+\frac{ \partial ^{2}V }{ \partial y^{2} }+\frac{ \partial ^{2}V }{ \partial x^{2} }= -\frac{\rho}{\epsilon_{0}}
$$


**Laplace's Equation**
$$
\nabla^{2}V = \left\{\begin{matrix*}[l]
-\frac{\rho}{\epsilon_{0}} & \text{ where charge is present} \\
0 & \text{ in empty space}
\end{matrix*}\right. 
$$




$\frac{ \partial ^{2}V }{ \partial x^{2} }+\frac{ \partial ^{2}V }{ \partial y^{2} }+\frac{ \partial ^{2}V }{ \partial x^{2} }=0$
$\frac{ \partial ^{2}V }{ \partial x^{2} },\frac{ \partial ^{2}V }{ \partial y^{2} }$ and $\frac{ \partial ^{2}V }{ \partial z^{2} }$ can't all three be $<0$ or $>0$.
→ $V$ must have no maxima or minima in free space, and all solutions of $V$ must be unique.


Grounded Conductor Example:
1. $V=0$ on the surface
2. $V=0$ at infinity
3. No maxima or minima allowed in the free space between
$\implies V=0$ everywhere outside