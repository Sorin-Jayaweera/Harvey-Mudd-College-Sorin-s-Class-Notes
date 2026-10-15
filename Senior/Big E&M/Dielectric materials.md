

We can take a material and scatter charges. We build up tiny dipole moments randomly, dependent on the charge distribution of atoms that make up the material. 

Lets focus only on statics (not considering lattice and stat mech stuff). 

We can place free charges outside of the material, making an electric field that goes around / inside the material, which is different from what would form from the free charges we placed. We already studied conductors - boxes of gasses of valence electrons that are free to move and rearrange to make $\phi=0$ inside.  We will see that the case of conductors is a special limit of the general solution that we will now work on. 

![[Pasted image 20261015094519.png]]

We have charges that make dipole moments with some polarity as horrific sums ($10^{23}$ particles)

$$
\begin{align}
\rho(x) = \sum_{i}^{} q_{i} \delta^{3}(x-x_{i}) \\
\vec{p}(x) = \sum_{i}^{} \vec{p}_{i} \delta^{3}(x-x _{i})
\end{align}
$$

Lets make the approximation where the leading monopole and dipole solutions of the Taylor expansion is sufficient. We have field from charges, and the field from net zero charge but with $+q$ and $-q$ separated a little bit.  

$$
\begin{align}
\phi = \sum_{i}^{} \frac{q_{i}}{\left| x- x_{i} \right| } + \underbrace{ \sum_{i}^{} \vec{p}_{i} \cdot \vec{\nabla}\left(  \frac{1}{\left| x-x _{i} \right| } \right) }_{ \phi \text{ from dipoles } }
\end{align}
$$
This is the sum over the dipoles. We had a $-$ something, but we would get a minus sign for another reason and ended up with a $+$. It was $-\vec{p}\cdot \vec{E}_{ext}$. 

The $\phi$ from a general dipole is $\frac{\vec{p}\cdot(\vec{x}-\vec{x}_{0})}{\left| \vec{x}-\vec{x}_{0} \right|^{3}}$ where $\vec{x}_{0}$ is the location of a dipole. 

$$
\begin{align}
\vec{E} & =-\vec{\nabla}\phi \\
\end{align}
$$
Lets do a progressive series of approximations - simplifying with an averaging scheme in a continuum instead of discretely $10^{23}$ particles. 

