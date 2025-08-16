
## Prove Theorem 4.19.

 Suppose the $n \times n$ matrix $A$ has eigenvectors $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_m$ with corresponding eigenvalues $\lambda_1, \lambda_2, \dots, \lambda_m$. If $\mathbf{x}$ is a vector in $\mathbb{R}^n$ that can be expressed as a linear combination of these eigenvectors, say
$$

\mathbf{x} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \cdots + c_m\mathbf{v}_m 
$$
then, for any integer $k$,
$$
A^kx = c_1 \lambda_1^k \mathbf{v}_1 + c_2 \lambda_2^k \mathbf{v}_2 + \cdots + c_m \lambda_m^k \mathbf{v}_m. 
$$
 -----------------------------------------------------------
Using the first equation, we can rewrite the second equation as
$$
\begin{align}
A^{k}(c_{1}v_{1}+\dots +c_{m}v_{m}) \\
 =A^{k}c_{1}v_{1}+\dots+A^{k}c_{m}v_{m} \\
 =c_{1}A^{k}v_{1}+\dots+c_{m}A^{k}v_{m}
\end{align}
$$

  We can use the property of eigenvectors and eigenvalues such that
$$
A\vec{v} = \lambda \vec{v} \implies A^{k}\vec{v}=\lambda^{k}\vec{v}
$$

This allows us to rewrite the expression as
$$
\begin{align}
c_{1}\lambda_{1}^{k} \vec{v}_{1} + c_{2}\lambda_{2}^{k}\vec{v}_{2}+\dots+c_{m}\lambda_{m}^{k}\vec{v}_{m}
\end{align}
$$
QED.

## 4.4.42
Prove that if $A$ is similar to $B$, then $A^T$ is similar to $B^T.$

We can use the property that there exists a matrix $P$ made of the eigenvectors of $A$ that satisfies 
$$
P^{-1}AP=B
$$
We can now manipulate this expression:
$$
\begin{align}
(P^{-1}AP)^{T}=B^{T}  \\
B^{T}= ((P^{-1}A)P)^{T}\\
B^{T}= P^{T}(P^{-1}A)^{T} \\
B^{T}= P^{T}A^{T}P^{-1,T}
\end{align}
$$
We can rewrite this as
$$
P^{-1,T}B^{T}P^{T}=A
$$
We can say that $P^{T}$ is a matrix that satisfies the same equality between $B^{T} \text{ and } A^{T}$. Thus, $A^{T}$ is similar to $B^{T}$. 

## 5.1.28

Prove that an orthogonal $2 \times 2$ matrix must have the form
$$
\begin{bmatrix*}[r] a & -b \\ b & a \end{bmatrix*}
	\text{ \ or \ }
	\begin{bmatrix*}[r] a & b \\ b & -a \end{bmatrix*}
$$
where $\begin{bmatrix*}[r] a \\ b \end{bmatrix*}$ is a unit vector.

let
$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$
We can write generally that for a general $2\times 2$ matrix to be orthonormal,
$$
\begin{align}
\begin{bmatrix}
a \\ c
\end{bmatrix} \cdot \begin{bmatrix}
b \\ d
\end{bmatrix} = 0 \\
ab + cd= 0  \\
ab=-cd
\end{align} 
$$

We must also enforce that the magnitudes of $\left| \begin{bmatrix}a \\ c\end{bmatrix} \right|= \left| \begin{bmatrix}b \\ d\end{bmatrix} \right|$,
so $a^{2}+c^{2}=b^{2}+d^{2}$ since $\begin{bmatrix}a \\ c\end{bmatrix}$ is a unit vector. 
2 trivial solutions to this system are $c=b,d=-a$, or $c=-b,d=a$.

We can show this more rigorously. We the relationship that for any orthonormal matrix $Q$, $QQ^{T}=I$. Thus,
$$
\begin{align}
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix} \begin{bmatrix}
a & c \\
b & d
\end{bmatrix} = \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix},  \\
\begin{bmatrix}
a^{2}+b^{2} & ac + db \\
ac+db & c^{2}+d^{2}
\end{bmatrix} = \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
\end{align}
$$

We can write out these equations
$$
\begin{align}
a^{2}+b^{2}=1 \\
c^{2}+d^{2}=1 \\
ac+db=0
\end{align}
$$
Which we can now manipulate:
$$
\begin{align}
a^{2}=1-b^{2}\\
c^{2}=1-d^{2} \\
(ac)^{2}=(db)^{2}
\end{align}
$$
Which simplifies to
$$
\begin{align}
a^{2}=1-b^{2} \\
d^{2}=1-c^{2} \\
(1-b^{2})c^{2} = (1-c)b^{2} \\
c^{2}-c^{2}b^{2}=b^{2}-c^{2}b^{2} \\
b^{2}=c^{2} \\
c=\pm b
\end{align}
$$
We can now use our original expression:
$$
\begin{align}
a^{2}+c^{2}=b^{2}+d^{2} \\
a^{2}+b^{2}=b^{2} +d^{2} \\
a^{2}=d^{2} \\
d = \pm a
\end{align}
$$
Thus, $c=\pm b,\text{ and } d=\pm a$

Using the fact that $ac+db=0$, $ac=-db$, $a(\pm b)=-(\pm a)(b)$
We get that the signs attached to c and d must be opposite.
QED.
## B
Using part (a), show that every orthogonal $2 \times 2$ matrix is of the form
$$
\begin{bmatrix*}[r]
                    \text{cos}\;\theta & -\text{sin}\;\theta \\
                    \text{sin}\;\theta & \text{cos}\;\theta
                \end{bmatrix*}
                \text{ \ or  \ }
                \begin{bmatrix*}[r]
                    \text{cos}\;\theta & \text{sin}\;\theta \\
                    \text{sin}\;\theta & -\text{cos}\;\theta
                \end{bmatrix*}
$$

where $0 \leq \theta < 2\pi$.

Having proven in part $A$ that the matrix must follow the form
$$
\begin{bmatrix}
a & -b \\
b & a
\end{bmatrix}\text{ or } 
\begin{bmatrix}
a & b \\
b & -a
\end{bmatrix}
$$, we can rewrite.
let $a = \cos\theta,b=\sin\theta$.
This statement becomes equivalent to 
$$
\begin{bmatrix*}[r]
                    \text{cos}\;\theta & -\text{sin}\;\theta \\
                    \text{sin}\;\theta & \text{cos}\;\theta
                \end{bmatrix*}
                \text{ \ or  \ }
                \begin{bmatrix*}[r]
                    \text{cos}\;\theta & \text{sin}\;\theta \\
                    \text{sin}\;\theta & -\text{cos}\;\theta
                \end{bmatrix*}
$$
