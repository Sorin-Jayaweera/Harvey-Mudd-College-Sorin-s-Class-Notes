Two of maxwells equations are perfectly fine and aren't going to change: Gauss's law and no monopoles.
$$
\begin{align}
∯ \vec{E}\cdot \vec{dA} =\frac{q_{enc}}{\epsilon_{0}} \\
\text{ and } \\
∯\vec{B}\cdot \vec{dA} =0
\end{align}
$$
However, we have to refine faraday's law.

There are three variants of the law, all of which are equivalent. Lets take the first .
$$
\begin{align} 
 & \text{ (voltage) }\\
E_{loop} & =-\frac{d}{dt}\Phi_{b}  \\
&  =-\frac{d}{dt} \iint\vec{B}\cdot \vec{dA} \\
\end{align}
$$
Lets show an example of how to do this.
![[Pasted image 20241017095246.png]]
As we move the magnet closer, the magnetic field gets bigger. This means that $\frac{d}{dt}\iint\vec{B}\cdot \vec{dA}$ is positive, so there is voltage (electromotive force) induced in the - direction. Electromotive force is not a force, it is a potential. It is work per unit charge.

##### Lenz's Law:
Induced EMF around a loop is always in the direction that opposes the change in magnetic flux through the loop. 

![[Pasted image 20241017100512.png]]

Lets do an example:
![[Pasted image 20241017102320.png]]
The magnetic field from a solenoid is $\mu_{0}n i$.
Our flux is
$$
\begin{align}
\Phi_{b}=\iint\vec{B}\cdot \vec{dA} =B(\pi r_{s}^{2}) \\
\end{align}
$$
How much current is induced?
$$
\begin{align}
i=\frac{E_{ind}}{R} \\
E_{ind}=-\frac{d}{dt} \pi r_{s}^{2} \frac{d}{dt} B \\
\text{ we can plug in the expression for I }, \\
E_{ind}=+\pi r_{s}^{2}\mu_{0}n \frac{i_{0}}{\tau}e^{-t/\tau}
\end{align}
$$
We drive currents by changing magnetic fields or the area of the loop. 
![[Pasted image 20241017104228.png]]
Sliding the bar to the left increases the area, and by Lenz's law the current will oppose the field $\to$ current is induced clockwise.

We could also rotate the area by changing the angle relative to $\vec{B}\cdot \vec{dA}$.

$$
\begin{align}
\oint\vec{E}\cdot \vec{dl} =-\frac{d}{dt}\iint\vec{B}\cdot \vec{ds}  \\
\vec{\nabla} \times \vec{E}=-\frac{ \partial \vec{B} }{ \partial t }   
\end{align}
$$
