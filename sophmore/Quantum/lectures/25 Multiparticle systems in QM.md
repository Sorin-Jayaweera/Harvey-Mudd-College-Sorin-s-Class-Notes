Review:

We have 4 quantum numbers that give a full description of an electron's state in a hydrogenic atom:
$$
\begin{align}
H_{op}   & & n, \\
 \vec{L}^{2}_{op}   & & l, \\
 L_{z_{op} }   & & m_{l} , \\
 S_{z_{op} } &   & m_{s} 
\end{align}
$$
With 
$$
\begin{align}
\psi = \sum_{n,l,m_{l} m_{s}}^{\infty}  c_{n,l,m_{l},m_{s}  } R_{n,l} (r)Y_{l,m_{l} } (\theta,\phi)\chi_{m_{s} } e^{-iE_{n} t/\hbar}  
\end{align}
$$

Lets step it up to helium.

The two particle operator is the sum of the two Hamiltonians for each individual electron, where there is no interaction between the electrons (this is a lie, but to start simply).

$$
\begin{align}
H_{op} = -\frac{\hbar}{2m_{1}} \frac{ \partial^{2} }{ \partial x_{1}^{2} } + V(x_{1})-\frac{\hbar}{2m_{1}} \frac{ \partial^{2} }{ \partial x_{2}^{2} } + V(x_{2})
\end{align}
$$

We need to solve the TISE:
$$
\begin{align}
H_{op} \Psi (x_{1},x_{2}) = E\Psi (x_{1},x_{2})
\end{align}
$$

Our $\Psi(x_{1},x_{2})$ represents the probability that particle 1 is in $[x_{1},x_{1}+dx_{1}]$ and that particle 2 is in $x_{2},x_{2}+dx_{2}$
The only way that this works is if the total probability is $1$.

$$
\begin{align}
dP = \left| \Psi (x_{1},x_{2}) \right| ^{2}dx_{1}dx_{2}
\end{align}
$$
$$
\begin{align}
\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} dP =1
\end{align}
$$

Because we are ignoring the interaction between electrons, we can just do separation of variables.
$$
\begin{align}
\Psi(x_{1},x_{2}) = \rho(x_{1})\phi(x_{2})
\end{align}
$$
We plug this in, do the math, and get two ordinary differential equations:
$$
\begin{align}
-\frac{\hbar^{2}}{2m_{1}} \frac{ d ^{2}}{d x_{1}^{2} } \rho(x_{1}) + V(x_{1})\rho(x_{1}) = E_{1}\rho(x_{1}) \\

-\frac{\hbar^{2}}{2m_{2}} \frac{ d ^{2}}{d x_{2}^{2} } \phi(x_{2}) + V(x_{2})\phi(x_{2}) = E_{2}\phi(x_{2})
\end{align}
$$

$$
\begin{align}
\Psi_{n_{1},n_{2}}(x_{1},x_{2}) = \psi(n_{1})(x_{1})\psi)n_{2} (x_{2}), E=E_{n_{1}} +E_{n_{2}}  
\end{align}
$$

Perhaps an example may be helpful. 

Consider 2 non interacting particles in an infinite square well. What are the non interacting eigenstates?
$$
\begin{align}
\psi_{n_{1},n_{2}} (x_{1},x_{2})=\frac{2}{L} \sin\left( \frac{n_{1}\pi}{L}x_{1} \right)\sin\left( \frac{n_{2}\pi}{L}x_{2} \right) \tag{1}
\end{align}
$$

The energy eigenvalue would be
$$
\begin{align}
E_{n_{1},n_{2}}= \frac{\hbar^{2}\pi^{2}}{2l^{2}} \left( \frac{n_{1}^{2}}{m_{1}}+\frac{n_{2}^{2}}{m_{2}} \right)
\end{align}
$$
## Identical particles

In quantum mechanics, identical particles are not distinguishable, which leads us to super conductivity, bosons and fermions, etc. 

The wave function for particles 1 and 2 should be identical, but we can't  measure the exact wave function. Instead, we have
$$
\begin{align}
\left| \Psi (x_{2},x_{1}) \right| ^{2} = \left| \psi(x_{1},x_{2}) \right| ^{2}
\end{align}
$$
This means that there could be a phase factor between the two. 
$$
\begin{align}
\psi(x_{2},x_{1})= e^{i\delta}\psi(x_{1},x_{2})
\end{align}
$$
This is kind of weird - with equation 1, we would notice if we swapped $x_{1}\text{ and } x_{2}$, since they have different $n_{1}\text{ and } n_{2}$. 


We define
## Exchange Operator
$$
\begin{align}
P_{1,2} \psi_{\text{ identical }} (x_{1},x_{2}) = \Psi_{\text{ identical }}  (2,1) = e^{i\delta}\Psi_{\text{ identical }}  (1,2)
\end{align}
$$
This is an eigen equation, with $e^{i\delta}$ as the eigenvalue.
$$
\begin{align}
P^{2}_{1,2} \psi_{\text{ identical }} (x_{1},x_{2}) = e^{2i\delta} \psi(x_{1},x_{2}) = \psi_{\text{ identical }} (x_{1},x_{2}) \\
(e^{i\delta})^{2}=1 \implies e^{-\delta}= \pm  1
\end{align}
$$
We have two options:

