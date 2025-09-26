Maxwells equations in materials. We are worried about free charges instead of total charges in a material, because we want to have a relation from the things that we can control. 

$$
\begin{align}
\vec{\nabla}\cdot \vec{E}=\frac{\rho}{\epsilon_{0}} \\
\vec{\nabla}\cdot \vec{E}_{free}=\frac{\rho _{f r e e}}{\epsilon_{0}} \\
\vec{E} = \frac{\vec{E}_{f r e e}}{\kappa_{e}}
\end{align}
$$
We can now write $\nabla\cdot E=\frac{\rho_{f r e e}}{\kappa_{e}\epsilon_{0}}\implies \frac{\rho_{f r e e}}{\epsilon}$
we have 
$\epsilon= k_{e}\epsilon_{0}$
$\mu=k_{m}\mu_{0}$

Speed of light:
$$
\begin{align}\text{ in a vacuum: }
v & =\frac{1}{\sqrt{ \mu_{0}\epsilon_{0} }}=c \\
\text{ in a material: } v & =\frac{1}{\sqrt{ \mu \epsilon }} \\
 & =\sqrt{ \frac{\epsilon_{0}}{e} }\sqrt{ \frac{\mu_{0}}{\mu} }c \\
 & =\frac{c}{\sqrt{ k_{m}k_{e} }} = \frac{c}{n}
\end{align}
$$
We call this term $\sqrt{ k_{m}k_{e} }$ the refractive index of a material. In a vacuum, n=1. In other materials, the speed of light is lower. 

This gives us Snells law for light in two materials, i.e. $n_{1}\sin \theta_{1}=n_{2}\sin \theta_{2}$ describes the angle of light when entering and leaving a boundary.

Because the frequency of a wave going into a material must stay the same (they're in phase), if the speed of the wave decreases, so must the wavelength. 
![[Pasted image 20241107101527.png]]![[Pasted image 20241107101543.png]]
We can calculate the magnitude of the reflected, transmitted, and initial waves relative to each other with Faraday's law.
$$
\begin{align}
\oint \vec{E}\cdot \vec{dl} =-\frac{d}{dt} \Phi_{b} \\
\left( \left| \vec{E}_{i} \right| + \left| \vec{E}_{r} \right|h\right) -\left|\vec{E}_{t}  \right|h=-\frac{d}{dt} \Phi_{b} \\
\left( E_{i}+E_{r}-E_{t} \right) =0 \\
E_{i}+E_{r}=E_{t}    
\end{align}
$$
We can also use Ampere's Law:
$$
\begin{align}
\oint \vec{B}\cdot \vec{dl} =\mu \epsilon \frac{d}{dt} \Phi_{e} \\
\end{align}
$$
make an Amperian loop with one end outside the material and one end inside. Outside, the reflected wave is going in the opposite direction of the loop, the original wave is going in the direction of the loop, and the transmitted wave (going the same direction as the original) is going the opposite way of the loop (technically we choose an arbitrary loop circulation, but parity is the same). Making the size of the 
$$
\begin{align}
\left| B_{i} \right| h-\left| B_{r} \right| h-\left| B_{t} \right| h \\
\frac{E_{i}n_{1}}{c}\cos(-\omega t)-\frac{E_{r}n_{1}}{c}\cos(+\omega t)-\frac{E_{t}n_{2}}{c}\cos(-\omega t)=0 \\
E_{i}n_{1}-E_{r}n_{1}=E_{t}n_{2}
\end{align}
$$

Solving these two expressions,
$$
\begin{align}
E_{r}=\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right)  \\
E_{t}=\left( \frac{2n_{1}}{n_{1}+n_{2}} \right) 
\end{align}
$$
If $n_{1}<n_{2}$,
The sign of $E_{r} \text{ and } E_{i}$ are opposite. 
If $n_{1}>n_{2}$, they have the same sign. 

Going from a low refractive index, we have a $\pi$ phase shift. 