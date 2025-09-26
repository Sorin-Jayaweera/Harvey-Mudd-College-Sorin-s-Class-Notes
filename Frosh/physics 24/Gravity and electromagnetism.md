### Gravity
long range but weak. $\propto \frac{1}{\left| r^2 \right|}$ 

Newton's Law of universal gravitation.$F_{1\to2} = -F_{2\to 1}$
$$
\begin{align} \\
F_{g} &= Mg, \, g=9.8 \frac{m}{s}\\
F_{g} &=G\frac{m_{1}m_{2}}{d^2} \\
G &= 6.67 \times \frac{10^{11}m^{3}}{kgs^{2}}
\end{align}
$$
#notation $\hat{\mathrm{Y}}$ is used to notate the direction away from earth's surface

Total force of gravity acting on a block is $\sum_{i} m_{i} g(-\hat{Y}) = Mg(-\hat{Y})$
 Because gravity is constant, this is the same as $M_{tot}g\times(-\hat{Y})$

### Contact forces
charged objects follow coulombs law. Short range but strong
$$
\vec{F_{1\to 2 } = \frac{keq_{1}q_{2}}{\left| \vec{r_{1\to 2}} \right|^2}}\hat{r_{2 ,1}}
$$
for two protons, $\frac{k_{e}q_{1}q_{2}}{Gm_{1}m_{2}}=10^{36}$. Electromagnetism is really strong!

There is also interaction between neutrally charged objects, through 
1) Vander waals Force (two electron clouds distribute electrons wave functions to make them oscillate in sync) $\frac{\propto_{1}}{\left| r \right|^7}$
2) Overlap of electron clouds. Two nuclei then repulse each other, as do overlapping electron louds. $\propto \frac{1}{\left| R^{13} \right|}$ 

Adding these two terms together is called Lennard Jones Force:
$$\begin{align}

\vec{F}_{1\to 2} = \left( -\frac{A}{\left| \vec{r}_{2,1} \right|}+\frac{B}{\left| \vec{r}_{2,1} \right|^{13}} \right)
\end{align}
$$ 
### Applications:
Imagine a book lying on a scale in static equilibrium.

The book experiences $F_{g}$ and an equal/opposite $F_{n}$ from the table. Because it is in static equilibrium, $\vec{A}_{cm} = 0$ (acceleration of the center of mass)
$F_{net}^{ext} = MA_{cm,\hat{Y}}$
A = 0, so $F_{n}-F_{g}=0$, $F_{n}=Mg$
![[Pasted image 20240125102208.png|300]]
###### Answer:
2
Explanation: The ramp isn't touching B, so no interaction there. Ramp touching A will effect A which might effect B, but not directly. Contact forces only work within nanometers. The applied force on A doesn't effect B. It doesn't matter if its moving or accelerating (except for kinetic friction)
###### cont...
![[Pasted image 20240125103211.png|300]]
###### Answer: 
Gravity acts on the center of mass, which points straight down.
They are in contact with the slope, so $F_{n}$ is perpendicular to the slope
There is a $F_{t}$ on the rope pulling them to keep from falling.
lets choose the basis vectors $\hat{X} \, \hat{Y}$ to be tilted. We define $\hat{Y}$ to be aligned with $F_{n}$, and with $F_{t}$ in -$\hat{X}$
We are given an angle $\theta$ below flat. Draw the coordinate grid (basically in that coordinate grid the ground is flat and gravity is at an angle). $Fg$ is $90-\hat{\theta}$ from x, and $\theta$ from y. 
This means that $F_{g,y}=-F_{g}\cos \theta$ and $F_{g,x} = F_{g}\sin \theta$
If we find the limit as $\theta\to 0$, then $F_{g}$ becomes $F_{n}$
But at an angle, $F_{n} = Mg\cos \theta$, where theta is the angle below ground. 
![[Pasted image 20240125104925.png|300]]

See next: [[Springs, Rods, and Ropes]]
reference: [[Formulas]]