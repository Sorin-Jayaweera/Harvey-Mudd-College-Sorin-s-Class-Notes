
We are bringing free charges through infitesimal steps from infinity into the presence of a dielectric.

$$
\begin{align}
\delta W \int \phi \underbrace{ \delta \rho dV }_{ \delta q }
\end{align}
$$

$$
\begin{align}
W = \int_{\rho=0}^{\rho}  \delta W
\end{align}
$$

$\rho$ is free charge, so
$$
\begin{align}
\vec{\nabla}\cdot \vec{D} = 4\pi \rho
\end{align}
$$
$\rho$ is *only* free charge, and only sources $\vec{D}$. $\vec{E}$ contains both the effect from free charges AND the materials response. 

$$
\begin{align}
\delta W  & = \int \phi \delta \rho dV  \\
 & = \int \phi \frac{\vec{\nabla} \delta \vec{D}}{4\pi} dV \\
 & = - \int \frac{\vec{\nabla} \phi \cdot \delta \vec{D}}{4\pi}dV \\
\end{align}
$$
For a linear material
$$
\begin{align}
\vec{D} = \epsilon \vec{E} \propto \vec{E} \\
\vec{E} \cdot \delta \vec{D} = \frac{1}{2} \delta(\vec{E}\cdot \vec{D})
\end{align}
$$

$$
\begin{align}
 & = \frac{1}{4\pi} \int \vec{E} \cdot \delta \vec{D} dV \\
 & = \frac{1}{8\pi} \int \delta(\vec{E}\cdot \vec{D})dV
\end{align}
$$

This gives us
$$
\begin{align}
W = \frac{1}{8\pi} \int (\vec{E} \cdot \vec{D}) dV
\end{align}
$$
In a vacuum, $\vec{D}= \vec{E}$, so energy density $u= \frac{E^{2}}{8\pi}$.
In a dielectric, the energy density is
$$
\begin{align}
u = \frac{\vec{E}\cdot \vec{D}}{8\pi}
\end{align}
$$


Lets look at two cases that arise commonly. 


1: What is we keep free charges fixed, pin them down, and bring in a dielectric. How much does the energy change? 

Initially, we have some $\vec{E}_{0}, \vec{D}_{0}$. After the dielectric, these become $\vec{E},\vec{D}$. The work done is
$$
\begin{align}
W = \frac{1}{8\pi} \int( \vec{E}\cdot \vec{D} - \vec{E}_{0}\cdot \vec{D}_{0} )dV
\end{align}
$$
We haven't yet used the fact that the free charges are fixed. Lets write this in a strange way. 

$$
\begin{align}
W = \frac{1}{8\pi} \int \vec{E} \cdot \vec{D}_{0} - \vec{E}_{0}\cdot \vec{D} 
\end{align}
$$
This is obviously not the same. We need to add a term to make it equal. 


$$
\begin{align}
W = \frac{1}{8\pi} \int [\vec{E} \cdot \vec{D}_{0} - \vec{E}_{0}\cdot \vec{D} + (\vec{E} + \vec{E}_{0}) \cdot (\vec{D}- \vec{D}_{0})] dV
\end{align}
$$
Why the hell?

Because! $$
\begin{align}
\vec{E}+\vec{E_{0}} =  -\vec{\nabla}\phi
\end{align}
$$
At infinity, it vanishes. The integration by parts will make the new term
$$
\begin{align}
(\vec{E}+\vec{E}_{0})\cdot(\vec{D}-\vec{D}_{0})dV = \phi \vec{\nabla} \cdot \cancelto{ 0 }{ (\vec{D}-D_{0}) }
\end{align}
$$

because the free charges don't change. 

Therefore, we can just write it like
$$
\begin{align}
W = \frac{1}{8\pi} \int (\vec{E}\cdot \vec{D}_{0} - \vec{E}_{0}\cdot \vec{D} )dV
\end{align}
$$
Weird.

Lets take a parallel plate capacitor. The area is $a$. Lets put $\sigma$ charge density on the top, and $-\sigma$ on the bottom.

