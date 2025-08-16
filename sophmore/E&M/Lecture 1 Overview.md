Coulomb is the fundamental SI unit of electric charge. Charge is relativistic-ly invariant (the same independent of the reference frame) and quantized (has a minimum smallest amount as the charge of a quark).

One electron has a charge $1.602\times 10^{-19}C$ of charge
but a mole of electrons has $96.5kC$ of charge.

## Coulombs law
The force of gravity follows $\vec{F}_{g} = -G \frac{M_{1}M_{2}}{r^{2}}\hat{r}$
Note the negative sign, which shows that the force is attractive

We have similarly coulomb's law, which states that $\vec{F}_{e}=\frac{1}{4\pi\epsilon_{0}}\frac{q_{1}q_{2}}{r^{2}}\hat{r}$
![[Pasted image 20240826093452.png|100]]
We have $\epsilon_{0}$ is the permittivity constant (permittivity of free space), $\epsilon_{0}=8.85*10^{-12} \frac{C^{2}}{Nm^{2}}$
The direction of the force is determined by the product between $q_{1}\text{ and } q_{2}$.


## Superposition
We can isolate the forces due to separate charges, and sum them. The net force on the test charge is equal to the vector sum of the forces due to the individual charges. 
$\vec{F}=\vec{F}_{1}+\vec{F}_{2}+\dots$

However, it becomes very useful to talk about the electric field, a force per unit charge.
$\vec{E}$ is the force per unit charge. It is the force on a test charge (that we could imagine at a spot) divided by the charge at that spot.
$\vec{E}=\frac{\vec{F}_{\text{ on q }}}{q_{0}}$
![[Pasted image 20240827100052.png|300]]
We take a source point that holds a charge, and consider a point in the field. Assuming (here) that $q$ is positive, the electric field points away from the source charge. We could similarly assume that q is negative, in which case the vectors would all point towards the source charge. 

We commonly represent the electric field with field lines
![[Pasted image 20240827100427.png|300]]

To get from the electric field to the force, preform
$\vec{F}_{\text{ on q }}=q_{0}\vec{E}$.

In the same way that superposition applies to individual forces, we get the same rule for the electric field.
If we have more than one point charge and want to find the total electric field at a point in space, we find the field due to each charge individually and find the vector sum.

$$
\begin{align}
\vec{E}=\vec{E}_{1}+\vec{E}_{2}+\dots
\end{align}
$$
It is worth writing again, coulombs law for a point charge is
$$
\boxed{
\begin{align}
\vec{E} = \frac{1}{4\pi \epsilon_{0}} \frac{q}{r^{2}}\hat{r}
\end{align}
}
$$


Lets put this to practice. Consider a water molecule, and represent it as two point charges.
0
Lets pick a point at a spot on the x axis, and calculate the field at that spot.
![[Pasted image 20240827101357.png|300]]
![[Pasted image 20240827102033.png|300]]
Because the two point charges are the same magnitude and same distance away (in this case), we can each will have the same magnitude but have different signs.
Lets call the distance from the point charge to the test charge $\Gamma=\sqrt{ \frac{d^{2}}{4}+r^{2} }$
$\cos\theta=\frac{d}{2\Gamma}$
$\vec{E}=2 \times \frac{1}{r\pi\epsilon_{0}} \frac{q}{\Gamma^{2}}\cos\theta$
We have now
$$
\begin{align}
\vec{E}=\frac{qd}{4\pi\epsilon_{0}} \frac{1}{(\frac{d^{2}}{4}+r^{2})^{3/2}}(-\hat{y})
\end{align}
$$
$p=qd$ is the "dipole moment".
Node that the field dies away at $\frac{1}{r^{3}}$ (expand the exponent in the denominator), because the two charges are close to each other and look more like a chargeless sphere than a strong point charge.


## Rules for drawing electric field lines:


* Electric field lines point parallel to the direction of the force felt by a  positive test charge 
* Electric field lines start/end on positive/negative charges, or at infinity  
* Electric field lines never intersect  (otherwise we wouldn't know which way a charge is being pushed at the intersection)
* Density of lines indicates strength of electric field  
* Near a point or line charge, electric field lines point radially  outward/inward  
* Near a charged surface, electric field lines point perpendicular to the surface
* **Symmetry of charges is reflected in the symmetry of the field**  
* We only draw field lines in the plane of the page – can draw multiple  perspectives if necessary

## Maxwell's equations
![[Pasted image 20240827094615.png|300]]


## Electrostatic Force: Coulombs Law

## Electric Field Force per unit charge
$$
\begin{align}
\vec{E}=\frac{\vec{F}}{\zeta}=\frac{\zeta}{4\pi\epsilon r^{2}},\vec{E}=\vec{E}_{1}+\vec{E}_{2}+\dots
\end{align}
$$

