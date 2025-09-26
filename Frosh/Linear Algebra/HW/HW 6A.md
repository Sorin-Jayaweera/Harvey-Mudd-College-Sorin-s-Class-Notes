
## 4.3.12
Compute
A)  the characteristic polynomial of $A$,
B) the eigenvalues of $A$,
C) a basis for each eigenspace of $A$, and
D) the algebraic and geometric multiplicity of each eigenvalue of $A$

where
$$

A = 
\begin{bmatrix*}[r]
4 & 0 & 1 & 0 \\
0 & 4 & 1 & 1 \\
0 & 0 & 1 & 2 \\
0 & 0 & 3 & 0 \\
\end{bmatrix*}.
$$

A) the characteristic polynomial can be found by
$\det(A-\lambda I) = 0$
$$
\begin{align}
= \det \left( \begin{bmatrix*}[r]
4-\lambda & 0 & 1 & 0 \\
0 & 4-\lambda & 1 & 1 \\
0 & 0 & 1-\lambda & 2 \\
0 & 0 & 3 & 0-\lambda \\
\end{bmatrix*}. \right) 
\end{align}
$$

$$
= (4 - \lambda) \det \left( 
\begin{bmatrix}
4-\lambda & 1 & 1 \\
0 & 1-\lambda & 2 \\
0 & 3 & -\lambda
\end{bmatrix} \right)  + 0 + 0 + 0
$$
$$
= (4-\lambda)(4-\lambda)\det \left( 
\begin{bmatrix}
1-\lambda & 2 \\
3 & -\lambda
\end{bmatrix} \right) 
$$
$$
\begin{align}
0 &= (4-\lambda)^{2} ((1-\lambda)(-\lambda))-6) \\
0 &= (4-\lambda)^{2} ( \lambda^{2}-\lambda-6)\\
0 &=\lambda^{4}-9\lambda^{3}+18x^{2}+32x-96 \\
\end{align}
$$
This gives us the eigenvalues as solutions to the equation. 
We can set two $4-\lambda =0$ to get the first root (multiplicity 2) $\lambda=4$.
For the other, we can write $\lambda^{2}-\lambda-6=0$
which yields the roots
$$
\lambda=-2, \lambda= 3
$$
This gives us the 3 eigenvalues as 
$\boxed{\lambda \in \left\{ 4,-2,3 \right\}}$.

c) we can find the eigenspaces by substituting these eigenvalues into the matrix and finding the result.

First, the easy ones:
$$
\begin{align}
\lambda= -2: \\
\begin{bmatrix*}[r]
4+2 & 0 & 1 & 0 & | & 0 \\
0 & 4+2& 1 & 1 & | & 0\\
0 & 0 & 1+2 & 2 & | & 0\\
0 & 0 & 3 & 2 & | & 0\\
\end{bmatrix*} 
=\begin{bmatrix}
6 & 0 & 1 & 0 & | & 0 \\
0 & 6 & 1 & 1 & | & 0 \\
0 & 0 & 3 & 2 & | & 0 \\
0 & 0 & 3 & 2 & | & 0 \\
\end{bmatrix} \\
\xrightarrow {R_{4}\to  R_{4}-R_{3}} 
\begin{bmatrix}
6 & 0 & 1 & 0 & | & 0 \\
0 & 6 & 1 & 1 & | & 0 \\
0 & 0 & 3 & 2 & | & 0 \\
0 & 0 & 0 & 0 & | & 0 \\
\end{bmatrix} 
\xrightarrow {R_{3}\to  \frac{R_{3}}{3}} 
\begin{bmatrix}
6 & 0 & 1 & 0 & | & 0 \\
0 & 6 & 1 & 1 & | & 0 \\
0 & 0 & 1 & \frac{2}{3} & | & 0 \\
0 & 0 & 0 & 0 & | & 0 \\
\end{bmatrix} \\
\end{align}
$$

