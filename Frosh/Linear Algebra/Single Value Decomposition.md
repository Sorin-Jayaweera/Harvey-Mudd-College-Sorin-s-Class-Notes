Recall:
Matrix Decomposition:
we learned 
* Product of elementary matrices, :$A=E_{k}E_{k-1}\dots E_{0}A'$
* QR Factorization: $A=AR$
* Similarity: $A=PBP^{-1}$
* Diagonalization: $A=PDP^{-1}$
* Orthogonal Diagonalization: $A=QDQ^{T}$
We will now add in single value decomposition, which contains all the information of those previous ones at once. This applies to any matrix.

Let $\underbrace{ A }_{ m\times n }=\underbrace{ U }_{ m\times m\text{ orthogonal } }\,\,\,\underbrace{ \Sigma }_{ m\times n \text{ diagonal } }\,\,\,\underbrace{ V^{T} }_{ n\times n \text{ orthogonal } }$
$A=U\Sigma V^{T}$ is the single value decomposition that exists for every matrix.
$$
\begin{align}
A=\begin{pmatrix}
\vec{u}_{1} &\dots& \vec{u}_{m}
\end{pmatrix} \begin{pmatrix}
\sigma_{1} & 0 & \dots \\
0 & \sigma_{2} & \dots \\
\vdots  & \vdots  & \vdots  \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}\begin{pmatrix}
\vec{v}_{1}\\ \vdots\\ \vec{v}_{4}
\end{pmatrix}
\end{align}
$$
Where the sigma values are the "singular values" of A.
The padding at the bottom of the Sigma matrix  acts to remove extra values from the $U$ matrix. 
Expanding this out,
$$
\begin{align}
A=\vec{u}_{1}\sigma_{1}\vec{v}^{T}_{1}+\dots+\vec{u}_{n}\sigma_{n}\vec{v}^{T}_{n}
\end{align}
$$
Any terms that aren't zero are rank one matrices. 

Idea: The SVD theorem generalizes the spectral theorem and spectral decomposition to all matrices.
The singular values measure how $A$ scales or transforms unit vectors.

For example: let $A=\begin{pmatrix}0&0\\0&3\\-2&0\end{pmatrix}$. Note that $T_{A}:\mathbb{R}^{2}\rightarrow \mathbb{R}^{2}$
Lets look at what happens to unit vectors (the unit circle) under $T_{A}(X)=Ax$
$$
\begin{align}
\left| Ax  \right|^{2}=(Ax)\cdot(Ax)=x^{T}A^{T}Ax \\
=X^{T}\begin{pmatrix}
0 & 0 & -2 \\
0 & 3 & 0
\end{pmatrix} \begin{pmatrix}
0 & 0 \\
0 & 3 \\
-2 & 0
\end{pmatrix}x \\
=X^{T}\begin{pmatrix}
4 & 0 \\
0 & 9
\end{pmatrix}x  \\
= 4x_{1}^{2}+9x_{2}^{2}
\end{align}
$$

This matrix generally scales vectors by 4 and 9. The norm image will transform to somewhere between our maximum eigenvalue and our minimum eigenvalue. 

Doing $A$ on the unit vectors:
$$
\begin{align}
v_{1} = \begin{pmatrix}
1\\0\\0
\end{pmatrix}, v_{2}=\begin{pmatrix}
0 \\1\\0
\end{pmatrix}, v_{3}=\begin{pmatrix}
0\\0\\1
\end{pmatrix}
\end{align}
$$
$$
\begin{align} \\
Av_{1}=\begin{pmatrix}
0\\0\\-2
\end{pmatrix}
Av_{2}=\begin{pmatrix}
0\\3\\0
\end{pmatrix}, Av_{3}=\begin{pmatrix}
0\\ \frac{3}{\sqrt{ 2 }}  \\
-\frac{2}{\sqrt{ 2 }}
\end{pmatrix}
\end{align}
$$

We can bound the magnitude of $\left| Ax \right|^{2}$ by
$$
\begin{align}
x^{T}A^{T}Ax=X^{T}QDQ^{T}x=(Q^{T}x)^{T}D(Q^{T}x) \\
\text{ let } y=Q^{T}x \\
= y^{T}Dy=\lambda_{1}y_{1}^{2}+\lambda_{2}y_{2}^{2} + \dots + \lambda_{n}y_{n}^{2} \\
\leq \lambda_{1}(y_{1}^{2} +y_{2}^{2}+\dots+y_{n}^{2}) = \lambda_{1}\left| y \right|^{2}
\end{align}
$$
This gives us that $$
\begin{align}
\left| Ax  \right|^{2}\geq \lambda _{n}\left|y\right|^{2}
\end{align}
$$
We can always find a vector $x$ that will be scaled by the eigenvalues.
We can find those vectors.

$$
\begin{align}
\text{ in our example, } \\
\sqrt{ 4 }\leq \left| Ax  \right| \leq \sqrt{ 9 }
\end{align}
$$

