---
tags:
  - Phys51
---
Does a one wire loop experience induction? Yes, induced back [[special/FriendsNotes/Phys51/Faraday's Law|EMF]] arising from self inductance.

#### Derivation:
By [[special/FriendsNotes/Phys51/Faraday's Law]]:
$$
\varepsilon = -\frac{d}{dt}\Phi_{B}
$$
$$
\Phi_{B} = \iint \vec{B}\cdot d\vec{A}
$$
Non-uniform/symmetric $\vec{B}$, so by [[Biot-Savart Law]]:
$$\vec{B} = \underset{ \text{loop} }{ \int } \frac{\mu_{0}}{4\pi}  \frac{id\vec{l}\times \hat{r}}{r^{2} }$$
Define the inductance, $L$:
$$
\Phi_{B} = i \underbrace{ \left[\underset{ \text{area} }{ \iint } \underset{ \text{loop} }{ \int } \left(\frac{\mu_{0}}{4\pi} \frac{d\vec{l}\times \hat{r}}{r^{2} }\right)\cdot d\vec{A} \right] }_{ L }
$$
$$
\varepsilon = -\frac{d}{dt} (iL) = -L \frac{di}{dt} \implies \varepsilon_{ind}=L \left\lvert  \frac{di}{dt} \right\rvert 
$$
**Units:**
$$
[L] = \frac{\mathrm{V}\cdot \mathrm{s}}{\mathrm{A}} = [\mu_{0}]\cdot \mathrm{m}
$$


#### Example:
Solenoid, calculate $L$:
![[Pasted image 20241022095956.png|650]]


### Definition:
An ***inductor*** is a [[Circuit Diagram|circuit element]] that stores energy in the [[Magnetic Field]]. Characterized by its *inductance*, $L$. Simplest example: solenoid.
![[Pasted image 20241022100540.png|450]]
**Kirchhoff Rule:**
$$
-\varepsilon = V_{a}-V_{b}=L \frac{di}{dt}
$$
#### Example:
LR circuit
![[Pasted image 20241022102340.png]]

## Energy in $B$ Fields:

$[\mathrm{Power}] = {\mathrm{J}}/{\mathrm{s}}$
$[V] = \mathrm{J} / \mathrm{C}$
$[i]=\mathrm{C} / \mathrm{s}$
$$
\frac{dW}{dt} = P = i\Delta V
$$

Work to "charge up" an inductor:
$$
W = \int P dt = \int \underbrace{ \left( i L \frac{di}{dt} \right) }_{ P }  dt = \frac{1}{2}Li^{2} 
$$

For solenoid, $B$ is constant
$$
\implies u_{B} = \frac{\mathbb{U}_{B}}{V_{sol}} = \frac{\frac{1}{2}Li^{2} }{\pi r_{s}^{2}l } = \frac{\frac{1}{2}(\mu_{0}n^{2}\pi r_{s}^{2}l)  i^{2} }{\pi r_{s}^{2}l } = \frac{1}{2}\mu_{0}n^{2}i^{2} = \frac{1}{2}\frac{B^{2} }{\mu_{0}} 
$$




Parallels with [[Capacitance|capacitors]]:

| Property        | Capacitors                           | Inductors                                                            |
| --------------- | ------------------------------------ | -------------------------------------------------------------------- |
| Proportionality | $\lvert Q\rvert=C \lvert V\rvert$    | $\lvert \varepsilon\rvert=L \left\lvert  \frac{di}{dt} \right\rvert$ |
| Energy Stored   | $\mathbb{U}_{E}=\frac{Q^{2}}{2C}$    | $\mathbb{U}_{B}=\frac{1}{2}Li^{2}$                                   |
| Energy Density  | $u_{E}=\frac{1}{2}\epsilon_{0}E^{2}$ | $u_{B}=\frac{1}{2} \frac{B^{2}}{\mu_{0}}$                            |


#### Example:
LC Circuits
![[Pasted image 20241022105128.png]]






