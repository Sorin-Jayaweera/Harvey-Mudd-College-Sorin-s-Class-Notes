
Lets put a permanent magnetic field by placing two magnets fairly close together. Lets then give the atoms in the oil a new field, let them align with that, then remove the field and watch them precess. 

![[Pasted image 20260216111853.png|300]]

Lets write out the Hamiltonian. 
Lets take the state
$$
\begin{align}
\ket{\psi(t)}  & \xrightarrow {s_{z} }  \begin{pmatrix}
a(t)\\ b(t)
\end{pmatrix} \\
\ket{\psi(t)}  & = a(t) \ket{\vec{z}} + b(t) \ket{-\vec{z}} 
\end{align}
$$

$$
\begin{align}
\vec{B}  & = \underbrace{ B_{0} }_{ \text{ permanent, big } } \vec{k} + B_{1} \cos\underbrace{  \omega  }_{ 2\pi f }t \vec{i} \\
\hat{H} &  = -\vec{\mu} \cdot \vec{B} = - \frac{gq}{2mc}(\hat{S}_{z} B_{0}+\hat{S}_{x} B_{1}\cos \omega t) \\
 & = \omega_{0} \hat{S}_{z} + \omega_{1} \cos \omega t \hat{S}_{x} \\
\xrightarrow {S_{z} } i\hbar \begin{pmatrix}
\dot{a} \\ \dot{b} 
\end{pmatrix}  & = \frac{\hbar}{2} \begin{pmatrix}
\omega_{0} & \omega_{1} \cos \omega t \\
\omega_{1}\cos \omega t & -\omega_{0}
\end{pmatrix} \begin{pmatrix}
a\\ b
\end{pmatrix}
\end{align}
$$




