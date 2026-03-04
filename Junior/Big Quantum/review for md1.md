$$
\begin{align}
\ket{+y} = \ket{+z} + i \ket{-z}    
\end{align}
$$




$$
\begin{align}
S_{z} =  
\end{align}
$$



$$
\begin{align}
\hat{A}\hat{C}+\hat{A}\hat{B}+\hat{B}\hat{C}+\hat{B}^{2}  \\
B^{2}= CA-AC  \\
AB+BC+CA
\end{align}
$$
We know that
AB-BA = -CA
AB = BA-CA

$BC+BA$
B(A+C)  0

# time
$$
\begin{align}
\hat{H}=\omega_{0}(\hat{S}_{1x}-\hat{S}_{2z}  )
\end{align}
$$
We can write out the eigenvalues
$$
\begin{align}
\hat{H} \ket{+x,+z} = 0 \\
\hat{H} \ket{+x,-z} = \hbar \\
\hat{H} \ket{-x+z} = \hat{h} \\
\hat{H} \ket{-x-z} = 0    
\end{align}
$$
$$
\begin{align}
\ket{0,0} = \frac{1}{\sqrt[]{ 2 } }(\ket{+z,-z} + \ket{-z,+z}  ) 
\end{align}
$$
We can translate $x$ into the z basis as
$$
\begin{align}
\ket{+x} = \frac{1}{\sqrt[]{ 2 } }(\ket{+z} +\ket{-z} ) \\
\ket{-x} = \frac{1}{\sqrt[]{ 2 } }(\ket{+z} -\ket{-z} ) 
\end{align}
$$
So
$$
\begin{align}
\ket{+z} = \frac{\sqrt[]{ 2 }}{2}(\ket{+x} + \ket{-x} ) 
\end{align}
$$

We time evolve with the generators as


$$
\begin{align}
\ket{0,0} = \frac{1}{2}\left( \, \, \left( \ket{+x}+\ket{-x}   \right) \ket{-z} - (\ket{+x} -\ket{-x} )\ket{+z} \, \,  \right) \\
\frac{1}{2}(\ket{+x}\ket{-z} +\ket{-x} \ket{-z} - \ket{+x}\ket{-z} +\ket{-x} \ket{+z}  ) \\
\end{align}
$$


We can now time evolve with the spins
$$
\begin{align}
e^{-i \omega_{0} }\ket{+x}\ket{-z} + e^{0}\ket{-x}\ket{-z} + e^{0}\ket{+x} \ket{+z}   +e^{i\omega_{0}}\ket{-x} \ket{+z} 
\end{align}
$$

$$
\begin{align}
\frac{1}{4} (e^{-i\omega_{0}t}+e^{i\omega_{0}t}+2) = 1 \\
\frac{1}{2}(\cos(\omega_{0}t)+1)=1 \\
\cos \omega_{0}t = 1
\end{align}
$$
$$
\begin{align}
t = \frac{2\pi}{\omega_{0}}
\end{align}
$$

# Spin

We can evolve
$$
\begin{align}
e^{-\frac{i}{\hbar} \phi \hat{j} } \ket{+z} \otimes  e^{\frac{-i}{\hbar} \theta \hat{i} } \ket{-z}  + e^{-\frac{i}{\hbar} \phi \hat{j} } \ket{-z} \otimes  e^{\frac{-i}{\hbar} \theta \hat{i} } \ket{+z}
\end{align}
$$
