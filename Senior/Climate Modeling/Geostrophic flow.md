
We had conservation of momentum
$$
\begin{align}
\frac{ \partial \vec{u} }{ \partial t } + \vec{u}\cdot \vec{\nabla}\vec{u} + f\hat{z}\times \vec{u} = -\frac{1}{\rho}\nabla p
\end{align}- \nabla \phi + v\vec{\nabla}^{2}\vec{u}
$$

$$
\begin{align}
\frac{ \partial \vec{u} }{ \partial t } \text{ is acceleration of the fluit }
\end{align}
$$
$$
\begin{align}
\vec{u}\cdot \nabla \vec{u} \text{ }
\end{align}
$$
Advection of momentum. This is non linear. We could imagine advection of temperature flowing, but instead its momentum flowing. Take a slow to fast momentum region, just because the background momentum is slower? Imagine a stream of currents. We measure the velocity at a location. There is an eddy coming by. We experience the boost in momentum from the eddy on top of stuff. The gradient of velocity of a source of velocity, and we see how much it is aligned. How aligned we are with current velocity gradients. 

$f\hat{z}\times \vec{u}$ is the Coriolis force, where $f \equiv 2\Omega \sin \varphi$.

$$
\begin{align}
-\frac{1}{\rho}\nabla p
\end{align}
$$
is just a pressure gradient

$$
\begin{align}
-\nabla \phi
\end{align}
$$
is effective gravity (centrifugal force plus gravity - it is some surface potential height that is generally  pointing down).

we sometimes have
$$
\begin{align}
v\nabla^{2}\vec{u}
\end{align}
$$
the molecular viscosity, aka the friction. We sometimes say that turbulence looks like friction, and make this instead $v_{eddy}\nabla^{2}\vec{u}$.


We have two different resonant frequencies: the Buoyancy Frequency, $N$, which is vertical motion. This is on the order of $8$ minutes to hours. $f$ is horizontal motion of waves. This is the natural frequency that the ocean wants to rotate and move at, $f=2\Omega \sin \varphi$.


Lets take a steady ( no $\frac{ \partial \vec{u} }{ \partial t }$), horizontal (no $\vec{\nabla}\phi$), frictionless (no $v\nabla^{2}\vec{u}$) fluid. This is geostrophic flow.

$$
\begin{align}
f\hat{z}\times \vec{u}_{g} = -\frac{1}{\rho}\Delta p
\end{align}
$$
We usually get rid of geostrophic flow when reporting numbers, because it is a background thing that is always happening. 

Let
$$
\begin{align}
\vec{U}_{g} = \begin{pmatrix}
u_{g} \\ V_{g} \\ 0
\end{pmatrix}  \\
\hat{z}= \begin{pmatrix}
0\\0\\1
\end{pmatrix}
\end{align}
$$

$$
\begin{align}
\hat{z}\times(\hat{z}\times U_{g} ) = \hat{z}\times\left( -\frac{1}{f\rho}\Delta p \right)
\end{align}
$$
$$
\begin{align}
\hat{z}\times \vec{u}_{g} = \begin{pmatrix}
-V_{g} \\ U_{g} \\ 0
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
\hat{z}\times(\hat{z}\times \vec{u}_{g} )= \begin{pmatrix}
-u_{g} \\ - V_{g} \\ 0 
\end{pmatrix} = -\vec{U}_{g} 
\end{align}
$$
Geostrophic velocity.
$$
\begin{align}
-\vec{u}_{g} = \frac{1}{f\rho} \hat{z} \times \nabla p 
\end{align}
$$

If pressure is going from high to low, fluid flows down. Because the fluid has the effects of rotation, we have a spiral that goes to the side. It wants to go from high to low, but ends up orbiting. 
![[Pasted image 20261012134453.png]]




## Non dimensional numbers

Everyone knows reynolds number (a ratio between the inertia term, and the friction term). 

We also have Rossby Number for geostrophic flow.


We guess order of magnitude of terms, 

$$
\begin{align}
\frac{U}{T} &  & U \left( \frac{U}{L} \right) &  & fU  &  & \text{ characteristic scales roughly } \\
\frac{1}{fT} \ll 1 &  & \frac{U}{fL}\ll 1 &  & 1 &  & \text{ nondimensionalized rosby numbers }
\end{align}
$$


The rosby number is
$$
\begin{align}
Ro = \frac{\frac{u^{2}}{L}}{fu} = \frac{u}{fL}
\end{align}
$$
$$
\begin{align}
T = \text{ time scale } \\
f = 10^{-4}s^{-1}
\end{align}
$$
![[Pasted image 20261012140627.png]]

We would expect the rotation with rosby numbers for stuff on the order of $10^{4\text{ or }5\text{ maybe }3}$ for time in seconds. We don't have the order of magnitud for $u$, but its roughtly the same OOM for lengths. 

At a constant pressure surface, change in height will change the wind speed. We have a geopotential height which would predict an always have motion. 