
We saw before that there is no probability current into a barrier, but there is a chance of finding a particle in the barrier. What if we make the barrier finite and put a lower potential area past the barrier? We have non zero probability in the barrier, so there is a chance of having a transmitted wave on the other side.

![[Pasted image 20250219101233.png|300]]

There is nothing to reflect it in the region $III$ , so there should be no reflected wave in that region. 
$$
\begin{align}
\psi=\begin{cases}
Ae^{ikx}+Be^{-ikx} & I \\
Fe^{\kappa x}+Ge^{-\kappa x} & I I \\
Ce^{ikx}+\cancelto{ 0 }{ D } e^{-ikx} & I I I\\
\end{cases}
\end{align}
$$
The C is a wave traveling right in region $I I I$, and similar stories for the others.

Boundary conditions: The wave function is continuous, differentiable, and has a continuous derivative (we don't have an infinite potential).  
$$
\begin{align}
\psi_{I}(0)=\psi_{I I}(0)  & \implies A+B = F+G\\
\psi_{I}'(0)=\psi_{I I}'(0)  & \implies ik(A-B)=\kappa(F-G)
\end{align}
$$

$$
\begin{align}
\psi_{I}(a)=\psi_{I I}(a)  & \implies Fe^{\kappa a}+Ge^{-\kappa a} & = Ce^{ika}\\
\psi_{I}'(a)=\psi_{I I}'(a)  & \implies \kappa (Fe^{\kappa a}-Ge^{-\kappa a}) & = ikCe^{ika}\\
\end{align}
$$
We'll have reflection at x=0 and x=a. We check region three to see if we measure a particle.

The $k's$ are the same in regions $I \text{ and } I I I$, so the particle has the same 'speed' (classically).

$T = \frac{j_{\text{ transmission (III)}}}{j\text{ incident (I) }}=\frac{\left| C \right|^{2}}{\left| A \right|^{2}}$
With some algebra, we get 
$$
\begin{align}
\frac{A}{C}=\frac{e^{ika}}{2ik \kappa}(k^{2}-\kappa^{2})\sinh(\kappa a) + 2ik \kappa \cosh(\kappa a)
\end{align}
$$
so
$$
\begin{align}
\left| \frac{A}{C} \right| ^{2} = \frac{1}{4\kappa^{2}k^{2}} \left[ (k^{2}-\kappa^{2})^{2}\sinh ^{2}\kappa a+4k^{2}\kappa^{2}\cosh ^{2}\kappa a \right] 
\end{align}
$$
Note our $\sinh \text{ and }  \cosh$ identities:
$$
\begin{align}
\cosh ^{2}-\sinh ^{2}=1 \\
\sinh\theta= \frac{e^{\theta}-e^{-\theta}}{2} \\
\end{align}
$$

We do some algebra,  and get
$$
\begin{align}
T = \left[ 1+\frac{\left( k^{2}+\kappa^{2} \right)}{4k^{2}\kappa^{2}}\sinh ^{2}\kappa a  \right]^{-1}
\end{align}
$$

Woah, that means quantum tunneling.
Lets think about the limits. 
### In the thin barrier limit, 
$$
\begin{align}
\kappa \text{ has units } \frac{1}{\underbrace{ L }_{ \text{ decay length } }}
\end{align}
$$
Lets have a thin barrier with a long decay length, $\kappa a\ll 1$.
We have a Taylor approximation of $\sin \kappa a=\kappa a$
$$
\begin{align}
T \approxeq \left[ 1+ \cancelto{ 0 }{ \frac{(\kappa^{2}+k^{2})^{2}}{4k^{2}\kappa^{2}}(\kappa a)^{2} } \right]  \implies T\approx 1
\end{align}
$$
### The thick barrier limit: 
$\kappa a\gg 1$
$$
\begin{align}
\sinh \kappa a= \frac{1}{2} (e^{\kappa a}-\cancelto{ 0 }{ e^{-\kappa a }}) \\
T = \left[ \cancelto{ 0 }{ 1+ }\frac{\left( \kappa^{2}+k^{2} \right) ^{2}}{4k^{2}\kappa^{2}} \frac{e^{2\kappa a}}{4} \right] \\ \\
 
\end{align}
$$
For a non square barrier, we approximate it as a lot of square barriers and make them small (calculus). We want the probability that it transmits through the whole thing, so multiplying the transmission probabilities for each delta x barrier. Our $\kappa's$ will be defined as a function $\kappa= \frac{\sqrt{ 2m(V(x)-E) }}{\hbar}.$
