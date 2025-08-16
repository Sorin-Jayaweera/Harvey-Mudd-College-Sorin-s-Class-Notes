---
tags:
  - Phys51
---
## Poynting Vector
$$
\vec{S}_{p} = \frac{\vec{E}\times \vec{B}}{\mu_{0}}
$$
Points in the direction of energy flow with [[magnitude]] of $\frac{\mathrm{Power}}{\mathrm{Area}}$, $[\vec{S}_{p}] = \frac{\mathrm{W}}{\mathrm{m}^{2}}$

##### Derivation - Energy Flow
![[Pasted image 20241031101038.png]]

#### [[Flux]]
$$
\underbrace{ \Phi_{S} }_{\begin{matrix}
\text{Poynting} \\
\text{Flux}
\end{matrix} } = \iint \vec{S}_{p}\cdot d\vec{A} = \iint\left( \frac{\vec{E}\times \vec{B}}{\mu_{0}} \right)d\vec{A}
$$
$[\Phi_{s}]$ = power flowing through surface $S'$ = J/s

**For a closed surface:**

![[Pasted image 20241031101915.png]]
[[Conservation of Energy]]: rate of energy change
$$
{\subset\!\supset} \mathllap{\iint} \vec{S}_{p}\cdot d\vec{A} = -\frac{dU_{enc}}{dt}
$$

#### Example:
$\vec{S}_{p}$ through a resistor
![[special/FriendsNotes/Phys51/Attachments/Pasted image 20241031104311.png]]


### Intensity
Time-averaged $\lvert \vec{S}_{p}\rvert$
$$
I = \;<\lvert \vec{S}_{p}\rvert >
$$
![[Pasted image 20241031104735.png|600]]

$$
<f(t)>\; = \frac{1}{\Delta t} \int _{t}^{t+\Delta t} f(t')dt' 
$$
$$
I = \;<S_{p}>\; =\; < \frac{1}{\mu_{0}}E_{0}\sin (kx-\omega t) \frac{E_{0}}{c}\sin(kx-\omega t)
$$
$$
 =\frac{E_{0}^{2} }{\mu_{0}c }<\sin^{2}(kx-\omega t) > \;=\frac{1}{2} \frac{E_{0}^{2} }{\mu_{0}c^{2} }c
$$
$$
I = \frac{1}{2}\epsilon_{0}cE_{0}^{2} 
$$
Momentum:
For EM Waves
Energy  = momentum $\cdot$ $c$
$$
E = pc
$$
$[\vec{S}_{p}] = \frac{\mathrm{Energy}}{\mathrm{Time}\cdot \mathrm{Area}}$

$$
\frac{\text{momentum/area}}{\text{time}} = \frac{\vec{S}_{p}}{c}
$$
$$
\text{force} = \frac{\text{momentum}}{\text{time}}
$$
$$
\text{pressure} = \frac{\text{force}}{\text{area}} = \left\{\begin{matrix}
\frac{\vec{S}_{p}}{c}\;\;\text{on absorber} \\
\frac{2\vec{S}_{p}}{c}\;\;\text{on reflector}
\end{matrix}\right.
$$
