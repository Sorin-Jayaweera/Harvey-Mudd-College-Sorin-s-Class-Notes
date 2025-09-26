We can explore Ampere's law, since it doesn't have a flux of $E$ in it, even though the rest do have some sort of flux.

Lets go back to an infinite wire with current $i$, and try to find the magnetic field with Ampere's law.

To find the field at some distance r from the wire, we make a symmetry argument and say that $\vec{B}=B(r)\hat{\phi}$. We made a circle Amperian loop circulating around. We calculated the left and right hand side of $\oint\vec{B}\cdot \vec{dl}=\mu_{0}i_{enc}$
$$
\begin{align}
\implies B(r)2\pi r =\mu_{0}i, \\
B(r)=\frac{\mu_{0}i}{2\pi r}
\end{align}
$$
We can imagine a different surface, like a bubble.![[Pasted image 20241024095410.png]]
We haven't yet broken anything.
Lets try adding a charging capacitor. We still have the magnetic field, but if we try to make the edge of our surface between the capacitor... 
![[Pasted image 20241024095745.png]]
What! 
Proposal: Add a term to Ampere's law. 
Between the parallel plate capacitor, we have a constant electric field. 
$\left| E \right|=\frac{\sigma}{\epsilon_{0}}, =\frac{q}{\pi r^{2}\epsilon_{0}}$. As q increases, the electric field becomes larger with time. 

We can write the law as
$$
\begin{align}
\oint\vec{B}\cdot \vec{dl} =\mu_{0}i_{enc}+(?)\frac{d}{dt} \iint\vec{E}\cdot \vec{dA} 
\end{align}
$$
We have no flux through the tube portion since $\vec{E}\cdot  \vec{dA}=0$, but for the cap we have $\frac{q}{\pi r^{2}\epsilon_{0}}*\pi R^{e}=\frac{q}{\epsilon_{0}}$
We now get
$$
\begin{align}
\oint\vec{B}\cdot \vec{dl} =0+(?)\frac{d}{dt} \frac{q}{\epsilon_{0}}=(?). \\
\text{ if  }(?)=\mu\epsilon_{0}, \text{ then we get }\mu_{0}i. \\
\text{ This gives us the fixed and final maxwell's equation }. \\
\oint\vec{B}\cdot \vec{dl} =\mu_{0}i_{enc}+\mu_{0}\epsilon_{0}\frac{d}{dt} \iint\vec{E}\cdot \vec{dA} 
\end{align}
$$
This new term is called the "displacement current".

Lets try to apply this. What is $\vec{B}$ inside the plates?
![[Pasted image 20241024101732.png]]
For $r>R$, we don't have any contribution beyond the R of the capacitor. That changes our expression instead to be
$B(r)2\pi r = \frac{\mu_{0}i\pi R^{2}}{\pi R^{2}}$
$B(r)=\frac{\mu_{0}i}{2\pi r}$


We also have a differential form via stokes theorem:
$$
\begin{align}
\iint(\vec{\nabla}\vec{x}\vec{B})\cdot \vec{dA} =\iint\left( \mu_{0}\vec{j}+\mu_{0}\epsilon_{0}\frac{ \partial \vec{E} }{ \partial t }  \right)\cdot \vec{dA}  \\
\vec{\nabla} \times  \vec{B} =\mu_{0}\vec{j}+\mu_{0}\epsilon_{0} \frac{ \partial \vec{E} }{ \partial t } 
\end{align}
$$
#### Implication 1)
$$
\begin{align}
\vec{\nabla}\cdot(\vec{\nabla}\times  \vec{B})=\mu_{0}(\vec{\nabla}\cdot \vec{j})+\mu_{0}\epsilon_{0}\frac{ \partial  }{ \partial t }(\vec{\nabla}\cdot \vec{e}) \\
0 = \vec{\nabla}\cdot \vec{j}+\frac{ \partial  }{ \partial t } \left( \frac{\rho}{\epsilon_{0}} \right) \\
\vec{\nabla}\cdot \vec{j}=-\frac{ \partial \rho }{ \partial t }  
\end{align}
$$
This is the continuity equation for charge. 
We can put this into an integral form that is more intuitive.
$$
\begin{align}
\iiint(\vec{\nabla}\cdot \vec{j})=-\frac{ \partial  }{ \partial t } \iiint \rho dv \\
\text{ by the divregence theorem } \\
∯\vec{j}\cdot \vec{dA} =-\frac{ \partial Q_{tot}   }{ \partial x } 
\end{align}
$$
Which shows charge conservation. 

#### Implication #2)
If we assume no sources of electric or magnetic field, i.e. $\rho=0,\vec{j}=0$.

$$
\begin{align}
\vec{\nabla}\cdot \vec{E}=0 \\
\vec{\nabla}\cdot \vec{B}=0 \\
\vec{\nabla}\times  \vec{E}=-\frac{ \partial \vec{B} }{ \partial t }  \\
\vec{\nabla}\vec{x}\vec{B}=\mu_{0}\epsilon_{0}\frac{ \partial \vec{E} }{ \partial t } 
\end{align}
$$
Lets take the curl of the third equation.

$$
\begin{align}
\vec{\nabla}\vec{x}(\vec{\nabla}\vec{x}\vec{E})=-\frac{ \partial (\vec{\nabla}\vec{x}\vec{B}) }{ \partial t } \\
\end{align}
$$
$$
\boxed{
\begin{align}
-\nabla^{2}\vec{E}=\mu_{0}\epsilon_{0}\frac{ \partial^{2}\vec{E} }{ \partial t^{2} }  
\end{align}
}
$$
This is a vector equation, so the Laplacian of the  electric field in the x direction is related to the second partial o the electric field in the x direction.
As a one d example, we can show:
![[Pasted image 20241024105132.png]]