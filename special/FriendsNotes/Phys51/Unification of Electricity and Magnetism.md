---
tags:
  - Phys51
---

Consider an infinitely long [[Current]]-carrying wire (length $L$, cross-sectional area $A$, drift velocity $v$.) and an [[electrons|electron]] outside of the wire with velocity $v$ and a distance $r$ from the center of the wire.

$\vec{E}$ and $\vec{B}$ fields "mix" upon change of inertial frames. Observers in different reference frames will calculate equivalent EM forces on a object but will attribute it differently to $\vec{E},\vec{B}$ forces.

### Unprime Frame:
Wire/ions at rest, moving electrons
![[Pasted image 20241010131357.png]]
Force on electrons by magnetic field:
$$
\vec{F}_{B}= q\vec{v}\times \vec{B}
$$
$$
\vec{B} = \frac{\mu_{0}i}{2\pi r}\; \hat{\otimes } \;\text{at e}^{-}\text{ position} 
$$
where $i=jA = \rho_{-}vA$ and $\rho_{tot} = \rho_{+}-\rho_{-} = 0$ (neutral)
$$
\vec{F}_{B}= e\vec{v}\times \vec{B} = \frac{e\mu_{0}\rho_{-}v^{2}A }{2\pi r} (-\hat{y}).
$$

### Prime Frame
Electrons at rest, moving wire/ions
![[Pasted image 20241010132016.png]]
$$
\vec{F}'_{B} = -e \cancelto{ 0 }{ \vec{v}' } \times \vec{B}' = 0 \implies \vec{F} = q\vec{E} + \cancelto{ 0 }{ q\vec{v}\times \vec{B} }
$$
No magnetic force, so electrons must feel an electric force that matches the unprime frame.

Unprime:$\rho_{+} = \rho_{-}$
Prime: $\rho_{+}'> \rho_{-}'$
$$
\rho_{+}' = \frac{Q}{AL/\gamma} = \frac{\gamma Q}{AL} = \gamma\rho_{+} = \gamma\rho_{-}
$$
$$
\rho_{-}' = \frac{Q}{AL\gamma} = \frac{1}{\gamma}\rho_{-}
$$
$$
\rho_{tot}' = \rho_{+}'-\rho_{-}' = \gamma \rho_{-}-\frac{1}{\gamma}\rho_{-}  = \gamma\rho_{-}\left(1 -\frac{1}{\gamma} \right)  = \gamma \frac{v^{2} }{c^{2} }\rho_{-} > 0
$$
By [[Gauss's Law]]
$$
{\subset\!\supset} \mathllap{\iint}\vec{E}\cdot d\vec{A} = \frac{Q'_{enc}}{\epsilon_{0}}
$$
By symmetry with Gaussian cylinder radius $r'$ and length $l'$: $\vec{E}' =\vec{E}(r')\;\hat{r}' = E'(r)\; \hat{r}$.
$$
E'(r) \hat{r} \cdot 2\pi r'l' = \frac{\rho'_{tot}l'A}{\epsilon_{0}} \implies E'(r) = \gamma\frac{v^{2}\rho_{-}A }{\epsilon_{0}c^{2} 2\pi r}\; \hat{r}
$$
$$
\vec{F}_{E} = \frac{\gamma ev^{2} \rho_{-}A}{\epsilon_{0}c^{2}2\pi r }\; (-\hat{y})
$$

Math suggests that
$$
\vec{F}_{B} = \vec{F}_{E}'
$$
$$
\mu_{0} \frac{ev^{2}\rho_{-}A }{2\pi r} \overset{?}{=} \frac{1}{\epsilon_{0}c^{2} } \frac{ev^{2} \rho_{-}A }{2\pi r}
$$
$$
\mu_{0} \overset{?}{=} \frac{1}{\epsilon_{0}c^{2} }
$$
$$
c \overset{✓}{=} \frac{1}{\sqrt{ \mu_{0}\epsilon_{0} }}
$$


##### In general:
$$
\begin{matrix*}[l]
\vec{E}'_{\parallel} = \vec{E}_{\parallel}  \\
\vec{E}'_{\perp} = \gamma[\vec{E}_{\perp}+\vec{v}\times \vec{B}] \\
\vec{B}'_{\parallel} =\vec{B}_{\parallel}   \\
\vec{B}'_{\perp} = \gamma\left[ \vec{B}_{\perp}-\frac{1}{c^{2}}\vec{v}\times \vec{E}  \right]
\end{matrix*}
$$



 