$$
\xrightarrow {\stackrel{R_{2}\to  R_{2}-R_{3}}{R_{1}\to  R_{1}-R_{3}} }\begin{bmatrix}
6 & 0 & 0 & -\frac{2}{3} & | & 0 \\
0 & 6 & 0 & \frac{1}{3} & | & 0 \\
0 & 0 & 1 & \frac{2}{3} & | & 0 \\
0 & 0 & 0 & 0 & | & 0 \\
\end{bmatrix} 
\xrightarrow {\stackrel{R_{1}\to  \frac{R_{1}}{6}}{R_{2}\to  \frac{R_{2}}{6}} }\begin{bmatrix}
1 & 0 & 0 & -\frac{1}{9} & | & 0 \\
0 & 1 & 0 & \frac{1}{18} & | & 0 \\
0 & 0 & 1 & \frac{2}{3} & | & 0 \\
0 & 0 & 0 & 0 & | & 0 \\
\end{bmatrix} 
$$

let $s_{1}=x_{4}$

$$
\begin{bmatrix}
x_{1} \\ x_{2} \\ x_{3} \\ x_{4}
\end{bmatrix} =S_{1}\begin{bmatrix}
\frac{1}{9} \\ -\frac{1}{18} \\ -\frac{2}{3} \\ 1
\end{bmatrix}
$$
This is our first eigenbasis.

We can now do $\lambda= 3$
$$
\begin{bmatrix*}[r]
4-\lambda & 0 & 1 & 0 \\
0 & 4-\lambda & 1 & 1 \\
0 & 0 & 1-\lambda & 2 \\
0 & 0 & 3 & 0-\lambda \\
\end{bmatrix*}
$$

$$
\begin{align}
\begin{bmatrix} 
4-3 & 0 & 1 & 0 \\
0 & 4-3 & 1 & 1 \\
0 & 0 & 1-3 & 2 \\
0  & 0& 3 & -3
\end{bmatrix} \\
= \begin{bmatrix}
1 & 0 & 1 & 0  \\
0 & 1 & 1 & 1 \\
0  & 0 & -2 & 2 \\
0  & 0& 3 & -3
\end{bmatrix}
\end{align}
$$
We can now reduce this to reduced row echelon form to find the eigenvector.
$$
\begin{align}
R_{3}\to  \frac{R_{3}}{-2}\\
\begin{bmatrix}
1 & 0 & 1 & 0  \\
0 & 1 & 1 & 1 \\
0  & 0 & 1 & -1 \\
0  & 0& 3 & -3
\end{bmatrix} \\
R_{1}\to  R_{1}-R_{3},R_{2}\to  R_{2}-R_{3},R_{4}\to  R_{4}-3R_{3} \\
\begin{bmatrix}
1 & 0 & 0 & 1 \\
0 & 1 & 0 & 2 \\
0 & 0 & 1 & -1 \\
0 & 0 & 0 & 0
\end{bmatrix}
\end{align}
$$
This gives us the equations
$$
\begin{align}
x_{1} = -x_{4} \\
x_{2} = -2x_{4} \\
x_{3} = x_{4} \\
x_{4} = x_{4}
\end{align}
$$
which has the corresponding representation
$$
\begin{bmatrix}
x_{1} \\ x_{2} \\ x_{3} \\ x_{4}
\end{bmatrix} = x_{4} \begin{bmatrix}
-1 \\ -2 \\ 1 \\ 1
\end{bmatrix}
$$

