This will be mostly linear algebra. 

QM is not just a way of asking where particles are  - its an operating system: Polarization of light, Solid State phonons, particle physics, String theory etc - anywhere that you are quantizing. They all work on the framework of quantization and probability.  

We have the bad view: imagine an electron as a ball of spinning charge. Rotating CCW viewed from above, it has $L$ pointing up. This looks like a magnetic dipole bar magnet with North going down (because the charge moving is negative, instead of North pointing up (positive charge), it points down). 

Think about the North pole as a positive charge in an electric field. If we put it in a uniform magnetic field, it points along the direction of the field (no torque). If the uniform were perpendicular to the magnet, there would be no net force but yes torque - it would rotate to align with the field, but not translate. 

The Stein Gerlach has a nonuniform field, where the lines are denser at the north side and less dense on the south side. A magnet with north to north would have a stronger push towards the south end, and has net force up. 
![[Pasted image 20260121111713.png]]

## Stern Gerlach 

We have a thing that shoots out silver atoms through a collimator (makes them all roughly in a straight line).
Silver is $Ag=[Kr]4d^{10}5s^{1}$ - it has a single unpaired electron that determines the charge. If it acts like a spinning ball of charge spitting out of the thermal oven, we should have a whole smear of silver deflecting up, down, not at all, just a little, whatever. However, we only see two discrete blobs of deposition. 

You can work out that this is as if each had angular momentum $\pm\frac{\hbar}{2}$ (units of $\hbar$ are angular momentum).

We write up as $\ket{+\vec{z}}$ or $\ket{\uparrow}$, down as $\ket{-\hat{z}} \text{ or } \ket{\downarrow }$.

$\ket{+\vec{z}}$ acts like a column vector $\begin{pmatrix}a\\b\end{pmatrix}$.
$\bra{+\vec{z}}$ acts like a row vector $(a^{*} \,b^{*})$ (more later why this has to be complex)
$\ket{+\hat{z}}^{\dagger}=\bra{+\vec{z}}$
The inner product between a ket and a bra is a magnitude, $\bra{+z}\ket{+z}$

If a measurement has $100\%$ probability of giving a result, we can assign it a ket.   


## 4 experiments
![[Pasted image 20260121114942.png]]

The information is stored somehow for what it was.

Now the weird thing: If we block one of the paths in the modified SG, we have both $\ket{\pm z}$.
![[Pasted image 20260121115418.png]]

This is reminiscent of light interference.
![[Pasted image 20260121115436.png]]

If we have two slits where we shine light, seeing only one or the other we would have two curves. If both at once, we see interference. There are spots where, with both, we would see nothing - but with just one we see something.

Lets build up a math of inner products:

| Familiar 3d Vectors                                                                                                                                          | Quantum State Vectors                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| (we don't use $\hat{x}$, because its an operator). <br>We use $\vec{i},\vec{k},\vec{k}$.                                                                     |                                                                                                                                              |
| $\vec{i}\cdot \vec{i}=1$ etc<br>$\vec{i}\cdot \vec{j}=0$ etc                                                                                                 | $\bra{+z}\ket{+z}=1$ <br>$\bra{-z}\ket{+z}=0$<br>$\bra{+z}\ket{+x}$ = neither 0 or 1.                                                        |
| $\vec{E}=E_{x}\vec{i} + E_{y}\vec{j}+E_{z}\vec{k}$<br>to extract a component in a vector direction with the inner product,<br>$E_{x}= \vec{i}\cdot \vec{E}$. | $\ket{\psi}=c_{+}\ket{+\hat{z}}+ c_{-}\ket{-z}$.<br>$\bra{+\vec{z}}\ket{\psi}=c_{+}$<br>                                                     |
| $\vec{i},\vec{j},\vec{k}$ form a complete orthonormal basis for 3D vectors                                                                                   | The set $(\ket{+z},\ket{-z})$ form a complete orthonormal basis.                                                                             |
| $\vec{A}\cdot \vec{B} \in \mathbb{R}^{}$.                                                                                                                    | $\bra{\psi}\ket{\phi} \in \mathbb{C}$.                                                                                                       |
|                                                                                                                                                              | $\bra{\psi}\ket{\psi}=1$                                                                                                                     |
|                                                                                                                                                              | $\left\| \bra{\psi}\ket{\phi} \right\|^{2}$ is the probability of finding state $\psi$ given state $\phi$.                                   |
|                                                                                                                                                              | $\bra{+\vec{x}}\ket{+\vec{z}}=\sqrt[]{ \frac{1}{2 } }e^{i\delta}$.<br>$\bra{-\vec{z}}\ket{+\vec{x}}= \sqrt[]{ \frac{1}{2} }e^{i\delta_{-} }$ |

This is a consistent way of describing it that works everywhere. 

