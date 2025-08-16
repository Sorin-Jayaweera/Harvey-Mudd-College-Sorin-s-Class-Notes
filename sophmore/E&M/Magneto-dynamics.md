Recall, $\vec{j}=\rho \vec{v}_{d}$
The density of electrons * the drift velocity.

We can look at a wire with current in the rest frame of the nuclei, in which case the electrons are flowing in the direction opposing current. A single electron outside the wire would experience a force
$$
\begin{align}
\vec{F}_{b}=q\vec{v}\times  \vec{B} \\
\vec{B}=\frac{\mu_{0}i}{2\pi r} \\
i=ja=\rho vA \\
F_{b}=\frac{e\mu_{0}\rho v^{2}A}{2\pi r}(-\hat{y})
\end{align}
$$
If we change our frame to have the electrons stationary, so there is no magnetic force. 
$$
\begin{align}
\vec{F}_{b} & =-e\vec{v}\times  \vec{B} \\
 & =0
\end{align}
$$
If we don't have a magnetic field, we are forced to conclude that there is an electric field, which is causing a force on the electron equal to what we see in the other rest frame.

Remember back to special relativity. In the frame where the electrons are moving, the length is L. In the frame where electrons are stationary, the distance between electrons is $\gamma L$, whereas the distance between nuclei is $\frac{L}{\gamma}$.
We can now look at the charge densities.
$$
\begin{align}
\rho_{+}=\rho_{-} \\
\rho_{+}'>\rho_{-}' \\
\rho_{+}'=\frac{Q}{\frac{Al}{\gamma}}=\gamma \rho_{+}=\gamma \rho_{-} \\
\rho_{-}'=\frac{Q}{A\gamma L}=\frac{1}{\gamma}\rho_{-} \\
\end{align}
$$
Which gives us the result 
$$
\begin{align}
\rho'_{tot} =\rho'_{+}-\rho'_{-} \\
=\gamma \rho_{-}-\frac{1}{\gamma}\rho_{-} \\
\rho'_{tot} =\frac{\gamma v^{2}}{c^{2}}\rho_{-}>0
\end{align}
$$
In the rest frame of the electrons, we can use gauss's law.
$$
\begin{align}
∯\vec{E}'\cdot d\vec{A}'=\frac{Q'enc}{\epsilon_{0}}
\end{align}
$$
We can say by symmetry that the electric field can only depend on $r$ and point in the $\hat{r}$ direction.
We can draw a cylinder around the wire.
$$
\begin{align}
E'(r')(2\pi r' l')=\frac{\rho_{_{tot} }l'A}{\epsilon_{0}} \\
r'=r \\
E'(r)=\rho'_{tot} \frac{A}{2\pi r\epsilon_{0}} \\
=\frac{\gamma v^{2}\rho_{-}A}{2\pi r\epsilon_{0}c^{2}}
\end{align}
$$
So the electric force in the primed frame is
$$
\begin{align}
\vec{F}_{e}'=\frac{\gamma ev^{2}\rho_{-}A}{2\pi r\epsilon_{0}c^{2}}(-\hat{y})
\end{align}
$$
We have to transform the forces to be in the same frame so that we can compare them.
$$
\begin{align}
F_{y}=\frac{1}{\gamma}Fy'
\end{align}
$$
so we get 
$$
\begin{align}
\vec{F}_{e} & \stackrel{?}{=}   \vec{F}_{b}\\
\frac{ev^{2}\rho_{-}A}{2\pi r\epsilon_{0}c^{2}}(-\hat{y}) & \stackrel{?}{=}  \frac{e\mu_{0}\rho_{-}v^{2}A}{2\pi r}(-\hat{y}) \\
\mu_{0} \, \, \, \frac{ev^{2}\rho_{-}A}{2\pi r}(-\hat{y}) & \stackrel{?}{=}  \frac{1}{\epsilon_{0}c^{2}}\, \, \,\frac{ev^{2}\rho_{-}A}{2\pi r}(-\hat{y})   \\
\mu_{0}=\frac{1}{\epsilon_{0}c^{2}} \\
\text{ plug in values, we} & \text{  get that this is true! }
\end{align} 
$$

## Electric and magnetic fields are not two entirely separate things, but aspects of a single phenomenon - ELECTROMAGNETISM!
