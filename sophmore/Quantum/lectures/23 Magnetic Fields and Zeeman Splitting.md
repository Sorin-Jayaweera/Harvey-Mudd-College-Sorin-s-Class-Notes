![[Pasted image 20250314100751.png]]
u

The probability current is proportional to the imaginary components.
the $R_{m,l}$ we set to be real, and $Y_{l,ml}(\theta, \phi)$ is real for all the $\theta$ and only imaginary with the $\phi$ parts. 
$$
\begin{align}
 & \vec{j} \propto \frac{\hbar}{m} \mathrm{Im}\left( \frac{e^{-im_{l} \phi}1}{r\sin\theta}\underbrace{ \frac{ \partial  }{ \partial \phi } e^{im_{l} \phi}  }_{ im_{l}  }\right)\hat{\phi} \\
 & \propto \frac{\hbar}{mr\sin\theta} \mathrm{Im}\left\{ im_{l} \hat{\phi} \right\}  \\
 & \hat{j}\propto \frac{\hbar m_{l} \hat{\phi}}{mr\sin\theta}\neq  0 & \text{ if }  m\neq  0
\end{align}
$$

Now a question:
## How do magnetic fields affect the hydrogen(ic) atom
Lets talk about the Zeeman effect!

In the classical picture: $e^{-}$ in a hydrogen atom.
We have the wrong and misleading picture of an electron orbiting at a radius $r$ with velocity $v$. This looks like a magnetic dipole - we have current flowing in a circle (remember from E&M). 

Current is the amount of charge that goes by in unit time
$I= \frac{q}{t}$ with an orbital period $\frac{2\pi r}{v}$. We know the area is $\pi r^{2}$.
The magnitude of the dipole moment $\mu=ia=\frac{qv}{2\pi r}\pi r^{2}$
$\mu= \frac{qvr}{2}$.

We can rewrite this nicely with classical Angular momentum $L=rmv$ 
$\mu=\frac{q}{2m}L$.

What happens when we apply a magnetic field to this classical point charge moving in a loop.

![[Pasted image 20250314102929.png|300]]
We have a Magnetic energy $-\vec{\mu}\cdot \vec{B}$
$$
\begin{align}
E_{b} = -\frac{q}{2m} \vec{L}\cdot \vec{B} \\
\text{ let } \vec{B} = B\hat{k} \\
E_{b} = -\frac{qB}{2m}L_{z} = \frac{eB}{2m}L_{z} 
\end{align}
$$

What is the Hamiltonian?

## Hamiltonian in a $\vec{B}$ Field
We convert this energy to write out our Hamiltonian.
$$
\begin{align}
H_{op} = \underbrace{ -\frac{\hbar^{2}}{2m}\nabla^{2} - \frac{e^{2}}{4\pi\epsilon_{0}r} }_{ h_{op} \text{  old } } + \underbrace{ \frac{eB}{2m}L_{z_{op} } }_{ h_{op} \text{ new } }  
\end{align}
$$

We can see that the operators commute
$$
\begin{align}
[H_{op,old} , L_{z_{op}} ] = 0 \\
\left[ H_{op} ^{B},L_{z_{op} }  \right] =0  
\end{align}
$$
$$
\begin{align}
H_{op} \Psi =E\psi \Leftrightarrow  Y_{n,l,m_{l} } =R_{n,l} Y_{l,m_{l} } 
\end{align}
$$
What are the eigenvalues?

When we operate on the old Hamiltonian, we just get the old eigenvalues.
On the new part of the Hamiltonian we have
$$
\begin{align}  
L_{z_{op} } Y_{n,l,m_{l} } = (l_{l} \hbar)\psi_{n,l,m_{l} } 
\end{align}
$$We have
$$
\begin{align}
E = \underbrace{ E_{n} }_{ \text{ old eigenvalues } } + \frac{eB}{2m}(m_{l} \hbar) 
\end{align}
$$
We define the Bohm magnetron (also using $\mu$ unfortunately)
$\mu_{b}=\frac{e\hbar}{2m} \approx 5.79\times 10^{-5} \frac{eV}{T}$
$E=E_{n}+\mu_{b}m_{l}B$
Last time we found that $E_{n}= -13.5 \frac{eV}{n^{2}}$