The image under $A$ is an ellipse:
* the major axis has length $\sigma_{1}=\sqrt{ \lambda_{1} }$ where $\lambda_{1}$ is the largest eigenvalue of $A^{T}A$
* and minor axis has length $\sigma_{2}=\sqrt{ \lambda_{2}2 }$ where $\lambda_{2}$ is the smallest eigenvalue of $A^{T}A$
* In higher dimensions: unit spheres $\rightarrow$ ellipsoids (like a football in $\mathbb{R}^{3}$).

We now have enough information to construct singular value decomposition. 

Steps to construct the $SVD$:
1) Find the singular values
We find the eigenvalues of $A^{T}A$. In this case, its $\begin{pmatrix}4&0\\0&9\end{pmatrix}$
$\lambda_{1}=9,\lambda_{2}=4$ (we always just go largest to smallest)
$$
\begin{align}
\sigma_{1}=3,\sigma_{2}=2
\end{align}
$$
2) This gives us $\Sigma$. 
$$
\begin{align}
\Sigma=\begin{bmatrix}
3 & 0 \\
0 & 2 \\
0 & 0
\end{bmatrix} \\
\text{ we pad with zeros to make it the same size as A }
\end{align}
$$

3) Construct $V$
Find the eigenvectors for $A^{T}A$ and normalize them $\rightarrow$ $V$ should be an orthogonal basis for $\mathbb{R}^{n}$... like the eigenvectors of $A^{T}A$!
$$
\begin{align}
A^{T}A & = QDQ^{T} \\
 & = V\Sigma^{T}U^{T}U\Sigma V^{T} \\
 & =V\Sigma^{T}\Sigma V^{T}
\end{align}
$$
$v_{1}$ for $\lambda_{1}=9$ is $\begin{align}\begin{pmatrix}0\\1\end{pmatrix} \\\end{align}$ 
$v_{2}$ for $\lambda_{2}=4$ is $\begin{pmatrix}1\\0\end{pmatrix}$
(this is a total fluke, we normally have to do more work. Just because $A^{T}A$ was diagonal this happened.)
We have to find the eigenvectors that are associated with each eigenvalue and then normalize them.

So
$$
\begin{align}
V=\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}\implies V^{T} = \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
\end{align}
$$
4) We now have to compute $U$.
We take an orthonormal basis of vectors and scale them by multiplying by $A$. 
The columns of $u$ should form an orthonormal basis for $\mathbb{R}^{m}$. Since $\left\{ v_{1},\dots,v_{n} \right\}$ are orthogonal eigenvectors of $A^{T}A$ in $\mathbb{R}^{n}$, the vectors $\left\{ Av_{1},\dots,Av_{n} \right\}$ are orthogonal in $\mathbb{R}^{m}$. 
$$
\begin{align}
A(v_{i})\cdot(Av_{j})=v_{i}^{T}A^{T}Av_{j}=v_{i}^{T}\lambda_{j}v_{j}=\lambda_{j}v_{i}^{T}v_{j}=0 \text{ if }i\neq j
\end{align}
$$
We have shown that the vectors are orthogonal. We can form the set $\left\{ Av_{1},\dots,Av_{n} \right\}$ and normalize them. This gets
$\left\{ \frac{1}{\sigma 1}Av_{1},\dots,\frac{1}{\sigma_{n}}Av_{n} \right\}$. 
This may not be enough to fit everything that we need. We'll extend our basis, choosing $m-n$ linearly independent vectors, apply gram Schmidt, and normalize them. For our example,
$$
\begin{align}
U= \begin{pmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & -1 & 0
\end{pmatrix} \\
 (\text{ the } \begin{pmatrix}
1\\0\\0
\end{pmatrix} \text{ is useless }) \\
\end{align}
$$

We now have everything we need for single value decomposition.
$$
\begin{align}
A  & = U \Sigma V^{T} \\
 & = \begin{pmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & -1 & 0
\end{pmatrix}\begin{pmatrix}
3 & 0 \\
0 & 2 \\
0 & 0
\end{pmatrix}\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
\end{align}
$$
Facts about the SVD:
1)  The rank of a is bounded by the minimum rank of any of these matrices. U is square and orthogonal, meaning it has rank $m$. Similarly, the rank of $V$ is $n$. The rank of $\Sigma$ is $r$, as there are $r$ different $\sigma$ values. We can see the rank of the matrix as the rank of $\Sigma$, which in this case is $2$.    
2) $\left\{ u_{1},\dots,u_{r} \right\}$ is an orthonormal basis for $col(A)$. $\left\{ u_{1},\dots,u_{r} \right\}$ is an orthonormal(linearly independent) set in col(A) by construction and $dim(col(A))=rank(A)=r$ 
3) $\left\{ u_{r+1},u_{r+2}\dots,U_{m} \right\}$ is an orthonormal basis for $null(A^{T})$. We picked those vectors for being orthogonal to all the values $u_{1}\dots u_{r}$, so it is already orthogonal and in the null.
4) $\left\{ v_{r+1},\dots, v_{n} \right\}$ is an orthonormal basis for $null(A)$.
5) $\left\{ v_{1},\dots,v_{r} \right\}$ is an orthonormal basis for $row(A)$.  