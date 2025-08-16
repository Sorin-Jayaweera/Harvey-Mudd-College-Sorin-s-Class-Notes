Imagine a baked potato rotating around an axis. We can add up
$E_{k}=\sum \frac{1}{2}m_{j}v_{j}^{2} = \frac{1}{2}\omega^{2}\sum m_{j}r_{j}^{2} = \frac{1}{2}I \omega^{2}$. 

For instance, a centrifuge spins at 55000 rpm, weighs 20 lbs, and has radius 24 cm.
$$
K=\frac{1}{2}I \omega^{2} \approx \frac{1}{2}\left( \frac{1}{2}MR^{2} \right) \omega^{2}
= \frac{1}{2} \left[ \frac{1}{2}20lb \frac{1kg}{2.2 l b}(0.24m)^{2} \right] \left( 550 \vec{0} \frac{\text{ rot }}{\text{ min }}\frac{2\pi}{1\text{ rot }} \frac{1\text{ min }}{\text{ 60 sec }} \right)
$$


What if we are considering a cylinder that is rolling without slipping? It is pivoting around the bottom of the roll, not about the center.$V=\omega R$
We want to find the kinetic energy, so we have a new formula.

$$
\begin{align}
K' = \sum \frac{1}{2}m_{j}\left| \vec{v'}_{j} \right|^{2}  \\
K = \sum \frac{1}{2}m_{j}\left| \vec{v}_{j} \right|= \sum \frac{1}{2}m \left| \vec{v'}_{j}+\vec{v_{cm} } \right|^{2} 
\end{align}
$$
We can do some nifty math to reduce this to
$K'+ \sum \left( m_{j}\vec{v'}_{j}\cdot \vec{V}_{cm} \right)+\sum \frac{1}{2}m_{j}\left| \vec{v}_{cm} \right|^{2}$
$K = K'+\frac{1}{2}MV_{cm}^{2}$
Total kinetic energy is the kinetic energy if the wheel were only rotating + the energy if the wheel were only translating. 
$K=\frac{1}{2}I'\omega^{2}+\frac{1}{2}MV^{2}_{cm}$ in the laboratory frame. 
Note that $I'$ is the moment of inertia around the center of mass, because the pivot is the point at the ground. 


There is rotational work done by torque,
$W_{rot,\tau}=\int_{i}^{f} \tau \, d\theta$
Total rotational torque done on a system is
$W_{rot,\tau}=\int_{i}^{f} \tau_{net} \, d\theta$
There is a rotational work energy theorem,
$W_{rot,to t}= K_{rot,f}-K_{rot,i}$

For instance, work done by friction on a rotating wheel:

$W_{cm,f}=-F_{s}D$
and
$W_{rot,f}=F_{s}D$

![[Pasted image 20240321105106.png]]
Formulas:

For an object rotating about a fixed axis,
$K = \frac{1}{2}I \omega^{2}$
for an object rotating about it's center of mass, with the center of mass rotating at speed $V_{cm}$,
$K=\frac{1}{2}I'\omega^{2}+\frac{1}{2}MV^{2}_{cm}$

Center axis theorem
$I=I'+Md^{2}$

Angular momentum:
$\vec{L}=I'\vec{\omega}+R_{cm}\times \vec{P}_{cm}$


Moment of inertias:
for a uniform pulley, $I=\frac{1}{2}m_{p}R^{2}$
