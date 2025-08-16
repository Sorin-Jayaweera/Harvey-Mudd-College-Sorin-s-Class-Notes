## Energy flow
$U_{e}=\iiint u_{e} dV$
$u_{e}=\frac{1}{2}\epsilon_{0}E^{2}$
$U_{b}=\iiint u_{b} dV$
$u_{b}=\frac{1}{2\mu_{0}}B^{2}$

$U_{tot}=U_{e}+U_{b}$
We found that $\left| B \right|=\frac{\left| E \right|}{c} \implies B^{2}=\frac{E^{2}}{c^{2}}$
We now simplify to get
$$
\begin{align}
\frac{1}{2}E^{2}\left( \epsilon_{0}+\frac{1}{\mu_{0}c^{2}} \right) \\
= \frac{1}{2}E^{2}(\epsilon_{0}+\epsilon_{0}) \\
=\epsilon_{0}E^{2}
\end{align}
$$
This shows that the energy density is the same in the electric and magnetic fields in electromagnetic waves.


>[!abstract]+ Definition: Poynting vector
>$\vec{S_{p}}=\frac{\vec{E}\times \vec{B}}{\mu_{0}}$
> $\vec{S_{p}}$ points in the direction of energy flow.
> Magnitude: $\frac{Power}{Area}$

We make a slab that intersects with the wave that has some thickness and some face area $A$ that the wave passes through. 
$U^{slab}_{tot}=\iiint u_{tot}dV$

$$
\begin{align}
Power &  = \frac{U^{slab}_{tot}}{\Delta t} \\
 & =\frac{1}{\Delta t}\iiint\epsilon_{0}E^{2} \\
 & =\epsilon_{0}E^{2}Ac \\
\frac{Power}{Area} & =\frac{EB}{\mu_{0}}
\end{align}
$$
>[!abstract]+ Definition: Poynting Flux
>$\Phi_{s}=\iint_{s'} \vec{S_{p}}\cdot \vec{dA}$
>$=\iint_{s'} \frac{\left( \vec{E}\times \vec{B} \right)}{\mu_{0}}\cdot \vec{dA}$
>This is the Power flowing through the surface $S'$.
>If we take a closed surface, we get conservation of energy
>$∯\vec{S_{p}}=\frac{-dU_{enc}}{dt}$, the change of energy enclosed in potato.


For example: $\vec{S_{p}}$ through a resistor.
![[sophmore/E&M/images/Pasted image 20241031104311.png]]![[Pasted image 20241031104321.png]]![[Pasted image 20241031104338.png]]
We define a value called intensity:
$\underbrace{ I }_{ scaler }= \underbrace{ <Sp> }_{ \text{ time average } }$
$$
\begin{align}
I= <S_{p}> = \left< \frac{\frac{1}{\mu_{0}}E_{0}\sin(kx-\omega t)E_{0}}{c}\sin(kx-\omega t) \right>   \\
I=\frac{1}{2}\epsilon_{0}cE_{0}^{2}
\end{align}
$$


For momentum:
$E=pc$

$\vec{S_{p}}=\frac{\text{ Energy }}{\text{ Time * Area }}$


