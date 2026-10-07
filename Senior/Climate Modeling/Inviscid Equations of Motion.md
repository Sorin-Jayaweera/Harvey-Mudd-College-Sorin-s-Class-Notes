
Last time we established that
$$
\begin{align}
 & \frac{D w}{Dt}  =   \\
&  \frac{ \partial w }{ \partial t } + \vec{V}\cdot(\vec{\nabla} w)   & = \frac{F_{p}}{m} - \frac{F_{g}}{m}  \\
 &    & = -\frac{1}{\rho} \frac{ \partial p }{ \partial z } - g
\end{align}
$$

---


We have the material derivative
$$
\begin{align}
\frac{ D }{D t } = \frac{ \partial  }{ \partial t } + \vec{v} \cdot u
\end{align}
$$
where $\vec{v}= \begin{bmatrix}u\\v\\w\end{bmatrix}$, the velocities in the $\hat{x},\hat{y},\hat{z}$ directions.

## The continuity equation

Mass conservation. Imagine we have a parcel with fixed volume. The mass is just density by volume.
$$
\begin{align}
\delta M = \rho \delta x \delta y \delta z
\end{align}
$$
The change in mass over time is just due to the change in density. 
$$
\begin{align}
\rho = \frac{m}{v}
\end{align}
$$
$$
\begin{align}
\frac{ d \rho}{d t } &  = \text{ flux of } \rho \text{ in }- \text{ flux of } \rho \text{ out } \\
\frac{ \partial \rho }{ \partial t } &  = -\nabla\cdot (\rho \vec{u})
\end{align}
$$

We have the conservation law
$$
\begin{align}
\frac{ \partial p }{ \partial t } + \vec{u}\cdot \nabla \rho + \rho(\nabla\cdot \vec{u}) = 0 \\
\frac{D\rho}{Dt} + \rho(\nabla\cdot \vec{u}) = 0
\end{align}
$$
If we have an incompressible fluid, 
$$
\begin{align}
\frac{1}{\rho} \frac{D\rho}{Dt}=0
\end{align}
$$
so $\vec{\nabla}\cdot\vec{U}=0$ has to be zero (in compressible -> divergence free, we don't have a source). 


When can we assume incompressibility? If any variation in density is really low relative to the average density
$$
\begin{align}
\rho' \ll  \rho
\end{align}
$$
and when the wave speed is low
$$
\begin{align}
\frac{u}{c}\ll 1
\end{align}
$$
(if the wave speed is comparable, i.e. a plane breaking the speed of sound, then we get compressible dynamics).



If only pressure gradient and gravity are relevant, then we have a simple equation of motion, but we are on a rotating planet with a rotating reference frame that messes stuff up.

The rotating reference frame means that something going straight up would actually look like it is curving sideways. 

Lets say Earth's angular velocity is $\Omega$. 

$$
\begin{align}
\left( \frac{ d A}{d t }  \right)_{\text{ inertial }} = \left( \frac{ d A}{d t }  \right)_{\text{ rotating }} + \Omega \times A 
\end{align}
$$
where $A$ is a position vector from the center of the axis of rotation (earth's core) to any point. 

We have the relative velocity + the velocity of the object moving around, in super position.

This gives us the transformation to derive a new acceleration equation. We can transform from inertial reference to the rotating frame velocities. 

Newton's second law: $F=m \frac{ d ^{2}r}{d t^{2} }_{\text{ inertial }}$

$$
\begin{align}
\left( \frac{ d^{2}r}{d t^{2} }  \right)_{\text{ inertial }} = \left( \frac{ d }{d t }  \right)_{\text{ inertial }}\underbrace{  \left[  \left(  \frac{ d r}{d t }  \right)_{\text{ rotating }} + \Omega \times r \right] }_{ \tilde{r} } \\
\left( \frac{ d ^{2}r}{d t^{2} }  \right)_{\text{ inertial }} = \left( \frac{ d }{d t }  \right)_{\text{ rotating }} \left[ \left( \frac{ d r}{d t } _{\text{ rotating }}+ \Omega \times r  \right) \right] + \Omega \times \underbrace{ \left[ \left( \frac{ d r}{d t } + \Omega \times r \right) \right] }_{ \tilde{r} }
\end{align}
$$

We define $u_{\text{ rot }}= \left( \frac{ d r}{d t } \right)_{rot}$
We can similarly define 
$$
\begin{align}
\left( \frac{ d u_{in} }{d t }  \right)_{in} = \left[ \frac{ d }{d t }  \right]_{\text{ rot }} [u_{rot}+ \Omega \times r ] + \Omega \times(u_{rot}+\Omega \times r )
\end{align}
$$
We can apply these easily

$$
\begin{align}
\left( \frac{ d u}{d t }  \right)_{in}  = \left( \frac{ d u_{rot} }{d t }  \right)_{rot} + \Omega \times\underbrace{ \left( \frac{ d r}{d t }  \right)_{rot} }_{ u_{rot}  }  
\end{align}
$$
We can move stuff around. We want something that is acceleration in terms of what we actually observe. 


$$
\begin{align}
\left( \frac{ d U_{rot} }{d t }  \right)_{rot} = \left( \frac{ d u_{in} }{d t }  \right)_{in} - \underbrace{ 2  \Omega \times u_{rot} }_{ \text{ coriolis } }  - \underbrace{ \Omega \times \Omega \times r }_{ \text{ centrifugal } }
\end{align}
$$


$$
\begin{align}
\left( \frac{d \vec{u}_{in} }{dt} \right)_{in} = -\frac{1}{\rho}\nabla p - g \hat{z} 
\end{align}
$$
We are almost there.

$$
\begin{align}
\frac{ D \vec{u}}{D t } = - \frac{1}{\rho} \nabla p - g\hat{z} - 2 \Omega \times u - \Omega \times \Omega \times r
\end{align}
$$

This doesn't look fun. We can make a big assumption. Lets define gravity as a potential
$$
\begin{align}
\nabla \phi = \underbrace{ g\hat{z} }_{ gravity } + \underbrace{ \Omega \times \Omega \times r }_{ \text{ centrifugal } }
\end{align}
$$
We call this whole thing "Modified Gravity", or "Effective Gravity". At the equator, the centrifugal direction is exactly aligned with $\hat{z}$. As we go away, $\hat{r}$ is radially inwards whereas $\hat{z}$ is always in one direction - so we have a $\cos\theta$ argument reducing the strength of how much they align / how much centrifugal contributes to the gravity potential. At the poles, they are perpendicular, so not aligned at all. Its a good approximation though (???).

We can now just write
$$
\begin{align}
\frac{D\vec{u}}{Dt}= -\frac{1}{\rho} \nabla p - \nabla \phi - 2 \Omega \times u
\end{align}
$$

We have to add in the Coriolis term - the $2 \Omega \times u$. 

We can make some approximations,