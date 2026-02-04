We thought about light as charge density and current density. Now lets think of free charge density and free current density.



$$
\begin{align}
\vec{\nabla}\times(\vec{\nabla}\times \vec{E})  & = -\frac{ \partial  }{ \partial t } (\vec{\nabla}\times \vec{B}) \\
\vec{\nabla}(\vec{\nabla}\cdot \vec{E})- \nabla^{2}\vec{E} &  = -\frac{ \partial  }{ \partial t } \left( \mu \frac{ \partial \vec{D} }{ \partial t }  \right)  \\
\nabla^{2} \vec{E}  & = \mu \frac{ \partial^{2} }{ \partial t^{2} } \vec{D} \\
\nabla^{2}\vec{E}  & = \mu\epsilon \frac{ \partial^{2}\vec{E} }{ \partial t^{2} } 
\end{align}
$$
We thus have the wave equation for wave speed
$$
\begin{align}
c = \frac{1}{\sqrt[]{ \epsilon \mu } } = \frac{C_{0}}{\eta}
\end{align}
$$
where $\eta$ is the index of refraction, $\sqrt[]{ \kappa_{e} \kappa_{m} }$

$$
\begin{align}
\vec{E}  & = \vec{E}_{0} \cos\left( 2\pi \left( \frac{x}{\lambda }- \frac{t}{T} \right)+ \phi_{0} \right) \\
 & =\vec{E}_{0} \cos(k x - \omega t + \phi_{0}) \\
 & =\vec{E}_{0}\left( k \left( x- \frac{\omega}{k}t \right)+ \phi_{0} \right) 
\end{align}
$$
$\frac{\omega}{k} = \lambda \nu = c$.

However, this is really much nicer to write as the real part of $e^{i\text{ stuff }}$ so that we can work with it easier.
$$
\begin{align}
\frac{\vec{E}_{0} }{2} e^{i (kx-\omega t+\phi_{0})}+ \frac{\vec{E}_{0}}{2} e^{-i(kx-\omega t+\phi_{0})} 
\end{align}
$$
For a general propagation direction, let $\vec{k}=\left( \frac{2\pi}{\lambda} \right)\hat{K}$
$$
\begin{align}
\vec{E}(\vec{r},t) = \frac{\vec{E}}{2}(e^{i(\vec{k} \cdot \vec{r} - \omega t + \phi_{0})}+e^{-i(\vec{k} \cdot \vec{r} - \omega t + \phi_{0})})
\end{align}
$$
We don't really car about $\phi_{0}$, so 
$$
\begin{align}
\vec{E}(\vec{r},t) = \frac{\vec{E}}{2}(e^{i\phi_{0}}e^{i(\vec{k} \cdot \vec{r} - \omega t)}+e^{-i\phi_{0}}e^{-i(\vec{k} \cdot \vec{r} - \omega t)})
\end{align}
$$
Lets call $\frac{\vec{E_{0}}}{2}e^{i\phi}=\vec{E}_{0}^{+}$, and the complex conjugate $\vec{E}_{0}^{-}$. Now we just have
$$
\begin{align}
\vec{E}_{0}^{+}e^{i(\vec{k}\cdot \vec{r}-\omega t)} + \text{ the complex conjugate }
\end{align}
$$
