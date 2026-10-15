

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