We have
$$
\begin{align}
\vec{E}=-\vec{\nabla} \int \frac{\overbrace{ \rho(x')_{\text{ mol }} dV' }^{ dq_{i} }}{\left| x-x' \right| } - \vec{\nabla} \int dV' \underbrace{ \vec{P}_{\text{ mol }}  }_{ \text{ dipole per unit volume } }(x') \cdot \vec{\nabla}'\left(  \frac{1}{\left| x-x' \right| } \right)
\end{align}
$$
where $\rho$ is the charge distribution/density of the material, and $\vec{P}$ which is dipole moment per unit volume of the material. 

We want to think of the electric field as the total thing due to all charges (molecular and the free charges that we add externally)/. We should remove the $mol$ subscript.

Lets imagine we have a material with many molecules that are being acocunted for, but which are discrete. Our continuum was really is a sum over delta functions. Except delta functions don't exist in real life - we don't have point charges. They take up some finite space. Instead of discontinuous discrete functions, lets think of this as semi microscopic cells (imagine 100 or 10000 $\AA$). 

We can find the field for each cell as
$$
\begin{align}
\left< \vec{E}(x) \right>  & \equiv \frac{1}{V_{\text{ cell }} } \int_{\text{ cell }} \vec{E}(x+x')d^{3}x' \\
\left< \rho(x) \right>  & \equiv  \frac{1}{V_{\text{ cell }} } \int_{\text{ cell }} \rho(x+x')d^{3}x' \\
\left< P(x) \right>  & \equiv  \frac{1}{V_{\text{ cell }} } \int_{\text{ cell }} P(x+x')d^{3}x'
\end{align}
$$

We can now fix the equation we had written earlier - we have to bracket everything (introducing another integral over the cell). It is a linear equation, so we can do it over all three terms and not really care. 

Lets relabel this average $\left< \vec{E}(x) \right>$ as a smooth function $\vec{E}(x)$, which is the average. 


$$
\begin{align}
\left< \vec{E} \right>  & =-\vec{\nabla} \int \frac{\overbrace{ \left< \rho(x') \right> _{\text{ mol }} dV' }^{ dq_{i} }}{\left| x-x' \right| } - \vec{\nabla} \int dV' \underbrace{ \left< \vec{P} \right> _{\text{ mol }}  }_{ \text{ dipole per unit volume } }(x') \cdot \vec{\nabla}'\left(  \frac{1}{\left| x-x' \right| } \right)
\end{align}
$$


Lets just relabel these averages but without the average symbol that would be tedious. We understand that we're talking about averages now.

Also, $\rho_{\text{ mol }}= \rho(x)+ \rho_{\text{ free }}(x)$


$$
\begin{align}
\vec{E}(x)   = &  -\vec{\nabla} \int \frac{\rho(x')+\rho_{\text{ free }} }{\left| x-x' \right| }dV' \\
 & -\vec{\nabla} \int dV' \vec{P}(x') \cdot \vec{\nabla} \left( \frac{1}{\left| x-x' \right| } \right)
\end{align}
$$
We can totally get rid of any $\delta$ function messiness that we have thought about. 


Lets compute the divergence of $\vec{E}$. 

$$
\begin{align}
\vec{\nabla}\cdot \vec{E} = -\nabla^{2} \int \frac{\rho(x')+\rho_{f}(x')}{\left| x-x' \right| } dV' - \vec{\nabla}^{2} \int dv' \vec{P}(x')\cdot \nabla'\left(  \frac{1}{\left| x-x' \right| }  \right)
\end{align}
$$

The gradient of $\frac{1}{r}$ is a delta function. Psych! 
$$
\begin{align}
= + 4\pi \int (\rho(x')+\rho_{f} (x'))\delta^{3}(x-x')dV' + 4\pi \int dV' \vec{P}(x')\cdot \vec{\nabla}' \underbrace{ (\delta^{3}(x-x')) }_{ -\vec{\nabla} \delta^{3}(x-x') } 
\end{align}
$$
This later term becomes
$$
\begin{align}
-4\pi \vec{\nabla} \int dV' \vec{P}(x')\delta^{3}(x-x')
\end{align}
$$
We could pull out the derivative from the integral by recognizing $\delta^{3}$ is just a function of the difference $x-x'$, and chain rule something something.

$$
\begin{align}
= 4\pi \rho(x) + 4\pi \rho_{f} (x) - 4\pi \vec{\nabla}\cdot \vec{P}(x)
\end{align}
$$
If we take a neutral material, we'll strike out $\rho(x)$ and just consider the dipole moments in the material. 

Lets define the divergence of the polarization of the material as a new variable (just a name)
$$
\begin{align}
-\rho_{b} (x) = \vec{\nabla} \cdot \vec{P}(x)
\end{align}
$$
We get (in the absence of charges in the material) is
$$
\begin{align}
\vec{\nabla}\cdot \vec{E}=4\pi \rho_{f} + 4\pi \rho_{b} 
\end{align}
$$

To be funky silly, 
$$
\begin{align}
\vec{\nabla}\cdot \vec{E} = 4\pi \rho
\end{align}
$$

$$
\begin{align}
\vec{\nabla}_{0} (\vec{E}+ 4\pi \vec{\rho}) = 4\pi \rho_{f} \\
[\vec{D}= \vec{E}+4\pi \vec{P}] \\
\vec{E}: \text{ total }E-\text{ field from everything} \\
\vec{P}: \text{ Polarization }    \\
\vec{D}: \text{ displacement field} \\
\vec{\nabla}\cdot \vec{D}= 4\pi \rho_{f} 
\end{align}
$$
Assuming someone hands us the $\vec{P}$, the field of dipole moment of a material, we can talk about 
$$
\begin{align}
\vec{\nabla}\cdot \vec{D} - 4\pi \rho_{f}  \\
\vec{D} = \vec{E} + 4\pi \vec{P}
\end{align}
$$

The polarization vector field is a contribution to the field from the material, and we are just labeling a new variable $\vec{D}=\vec{E}+4\pi \vec{P}$. The only new thing we really defined is this $\vec{P}(x)$. 

A materials polarization (how the dipoles in the material) depends on the structure of the material. We are only a bit more complicated, because we have external fields - and we might force the dipoles to align with the external field, changing the configuration of the $\vec{P}(x)$ in the material. This $\vec{P}(x)$ vector field is usually zero, but when we add in free charges to impose an electric field, we will get a non zero $\vec{P}(x)$. 


If we have a total electric field $\vec{E}$ (including the material), we generate a Polarization
$$
\begin{align}
\vec{P} = \overbrace{ \chi_{e} }^{ \text{ electrical susceptability } }
\end{align}
$$
This $\chi_{e}$ depends on the temperature of the material, and we summon the beast of statistical mechanics. 

We are able to say that all these different complexities - lattice spacing, structure (cubic, hexagonal), how much charge, etc - and distill all of it to a single scaler parameter (experimentally derived) $\chi_{e}$ which is specific to a material, and now we can find $\vec{P}$ or $\vec{E}$ for a scenario. 

All electrostatic material properties are carried in $\chi_{e}$. this works because of a deep principle - ***Renormalization***.  This was a noble prize winning thing. We can think about laws of physics as organized by length scale. The theory at the millimeter level can be described by the same Angstrom theory, but packaging and averaging the things from that smaller scale. 

This $\chi_{e}$ is just a packaging of a lot of parameters into a single variable. Detail shmetails. 

We can have a more sophisticated description if we want - 
$$
\begin{align}
P^{i} = a_{ij}E^{j}+ b_{ijk} E^{j}E^{k}+ \dots
\end{align}
$$
This $\chi$ only special case is saying $b_{i j k}=0$ and $a_{ij}=\chi_{e}\delta _{ij}$.

Lets go back to the displacement thing. We can write
$$
\begin{align}
\vec{D}  & = \vec{E} + 4\pi \vec{P} \\
 & = \vec{E} + 4\pi \chi_{e} \vec{E} \\
 & = \vec{E} (1+ r\pi \chi_{e} )
\end{align}
$$
Lets call this promiscuity, we like it more than perduity or persividity or whatever random thing Sahakian said. 
$$
\begin{align}
\epsilon= 1+r\pi \chi_{e}  &  & \text{ permittivity } 
\end{align}
$$

$$
\begin{align}
\vec{D} = \epsilon \vec{E} \\
\vec{\nabla}\cdot \vec{D} =\epsilon \vec{\nabla}\cdot \vec{E} = \epsilon4\pi \rho = 4\pi \rho_{f} 
\end{align}
$$
Therefore,
$$
\begin{align}
\vec{\nabla}\cdot \vec{E} = \frac{4\pi \rho_{f} }{\epsilon}
\end{align}
$$

Woah. Heh. Nice. 


Lets solve actual problems with dielectrics. Take every maxwell's equation, and write boundary conditions. 

Boundary Condition consistency:

Imagine a boundary, with a normal vector from $1\to 2$. We dray tiny gaussian surfaces, gauss's law, yadda yadda. 
![[20261015_103707.jpg]]
$$
\begin{align}
\vec{\nabla}\cdot \vec{D} = 4\pi \rho_{f}  \\
\hat{n} \cdot (\vec{D}_{2} -\vec{D}_{1} ) = 4\pi\sigma_{f}  \\
\vec{\nabla}\cdot \vec{E} = 0 \\
(\vec{E}_{2} -\vec{E}_{1} )\times \hat{n} = 0
\end{align}
$$

We can write
$$
\begin{align}
\hat{n}\cdot (\vec{P}_{2} -\vec{P}_{1} )= -\sigma_{b} 
\end{align}
$$
This is the something something (maybe charge) polarization at the boundary. 



Lets do a real problem.

Lets take an infinite plane, with the $z$ axis. We have a dielectric above and below $z=0$, with $\epsilon_{1}$ above and $\epsilon_{2}$ below. (two different dielectric permittivities). Lets place a free charge $q$. What is $\vec{E}$ everywhere? The field is both due to the polarization of the materials, and the $q$. 

![[Pasted image 20261015104206.png]]


Lets solve the Laplace equation.

$$
\begin{align}
\vec{\nabla} \cdot \vec{E} = \frac{4\pi \rho_{f} }{\epsilon} \\
\vec{E} = -\vec{\nabla} \phi \\
\vec{\nabla}^{2}\phi = \frac{-4\pi \rho_{f} }{\epsilon}
\end{align}
$$
This is the Poisson equation that we will be solving. 

$$
\begin{align}
\vec{\nabla}^{2} \phi_{1,2} = \frac{- 4\pi q \delta(z-d) \delta(x)\delta(y)}{\epsilon_{1,2} }
\end{align}
$$
Where the equation is for $\phi_{1}$ using $\epsilon_{1}$, or $\phi_{2}$ using $\epsilon_{2}$. And now.... Method of images!

Region 1; We want a point that is above the $z$ axis a distance $R_{1}$ from the charge. We put a charge $q'$ below the $z$ axis a distance $R_{2}$ away. ![[Pasted image 20261015104556.png]]

We have
$$
\begin{align}
\phi_{1} = \frac{q}{\epsilon_{1}R_{1}} + \frac{q'}{\epsilon_{1}R_{2}}
\end{align}
$$

For region 2, lets put a charge $q''$ in region 1, above $z=0$. 

We have two unknowns - an ansatz for $\phi_{1}$ and $\phi_{2}$, and this $q''$. We can get the thing we want from the boundary conditions. 
$$
\begin{align}
\frac{q''}{\epsilon_{2}R_{1}} 
\end{align}
$$

The boundary conditions are coming from 
$$
\begin{align}
\hat{n} \cdot (\vec{D}_{2} -\vec{D}_{1})= 4\pi\sigma_{f} 
\end{align}
$$

We ensure that the tangential field is continuous - that is one equation. We also ensure the discontinuity of the normal part of the electric field conforms with what we had from the boundary condition consistency. 

The equations come from
$$
\begin{align}
1 & : & &   \hat{n}\cdot (\vec{D}_{2} -\vec{D}_{1} )=4\pi\sigma_{f} \\
2 & :  & &  (\vec{E}_{2} -\vec{E}_{1}) \times \hat{n} = 0 
\end{align}
$$



