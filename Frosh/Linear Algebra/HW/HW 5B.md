
## 4.2.55
If $A$ is $idempotent$ (that is, $A^2 = A$), find all possible values of $\text{det} A$.

The zero matrix and the identity matrices are both idempotent. The zero matrix will always be zero when multiplied with anything. By definition, the identity matrices don't apply transformations, so $I^{2}=0$. 
$\det(\begin{bmatrix}\vec{0}&\dots&\vec{0}\end{bmatrix})$ = 0.
$\det(I) = 1$. 

We can see that no other values for the determinant exist. For $A^{2}=A$ to be true, $A$ must not have an effect on the space that it is acting on. 
We can see this by the fact that $n^{2}>n\text{   }\forall n\neq 0\text{ or } 1$. 

## 4.3.41
Let $A$ and $B$ be $n\times n$ matrices. Prove that the sum of *all* of the eigenvalues of $A+B$ is the sum of all the eigenvalues of $A$ and $B$ individually. Prove that the product of all the eigenvalues of $AB$ is the product of all the eigenvalues of $A$ and $B$ individually.

You may use the following fact:


Let $\lambda_1, \lambda_2, \dots, \lambda_n$ be a complete set of eigenvalues (repetitions included) of the $n \times n$ matrix $A.$ Then
$$
\begin{align*}
\text{det} A = \lambda_1 \lambda_2 \cdots \lambda_n, \quad \text{and} \\
\text{tr} A = \lambda_1 + \lambda_2 + \cdots + \lambda_n \,.
\end{align*}
$$

1) Prove that the sum of *all* of the eigenvalues of $A+B$ is the sum of all the eigenvalues of $A$ and $B$ individually.
We can use the fact that 
$tr(A+B) = tr(A)+tr(B)$
we can write this out as 
$tr(A+B) = \lambda_{1,a} + \lambda_{1,b} +\dots+\lambda_{n,a}+\lambda_{2,b}$ 
Which gives the values of all of the eigenvalues in $A+B$ as
$$
(\lambda_{1,a} + \lambda_{1,b}) +\dots+ (\lambda_{n,a}+\lambda_{2,b})
$$
This gives us each eigenvalue in $A+B$ as $\lambda_{n,a}+\lambda_{n,b}$ for all n in $A$.  

3) Prove that the product of all the eigenvalues of $AB$ is the product of all the eigenvalues of $A$ and $B$ individually.
We can represent this with properties of the determinant:
$\det(AB)=\det(A)\det(B)$. 
We can now represent this with eigenvalues:

$\det A=\lambda_{1a} \lambda_{2a} \cdots \lambda_{n,a},$
$\det B=\lambda_{1b} \lambda_{2b} \cdots \lambda_{n,b}$
$\det(AB) = \lambda_{1,a}\lambda_{1,b}\dots \lambda_{n,a}\lambda_{n,b}$
By the definition that the determinant of a matrix is the product of it's eigenvalues, this is equivalent to the statement that each eigenvalue in $AB$ is given by $\lambda_{n,a}\lambda_{n,b}$ for all $n$. 



