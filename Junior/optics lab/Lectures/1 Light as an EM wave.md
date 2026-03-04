
## Derivation of wave equation from Maxwell's equations, in a vacuum and in clear dialectrics
Typo in Steck Eq 4.16


$$
\begin{align}
\vec{\nabla}\cdot \vec{E}= \frac{\rho}{\epsilon_{0}} \\
\vec{\nabla}\times  \vec{E}=-\frac{ \partial \vec{B} }{ \partial t} \\
\vec{\nabla}\cdot \vec{B}=0 \\
\vec{\nabla}\times  \vec{B}=\mu_{0} \vec{J} + \mu_{0}\epsilon_{0}\frac{ \partial \vec{E} }{ \partial t }  
\end{align}
$$


In a vacuum we set $\rho=0$ (charge density) and $\vec{J}=0$ (current density), but in a glass this won't be true. In a vacuum, we can derive
$$
\begin{align}
\nabla^{2} \vec{E} = \mu_{0}\epsilon_{0} \frac{ \partial^{2}\vec{E} }{ \partial t^{2} } \\
\implies c_{0} = \frac{1}{\sqrt[]{ \mu_{0} \epsilon_{0} } } 
\end{align}
$$

Lets look inside a crystal. We can set a "free" and a "bound" charge density.  We also define $\vec{P}$ - the "polarization density", the electric dipole moment per unit volume. 



$$
\begin{align}
\vec{\nabla} \cdot \vec{E} = \left(  \frac{\rho_{\text{ free }} }{\epsilon_{0}}  + \frac{\rho_{\text{ bound }} }{\epsilon_{0}}\right) \\
\epsilon_{0} \vec{\nabla} \cdot \vec{E} - \rho_{\text{ bound }} = \rho_{\text{ free }} 
\end{align}
$$
If we let $\vec{\nabla} \cdot \vec{\rho} = - \rho_{\text{ bound }}$ then we get 
$$
\begin{align}
\epsilon_{0} \vec{\nabla} \cdot \left( \vec{E} + \frac{\vec{\rho}}{\epsilon_{0}} \right) = \rho_{\text{ free }} 
\end{align}
$$

![[Pasted image 20260130103306.png|400]]




$$
\begin{align}
\vec{\nabla}\times \vec{B} = \mu_{0} \vec{J}_{\text{ free }} + \mu_{0} \vec{J}_{\text{magnetic }} + \mu_{0} \frac{ \partial \vec{\rho} }{ \partial t } + \mu_{0} \epsilon_{0} \frac{ \partial \vec{E} }{ \partial t } \\   
\end{align}
$$
We can rearrange the right two terms to be
$$
\begin{align}
\mu_{0} \frac{ \partial  }{ \partial t } (\vec{\rho} + \epsilon_{0} \vec{E})= \mu_{0} \frac{ \partial \vec{D} }{ \partial t } 
\end{align}
$$

Imagine a capacitor, two plates with free space between them. We define $\vec{D}$ as the electric field that would be in that free space. If we place a dielectric between the plates, then the charges in the material rearrange a bit and make the new overall $\vec{E}$. 

We now have
$$
\begin{align}
\vec{\nabla} \times \vec{B} - \mu_{0} \vec{J}_{\text{ mag }}  = \mu_{0} \vec{J}_{\text{ free }}  + \mu_{0} \frac{ \partial \vec{D} }{ \partial t }  \\
\end{align}
$$
Lets make this easier to solve by rewriting $\vec{j}_{\text{ mag }}$ as a curl so that we can pull things together

$$
\begin{align}
\text{ let } \vec{\nabla}\times \vec{M} \equiv \vec{J}_{\text{ mag }}  \\
\vec{\nabla}\left( \frac{\mu_{0}\vec{B}}{\mu_{0}}- \mu_{0} \vec{M} \right) = \mu_{0} \vec{J}_{\text{ free }} + \mu_{0} \frac{ \partial \vec{D} }{ \partial t } 
\end{align}
$$
Lets get rid of all those pesky $\mu_{0}$
$$
\begin{align}
\text{ let } \vec{H} \equiv \frac{\vec{B}}{\mu_{0}} - \vec{M}
\end{align}
$$
Then,
$$
\begin{align}
\vec{\nabla} \times \vec{H} = \vec{J}_{\text{ free }} + \frac{ \partial \vec{D} }{ \partial t } 
\end{align}
$$
What is $\vec{M}?$
The units of $\vec{\nabla}\times \vec{M}$ are $\frac{\text{ current }}{\text{ distance }^{2}}$
So $\vec{M}$ has units $\frac{\text{ current } \cdot \text{ distance }^{2}}{\text{ distance }^{3}}$
$\vec{M}$ is the "magnetization density", is the $\frac{\text{ Magnetic Dipole Moment }}{\text{ volume }}$
![[Pasted image 20260130105110.png|300]]

## Summary
We can't yet derive the speed of light, but we are closer.
We now have new versions of Maxwell's equations.

$$
\begin{align}
\vec{\nabla} \cdot \vec{D} &  = \rho_{\text{ free }} \\
\vec{\nabla} \cdot \vec{B} &  = - \\
\vec{\nabla} \times \vec{E} &  = - \frac{ \partial \vec{B} }{ \partial t }  \\
\vec{\nabla} \times \vec{H} &  = \vec{J}_{\text{ free }} + \frac{ \partial \vec{D} }{ \partial t }  
\end{align}
$$

We have polarization density $\vec{P}$
$$
\begin{align}
\vec{\nabla} \cdot \vec{P} = - \rho_{\text{ bound }} \\
\vec{D} = \epsilon_{0} \vec{E} + \vec{P} 
\end{align}
$$
As well as magnetization density $\vec{M}$
$$
\begin{align}
\vec{\nabla} \times \vec{M} = \vec{J}_{\text{ magnetization }} \\
\vec{H} = \frac{\vec{B}}{\mu_{0}} - \vec{M} 
\end{align}
$$


