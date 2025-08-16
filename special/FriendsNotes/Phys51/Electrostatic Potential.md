---
tags:
  - Phys51
---

##  Electrostatic Potential
 > [!note]+ Definition 
 > Electrostatic potential energy
 > $$
U_{E}(b)-U_{E}(A) = \int _{a}^{b}\vec{F}_{E}\cdot   d\vec{s} $$
is a [[Conservative Forces|conservative force]], $\vec{F}_{E} = -\vec{\nabla}U_{E}$, where $$
U(r) = \frac{q_{0}q}{4\pi\epsilon_{0}r},$$
and $U(\infty)=0$.
> The ***electrostatic potential*** is given by $$
V = \frac{U_{E}}{q_{0}}$$
> like $\vec{E}=\frac{\vec{F}_{E}}{q_{0}}$.
> $$
V(b)-V(a) = -\int _{a}^{b}\vec{E}\cdot d\vec{s},\quad \vec{E} = -\vec{\nabla}V 
$$

$\vec{V}(x,y,z) \overset{\vec{E}=-\vec{\nabla}V}\longleftrightarrow \vec{E}(x,y,z)$
Potential is *constant* throughout a [[Conductor]].

#### Review: [[gravity|Gravitational Potential Energy]] 
$\vec{F}=m\vec{g}$       $U_{g}=mgz$
![[Pasted image 20240912094233.png]]
$$
W = \int _{a}^{b} -\vec{F}_{g}\cdot d\vec{s}
$$
$$
=\int_{a}^{b} - mg(-\hat{z})\cdot (dx\hat{x}+dy\hat{y}+dz\hat{z})   = \int_{a}^{b}mg\,dz  
$$
$$
=mgz\big\vert_{a}^{b} = mgb-mga\implies  \underline{-\int _{a }^{b} \vec{F}_{g}\cdot d\vec{s}  = U_{g}(b)-U_{g}(a)}
$$

$\vec{F}_{g}$ is a conservative force: 
- Path-independent [[work]]
- No work for closed path
- $\vec{F}_{g}=-\vec{\nabla} U_{g}$


