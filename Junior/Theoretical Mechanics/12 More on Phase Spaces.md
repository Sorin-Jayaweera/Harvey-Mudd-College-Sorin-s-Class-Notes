## Pendulum on an Oscillating Support
Lets make the fixed point of the pendulum vibrate up and down.

![[Pasted image 20251008145445.png]]

$$
\begin{align}
y_{\text{ support }}  = a\cos(\Omega t)
\end{align}
$$

The Lagrangian is
$$
\begin{align}
\frac{1}{2}ml^{2}\dot{\theta}^{2}+mgl\cos\theta +mal \Omega^{2}\cos \Omega t\cos\theta \\
\ddot{\theta} = -\left[ \frac{g}{l}+ \frac{a\Omega^{2}}{l}\cos \Omega t \right]\sin\theta
\end{align}
$$
The free parameters are
$$
\begin{align}
m,l,a,\Omega,g
\end{align}
$$
If we wanted to try 3 cases for each free parameter, that's way too many. Lets write each of these expressions to reduce how many things we have to vary, so that we aren't redundant.

For small angle if we ignore the pivot, then we have
$$
\begin{align}
\omega_{0}^{2}= \frac{g}{l}
\end{align}
$$
We have some arguments that actually matter:
$$
\begin{align}
\frac{g}{l}, \frac{\alpha \Omega^{2}}{l}, \text{ and }  \Omega tg
\end{align}
$$
Lets see how we can modify our expression for non-dimensionalization.
Let $\tau=\frac{t}{T}=\Omega t$, where $T$ is the timescale $\frac{1}{\Omega}$.

$$
\begin{align}
\frac{d}{dt} = \frac{ d }{d \tau } \frac{ d \tau}{d t } = \Omega \frac{ d }{d \tau } 
\end{align}
$$
We can write our second order differential equation in terms of the dimensionless variables.
$$
\begin{align}
\frac{ d ^{2} \theta}{d t^{2} } = \Omega^{2} \frac{ d ^{2}\theta}{d \tau^{2} }  = -\omega_{0}^{2}\left[ 1+ \frac{\alpha \Omega^{2}}{g}\cos \tau \right] \sin\theta
\end{align}
$$
We let $\tau$ be its own free variable because even though it depends on $\Omega$, it is a thing that changes with time -- so it could be unique from the other instances of $\Omega$. 

$$
\begin{align}
\frac{ d ^{2}\theta}{d \tau^{2} } = -\frac{\omega^{2}}{\Omega^{2}} \left[  1+ \frac{\alpha \Omega^{2}}{g}\cos \tau \right]\sin\theta \\
\frac{ d ^{2}\theta}{d \tau^{2} } = - \alpha^{2} [ 1+ \beta \cos(\tau)]\sin\theta
\end{align}
$$
We now only have two parameters:
$$
\begin{align}
\alpha^{2} = \frac{\omega^{2}}{\Omega^{2}} \\
\beta= a \frac{\Omega^{2}}{g}
\end{align}
$$
where $\alpha$ is how fast were driving, and $\beta$ is a dimensionless measure of how strong the perturbation is.  $\theta$ and $\tau$ are dimensionless, so the parameters should be as well. 

We really have three variables - $\theta,\dot{\theta},\tau$. The $\tau$ argument is in a cos, so it looks like an angle even though its related to time - so we can draw our state space in 3d with each plane as a cross section of a rectangular torus. 
![[Pasted image 20251008152245.png|500]]


## Poincare' Surface Sections


If we draw our weird donut thing and have a specific plane cutting through at one angle and then record all the intersections, then we'll have found the Poincare' surface. 

We only plot points when they pass through our cross section. There are two things that could happen:

* If points fall on a 1D curve (i.e. a circle) then there is a relationship between $\theta$ and $\dot{\theta}$, maybe a conserved quantity. 
* Fill a 2D area - no nice curve, but scattering all over the place (the generic usual outcome when things can end up anywhere in state space). There are many more questions from here - is the area densely filled, only certain regions, etc.

### Regular Trajectory (non chaotic)
* Shows up as a 1D curve on the section. 
* We can write down a valid solution for any arbitrary time in terms of periodic functions.  

### Chaotic Trajectory
* Fills a 2D area on a section
* Aperiodic
* Can't write down a solution








 