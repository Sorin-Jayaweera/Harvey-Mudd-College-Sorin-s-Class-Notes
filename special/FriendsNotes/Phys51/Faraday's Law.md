---
tags:
  - Phys51
---
With time dependence, only [[Gauss's Law]] and [[Maxwell's Equations|no monopoles]] still apply.

For [[Maxwell's Equations|Faradays' Law]]:

#### Faraday's Law: 
##  
 > [!abstract]+ Faraday's Law #1
 > The ***electromotive force*** $\varepsilon$ around a loop is given by
> $$ \varepsilon_{loop} = -\frac{d}{dt}\Phi_{B} = -\frac{d}{dt} \iint\vec{B}\cdot d\vec{A}, $$
> where $\Phi_{B}$ is the [[Flux]] of the [[Magnetic Field]] through the area enclosed by the loop.
> $$ \oint \vec{E}\cdot d \vec{l} = -\frac{d}{dt} \iint\vec{B}\cdot d\vec{A}$$

![[Pasted image 20241017095611.png|500]]

Changing magnetic [[Flux]] through a loop induces a current, so it must induce [[special/FriendsNotes/Phys51/Electric Field]] point around the loop.


**Electromotive Force:**
$$
\varepsilon = \frac{W}{q} = \frac{1}{q} \int \vec{F}\cdot d\vec{l} 
$$
$[\varepsilon]=\mathrm{V}$. **Not** a force. Work per unit charge that can establish a current in a circuit. Arises from an external source of energy.


#### Lenz's Law
Induced EMF around a loop is always in the direction that **opposes the change*** in the magnetic flux through the loop. Tells sign/direction of $\varepsilon$.
$$
\lvert \varepsilon_{loop}\rvert  = \left\lvert  \frac{d}{dt} \Phi_{B} \right\rvert 
$$
![[Pasted image 20241017100040.png|500]]


#### Example:

![[Pasted image 20241017100500.png|500]]

Closing the switch leads to a $\vec{B}$ that points towards the battery. To oppose this change in flux, a CCW current is induced in the left loop. "South poles" of the loops are both facing inside, leading to a repulsive force.



#### Example:
Circuit around solenoid
![[Pasted image 20241017103007.png]]
#### Example:
Resistor bar moving in uniform $\vec{B}$
![[Pasted image 20241017104238.png]]


#### Differential Form
$$
\varepsilon = \int \frac{\vec{F}_{E}}{q} \cdot d\vec{l} = \oint\vec{E}\cdot d\vec{l} = -\frac{d}{dt}\Phi_{B}
$$
$$
\implies \vec{\nabla}\times \vec{E} = -\frac{ \partial B }{ \partial t } 
$$
