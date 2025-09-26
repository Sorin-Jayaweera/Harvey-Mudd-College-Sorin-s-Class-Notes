---
tags:
  - Phys51
---

One of [[Maxwell's Equations]].
# Electric Form
## Integral Form
$$
\Phi_{E}=\underbrace{ {\subset\!\supset} \mathllap{\iint}\vec{E}\cdot d\vec{A} }_{ \text{LHS} } = \underbrace{ \frac{q_{enclosed}}{\epsilon_{0}} }_{ \text{RHS} }
$$
LHS: the [[Flux]] of the [[special/FriendsNotes/Phys51/Electric Field]] out through a closed surface
$$
=
$$
RHS: the [[Charge]] enclosed in the surface, $q_{enc}$, div. by $\epsilon_{0}$.


**Ex 1:**
$\vec{E}$ of a point charge through sphere:
![[Pasted image 20240903100214.png]]
**Ex 2:**
Through an arbitrary shape:
![[Pasted image 20240903101117.png]]
$d\Phi_{1}=\vec{E}(r_{1})\cdot d\vec{A}_{1}=\frac{q}{4\pi\epsilon_{0}r_{1}^{2}}dA_{1}$
$d\Phi_{2}-\vec{E}(r_{2})\cdot d\vec{A}_{2}=\frac{q}{4\pi\epsilon_{0}r_{2}^{2}}dA_{2}\cos\theta$
Ratio: $\frac{d\Phi_{2}}{d\Phi_{1}} = \frac{dA_{2}\cos\theta r_{1}^{2}}{dA_{1}r_{2}^{2}} = \frac{\cancel{ r_{2}^{2} }}{\cancel{ r_{1}^{2} }} \frac{1}{\cancel{ \cos\theta }}\cancel{ \cos\theta } \frac{\cancel{ r_{1}^{2} }}{\cancel{ r_{2}^{2} }}=1$
Same flux


**Ex:** Two infinite, uniformly charged plates


## Differential Form
$$
\underbrace{ \vec{\nabla}\cdot \vec{E} }_{ \text{LHS} }=\underbrace{ \frac{\rho}{\epsilon_{0}} }_{ \text{RHS} }
$$
Relates how much electric field "sprays out"  from a point (the [[Divergence]]) to the charge density at *that* point.

LHS: [[Divergence]] of $\vec{E}$ at a specific point
RHS: Charge per unit volume at that specific point



#### Divergence Recap
For a generic [[Vector Field]], $\vec{C}$:

**Cartesian:**
$$
\vec{\nabla}\cdot \vec{C}=\frac{ \partial C_{x} }{ \partial x }  + \frac{ \partial C_{y} }{ \partial y } + \frac{ \partial C_{z} }{ \partial z } 
$$
**Cylindrical:**
$$
\vec{\nabla}\cdot \vec{C}=\frac{1}{r}\frac{ \partial }{ \partial r }  (rC_{r})+\frac{1}{r} \frac{ \partial C_{\theta} }{ \partial \theta }  + \frac{ \partial C_{z} }{ \partial z } 
$$
**Spherical:**
$$
\vec{\nabla}\cdot  \vec{C} = \frac{1}{r^{2} } \frac{ \partial}{ \partial r } (r^{2} C_{r}) + \frac{1}{r\sin\theta} \frac{\partial}{\partial\theta}(\sin\theta C_{\theta}) + \frac{1}{r\sin\theta} \frac{\partial C_{\phi}}{\partial\phi} 
$$

$\vec{\nabla}\cdot \vec{C} > 0$: "source"
$\vec{\nabla}\cdot \vec{C} < 0$: "sink

$$
\vec{\nabla}\cdot \vec{C} = \lim_{ \Delta V \to 0 } \frac{1}{\Delta V} \underset{\text{of } \Delta V}{\underset{\text{surface}}{{\subset\!\supset} \mathllap{\iint}}} \vec{C}\cdot d\vec{A}
$$



**Ex 1:** Uniform sphere of charge, radius $R$
Known:
$$
\vec{E}=\left\{\begin{matrix*}[l]
\frac{Qr}{4\pi\epsilon_{0}R^{3}}\hat{r} & r\leq R \\
\frac{Q}{4\pi\epsilon_{0}r^{2} }\hat{r}
 & r \geq R\end{matrix*}\right.
$$
Inside point:
$$
\rho=\frac{Q}{\frac{4}{3}\pi R^{3} }
$$
$$
\vec{\nabla}\cdot \vec{E} = \frac{1}{r^{2} }\frac{ \partial  }{ \partial r }\left(r^{2} \frac{Qr}{4\pi\epsilon_{0}R^{3}}\right)  = \frac{Q}{4\pi\epsilon_{0}R^{3}} \frac{1}{r^{2} } \frac{ \partial  }{ \partial r } (r^{3} ) = \frac{3Q}{4\pi \epsilon_{0}R^{3} } = \frac{\rho}{\epsilon_{0}}
$$

Outside point:
$$
\rho=0
$$
$$
\vec{\nabla}\cdot \vec{E} = \frac{1}{r^{2} } \frac{ \partial }{ \partial r } \cancelto{ 0 }{ \left( \cancel{ r^{2} } \frac{Q}{4\pi\epsilon_{0}\cancel{ r^{2} } }\right) } = 0 = \frac{\rho}{\epsilon_{0}}
$$



## Form Equivalence
Are the two forms really equivalent?

[[Divergence Theorem]]:

$$
{\subset\!\supset} \mathllap{\iint}_{\partial W}\vec{F}\cdot \vec{n}\,dS = \iiint_{W}\text{div}\vec{F}\,dV
$$
$$
{\subset\!\supset} \mathllap{\iint}\vec{C}\cdot d\vec{A} = \iiint \left( \vec{\nabla}\cdot \vec{C} \right)dV 
$$


$$
\underset{\text{vol enc}}{\iiint}  (\vec{\nabla}\cdot \vec{E})dV = \frac{q_{enc}}{\epsilon_{0}} = \frac{1}{\epsilon_{0}}\underset{\text{same surface}}{\underset{\text{vol enc by }}{\iiint}} \rho dV
$$
$$
\underset{\text{chosen surface}}{\underset{\text{ randomly}}{\underset{\text{vol enc by}}{\iiint}}} (\vec{\nabla}\cdot  \vec{E})dV = \underset{\text{same volume}}{\iiint} \frac{\rho}{\epsilon_{0}}dV
$$

Since this holds for *any* surface, the integrals are equal
$$
\implies \vec{\nabla}\cdot \vec{E} = \frac{\rho}{\epsilon_{0}}.
$$




# Magnetic Form

$$
{\subset\!\supset} \mathllap{\iint} \vec{B}\cdot d\vec{A}=0 \iff \nabla\cdot \vec{B}=0
$$
([[Maxwell's Equations]])

No magnetic "point charges" (monopoles).