---
tags:
  - Phys51
---
**On a Point Charge:**

$$
\vec{F}_{B} = q\vec{v}\times \vec{B}
$$
**In combination with an [[special/FriendsNotes/Phys51/Electric Field]]:** [[Lorentz Force]]

**On a Current-carrying Wire:**
$$
\vec{F}_{wire} = i\vec{L}\times \vec{B}
$$



$$
[\vec{B}] = \frac{\text{Force}}{\text{Charge}\cdot \text{Velocity}} = \frac{\text{kg}}{\text{C}\cdot \text{s}} = \text{Telsa}
$$

|                        | $B\; \text{(T)}$ |
| ---------------------- | ---------------- |
| Earth Surface          | $0.00006$        |
| Sunspots               | $0.4$            |
| Refrigerator magnet    | $0.01$           |
| Sustained in Lab       | $45$             |
| Briefly created in Lab | $10^3$           |
| Neutron Stars          | $10^8-10^{11}$   |





## Force on a Moving Charge
![[Pasted image 20241001101516.png]]

Undergoes [[Uniform Circular Motion]]
$$
\sum F_{r} = -qvB = ma_{r}
$$
$$
-qvB = m \frac{v^{2} }{R} \implies R = \frac{mv}{qB}
$$
#### Example:
Mass Spectrometer #Chem42 

![[Pasted image 20241001102848.png]]Only particles with specific velocity can pass through
If $\sum F_{y} = 0$, then
$$
qvB = qE \implies v = \frac{E}{B}
$$
Combine with previous result:
$$
R = \frac{mv}{qB} = \frac{mE}{qB^{2} }=R
$$
Mass-to-Charge Ratio:
$$
\frac{m}{q} = \frac{B^{2}R}{E} 
$$

## Force on a [[Current]]
![[Pasted image 20241001103525.png]]
Cross-sectional area $A$.
$$
\vec{j} = \rho \vec{v}_{d} =-ne\vec{v}_{d}
$$
Force per electron:
$$
\vec{F}_{B,e} = -e\vec{v}_{d}\times \vec{B} = \frac{\vec{j}}{n}\times \vec{B}
$$
Force on length $L$ of wire:
$$
F_{\text{wire}} = \underbrace{ \frac{\vec{j}}{n} \times B }_{ \vec{F}_{B,e} }\;\times\;nLA$$
$$
\implies F_{\text{wire}} = \vec{j}(LA) \times \vec{B} = \vec{iL} \times \vec{B}
$$
Notation:
$$
F_{\text{wire}} = i\vec{L}\times \vec{B}
$$
where $i\vec{L}$ points in the direction of $\vec{j}$.


