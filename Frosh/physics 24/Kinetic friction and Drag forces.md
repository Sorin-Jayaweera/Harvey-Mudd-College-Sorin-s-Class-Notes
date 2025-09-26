Kinetic friction is when two bodies are moving relative to each other and sliding instead of gripping.

We label this $\vec{F}_{k}$

Typically static friction coefficient is greater than kinetic. 
A box moves to the right with static friction. 
![[Pasted image 20240208095825.png]]
![[Pasted image 20240208095849.png]]
![[Pasted image 20240208095935.png]]
![[Pasted image 20240208095952.png]]
![[Pasted image 20240208100019.png]]

# Drag force:
Air resistance, etc. We don't want to ignore this beast anymore. 
Its like kinetic friction but for a fluid. The faster you move the more drag is experienced. 
There are two main types of drag forces.

## Viscous drag
#viscous_drag: $\vec{F}_{D}\propto v$
For a spherical object of radius $R$, $F_{d}=6\pi \eta Rv$, where Eta $\eta$ represents the viscosity.
We typically ignore inertial drag.
Dropping a ball through a viscous fluid,
twice the radius $\implies$ four times the speed?
![[Pasted image 20240208102525.png]]
Because we have mass on the top, twice the radius increases he mass. $M=\frac{4}{3}\pi R^{3}$
this makes the effect of the radius overall $R^{2}$. So yes! $2R\to 4V_{terminal}$


![[Pasted image 20240208103627.png]]
![[Pasted image 20240208103658.png]]
![[Pasted image 20240208103716.png]]

## Inertial drag
#inertial_drag: $\vec{F}d\propto v^{2}$
When a bus passes, you can feel a whoosh. This is the momentum imparted by high speed large objects. Caused by the transfer of momentum. 
$F_{0}=\frac{1}{2}\rho_{f}C_{D}Av^{2}$.
$C_{D}:$Drag coefficient 
$\rho_{f}:$ density of the fluid 

Imagine a mass M moving through fluid. We make the system the mass + fluid particles. Total momentum of the system is conserved. Lets say that the fluid particles all stick to the mass.
$P_{tot,x}^{t}=P_{tot,f}^{x}$
$Mv(t) = (M+m_{stuck})v(t+dt)$
$-m_{stuck}V(t+dt) = M(v(t+dt)-v(t))$ 
$m_{stuck}=\rho_{f}V_{stuck}=\rho_{f}(AD)$ mass of stuff stuck to the object is density time area * area per time (v(t))
$m_{stuck}=\rho_{f}(A\times v(t)\times d t)$ We can now sub this in
-$\left( \rho_{f}Av(t)dt \right)v(t+d t) = M \frac{v(t + dt)-v(t)}{d t}$
$\lim_{ d t \to 0 } -\rho_{f}Av(t)=M \frac{d}{dt}$