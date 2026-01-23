Imagine a wave function with probability amplitude $P=\left| \psi \right|^{2}$. The wave function evolves over time. 

Every observable is associated with some operator, labeled with $\hat{A}$. 
$\left< \hat{A} \right>$ is the average over many measurements.
$$
\begin{align}
\left< \hat{A}  \right>   = \int \psi ^{*}(x,t) \hat{A} \psi(x,t)dt
\end{align}
$$

## Comparing formalisms
### Schrödinger Picture
Operators are fixed, but the wavefunction evolves in time.

These are things like the position, momentum, and energy operators: $\hat{x},\hat{p},\hat{H}$. $\Psi$ evolves in time. 

The Schrödinger equation tells us how $\psi$ evolves with time. 

$$
\begin{align}
i\hbar \frac{ \partial \psi }{ \partial x }  & = \hat{H}\psi, \\
\hat{H} &  = \frac{-\hbar^{2}}{2m} \frac{ \partial^{2} }{ \partial 2m } + V(x) 
\end{align}
$$
### Heisenberg Picture
If we solve the Schrödinger equation with separation of variables, we see that we have solutions
$$
\begin{align}
\psi(x,t) = \psi(x,0) e^{\frac{iHt}{\hbar}}
\end{align}
$$
We can write the average of an arbitrary operator $\hat{A}$ as
$$
\begin{align}
\left< \hat{A} \right>  = \int \psi ^{*}(x,0)\underbrace{  e^{\frac{iHt}{\hbar}}\hat{A} e^\frac{-iHt}{\hbar} }_{ \hat{A}(t) }\psi(x,0)
\end{align}
$$
$\psi = \psi(x,0) = \text{ constant in time }$, but the operators evolve in time. 

So we could have operators $\hat{x}(t)$.

### Classical Mechanics
We wouldn't even thing about observables or not, but to put them in the same language: Observables in classical mechanics $A$ are just numbers, not operators. They are just coordinates, like position or momentum, or functions of coordinates (energy is an observable function of $x$ and $t$). 

### Quantum Mechanics
Observables $\hat{A}$ are operators. 



## Poisson Brackets

Poisson brackets are a classical object.

for any observable $A = f(q_{i},p_{i},t)$ and $B=(q_{i},p _{i},t)$, we have a Poisson bracket
$$
\begin{align}
\left\{ A,B \right\}  = \sum_{i}^{}\left(  \frac{ \partial A }{ \partial q_{i} } \frac{ \partial B }{ \partial p _{i} } - \frac{ \partial B }{ \partial q_{i} } \frac{ \partial A }{ \partial p _{i} }  \right)
\end{align}
$$
We can build a really nice formalism (Lie Algebra) by considering the space of these functions together. 

The simplest that are not very interesting for functions over phase space is to say that $A$ is a coordinate (i.e. y, z)
$$
\begin{align}
\left\{ q_{j},q_{k} \right\} = \sum_{i}^{} \frac{ \partial q_{j} }{ \partial q_{i} } \frac{ \partial q_{k} }{ \partial p _{i} } - \frac{ \partial q_{k} }{ \partial q_{i} } \frac{ \partial q_{j} }{ \partial p _{i} } 
\end{align}
$$
If something is only a function of position and momentum, 
$$
\begin{align}
\frac{ \partial q_{k} }{ \partial q_{i} } = \frac{ \partial q_{j} }{ \partial p _{i} } = 0
\end{align}
$$

Similarly,
$$
\begin{align}
\left\{ p_{j},p_{k} \right\}  = 0
\end{align}
$$

Lets do more interesting ones.

What if we took
$$
\begin{align}
\left\{ q_{j},p_{k} \right\}  & = \sum_{i}^{} \frac{ \partial q_{j} }{ \partial q _{i} } \frac{ \partial p_{k} }{ \partial p _{i} } - \cancelto{ 0 }{ \frac{ \partial p_{k} }{ \partial q_{i} } \frac{ \partial q_{j} }{ \partial p _{i} } U } \\
 & = \sum_{i}^{}  \delta _{ij}\delta_{ik}  \\
\end{align}
$$
$$
\boxed{
\begin{align}
\left\{ q_{j},p_{k} \right\} & = \delta _{jk} 
\end{align}
}
$$


Lets let 
$$
\begin{align}
A = (q_{i},\dots,q_{n},p_{1} ,\dots,p_{n},t)
\end{align}
$$
We can take
$$
\begin{align}
\frac{ d A}{d t }  = \frac{ \partial A }{ \partial t } + \sum_{i=1}^{n} \frac{ \partial A }{ \partial q_{i} } \dot{q_{i}} + \frac{ \partial A }{ \partial p _{i} } \dot{p_{i}}
\end{align}
$$



