## Review: Identical Particles

We have two types of particles
$$
\begin{align}
\begin{bmatrix}
\text{ types: } & \text{ Bosons } & \text{ Fermions } \\
\text{ Spin } & \text{ integer } & \text{ Half-Integer } \\
s & 0,1,2 & \frac{1}{2} \frac{3}{2} , \frac{5}{2} \\
\text{ symmetry } & \Psi (1,2)=\Psi (2,1) & \Psi (1,2)=-\Psi (2,1) \\
\text{ Vibe } & \text{ social } & \text{ antisocial }
\end{bmatrix}
\end{align}
$$

Lets do some problems:
$$
\begin{align}
\Psi (1,2)=\Psi_{\alpha} (1)\Psi _{\alpha} (2)
\end{align}
$$
these would be bosons, since there is symmetry under change. 
$$
\begin{align}
\Psi (1,2)=\Psi_{\alpha} (1)\Psi _{\beta} (2)
\end{align}
$$
This doesn't work, since
$$
\begin{align}
\Psi_{\alpha}(1)\psi_{\beta} (2) \neq  \pm  \Psi _{\alpha}(1)\Psi_{\beta}(2)
\end{align}
$$


![[Pasted image 20250331101356.png]]

What do we do if we have a lot more than 2 particles?

Lets consider the average number of particles in a single particle quantum state with energy $E$.

## Quantum Statistics
when $N\gg 1$, we forget $\Psi$ and instead consider the energy of the occupied and unoccupied states. We track which states are occupied, and for Bosons how occupied they are (bosons are social, so we can have any number in the same state).

We define $n(E)=\text{ average number of particles in a quantum state with energy E }$
We can write the number of particles
$$
\begin{align}
N = \sum_{i}^{} n(E_{i}) \approx \int_{0}^{\infty} n(E)D(E)dE
\end{align}
$$
Where $D(E)$ is the density of states
$$
\begin{align}
D(E)= L^{3} (2m)^{\frac{3}{2}} \frac{\sqrt[]{ E }}{2\hbar^{3}}\pi^{2}
\end{align}
$$


Also note, that 
$$
\begin{align}
E_{tot} = \sum_{i}^{}  E_{i} n(E_{i} ) \approx \int_{0}^{\infty} E \, \, n(E)D(E)dE
\end{align}
$$

The more particles we have, the better this approximation is.

Example:

Consider a one-particle system in a quantum state:
$$
\begin{align}
\Psi  = \frac{1}{\sqrt[]{ 3 } } \psi_{1} (\vec{r})\chi_{+} + \sqrt[]{ \frac{2}{3} } \psi_{2} (\vec{r})\chi_{-} 
\end{align}
$$
where $\psi_{1}(\vec{r})\text{ and } \psi_{2}(\vec{r})$ are the energy eigenfunctions with corresponding eigenvalues $E_{1}\text{ and } E_{2}$. Find $n(E)$.

We have
$$
\begin{align}
n(E_{1})  & =  \left| C_{1}  \right| ^{2}  & =  \frac{1}{3} \\
n(E_{2}) & = \left| c_{2}  \right| ^{2}  & =\frac{2}{3} \\
n(E_{3} ) & = \lvert c_{3}  \rvert ^{2}  & = 0
\end{align}
$$
$$
\begin{align}
n(E_{1})+n(E_{2})=N=1
\end{align}
$$
so we have 1 particle. We will now move on and not hold onto the wavefunction, and have multiple particles at each energy. 

![[Pasted image 20250331102658.png|600]]
Note that this is at zero temperature. 

N is talking about the states, not the energy levels. At far out positions we have high degeneracy, but if it is a fermion only 1 can be in each state.

The highest filled energy, the Fermi energy, is
$$
\begin{align}
E_{f} = \frac{\hbar^{2}}{2m} (3\pi^{2})^\frac{4}{3}\left( \frac{N}{L} \right)^{\frac{2}{3}}
\end{align}
$$
## Temperature
We can relate temperature to degrees of freedom. It is related to the average excess energy that a particle has, $E_{\text{ excess }}\approx k_{b}T$.

Boltzmann's Constant $=1.38*10^{-23} \frac{J}{k}$ (joules per kelvin).

We can also think of temperature as flux. When you put two things with different temperatures together, heat flows from the high $T$ to low $T$. Temperature is only defined in the context of putting things together and seeing what happens. If two things are the same temperature, no heat flows between them. 


Question: Is a degenerate Fermi gas hot or cold?

Temperature is a measure of the capacity of a thing to give away energy, and the degenerate Fermi gas is all at the lowest possible energy states, so cold.


## Constraints of n(E) for T > 0

For 
$$
\begin{align}
0\leq n(E)\leq 1, & (\text{ fermions })
\end{align}
$$
On average, higher energies have fewer particles. $n(E)$ decreases monotonically with the energy $E$. 

$$
\begin{align}
0\leq n(E) \text{ Fermions and Bosons } \\
N = \sum_{i}^{} n(E_{i} ) \approx \int_{0}^{\infty} n(E)D(E)dE
\end{align}
$$

We wave a magic wand and have the distribution functions for Bosons and Fermions.

![[Pasted image 20250331104642.png]]
$\alpha$ is a fudge factor that ensures we have a conservation of particles.


