![[Pasted image 20250307102939.png|600]]

We can take the 3d time independent Schrödinger equation and break it into separate components of angular momentum:

$$
\begin{align}
\left[ -\frac{\hbar^{2}}{2mr^{2}}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right) + \frac{\vec{L}^{2}_{op} }{2mr^{2}} + V(r) \right] \psi (r,\theta,\phi)=E \psi (r,\theta,\phi) \\
\psi(r,\theta,\phi)= R(r)\Phi(\phi)\Theta(\theta) \\
\text{ we combine angular momentum } \Theta(\theta)\Phi(\phi) \text{ into } Y(\theta,\phi) \\
L^{2}_{op} Y(\theta,\phi)=L^{2}Y(\theta,\phi)=\lambda \hbar^{2}Y(\theta,\phi)
\end{align}
$$
$L^{2}_{op}$ corresponds to the total angular momentum, its a Hermitian operator (real eigenvalues and equal to its conjugate transpose, has orthogonal eigenfunctions that form a complete set). 

## Eigenfunctions and Eigenvalues of $\vec{L}_{op}^{2}$

$$
\begin{align}
-\frac{\hbar^{2}}{\sin(\theta)} \frac{ \partial  }{ \partial \theta } \left( \sin(\theta)\frac{ \partial  }{ \partial \theta }  \right) Y(\theta,\phi) - \frac{\hbar^{2}}{\sin ^{2}}\frac{ \partial^{2} }{ \partial \phi } Y(\theta,\phi)= \lambda \hbar^{2}Y(\theta,\phi) \\
Y(\theta,\phi)= \Theta(\theta)\Phi_{ml} (\phi) \\
L_{z o p}= \frac{\hbar}{i} \frac{ \partial^{2} }{ \partial \phi^{2}} + \frac{L_{z op}^{2}}{\sin ^{2}\theta} \\
-\frac{\hbar^{2}}{\sin\theta}\Phi_{ml} \frac{ \partial  }{ \partial \theta } \left( \sin\theta \frac{ \partial  }{ \partial \theta } \Theta \right) + L_{z o p} ^{2} \Phi_{ml} \frac{\Theta}{\sin ^{2}\theta} = \lambda \hbar^{2} \Theta \Phi_{ml}     
\end{align}
$$
We know that

$$
\begin{align}
L_{z op} \Phi = (ml \hbar)\Phi_{m l}  
\end{align}
$$
We can cancel components and simplify to get
$$
\begin{align}
-\frac{1}{\sin\theta} \frac{ d  }{ d \theta } \left( \sin\theta \frac{ d  }{ d\theta } \Theta \right) + \left( \lambda- m_{l} \frac{^{2}}{\sin ^{2}\theta} \right)\Theta=0
\end{align}
$$
This is the non partial ordinary differential equation that gives us what $\Theta$ is. This works because $\Phi$ was an eigenfunction of $L_{z op}$. 
$Y(\theta,\phi)=\Theta(\theta)\phi m_{l}(\phi)$.
Different equations and solutions for different $m_{l}$


We can try solving with $m_{l}=0$:
$$
\begin{align}
\frac{1}{\sin\theta}\frac{ d }{d \theta } \left( \sin\theta \frac{ d }{d \theta }  \right) + \lambda\Theta(\theta)=0 \\
\end{align}
$$
We can make a guess at the solution
$$
\begin{align}
\Theta(\theta)=\sum_{k=0}^{\infty} a_{k}\cos ^{k}\theta
\end{align}
$$
Which has a recursion relation
$$
\begin{align}
\frac{a_{k+2}}{a_{k} }= \frac{k(k+1)-\lambda}{(k+1)(k+2)} 
\end{align}
$$
We must have a maximum k value beyond which $a_{k+n}=0$ ![[Pasted image 20250307104239.png|300]]

![[Pasted image 20250307104251.png|300]]


![[Pasted image 20250307104303.png|300]]


![[Pasted image 20250307104322.png|300]]
![[Pasted image 20250317223652.png]]

This is the basis set for any functions that are defined over the surface of the sphere. 