Taking Hamilton's equations, we know that
$$
\begin{align}
\dot{q_{i}}= \frac{ \partial H }{ \partial p_{i} } \\
\dot{p}_{i} = -\frac{ \partial H }{ \partial q_{i} }  
\end{align}
$$
We'll get
$$
\begin{align}
\sum_{i=1}^{N} \left(  \frac{ \partial A }{ \partial q_{i} } \frac{ \partial H }{ \partial \pi i } - \frac{ \partial A }{ \partial p_{i} }\frac{ \partial H }{ \partial q_{i} }   \right) + \frac{ \partial A }{ \partial t } 
\end{align}
$$

We found that
$$
\boxed{
\begin{align}
\frac{ d A}{d t } = \left\{ A,H \right\} + \frac{ \partial A }{ \partial t } 
\end{align}
}
$$


What if we want to think about infitesimal transformation that are rotations?

We would find that Transformations that are rotations by $d\phi$ around $z$ lead to
$$
\begin{align}
dA = \left\{ A,L_{z}  \right\} d\phi
\end{align}
$$
The Hamiltonian is the infinite generator of time translation, and the angular momentum is the infinite generator of rotations. 
$$
\begin{align}
\left\{ L_{x} ,L_{y}  \right\}  & = L_{z} \\
\left\{ L_{y},L_{z}   \right\}  & = L_{x}    \\
\left\{ L_{z} ,L_{x}  \right\}  & = L_{y} 
\end{align}
$$

## Commutators

Similar to Poisson brackets, but for operators in Quantum mechanics.

The commutator
$\bigg[ \hat{A},\hat{B} \bigg]= \hat{A}\hat{B}-\hat{B}\hat{A}$
$$
\begin{align}
[\hat{q}_{j} ,\hat{p}_{k}  ] = i\hbar \delta _{ij} \\
[L_{x} ,L_{y} ]= i\hbar L_{z} 
\end{align}
$$

We have Ehrenfest's theorem:
$$
\begin{align}
\frac{ d \left< \hat{A} \right>  }{d t } = \frac{1}{i\hbar} \left< [\hat{A},\hat{H}] \right>  + \frac{ \partial \left< \hat{A} \right>   }{ \partial t } 
\end{align}
$$
Classical is derivable as a macroscopic limit. It makes sense that the same theories - quantum and classical - observe the same types of structures. 

For instance, $[\hat{A},\hat{B}]=-[\hat{B},\hat{A}]$, which is the same for Poisson brackets.
$$
\begin{align}
[\hat{A},[\hat{B},\hat{C}]] + [\hat{B},[\hat{C},\hat{A}]] + [\hat{C},[\hat{A},\hat{B}]] = 0
\end{align}
$$



Lets think about the Least Action Principle, where we have different paths from points $A$ and $B$, where we calculate the action for any path $S$ and minimize that function. 

We can think about multiple paths interfering with each other. 

## Quantum Optics
In a quantum theory of photons, we had to calculate probability amplitude 
$$
\begin{align}
z = \sum_{\text{ all paths j }}^{} e^{i\overbrace{ k dj}^{ \phi }}
\end{align}
$$
where the phase $\phi _{j} = kd_{j} = \frac{2\pi d_{j}}{\lambda}$

Maybe we can break this down into little tiny pieces of the path for photons traveling along a path at speed $c$

$$
\begin{align}
d_{j}  = \int d(d_{j} ) = \int_{\text{ along path j }} c \,  & dt
\end{align}
$$
$$
\begin{align}
z  & = \sum_{\text{ all paths }}^{} exp\left[  i \int_{\text{ along path j }}^{} \frac{2\pi}{\lambda} c \, dt \right] \\
  & = \sum_{\text{ all paths }}^{} exp \left[ i \int\text{ path j }\left( \frac{2\pi}{h} \right)E \,  dt \right]
\end{align}
$$
We have
$$
\begin{align}
\sum_{\text{ paths }}^{} exp\left[  \frac{i}{\hbar} \int_{\text{ path j }} T dt \right]
\end{align}
$$
This derivation is completely bogus, but
$$
\begin{align}
Z = \sum_{\text{ all paths }}^{} e^{i \frac{S_{j}}{\hbar} }
\end{align}
$$
(is the right answer).

This is a very important equation in particle physics to think about probability amplitudes for things that aren't juts photons. 

$$
\begin{align}
z_{j} = e^{i \frac{S_{j}}{\hbar} }
\end{align}
$$
We can draw this in complex space as a phasor, with angle $\phi_{j}$. 

Lets sum up the phasors for every path in the complex plane. If all paths point in the same direction, their probability amplitudes add up constructively. As the phase between paths differs, they each get cranked around, curling around themselves. 


The reason why the path with least action is the best path, by quantum, is that (relative to units of $\hbar$, which has magnitude $10^{-34}$) tiny perturbations make the phasors all cancel out with each other basically always. The only ones that don't are the ones that are basically the same, which only happens at the minimum of. There is no way to get the right answer without adding up the phasors for all other paths... neat. 



