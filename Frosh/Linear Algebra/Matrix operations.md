Recall:
	#linear_independence a set of vectors is linearly dependent if there are scalars $c_{1},c_{2}\dots c_{k}$ not all zero such that
	$c_{1}\vec{v}_{1}+c_{2}\vec{v}_{2}+\dots+v_{k}\vec{v}_{k}=0$ 
	Geometrically, if a set is dependent than you can make one vector by scaling and adding the other vectors in the set to generate that vector. That means that you could rearrange the equation and get zero with the new $c = -1$, which means that  the set is dependent. For it to be independent, there isn't a linear combination of other vectors to generate the new one, so it contains new information. The row reduced echelon form of a matrix of these vectors would have no rows of zeros in an independent set.
	This can be expressed by the theorem: 
	The set $\{  \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{m}\}$ is linearly dependent if and only if the homogenous linear system with the augmented matrix 
	$$
	\begin{pmatrix}
	| & | & \dots & | & | &  \\
	\vec{v}_{1} & \vec{v}_{2} & \dots & \vec{v}_{m} & |  & \vec{0} \\
	| & | & \dots & | & | &  \\
	
	\end{pmatrix}
	$$ has a nontrivial solution.
	Homogenous systems have either one or infinitely many solutions. The one solution is the zero vector $\vec{0}$, otherwise  there are infinite solutions. See: homogenous systems in [[Spanning Sets and Linear Independence]]
	is the following set linearly independent?
	$$
	\begin{pmatrix}
	2 \\
	1 
	\end{pmatrix}, \begin{pmatrix}
	4 \\
	-1 
	\end{pmatrix},
	\begin{pmatrix}
	-2 \\
	2
	\end{pmatrix}
	$$
	Write out in augmented matrix form
	$$
	\begin{bmatrix}
	2 & 4 & -2  & | & 0\\
	1 & -1 & 2 & | & 0
	\end{bmatrix}
	$$
	We could, with a little bit of work, use ERO's to reduce this and find infinitely many solutions to the system of linear equations, however we don't even have to. We will always have a free variable. The vectors are in $\mathbb{R}^{2}$, so there are at most 2 leading variables. There are 3 vectors, so there is at least 1 free variable. Therefore, this system is not linearly independent! 
	Theorem: A set of $m$ vectors in $\mathbb{R}^{n}$ is linearly dependent if $m>n$. At most there can be $n$ linearly independent vectors in $\mathbb{R}^{n}$. If one vector is already in the span of the others, then they are linearly dependent. 
. 
Linear algebra unifies matrixes, vectors, and systems of equations. Operations that we do on these sets transforms the space defined by those sets in interesting ways.

Matrix algebra means that we have matrixes as the set. 
There are several operations that we can perform on matrixes
![[Pasted image 20240131112249.png]]
We can think about the matrix equation $\vec{b}=A\vec{x}$ as a transformation: the matrix A "acts on" the vector $\vec{x}$ to yield a new vector $\vec{b}$. $A$ is the action that we are doing on $\vec{x}$ to transform the space.
This is #matrix_multiplication
For example, if we take
$$
\begin{align}
A = \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} \text{ and } \vec{x} = \begin{pmatrix}
1 \\
2
\end{pmatrix} \\
A\vec{x} = 1\begin{pmatrix}
0 \\
-1
\end{pmatrix}+2\begin{pmatrix}
1 \\
0
\end{pmatrix} = \begin{pmatrix}
2 \\
-1
\end{pmatrix}
\end{align}
$$
We have taken the initial vector $\vec{X}$ and transformed it t o the vector $\begin{pmatrix}2\\-1\end{pmatrix}$.
Instead of having just one vector $\vec{x}$, we can transform multiple vectors at a time.
In a new problem,
We can take $x_{1} \text{ and } x_{2}$ and write them in a matrix
$$
A=\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}, X = \begin{pmatrix}
\frac{1}{x_{1}} & \frac{1}{x_{2}} \\
1 & 1
\end{pmatrix} = \begin{pmatrix}
1 & -1 \\
2 & 1
\end{pmatrix}
$$
Then, $AX$ = $\begin{pmatrix}2&1\\-1&1\end{pmatrix}$
**There is a very subtle thing that is happening here**. We have taken the dot product between the first row of $A$ and the first column of $X$. The matrix X is vectors that are being manipulated, and A is the space that is acting on those vectors. Each $\vec{x}$ is multiplied by the basis vectors of A and transformed to be a new vector. The results of this happening for each vector in X is compiled into the new matrix B. 

Multiplying by matrixes is similar to a function, called #matrix_transformations. We are taking an input X and acting on it in a way defined by A and outputting a new function.

How do we do matrix transformations in practice?
We have to match up the number of input vectors with the number of columns of a matrix, and the output size with the number of rows of a matrix.
Take $$
A=\begin{pmatrix}
a_{1,1} & a_{2,1} & a_{3,1} \\
a_{1,2} & a_{2,2} & a_{3,2}
\end{pmatrix}
$$This is a $2\times 3$ matrix, so there has to be 3 input vectors, and the output dimension is 2. 

For practice:
	$$
	\text{ Take A }= \begin{pmatrix}
	1 & 0 & -7 \\
	0 & 4 & 3
	\end{pmatrix} \text{ and } B=\begin{pmatrix}
	3 \\
	2 \\
	1
	\end{pmatrix}
	$$$$
	\begin{align}
	AB= 3\begin{pmatrix}
	1 \\
	0
	\end{pmatrix} + 2\begin{pmatrix}
	0 \\
	4
	\end{pmatrix} + 1\begin{pmatrix}
	-7\\3
	\end{pmatrix} \\
	=\begin{pmatrix}
	3 & 0 & -7 \\
	0 & 8 & 3
	\end{pmatrix}
	\end{align}
	$$
	So we have successfully transformed the three vectors by scaling each one by the associated one in $B$.

We can also do some more easy transformations. I.E: #matrix_addition
take
$$
A = \begin{pmatrix}
1 & 0 & -7 \\
0 & 4 & 3
\end{pmatrix}, B=\begin{pmatrix}
2 & 2 & 2 \\
3 & -1 & 0
\end{pmatrix}
$$
To add together matrixes, they have to have the same dimensions, and they just add component wise.
$$
A+B = \begin{pmatrix}
1+2 & 0+2 & -7+2 \\
0+3 & 4-1 & 3+0
\end{pmatrix} = \begin{pmatrix}
3 & 2 & -5 \\
3 & 3 & 3
\end{pmatrix}
$$


There are nice vectors called Standard unit vectors, or sometimes "one-hot" vectors.
examples are 
$$
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \text{ and }  \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
$$
These, when multiplying, conserve specific entries during matrix multiplication.

see next: [[Matrix Algebra and Inverse]]
see previous: [[Spanning Sets and Linear Independence]]
