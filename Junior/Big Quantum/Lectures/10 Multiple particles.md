Radio Astronomy and quantum optics connections?
## Multiple particles

Instead of writing out the whole basis for N particles as
$$
\begin{align}
\psi_{1} = a \ket{\hat{z}}  + b \ket{-\hat{z}} \\
\psi_{2} = c  \ket{\hat{z}}  + d \ket{-\hat{z}} \\ \\
\vdots
\end{align}
$$
We can write out the correlations for things. I.e.
$$
\begin{align}
\ket{\psi} = \alpha \ket{\uparrow  ,\uparrow  ,\uparrow  } + \beta \ket{\uparrow  ,\uparrow  ,\downarrow  } + \dots
\end{align}
$$

We cna then make an array for the amplitudes of this
$$
\begin{align}
\begin{bmatrix}
\alpha\\ \beta\\ \vdots
\end{bmatrix}
\end{align}
$$
They don't have to be in the same basis, I'm just writing out every combination of states of all the particles, each in whatever basis it is measured in.

Direct product notation:
$$
\begin{align}
\ket{+\vec{z}}_{1}  \otimes  \ket{+\vec{z}} _{2} = \ket{+\vec{z}_{1},\vec{z}_{2}} = \ket{\vec{z}_{1}},\ket{\vec{z}_{2}}=\ket{1} \xrightarrow {s_{z}s_{z}} = \begin{pmatrix}
1\\0\\0\\0
\end{pmatrix}      
\end{align}
$$
Where we could have other states, i.e. 
$\ket{2}\xrightarrow {s_{z}s_{z}}\begin{pmatrix}0\\1\\0\\0\end{pmatrix}$
etc.
## Operators

Ex 1:
$$
\begin{align}
\hat{S}_{z,1} (\ket{+\vec{z}}_{1}\otimes \ket{+\vec{z}}_{2}   ) \\
= & (\hat{S}_{z_{1}} \ket{+\vec{z}}_{1})\otimes  \ket{+\vec{z}}_{2}  \\
 & = \frac{\hbar}{2} \ket{+\vec{z}}_{1} \otimes  \ket{+\vec{z}}_{2}  
\end{align}
$$

Ex 2:
$$
\begin{align}
\hat{S}_{z}  & = \hat{S}_{z_{1}} + \hat{S}_{z_{2}} \\
\hat{S}(\ket{\uparrow_{1}, \uparrow_{2}} ) & = (\hat{S}_{z_{1}} +\hat{S}_{Z_{2}} )(\ket{\uparrow  }_{1} \ket{\uparrow  }_{2}    )  \\
 & = \underbrace{ \hat{S}_{z_{1}} \ket{\uparrow  }_{1}\ket{\uparrow  }_{2} }_{ \frac{\hbar}{2} }  + \underbrace{ \ket{\uparrow  }_{1} (\hat{S}_{z_{2}} \ket{\uparrow  } _{2} )   }_{ \frac{\hbar}{2} }\\
  & = \hbar \ket{\uparrow_{1}\uparrow_{2}} 
\end{align}
$$
Each component acts individually on its individual ket


## Given a hamiltonian, find eigenstates
$$
\begin{align}
\hat{H} \xrightarrow {sz,sz}  \begin{bmatrix}
\bra{1} \hat{H} \ket{1}  & \bra{1} \hat{H} \ket{2} \dots \\
\vdots
\end{bmatrix}
\end{align}
$$
Lets do an example: $\bra{3}\hat{H}\ket{2}$. Lets take a hamiltonian
$$
\begin{align}
\hat{H} = \frac{2A}{\hbar^{2}} \hat{\vec{S}}_{1}\cdot \hat{\vec{S}}_{2}  
\end{align}
$$


$$
\begin{align}
\bra{3} = \bra{-\vec{z}}_{1} \bra{+\vec{z}}_{2} \\
\ket{2} = \ket{+\vec{z}_{1}} \ket{-\vec{z}} _{2} 
\end{align}
$$
So we have
$$
\begin{align}
\bra{-\vec{z}}_{1} \bra{+\vec{z}}_{2} \frac{A}{\hbar^{2}}(\hat{S}_{1+}\hat{S}_{2-} + \hat{S}_{1-}\hat{S}_{2+} + 2\hat{S}_{1z}\hat{S}_{2}z  )\ket{+\vec{z}_{1}} \ket{-\vec{z}} _{2}  \\
\hat{S}_{\pm  } \ket{j,m} = \hbar \sqrt[]{ j(j+1) - m(m \pm 1 ) } \ket{j,m\pm 1 } 
\end{align}
$$