#### Review: [[Del Operator]]
$$
\text{Cartesian} = \left\{\begin{matrix*}[l]
\vec{\nabla} = \hat{x} \frac{ \partial  }{ \partial x } +\hat{y} \frac{ \partial  }{ \partial y  } + \hat{z}\frac{ \partial  }{ \partial z }   \\
d\vec{s} = dx\,\hat{x} + dy\, \hat{y} + dz\,\hat{z}
\end{matrix*}\right.
$$
$$
\text{Spherical} = \left\{\begin{matrix*}[l]
\vec{\nabla} = \hat{r} \frac{ \partial  }{ \partial x } +\hat{\theta} \frac{1}{r}\frac{ \partial  }{ \partial \theta  } + \hat{\phi} \frac{1}{r\sin\theta}\frac{ \partial  }{ \partial \phi }   \\
d\vec{s} = dr\,\hat{r} + rd\theta\, \hat{\theta} + r\sin\theta d\phi\,\hat{\phi}
\end{matrix*}\right.
$$



### Ex: One-point System

![[Pasted image 20240912095427.png]]
$\vec{F}=\frac{q_{0}q}{4\pi\epsilon_{0}r^{2}}\hat{r}$
[[Work]] done by external agent: $\int _{a}^{b}-\vec{F}_{E}\cdot d\vec{s}$
$$
\int _{a}^{b}-\vec{F}_{E}\cdot d\vec{s} = \int \frac{-q_{0}q}{4\pi\epsilon_{0}r^{2}}\hat{r} \cdot (dr \hat{r} + r d\theta\hat{\theta} + r\sin\theta d\phi \hat{\phi}) 
$$


$$
=\frac{-q_{0}q}{4\pi\epsilon_{0}}\int _{a }^{b} \frac{1}{r^{2} }dr  = \frac{-q_{0}q}{4\pi\epsilon_{0}} \left[ - \frac{1}{r} \right]_{a}^{b}  = \frac{q_{0}q}{4\pi\epsilon_{0}} \left( \frac{1}{b}-\frac{1}{a} \right) 
$$
$$
=\underbrace{ \frac{q_{0}q}{4\pi\epsilon_{0}b}B }_{ U_{e}(b) }-\underbrace{ \frac{q_{0}q}{4\pi\epsilon_{0}a} }_{ U_{E}(a) }
$$



Depends only on the radial component of the ending and starting points (i.e. independent of the path taken).


For a point charge:
$$
V(r) = \frac{q}{4\pi\epsilon_{0}r}
$$

### Ex: Multiple Charge System
![[Pasted image 20240912101537.png]]
$q_{1}$ is free
$q_{2}$ requires work: $$\displaystyle\int -\frac{q_{1}q_{2}}{4\pi\epsilon_{0}r^{2}}\cdot(dr \hat{r}+ r d\theta\hat{\theta}+r\sin\theta d\phi \hat{\phi})$$ $$
-\frac{q_{1}q_{2}}{4\pi\epsilon_{0}} \int _{\infty}^{r_{12}} \frac{dr}{r^{2} } = \frac{q_{1}q_{2}}{4\pi\epsilon_{0}} \frac{1}{r_{12}}
$$$q_{3}$ requires work:
$$
-\int (\vec{F}_{E_{13}}-\vec{F}_{E_{23}}) d\vec{s} 
$$
$$
 = -\int \frac{q_{1}q_{3}}{4\pi\epsilon_{0}r^{2} }\hat{r}-\int \frac{q_{2}q_{3}}{4\pi\epsilon_{0}r^{2} }\hat{r}  = -\frac{q_{1}q_{3}}{4\pi\epsilon_{0}}\int_{\infty}^{r_{13}}  \frac{dr}{r^{2} } -  \frac{q_{2}q_{3}}{4\pi\epsilon_{0}}\int_{\infty}^{r_{23}}  \frac{dr}{r^{2} }
 $$
 $$
=\frac{q_{1}q_{3}}{4\pi\epsilon_{0}r_{13}} + \frac{q_{2}q_{3}}{4\pi\epsilon_{0}r_{23}}
$$


**Total Potential Energy of System:**
$$
\frac{q_{1}q_{2}}{4\pi\epsilon_{0}r_{12}}+\frac{q_{1}q_{3}}{4\pi\epsilon_{0}r_{13}} + \frac{q_{2}q_{3}}{4\pi\epsilon_{0}r_{23}}
$$
(sum of energies between points)



### Closed Loop
If $$
\int _{a}^{b}-\vec{E}\cdot   d\vec{s} = V(b)-V(a),
$$
then for a closed loop where $a=b$,
$$
\oint \vec{E}\cdot d\vec{s} = 0 \iff \vec{E} = -\vec{\nabla}V
$$
([[Maxwell's Equations]])



### Example: Uniform Ring of Charge
![[Pasted image 20240912104406.png]]
$$dV = \frac{dq}{4\pi\epsilon_{0}\mathcal{R}}
$$
$$V(z) = \int_{ring} \frac{dq}{4\pi\epsilon_{0}\mathcal{R} } = \frac{1}{4\pi\epsilon_{0}\mathcal{R} } \int  dq = \frac{Q}{4\pi\epsilon_{0}\sqrt{ R^{2}+z^{2}   } } 
$$
$$
\vec{E}(z) = -\vec{\nabla}V = -\left(\hat{x} \frac{ \partial }{ \partial x } +\hat{y} \frac{ \partial  }{ \partial y } + \hat{z} \frac{ \partial }{ \partial z }   \right) \frac{Q}{4\pi\epsilon_{0}\sqrt{ R^{2}+z^{2}   } } 
$$
$$
 = -\hat{z} \frac{ \partial }{ \partial z } \left( \frac{Q}{4\pi\epsilon_{0}\sqrt{ R^{2}+z^{2}   } }  \right)\hat{z}  = -\frac{Q}{4\pi\epsilon_{0}} \frac{ \partial  }{ \partial z } \left( (R^{2}+z^{2}  )^{-1/2}  \right)  \hat{z}
$$
$$
\vec{E}(z) = \frac{-Qz}{4\pi \epsilon_{0}(R^{2}+z^{2}  )^{3/2} }\hat{z}
$$



**Ex:** A charged conducting sphere
![[Pasted image 20240917094906.png]]
**Finding electric field:**
Spherical symmetry $\implies \vec{E}= E(r)\hat{r}$
For $r<R$:
$$
{\subset\!\supset} \mathllap{\iint} \vec{E}\cdot d\vec{A} = {\subset\!\supset} \mathllap{\iint} \cancelto{ 0 }{ E(r) }dA\implies \vec{E}=0
$$
For $r>R$:
$$
{\subset\!\supset} \mathllap{\iint} \vec{E}\cdot d\vec{A} = E(r){\subset\!\supset} \mathllap{\iint}dA = E(r)4\pi r^{2} 
$$
$$
\frac{q_{enc}}{\epsilon_{0}} = \frac{Q}{\epsilon_{0}}
$$
$$
\implies \vec{E} = \frac{Q}{4\pi\epsilon_{0} r^{2} }\hat{r}
$$

**Finding potential**
For $r<R$:
$$
V(b)-V(a) = -\int _{a}^{b} \vec{E}\cdot d\vec{s} 
$$
$$
V(r)-V(\infty)= -\int _{\infty}^{r} \vec{E}\cdot d\vec{s}
$$
$$
V(r) = \int _{r}^{\infty}\vec{E}\cdot d\vec{s} = \int _{0}^{R}\vec{0}\cdot d\vec{s} + \int_{R}^{\infty} \frac{Q}{4\pi\epsilon_{0}r^{2} }\underbrace{ \hat{r}\cdot d\vec{s} }_{ dr } = \frac{Q}{4\pi\epsilon_{0}R}
$$
For $r>R$:
$$
V(r)-V(\infty) = -\int _{\infty}^{r}\vec{E}\cdot d\vec{s}
$$
$$
V(r) = \int _{0}^{\infty}\vec{E}\cdot d\vec{s} = \int _{r}^{\infty} \frac{Q}{4\pi\epsilon_{0}r^{2}}dr = \frac{Q}{4\pi \epsilon_{0}r}  
$$



$$
V(r) = \left\{\begin{matrix*}[l]
\frac{Q}{4\pi\epsilon_{0}r} & r>R \\
\frac{Q}{4\pi\epsilon_{0}R} & r<R
\end{matrix*}\right.
$$
![[Pasted image 20240917100603.png]]



Since a [[Conductor]] is an [[Equipotential Surface]], we can visualize where the field (and charge) is more or less intense. The equipotential surfaces mimic the shape of the conductor, and field lines are always perpendicular to the equipotential surface.




