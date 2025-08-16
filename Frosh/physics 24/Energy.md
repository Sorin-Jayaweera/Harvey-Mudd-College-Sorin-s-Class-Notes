$\vec{F}=-\nabla U$


This is super neat. Draw any random diagram with a block going down then up a weird frictionless surface.

$$
\begin{align}
F_{net,x}=ma_{x}, -mg\sin\theta=ma_{x} \\
\frac{dv_{x}^{2}}{dt}=2v_{x}\frac{dv_{x}}{dt}=2v_{x}a_{x} \\
-mg\sin\theta v_{x}=ma_{x}v_{x} \\
\frac{1}{2}m\frac{dv^{2}}{dt}+mg\frac{dY}{dt}=0 \\
\frac{d\left( \frac{1}{2}mv^{2}+mgY \right)}{dt}=0
\end{align}
$$
Energy is conserved.
Total energy $E=\frac{1}{2}mv^{2}+mgY$
Spring kinetic energy $=\frac{1}{2}kx^{2}$

There  is kinetic energy in translation across space, ie motion of the center of mass. There is also rotational energy and vibrational kinetic energy, which are motions relative to the center of mass. 

## Power
By definition, #power is the rate of change of kinetic energy over time.

$$
\begin{align}
\mathbb{P}_{cm} = \frac{d}{dt}K_{cm}  \\
= \frac{d}{dt} \left( \frac{1}{2}mv^{2} \right)= \frac{1}{2}m\frac{d}{dt} (\vec{v}_{cm} \cdot \vec{v}_{cm} ) \\
= \frac{1}{2}m\left[ \frac{d\vec{v}_{cm} }{dt}\cdot \vec{v}_{cm}  + \vec{v}_{cm} \cdot \frac{d\vec{v}_{cm} }{dt} \right]  \\
\mathbb{P}_{cm} =m\vec{a}_{cm} \cdot \vec{v}_{cm}=\vec{F}net\cdot v_{cm}  \\
 
\end{align}
$$
By definition, $\mathbb{P}_{cm}$ can also be written as 
$$
\begin{align}
\mathbb{P} _{cm} =\frac{d}{dt} k_{cm} =\vec{F}_{net}\cdot\vec{v}_{cm}  \\
= (\vec{F}_{g}+\vec{F}_{n}+\vec{F}_{k} )\cdot \vec{v}_{cm}  \\
= \mathbb{P}^g_{cm} +\mathbb{P}^n_{cm} +\mathbb{P}_{cm}^{k}
\end{align}
$$
If we take a projectile, the work of gravity changes signs throughout the arc. At first gravity is unaligned, later it is aligned. work uses the dot product, so we simplify to $F_{g}\cdot v= \left| F_{g} \right|\left| v \right|\cos\theta$ where $\theta$ is the angle between the velocity vector and the force vector.

![[Pasted image 20240215100435.png|300]]

Imagine a mass m sliding down an incline at constant speed v 
![[Pasted image 20240215102601.png|300]]
*Be careful*: Normal force, gravity, and friction don't always follow the same work as above. An elevator going up has normal force doing positive work, a conveyer belt pulling a mass along due to friction has friction doing positive work, etc. 

## Work energy theorem

$$
W=\int_{c}^{} \vec{F}\cdot \vec{dr}
$$
![[Pasted image 20240215104116.png|500]]
$$
\vec{F}_{0}\cdot \left[ \int_{ti}^{tf}  \, dR_{cm}   \right]= \vec{F}_{0}\cdot(\vec{R}_{cm,f}-\vec{R}_{cm,i} ) 
$$
Is this always true? **NO!** This requires $\vec{F}_{0}$ to be constant along the entire path. If direction of friction changes or something then the vectors switch directions.
In general, a vector line integral is ***not*** independent of the path from initial position to the final position. 
$$

$$
