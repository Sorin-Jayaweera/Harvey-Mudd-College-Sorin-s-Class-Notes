>[!abstract]+ Recall:
>We saw that spinning charges classically (and quantum mechanically) act like a dipole. Place it in a magnetic field and it experiences a torque. In an inhomogeneous field, they experience a torque AND a force. The stern Gerlach puts a think with spin in an inhomogeneous magnetic field. We saw deflection that is quantized, with two clumps of particles no matter how the detector is oriented. The angular momentum is always measured to be $\pm\frac{\hbar}{2}$.
>We also saw interference phenomena by blocking slits and getting rid of destructive interference. 

Today, we will talk about the linear algebra formalism that will be used to understand every quantum experiment. 

$\ket{+\hat{z}}$ definitely has $S_{z}= \frac{\hbar}{2}$.
$\ket{-\hat{z}}$ definitely has $S_{z}=-\frac{\hbar}{2}$.
The same for $\ket{\pm x}, \ket{\pm y}$ for $S_{x},S_{y}$.

We can represent a state with these as basis vectors. We can draw a unit sphere with angle down from $z$ as $\theta$ and angle around the $xy$ plane as $\phi$. Classically, this would let a vector $\vec{n}$ as
$$
\begin{align}
\vec{n}  & = \sin\theta \cos \phi \vec{i} + \sin\theta \sin \phi \vec{j} + \cos\theta \vec{k}   \\
 \text{ but we can} &  \text{ show that it is equivalent to the complex }\\
\ket{+\vec{n}}  & = \cos \frac{\theta}{2} \ket{+z} + e^{i\phi}\sin \frac{\theta}{2} \ket{-\vec{z}} 
\end{align}
$$
What is surprising is that we can write any spin direction as a linear combination of only two basis vectors. The geometry of this is very different from the geometry of 3-space. 

