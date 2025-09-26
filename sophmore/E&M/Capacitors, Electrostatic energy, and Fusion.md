---
lecture: phys-51-8
---
Special lecture by Prof. Donnelly.

An isolated conductor carrying a charge $Q$ will have a potential $V_{0}$ with the zero of potential at infinity; $Q$ is proportional to $V_{0}$. The proposition in electrostatics is that $Q \propto V_{0}$ at its surface.

If we remember that $V=-\int_{a}^{b}\vec{E}\cdot \vec{ds}$, we can note that doubling a charge will double the field, then doubling the potential. 
Capacitance is taking that statement, it is the concept of proportionality between a charge and the potential.
$$
\begin{align}
Q=CV \\
C\geq 0 \text{ (Farads) }
\end{align}
$$
This is for a single conductor, but we can write out a more common system with a $+Q$ and a $-Q$.

![[Pasted image 20240919095432.png]]

We can calculate the capacitance between the system by first solving for the potential difference between the plates, then substituting $Q=CV$ and solving for $C$. Notice, this is a geometric quantity, it does not depend on the potential difference across the plates.


How much work does it cost to generate a potential across a plate?
The potential is the work per unit charge (joules per coulomb).
$$
\begin{align} \\
W=VQ\\
dw=Vdq\\
\end{align}
$$

We can now calculate,
$$
\begin{align}
W & =\int_{0}^{Q} Vdq \\
 & = \int_{-}^{Q} \frac{q}{c}dq \\
 & =\frac{1}{2C}Q^{2} \\
W& = \frac{1}{2}CV^{2}
\end{align}
$$
We can now think of energy as mechanical work!
$$
\begin{align}
U=W_{charging}=\frac{1}{2}cV^{2}. \\
\left( \text{ remember }V=-\int_{-}^{+} \vec{E}\cdot \vec{ds}  \right) \\
V_{\mid\mid}=Ed \\
\frac{1}{2}cV^{2}=\frac{1}{2}C(E^{2}d^{2}) \\
=\frac{1}{2}\left( \frac{\epsilon_{0} A}{d} \right)(E^{2}d^{2}) \\
= \frac{1}{2\epsilon_{0}E^{2}\underbrace{ (Ad) }_{ \text{ volume } }} \\
\mu=\frac{U}{\text{ volume }}=\frac{1}{2}\epsilon_{0}E^{2}
\end{align}
$$

This gives us a different way of thinking about the system. Before we thought of this as mechanical work where we are manually moving the charges around. Now, we can think about the energy as the density stored in the electric field.
$u_{e}=\frac{1}{2}\epsilon_{0}E^{2}=\frac{\text{ work }}{\text{ volume }}$.

In the case of a photon (which has no mass), the energy is stored in the oscillations in the electric and magnetic field.

Aside: an electron volt is the energy gained by a single electron when moving across a 1 volt potential difference. 


Lets consider building a ball of charge mechanically.
![[Pasted image 20240919104439.png]]
$$
\begin{align} 
W=Vdq\\
W=\int_{0}^{Q} \frac{q}{4\pi\epsilon_{0}r}d_{q} \\
\text{ r and q are dependent on each other } \\
\Rightarrow  \left( \frac{q}{\frac{4}{3}\pi \rho} \right) ^{\frac{1}{3}} \\
W=\int_{0}^{Q} \text{ constants }q^{2/3}dq \\
W=\frac{3}{5} \frac{1}{4\pi\epsilon_{0}} \frac{Q^{2}}{R}
\end{align}
$$

We can also build this sphere using the electric field approach.
$$
\begin{align}
U_{e} & =\int \frac{\epsilon_{0}E^{2}}{2}d(\text{ volume }) \\
U & =\int \underbrace{ \mu }_{ \frac{J}{m^{3}} }  \, dV \\
 & = \int \frac{1}{2}\epsilon E^{2} \, dV \\
   
\end{align}
$$![[Pasted image 20240919104415.png]]

See previous [[More on the electrostatic field]]
See next [[Current and Circuits]]