$\lambda= 4$: 
$$
\begin{align}
\begin{bmatrix*}[r]
4-4 & 0 & 1 & 0 & | & 0 \\
0 & 4-4& 1 & 1 & | & 0\\
0 & 0 & 1-4 & 2 & | & 0\\
0 & 0 & 3 & 0-4 & | & 0\\
\end{bmatrix*} \\
=  
\begin{bmatrix}
0 & 0 & 1 & 0 & | & 0\\
0 & 0 & 1 & 1 & | & 0\\
0 & 0 & -3 & 2 & | & 0\\
0 & 0 & 3 & -4 & | & 0\\
\end{bmatrix}
\end{align} 
$$
We can now reduce to find the eigenvectors
$$
\begin{align}
R_{2}\to  R_{2}-R_{1},R_{3}\to  R_{3}+3R_{1},R_{4}\to  R_{4}-3R_{1} \\
\begin{bmatrix}
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 2 \\
0 & 0 & 0 & -4
\end{bmatrix}
\end{align}
$$
Which we can see corresponds to 
$$
\begin{bmatrix}
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{bmatrix}
$$
This corresponds to the equations
$$
\begin{align}
x_{1} = x_{1} \\
x_{2} =  x_{2}
\end{align}
$$
which we can write this as
$$
\begin{bmatrix}
x_{1} \\ x_{2} \\ x_{3} \\ x_{4}
\end{bmatrix} = x_{1} \begin{bmatrix}
1 \\ 0 \\ 0 \\ 0 \\
\end{bmatrix} + x_{2} \begin{bmatrix}
0 \\ 1 \\ 0 \\ 0 \\
\end{bmatrix}.
$$
These are two more eigenvectors. We now have the eigenbases a
$$
\boxed{
\begin{bmatrix}
\frac{1}{9} \\ -\frac{1}{18} \\ -\frac{2}{3} \\ 1
\end{bmatrix},
\begin{bmatrix}
-1 \\ -2 \\ 1 \\ 1
\end{bmatrix}, \begin{bmatrix}
1 \\ 0 \\ 0 \\ 0\\
\end{bmatrix}, \begin{bmatrix}
0 \\ 1 \\ 0 \\ 0 \\
\end{bmatrix}
}
$$
$$
\boxed{
\begin{align}
\text{ We can see that we have 3 unique eigenvalues, }\\
\text{  one of which has geometric multiplicity 2 } \\
\text{ and generates two eigenvectors,  } \\
\text{  giving it geometric multiplicity 2.  } \\
\text{ The other two eigenvalues have } \\
\text{  geometric and algebraic multiplicity 1. }
\end{align}
}
$$

## 4.3.16
Let $A$ be a $2 \times 2$ matrix with eigenvectors $\mathbf{v}_1 = \begin{bmatrix*}[r]1 \\ -1\end{bmatrix*}$ and $\mathbf{v}_2 = \begin{bmatrix*}1 \\ 1\end{bmatrix*}$ corresponding to eigenvalues $\lambda_1 = \frac{1}{2}$ and $\lambda_2 = 2$, respectively. Let $\mathbf{x} = \begin{bmatrix*}5 \\ 1\end{bmatrix*}$.

Find $A^k\mathbf{x}$. What happens as $k$ becomes large (i.e., $k \rightarrow \infty$)?

