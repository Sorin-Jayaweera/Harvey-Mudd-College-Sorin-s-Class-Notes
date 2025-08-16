---
tags:
  - Phys51
---

## Electrostatics

 > [!abstract]+ Ampere's Law
 > $$ \underset{ \begin{matrix}
\text{ a closed} \\ \text{loop}
\end{matrix} }{ \oint } \vec{B}\cdot d\vec{l} = \mu_{0}i_{enc}= \mu_{0}\underset{ \begin{matrix}
\text{area} \\ \text{enclosed} \\ \text{by loop}
\end{matrix} }{ \iint }\vec{j}\cdot d\vec{A} $$
> LHS: $\vec{B}$ due to all current
> RHS: $i_{enc}$ current "punctured" by the surface

([[Maxwell's Equations]])
#### Example 1:
Infinitely long, thin wire

![[Pasted image 20241008100534.png]]




#### Example 2:
Infinitely long, thick wire
![[Pasted image 20241008103423.png]]


#### Example 3:
Infinitely long solenoid
![[Pasted image 20241010094102.png]]




## Electrodynamics

**Static Recap:**
Infinite wire, $\vec{B}$ at some $r$:
LHS: $\oint \vec{B}\cdot d\vec{l} = B(r)2\pi r$,   RHS: $\mu_{0}i_{enc} = +\mu_{0}i$
$B(r) = \frac{\mu_{0}i}{2\pi r}$

![[Pasted image 20241024101024.png]]

Law Derivation:
![[Pasted image 20241024101033.png]]

So
$$
\oint\vec{B}\cdot d\vec{l} = \mu_{0}i_{enc} + \mu_{0}\epsilon_{0} \frac{d}{dt}\iint\vec{E}\cdot d\vec{A}
$$
([[Maxwell's Equations]])



**Application:** $\vec{B}$ in between plates of [[Capacitance|capacitor]]
![[Pasted image 20241024101952.png]]

### Displacement Current $i_{D}$:
$$
\oint\vec{B}\cdot d\vec{l} = \underbrace{ \mu_{0} \iint \vec{j}\cdot d \vec{A} }_{ i_{enc} } + \mu_{0}{\color{cornflowerblue}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }}
$$
#### Differential Form:
$$
\oint\vec{B}\cdot d\vec{l} = \mu_{0} \iint\vec{j}\cdot d\vec{A} + \mu_{0} \epsilon_{0} \frac{d}{dt} \iint\vec{E}\cdot d\vec{A}
$$
By [[Stoke's Theorem]]:
$$
\iint(\vec{\nabla} \times \vec{B})\cdot d\vec{A} = \iint\left( \mu_{0} \vec{j} + \mu_{0}\epsilon_{0} \frac{ \partial \vec{E} }{ \partial t } \right) \cdot d\vec{A}
$$
$$
\implies \underline{\vec{\nabla} \times \vec{B} = \mu_{0}\vec{j} + \mu_{0}\epsilon_{0} \frac{ {\partial} \vec{E} }{ \partial t } }
$$
**Implication 1**:
$$
\vec{\nabla}\cdot \left[ \vec{\nabla}\times \vec{B} = \mu_{0}\vec{j} + \mu_{0}\epsilon_{0} \frac{ \vec{\partial}E }{ \partial t }  \right] 
$$
$$
 = \vec{\nabla}\cdot (\vec{\nabla}\times \vec{B}) = \mu_{0}\left( \vec{\nabla}\cdot \vec{j} \right)  + \mu_{0}\epsilon_{0} \frac{ \partial }{ \partial t }(\vec{\nabla}\cdot \vec{E}) 
$$
$$
\implies 0 = \mu_{0}(\vec{\nabla}\cdot \vec{j}) + \mu_{0}\epsilon_{0}\frac{ \partial  }{ \partial t }\left( \frac{\rho}{\epsilon_{0}} \right) 
$$
$$
\implies \vec{\nabla}\cdot \vec{j} = -\frac{ \partial \rho }{ \partial t } 
$$

**Continuity Equation for Charge**:
For an arbitrary shape
$$
\iint(\vec{\nabla}\cdot \vec{j})dV = -\frac{ \partial  }{ \partial t } \underset{ \text{shape} }{ \iiint }\rho dV
$$
By [[Divergence Theorem]]:
$$
\underset{ \text{surface} }{ {\subset\!\supset} \mathllap{\iint} } \vec{j}\cdot d\vec{A} = -\frac{ \partial Q_{tot} }{ \partial t } 
$$

i.e. charge conservation equation (charged shape, losing charge)

**Implication 2**:
$$
\begin{matrix*}[l]
\vec{\nabla}\cdot \vec{E} = 0  \\
\vec{\nabla}\cdot \vec{B} = 0 \\
\vec{\nabla}\times\left[\vec{\nabla}\times \vec{E} = -\frac{ \partial \vec{B} }{ \partial t }\right] \\
\vec{\nabla}\times \vec{B} = \mu_{0}\epsilon_{0} \frac{ \partial \vec{E} }{ \partial t } 
\end{matrix*}
$$

$$
\vec{\nabla}\times(\vec{\nabla}{ \times \vec{E} }) = -\frac{ \partial }{ \partial t } (\vec{\nabla}\times \vec{B})
$$
$$
\cancelto{ 0 }{ \vec{\nabla}(\vec{\nabla}\cdot \vec{E}) }-\nabla^{2}\vec{E} = -\frac{ \partial  }{ \partial t }\mu_{0}\epsilon_{0} \frac{ \partial \vec{E} }{ \partial t }   
$$
$$
\implies \nabla^{2}\vec{E} = \mu_{0}\epsilon_{0} \frac{ \partial^{2}  \vec{E} }{ \partial t^{2}  }  
$$
([[Conductor#Laplacian|Laplacian]])
For vertically oriented $\vec{E}$
$$
\nabla^{2} E_{y} = \mu_{0}\epsilon_{0} \frac{ \partial^{2}  E_{y} }{ \partial^{2}  t }  \implies \frac{ \partial^{2}  E_{y} }{ \partial x^{2}  }  = \mu_{0}\epsilon_{0} \frac{ \partial^{2}  E_{y} }{ \partial t^{2}  } 
$$
i.e. equation for wave motion. Recall:
$$
\frac{ \partial^{2}  y }{ \partial x^{2}  }  = \frac{1}{v^{2} } \frac{ \partial^{2}  y }{ \partial t^{2}  } 
$$
$$
v = \frac{1}{\sqrt{ \mu_{0}\epsilon_{0} }} = c = 2.99 \times 10^{8}\;  \mathrm{m/s}
$$








$$
\begin{matrix*}[l]
\text{red} & {\color{red}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{green}  & {\color{green}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{blue}  & {\color{blue}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{cyan}  & {\color{cyan}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{magenta}  & {\color{magenta}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{yellow}  & {\color{yellow}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{black}  & {\color{black}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{gray}  & {\color{gray}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{darkgray}  & {\color{darkgray}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }} \\
\text{lightgray}  & {\color{lightgray}\underbrace{ \epsilon_{0} \frac{d}{dt} \iint \vec{E}\cdot d\vec{A} }_{ i_{D} }}
\end{matrix*}


$$