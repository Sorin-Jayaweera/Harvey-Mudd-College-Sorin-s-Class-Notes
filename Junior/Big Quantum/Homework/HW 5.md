Collaborators:
Annika Larson
Cameron Warmerdam
Ian Mcguire

![[Pasted image 20260225191800.png]]

## 5.30 A
$$
\begin{align}
\ket{1,1}  = \ket{+z,+z} 
\end{align}
$$
We have the projection operator to get four coefficients of superposition

$$
\begin{align}
\ket{+z,+z} = \alpha \ket{+x,+x} + \beta \ket{+x,-x} + \gamma \ket{-x,+x} + \delta \ket{-x,-x}     
\end{align}
$$
$$
\begin{align}
\bra{+x} _{z} = \frac{1}{\sqrt[]{ 2 } }\bra{+z}  + \frac{1}{\sqrt[]{ 2 } }\bra{-z} \\ \\
\bra{-x}_{z} = \frac{1}{\sqrt[]{ 2 } }\bra{+z}  - \frac{1}{\sqrt[]{ 2 } }\bra{-z}  
\end{align}
$$


We can now do
$$
\begin{align}
 \ket{+z}_{x}  &= \ket{+x} \bra{+x} \ket{+z} + \ket{-x} \braket{ -x | +z }  \\
 & = \frac{1}{\sqrt[]{ 2 } } \ket{+x} + \frac{1}{\sqrt[]{ 2 } }\ket{-x} 
\end{align}
$$
Having two particles in the $\ket{+z}$ state gives us
$$
\boxed{
\begin{align}
\ket{+z,+z} =  \frac{1}{2}\ket{+x,+x} + \frac{1}{2} \ket{+x,-x}  + \frac{1}{2}\ket{-x,+x} + \frac{1}{2}\ket{-x,-x}  
\end{align}
}
$$


We can do the same for the other:
$$
\boxed{
\begin{align}
\ket{1,-1}  & = \ket{-z,-z} \\
 & = \frac{1}{2}\ket{+x,+x } - \frac{1}{2} \ket{+x,-x} -\frac{1}{2} \ket{-x,+x} + \frac{1}{2}\ket{-x,-x}     
\end{align}
}
$$

Now we can find $\hat{S}^{2}$.

We know that 
$$
\begin{align}
\hat{S}^{2}  & = (\hat{S}_{1} + \hat{S}_{2} )^{2} \\
 & = \hat{S}_{1}^{2}+\hat{S}_{2} ^{2}+2\hat{S}_{1}\hat{S}_{2}
\end{align}
$$

$$
\begin{align}
\hat{S}^{2}_{1}\ket{+x}_{1}   & = \frac{1}{2}\left( \frac{1}{2}+1 \right)\hbar^{2} \ket{+x}   \\
 & = \frac{3}{4}\hbar^{2} \ket{+x} \\
\hat{S}^{2}_{1}\ket{-x}_{1}   & = \frac{-1}{2}\left( \frac{1}{2} \right)\hbar^{2} \ket{-x}  \\
 & = \frac{-\hbar^{2}}{4}\ket{-x} 
\end{align}
$$

The same applies for $\hat{S}^{2}_{2}$.

We still have to find
$$
\begin{align}
2 \hat{S}_{1}\hat{S}_{2}   &  \\
2\hat{S}_{1}\hat{S}_{2}\ket{+x,-x}=2\hat{S}_{1}\hat{S}_{2}\ket{-x,+ x} = -\frac{3}{2}\hbar^{2}  \\
2 \hat{S}_{1}\hat{S}_{2} \ket{+z+z}=2 \hat{S}_{1}\hat{S}_{2} \ket{-z-z}= \frac{\hbar^{2}}{2}   
\end{align}
$$

# old work
$$
\begin{align}
\ket{+z} = \frac{1}{\sqrt[]{ 2 } } \ket{+x} + \frac{1}{\sqrt[]{ 2 } }\ket{-x}  
\end{align}
$$