$A^{k} =$
$$
\begin{bmatrix}
1  & 1\\
-1 & 1
\end{bmatrix}^{k}
$$
However, this is annoying to compute. Instead, we can represent A with a similar diagonal matrix of the eigenvalues.
$$
\text{ let } p = \begin{bmatrix}
1 & 1 \\
-1 & 1
\end{bmatrix}
$$
$\det(P) = 2$
so $P^{-1} =$ 
$$
\frac{1}{2}
\begin{bmatrix}
1 & -1 \\
1 & 1
\end{bmatrix}
$$
$$
\text{ let } b = 
\begin{bmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{bmatrix}
$$
We can now find the similar diagonal matrix. First, I find a similar matrix with the result



$$
\begin{align}
(PBP^{-1}) = \begin{bmatrix}
1 & 1 \\ -1 & 1
\end{bmatrix}\begin{bmatrix}
\frac{1}{2^{k}} & 0 \\
0 & 2^{k}
\end{bmatrix} \begin{bmatrix}
\frac{1}{2} & -\frac{1}{2} \\
\frac{1}{2} & \frac{1}{2}
\end{bmatrix} \\
= \begin{bmatrix}
1 & 1 \\ -1 & 1
\end{bmatrix}\begin{bmatrix}
\frac{1}{2^{k+1}} & -\frac{1}{2^{k+1}} \\
2^{k-1}  & 2^{k-1}
\end{bmatrix} \\
= \begin{bmatrix}
\frac{1}{2^{k+1}}+2^{k-1} & 2^{k-1}-\frac{1}{2^{k+1}} \\
2^{k-1}-\frac{1}{2^{k+1}} & \frac{1}{2^{k+1}}+2^{k-1}
\end{bmatrix}
\end{align}
$$
We can now multiply this matrix by the original vector $x$. 
We get 
$$

\begin{bmatrix}
\frac{1}{2^{k+1}}+2^{k-1} & 2^{k-1}-\frac{1}{2^{k+1}} \\
2^{k-1}-\frac{1}{2^{k+1}} & \frac{1}{2^{k+1}}+2^{k-1}
\end{bmatrix}
\begin{bmatrix}
5 \\ 1
\end{bmatrix} = \begin{bmatrix}
5 \left(\frac{1}{2^{k+1}}+2^{k-1} \right) + 2^{k-1}-\frac{1}{2^{k+1}}  \\
5(2^{k-1}-\frac{1}{2^{k+1}}) + \frac{1}{2^{k+1}}+2^{k-1}
\end{bmatrix}
$$
We can take the limit $\lim_{ k \to \infty }$. This approaches
$$
\begin{bmatrix}
\infty \\
\infty
\end{bmatrix}
$$

## 4.3.20
Let $A$ be a nilpotent matrix (that is, $A^m = O$ for some $m > 1$). Show that $\lambda = 0$ is the only eigenvalue of $A$.

We know that $A^{m}=0$ for some m.
We can find a similar matrix $D$ composed of the eigenvalues of $A$ with the following property:
$$
O=P^{-1}A^{m}P = D^{m}, D^{m} = O
$$
D is a diagonal matrix whose diagonal entries are the eigenvalues of A. Every diagonal on $D$ is zero, so zero is the only eigenvalue of $A$.

## 4.3.24c
Let $A$ and $B$ be $n \times n$ matrices with eigenvalues $\lambda$ and $\mu$, respectively. Suppose $\lambda$ and $\mu$ correspond to the same eigenvector $\mathbf{x}$. Show that, in this case, $\lambda + \mu$ is an eigenvalue of $A + B$ and $\lambda\mu$ is an eigenvalue of $AB$.

There exists some constant $c$ such that $c \lambda x = \mu x$.  
We can represent $A$ and $B$ by their similar matrices, which each contain $\lambda \text{ or } \mu$ along their diagonals. 
For example: 
$$
A \text{ is similar to } D_{a}=\begin{bmatrix}
\lambda & 0 & \dots \\
0 & \ddots\  & 0 \\
 \vdots & 0 & \ddots 
\end{bmatrix} \text{ and }  B \text{ is similar to } D_{b}=\begin{bmatrix}
\mu & 0 & \dots \\
0 & \ddots\  & 0 \\
 \vdots & 0 & \ddots 
\end{bmatrix}
$$
$AB = D_{a}D_{b} =$
$$
\begin{bmatrix}
\lambda \mu  & \dots \\
\vdots & 
\end{bmatrix}
$$
This shows that the similar diagonal matrix $AB$ contains a diagonal corresponding to 
$$
\lambda \mu
$$
Because we can construct these similar diagonal matrixes by putting eigenvalues along the diagonal, this shows that $\lambda \mu$ is an eigenvalue in $AB$. 

We can show that $A+B$ corresponds to pairwise addition of these similar matrices, so 
$$
A+B = \begin{bmatrix}
\lambda & 0 & \dots \\
0 & \ddots\  & 0 \\
 \vdots & 0 & \ddots 
\end{bmatrix}+\begin{bmatrix}
\mu & 0 & \dots \\
0 & \ddots\  & 0 \\
 \vdots & 0 & \ddots 
\end{bmatrix}
$$

$$
\begin{bmatrix}
\lambda + \mu  & 0 &  \dots \\
0  &  \ddots  & 0  \\
\vdots & 0 & \ddots

\end{bmatrix}
$$
We can see that one of the eigenvalues of this diagonal similar matrix is $\lambda+\mu$.
$$

$$
## 4.3.34
Verify the Cayley--Hamilton Theorem (see page 300) for
$$
A = 
\begin{bmatrix*}[r]
1 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix*}. 
$$

First we must find the characteristic polynomial of $A$. For this, we must compute 
$$
\det \begin{bmatrix}
1- \lambda & 1 & 0 \\
1 & -\lambda & 1  \\
0 & 1 & 1-\lambda
\end{bmatrix} = 0
$$

