---
tags:
  - Phys51
---
**What is a wave?**
From #Phys24 : String, Water, Sound [[Waves]]
In #Phys51 : EM Waves.

##### 1-D
Disturbance (arbitrary shape) in a field that propagates a speed $v$ along $x$.
![[Pasted image 20241029094727.png]]
Caused by:
- The initial disturbance in some field $H(x)$ + coupling to nearest neighbors (nearby $x$)

**Wave Equation**
$$
\frac{ \partial^{2}  H }{ \partial x^{2}  } = \frac{1}{V^{2} } \frac{ \partial^{2}  H  }{ \partial t^{2}  } 
$$
Right/left-propagating wave solution:
$$
H(x,t) =h(x\mp vt)
$$

[[Maxwell's Equations]]: No sources → Wave equation
$$
\left.\begin{matrix}
\vec{\nabla}\cdot \vec{E}=0 \\
\vec{\nabla}\times \vec{E} = -\frac{ \partial \vec{B} }{ \partial t }  \\
\vec{\nabla}\cdot \vec{B} = 0 \\
\vec{\nabla}\times \vec{B} = \mu_{0}\epsilon_{0}\frac{ \partial \vec{E} }{ \partial t }
\end{matrix}\right\}\; \nabla^{2} \vec{E} = \mu_{0}\epsilon_{0}\frac{ \partial^{2}  }{ \partial^{2}  t } \vec{E} 
$$
$$
\frac{1}{V^{2}} = \mu_{0}\epsilon_{0} \implies V = \frac{1}{\sqrt{\mu_{0} \epsilon_{0} }}  = c
$$

But this is from no sources - where does the initial disturbance of the EM wave come from?

**ex**. [[special/FriendsNotes/Phys51/Electric Field#Point Masses|Electric dipole]] (cut wire) or [[Magnetic Field|magnetic dipole]] (ring) connected to a sinusoidal oscillation

##### Generalize from 1D to 3D:
$$
\begin{matrix}

\frac{ \partial^{2}  H(x,t) }{ \partial x^{2}  }  = \frac{1}{V^{2} } \frac{ \partial^{2}  H(x,t) }{ \partial t^{2}  } \\
\downarrow \\
\underset{\text{Laplacian} }{\left(   \frac{ \partial }{ \partial x^{2}  }+\frac{ \partial }{ \partial y^{2}  }+\frac{ \partial }{ \partial z^{2}  }   \right)}H = \frac{1}{V^{2} } \frac{ \partial^{2}  H(x,t) }{ \partial t^{2}  } 
\end{matrix} 
$$$$
\nabla^{2}H(x,y,z,t) = \frac{1}{V^{2} } \frac{ \partial^{2} H(x,y,z,t) }{ \partial t^{2}  }  
$$


#### Properties of EM Waves:
Let $\vec{E}(x,y,z,t)=\vec{E}_{0}f(x-ct) = \vec{E}_{0}\sin(x-ct)$
Constant vector $\vec{E}_{0}= E_{0x}\,\hat{x}+ E_{0y}\,\hat{y}+ E_{0z}\,\hat{z}$
$$
\vec{\nabla}\cdot \vec{E} = 0 \quad(\rho=0)
$$
$$
\frac{ \partial E_{x} }{ \partial x }  + \cancelto{ 0 }{ \frac{ \partial E_{y} }{ \partial y } }  + \cancelto{ 0 }{ \frac{ \partial E_{z} }{ \partial z } } = 0
$$
$$
\begin{matrix}
\frac{ \partial E_{x} }{ \partial x }  = \frac{ \partial  }{ \partial x } (E_{0x}\sin(x-ct))=0 \\
E_{0x}\cos(x-ct) = 0 \implies \underline{E_{0x} = 0}.
\end{matrix}
$$
Therefore, EM waves are transverse: $\vec{E}$ cannot have a component in the direction of propagation.

##### How are $\vec{B}$ and $\vec{E}$ related?
$$
\vec{\nabla}\times \vec{E} = -\frac{ \partial B }{ \partial t } 
$$
Define $\hat{y}$ direction such that
$$
\vec{E} = \underbrace{ E_{0}\,\hat{y} }_{ \begin{matrix}
\vec{E} \text{ points} \\
\text{along }y
\end{matrix}}\;\sin(x-ct)
$$
$$
\vec{\nabla}\times \vec{E}
 = \begin{vmatrix*}
\hat{x} & \hat{y} & \hat{z} \\
\frac{ \partial  }{ \partial x }  & \frac{ \partial  }{ \partial y } & \frac{ \partial  }{ \partial z } \\
0 & E_{0} \sin(x-ct) & 0
\end{vmatrix*}$$
$$
=0\, \hat{x} + 0\,\hat{y} + \frac{ \partial }{ \partial x } (E_{0}\sin(x-ct)) \hat{z}
$$

$$
\implies \frac{ \partial \vec{B} }{ \partial t }  = \frac{ \partial }{ \partial x } (E_{0} \sin(x-ct))\,(-\hat{z})
$$
$\vec{B}$ must points in $\pm \hat{z}$
$$
\frac{ \partial \vec{B} }{ \partial t } = E_{0}\cos(x-ct) \;(-\hat{z})
$$
$$
\implies \vec{B} = \frac{E_{0}}{(-c)}\sin(x-ct)\;(-\hat{z})  = B_{0}\sin(x-ct)\;\hat{z}$$
where
$$
B_{0} = \frac{E_{0}}{c}
$$


#### Plotting
In case of general $f$, same result:
$$
\begin{matrix}
\vec{E} = E_{0}\,\hat{y}\;f(x-ct) \\
\vec{B} = B_{0}\,\hat{z}\;f(x-ct)
\end{matrix}
$$
![[Pasted image 20241029103031.png]]
Aside: $\vec{E}\times \vec{B}=$ direction of propagation




**Idealization:** Sinusoidal "plane waves"
![[Pasted image 20241029105226.png]]
$$
\vec{E} = E_{0} \,\hat{y} \sin(x-ct)\quad\quad\frac{ \partial ^{2} H }{ \partial x^{2}  }  = \frac{1}{c^{2} }\frac{ \partial ^{2}  H }{ \partial t^{2}  } 
$$
$$
\vec{E} = E_{0} \,\hat{y} \sin(kx-\omega t) =E_{0} \,\hat{y} \sin\left( x-\frac{\omega}{k} t \right)
$$
$k$: wave number $=\frac{2\pi}{\lambda}$
$\omega$: angular frequency $=\frac{2\pi}{T} = 2\pi\nu$
$\frac{\omega}{k}=\lambda\nu=c$


#### Energy in [[special/FriendsNotes/Phys51/Electric Field|Electric]] and [[Magnetic Field|Magnetic]] Fields:
General:
$$
U_{E} = \iiint u_{E}\,dV = \iiint\left(\frac{1}{2}\epsilon_{0}E^{2}   \right) dV
$$
$$
U_{B} = \iiint u_{B}\,dV = \iiint\left( \frac{1}{2} \frac{B^{2} }{\mu_{0}} \right) dV
$$
$$
U_{tot} =  \iiint(u_{E}+u_{B})\,dV
$$
For [[Electromagnetic Wave|EM waves]]:
$$
\lvert \vec{B}\rvert  = \frac{\lvert \vec{E}\rvert }{c} \implies B^{2} = \frac{E^{2} }{c^{2} }  
$$
$$
u_{tot} = \frac{1}{2}\epsilon_{0}E^{2}  + \frac{1}{2} \frac{E^{2} }{\mu_{0}c^{2} }
$$
Since $c^{2} = \frac{1}{\mu_{0}\epsilon_{0}}$:
$$
u_{tot} = \frac{1}{2}\epsilon_{0}E^{2} + \frac{1}{2}\epsilon_{0} E^{2} = \epsilon_{0}E^{2}    
$$
$\implies$ EM waves have equal energy density in $\vec{E}$ and $\vec{B}$.


For standing EM wave:
$$
\begin{matrix}
\vec{E} = 2E_{0} \sin(kx)\underline{\cos(\omega t)} \\
\vec{B} = \frac{2E_{0}}{c} \cos(kx)\underline{\sin(\omega t)}
\end{matrix}
$$
Energy is [[Conservation of Energy|conserved]] by being transferred between $\vec{E}$ and $\vec{B}$

## Properties:
Materials reminder: 
A [[Dielectric]] (such as water or glass) reduced the [[special/FriendsNotes/Phys51/Electric Field]]. Define $\vec{E}_{free}$ as the field that *would* have been been due to just $Q_{free}$ alone.
$$
\vec{E} = \frac{E_{free}}{\kappa_{e}}
$$
[[Maxwell's Equations]] in materials:
$$
\vec{\nabla}\cdot \vec{E} = \frac{\rho}{\epsilon_{0}}
$$
Also the case that
$$
\vec{\nabla}\cdot(\vec{E}_{free}) = \vec{\nabla}\cdot(\kappa_{e}\vec{E})= \frac{\rho_{free}}{\epsilon_{0}}
$$
Define permittivity of material $\epsilon$:
$$
\epsilon=\kappa_{e}\epsilon_{0}
$$
So 
$$
\vec{\nabla}\cdot \vec{E}=\frac{\rho_{free}}{\epsilon}
$$
In [[Magnetic Field|magnetic]] materials:
$$
\vec{B}=\kappa_{m}\vec{B}_{free}
$$
$\kappa_{m}$: magnetic susceptibility
Define permeability of the material:
$$
\mu = \kappa_{m}\mu_{0}
$$
$$
\vec{\nabla}\times \vec{B} = \mu \vec{j}_{free} + \mu\epsilon \frac{ \partial \vec{E} }{ \partial t } 
$$
Travelling EM wave in terms of only the free sources
___
##### Speed of Light
In a vacuum:
$$
v = \frac{1}{\sqrt{ \mu_{0}\epsilon_{0} }} = c
$$
In a material:
$$
v = \frac{1}{\sqrt{ \mu\epsilon }} = \frac{1}{\sqrt{ \mu\epsilon }} \cdot \frac{\sqrt{ \mu_{0}\epsilon_{0} }}{\sqrt{ \mu_{0}\epsilon_{0} }} = \sqrt{ \frac{\mu_{0}}{\mu} }\sqrt{ \frac{\epsilon_{0}}{\epsilon} }\; c
$$
$$
 = \frac{c}{\sqrt{ \kappa_{m}\kappa _{e} }} = \frac{c}{n}
$$
where $n=\sqrt{ \kappa_{m}\kappa_{e} } \geq 1$ is the material's ***index of refraction***.

Often, $\mu=\kappa_{m}\mu_{0}\approx\mu_{0}$ for many materials.
___
#### Reflection and Transmission at an Interface
Implications:
$$
v = \frac{d}{T} = \lambda \nu
$$
For vacuum → material:
$$
\begin{matrix*}
\nu_{mat} = \nu_{vac}\\ 
v_{mat} = \frac{v_{vac}}{n}\\
\lambda_{mat} = \frac{\lambda_{vac}}{n} \\
k_{mat} = \frac{2\pi}{\lambda_{mat}} = k_{vac}n
\end{matrix*}
$$
###### Boundary between materials $n_{1}$ and $n_{2}$
![[Pasted image 20241107104657.png]]
$$
E_{r} = \left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right) E_{i}
$$
$$
E_{t} = \left( \frac{2n_{1}}{n_{1}+n_{2}} \right) E_{i}
$$
___
Energy:
$$
<S> = I = \frac{<\vec{E}\times \vec{B}>}{\mu_{0}}\simeq \frac{<\vec{E}\times \vec{B}>}{\mu}
$$
$$
\frac{I_{r}}{I_{i}} = \frac{\frac{E_{r}^{2}n_{1}}{2\mu_{0}c} }{\frac{E_{i}^{2}n_{1}}{2\mu_{0}c} } = \frac{E_{r}^{2} }{E_{i}^{2} }=\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right) ^{2} 
$$

$$
\frac{I_{t}}{I_{i}} = \frac{\frac{E_{t}^{2}n_{2}}{2\mu_{0}c} }{\frac{E_{i}^{2}n_{1}}{2\mu_{0}c} } = \frac{E_{t }^{2}n_{2} }{E_{i}^{2}n_{1} }=\frac{n_{2}}{n_{1}}\left( \frac{2n_{1}}{n_{1}+n_{2}} \right) ^{2} 
$$