We know that 
$$
\begin{align}
\hat{S}^{2} = (\hat{S}_{1} + \hat{S}_{2} )^{2}
\end{align}
$$
And $\hat{S}_{1}^{2}= \hat{S}_{x}^{2}+\hat{S}_{y}^{2}+\hat{S}_{z}^{2}$
Because each particle is in the $\ket{+z}$ state, we just have
$$
\begin{align}
\hat{S}_{1}^{2}= \hat{S}_{z}^{2} 
\end{align}
$$
The same applies for 2. 
$$
\begin{align}
\hat{S}^{2} \ket{1,1} &  = (\hat{S}_{z}^{2}+\hat{S}_{z}^{2}+\hat{S}_{z}\hat{S}_{z})\ket{+z,+z }  \\
 & =3 \hat{S}^{2}_{z}\ket{+z,+z} \\
 & = 3 \left( \frac{1}{2}\left( \frac{1}{2}+1 \right) \right)\hbar^{2} \ket{+z,+z} \\
 & = \frac{9}{4}\hbar^{2} \ket{+z,+z }  
\end{align}
$$

Therefore, 
$$
\begin{align}
\hat{S}\ket{1,1} = \frac{3}{2}\hbar^{2} \ket{+z,+z} 
\end{align}
$$




![[Pasted image 20260225191809.png]]

![[Pasted image 20260226185602.png]]
We can rearrange to find $\ket{+z}$ and $\ket{-z}$ in the $n$ basis. This is just a system of equations.
$$
\begin{align}
\cos  \frac{\theta}{2}\ket{+n}  & = \cos ^{2} \frac{\theta}{2}\ket{+z}  + e^{i\phi}\sin \frac{\theta}{2} \cos \frac{\theta}{2} \ket{-z} \\
\sin \frac{\theta}{2}\ket{-n}   & = \sin ^{2} \frac{\theta}{2} \ket{+z} - e^{i\phi}\sin \frac{\theta}{2}\cos \frac{\theta}{2} \ket{-z}     \\
\end{align}
$$
Adding these, we get
$$
\begin{align}
\ket{+z} = \cos \frac{\theta}{2}\ket{+n} + \sin \frac{\theta}{2} \ket{-n}   
\end{align}
$$

We can do the same for $\ket{-z}$, just subtracting 

$$
\begin{align}
\sin \frac{\theta}{2} \ket{+n}  & = \cos \frac{\theta}{2} \sin \frac{\theta}{2}\ket{+z} + e^{i\phi}\sin ^{2} \frac{\theta}{2}\ket{ -z} \\
 \cos \frac{\theta}{2} \ket{-n}  & = \cos \frac{\theta}{2} \sin \frac{\theta}{2} \ket{+z}  - e^{i\phi} \cos ^{2} \frac{\theta}{2} \ket{-z} 
\end{align}
$$

$$
\begin{align}
e^{i\phi}\ket{-z} = \sin \frac{\theta}{2} \ket{+n} - \cos \frac{\theta}{2} \ket{-n}  \\
\ket{-z}  = e^{-i\phi}\sin \frac{\theta}{2} \ket{+n} -e^{-i\phi} \cos \frac{\theta}{2} \ket{-n} 
\end{align}
$$

![[Pasted image 20260226185602.png]]

This gives us
$$
\begin{align}
\ket{+z,-z}  & =  \left( \cos \frac{\theta}{2} \ket{+n} + \sin \frac{\theta}{2}\ket{-n}  \right)\left( e^{-i\phi}\sin \frac{\theta}{2}\ket{+n} - e^{-i\phi}\cos \frac{\theta}{2} \ket{-n}  \right) \\
 & = e^{-i\phi}\cos \frac{\theta}{2} \sin \frac{\theta}{2} \ket{+n, +n}  - e^{-i\phi}\cos ^{2} \frac{\theta}{2} \ket{+n,-n} + e^{-i\phi}  \sin ^{2} \frac{\theta}{2} \ket{-n,+n} - \cos \frac{\theta}{2} \sin \frac{\theta}{2} e^{-i\phi} \ket{-m,-n}  
\end{align}
$$
We can also do this for
$$
\begin{align}
\ket{-z,+z }  & =   \left( e^{-i\phi}\sin \frac{\theta}{2}\ket{+n} - e^{-i\phi}\cos \frac{\theta}{2} \ket{-n}  \right) \left( \cos \frac{\theta}{2} \ket{+n} + \sin \frac{\theta}{2}\ket{-n} \right) \\
 & = e^{-i\phi}\sin \frac{\theta}{2} \cos \frac{\theta}{2} \ket{+n,+n} + e^{-i\phi}\sin ^{2} \frac{\theta}{2} \ket{+n,-n} - e^{-i\phi}\cos ^{2} \frac{\theta}{2} \ket{-n,+n} - e^{-i\phi}\cos \frac{\theta}{2} \sin \frac{\theta}{2} \ket{-n,-n}    
