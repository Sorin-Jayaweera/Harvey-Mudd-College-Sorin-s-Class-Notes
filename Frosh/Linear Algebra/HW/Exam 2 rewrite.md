## A
![[Pasted image 20240416174643.png]]
![[Pasted image 20240416174709.png]]
In the above, Problem 2 part 2 is marked incorrectly. 
If the null space of A is one dimensional, then there is a line where every value is scaled to zero. This corresponds to multiplication by the eigenvalue "zero". Thus, A must have zero as an eigenvalue.

![[Pasted image 20240416175014.png]]
This page has an arithmatic error in the very last step. Take the final answer in the above and replace the bottom middle value with 
$$
\begin{align}
-\frac{2}{\sqrt{ 6 }}
\end{align}
$$



![[Pasted image 20240322183759.png]]
I, Sorin Jayaweera, agree to the above. 3/22/2024

![[Pasted image 20240322183845.png]]

To find the eigenvalues off A, we must first find the solution to the equation
$\det(A-\lambda I)= 0$
This can be written as
$$
\begin{align}
\det(\begin{bmatrix}
2-\lambda & 0 & 3 \\
0 & 2-\lambda & 3 \\
0 & 0 & 5-\lambda
\end{bmatrix}) = 0 \\
= (2-\lambda ) \det(\begin{bmatrix}
2-\lambda & 3 \\
0 & 5-\lambda
\end{bmatrix}) \\
= (2-\lambda)((2-\lambda)(5-\lambda)-(3*0)) \\
= (2-\lambda)(2-\lambda)(5-\lambda) \\
\end{align}
$$
The solutions to this characteristic polynomial are

$$
2,2,\text{ and }  5
$$
The eigenvalue 2 has algebraic multiplicity 2. 

We (there is no we, it just feels weird to say "I") can now solve for the eigenvectors:
First, the eigenvector associated to $\lambda= 2$
$$
\begin{bmatrix}
0 & 0 & 3 \\
0 & 0 & 3 \\
0 & 0 & 3
\end{bmatrix}
$$
This reduces to 
$$
\begin{bmatrix}
0 & 0 & 1  & | & 0 \\
0 & 0 & 0  & | & 0\\
0 & 0 & 0 & | & 0
\end{bmatrix}
$$
Which has the equation
$$
\begin{align}
x_{3}=0,  \\
x_{1}=x_{1} \\
x_{2}=x_{2}
\end{align}
$$
And can be written as 
$$
\begin{pmatrix}
x_{1} \\
x_{2} \\
x_{3} 
\end{pmatrix} = x_{1} \begin{pmatrix}
1 \\ 0 \\ 0
\end{pmatrix}+ x_{2} \begin{pmatrix}
0 \\ 1 \\ 0
\end{pmatrix}
$$
And thus has the eigenvectors
$$
\begin{pmatrix}
1 \\ 0 \\ 0
\end{pmatrix}, \begin{pmatrix}
0 \\ 1 \\ 0
\end{pmatrix}
$$

Now, $\lambda= 5$
$$
\begin{bmatrix}
-3 & 0 & 3 \\
0 & -3 & 3 \\
0 & 0 & 0
\end{bmatrix}
$$
We can row reduce this easily to
$$
\begin{bmatrix}
-1 & 0 & 1 \\
0 & -1 & 1 \\
0 & 0 & 0
\end{bmatrix}
$$
This corresponds to the equations
$$
\begin{align}
-x_{1}=-x_{3} \\
-x_{2}=-x_{3}\\
x_{3}=x_{3} \\
\end{align}
$$
This has the eigenvector $\begin{pmatrix}1\\1\\1\\\end{pmatrix}$

Thus the eigenspace is represented by the basis
$$
\begin{bmatrix}
1 & 1 & 0 \\
1 & 0 & 1 \\
1 & 0 & 0
\end{bmatrix}
$$


