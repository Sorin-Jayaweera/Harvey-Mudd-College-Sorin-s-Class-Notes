This is so far made up, cultural enrichment. The physics of a cool idea that maybe there are extra spatial dimensions, and to understand the implications of that idea. 



## Gravity is puny
$$
\begin{align}
\vec{F}_{g}  = \frac{GMm}{r^{2}}\hat{r} \\
\vec{F}_{E} = \frac{1}{r\pi\epsilon_{0}} \frac{q_{1}q_{2}}{r^{2}}\hat{r}
\end{align}
$$

We choose to compare the forces for an electron.
$$
\begin{align}
\frac{F_{e}}{F_{g} } = \frac{\frac{e^{2}}{4\pi\epsilon_{0}}}{GM_{e} ^{2}} = 4\times  10^{42} = \frac{\alpha_{EM}}{\alpha_{g} } 
\end{align}
$$



Recall for the electric field we have gauss's law:
$$
\begin{align}
\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\epsilon_{0}} \\
∯ \vec{E}\cdot dA = E \cdot 4\pi r^{2} = \frac{q}{\epsilon_{0}}  \\
\implies E = \frac{q}{r\pi\epsilon_{0}r^{2}}
\end{align}
$$

We have a similar law for gravitation:
$$
\begin{align}
\vec{\nabla}\cdot \vec{g} = -4\pi G \rho_{m}  \\
∯ \vec{g}\cdot d\vec{A} = 4\pi r^{2}\cdot g = -4\pi GM \\
\vec{g} = - \frac{GM}{r^{2}}\hat{r}
\end{align}
$$

How would this change if we were in two dimensions?
We integrate around the surface of a circle, and have $dl$ instead of $dA$. 
Gravity becomes
$$
\begin{align}
\vec{g} = -\frac{2GM}{r}\hat{r}
\end{align}
$$
## In more dimensions
in $3+{N}$ dimensions 
$$
\begin{align}
\vec{g} = \frac{\vec{F}}{m} = -G_{n} \frac{M}{r^{2+n}}\hat{r}
\end{align}
$$
We are spreading out the force over larger surface areas, but also $G$ is changing.
$$
\begin{align}
G_{n} = GR^{n}
\end{align}
$$
$r$ is the separation between the test objects, and $R$ is some length scale associated with the dimension. 

The idea is that we have gravity leaking out to other dimensions on tiny length scales to fill up the space. 

Note this is a "crazy theory" because it is totally unverified. However, experiments that would explore this are hard, because of how puny gravity is. 


Lets talk about the quantum mechanical implications

The Schrödinger is non relativistic. 

## Relativistic Wave Equation
The Klein-Gordan Equation acts twice on the Schrödinger with a relativistic Hamiltonian operator
$$
\begin{align}
-\hbar^{2}c^{2} \nabla^{2} \Psi + m^{2}c^{4}\Psi = -\hbar^{2} \frac{ \partial^{2} }{ \partial t^{2} } \Psi 
\end{align}
$$
This comes from taking the assumption:
$$
\begin{align}
\Psi = e^{i(\vec{k}\cdot \vec{r} - \omega t)} \\
\underbrace{ \hbar \omega }_{ E } = \sqrt[]{\underbrace{  \hbar^{2}k^{2}c^{2} }_{ P }+m^{2}c^{4} }   \\
E^{2} = p^{2}c^{2}+m^{2}c^{4} 
\end{align}
$$

Anyways, the klein gordon equation has a laplacian so we would extend this to more dimensions. For 4:
$$
\begin{align}
\nabla^{2} = \frac{ \partial^{2} }{ \partial x^{2} } + \frac{ \partial^{2} }{ \partial y^{2} } + \frac{ \partial^{2} }{ \partial z^{2} } + \frac{ \partial^{2} }{ \partial u^{2} } 
\end{align}
$$
$$
\begin{align}
\hbar^{2}c^{2} \left[  \frac{1}{c^{2}} \frac{ \partial^{2} }{ \partial t^{2} } - \nabla^{2} \right]\Psi  + m^{2}c^{4}\Psi  = 0
\end{align}
$$
The solutions to this are very similar,
$$
\begin{align}
\Psi  = e^{i(\vec{k}\cdot \underbrace{  \vec{r} }_{ x \hat{x}+y \hat{y} + z \hat{z} } + k_{u} u - \omega t )} e^{\frac{-iEt}{\hbar}}
\end{align}
$$
The wave function has to be single valued and continuous as we go around the new dimension. 
$$
\begin{align}
\Psi (\dots,u,\dots) = \Psi (\dots,u+2\pi R,\dots)
\end{align}
$$
$$
\begin{align}
e^{\frac{-iEt}{\hbar}}e^{i(\vec{k}\cdot \vec{r}+k_{u}u)}= e^{\frac{-iEt}{\hbar}}e^{-i(\vec{k}\cdot r + k_{u} (u+2\pi R))} \\
e^{i k_{u} u} = e^{ik_{u} (u+2\pi R)}  \\
\implies k_{u} R = 0,\pm  1,\pm  2,\dots 
\end{align}
$$
$$
\begin{align}
k_{u} = \frac{n}{R}, n \in \mathbb{Z}
\end{align}
$$
So the momentum along $u$ is quantized.

The energies associated with those states
$$
\begin{align}
E_{n}^{2} = \hbar^{2} \left| \vec{k} \right| ^{2} c^{2} + \hbar^{2}\left( \frac{n}{R} \right)^{2}c^{2}+m^{2}c^{4} \\
\end{align}
$$
in the rest frame of the particle's 3d motion, we would get
$$
\begin{align}
E_{n} ^{2} = \hbar^{2}\left( \frac{n^{2}c^{2}}{R^{2}} \right)+ m^{2}c^{4}
\end{align}
$$
