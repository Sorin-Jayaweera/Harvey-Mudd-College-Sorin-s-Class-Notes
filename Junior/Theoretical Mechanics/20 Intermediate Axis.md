We can solve for the equations of motion for the case of a free system with no torques by considering the rotating frame
$$
\begin{align}
\left( \frac{ d \vec{L}}{d t }  \right)_{\text{ inertial }} = \left( \frac{ d \vec{L}}{d t }  \right)_{\text{ rot }}  + \vec{\omega}\times \vec{L}  
\end{align}
$$
This rotating part is asking how the angular moment vector is moving in the rotating frame, and just on top of that we have the motion around a circle in the global space frame. 

If 
$$
\begin{align}
\left(  \frac{ d \vec{L}}{d t }  \right)_{\text{ inertial }} = 0  & &  \text{ (no forces) }
\end{align}
$$
Then we get the Torque free rotation of the components of the $\vec{\omega}$ change with time.

$$
\begin{align}
\dot{\omega}_{x}' = \left( \frac{\lambda_{2}-\lambda_{3}}{\lambda_{1}} \right) \omega_{y}'\omega'_{z}  \\
\dot{\omega}_{y}' = \left( \frac{\lambda_{3}-\lambda_{1}}{\lambda_{2}} \right) \omega_{x}'\omega'_{z}  \\
\dot{\omega}_{z}' = \left( \frac{\lambda_{1}-\lambda_{2}}{\lambda_{3}} \right) \omega_{x}'\omega'_{y} 
\end{align}
$$

For axisymmetric bodies (they have a rotational symmetry about one axis), we have
$$
\begin{align}
(\lambda_{1}=\lambda_{2}=\lambda)
\end{align}
$$
This gives us
$$
\begin{align}
\dot{\omega}'_{z} = 0 \implies \omega_{z}' = \text{ const } \\
\dot{\omega}'_{x} = \Omega_{b} \omega'_{y} \\
\dot{\omega}'_{y} = \Omega_{b} \omega'_{x} \\
 \text{ where } \\
\Omega_{b} = \left( \frac{\lambda-\lambda_{3}}{\lambda} \right) \omega'_{z} 
\end{align}
$$
This $\Omega_{b}$ is a measure of the asymmetry in the object.  If the object had the exact same moments of inertia across each axis, then there would be no rotation. 

Lets think about the earth. $\omega'_{z}$ is 1 rotation in 24 hours.  The earth is slightly oblong, by about $0.3\%$, so we would expect to see a chandler wobble of the earth with a period of ~300 days. As earthquakes etc happen, the principle axes slightly change (on the order of 1 meter off, basically nothing) - but that brings it up to ~ 400 days. That is the component of earth's rotation that is torque free.  

stuff I didn't write down: See the tennis racket (or more formally, intermediate axis) theorem [Wikipedia](https://en.wikipedia.org/wiki/Tennis_racket_theorem).


Lets think about the stability of rotations.

## Around z' axis
Lets solve for the dynamics to leading order in a tiny perturbation from prefection.
$$
\begin{align}
\vec{\omega}  & = \omega_{0}\hat{z} + \epsilon(\omega'_{x}\hat{x}+\omega'_{y} \hat{y} ) \\
\dot{\omega}_{x'}  & = \left( \frac{\lambda_{2}-\lambda_{3}}{\lambda_{1}} \right)(\epsilon \omega_{y}' )\omega_{0} \\
\dot{\omega}'_{y}  & = \left( \frac{\lambda_{3}-\lambda_{1}}{\lambda_{2}} \right) (\epsilon \omega'_{x} )\omega_{0} \\
\dot{\omega}_{z}'  & = \left( \frac{\lambda_{1}-\lambda_{2}}{\lambda_{3}} \right) (\epsilon \omega'_{x} )(\epsilon \omega'_{y} ) = \mathcal{O} (\epsilon^{2}) \approx 0 \\
\omega'_{z}  & = \omega_{0} = \text{ constant }
\end{align}
$$
These rotation equations are non linear, but if we have a small perturbation from equilibrium we can solve.
$$
\begin{align}
\ddot{\omega}'_{x}  & = \delta \left( \frac{\lambda_{2}-\lambda_{3}}{\lambda_{1}} \right)  \omega_{0} \dot{\omega}_{y}' \\
\ddot{\omega}'_{x}  & = \epsilon^{2} \left( \frac{\lambda_{2}-\lambda_{3}}{\lambda_{1}} \right)\left(  \frac{\lambda_{3}-\lambda_{1}}{\lambda_{2}} \right)\omega_{0}^{2}\omega'_{x} 
\end{align}
$$
This goes by $\epsilon^{2}$, but is still the leading order behavior. 

We've ordered the moments of inertia by size, so $\lambda_{1}>\lambda_{2}>\lambda_{3}$.
$\lambda_{3}-\lambda_{1}>0, \text{ but } \lambda_{2}-\lambda_{3}<0$. This gives us the differential equation
$$
\begin{align}
\ddot{\omega}'_{x} = - \Omega^{2} \omega'_{x} 
\end{align}
$$
This gives the usual solution
$$
\begin{align}
\ddot{\omega}'_{x}  = \omega_{x'0} \cos(\Omega t+\delta)
\end{align}
$$
We trace circles because one axis travels in $\cos$ and the other in $\sin$.

What is unique about the intermediate axis for small perturbation?
$$
\begin{align}
\vec{\omega}  & = \omega_{0} \hat{y'} + \epsilon (\omega_{x}' \hat{x'}+ \omega_{z}'  \hat{z'}) \\
\dot{\omega }_{x'}  & = \left( \frac{\lambda_{2}-\lambda_{3}}{\lambda_{1}} \right)\omega_{0} (\epsilon \omega_{z}') \\
\dot{\omega}_{y}'  & = \left( \frac{\lambda_{3}-\lambda_{1}}{\lambda_{2}} \right)(\epsilon \omega'_{x} )(\epsilon \omega'_{z} )  & = \mathcal{O}(\epsilon^{2}) \approx 0 \\
\dot{\omega}'_{z} &  = \left( \frac{\lambda_{1}-\lambda_{2}}{\lambda_{3}} \right)(\epsilon \omega_{x}' )\omega_{0}
\end{align}
$$

We get
$$
\begin{align}
\ddot{\omega}'_{x} = \epsilon^{2} \left( \frac{\lambda_{2}-\lambda_{3}}{\lambda_{1}} \right)\left( \frac{\lambda_{1}-\lambda_{2}}{\lambda_{3}} \right)\omega_{0}^{2}\omega'_{x} 
\end{align}
$$
We now get
$$
\begin{align}
\ddot{\omega}'_{x}  = \Omega^{2}\omega'x
\end{align}
$$
This is positive, because both $\lambda_{2}-\lambda_{3} <0 \text{ and } \lambda_{1}-\lambda_{2}<0$.
The solutions grow exponentially, we will leave equilibrium as perturbations push us away.
$$
\begin{align}
\omega'_{x} (t) = Ae^{\Omega t}+ Be^{-\Omega t}
\end{align}
$$
The intermediate axis must, therefore, always be an unstable axis to rotate about. 

