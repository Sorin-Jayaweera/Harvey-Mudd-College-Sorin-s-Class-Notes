Orbital angular momentum 
$$
\begin{align}
\hat{\vec{L}} \ket{x,y,z} 
\end{align}
$$
acting on states of definite positions.

We can see how rotations would act
$$
\begin{align}
\hat{R}(d\phi \vec{k}) \ket{x,y,z} = \ket{x\underbrace{ -yd\phi }_{ dx },y\underbrace{ +xd\phi }_{ dy },z} 
\end{align}
$$

If we have an arbitrary point in xyz, rotating it by a $d\phi$, the components increase/decrease following usual rotation geometry rules.

Lets connect this to the angular momentum operators we've been talking about in general. 
$$
\begin{align}
\left( 1- \frac{i}{\hbar}\hat{L}_{z} d\phi\right) \ket{x,y,z}  & = \hat{T}(dx \mathbf{\vec{i}})\hat{T}(dy \mathbf{\hat{j}})\ket{x,y,z}  \\
 & = \left( 1- \frac{i}{\hbar}\hat{p}_{x} dx \right)\left( 1- \frac{i}{\hbar} \hat{p}_{x} dx \right)\left( 1- \frac{i}{\hbar}\hat{p}_{y} dy \right) \ket{x,y,z}  \\
 & = \left( 1 - \frac{i}{\hbar}(\hat{p}_{x} (-yd\phi)+ \hat{p}_{y} (xd\phi) ) \right) \ket{x,y,z} \\
 & = \left( 1- \frac{i}{\hbar} ( \hat{x} \hat{p}_{y} - \hat{y}\hat{p}_{x}  )d\phi \right) 
\end{align}
$$

If we generate the rotation with an angular momentum, or doing the same effect by translating in x and y, we can match the operators by first order. We get that
$$
\begin{align}
\hat{L}_{z} = \hat{x}\hat{P}_{y} - \hat{y}\hat{P}_{x} 
\end{align}
$$
This was done for the $z$ axis, but we could really have done this for anything. Therefore, we generalize to
$$
\begin{align}
\hat{\vec{L}} = \hat{\vec{r}} \times \hat{\vec{p}}
\end{align}
$$
(this is really secretly three equations, since $\hat{\vec{r}}$ is a vector of all three components $(\hat{x},\hat{y},\hat{z})$)

Angular momentum is really the generator of rotations, and linear momentum should be thought of as the generator of translations. 

If we look at the commutation relationship between
$$
\begin{align}
[\hat{L}_{z} , \hat{\vec{P}}^{2}] = 0
\end{align}
$$
Similarly, 
$$
\begin{align}
[\hat{L}_{z}, \hat{\vec{r}}^{2} ] = 0 \\
\end{align}
$$
The same holds for $\hat{L}_{x}\text{ and } \hat{L}_{y}$.

For the $\hat{H}$ with a central potential $V(\vec{r})$, 
$$
\begin{align}
[\hat{L}_{z} , \hat{H}] = 0
\end{align}
$$
(same for $\hat{L}_{x},\text{ and } \hat{L}_{y}$)

We have conservation of orbital angular momentum
$$
\begin{align}
\hat{L}_{i} \ket{m_{i}}  & = m_{i}\ket{m_{i}}  \\
\ket{\psi(t=0)}  & = \ket{m_{i}}  \\
\ket{\psi(t)}  & = \hat{U}(t)\ket{\psi(0)} \\
\hat{L}_{i} \ket{\psi(t)}  &  = \hat{L}_{i} e^{\frac{-i\hat{H}t}{\hbar}}\ket{\psi(0)} \\
 & = m_{i} \ket{\psi(t)}      
\end{align}
$$
Angular momentum is conserved in a central potential. 

If we put it in a magnetic field in $\hat{z}$ then we wouldn't have a symmetric central potential, we would have procession around $\hat{z}$. We would have conservation of the $\hat{L}_{z}$, but not in $\hat{L}_{x}\text{ or } \hat{L}_{y}$. (Linear momentum is also not necessarily conserved).

For a central potential,
$$
\begin{align}
[\hat{H},\hat{\vec{L}}]= 0 \\
\end{align}
$$
Rotationally symmetry of the $\hat{H}$ implies the conservation of $L_{x},L_{y},L_{z}, \text{ and therefore } L^{2}$

We have a complete set of observables
$$
\begin{align}
[\hat{L}_{x}, \hat{L}_{y} ]= i\hbar \hat{L}_{z}  &  & [\hat{L}^{2},\hat{L}_{z} ]\\
[\hat{L}_{y}, \hat{L}_{z} ]= i\hbar \hat{L}_{x}  &  & [\hat{L}^{2},\hat{L}_{x} ]\\
[\hat{L}_{z}, \hat{L}_{x} ]= i\hbar \hat{L}_{y}  &  & [\hat{L}^{2},\hat{L}_{y} ]\\
\end{align}
$$
Because $\hat{L}^{2}$ commutes with all three of them, we can make simultaneous eigenstates of all of them. 
$$
\boxed{
\boxed{
\boxed{
\boxed{
\boxed{
\boxed{
\boxed{
\boxed{
\begin{align}
\hat{H} \ket{E,l,m}  & = E \ket{E,l,m} \\
\hat{L}^{2} \ket{E,l,m} &  = \hbar^{2}l(l+1)\ket{E,l,m}  \\
\hat{L}_{z} \ket{E,l,m} &  = \hbar m \ket{E,l,m} 
\end{align}
}
}
}
}
}
}
}
}
$$