First we must compute the characteristic polynomial for the matrix. This can be found as

$$
\det(\begin{bmatrix}
1-\lambda  & 1 & 0 \\
1 & -\lambda & 1 \\
0 & 1 & 1-\lambda
\end{bmatrix}) = 0
$$
$$
\begin{align}
0=(1-\lambda)\det \begin{bmatrix}
-\lambda & 1\\
1 & 1-\lambda
\end{bmatrix} - (1)\det 
\begin{bmatrix}
1 & 0 \\
1 & 1-\lambda
\end{bmatrix} \\
= (1-\lambda)((-\lambda)(1-\lambda)-2)-(1-\lambda) \\
= (1-\lambda)(\lambda^{2}-\lambda-2)-1+\lambda \\
0= \lambda^{2}(1-\lambda)-\lambda(1-\lambda)-2(1-\lambda)-1+\lambda \\
0 = \lambda^{2}-\lambda^{3}-\lambda+\lambda^{2}-2+\lambda-1+\lambda \\
0 = -\lambda^{3}+2\lambda^{2}+\lambda-2

\end{align}
$$

This is $C_{a}(\lambda)$. 
By the Cayley-Hamilton theorem, $C_{a}(A)=0$
We can now begin to verify the theorem for this case:
$$
-A^{3}+2A^{2}+A-2I\stackrel{?}{=} 0
$$
By direct computation, 
$$
A^{3}=\begin{bmatrix}
3 & 3 & 2 \\
3 & 2 & 3 \\
2 & 3 & 3
\end{bmatrix}
$$
$$
A^{2} = \begin{bmatrix}
2 & 1 & 1 \\
1 & 2 & 1 \\
1 & 1 & 2
\end{bmatrix}
$$
$$
A = \begin{bmatrix}
1 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix}
$$
$$
2I = \begin{bmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{bmatrix}
$$
We can now solve the characteristic polynomial expression:
$$
-\begin{bmatrix}
3 & 3 & 2 \\
3 & 2 & 3 \\
2 & 3 & 3
\end{bmatrix} +2\begin{bmatrix}
2 & 1 & 1 \\
1 & 2 & 1 \\
1 & 1 & 2
\end{bmatrix}+\begin{bmatrix}
1 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix}-\begin{bmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{bmatrix}
$$

Simplifying,
$$
-\begin{bmatrix}
3 & 3 & 2 \\
3 & 2 & 3 \\
2 & 3 & 3
\end{bmatrix} +\begin{bmatrix}
4 & 2 & 2 \\
2 & 4 & 2 \\
2 & 2 & 4
\end{bmatrix}+\begin{bmatrix}
1 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix}-\begin{bmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{bmatrix}
$$
$$
= -\begin{bmatrix}
3 & 3 & 2 \\
3 & 2 & 3 \\
2 & 3 & 3
\end{bmatrix} +\begin{bmatrix}
4 & 2 & 2 \\
2 & 4 & 2 \\
2 & 2 & 4
\end{bmatrix}+\begin{bmatrix}
-1 & 1 & 0 \\
1 & -2 & 1 \\
0 & 1 & -1
\end{bmatrix}
$$
$$
= -\begin{bmatrix}
3 & 3 & 2 \\
3 & 2 & 3 \\
2 & 3 & 3
\end{bmatrix} +\begin{bmatrix}
3 & 3 & 2 \\
3 & 2 & 3 \\
2 & 3 & 3
\end{bmatrix}
$$
$$
= \begin{bmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}
$$
quod erat demonstrandum.
## 4.3.36
Use the Cayley--Hamilton Theorem (see page 300) to compute $A^3$ and $A^4$ by expressing each as a linear combination of $I$, $A$, and $A^2$, where
$$
A = 
\begin{bmatrix*}[r]
1 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix*}. 
$$