\end{align}
$$
(SIDE NOTE: TENSOR PRODUCTS DON'T COMMUTE BECAUSE ORDER OF $N$ IN KETS MATTERS OOOOH)

We can add these two. The identical $\ket{+n,+n}$ and $\ket{-n,-n}$ cancel. 

Finally, we get:
$$
\begin{align}
\ket{0,0}  & = \frac{1}{\sqrt[]{ 2 } }\left( -e^{-i\phi}\cos ^{2} \frac{\theta}{2} -e^{-i\phi}\sin ^{2} \frac{\theta}{2}\right) \ket{+n,-n} +  \frac{1}{\sqrt[]{ 2 } }\left( +e^{-i\phi}\cos ^{2} \frac{\theta}{2}+e^{-i\phi}\sin ^{2} \frac{\theta}{2}\right) \ket{-n,+n}  \\
 & = \frac{-1}{\sqrt[]{ 2 } }e^{-i\phi} \ket{+n,-n} + \frac{1}{\sqrt[]{ 2 } } e^{-i\phi}\ket{-n,+n}  
\end{align}
$$



![[Pasted image 20260225191821.png]]
![[Pasted image 20260226185602.png]]
We have
$$
\begin{align}
\ket{\psi(0)} = \frac{1}{\sqrt[]{ 2 } }\ket{+z,-z} - \frac{1}{\sqrt[]{ 2 } } \ket{-z,+z} 
\end{align}
$$
The Spin Hamiltonian for an electron is
![[Pasted image 20260227090433.png]]
For a positron, this is
$$
\begin{align}
\hat{\mu}_{z} = \frac{ge}{2mc}\hat{S}_{z}  
\end{align}
$$
The Hamiltonian for each is
$$
\begin{align}
\hat{H} = -\hat{\mu}_{z} B
\end{align}
$$

The difference between these is
$$
\begin{align}
H_{e} - H_{p} = \frac{-ge}{2mc}(\hat{S}_{ez} - \hat{S}_{pz} )  
\end{align}
$$
If we label
$$
\begin{align}
\omega_{0} = -\frac{ge}{2mc}
\end{align}
$$
then we have
$$
\begin{align}
\hat{H} = \omega_{0} ( S_{1z}- S_{2z}  )
\end{align}
$$
## b
![[Pasted image 20260227091523.png]]

We can find the eigenvalues of the operators $\hat{S}_{1,z}$ and $\hat{S}_{2,z}$. 
$$
\begin{align}
\hat{S} \ket{z}  & = \frac{\hbar}{2}\ket{z} \\
\hat{S} \ket{-z}  & = - \frac{\hbar}{2}\ket{-z} 
\end{align}
$$

The spin zero states are $\ket{+z,-z}\text{ and } \ket{-z,+z}$, while the spin 1 states are $\ket{-z,-z}\text{ and } \ket{+z,+z}$.
$$
\begin{align}
\hat{H} \ket{+z,-z} = \omega_{0} \hbar \ket{+z,-z} \\
\hat{H}\ket{-z,+z} = -\omega_{0} \hat{h}\ket{-z,+z}    
\end{align}
$$

We can find the Hamiltonian acting on each $z_{1},z_{2}$ - as they rotate they'll align and move away, shifting between these four states. 

If we start in spin zero, then we have the time evolution given by
$$
\begin{align}
\psi(t) = e^{-i\omega_{0}t}\ket{+z}_{1} \otimes e^{i\omega_{0}t}\ket{-z}_{2}     \\
\end{align}
$$
(side note to the gruter - do we have to normalize this with a $\frac{1}{\sqrt[]{ 2 }}$ I'm not sure, since each one is definitely in that state and not split, so each has magnitude 1? It feels like for problem c i need a normalization though)

These are 90 degrees apart and counter rotating. When one has moved $\pi$, the other has moved $-\pi$, so they are aligned into a spin 1 state. Another $\pi$ and they are in opposite spins, and in a spin zero state. 

This gives the period of oscillation as 
$$
\begin{align}
t= \frac{\pi}{\omega_{0}}
\end{align}
$$

## c
![[Pasted image 20260227092725.png]]
$$
\begin{align}
\psi_{1}(t) = e^{- \frac{i}{2}t}\ket{+z}   \\
\end{align}
$$

We can find this as
$$
\begin{align}
(\bra{+x_{1}}\ket{\psi(t)_{1} } )^{2} + (\bra{+x_{2}}\ket{\psi(t)_{2} } ) ^{2}
\end{align}
$$

We know that
$$
\begin{align}
\bra{+x}\ket{+z} = \frac{1}{2} \\
\braket{ +x |-z} = \frac{1}{2} 
\end{align}
$$
For the first term, we have
$$
\begin{align}
\bra{+x}e^{i\omega_{0}t}\ket{+z} 
\end{align}
$$


# old work
We can write out our time evolving states as 
$$
\begin{align}
\psi_{1}(t) = e^{- \frac{i}{2}t}\ket{+z}   \\
\ket{+z} = \psi(t)e^{\frac{i}{2}t} 
\end{align}
$$

$$
\begin{align}
\ket{+x}  & = \frac{1}{\sqrt[]{ 2 } } \ket{+z} + \frac{1}{\sqrt[]{ 2 } } \ket{-z}    \\
 & = \frac{1}{\sqrt[]{ 2 } }e^{\frac{i}{2}t}\ket{\psi_{1}(t)} +  
\end{align}
$$

We will measure $\frac{\hbar}{2}$ half of the time in a pure $\ket{+z}$ and a pure $\ket{-z}$. 




![[Pasted image 20260225191829.png]]

$$
\begin{align}
\hat{S}_{1}\cdot \hat{S}_{2} = \hat{S}_{1x}\hat{S}_{2x}  + \hat{S}_{1y}\hat{S}_{2y}  + \hat{S}_{1z}\hat{S}_{2z}  
\end{align}
$$
$$
\begin{align}
S_{+} = S_{x} +iS_{y}  \\
S_{-} = S_{x}  - iS_{y}  \\ 
\end{align}
$$
We can rewrite this with the raising and lowering operators
$$
\begin{align}
S_{x} = \frac{S_{+} + S_{-}  }{2} \\
S_{y} = \frac{S_{+} - S_{-}   }{2i}  
\end{align}
$$

We can write out the spin $\otimes$ product with the raising and lowering operators as
$$
\begin{align}
\hat{S}_{1} \cdot \hat{S}_{2}  & = \hat{S}_{1z}\hat{S}_{2z}  +\frac{\hat{S}_{1+} + \hat{S}_{1-}  }{2} \frac{\hat{S}_{2+} + \hat{S}_{2-} }{2} + \frac{\hat{S}_{1+} - \hat{S}_{1-}  }{2i} \frac{\hat{S}_{2+} - \hat{S}_{2-} }{2i} \\
 & =\hat{S}_{1z}\hat{S}_{2z}  + \frac{1}{4}(S_{1+}S_{2+} + S_{1+}S_{2-} + S_{1- }S_{2+}+ S_{1-}S_{2-}  ) -\frac{1}{4}(S_{1+}S_{2+}+S_{1-}S_{2-}) \\
 & = \hat{S}_{1z}\hat{S}_{2z} + \frac{1}{4}(S_{1+}S_{2-}+ S_{1-}S_{2+}   )
\end{align}
$$
Also, note that
$$
\begin{align}
\hat{S}_{+}\ket{+z} & =0 \\
\hat{S}_{+}\ket{-z} &  = \hbar \ket{+z}     \\
\hat{S}_{-}\ket{+z} & = -\hbar \ket{-z}  \\
\hat{S}_{-}\ket{-z} &  = 0    
\end{align}
$$
We can now find the effect of the Hamiltonian on each state
$$
\begin{align}
\hat{H} \ket{ +z,+z} &  = \frac{2A}{\hbar^{2}} \left( \frac{\hbar^{2}}{4} \ket{+z,+z}  \right)  \\
 & = \frac{A}{2}\ket{+z,+z} \\
\hat{H} \ket{+z,-z} &  =  \frac{2A}{\hbar^{2}} \left(-\frac{\hbar^{2}}{4}\ket{+z,-z} - \frac{\hbar^{2}}{2}\ket{-z,+z}   \right) + \omega_{0}\hbar\\
\hat{H} \ket{-z,+z} &  =  \frac{2A}{\hbar^{2}} \left(  \frac{-\hbar^{2}}{4} \ket{-z,+z} -\frac{\hbar^{2}}{2}  \ket{+z,-z}  \right)+ \omega_{0}\hbar\\
\hat{H} \ket{-z,-z} &  = \frac{2A}{\hbar^{2}} \left( \frac{\hbar^{2}}{4} \ket{-z,-z} \right) \\
 & =\frac{A}{2}\ket{ -z,-z} 
\end{align}
$$


This gives us the matrix

$$
\begin{align}
\hat{H} = \begin{bmatrix}
\frac{A}{2} & 0 & 0 & 0 \\
0 & -\frac{A}{2}+\omega_{0}\hbar & - A & 0 \\
0 & -A & \frac{-A}{2}-\omega_{0}\hbar & 0 \\
0 & 0 & 0 & A
\end{bmatrix}
\end{align}
$$

We can find the eigenvalues for the innermost matrix
$$
\begin{align} 
\begin{bmatrix}
-\frac{A}{2}+\omega_{0}\hbar & A \\
A & -\frac{A}{2}- \omega_{0}\hbar
\end{bmatrix}
\end{align}
$$
This gets
$$
\begin{align}
\left( -\frac{A}{2}+\omega \hbar - \lambda \right)\left( -\frac{A}{2}-\omega \hbar- \lambda \right)-A^{2}  & = 0 \\
\left( \left( - \frac{A}{2}-\lambda \right)^{2} - \omega^{2}\hbar^{2} \right) - A^{2}  & = 0 \\
\end{align}
$$
$$
\begin{align}
\left( -\frac{A}{2}-\lambda \right)^{2}  & = A^{2} + \omega^{2}\hbar^{2} \\
-\frac{A}{2}-\lambda & = \pm  \sqrt[]{ A^{2}+\omega^{2}\hbar^{2} }  \\
\lambda & = - \left( \frac{A}{2} \pm     \sqrt[]{ A^{2}+\omega^{2}\hbar^{2}  }  \right)
\end{align}
$$
The top left and bottom right entry don't multiply with anything 

Our eigenvalues are thus
$$
\begin{align}
\frac{A}{2}, -\left( \frac{A}{2} + \sqrt[]{ A^{2} + \omega^{2}\hbar^{2} }   \right),-\left( \frac{A}{2} - \sqrt[]{ A^{2} + \omega^{2}\hbar^{2} }   \right), \frac{A}{2}
\end{align}
$$






# old work, thanks Ian for helping
We can check the effect of the Hamiltonian on each of the spin $\frac{1}{2}$ states.
$$
\begin{align}
\hat{H} \ket{ +z,+z} &  = \left( \frac{2A}{\hbar^{2}}\left( \frac{1}{2} \frac{1}{2}\hbar^{2} \right)  + \omega_{0}\hbar (0) \right) \ket{+z,+z} \\
\hat{H} \ket{+z,-z} &  = \left( \frac{2A}{\hbar^{2}}\left( \frac{1}{2}\frac{-1}{2}\right) \hbar^{2}  + \omega_{0}\hbar (1) \right)\ket{+z,-z} \\
\hat{H} \ket{+z,-z} &  = \left( \frac{2A}{\hbar^{2}}\left( \frac{1}{2}\frac{-1}{2}\right) \hbar^{2}  + \omega \hbar(0) \right)\ket{-z,+z}\\
\hat{H} \ket{-z,-z} &  = \left( \frac{2A}{\hbar^{2}}\left( \frac{-1}{2} \frac{-1}{2}\right) \hbar^{2}  + \omega_{0}\hbar(0) \right)\ket{-z,-z} \\
\end{align}
$$

These simplify down to
$$
\begin{align}
\hat{H} \ket{+z,+z}  & = \frac{A}{2} \ket{+z,+z} \\
\hat{H} \ket{+z,-z}  & = -\left( \frac{A}{2} +\omega_{0} \right)\ket{+z,-z}     \\
\hat{H} \ket{-z,+z}  & = -\left( \frac{A}{2} + \omega_{0} \right)\ket{-z,+z} \\
\hat{H} \ket{-z,-z}  & = - \frac{A}{2} \ket{-z,-z}     
\end{align}
$$

We can write this in a matrix
$$
\begin{align}
\hat{H} = \begin{bmatrix}
\frac{A}{2} & 0 & 0 & 0 \\
0 & \frac{-A}{2}+\omega_{0}\hbar & 0 & 0 \\
0 & 0 & -\frac{A}{2}+\omega_{0}\hbar  & 0 \\
0 & 0 & 0 & & -\frac{A}{2}
\end{bmatrix}
\end{align}
$$


# This is bad, the $\ket{+z,+z}$ is not the eigenbasis of the hamiltonian, I can't just construct stuff like this. RAGH