These are the orbitals that we know and love from chemistry.

In the center of mass frame for a central potential, $\hat{P}\ket{\psi _{cm}}=0\ket{\psi _{cm}}$ . We still have arbitrary relative positions, so $\vec{r}$ is still arbitrary. 

$$
\begin{align}
\hat{H}_{cm} = \frac{\hat{\vec{p}}^{2}}{2\mu}+ v(\left| \vec{r} \right| )  \\
[\hat{r}_{i} , \hat{p}_{j} ]= i\hbar\delta _{ij} \neq  0 \\
[\hat{\vec{r}}^{2}, \hat{\vec{p}}^{2}] \neq  0 \\
[\hat{H},\hat{\vec{p}}^{2}] \neq  0 \\
[\hat{H},\hat{\vec{r}}^{2}]\neq  0
\end{align}
$$
We can't make simultaneous eigenstates with these because the commutators with the Hamiltonian are zero. 

However, if we write 
$$
\begin{align}
\hat{\vec{L}}^{2} & =  (\hat{\vec{r}}\times \hat{\vec{p}})\cdot(\hat{\vec{r}}\times \hat{\vec{p}}) \\
 & = \hat{\vec{r}}^{2} \hat{\vec{p}}^{2} - (\hat{\vec{r}}\cdot \hat{\vec{p}})^{2} + i\hbar \hat{\vec{r}}\cdot \vec{\hat{p}}
\end{align}
$$
$L^{2}$ is the only thing that does commute with the Hamiltonian. Lets write other things in terms of this. 

$$
\begin{align}
\ket{\psi} &  = \ket{E,l,m}  \\
\hat{H}\ket{\psi}  & = E\ket{\psi}  \\
\bra{\vec{r}} \hat{H}\ket{\psi} &  = E \underbrace{ \braket{ \vec{r} | \psi } }_{ \psi(\vec{r})= \psi(x,y,z) } 
\end{align}
$$
We can write this by components
$\hat{\vec{r}}$ is a Hermitian operator, so we can move it around
$$
\begin{align}
\frac{1}{2\mu} \bra{\vec{r}} \hat{\vec{p}}^{2} \ket{\psi} + \bra{\vec{r}} \left| V(\vec{r}) \right| \ket{\psi}  \\
\frac{1}{2\mu} \bra{\vec{r}} \hat{\vec{p}}^{2} \ket{\psi} + V(\left| \vec{r} \right| )\braket{ \vec{r} | \psi } 
\end{align}
$$
$$
\begin{align}
\hat{p}_{x} \to   \frac{\hbar}{i} \frac{ \partial  }{ \partial x } 
\end{align}
$$
So we have
$$
\begin{align}
\bra{\vec{r}} \hat{\vec{p}}^{2} \ket{\psi} = -\hbar^{2} \nabla^{2} \braket{ \vec{r} | \psi } = -\hbar^{2} \nabla^{2} \psi(x,y,z)
\end{align}
$$
But this gives us in cartesian. If we want to get it in terms of $P's$ and $r's$, then we should use $\hat{\vec{L}}^{2}$.

$$
\begin{align}
\bra{\vec{r}} \hat{\vec{L}}^{2} \ket{\psi} = \vec{r}^{2} \bra{\vec{r}}  \hat{\vec{p}}^{2} \ket{\psi} - \bra{\vec{r}} (\hat{\vec{r}}\cdot \hat{\vec{p}})\ket{\psi} + i\hbar \vec{r} \cdot \bra{\vec{r}} \hat{\vec{p}}\ket{\psi} 
\end{align}
$$
Lets try to solve for $\ket{\vec{r}}\hat{\vec{p}}^{2}\ket{\psi}$ in terms of $\ket{\vec{r}}\hat{\vec{L}}^{2}\ket{\psi}$ and the other things on the right (which are maybe a little bit more subtle).

If we were to do this very carefully, we would get 
$$
\begin{align}
-\frac{\hbar^{2}}{2\mu}\left( \frac{ \partial^{2} }{ \partial r^{2} } + \frac{2}{r} \frac{ \partial  }{ \partial r }  \right) \braket{ \vec{r} | \psi } + \frac{\bra{\vec{r}} \hat{\vec{L}}^{2} \ket{\psi} }{2\mu r^{2}} + V(\left| r \right| )\braket{ \vec{r} | \psi } = E\braket{ \vec{r} | \psi } 
\end{align}
$$

If we then write this in terms of the eigenstates from before ($\ket{E,l,m}$), 
$$
\begin{align}
\ket{\psi}  & = \ket{E,l,m} \\
\braket{ \vec{r} | \psi }  & = \braket{ \vec{r} | E,L,m }  \\
\psi(x,y,z) & = \psi_{E,L,M} (r,\theta,\phi)  
\end{align}
$$
$$
\begin{align}
\left[ -\frac{\hbar^{2}}{2\mu}\left(  \frac{ \partial^{2} }{ \partial r^{2} } + \frac{2}{r}\frac{ \partial  }{ \partial r }  \right) + \frac{\hbar^{2}l(l+1)}{2\mu r^{2}}+ V(\left| \vec{r} \right| ) \right] \psi_{elm} (r,\theta,\phi) = E \psi_{Elm} (r,\theta, \phi)
\end{align}
$$


$$
\begin{align}
\left[  \frac{-\hbar^{2}}{2\mu}\frac{ d ^{2}}{d r^{2} } + \underbrace{ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}}+ V(r)  }_{ V_{eff}^{l}(r)  }\right] u(r)= E u(r)
\end{align}
$$