We found the characteristic function of A as
$$
0=-A^{3}+2A^{2}+A-2I
$$
This can be rewritten as 
$$
\boxed{
A^{3}=2A^{2}+A-2I
}
$$
We can multiply to find $A^{4}$ by multiplying both sides by $A$.
This yields:
$$
\begin{align}
A^{4}=(2A^{3})+A^{2}-2A \\
\text{ we can substitute for what we know as  } A^{3} \\
A^{4} = (2(2A^{2}+A-2I))+A^{2}-2A \\
\end{align}
$$
$$
\boxed{
A^{4} = 5A^{2}-4I
}
$$


## 4.4.8
Determine whether the matrix $A$ is diagonalizable and, if so, find an invertible matrix $P$ and a diagonal matrix $D$ such that $P^{-1}AP = D$, where

$$
\begin{bmatrix*}[r] 5 & 2 \\ 2 & 5\end{bmatrix*}. 

$$
We can look at the characteristic polynomial of this matrix:
$$
\begin{align}
\det(\begin{bmatrix}
5-\lambda & 2 \\
2 & 5 - \lambda
\end{bmatrix}) = (5-\lambda)^{2}-4 = 0 \\
0 = (\lambda^{2}-10\lambda+21) \\
0 = (x-3)(x-7))
\end{align}
$$
This gives us two eigenvalues 3 and 7. With two unique eigenvalues, there must be two eigenvectors. This means that the geometric multiplicity is two, as the the algebraic multiplicity. Thus the matrix is diagonalizable. 
The diagonal matrix $D$ is 
$$
\begin{bmatrix}
3 & 0 \\
0 & 7
\end{bmatrix}
$$
To find $P$ and $P^{-1}$, we must find the eigenvectors associated with these values.

We can write this out as
$$
\begin{bmatrix}
5 - 3 & 2 \\
2 & 5-3
\end{bmatrix} = \begin{bmatrix}
2 & 2 \\
0 & 0
\end{bmatrix}
$$
which gets the first eigenvector 
$$
\begin{bmatrix}
1\\ -1
\end{bmatrix}
$$
We can find the other eigenvector as
$$
\begin{bmatrix}
5-7 & 2 \\
2 & 5-7
\end{bmatrix} = \begin{bmatrix}
-2 & 2 \\
2 & -2
\end{bmatrix} = \begin{bmatrix}
-2 & 2 \\
0 & 0
\end{bmatrix}
$$
which yields the eigenvector 
$$
\begin{bmatrix}
1 \\ 1
\end{bmatrix}
$$
We can now construct $P =$
$$
\boxed{
\begin{bmatrix}
1  & 1 \\
-1 & 1
\end{bmatrix}
}
$$


## 4.4.10
Determine whether the matrix $A$ is diagonalizable and, if so, find an invertible matrix $P$ and a diagonal matrix $D$ such that $P^{-1}AP = D$, where
$$
A = 
\begin{bmatrix*}[r]
3 & 1 & 0 \\
0 & 3 & 1 \\
0 & 0 & 3
\end{bmatrix*}. 
$$
For A to be diagonalizable, there must exist three linearly independent eigenvectors that describe it.

We can find the eigenvalues as solutions to 
$$
\begin{align}
\det(A-\lambda I)=0 \\
\det \left( \begin{bmatrix}
3 - \lambda & 1 & 0 \\
0 & 3-\lambda & 1 \\
0 & 0 & 3 - \lambda
\end{bmatrix} \right) 
\end{align}
$$
This is a triangular matrix, so the determinant is just the product of the diagonal entries.
Thus, $\det(A-\lambda I) = (3-\lambda)^{3}$.
This means $\lambda=3$.
This has Algebraic multiplicity 3. 

this makes the eigenvector equation:
$$
\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{bmatrix}
$$
We can see that this has geometric multiplicity 2. 
By the property that diagonalizable matrices must have equal geometric and algebraic multiplicity for eigenvectors and eigenvalues respectively, the matrix is not diagonalizable. 

## 4.4.22

Use the method of Example 4.29 to compute the indicated power of the matrix:
$$
A=\begin{bmatrix*}[r]
2 & 0 & 1 \\
1 & 1 & 1 \\
1 & 0 & 2
\end{bmatrix*}^k. 
$$


