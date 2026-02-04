
## Questions for Gallicchio
I don't understand why the identity operator is introduced, not the difference between using intermediary states $a_{1} \text{ and }  a_{2}$ that result from the use of the identity operator. Aka, explain this quote:

"
When we do not make a measurement that permits us to distinguish the intermediate states $\ket{a_{1}}$ and $\ket{a_{2}}$, we add the amplitudes and then square to get the probability, while if
we do make a measurement that can distinguish which of the states $\ket{a_{1}}$ and $\ket{a_{2}}$ the particle is in, we add the individual probabilities, not the amplitudes. 
"
## 2.5 Changing Representations

We can use the rotation operator to change to a new basis by rotating the $\ket{+z}$ that we normally see to a $\ket{+x}$
$$
\begin{align}
R^{\dagger}\left( \frac{\pi}{2}\vec{j} \right)\ket{+z} = \ket{+x} 
\end{align}
$$
and can do this on any state $\ket{+n}$ with any phase around any axis. 

Passive rotation: The basis is changed, but we have the same overall thing
Active rotation: We change the thing


S basis:
$$
\begin{align}
\hat{A} \xrightarrow {S_{x} }  = \mathbb{S}^{\dagger} \mathbb{\hat{A}S}
\end{align}
$$
I,e, 
$$
\begin{align}
\mathbb{S} &  = \begin{pmatrix}
\braket{ +z | +x }  & \braket{ +z | -x }  \\
\braket{ -z | +x }  & \braket{ -z | -x }  
\end{pmatrix} \\
 & = \frac{1}{\sqrt[]{ 2 } }\begin{bmatrix}
1 & -1  \\
1 & 1
\end{bmatrix}
\end{align}
$$

## 2.6 Expectation values

$$
\begin{align}
\left< S_{z}  \right> = \left( \frac{\hbar}{2} \right) \left| \braket{ +z | \psi }  \right|^{2} + \left( -\frac{\hbar}{2} \right) \left| \braket{ -z | \psi }  \right| ^{2} 
\end{align}
$$
![[Pasted image 20260201171732.png]]
![[Pasted image 20260201171722.png]]


## 2.7 Photon Polarization

infinite small angle rotations take a pure $x$ to a pure $y$ photon. 

Light acts like a spin $\frac{1}{2}$ particle.

Basis in circular coordinates - right or left hand because easy eigen vectors. Then change basis with matrices.
![[Pasted image 20260201174329.png]]

## 2.8 Summary:

rotations, bases, the identity operator.


"When we do not make a measurement that permits us to distinguish the intermediate states $\ket{a_{1}}$ and $\ket{a_{2}}$, we add the amplitudes and then square to get the probability, while if
we do make a measurement that can distinguish which of the states $\ket{a_{1}}$ and $\ket{a_{2}}$ the particle is in, we add the individual probabilities, not the amplitudes. 