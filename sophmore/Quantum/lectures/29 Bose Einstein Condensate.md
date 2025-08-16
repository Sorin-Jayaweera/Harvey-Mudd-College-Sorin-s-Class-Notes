
We have a macroscopic number of bosons in their ground state. Having $n$ bosons is not the same as having $\underset{ n }{ 1+1+1\dots+1}$ bosons. 


We have the distribution function
$$
\begin{align}
n_{BE} = \frac{1}{e^{\frac{E-\mu}{k_{B}T}}-1} 
\end{align}
$$
where $\mu$ was a fudge factor that is the chemical potential. 

This is a continuous function, but it is only evaluated at energies where we have a state. It is only meaningful at those energies. 

![[Pasted image 20250407101344.png|300]]

We have the actual energy states that we can evaluate it, and we don't have outside of these discrete points. 
![[Pasted image 20250407101545.png]]

At the chemical potential, the number of particles is diverging (going to infinity), so it has to be below our ground state so that we have a finite number. 

We would expect to have particles in the ground state if the spread is not enough to travel the gap in energy from $E_{0}\to E_{1}$.

This means, for us to be confident that a large number of particles will be in the ground state, we should satisfy. The thermal energy is roughly $k_{B}T$
$$
\begin{align}
k_{B}T \leq  \Delta E = E_{1}-E_{0} = \frac{3\hbar^{2}\pi^{2}}{2mL^{2}}
\end{align}
$$
We define
$$
\begin{align}
T_{0} = \frac{\Delta E}{kb}  \\
T_{0} = \frac{3\hbar^{2}\pi^{2}}{2mk_{b} V^\frac{2}{3}}
\end{align}
$$

For the MIT Bose Einstein Condensate experiment,
$M = M_{na}=23mp$
$V = (15\mu m)^{3}\approx_{3}*1-^{-15}m^{3}$
$T_{0} \approx 1.5*10^{-9}k (1.5nK)$


The actual experiment found the temperature to be 
$T_{bec}\approx 2\times 10^{-6}k (2000nK)$. Woah, that's a huge difference.

What happens at $T_{0}$?

The size of the particle would be the De Broglie wavelength,
$la_{db}=\frac{h}{p}$. The thermal energy $k_{B}T=\frac{p^{2}}{2m}$. 

At $T_{0}$, $\lambda_{dB}= \frac{h}{\sqrt[]{ 2mk_{B}T_{0} }}$
$$
\begin{align}
\lambda_{db} = \frac{h}{\left( 2mk_{b}  \frac{3\hbar^{2}\pi^{2}}{2mk_{b} L^{2}} \right)^{1/2} } \\
\lambda_{db} = \frac{hL}{\sqrt[]{ 3 } \hbar \pi} \\
= \frac{2}{\sqrt[]{ 3 } }L
\end{align}
$$
The DE Broglie wavelength... is larger than the box? 

Maybe we need a gentler restriction on the size of the particles?

## Intuitive picture for the Bose Einstein Condensate
We can think of the particle as a volume. To see overlap in the waves of each particle, we could set the volume of the box = $N(\lambda_{db})^{3}$. (the particles are talking up the volume). 
$$
\begin{align}
\lambda_{db}  = \left( \frac{V}{N} \right)^{1/3} \\
= \frac{h}{\sqrt[]{ 2mk_{B}T_{c}  } } \\
T_{c} \sim \frac{h^{2}}{2mk_{B}} \left( \frac{N}{V} \right)^{\frac{2}{3}}
\end{align}
$$
When we have a lot of particles, $T_{c}\gg T_{0}$.

Note: While their wavefunctions overlap, we aren't including their interactions in the Hamiltonian, since we don't want coulombic interactions. 

## Technical Picture for BEC
$$
\begin{align}
N=\underbrace{ \sum_{}^{} N_{BE} (E_{i} }_{ \text{ all quantum states } } )
\end{align}
$$
$$
\begin{align}
N\approx \int_{0}^{\infty} \underbrace{ (2s+1) }_{ \text{ spin } } \frac{1}{8}\underbrace{ 4\pi r^{2}dr }_{ \text{ octant } } n_{BE} (E(r)) \\
\text{ with a change of variables } \\
N \approx \int_{0}^{\infty} \frac{V(2m)^{\frac{3}{2}}}{4\hbar^{3}\pi^{2}} \frac{\sqrt[]{ E } }{e^{\frac{E-\mu}{k_{B}T}}-1} dE
\end{align}
$$

We're suspicious that this would break down. 

![[Pasted image 20250407104138.png|500]]

We have an improper integral at zero....
(Note that this has 2 unique y axes, but for simplicity to visualize).


The solution: We seperate the ground state

$$
\begin{align}
N= \underbrace{ N_{0} }_{ \text{ \# in gnd state } } + \underbrace{ \int_{E_{0}}^{\infty} \frac{1}{e^{\frac{E-\mu}{k_{B}T}}-1} \frac{V(2m)^\frac{3}{2}}{4\hbar^{3}\pi^{2}}\sqrt[]{ E } dE }_{ \# \text{ excited } }
\end{align}
$$
As an aside, we can estimate $\mu$.
$$
\begin{align}
N_{0} = \frac{1}{e^{\frac{E-\mu_{0}}{k_{B}T}}-1} \\
N_{0} \gg 1 \implies \frac{E_{0}-\mu}{k_{B}T} \ll 1 \\
N_{0} \approx   \frac{1}{\left( 1+ E_{0}-\frac{\mu}{k_{B}T+\dots}-1 \right)}  \\
= \frac{kbT}{E_{0}-\mu} \\
\mu \approx E_{0} - \frac{k_{B}T}{N_{0}} 
\end{align}
$$


