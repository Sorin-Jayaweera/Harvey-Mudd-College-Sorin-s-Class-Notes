Lets go off the rails today. 

We'll start with the $H_{op}$ for a central potential $V(r)$
$V(r)= \frac{-e^{2}}{r\pi\epsilon_{0} r}$. This is the coulomb potential. In $E\&M$ we called this $\underbrace{ u }_{ \text{ potential energy } }=\underbrace{ q }_{ \text{ electron } }\underbrace{ \Phi }_{ \text{ electrical potential due to a proton } }$

We write out the $TISE:$ 
$$
\begin{align}
-\frac{\hbar^{2}}{2m} \left( \frac{ \partial^{2} }{ \partial x^{2} } + \frac{ \partial^{2} }{ \partial y^{2} } +\frac{ \partial^{2} }{ \partial z^{2} }  \right) \psi+V(r)\psi=E\psi \\
r=\sqrt[]{x^{2}+y^{2}+z^{2}} 
\end{align}
$$
We have a central force due to the electric potential. $\vec{F}_{\text{ central }}=-\vec{\nabla}V(r)=-\frac{ \partial V(r) }{ \partial r }\hat{r}$.
$$
\begin{align}
\vec{F}_{\text{ central }}  = F(r)\hat{r}, \vec{\tau}_{net} = \frac{ d \vec{L}}{d t }  \\
\vec{\tau}=\vec{r}\times  \vec{F}=0
\end{align}
$$

We're basically just saying that the electric potential exerts no torque if it is acting central to our particle.

Lets try to write our Schrödinger equation in spherical coordinates to make it nicer, and see how it works.
$$
\begin{align}
H_{op} = -\frac{\hbar^{2}}{2mr^{2}} \left[ \frac{ \partial  }{ \partial r } \left( r^{2} \frac{ \partial  }{ \partial r }  \right) + \frac{1}{\sin(\theta) }\frac{ \partial  }{ \partial \theta }  \sin\theta \frac{ \partial  }{ \partial \theta } + \frac{1}{\sin ^{2}\theta}\frac{ \partial^{2} }{ \partial \phi^{2} }  \right] + V_{r}
\end{align}
$$

We have the eigenvalue equation:
$$
\begin{align}
H_{op} \Psi (r,\theta,\phi)= E\Psi (r,\theta,\phi)
\end{align}
$$
We can use separation of variables to take apart the $H_{op}$.
First, lets do a dimensional analysis:
$-\frac{\hbar^{2}}{2mr^{2}}$: $\hbar$ has the same units as angular momentum ($\frac{kgm^{2}}{s^{2}}$), and $mr^{2}$ looks like moment of inertia. 
This looks like
$$
\begin{align}
\sim  \frac{L^{2}}{2I}= \frac{(I\omega)^{2}}{2I}=\frac{1}{2}I\omega^{2}
\end{align}
$$
We have a new operator:
$$
\begin{align}
\vec{L^{2}_{_{op} }} = - \hbar^{2} \left[ \frac{1}{\sin\theta} \frac{ \partial  }{ \partial \theta } \left( \sin\theta \frac{ \partial  }{ \partial \theta }  \right) + \frac{1}{\sin ^{2}\theta}\frac{ \partial^{2} }{ \partial \psi^{2} }  \right] 
\end{align}
$$
We can motivate this by having the classical version $\vec{L}=\vec{r}\times \vec{p}$

![[Pasted image 20250305102625.png|300]]


We can write out spherical coordinates with
$$
\begin{align}
z=r\cos\theta, \\
x=r\sin\theta \cos \phi \\
y=r\sin\theta \sin \phi
\end{align}
$$
We get 
$L_{zop}= \frac{\hbar}{i} \frac{ \partial  }{ \partial \phi }$

## Hop for a central potential
We can write the function $\psi_{E}(r,\theta,\phi=R(r)Y(\theta,\phi)$
# stuff I missed


## Eigenstates of $Lz_{op}$

$L_{zop}=\frac{\hbar}{i}\frac{ d }{d \phi }\Phi(\phi)=L_{z} \Phi(\phi)$
We get the differential equation
$$
\begin{align}
\frac{ d }{d \phi } \Phi(\phi)= \frac{iL_{z}}{\hbar}\Phi(\phi) \\
\text{ which has the solution } \\
\Phi(\phi)=\frac{Ne^{iL_{z}\phi}}{\hbar}  
\end{align}
$$
Which we can normalize by going through all of space
$$
\begin{align}
\int_{0}^{2\pi} \left| \Phi \right| ^{2}d\phi=1 \\
N= \frac{1}{\sqrt[]{ 2\pi } } (\text{ assuming Real N}) \\
\end{align}
$$
$N$ must be single valued, since rotating about the plane must get the same value
$$
\begin{align}
\Phi(\phi)=\Phi(\phi+2\pi) \\
\frac{1}{\sqrt[]{ 2\pi } }e^{\left( iL_{z}\frac{\phi}{\hbar} \right)}+ \frac{1}{\sqrt[]{ 2 \pi} }e^{iL_{z}  \frac{\phi+2\pi}{\hbar}} \\
1= e^{\frac{iL_{z}2\pi}{\hbar}}
\end{align}
$$
This gives us quantization of angular momentum,
$L_{z}=m_{e} \hbar$    $m_{l}=0,\pm 1, \pm ~2, \pm ~3$


$$
\begin{align}
\Phi(\phi)=\frac{1}{\sqrt[]{ \pi }}\cos \phi= \frac{1}{\sqrt[]{ \pi } } \left(  \frac{e^{i\phi}}{2}+\frac{e^{-i\phi}}{2} \right)  \\
= \frac{1}{\sqrt[]{ 2 } } \left( \frac{e^{i\phi}}{\sqrt[]{ 2\pi } }+\frac{e^{-i\phi}}{\sqrt[]{ 2\pi } } \right) 
\end{align}
$$

