We have two core problems in linear algebra:
$$
\begin{align}
\hat{A}\cdot \vec{x}=\vec{b} \\
\text{ and }   \\
\hat{A}\cdot \vec{x}=\lambda \vec{x}
\end{align}
$$
Let's explore the eigenvector problem:
$$
\begin{align}
\hat{A}\cdot \vec{x}=\lambda  \hat{\mathbb{I}}\cdot \hat{x} \\
(\hat{A}-\lambda  \hat{\mathbb{I}})\cdot \vec{x}=0 \\
\implies \det{(\hat{A}-\lambda  \hat{\mathbb{I}})}=0 
\end{align}
$$
$$
\begin{align}
\det{(\begin{pmatrix}
a_{1,1}-\lambda & a_{1_{2}}  & \dots \\
a_{2,1} & a_{2,2}- \lambda &  \dots \\
\vdots
\end{pmatrix})} 
\end{align}
$$
Let
$$
\begin{align}
\hat{A}=\begin{pmatrix}
1 & 2 \\
3 & 2
\end{pmatrix}, \\
\det{(\begin{pmatrix}
1-\lambda & 2 \\
3 & 2-\lambda
\end{pmatrix})} \implies (1-\lambda)(2-\lambda)-6 \\
\implies (\lambda-4)(\lambda+1)=0 \\ 
\end{align}
$$
We can now find the eigenvectors. Let's start with $\lambda=4$
$$
\begin{align}
\begin{bmatrix}
3 & 2 \\
3 & -2
\end{bmatrix} \begin{pmatrix}
x_{1}\\ x_{2}
\end{pmatrix} = 0 \\
-3x_{1}+2x_{2}=0, x_{2}=\frac{3}{2}x_{1} \\
\end{align}
$$
We want to normalize the eigenvectors, since they just tell us direction
$$
\begin{align}
\begin{pmatrix}
1 \\ \frac{3}{2}
\end{pmatrix}x_{1} \implies \frac{2}{\sqrt{ 13 }}\begin{pmatrix}
1\\ \frac{3}{2}
\end{pmatrix}
\end{align}
$$

The second eigenvector should be
$$
\begin{align}
\begin{bmatrix}
2 & 2 \\
3 & 3
\end{bmatrix} \begin{pmatrix}
x_{1}\\x_{2}
\end{pmatrix} =0\\
\end{align}
$$
$x_{1}=-x_{2}, so$

$$
\begin{align}
\frac{1}{\sqrt{ 2 }} \begin{bmatrix}
1 \\ -1
\end{bmatrix}
\end{align}
$$

We can see that these two eigenvectors are not orthogonal. 


Now, let us consider something special
## Hermitian matricies
These satisfy $\hat{H}^{\dagger}=\hat{H}$
$^{\dagger}$ is the complex conjugate of the transpose.
$$
\begin{align}
\hat{H}\ket{a} = \ket{b} 
\end{align}
$$
Recall, $\left< A|B \right> = \sum_{i}^{}a^{*}_{i}b_{i}$
Also, note that this could be written.
$$
\begin{align}
(a_{1}^{*},a_{2}^{*}\dots) \begin{pmatrix}
b_{1}\\b_{2}\\\vdots
\end{pmatrix}
\end{align}
$$
It collapses to a single number.
We can swap the order and get
$\left< a|b \right> = \left< b|a \right>^{*}$

We have the operators
$$
\begin{align}
\hat{A}\ket{a} =\ket{b}  \\
\braket{ a}  | \hat{A}^{\dagger}=\bra{b}  
\end{align}
$$
If A is Hermitian than these two are the same. 

If $\hat{H}^{\dagger}=\hat{H}$, we can prove that the eigenvalues of $\hat{H}$ are real:
$$
\begin{align}
\hat{H}\ket{a} =\lambda_{a}\ket{a} \\
\bra{a} \hat{H}\ket{a} =\lambda_{a} \underbrace{ \left< a|a \right> }_{ \text{ non negative real } }   
\end{align}
$$

$$
\begin{align}\text{ The adjoint of  }
\bar{H}\ket{a} =\lambda_{a}\ket{a} \text{ is } \\
\braket{ a} \bar{H}^{\dagger}=\lambda_{a}^{*}\bra{a}  \\
\bra{a} \hat{H}^{\dagger}\ket{a}=\lambda_{a}^{*}\left< a | a  \right>  
\end{align}
$$
if $\hat{H}^{\dagger}=\hat{H}$, then
$\bra{ a}\hat{H}\ket{a}=\lambda ^{*}_{a} \left< a|a \right>$

How can we convert 
$$
\begin{align}
\begin{bmatrix}
1 & 2 \\
3 & 2
\end{bmatrix} \text{ into a hermetian matrix }
\end{align}
$$

Assuming that we are dealing with a Hermitian operator, if we have two distinct eigenvalues, then the eigenvectors are orthogonal. 

We have 
$$
\begin{align}
\hat{H}\ket{a} =\lambda_{a}\ket{a} \\
\hat{H}\ket{b} =\lambda_{b}\ket{b} \\  
\end{align}
$$
We can show that $\left< a|b \right> = 0$ if $\lambda_{a}\neq \lambda_{b}$
$$
\begin{align}
\bra{ b} \hat{H} \ket{a} =\lambda a \left< b | a  \right>  \\
\bra{ b} \hat{H}^{\dagger}=\lambda_{b}^{*} \braket{ b}  \\
\lambda_{b}^{*}\left< b | a  \right> =\lambda_{a} \left< b|a \right>  
\end{align}
$$

