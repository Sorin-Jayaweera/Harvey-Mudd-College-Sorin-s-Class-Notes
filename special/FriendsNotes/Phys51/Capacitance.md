---
tags:
  - Phys51
---

An isolated [[Conductor]] with [[Charge]] $Q$ will have a [[special/FriendsNotes/Phys51/Electrostatic Potential|potential]] $V_{0}$; $Q$ is proportional to $V_{0}$

**Ex:** Point charge $q$
	$q$ → $2q$ $\implies$ $E$ → $2E\implies V_{0}→2V_{0}$

## Capacitance 
 > [!note]+ Definition 
 > ***Capacitance*** ($\text{C}$) is defined as this proportionality constant between [[Charge]] and [[special/FriendsNotes/Phys51/Electrostatic Potential|potential]]: $$
 > Q = CV_{0}$$
 > ($C\geq 0,\;[\text{Farads}] = \frac{[\text{Coulomb}]}{[\text{Volt}]}$)

Capacitors can be used to store energy



##### Example: Parallel Plate Capacitor
Two parallel plates, equal and opposite charges. Area $A$, charge $Q$ (on each plates), distance between $d$.
$$
E= \frac{\sigma}{\epsilon_{0}} = \frac{Q}{A\epsilon_{0}}
$$
$$
\Delta V = V_{+}-V_{-} = -\int _{-}^{+} \vec{E}\cdot d\vec{s} = +\int _{-}^{+}\left( \frac{Q}{A\epsilon_{0}} \right)ds =\frac{Qd}{A\epsilon_{0}}  
$$
So
$$
V = Q \left( \frac{d}{A\epsilon_{0}} \right) ,
$$
 and since $Q=CV,$
$$
Q = \left( \frac{\epsilon_{0}A}{d} \right) V\implies C_{\parallel} = \frac{\epsilon_{0}A}{d}.
$$


#### Stored Energy
Work done in charging the plates; start with an uncharged plate and move $dq$'s up one at a time.
Infinitesimal work required to bring $dq$ from the bottom plate to the top plate:
$$
dW = dq\Delta V
$$
where $\Delta V(q) = \frac{q}{C}$.
$$
W = \Delta V\cdot Q = \int dW = \int _{0}^{Q}V dq = \int _{0}^{Q} \frac{q}{C}dq   
$$
$$
\implies W= \frac{1}{2C} Q^{2} \iff \frac{1}{2}CV^{2} 
$$

$$
W = U = \frac{Q^{2} }{2C} = \frac{C(\Delta V)^{2} }{2} = \frac{Q\Delta V}{2}
$$
(true for any capacitor shape)

#### Corollary
$$
U = \frac{1}{2}C(\Delta V)^{2} = \frac{1}{2}C(E^{2}d^{2}  )=
\frac{1}{2}\left( \frac{\epsilon_{0}A}{d} \right) (E^{2}d^{2}  )=
\frac{1}{2}\epsilon_{0}E^{2} \underbrace{  (Ad)}_{ \text{volume }[\text{m}^{3} ]  }
$$
$$
u = \frac{U}{\text{volume}} \left[ \frac{\text{J}}{\text{m}^{3} } \right] = \frac{1}{2}\epsilon_{0}E^{2} 
$$
So the energy density stored in the [[special/FriendsNotes/Phys51/Electric Field]] is
$$
u_{e}=\frac{1}{2}\epsilon_{0}E^{2} 
$$


Can we store enough energy in a ball of charge to drive fusion?
$$
W = \int _{0}^{Q}Vdq = \int _{0}^{Q} \left( \frac{q}{4\pi\epsilon_{0}r} \right)dq     
$$
Since $r=\left[\frac{q}{\frac{4}{3}\pi\rho}\right]^{\frac{1}{3}}$
$$
W=\int _{0}^{Q} \left( \text{constant} \right) q^{\frac{2}{3}}   dq
$$
$$
W = \left( \frac{3}{5} \right) \left( \frac{1}{4\pi\epsilon_{0}} \frac{Q^{2} }{R}\right) 
$$

Energy contained in the electric field:
$$
U_{e}=\int \frac{\epsilon_{0}E^{2} }{2}d(\text{Vol}) 
$$
$$
\vec{E} = \left\{\begin{matrix*}[l]
\frac{Qr}{4\pi\epsilon_{0}R^{3} }\hat{r} & \text{if }\; r<R \\
\frac{Q}{4\pi\epsilon_{0}r^{2}  }\hat{r} & \text{if }\; r>R
\end{matrix*}\right.
$$
$$U_{e} = \int_{0}^{R} \frac{\epsilon_{0}}{2}\left[ \frac{Qr}{4\pi\epsilon_{0}R^{3}} \right]^{2}(4\pi r^{2}dr)+\int_{R}^{\infty} \frac{\epsilon_{0}}{2}\left[ \frac{Q}{4\pi\epsilon_{0}r^{2} }\right]^{2}(4\pi r^{2}dr)$$
$$
U_{e} = \frac{3}{5} \left(\frac{Q^{2} }{4\pi\epsilon_{0}R}\right)
$$
Same as other result ✓

