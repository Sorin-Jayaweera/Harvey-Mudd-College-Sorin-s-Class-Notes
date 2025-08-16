---
tags:
  - Phys51
---
***Current*** ($i$) is the flow of [[Charge|charges]] through a medium.

$$
i = \frac{dq}{dt}
$$
$[i]=\text{Ampere} = \frac{\text{Coulomb}}{\text{Second}}$


Current density $\vec{j}$, $[j] = \frac{\text{Ampere}}{\text{Meter}^{2}}$
$$
i =\underset{\text{area}  }{ \iint }\vec{j}\cdot d\vec{A}
$$
**Note:** $i$ is the flow of positive charges


If we have a uniform $\vec{j}$, and $\vec{j} \parallel \vec{A}$
$$
i = j(area)
$$




**Conditions for steady current flow:**
- Charge carriers ([[electrons]]) move at a constant speed
- [[special/FriendsNotes/Phys51/Electric Field]] is *not* zero
- Net force from $\vec{E}$ an "drag" force add to zero $\implies$ constant, uniform velocity $v_{d}$.
	- Drift speed $v_{d}$ is typically $1 \frac{\text{mm}}{\text{s}}$
	- Thermal speed of electrons is typically $10^{9} \frac{\text{mm}}{\text{s}}$
	- Slowed by collisions with positive atomic ions in a random walk



$$
\lvert \vec{j}\rvert = \frac{i}{A} = \frac{\frac{q}{\Delta t}}{A}
$$
$q = \rho A L = \rho  A(\Delta t\cdot \underbrace{ v_{d})= (-e)(n)v_{d}\Delta tA }_{ \text{for electrons} }$
$$
\lvert \vec{j}\rvert = \frac{\rho Av_{d}\Delta t}{A\Delta t} = \rho \vec{v}_{d} = (-en)\vec{v}_{d}
$$

**Ohm's Law:**
$$
\vec{j} \propto \vec{E} \implies \vec{j} = \sigma \vec{E}
$$

$\sigma:$ conductivity, $[\sigma] = \frac{1}{\Omega \cdot \text{m}}$, $\frac{1}{\sigma}$ is [[Resistance|resistivity]]




**Resistivity:**

| Material | Resistivity ($\Omega\,\text{m}$) |
| -------- | -------------------------------- |
| Nb (4k)  | $<10 ^{-26}$                     |
| Copper   | $1.69\times 10^{-8}$             |
| Gold     | $2.44 \times 10^{-8}$            |
| Silicon  | $2.5 \times 10^{3}$              |
| Teflon   | $10^{24}$                        |
Wide range of values