![[Pasted image 20240322183853.png]]
Rigorously:
$$
\begin{align}
\vec{v}\in  w^{\perp} \\
\text{ implies } \\
\vec{v}\perp \vec{w} \, \forall \vec{w}\in  W  \\
\text{ because U is a subspace of W, }\\
\vec{v}\perp \vec{u} \,  \forall \,  \vec{u} \in   U  \\
\end{align}
$$
All vectors $v$ from $w^{\perp}$ are in $U^{\perp}$,
Therefore, $\vec{w}^{\perp}$ is a subset of $u^{\perp}$.

Geometrically:
$W$ is either smaller than $W$ or $U$ is $W$. In the case where $U=W$, then $U^{\perp}=W^{\perp}$. Otherwise, $U$ having less vectors than $W$ means that it has more potential perpendicular vectors. Because decreasing the dimension of $U$ doesn't change the viability of the perpendicular vectors that $U^{\perp}$ shared with $W^{\perp}$, all of those vectors in $W^{\perp}$ are in $U^{\perp}$. Thus, $W^{\perp}$ is a subspace of $U^{\perp}$. 



![[Pasted image 20240322183901.png]]

* denoting the vectors in $A$ as $x_{1},x_{2},x_{3}$ and the orthogonal basis as $X_{1},X_{2},X_{3}$
For the gram-schmidt process, I will choose $\begin{pmatrix}1\\1\\1\\1\end{pmatrix}$ as the original vector. With this, $X_{1}=x_{1}$ 
The next vector in the basis is $\begin{pmatrix}-1\\4\\4\\-1\end{pmatrix}-proj_{x_{1}}x_{2}$
The projection of $x_{2}$ onto $x_{1}$ is 

$$
\frac{x_{1}\cdot x_{2}}{\left| x_{1} \right|^{2}}x_{1}
$$
This means that the projection is 
$$
\begin{align}
\frac{(1,1,1,1)\cdot(-1,4,4,-1)}{(1,1,1,1)\cdot(1,1,1,1)}\begin{pmatrix}
1\\1\\1\\1
\end{pmatrix}\\
= \frac{-1+4+4-1}{4}\begin{pmatrix}
1\\1\\1\\1\\
\end{pmatrix} \\
= \frac{3}{2}\begin{pmatrix}
1\\1\\1\\1
\end{pmatrix}
\end{align}
$$
This gives us the new vector in the basis as 
$$
\begin{align}
\begin{pmatrix}-1\\4\\4\\-1\end{pmatrix}-\frac{3}{2}\begin{pmatrix}
1\\1\\1\\1
\end{pmatrix} \\
= \begin{pmatrix}
-\frac{5}{2} \\
\frac{5}{2} \\
\frac{5}{2} \\
-\frac{5}{2} \\
\end{pmatrix}
\end{align}
$$
We can see that this $X_{1}$ and $X_{2}$ are orthogonal!
$$
\begin{align}\begin{pmatrix}
1\\1\\1\\1\\
\end{pmatrix} \cdot
\begin{pmatrix}
-\frac{5}{2} \\
\frac{5}{2} \\
\frac{5}{2} \\
-\frac{5}{2} \\
\end{pmatrix}\\
= -\frac{5}{2}+\frac{5}{2}+\frac{5}{2}-\frac{5}{2}=0\\
\end{align}
$$
We have the first two basis vectors as
$$
\begin{bmatrix}
1 & -\frac{5}{2} \\
1 & \frac{5}{2} \\
1 & \frac{5}{2} \\
1 & -\frac{5}{2}
\end{bmatrix}
$$
We can now find $X_{3}$ by performing $x_{3}-proj_{x_{1}}x_{3}-proj_{x_{2}}x_{3}$

$x_{3}=\begin{pmatrix}4\\-2\\2\\0\end{pmatrix}$
First, the projection of $x_{3}$ onto $x_{1}$

