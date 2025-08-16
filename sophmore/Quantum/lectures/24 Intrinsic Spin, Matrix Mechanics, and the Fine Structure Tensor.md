## Review
Eigenstates of $L_{z_{op}}$ and $L^{2}_{op}$

For Orbital angular momentum,
$\left[ L_{z_{op}},L^{2}_{op} \right]=0$, they commute. We saw that for the spherical harmonics we have
$$
\begin{align}
L^{2}_{op} Y_{l,m_{l} } = l(l+1)\hbar^{2} Y_{l,l_{l} }, \, L = 0,1,2,3  \\
L_{z_{op} } Y_{l,m_{l} } = m_{l} \hbar Y_{l,m_{l} }  \, m_{l} = \pm  0, \pm  1\dots\pm  L
\end{align}
$$

We can know one elevation that the angular momentum is on, but can't fully resolve it - instead, it could lie anywhere on a circle of the 3d sphere.

Stern-Gerlach Experiment: 
If we put a magnetic field around an electron, we exert a net upwards torque. The magnetic moment $F_{B}\propto-L_{z}$. We can make use of this to sort particles by their angular momentum. They sent particles through a non uniform magnetic field. If the angular momentum points up, they deflect down (towards N side), and if down then they deflect up. They predicted that we would have 3 bands for l=1. But first, they test the basic case where the particle has $l=0$, and should all land in one spot. BUT! They don't, there are two bands. 

They found that there is another type of spin - intrinsic spin. Instead of just orbital momentum, there is also spin. 

## What is Spin?
Spin angular momentum:
We have the individual components don't commute, but $s_{z_{op}}$ and $s^{2}_{op}$ do commute, so we can have simulations eigenstates.
![[Pasted image 20250324101521.png]]

$$
\begin{align}
\vec{S}^{2}_{op} \chi_{s,m_{s} } = s(s+1)\hbar^{2} \chi _{s,ms} , s = 0, \frac{1}{2}, 1, \frac{3}{2}\dots \\
S_{z_{op} } \chi _{s,ms} = m_{s} \hbar \chi _{s,ms} , m_{s} = 0,\pm  1,\pm  2,\dots,\pm  s  
\end{align}
$$

$s=0$ corresponds to the Higgs boson.
$s=\frac{1}{2}$ corresponds to electrons, muons, neutrinos, protons, quarks, etc.
$s=1$ corresponds to photons.

Note: There is no relationship between spin angular momentum and the 3d world. Everything up until now has been seated in a wave function of some sort, but here we have eigenstates of a thing that don't correspond to coordinates. Where is this vector pointing? 

### Representation
Recall, the infinite square well

We could expand any wave function
$$
\begin{align}
\Psi (x,0)= \sum_{n}^{}C_{n} (0)\psi_{n}  
\end{align}
$$
We had complex number coefficients, and we represented this wavefunction as a vector in an abstract Hilbert space. 
Similarly, for here we have Spin $\frac{1}{2}$ angular momentum eigenstates.
$$
\begin{align}
S=\frac{1}{2} \to   m_{s} = \frac{1}{2} \text{ or }  -\frac{1}{2} \\ 
\end{align}
$$
We can write it with two basis vectors
$$
\begin{align}
\chi_{\frac{1}{2}, \frac{1}{2}} \equiv  X_{+} , S_{z} = +\frac{\hbar}{2} , S^{2} = \frac{3}{4} \hbar^{2}\\
\chi_{\frac{1}{2}, -\frac{1}{2}} \equiv \chi_{-}, S_{z} = -\frac{\hbar}{2}, S^{2} = \frac{3}{4}\hbar^{2}  
\end{align}
$$
These two vectors form a complete basis, so we can write everything as a linear combination of these two states. We define the vector space in this basis as
$$
\begin{align}
\chi_{+} = \begin{pmatrix}
1 \\ 0
\end{pmatrix}, \chi_{-} = \begin{pmatrix}
0 \\ 1
\end{pmatrix} 
\end{align}
$$
Where we have the coefficients for how much of that vector labeled as $c_{+}\text{ and } c_{-}$
We can write a generic state: 
$$
\begin{align}
\chi = c_{+} \chi_{+} + c_{-}\chi_{-}   
\end{align}
$$

Anyways, the big take away - spin operators and spin states are not correlated to position space. But, we can still see some nice things.

If we act with $S_{z_{op}}$ on $\chi_{+}$, we get the eigenvalue $+\frac{\hbar}{2}\chi_{+}$. 
We also want 
$$
\begin{align}
s_{z_{op} } \chi_{-}  = - \frac{\hbar}{2} \chi_{-}  
\end{align}
$$