$$
\begin{align}
\ket{\psi} & = c_{+}\ket{+\vec{z}}+ c_{-}\ket{-\vec{x}} \\
 & = e^{i\chi} (\underbrace{  c_{+}' }_{ \text{ positive and real } }\ket{+\vec{z}} + c_{-}' \ket{-\vec{z}}  )
\end{align}
$$



| Familiar 3d Vectors                                                            | Quantum State Vectors                                                                                                                                                                                                                                                                  | Spin $\frac{1}{2}$ examples                                      |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| $\vec{E}= E_{x}\vec{i}+ E_{y}\vec{j}+e_{z}\vec{k}$                             | Ket: $\ket{\psi}= \sum_{n}^{}c_{n} \ket{a_{n}}$ <br>where $a_{n}$ is the possible measurement results (position, momentum, energy, whatever), and $c_{n}$ are complex numbers with amplitude and phases that are both important. All results from $\sum_{}^{}$ are mutually exclusive. | $\ket{\psi}= c_{+}\ket{+\vec{z}}+ c_{-}\ket{-\vec{z}}$           |
| $\vec{A}\cdot \vec{B}$ is a real number<br>$=A_{x}B_{x}+A_{y}B_{y}+A_{z}B_{z}$ | Bra: $\bra{\psi}$ corresponds to the same physical situation as $\ket{\psi}$. $\bra{\psi}^{\dagger}=\ket{\psi}$.<br>$\bra{\psi}=\sum_{n}^{}c_{n}^{*}\ket{a_{n}}$                                                                                                                       | $\ket{\psi}= c_{+}^{*}\bra{_{\vec{z}}}+c_{-}^{*}\ket{-\vec{z}}$. |
| $\vec{i}\cdot \vec{E}=E_{x}$                                                   | $\left< \phi\|\psi \right> = \text{ complex number }$                                                                                                                                                                                                                                  |                                                                  |
|                                                                                | $\left< a_n\|a_n \right>=1$<br>$\left< a_{n}\|a_{m} \right>=0$ for $m\neq n$<br>                                                                                                                                                                                                       |                                                                  |
|                                                                                | The probability to measure a result $a_{n}$ is<br>$\left\| c_{n} \right\|^{2}= \left\| \left< a_{n}\|\psi \right> \right\|^{2}$<br>$\left\| \left< \psi\|\psi \right> \right\|^{2}= 1=\sum_{n}^{} \left\| c_{n} \right\|^{2}$                                                          |                                                                  |
|                                                                                |                                                                                                                                                                                                                                                                                        |                                                                  |


Lets look at two experiments. 

![[Pasted image 20260123113531.png]]
$$
\begin{align}
\ket{+x}  = c_{+} \ket{+\vec{z}} + c_{-} \ket{-\vec{z}}  \\ 
= e^{-\delta_{+} }\sqrt[]{ \frac{1}{2 } }\ket{+\vec{z}} + e^{i\delta_{-}  }\sqrt[]{   \frac{1}{2}}\ket{-\vec{z}} \\

\left< +z|+x \right> = c_{+} \text{ Prob }\left( S_{z} =+ \frac{\hbar}{2} \right) =\left| \left< +\vec{z}|+\vec{x} \right>  \right| ^{2}  \\
\implies \left| c_{+}  \right|^{2} = C_{+}^{*}C_{+}   \\
\end{align}
$$

so $\ket{+\vec{x}}= e^{i\delta_{+}}\left( \sqrt[]{ \frac{1}{2} } \ket{+\vec{z}}+ \sqrt[]{ \frac{1}{2} }e^{i(\delta_{-} \,- \, \delta_{+})}\ket{-\vec{z}}\right)$

We can choose $\delta_{+}=0$ and $\delta_{-}-\delta_{+}\equiv\delta$
$\ket{+\vec{x}}= \sqrt[]{ \frac{1}{2} }\ket{+\vec{z}}+ \sqrt[]{ \frac{1}{2} }e^{i\delta}\ket{-\vec{z}}$

Similarly for $\ket{-\vec{x}}$, we have
$\ket{-\vec{x}}= \sqrt[]{ \frac{1}{2}  }\ket{+\vec{z}} + \sqrt[]{ \frac{1}{2} }e^{i\delta'}\ket{-\vec{z}}$.


$$
\begin{align}
\left| \left<  {-\vec{x}|+\vec{x}}  \right>  \right|^{2} = 0 \\
\left< {-x | +x}  \right> = 0  \\
\end{align}
$$
We can take the new representation that we just found, changing $\ket{-\vec{x}} \to \bra{-\vec{x}}$.

$$
\begin{align}
\left(\sqrt[]{ \frac{1}{2} }\ket{+\vec{z}}+ \sqrt[]{ \frac{1}{2} }e^{-i\delta'}\bra{-\vec{z}}\right)\left(\sqrt[]{ \frac{1}{2} }\bra{+\vec{z}}+ \sqrt[]{ \frac{1}{2} }e^{i\delta}\ket{-\vec{z}}\right)=0 \\
\frac{1}{2} + \frac{1}{2} e^{i(\delta-\delta')}=0 \\
e^{i(\delta-\delta')}=-1 = e^{i\pi}
\end{align}
$$


Only the relative phases matter, so we can choose $\delta=0$ and $\delta'=\pi$.

![[Pasted image 20260123114915.png]]
This looks the same (just with new variable names)
$$
\begin{align}
\ket{+\vec{x}} = \sqrt[]{  \frac{1}{2} } \ket{+z} + \sqrt[]{ \frac{1}{2} } e^{i\delta}\ket{-\vec{z}}  \\
\ket{+\vec{y}} = \sqrt[]{ \frac{1}{2} } \ket{+\vec{z}} + \sqrt[]{ \frac{1}{2} }  e^{i \gamma}\ket{-\vec{z}} 
\end{align}
$$
We have a probability of starting with $\ket{+\vec{x}}$ and getting $\ket{+y}$ is
$\frac{1}{2}= \left| \left< +\vec{y}|+\vec{x} \right> \right|^{2}=\frac{1}{2}[1+\cos(\delta -\gamma)]$

This happens when $\cos$ is zero, so $\frac{\pi}{2}$. 


