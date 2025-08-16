### important concepts
see [[Newtons Laws]] 
always label the axis that you are using to referenced
always justify any equations and specify any assumptions, i.e. that acceleration is constant

CONSTANT SPEED DOESN'T MEAN NO ACCELERATION, AS CIRCULARLY THERE IS CENTRIPITAL ACCELERATION FOR CONSTANT TANGENTAL SPEED.
[W] refers to the units of Wb
some standard units
$$
\begin{aligned}
\vec{v} &= LT^{-1} \\
\\
E &= mc^2 \\
 &= [m][LT^{-1}]^2 
\end{aligned}
$$



We typically describe position, velocity, and acceleration with a set of basis vectors. 
We can define the basis vectors as any pair of axis that are not on the same span, allowing for some combination of that vector to find any coordinate. These basis vectors are typically expressed $$
\begin{matrix}
\hat{x} & \hat{y} & \hat{z}
\end{matrix}$$
we should think of velocity as an expanded product rule. For cartesian basis vectors that don't change over time,
$$
\begin{align}
\vec{v} &= \frac{\vec{dr}}{dt} = \frac{d}{dt} x(t)\hat{x} + \frac{d}{dt} y(t)\hat{y}
\end{align}
$$
which can be expanded by product rule for derivatives along each basis vector   

###### tricky notes in notation:
#notation
any vector quantity requires the vector sign $\mid\mid\vec{x}\mid\mid = \mid\vec{x}\mid = x$ which is the magnitude.
$a_{0}$ represents a constant
### Parabolic motion
we can say that
$$
\vec{t} = c_{1}t\hat{x} + (c_{2}t - c_{3}t^2)\hat{y}
$$
we can see that x(t) is given by a constant c1 
and y(t) is given by a function $$
(c_{2}-2c_{3}t)
$$
we can find the acceleration to be a constant $$
\vec{a}(t) = \frac{d\vec{v}}{dt} = -2c_{3}\hat{y} = g = \frac{9.8m}{s^2}
$$
If instead,, we wanted to go from acceleration to position, then it is a more complicated story. 
for instance, there are some interesting differential equations that appear throughout physics.
$$
\begin{matrix}
\vec{a} = -c_{1}\vec{v} + \vec{c}_{2} & \vec{a} = -c_{2}v_{1}\vec{r} + c_{2}\vec{}  \\

\end{matrix}
$$

**If we assume that we have uniform acceleration**, then we can integrate to get velocity, and integrate again to get position over time. 
$$
\begin{aligned}
dx = V_{x}(t) \\
= v_{0}+a_{0}t \\
\end{aligned}
$$
which yields $\int_{0}^{t} (v_{0}+a_{0}t) \, dt$ 
$$
\vec{v}(t)=\vec{v_{0}} + \vec{a}t ,  \vec{r}(t)=\vec{r_{0}} + \vec{v}_{0}t +{ \frac{1}{2}}at^2
$$
### circular motion
We also have a rotational equivalent of speed and acceleration. Given $\theta$ as a position, $\omega$ as an angular velocity, and $\alpha$ as angular acceleration. $\theta = \omega t$ describes uniform circular motion. in a circle there are $2\pi$ radians that can be traveled across. We have an exact equivalent to linear motion, using x position as angle. The magnitude of a uniform circular motion is R, and the acceleration is always radially inwards towards the center of the circle as $-\omega^2 \times R$ 

For Uniform circular motion,
$$
\begin{align}
v = \omega r \\
a_{c} = \omega^2r = \frac{v^2}{r} \\
\theta=\omega t
\end{align}
$$


see next: [[Newtons Laws]]
reference: [[Formulas]]
#kinematics
#circular_motion
#uniform_motion
#physics
