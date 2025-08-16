It is time for us to embrace 3 dimensionality!
Spherical coordinates, extra derivatives, hold on to your hats. But applications! 

Today we will calculate the temperature of the electrons in the white dwarf Sirius A!

We'll make a 3-D particle box and define Fermi Energy. 

We have a box with zero potential inside, and infinite outside.
![[Pasted image 20250303100724.png|300]]

To write out the Schrödinger, we have to have new definitions of operators:
$$
\begin{align}
p_{xop}=\frac{\hbar}{i} \frac{ \partial  }{ \partial x } , x_{op} =x \\
p_{yop}=\frac{\hbar}{i} \frac{ \partial  }{ \partial y } , x_{op} =x \\
p_{zop}=\frac{\hbar}{i} \frac{ \partial  }{ \partial z } , x_{op} =z
\end{align}
$$
The 3D $H_{op}=\frac{\hbar^{2}}{2m}\left( \frac{ \partial^{2} }{ \partial x^{2} }+\frac{ \partial^{2} }{ \partial y^{2} }+\frac{ \partial^{2} }{ \partial z^{2} } \right)+V(x,y,z)$
This looks like the Laplace operator $\nabla^{2}$
$H_{op}=\frac{\hbar^{2}}{2m}(\nabla^{2})$

We write out the Schrödinger equation for 3d
$$
\begin{align}
H_{op} \Psi(x,y,z,t)=i \hbar \frac{ d }{d t } \Psi (x,y,z,t)
\end{align}
$$
We can use separation of variables. Lets guess that each of these components is a unique function.
$$
\begin{align}
\Psi (x,y,z,t)=\Psi (x,y,z)f(t)= \Psi (x,y,z)e^{\frac{-iEt}{\hbar}} \\
H_{op} \Psi (x,y,z)=E\Psi (x,y,z) \\
\end{align}
$$
We have our time dependent solution, and the time independent equation.

For the box, we get:
$$
\begin{align}
\left[ -\frac{\hbar^{2}}{2m}\left( \frac{ \partial^{2} }{ \partial x^{2} } +\frac{ \partial^{2} }{ \partial y^{2} }+\frac{ \partial^{2} }{ \partial z^{2} }   \right) +\cancelto{ 0 }{ V(x,y,z) } \right] \Psi =E\psi
\end{align}
$$
We want to define $\Psi(x,y,z)$ as a product of independent functions of $x,y,z$. We write this as:

$\Psi(x,y,z)=\mathbb{X}(x)\mathbb{Y}(y)\mathbb{Z}(z)$

We get
$$
\begin{align}
-\frac{\hbar^{2}}{2m}\left[ \frac{1}{\mathbb{X}}\frac{ \partial^{2} \mathbb{X} }{ \partial x^{2} } +\frac{1}{\mathbb{X}}\frac{ \partial^{2} \mathbb{Y} }{ \partial y^{2} } +\frac{1}{\mathbb{Z}}\frac{ \partial^{2} \mathbb{Z} }{ \partial x^{2} } + \right] =E \\
E = E_{x}+E_{y}+E_{z}
\end{align}
$$
We can rearrange this to be three one dimensional versions:
$$
\begin{align}
-\frac{\hbar^{2}}{2m} \frac{ d ^{2}\mathbb{X}}{d x^{2} } =E_{x}\mathbb{X } \\

-\frac{\hbar^{2}}{2m} \frac{ d ^{2}\mathbb{Y}}{d y^{2} } =E_{y}\mathbb{Y } \\

-\frac{\hbar^{2}}{2m} \frac{ d ^{2}\mathbb{Z}}{d z^{2} } =E_{z}\mathbb{Z }
\end{align}
$$
We solve this just as we did before:
$$
\begin{align}
\mathbb{X}_{x}= \sqrt{ \frac{2}{L} } \sin \left(  \frac{n_{x}\pi x}{L} \right) , n_{x}= 1,2,3\dots \\
E_{x} = \frac{\hbar^{2}\pi^{2}}{2mL^{2}}n_{x}^{2}
\end{align}
$$
We can write out a similar expression for the $\mathbb{Y} \text{ and } \mathbb{Z}$ components. For a review of this, see [[5 Solutions, Energy, and Forces]]. 

We now have
$$
\begin{align}
E= \frac{n^{2}\pi^{2}}{2mL^{2}}(n_{x}^{2}+n_{y}^{2}+n_{z}^{2})
\end{align}
$$

Lets do an example:
If we have $\Psi_{121}= \left( \frac{2}{L} \right)^{\frac{3}{2}}\sin\left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi y}{L} \right)\sin\left( \frac{\pi z}{L} \right)$
We have $n_{x} \frac{\hbar^{2}\pi^{2}}{2mL^{2}}(1^{2}+2^{2}+4^{2})=\frac{6\hbar^{2}\pi^{2}}{2mL^{2}}$
We see that this is the same as if we had $\Psi_{211},\Psi_{1}12$
We have degeneracy, which means that the energy state is shared between different wavefunctions. 

## Degeneracy and Degenerate Matter
Some material, like copper, metal, or a piece of a white dwarf.

Lets assume that the electrons are non interacting, so the electrons would go to the lowest energy state (ignoring Hund's rule and chemistry stuff):

![[Pasted image 20250303103701.png|300]]

## Fermi Energy

Imagine a block of copper as a cube with side lengths $L=1_{cm}$. It has approximately $10^{23}e^{-}$, $\left( \frac{N}{L^{3}}= \frac{8\cdot10^{22}}{cm^{3}} \right), n\gg 1$. We want to understand the total energy in the copper, so we'll start at $n_{x},n_{y},n_{z}=1$ and start filling in 2 electrons going radially out (fill out each radius and then move up). We go out to $r_{max}$. 
![[Pasted image 20250303104258.png|300]]

This is $\frac{1}{8}$ of a sphere, so we have
$$
\begin{align}
\underbrace{ \frac{1}{8} }_{ \text{ octant } }\underbrace{ \frac{4}{3} \pi r_{max}^{3} }_{ \text{ v sphere } } \cdot \underbrace{ 2 }_{ \text{ electrons per unit box} } \cdot \underbrace{ 1 }_{ \text{ unit box per unit area } }
\end{align}
$$
$r_{max}=\sqrt[3]{\frac{3n}{\pi}  }$
The maximum energy is 
$$
\begin{align}
E_{max}  =\frac{\hbar^{2}\pi^{2}}{2mL^{2}} \left( \frac{3N}{\pi} \right) ^\frac{2}{3}
\end{align}
$$
$$
\begin{align}
E_{\text{ Fermi }}  = \frac{\hbar^{2}}{2m}(3\pi^{2})^{\frac{2}{3}} \left( \frac{N}{L^{3}} \right)^{\frac{2}{3}} 
\end{align}
$$
You tell us how many electrons you are doing per unit volume, and we have the maximum energy of the electrons. 
>[!abstract]+ Definition:  Fermi Enegy
>the maximum energy of the occupied quantum states when $N$ fermions are placed into a 3-D box of volume $V$. It depends only on the number density (number per unit volume) of the particles and their mass. 

![[Pasted image 20250303105226.png]]
![[Pasted image 20250303105235.png]]
![[Pasted image 20250303105249.png]]