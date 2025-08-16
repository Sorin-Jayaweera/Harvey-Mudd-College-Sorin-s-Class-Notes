Solid State Physics!

Why are some things shiny, some see transparent, dielectric, insulators, etc?

## Band structure of solids

We model a one dimensional chain of atoms in a first order model.
Lets start with Sodium, which has a hydrogenic potential. 

![[Pasted image 20250411100620.png]]

Lets put a delta function between each atom, and write the potential function
![[Pasted image 20250411101043.png]]
We have a bunch of delta functions between each atom, and within we have a function $\alpha$ that tells us the height.

This is the 
## Kronig-Penny model
We can draw a picture and identify symmetries. 

We have a discrete translational symmetry, where shifting by the lattice constant (spacing) gives us the same function. 
$$
\begin{align}
\left| \Psi (x+a) \right| ^{2}=\left| \Psi (x) \right| ^{2}
\end{align}
$$
so we can have a phase difference but preserve the overall magnitude. We have:
$$
\begin{align}
\Psi (x+a) = e^{i\theta}\Psi (x)
\end{align}
$$
We can solve for the phase by applying periodic boundary conditions. 

This is the boundary at the far left and far right side of our infinite chain, and then later in between the atoms. 

### The edges of the box:
![[Pasted image 20250411101530.png|300]]
![[Pasted image 20250411101547.png|300]]

Lets make an approximation and say our chain is infinite because we are tying the atoms in a loop. In a small block of copper with Avogadro's number of atoms, just along one side length we have $10^{8}$  (cubed root to get just a length ) or more atoms -- the farthest boundary conditions shouldn't affect the internal atoms with this many. 

Lets make an ansatz argument that we add a phase factor each atom we jump. 
$$
\begin{align}
\Psi (x+Na)=e^{iN\theta}\Psi (x)=\Psi (x)
\end{align}
$$
by our periodic boundary conditions.
$$
\begin{align}
e^{IN\theta}=1, \\
 \theta= \frac{2\pi}{N}r,  &  & r = 0,\pm  1,\pm  2,\dots,\pm  N-1
\end{align}
$$

We can quantize the allowed values of energy and $\theta$. 

## Kronig Penny Solutions
$$
\begin{align}
E= \frac{\hbar^{2}k^{2}}{2M}, k=\sqrt[]{ \frac{2Me}{\hbar^{2}} } 
\end{align}
$$
We write the time independent Schrödinger for each location, but that seems like too much work. What if we build in the block ansatz to make our lives easier?

$$
\begin{align}
\Psi_{n} (x) = A_{n} Sin(k[x-na])+B_{n}\cos(k[x-na]), (n-1)a < x < na
\end{align}
$$
We build in the block ansatz by saying $a_{n}+1=e^{i\theta}A_{n} \text{ and } B_{n+1}= e^{i\theta}B_{n}$.


Now lets apply interior boundary conditions, on either side of the $\Psi_{n}^{th}$ block.

For continuity of the wavefunction,
$$
\begin{align}
\Psi_{n} (x=na) = \Psi _{n+1} (na)   \tag{1} 
\end{align}
$$
While the value is continuous, the derivative is discontinuous. We have the condition for discontinuous functions that
$$
\begin{align}
\left( \frac{ d \Psi _{n+1} }{d x }  \right) _{na^{+}} - \left( \frac{ d \Psi_{n}  }{d x }  \right) _{na^{-}}  = \frac{\alpha}{a} \psi _{n}(na)   \tag{2} 
\end{align}
$$

Applying 1) 

$$
\begin{align}
\cancelto{ 0 }{ A_{n}\sin(k(0)) }+B_{n}\cancelto{ 1 }{ Cos(0) }= \underbrace{ a_{n+1} }_{ a_{n}e^{i\theta} }\sin(k(-a))+ B_{n+1 } \cos(-ka) \\
B_{n}= A_{n}e^{i\theta}(-\sin(ka))+ B_{n}e^{i\theta}\cos(ka)
\end{align}
$$

Applying 2) 
$$
\begin{align}
k[A_{n+1 }\cos(-ka) - B_{n+1}\sin(-ka) ] - k[A_{n}\cancelto{ 1 }{ \cos(0) } - B_{n}\cancelto{ 0 }{ \sin(0) }] = \frac{\alpha}{a}B_{n} \\
A_{n}e^{i\theta}\cos(ka) + B_{n}e^{i\theta}\sin(ka)- A_{n}= \frac{\alpha}{ka}B_{n} \\

\end{align}
$$

For both of our conditions, we have the nice final forms:

$$
\begin{align} 
A_{n}(e^{i\theta}\sin(ka)) = B_{n}(e^{i\theta}\cos(ka)-1)\\
A_{n}e^{i\theta}\cos(ka)-1 = B_{n}\left(\frac{\alpha}{ka}-e^{i\theta}\sin(ka)\right)
\end{align}
$$
We could solve this with some algebra. We get
$$
\begin{align}
\cos\theta=\cos(ka)+ \frac{\alpha}{2ka}\sin(ka), \\
\text{ recall } \\
\theta= \frac{2\pi r}{N}, r= 0,1,\dots,N-1
\end{align}
$$
There are n solutions but $\cos$ is periodic so we have $\frac{n}{2}$ values.
![[Pasted image 20250411104526.png]]
We have solutions over a finite range of ka, then no solutions. 

![[Pasted image 20250411104749.png]]




