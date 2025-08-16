---
lecture: phys-51-9
---
On the docket for today:
1) Flowing charge $\rightarrow$ current
2) Ohm's law
3) Circuits & Kirchoff's laws
4) Energy and Joule heating
5) Time varying circuits

## Circuits
- Positive current $\implies$ flow of positive charges
- batteries have $\nabla v=E$
- Resistors have $v=IR$
- a wire has $R=0,\implies V=0$


## Current:
Current is measured as $i=\frac{dq}{dt}$ ($\frac{\text{ coulombs }}{\text{ second }}$), the rate of flow of charge.
We can define a current density $\vec{j}$, in $\frac{\text{ ampre }}{m^{2}}$
$i=\iint \vec{j}\cdot  \vec{da}$.

If we have a uniform $\vec{j}, \text{ and }  j \left|  \right|\vec{dA}$, then $i=jA$

note that the positive direction for $\vec{dA}$ is in the positive flow of current.
$\vec{dA}$.

Because current means that electrons are flowing (they go in the opposite direction that current flows), there must be an electric field. However, for them to flow at a constant speed, there has to be a 'drag' or 'viscous' force.
While they are bouncing around with a thermal speed $\approx 10^{9} \frac{mm}{s}(\text{ 1\% the speed of light! })$, they have a drift speed along the length of a wire around $1 \frac{mm}{s}$. 

we have Charge $q=\rho Ac$
$$
\begin{align}
= \rho A(vd\nabla t) \\
= (-e)(\underbrace{ n }_{ \text{\# electrons/volume } }Vd \nabla tA) \\
\end{align}
$$
we can write now
$$
\begin{align}
\vec{j}=\frac{i}{A}=\frac{\frac{q}{\nabla t}}{A}=\frac{\rho Av_{d}\nabla t}{A\nabla t} \\
\vec{j}=\rho v_{d}
\end{align}
$$
note that $v_{d}$ is the distance/time that an electric charge is moving. 

We can empirically claim that
$\vec{j}\propto \vec{E}$. We can call the constant that is the proportion between each other $\sigma$. $\vec{j}=\sigma\vec{E}$. This is Ohm's law. $\sigma$ is conductivity,
$[\sigma]=\frac{1}{ohm*m}$, $\frac{1}{\sigma}$ is resistivity.

We can rewrite this in the form that we usually think of for Ohm's law.
![[Pasted image 20240924100832.png]]


## Kirchhoff's laws:

1) Conservation of energy:
The sum of voltage drops around a loop = 0. 
We can express the potential $u=q\nabla v$
2) Conservation of charge
The current flowing into a node = the sum of current out of the node.



Two resistors in series:
$$
\begin{align}
R_{1}+R_{2}=R_{eff}
\end{align}
$$
Two resistors in parallel:
$$
\begin{align}
\left( \frac{1}{R_{1}}+\frac{1}{R_{2}} \right)^{-1}=R_{eff} 
\end{align}
$$


Power from a battery is $P_{battery}=iV_{0}$.
Power for any circuit component that is dissipated = $iV=i^{2}R$ 

See previous: [[Capacitors, Electrostatic energy, and Fusion]]
See next: [[The Magnetic Field]]