$$
\begin{align}
\frac{x_{3}\cdot x_{1}}{\left| x_{1} \right|^{2}}x_{1} \\
= \frac{4-2+2}{4} x_{1} \\
= x_{1}
\end{align}
$$
Now the projection of $x_{3}$ onto $x_{2}$
$$
\begin{align} \\
\frac{x_{3}\cdot x_{2}}{x_{2}\cdot x_{2}}x_{2} \\
= \frac{(4,-2,2,0)\cdot\left( -\frac{5}{2}, \frac{5}{2}, \frac{5}{2}, -\frac{5}{2} \right)}{\left( 4\frac{5}{2}^{2} \right)}x_{2} \\
= \frac{-\frac{20}{2}- \frac{10}{2} + \frac{10}{2}}{25}x_{2} \\
= -\frac{2}{5}\begin{pmatrix}
-\frac{5}{2} \\
\frac{5}{2} \\
\frac{5}{2} \\
-\frac{5}{2} \\
\end{pmatrix} \\
= \begin{pmatrix}
1 \\-1 \\ -1 \\ 1
\end{pmatrix}
\end{align}
$$
We can now find the last orthogonal vector:
$$
\begin{align}
X_{3}=\begin{pmatrix}4\\-2\\2\\0\end{pmatrix}-\begin{pmatrix}
1\\1\\1\\1\\
\end{pmatrix}-\begin{pmatrix}
1 \\-1 \\ -1 \\ 1
\end{pmatrix}\\
X_{3} = \begin{pmatrix}
3\\-3\\1\\-1
\end{pmatrix} - \begin{pmatrix}
1 \\-1 \\ -1 \\ 1
\end{pmatrix}\\
= \begin{pmatrix}
2 \\ -2 \\ 2 \\ -2
\end{pmatrix}
\end{align}
$$

We can now check that this is orthogonal to both other basis vectors:

Thus, the orthogonal vectors for $col(A)$ is
$$

\begin{bmatrix}
\begin{pmatrix}
2 \\ -2 \\ 2 \\ -2
\end{pmatrix},  & \begin{pmatrix}
-\frac{5}{2} \\ \frac{5}{2}\\ \frac{5}{2} \\ -\frac{5}{2}
\end{pmatrix}, & \begin{pmatrix}
1\\1\\1\\1\\
\end{pmatrix}
\end{bmatrix}
$$
Normalizing each vector, this becomes the orthogonal basis 

$$
Q=\begin{bmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & -\frac{1}{2} & -\frac{1}{2}
\end{bmatrix}
$$

Using this orthogonal matrix, we can now perform QR factorization to represent $A$ by the upper triangular $R$ and the orthogonal matrix $Q$. 

$A=QR$
Using the fact that $Q^{-1}=Q^{T}$,
$Q^{T}A=R$

$$
Q^{T}=\begin{bmatrix}
\frac{1}{2} & \frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} & -\frac{1}{2}
\end{bmatrix}
$$
This becomes the nasty direct computation:

$$
\begin{bmatrix}
\frac{1}{2} & \frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} & -\frac{1}{2}
\end{bmatrix}\begin{bmatrix}
1 & -1 & 4 \\
1 & 4 & -2  \\
1 & 4 & 2 \\
1 & -1 & 0
\end{bmatrix}
$$

This becomes
$$
\begin{bmatrix}
4*\frac{1}{2} & -\frac{1}{2}+2+2-\frac{1}{2} & 2-1+1 \\
0 & 5 & -2 \\
0 & 0 & 4
\end{bmatrix}
$$

$$
R = \begin{bmatrix}
2 & 3 & 2 \\
0 & 5 & -2 \\
0 & 0 & 4
\end{bmatrix}
$$
Thus, we finally have the $QR$ factorization of $A$ by direct computation (I'm sure I remember there being a nicer way to find it then just this?)

$$
\boxed{
A=\begin{bmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & -\frac{1}{2} & -\frac{1}{2}
\end{bmatrix}
\begin{bmatrix}
2 & 3 & 2 \\
0 & 5 & -2 \\
0 & 0 & 4
\end{bmatrix}
}
$$
