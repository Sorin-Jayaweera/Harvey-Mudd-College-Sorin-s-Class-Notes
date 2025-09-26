Recall the electrostatic potential. Lets try an example problem of a solid charged conducting sphere. What is V(r)?

We want two cases: the potential outside and inside the sphere.
![[Pasted image 20240917100831.png]]![[Pasted image 20240917100842.png]]


Since a conductor is an equipotential surface, we can start to visualize where the field (and charge) is more or less intense. We can show this as a topographical map with lines tracing across steps of the same potential.

The equipotential surfaces are always perpendicular to the field lines. It turns out that charge gets concentrated at the pointiest parts of conductors. 
![[Pasted image 20240917101247.png]]


Random mathematical interlude: What is the differential equation that governs V?

$$
\begin{align}
\nabla\cdot \vec{E}=\frac{\rho}{\epsilon_{0}}, \vec{E}=-\nabla V \\
\implies -\vec{\nabla}\cdot(\vec{\nabla}V)=\frac{\rho}{\epsilon_{0}} \\
\nabla^{2}V=\frac{ \partial^{2} V }{ \partial x^{2} }+\frac{ \partial^{2}V }{ \partial y^{2} } +\frac{ \partial^{2}V }{ \partial z^{2} } \\
\text{ Laplaces equation sets this as zero },   \\
\frac{ \partial^{2} V }{ \partial x^{2} }+\frac{ \partial^{2}V }{ \partial y^{2} } +\frac{ \partial^{2}V }{ \partial z^{2} } =0\\ 
\text{ which means that there are no maxima}\\\text{  or minima in free space,} \text{ as if two partials are positive}\\\text{  then the other has to be negative } \\
\text{ solutions to Laplaces equations are unique }
\end{align}
$$
![[Pasted image 20240917102310.png]]



Now we can talk about...
## Curl of the electrostatic field
$$
\begin{align}
\oint\vec{E}\cdot \vec{ds} =0 \\
\vec{\nabla}\times  \vec{E}=0 \\

\end{align}
$$
The line integral of the electric field around any closed path - or "circulation " of the electric field - is equal to zero in electrostatics.

The electric circulation per unit area at any point - or 'curl' of the electric field - is equal to zero in electrostatics.



![[Pasted image 20240917104721.png]]


We can combine the two electrostatics equations

$$
\begin{align}
\oint\vec{E}\cdot \vec{ds} =0 = \iint \vec{\nabla}\times  \vec{E}\cdot d\vec{A} \\
\text{ to get } \\
\iint (\vec{\nabla}\times  \vec{E})\cdot d\vec{A}
\end{align}
$$
See previous: [[sophmore/E&M/Electrostatic Potential]]
See next: [[Capacitors, Electrostatic energy, and Fusion]]