Lets put a dielectric immersed in between the plates, which has some width $x$ and height $l$. 

![[Pasted image 20261029095637.png]]

If we make it a square, the area of our dielectric is $lx$, and the area of the other bit is $l(l-x)$. (The capacitor is also a square). 

We have $Q = \sigma l^{2}$. 

We will now have two different densities: $\sigma_{1}$ above the dielectric on the top plate, and $\sigma_{2}$ not above the dielectric. We have the negatives of these on the lower plate. 

We have
$$
\begin{align}
\sigma_{1} lx + \sigma_{2} l(l-x) = Q \\
\vec{\nabla}\cdot \vec{D} = 4\pi \rho \\
\vec{D} = 4\pi\sigma \hat{z}\\
\vec{D}_{1} = 4\pi \sigma_{1}\hat{z} \\
\vec{D}_{2} = 4\pi\sigma_{2}\hat{z}
\end{align}
$$

We know that
$$
\begin{align}
\vec{D} = \epsilon \vec{E} \\
\vec{D}_{1} = \epsilon_{1} \vec{E}_{1} \\
\vec{D}_{2} = \epsilon_{2} \vec{E}_{2} = \vec{E}_{2} \\
\end{align}
$$

$$
\begin{align}
\vec{E}_{1} = \frac{\vec{D}_{1}}{\epsilon_{1}} \\
E_{1} = \frac{4\pi\sigma_{1}}{\epsilon_{1}} \\
E_{2} = 4\pi\sigma_{2}
\end{align}
$$

At the boundary, the tangential component of $\vec{E}$ is continuous (pointing from one plate to the other). Therefore, $\vec{E}_{1}=\vec{E}_{2}$. OR $\frac{\sigma_{1}}{\epsilon_{1}}=\sigma_{2}$. Remember that we had $\sigma_{1}lx + \sigma_{2}l(l-x)=Q$. We can now find $\sigma_{1}$ and $\sigma_{2}$. Two linear equations, two unknowns. Easy peasy. 

$$
\begin{align}
\sigma_{2}  & =  \frac{Q}{(\epsilon_{1}-1)lx+l(l-x)} \\
\Delta W  & = \frac{1}{8\pi} \int (\vec{E}\cdot \vec{D}_{0} - \vec{E}_{0}\cdot \vec{D})dV
\end{align}
$$

$$
\begin{align}
\Delta W = \frac{-2\pi Q^{2} h (\epsilon-1)}{(\epsilon-1)lx + l(l-x)} < 0
\end{align}
$$
where $h$ is the width and height of the dielectric. 

Dielectrics lower the energy needed per free charge, which increases the capacitance of a capacitor.
$$
\begin{align}
C \to  \epsilon C
\end{align}
$$
For $\epsilon>1$, the capacity to store energy in charge increases. 


In the second case, we keep a battery hooked up while we insert a dielectric in between the plates of the capacitor. 

We fix the potential difference $\Delta \phi$ with the battery. 
![[Pasted image 20261029100905.png]]

Because $\vec{E}$ is uniform, from a fixed $\Delta \phi$, 
$$
\begin{align}
\vec{E} = \frac{\Delta \phi}{h}
\end{align}
$$
Knowing the $\vec{E}$ field in both regions ($\vec{E}_{1}$ is in the dielectric)
$$
\begin{align}
\vec{E}_{1} = \frac{\nabla \phi}{h} &  & = \vec{E}_{2} &  \\
\vec{D}_{1} = \epsilon_{1} \vec{E}_{1}  &  & \vec{D}_{2} = \vec{E}_{2} 
\end{align}
$$

We find
$$
\begin{align}
W &  = \frac{1}{8\pi} \int \vec{E}\cdot \vec{D} dV \\
 & = \frac{1}{8\pi} E^{2} ((l-x)l + \epsilon lx)h \\
\frac{ d W}{d x }  & = \frac{E^{2}}{8\pi} (-l + \epsilon l)h >0
\end{align}
$$


$$
\begin{align}
F = - \frac{ d W}{d x } 
\end{align}
$$
so the force is negative, which tries to eject the dielectric. 
