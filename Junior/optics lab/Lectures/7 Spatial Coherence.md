We have the wave equation
$$
\begin{align}
\nabla^{2} E^{(+)} - \frac{1}{c^{2}} \frac{ \partial^{2} E^{(+)} }{ \partial t^{2} } = 0  \\
\nabla^{2} E^{(+)} = \frac{1}{c^{2}} \frac{ \partial^{2} E^{(+)} }{ \partial t^{2} }   \\ \text{ if we have seperation of variables } E^{(+)}(\vec{r},t) & = U(\vec{r})T(t)\\
T(t)\nabla^{2}U(\vec{r})= \frac{1}{c^{2}}u(\vec{R})\frac{ \partial^{2}T(t) }{ \partial t^{2} }  \\
\text{ or } \\
\frac{\nabla^{2}u}{u}= \frac{1}{c^{2}} \frac{\frac{ \partial^{2}T }{ \partial t^{2} } }{T} = -k^{2}
\end{align}
$$


This is only true if each side equals the same constant independent of $\vec{r}(t)$
This gives us 
$$
\boxed{
\begin{align}
\nabla^{2}u = -k^{2}u
\end{align}
}\, \, \, 

\boxed{
\begin{align}
\frac{ \partial^{2}T }{ \partial t^{2} } = -c^{2}K^{2}T=-\omega^{2}T \text{ if } \frac{\omega}{k}=c
\end{align}
}
$$
Lets take the Ansatz $T(t)=e^{-i\omega t}$. 


We take a paraxial approximation, end up with basically the Schrödinger equation but spatially and without some constants
$$
\boxed{
\begin{align}
\frac{ \partial^{2}\psi }{ \partial x^{2} } + \frac{ \partial^{2} \psi}{ \partial y^{2} } = -i 2k \frac{ \partial \psi }{ \partial z } 
\end{align}
}
$$
We can just take solutions from the same ideas we have for solutions from the Schrödinger. 

The simplest type of solution is a gaussian wave packet. 