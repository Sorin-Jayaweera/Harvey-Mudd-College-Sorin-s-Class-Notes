## Questions for Gallicchio
how is $\ket{\psi}\bra{\psi}$ different from $\bra{\psi}\ket{\psi}$? If its $1\times N$ vs $N\times 1$, we still just end up with one number when doing matrix multiplication? How does the $\ket{+z}\bra{+z} + \ket{-z}\bra{-z}$ multiply out to make the identity? 

## 2.1

We define the adjoint which takes conjugate transpose ( Hermitian?) $^{\dagger}$. This take $\ket{} \to \bra{}$

We introduce the rotation generator operator $\hat{j}$ which takes infitesimal rotations
$$
\begin{align}
\hat{R}(d\phi \mathbf{k}) = 1- \frac{i}{\hbar} \hat{J}_{z} d\phi 
\end{align}
$$
Which is self adjoint, and satisfies
$$
\begin{align}
\hat{R}^{\dagger}(d\phi \mathbf{k})\hat{R}(d\phi \mathbf{k}) = \left( 1+ \frac{i}{\hbar}\hat{J}_{z} ^{\dagger} d\phi \right)\left( 1 - \frac{i}{\hbar}\hat{J}_{z} d\phi \right)
\end{align}
$$
The operator undoes itself when acting with argument angles rotated by $\pi$. 
Taking $N\to \infty$ actions of this $\hat{J}_{z}$ rotation generator, we can deflect by any angle? 

Doing the rotation to make an overall phase doesn't change the state, i.e.
$$
\begin{align}
\hat{J}_{z}\ket{ z } = \ket{z}   
\end{align}
$$

This introduces Eigenkets. 

We have projection operators $\hat{P}_{\pm}$ that compose to make an identity operator.
$$
\begin{align}
\ket{\psi} =( \underbrace{ \ket{+z} \bra{+z} }_{ \hat{P}_{+}  }  + \underbrace{ \ket{-z} \bra{-z} }_{ \hat{P}_{-}  } )\ket{\psi}   
\end{align}
$$

Where each projection finds the component along a vector 
$$
\begin{align}
\hat{P}_{+}\ket{\psi} = \ket{+z}\left< +z|\psi \right>   
\end{align}
$$
This is the component of psi that lies along the $z$ direction for the +z ket. 

Blocking a path in the Modified Stern Gerlach that recombines beams is the same as taking the projection, and just leaving one portion. 

We can write these as matrix representations, so
$$
\begin{align}
\vec{P}_{+}  = \begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}, \vec{P}_{-} = \begin{bmatrix}
0 & 0\\ 0  & 1
\end{bmatrix} 
\end{align}
$$
or the rotation generator 
$$
\begin{align}
\hat{J}_{z}  = \begin{bmatrix}
\frac{\hbar}{2 } & 0 \\
0 & \frac{\hbar}{2 }
\end{bmatrix}
\end{align}
$$

$$
\begin{align} 
\text{ if } \hat{A}\ket{\psi}  & = \phi \\
\left< \chi | \hat{A} | \psi \right>  & = \left< \chi |\phi\right>  \\
\left< \psi|\hat{A}^{\dagger}|\chi \right>  & = \left< \phi|\chi \right> 
\end{align}
$$


