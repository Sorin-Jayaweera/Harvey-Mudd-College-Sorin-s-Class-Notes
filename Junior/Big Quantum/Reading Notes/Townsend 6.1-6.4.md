## Questions for Gallicchio:
na: we defined two operators and generators for position/momentum with uncertainty and commutation. That's a thing we've done a lot of before. 

## Wave functions

We can write $\ket{\psi}$ as a superposition of states

$$
\begin{align}
1= \int dx \left| \braket{ x | \psi }  \right| ^{2}
\end{align}
$$

## Translation operators

We can translate each basis function, making overall time translation. This works the same as time, but its position.
$$
\begin{align}
\ket{x} \hat{T}^{\dagger}= \ket{x+a} 
\end{align}
$$
where $x$ is the $x$ axis, not a spin in $\ket{+x}$.


## Generator of translations
$$
\begin{align}
\hat{T}(dx) = 1- \frac{i}{\hbar} \hat{\rho}_{x} dx
\end{align}
$$
$$
\begin{align}
\hat{T}(dx)\ket{x} = \ket{x+dx} 
\end{align}
$$
As we have infinite tiny steps, we get
![[Pasted image 20260303142325.png]]

We have commutation relations
$$
\begin{align}
[\hat{x},\hat{p}_{x} ] = i\hbar
\end{align}
$$

We have a momentum (non spin) Hamiltonian
$$
\begin{align}
\hat{H} = \frac{\hat{p}_{x}^{2} }{2m }+ v(\hat{x})
\end{align}
$$
Ehrenfest's theorem:
$$
\begin{align}
\frac{ d \left< x \right> }{d t } = \frac{\left< p_{x}  \right> }{m}
\end{align}
$$
$$
\begin{align}
\frac{ d \left< p_{x}  \right> }{d t } = \left< - \frac{dV}{dx} \right> 
\end{align}
$$
motion is not essentially classical as these imply though.

$$
\begin{align}
\Delta x \Delta p_{x}\geq \frac{\hbar}{2} 
\end{align}
$$

## Momentum operator
$$
\begin{align}
\bra{x} \hat{p}_{x} \ket{\psi} = \frac{\hbar}{i} \frac{ \partial  }{ \partial x } \braket{ x | \psi } 
\end{align}
$$