$$
\begin{align}
P_{1,2} \Psi_{\text{ identical }} (x_{1},x_{2}) = + \Psi_{\text{ identical }} (1,2)  & \text{ symmetric under exchange } \\
P_{1,2} \Psi _{\text{ identical }}(1,2)= -\Psi (x_{1},x_{3} )  & \text{ anti-symmetric  }  
\end{align}
$$
Any pair of identical particles has to be symmetric or anti-symmetric. 

Lets look at some examples:

$$
\begin{align}
\Psi (x_{1},x_{2}) = \psi_{\alpha}(x_{1})\psi_{\beta}(x_{2})
\end{align}
$$
We could write out the symmetric example
$$
\begin{align}
\Psi_{s} (x_{1},x_{2}) = \frac{1}{\sqrt[]{ 2 } } \left( \psi_{\alpha} (x_{1})\psi_{\beta} (x_{2}) + \Psi _{\beta} (x_{1})\Psi _{\alpha} (2) \right) 
\end{align}
$$
We can see that if we were to swap the $x_{1}$ and $x_{2}$.

If we want the antisymmetric property, we just change this to be a $-1$:
$$
\begin{align}
\Psi_{s} (x_{1},x_{2}) = \frac{1}{\sqrt[]{ 2 } } \left( \psi_{\alpha} (x_{1})\psi_{\beta} (x_{2}) - \Psi _{\beta} (x_{1})\Psi _{\alpha} (2) \right) 
\end{align}
$$
We saw states like this before when looking at entanglement. When we have a superposition of products of single particle states, we have entanglement. When we have an antisymmetric state, we definitely have entanglement. For the symmetric, they are entangled unless they are in the same state. 

It turns out that particles with integer spin, i.e. with $s= 0,1,2$ are in the symmetric state. Particles with half integer spins are in anti-symmetric states. $S=\frac{\frac{1}{2},3}{2},\dots$  electrons, protons, neutrinos, Fermions. To prove this needs QED, so we won't do it here.

## Pauli exclusion principle
We can prove this:
Fermions must be in an antisymmetric state. If we try to put them in the same state, we would have 

$$
\begin{align}
\Psi_{s} (x_{1},x_{2})  & = \frac{1}{\sqrt[]{ 2 } } \left( \psi_{\alpha} (x_{1})\psi_{\alpha} (x_{2}) - \Psi _{\alpha} (x_{1})\Psi _{\alpha} (2) \right)  \\
 & =0
\end{align}
$$
The Pauli exclusion principle is a corollary of the fact that identical particles are eigenstates of the exchange operator. 

## More particles
The symmetric condition is easy, we just add every permutation of states for each particle. For the antisymmetric state, we have to subtract off things but it looks just like a determinant. 

![[Pasted image 20250326104323.png|400]]

## Helium
Lets actually write this out for helium, and ignore the interactions between the electrons. 

$$
\begin{align}
H_{he} = -\frac{\hbar^{2}}{2m}\nabla^{2}_{1} - \frac{2e^{2}}{4\pi\epsilon_{0}r_{1}} - \frac{\hbar^{2}}{2m}\nabla_{2} ^{2} - \frac{2e^{2}}{4\pi\epsilon_{0}r_{2} } \cancelto{ 0 }{ + \frac{e^{2}}{4\pi\epsilon_{0} \left| \vec{r_{1}}-\vec{r_{2}} \right| }  }
\end{align}
$$
Ignoring the interaction makes this bad unless electrons are far away, but its still a useful result.

In general our states for the two particles can be written by introducing a new variable, the spatial part 

$$
\begin{align}
\psi(x_{1},x_{2}) = \underbrace{ \Phi(\vec{r_{1}},\vec{r_{2}}) }_{ \text{ spatial } } \underbrace{ \mathbf{X}(x_{1},x_{2}) }_{ \text{ spin } }
\end{align}
$$

EX for spatial, $\psi_{10 0}(\vec{r_{1}})\psi_{200}(\vec{r_{2}})$ or a superposition.
EX for spin, $\chi_{+}(x_{1})\chi_{+}(x_{2})$, or a superposition.

Overall, we know that the overall state $\Psi(x_{2},x_{1})=-\Psi(x_{1},x_{2})$, since electrons are fermions. 
We can achieve that by having a symmetric spatial part with an antisymmetric spin, or vice versa. 

Our options:
$$
\begin{align}
\Psi (x_{1},x_{2}) = \Phi_{s} (x_{1},x_{2}) \mathbf{X}_{A} (x_{1},x_{2}) \\
\text{ or } \\
\Psi (x_{1},x_{2}) = \Phi_{A} (x_{1},x_{2})\mathbf{X}_{s}(x_{1},x_{2}) 
\end{align}
$$

The ground state has $n=1$ which is symmetric, so the spin state must be antisymmetric. 

The first excited state is more interesting. 
![[Pasted image 20250326105221.png]]
We have 3 symmetric spin states, and only 1 anti symmetric spin state. We have 1 symmetric and 1 antisymmetric spatial state. 

The particles could occupy the same location with different spins, or different areas with symmetric spins. 

![[Pasted image 20250326105346.png]]

This is the origin of antiferromagnetism.

![[Pasted image 20250326105410.png]]

What about lithium? We have to have the n=1 n=2 state. The classic chemistry diagram has antisymmetric 


![[Pasted image 20250326105544.png]]