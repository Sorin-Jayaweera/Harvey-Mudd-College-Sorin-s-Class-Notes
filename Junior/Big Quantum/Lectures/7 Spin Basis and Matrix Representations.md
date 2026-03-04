Because rotations don't commute, components of angular momentum don't either. We can find how those don't commute, and find the valid states of angular momentum. 

$$
\begin{align}
[\hat{J}_{x},\hat{J}_{y}  ] & = i\hbar \hat{J}_{z} 
\text{ and } \\ 
[\hat{J}^{2},J_{x} ] & =0
\end{align}
$$
Note $J$ is generic angular momentum - orbital or spin. Later we'll specify that $\underbrace{ \hat{\vec{J}} }_{ \text{ total } }= \underbrace{ \hat{\vec{L}} }_{ \text{ orbital } }+ \underbrace{ \hat{\vec{S}} }_{ \text{ spin } }$ , but not yet.

Because the $\hat{J}^{2}$ commutes, we can totally have states with eigenvalue of $m \,\vec{z}$ angular momentum and $j$ total momentum.
$$
\begin{align}
\ket{j,m} \\
\hat{J}_{z} \ket{j,m} = \hbar m \ket{j,m} \\
\hat{J}^{2}\ket{j,m} = \hbar^{2}j(j+1) \ket{j,m}     
\end{align}
$$

We have states for different spin systems given by
$\ket{\lambda,m}$
(note, the generic eigenvalue is $\ket{\lambda,m}$, and the maximum angular momentum is $\ket{\pm i,m}$). Moving right on the table below is the raising operator, and left is the lowering. 
$$
\begin{align}
 & \ket{0,0} \to  1 \\
 & \ket{\frac{1}{2},- \frac{1}{2}} &   \ket{\frac{1}{2},\frac{1}{2}} \\  
 & \ket{1,-1}   & \ket{1,0}  & &  \ket{1,1} \\
 & \ket{\frac{3}{2},-\frac{3}{2}}   & \ket{\frac{3}{2},-\frac{1}{2}}     & &   \ket{\frac{3}{2},\frac{1}{2}}   & & \ket{\frac{3}{2},\frac{3}{2}} \\
 & \ket{2,-2} & \ket{2,-1}  &  & \ket{2,0}   & & \ket{2,1}  &  & \ket{2,2}  
\end{align}
$$
We can have any linear combination of these states. 

Some derivations

$$
\begin{align}
\hat{J}_{y} = \frac{1}{2_{i}} \hat{J}_{+} - \frac{1}{2i} \hat{J}_{-} \\
\hat{J}_{x} = \frac{1}{2} \hat{J}_{+} + \frac{1}{2} \hat{J}_{-} 
\end{align}
$$

Lets find representations of subspace of some definite total angular momentum.
For example: $j=1$
Lets assign column vectors
$$
\begin{align}
\ket{1,+1} \to   \begin{pmatrix}
1\\0\\0
\end{pmatrix} \\
\ket{1,0} \to   \begin{pmatrix}
0\\1\\0
\end{pmatrix} \\
\ket{1,-1} \to   \begin{pmatrix}
0\\0\\1
\end{pmatrix} 
\end{align}
$$
Lets call this basis "$J_{z}$ Spin 1"

$$
\begin{align}
\hat{J}z \to  \begin{pmatrix}
\hbar & 0 & 0 \\
0 & 0 \hbar & 0 \\
0 & 0 & -\hbar
\end{pmatrix}
\end{align}
$$
The hardest part is the next step. Lets find $\hat{J}_{+}$.
$$
\begin{align}
\hat{J}_{+}\ket{1,1} & =0  & =0\\
\hat{J}_{+}\ket{1,0}  & = \hbar\sqrt[]{j(j+1)- m(m+  1)  } \ket{1,1}    \\
 & =\hbar \sqrt[]{ 1 \cdot 2 - 0 } \ket{1,1}  & = \hbar \sqrt[]{ 2 } \ket{1,1} \\
\hat{J}_{+}\ket{1,-1}  & = \hbar \sqrt[]{ 1\cdot 2 - (-1)(-1+1) }       & = \hbar \sqrt[]{ 2 } \ket{1,0} 
\end{align}
$$
We now get
$$
\begin{align}
\hat{J}_{+} \to   \hbar \begin{pmatrix}
0 & \sqrt[]{ 2 }   & 0 \\
0 & 0  &  \sqrt[]{ 2 }\\
0 & 0 & 0
\end{pmatrix} 
\end{align}
$$
(we do this by multiplying by each basis vector and figuring out what value we would need to have). Think of it as each row's multiplication step asking how much of each basis should be there. I.e. if I do $\ket{1,0}$ (represented $\begin{pmatrix}0\\1\\0\end{pmatrix}$) then I would end up with $\hbar \sqrt[]{ 2 }$ of the state $\ket{1,1}$. 
The multiplication is 
$$
\begin{align}
(0*0 + \sqrt[]{ 2 } * 1 + 0 * 0 ) \ket{1,1} \\
 (0*0 + 0*1+\sqrt[]{ 2 } *0) \ket{1,0} \\
0*\dots \ket{1,-1}  
\end{align}
$$
so this ends up with $\sqrt[]{ 2 } \ket{1,0}$.  


We know that $\hat{J}_{-}= \hat{J}_{+}^{\dagger}$ which is just
$$
\begin{align}
\hbar \begin{pmatrix}
0 & 0 & 0 \\
\sqrt[]{ 2 }  & 0 & 0 \\
0 & \sqrt[]{ 2 }  & 0
\end{pmatrix}
\end{align}
$$
We can now see that $\hat{J}_{x}$ is
$$
\begin{align}
\hat{J}_{x} &  = \frac{1}{2} ( \hat{J}_{+}+\hat{J}_{-}  ) \\
 & = \hbar \frac{\sqrt[]{ 2 }}{2} \begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 0
\end{pmatrix}
\end{align}
$$
and $\hat{J}_{y}$ as
$$
\begin{align}
\hbar \frac{i\sqrt[]{ 2 }}{2}  \begin{pmatrix}
0 & -1 & 0 \\
1 & 0 & -1 \\
0 & 1 & 0
\end{pmatrix}
\end{align}
$$