The proposal is that we can write this as a matrix and vector operation.
$$
\begin{align}
S_{z_{op} } \chi_{-} = -\frac{\hbar}{2}\chi_{-} \\
\downarrow   \\
\begin{pmatrix}
? & 0 \\
? & -\frac{\hbar}{2} 
\end{pmatrix} \begin{pmatrix}
0 \\1
\end{pmatrix} = -\frac{\hbar}{2} \begin{pmatrix}
0\\1
\end{pmatrix}
\end{align}
$$

$$
\begin{align}
S_{z_{op} } \chi_{+}  & = +\frac{\hbar}{2}\chi_{+} \\
 & \downarrow   \\ \begin{pmatrix}
\frac{\hbar}{2}  & ? \\
0 & ?
\end{pmatrix}
 \begin{pmatrix}
1 \\0 
\end{pmatrix}  & = + \frac{\hbar}{2} \begin{pmatrix}
1\\0
\end{pmatrix}
\end{align}
$$
Therefore, we write out
$$
\begin{align}
S_{z_{op} } = \frac{\hbar}{2} \begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
\end{align}
$$

$S_{z}$ is nice: in the basis of $s_{z}$ it is diagonal. $\chi_{+}\text{ and } \chi_{-} \text{ are not eigenstates of }S_{x}$, so if we want to look at others they aren't as nice.
$$
\begin{align}
S_{x_{op} } = \frac{\hbar}{2} \begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix} \\
\text{ in the } \chi_{-} , \chi_{+} \text{ basis }
\end{align}
$$
$$
\begin{align}
s_{y_{op} } = \frac{\hbar}{2} \begin{pmatrix}
0 & -i \\
i & 0
\end{pmatrix}
\end{align}
$$
Fun thing, we can check the total spin operator
$$
\begin{align}
\vec{S}_{op} ^{2} = S^{2}_{x_{op} } +S^{2}_{y_{op} } +S^{2}_{z_{op} } = 3 \frac{\hbar^{2}}{4} \begin{pmatrix}
1 & 0 \\ 0 & 1
\end{pmatrix} \\
= \frac{1}{2} \left( 1+ \frac{1}{2}\hbar^{2} \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \right) 
\end{align}
$$

## Repeated Spin measurements
We send in particles that are a random collection of spin up and down. 
If we measure the ones that are spin down and pass it through a second, they all come through spin down. That makes sense. But what if we change the polarization? If we have the first polarized to only let through ones that are in the $x$ direction, and a second to only let through ones that are in the $z$ direction, what would happen?
![[Pasted image 20250324104210.png]]

### $S_{x_{op}}$ eigenstates: 
If we've only let through the $\chi_{+}$, the only eigenstates are
$$
\begin{align}
S_{x_{op} } \chi_{+} ^{x} = + \frac{\hbar}{2} \chi_{+} ^{x}
\end{align}
$$
If we knew that
$$
\begin{align}
\chi_{+} ^{x}= c_{+} \chi_{+} + c_{-} \chi_{-} \\
P\left( \underbrace{ \chi_{+} }_{ s_{z} = +\frac{\hbar}{2} }  \right) = \left| c_{+}  \right| ^{2} 
\end{align}
$$
We can turn these into matrix equations.
We can write the decomposition of $\chi_{+}^{x}$ in the basis of $\chi_{+}\text{ and } \chi_{-}$ as $\begin{pmatrix}c_{+} \\ c_{-}\end{pmatrix}$

$$
\begin{align}
\frac{\hbar}{2} \begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix} \begin{pmatrix}
c_{+} \\ c_{-} 
\end{pmatrix} = + \frac{\hbar}{2} \begin{pmatrix}
c_{+} \\ c_{-} 
\end{pmatrix} \\
\end{align}
$$
Lets say we have a vector with equal parts in each basis direction, so $c_{+}=c_{-}$. We choose normalized
$$
\begin{align}
\chi_{+} ^{x}= \frac{1}{\sqrt[]{ 2 } } \begin{pmatrix}
1 \\1
\end{pmatrix} \implies P(\chi_{+} )= \frac{1}{2}
\end{align}
$$
Similarly, if we write $\chi_{-}^{x}=\frac{1}{\sqrt[]{ 2 } } \begin{pmatrix}1\\1\end{pmatrix} \implies P(\chi_{+}) = \frac{1}{2}$.

So in the experiment, we would have equal probability of measuring the particles in up and down if we had first filtered to left and right. 



We now have a complete description of an electron in a hydrogenic atom:

![[Pasted image 20250324105009.png]]
We have an additional Hamiltonian given by the coupling between the electrons orbital momentum and its spin - in the electrons rest frame, the proton orbiting causes a magnetic moment.



