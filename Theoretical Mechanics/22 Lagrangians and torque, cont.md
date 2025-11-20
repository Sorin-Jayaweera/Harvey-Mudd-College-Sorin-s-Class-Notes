
## Review

### Torque-Free Rotation
$$
\begin{align}
\mathscr{L}  & = T_{\text{ rot }}  = \frac{1}{2}\lambda(\dot{\theta} + \sin ^{2}\theta \dot{\phi}) + \frac{1}{2} \lambda_{3}(\dot{\psi}+\dot{\phi}\cos\theta)^{2} \\
P_{\psi }  & = \frac{ \partial \mathscr{L} }{ \partial \psi } = \lambda_{3}(\dot{\psi}+\dot{\phi}\cos\theta) \\
P_{\phi}  & = \frac{ \partial \mathscr{L} }{ \partial \phi } = \lambda \dot{\phi}\sin ^{2}\theta+\lambda_{3}(\dot{\psi}+\dot{\phi}\cos\theta)\cos\theta \\
 & = \lambda \dot{\phi}\sin ^{2}\theta+P_{x}\cos\theta   
\end{align}
$$

Today we will solve for the motion using a Lagrangian.

$\dot{\phi}$: Procession
$\dot{\psi}$: Spin, about the $\hat{z}$ axis.
$\dot{\theta}$: Nutation. Along the line of nodes. 

If we choose $\hat{z}$ along the $\vec{l}$ (angular momentum direction), we can build up our coordinate frame. 
![[Lecture 24.jpeg.jpg|300]]
We can write out the angular momentum in this new frame. Lets also take the assumption that this body is Axisymmetric ($\lambda_{1}=\lambda_{2}=\lambda$)
$$
\begin{align}
l_{z'} & = l\cos\theta   &  = \lambda_{3} \omega_{z'}   & = \lambda_{3}(\dot{\psi}+\phi \cos\theta) \\
l_{\perp'}  & = l\sin\theta    &  =  \lambda \omega_{\perp'}   & = \lambda \dot{\phi}\sin\theta \\
\end{align}
$$
We get from here,
$\dot{\phi}= \frac{l}{\lambda}$
$$
\begin{align}
P_{\phi} = \underbrace{ (\lambda\dot{\phi}\sin\theta )}_{ l_{\perp'} }\sin\theta + \underbrace{ p_{\psi} }_{ l_{z'}  }\cos\theta  \\
P_{\phi} = l\sin ^{2}\theta + l\cos ^{2}\theta = l
\end{align}
$$
We can write out our Euler Lagrange equation:

$$
\begin{align}
\lambda \ddot{\theta}  & = \lambda \dot{\phi}^{2}\sin\theta \cos\theta - \lambda_{3}(\dot{\psi}+\dot{\phi}\cos\theta)\dot{\phi}\sin\theta \\
 & = \dot{\phi}\sin\theta(\lambda \dot{\phi}\cos\theta- P_{\psi} ) \\
 & = \dot{\phi}\sin\theta\left(  \frac{\lambda l}{\lambda} \cos\theta - l\cos\theta\right) \\
 \ddot{\theta} &  = 0 \text{ If } \hat{z} \text{ along  } \vec{l}
\end{align}
$$

## Gyroscopes
In trying to model torque free procession, we made the gyroscope balanced with the center of mass on the hinge:

![[Pasted image 20251119152230.png|400]]
The center of mass is going to be moving around.
$$
\begin{align}
T = \frac{1}{2}Mv^{2}_{\text{ tagged point }} + T_{\text{ cross }} + T_{rot} 
\end{align}
$$

If we make the tagged point the hinge instead of the center of mass, then this will cancel out. Lets define $u=0$ at the line of the fixed point so that the center of mass has a height $dg\cos\theta$ above it.
$$
\begin{align}
T = T_{\text{ rot }}^{\text{ axisymmetric }} + \stackrel{U}{Mgd\cos\theta} 
\end{align}
$$
We get the Lagrangian:
$$
\begin{align}
\mathscr{L} = \frac{1}{2}\lambda(\dot{\theta}^{2}+\dot{\phi}^{2}\sin ^{2}\theta)+ \frac{1}{2}\lambda_{3}(\dot{\psi}+\dot{\phi}\cos\theta)^{2}- Mgd\cos\theta
\end{align}
$$
$P_{\psi}$ and $P_{\phi}$ are both conserved, since $\psi \text{ and } \phi$ don't show up in the Lagrangian. Because there is no time dependence and no time varying axes, the Hamiltonian $\mathcal{H}$ is conserved.   

We can totally make this nice, its just the same as what we did with the two body problem. 

For that, we reduced from 2 variables to 1 by taking advantage of conserved quantities (replacing $\dot{\theta}$ with $\frac{l}{\mu r^{2}}$). 
![[Pasted image 20251119152926.png]]
Note that this $\dot{\phi}$ could be written as
$$
\begin{align}
\dot{\phi} = \frac{P_{\phi}-P_{\psi}\cos\theta}{\lambda \sin ^{2}\theta}
\end{align}
$$

In our case now, the Hamiltonian is
$$
\begin{align}
\mathcal{H}  & = T+U \\
 & = \frac{1}{2} \lambda(\dot{\theta}^{2}+ \dot{\phi}^{2}\sin ^{2}\theta) + \frac{1}{2}\lambda_{3}(\dot{\psi} + \dot{\phi}\cos\theta )^{2}+MGd\cos\theta \\
 & = \frac{1}{2} \lambda\dot{\theta}^{2} + \frac{P_{\psi}^{2}}{2\lambda_{3}} + \frac{(P_{\phi}-P_{\psi} \cos\theta )}{2\lambda \sin ^{2}\theta} + Mgd\cos\theta
\end{align}
$$
Note that $\mathcal{H}$ is constant, and that we just have terms that are either constant or only in terms of $\theta$.

$$
\begin{align}
\frac{1}{2}\lambda\left(  \frac{ d \theta}{d t } \right)^{2} = H- u_{eff}(\theta) \\
d\theta = \pm \sqrt[]{  \frac{2}{\lambda}(H-U_{eff}(0) ) }  dt 
\end{align}
$$
This doesn't have an analytic solution, but qualitatively it looks like the 3 body problem still. 

## Effective Potential

$\theta$ is from $0\text{ to }\pi$. Our $U_{\text{ eff }}$ will explode with $\theta$ is $0$ or $\pi$, because we have a $\frac{1}{\sin ^{2}\theta}$. 

Lets plot.
![[Pasted image 20251119154805.png]]
