 Recall:
 
#kinematics
Uniform Circular Motion, see [[Kinematics]] 
$$\begin{align}
v = \omega R \\
a_{c} = \omega^2R = \frac{V^2}{r}
\end{align}$$
## First law
Consider an inertial observer $O$ , aka one that is not accelerating. 
This particle is isolated, not interacting with anything. 
It will stay in its inertial frame unless acted upon by another force. AKA
**Momentum is constant for an isolated inertial frame** 
## Second law
The net force acting on a particle is equal to the rate of change of it's momentum
$$ \vec{F}_{net} = \frac{d\vec{p}}{dt}$$
we know that $\begin{align} \vec{p} &= m\vec{v} \\\end{align}$ . If we assume that mass is constant, than
$$
\frac{d}{dt} \vec{p} = \frac{d}{dt(m\vec{v})} = m\times \frac{d\vec{v}}{dt} = ma
$$
thus, $$\begin{align}
\vec{f}_{net} = ma \\
\frac{d\vec{p}_{tot}}{dt} &= \vec{F_{net}}
\end{align}$$ #momentum
## Third law
#notation 
Every action has an equal and opposite reaction.
We notate this as $\vec{F}_{2\to_{1}}=-\vec{F}_{1\to_{2}}$ 
This implies that $\mid\mid \vec{F}_{2\to_{1}}\mid\mid = \mid\mid \vec{F}_{1\to_{2}}\mid\mid$ and that they point in opposite directions on the same line.


## Center of mass
#center_of_mass 
All three laws consider objects about their center of mass, and imagine them as a point particle at that center. COM is the average of their masses, so integrate along the entire surface of the object.

We can express the center of mass as the center in each coordinate in the discrete case.  
$$
\begin{align}
x_{cm} = \frac{\sum_{i = 1}^{N}{m_{i}x_{i}}}{M_{tot}}\\
y_{cm} = \frac{\sum_{i = 1}^{N}{m_{i}y_{i}}}{M_{tot}}\\
\end{align}
$$

 ![[Pasted image 20240118102744.png]]

Changing this into a continuous function, we express this as 
$$
\vec{R}_{cm} =\frac{{ \int \vec{\Gamma} dm }}{M_{tot}}
$$ in 3d objects, $dm = \rho dV$, in 2d objects $dm = \Gamma dA$, and in 1d $dm=\lambda dx$  

If we are finding the center of mass of a single object that is not of uniform density,
$\Gamma_{cm} = \frac{\int_{0}^{l} \lambda(x) \, dx}{L} \hat{x} + \frac{\int_{0}^{l} \lambda(y) \, dy}{L} \hat{y}$   where $\lambda$ is a function of the mass at a position.
total mass $M_{tot}$ is written as $\int \int \lambda(x,y)  \, dxdy$  

For example, lets take a uniform isosceles triangle of Mass M, x length h and width w (center line resting on the x axis) whose tip is located at the origin.
We can integrate this in 2 ways: strips along x, or boxes along x and y. The boxes is more work as a double integral, so lets only do x position bars going up.

$$\begin{align}
X_{cm} &= \frac{\int x \, dm}{M}  \\ \\
y(x) &= \frac{w}{h} x  \\
dm&= \sigma \frac{2w}{h}x dx  \\
M = \int \, dm = \int_{0}^{h} \frac{2\sigma2w}{h}xdx &=  \frac{2\sigma w}{h} \frac{h^2}{2} \int_{0}^{h} x \, dx   \\
x_{cm} &= \frac{2}{3}h
\end{align}$$


See next: [[Gravity and electromagnetism]]
See previous: [[Kinematics]]
reference: [[Formulas]]
#Newtons_laws