First, we must find the eigenvalues of the matrix and the following eigenvectors. By definition, eigenvalues of the matrix satisfy $\det(A-\lambda I)=0$.
We can calculate this with cofactor expansion:
$$
\begin{align}
\det(A-\lambda I) =  \\
(2-\lambda)\det(\begin{bmatrix}
1-\lambda & 1 \\
0 & 2- \lambda
\end{bmatrix})\\
\text{ which results in the characteristic equation }  \\
(2-\lambda)((1-\lambda)(2-\lambda)-1) \\
= -\lambda^{3}+5\lambda^{2}-7\lambda+3 \\
= -(\lambda-1)^{2}(\lambda-3)\\
\lambda_{1}=1,\lambda_{2}=1,\lambda_{4}=3
\end{align}
$$

We can now find our eigenvectors:
for $\lambda_{1}=1:$
$$
\begin{align}
A-\lambda I = \begin{bmatrix}
1 & 0 & 1 \\
1 & 0 & 1 \\
1 & 0 & 1
\end{bmatrix} \to   \begin{bmatrix}
1 & 0 & 1 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}
\end{align}
$$

We have three equations that we generate:
$$
\begin{align}
x_{1}=-x_{3} \\
x_{2}=x_{2} \\
x_{3}=x_{3}
\end{align}
$$
Which can be expressed as 
$$
x_{2}\begin{bmatrix}
0 \\ 1 \\ 0
\end{bmatrix} + x_{3} \begin{bmatrix}
-1 \\ 0\\ 1
\end{bmatrix}
$$
This corresponds to the eigenvectors
$$
\begin{bmatrix}
-1 \\ 0 \\ 1
\end{bmatrix}\text{ and }  \begin{bmatrix}
0  \\ 1 \\ 0
\end{bmatrix}
$$

for $\lambda_{2}=3$:
$$
\begin{align}
A-\lambda I = \begin{bmatrix}
-1 & 0 & 1 \\
1 & -2 & 1 \\
1 & 0 & -1
\end{bmatrix} \\
\xrightarrow {R_{1}\leftrightarrow R_{2} }
\begin{bmatrix}
1 & -2 & 1 \\
-1 &0 & 1 \\
1 & 0 & -1 
\end{bmatrix} \xrightarrow {\stackrel{R_{2}\to  R_{2}+R_{1}}{R_{3}\to  R_{3}-R_{1}} } \begin{bmatrix}
1 & -2 & 1 \\
0 & -2 & 2 \\
0 & 2 & -2
\end{bmatrix} \\
\xrightarrow {\stackrel{R_{1}\to  R_{1}-R_{2}}{R_{3}\to  R_{3}+R_{2}} }\begin{bmatrix}
1 & 0 & -1 \\
0 & -2 & 2 \\
0 & 0 & 0
\end{bmatrix} \xrightarrow {R_{2}\to  \frac{R_{2}}{-2}} 
\begin{bmatrix}
1  & 0 & -1 \\
0 & 1 & -1 \\
0 & 0 & 0
\end{bmatrix} 
\end{align}
$$
We can write this as equations
$$
\begin{align}
x_{1} = x_{3} \\
x_{2} = x_{3} \\
x_{3} = x_{3}
\end{align}
$$
Which corresponds to the eigenvector
$$
\begin{bmatrix}
1 \\ 1  \\ 1
\end{bmatrix}
$$

We can write a similar diagonal matrix $D$ with the eigenvalues as the values along the diagonal.
this gets 
$$
D = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 3
\end{bmatrix}
$$
Because one of the eigenvalues has multiplicity 2, I want to check that this is valid.

We can use the eigenvectors to fill the matrix $P$ that satisfies
$P^{-1}AP=D$.
P is constructed as the set of eigenvectors that we just found, aka:
$$
P=\begin{bmatrix}
-1  & 0 & 1\\
0  & 1 & 1\\
1 & 0  & 1\\
\end{bmatrix}
$$

This gives us the inverse matrix as
$$
P^{-1} = \begin{bmatrix}
-\frac{1}{2} & 0 & \frac{1}{2} \\
-\frac{1}{2} & 1 & -\frac{1}{2} \\
\frac{1}{2} & 0 & \frac{1}{2}
\end{bmatrix}
$$
We can now compute $D$:
$$
D = \begin{bmatrix}
-\frac{1}{2} & 0 & \frac{1}{2} \\
-\frac{1}{2} & 1 & -\frac{1}{2} \\
\frac{1}{2} & 0 & \frac{1}{2}
\end{bmatrix}
\begin{bmatrix*}[r]
2 & 0 & 1 \\
1 & 1 & 1 \\
1 & 0 & 2
\end{bmatrix*}
\begin{bmatrix}
-1  & 0 & 1\\
0  & 1 & 1\\
1 & 0  & 1\\
\end{bmatrix}
$$

$$
\begin{align} 
\begin{bmatrix}
-\frac{1}{2} & 0 & \frac{1}{2} \\
-\frac{1}{2} & 1 & -\frac{1}{2} \\
\frac{1}{2} & 0 & \frac{1}{2} \\
\end{bmatrix}
\begin{bmatrix} 
-1 & 0 & 1 \\
0 & 1 & 3 \\
1 & 0 & 3
\end{bmatrix} \\
= \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 3
\end{bmatrix}
\end{align}
$$


This matrix $D$ is similar to $A$. Doing the diagonal as eigenvalues worked, even with multiplicity! That was surprising! 
We can now then take $D^{k}$. 
$$
\begin{align}
D^{k}=\\
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 3
\end{bmatrix}^{k}
 \\
= \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 3^{k}
\end{bmatrix}
\end{align}
$$
We can rewrite the expression $P^{-1}A^{k}P=D^{k}$ as
$$
A^{k}= P^{-1}D^{k}P
$$
$$
\begin{align}
A^{k} =  \begin{bmatrix}
-\frac{1}{2} & 0 & \frac{1}{2} \\
-\frac{1}{2} & 1 & -\frac{1}{2} \\
\frac{1}{2} & 0 & \frac{1}{2}
\end{bmatrix}\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 3^{k}
\end{bmatrix}\begin{bmatrix}
-1  & 0 & 1\\
0  & 1 & 1\\
1 & 0  & 1\\
\end{bmatrix} \\
= \begin{bmatrix}
-\frac{1}{2} & 0 & \frac{1}{2} \\
-\frac{1}{2} & 1 & -\frac{1}{2} \\
\frac{1}{2} & 0 & \frac{1}{2}
\end{bmatrix} \begin{bmatrix}
-1 & 0 & 3^{k} \\
0 & 1 & 3^{k} \\
1 & 0 & 3^{k}
\end{bmatrix}\\
A^{k}= \begin{bmatrix}
\frac{3^{k}+1}{2} & 0 & \frac{3^{k}-1}{2} \\
\frac{3^{k}-1}{2} & 1 & \frac{3^{k}-1}{2} \\
\frac{3^{k}-1}{2}  & 0 & \frac{3^{k}+1}{2}
\end{bmatrix}
\end{align}
$$

## 4.4.26
Find all real values of $k$ for which $A$ is diagonalizable, where
$$
A = 
\begin{bmatrix*}[r] k & 1 \\ 1 & 0 \end{bmatrix*}. 
$$
By definition, an $n\times n$ matrix is diagonalizable if and only if $A$ has $n$ linearly independent eigenvectors.

We can find the eigenvalues by
$$
\begin{align}
\det(A-\lambda I)=0\\
\to ( k-\lambda)(-\lambda) - 1 = 0 \\
\to   \lambda^{2}-k \lambda-1=0 \\
\lambda_{1}= \frac{k+\sqrt{ k^{2}+4 }}{2} \\
\lambda_{2}= \frac{k-\sqrt{ k^{2}+4 }}{2}
\end{align}
$$
For the eigenvectors to be linearly independent, they need two different $\lambda$ values that satisfy $|\lambda_{1}| \neq |\lambda_{2}|$
This means that 
$$\begin{align}
k^{2}+4 \neq 0 \\
\to   k \neq 2i
\end{align}
$$
Thus, $A$ is diagonalizable for all values $k \in \mathbb{R}^{n}$. 

