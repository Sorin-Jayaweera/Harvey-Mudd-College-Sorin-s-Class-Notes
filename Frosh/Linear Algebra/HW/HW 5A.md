
## 4.1.24
Use the method of Example 4.5 to find all of the eigenvalues of the matrix $A$, where
$$
A = \begin{bmatrix*}[r] 2 & 4 \\ 6 & 0 \end{bmatrix*}. 
$$
Give bases for each of the corresponding eigenspaces. Illustrate the eigenspaces and the effect of multiplying eigenvectors by $A$ as in Figure 4.8.

To find the eigen vectors, we need a solution to
$$
\begin{align}
A\vec{v}=\lambda \vec{v} \\
A\vec{v}=(\lambda I)\vec{v} \\
(A-\lambda I)\vec{v}=0 \\
\text{ which we can express similarly as } \\
\det(A-\lambda I)=0 \\
\text{ this gets us the expression } \\
\det \left( \begin{bmatrix}
2-\lambda & 4 \\
6 & -\lambda
\end{bmatrix} \right) =0 \\
\implies -2\lambda+\lambda^{2}-24=0 \\
\implies (\lambda-6)(\lambda+4)=0 \\
\implies \lambda= 6, \lambda= -4
\end{align}
$$
This gives us the eigenvalues 6 and -4. We can now find the eigenvectors as solutions to
$$
\begin{bmatrix}
2+4 & 4 \\
6 & 4
\end{bmatrix}\begin{bmatrix}
x\\ y
\end{bmatrix} = \vec{0}
\text{ and }  
\begin{bmatrix}
2-6 & 4 \\
6 & -6
\end{bmatrix}\begin{bmatrix}
x \\ y
\end{bmatrix} = \vec{0}.
$$

We can solve this with an augmented matrix
$$
\begin{bmatrix}
6 & 4 & | & 0 \\
6 & 4 & | & 0
\end{bmatrix} \xrightarrow {R_{2}\to  R_{2}-R_{1}}
\begin{bmatrix}
6 & 4 & | & 0 \\
0 & 0 & | & 0
\end{bmatrix}
$$
which gives the solution of vectors $6x+4y=0$
or $y=-\frac{6}{4}x$
This gives us the first basis:
$$
\begin{bmatrix}
x \\ y
\end{bmatrix} = t\begin{bmatrix}
1 \\ -\frac{6}{4}
\end{bmatrix}
$$
We can do the same for the other eigenvalue that we found:
$$
\begin{align}
\begin{bmatrix}
2-6 & 4 \\
6 & -6
\end{bmatrix}\begin{bmatrix}
x \\ y
\end{bmatrix} = \vec{0} \\ \text{solves}
\begin{bmatrix}
-4  & 4  & | & 0\\ 6 & -6 &  | & 0 
\end{bmatrix} \xrightarrow {\stackrel{R_{1}\to  \frac{R_{1}}{4}}{r_{2}\to  \frac{R_{2}}{6}} } \\
\begin{bmatrix}
-1 & 1 & | & 0 \\
1 & -1 & | & 0
\end{bmatrix} \xrightarrow {R_{1}\to  R_{1}+R_{2}} 
\begin{bmatrix}
0 & 0  & | & 0 \\
1 & -1 & | & 0
\end{bmatrix}
\end{align}
$$
which gives the solution as
$x - y =0, x = y$
$$
\begin{bmatrix}
x\\ y
\end{bmatrix} = t\begin{bmatrix}
1 \\ 1
\end{bmatrix}
$$

We now have the bases for the eigenspaces as
$$
\begin{bmatrix}
1 &  1 \\
1 & -\frac{6}{4}
\end{bmatrix}
$$
Doing A on this matrix has the effect of multiplying any line along $\begin{bmatrix}1 \\ 1\end{bmatrix}$ by 6 and any line along $\begin{bmatrix}1 \\ -\frac{6}{4}\end{bmatrix}$ by -4.

![[Pasted image 20240224144145.png|300]]



## 4.1.26
Use the method of Example 4.5 to find all of the eigenvalues of the matrix $A$, where
$$
A = \begin{bmatrix*}[r] 1 & 2 \\ -2 & 3 \end{bmatrix*}.
$$
We can express the eigenvalues as solutions to the equation
$$
\begin{align}
A \vec{v} = \lambda \vec{v} \\
\implies(A-\lambda I)\vec{v} = 0 \\
\implies \det(A-\lambda I) = 0
\end{align}
$$
This gives us the following:
$$
\begin{align}
\det \left( \begin{bmatrix}
1-\lambda &  2 \\
-2  & 3-\lambda
\end{bmatrix} \right) = 0\\
(1-\lambda)(3-\lambda)+4=0 \\
7-4\lambda+\lambda^{2} =0 \\
\end{align}
$$
This has no real solutions, but there are complex ones. Using the quadratic equation,
$$
\begin{align}
\lambda= \frac{4\pm \sqrt{ 16-28 }}{2} \\
\lambda=2\pm \sqrt{3}i 
\end{align}
$$

We can now find our complex eigenvectors:
$$
\begin{align}
&\begin{bmatrix}
1-(2+\sqrt{ 3 }i) & 2  & | & 0\\
-2 & 3-(2+\sqrt{ 3 }i) & | & 0\\
\end{bmatrix} \\
&= \begin{bmatrix}
-1+\sqrt{ 3 }i & 2 \\
-2 & 1+\sqrt{ 3i }
\end{bmatrix} \\
&\xrightarrow {\stackrel{R_{1}\to  \frac{R_{2}}{2}}{R_{2}\to  \frac{R_{2}}{-2}} }\begin{bmatrix}
\frac{-1+\sqrt{ 3 }i}{2} & 1 \\
1 & \frac{1+\sqrt{ 3i }}{2}
\end{bmatrix}  \\
&\xrightarrow {R_{1}\leftrightarrow R_{2}}\begin{bmatrix}
1 & \frac{1+\sqrt{ 3 }i}{2} \\
\frac{-1+\sqrt{ 3 }i}{2} & 1 \\

\end{bmatrix}   \\
\end{align}
$$
$$
\begin{align}
&R_{2}\to  R_{2}-\frac{-1+3i}{2}R_{1}\\
&\begin{bmatrix}
1 & \frac{1+\sqrt{ 3 }i}{2} \\
0 & 1-\frac{-1+\sqrt{ 3 }i}{2}\frac{1+\sqrt{ 3 }i}{2} \\
\end{bmatrix}  \\
=&\begin{bmatrix}
1 & \frac{1+\sqrt{ 3 }i}{2} \\
0 & 1-\left( \frac{-1-3}{2} \right)  \\
\end{bmatrix}   \\
=&\begin{bmatrix}
1 & \frac{1+\sqrt{ 3 }i}{2} \\
0 & 3
\end{bmatrix} \\
&R_{2}\to  \frac{(1+\sqrt{ 3 }i)R_{2}}{3}-R_{1} \\
&\begin{bmatrix}
1 & \frac{1+\sqrt{ 3 }i}{2} \\
0 & 0
\end{bmatrix}
\end{align}
$$
This gives us the first eigenvector as 
$$
\begin{bmatrix}
1 \\ \frac{ -1- \sqrt{ 3 }i}{2}
\end{bmatrix}
$$
We can now find the other:

$$
\begin{align}
&\begin{bmatrix}
1-(2-\sqrt{ 3 }i) & 2  & | & 0\\
-2 & 3-(2-\sqrt{ 3 }i) & | & 0\\
\end{bmatrix} \\
=&\begin{bmatrix}
-1+\sqrt{ 3 }i & 2 & | & 0 \\
-2 & 1+\sqrt{ 3 }i & | & 0
\end{bmatrix} \\
&R_{1}\to  \frac{R_{1}}{2}, R_{2}\to  -\frac{R_{2}}{2 } \\
&\begin{bmatrix}
 \frac{-1 +\sqrt{ 3 }i}{2}   & 1 \\
1 & -\frac{1+\sqrt{ 3 }i}{2}
\end{bmatrix}    \\
\end{align}
$$
$$
\begin{align}
&R_{1}\leftrightarrow R_{2}\\
&\begin{bmatrix} 
1 & -\frac{1+\sqrt{ 3 }i}{2} \\
\frac{-1 +\sqrt{ 3 }i}{2}   & 1 \\
\end{bmatrix}  \\
&R_{2}\to  R_{2}-\frac{-1+\sqrt{ 3 }i}{2}R_{1} \\
&\begin{bmatrix} 
1 & -\frac{1+\sqrt{ 3 }i}{2} \\
0   & 1 - \left( \frac{-1 +\sqrt{ 3 }i}{2} \right)\left( -\frac{1+\sqrt{ 3 }i}{2} \right)  \\
\end{bmatrix} \\
 =&\begin{bmatrix} 
1 & -\frac{1+\sqrt{ 3 }i}{2} \\
0   & 1 + \frac{\left( -1 +\sqrt{ 3 }i\right)\left( 1+\sqrt{ 3 }i \right) }{2}  \\
\end{bmatrix}  \\
\end{align}
$$
$$
\begin{align}
&= \begin{bmatrix}
1 & -\frac{1+\sqrt{ 3 }i}{2} \\
0 & 1+\frac{\left( -1-3 \right)}{2} 
\end{bmatrix} \\
&= \begin{bmatrix}
1 & -\frac{1+\sqrt{ 3 }i}{2} \\
0 & -1 
\end{bmatrix} \\
R_{2}\to  -\frac{1+\sqrt{ 3 }i}{2}R_{2}+R_{1} \\
 &= \begin{bmatrix}
1 & -\frac{1+\sqrt{ 3 }i}{2} \\
0 & 0
\end{bmatrix} \\
\end{align}
$$
This gives us the last eigenvector as 
$$
\begin{bmatrix}
 1 \\ \frac{1+\sqrt{ 3 }i}{2}
\end{bmatrix}
$$
We now have both eigenvectors as 
$$
\boxed{
\begin{bmatrix}
1 \\ \frac{1+\sqrt{ 3 }i}{2}
\end{bmatrix}\text{ and }  \begin{bmatrix}
1 \\ -\frac{ 1+ \sqrt{ 3 }i}{2}
\end{bmatrix}
}
$$
Corresponding to the eigenvalues $\lambda=2 + \sqrt{3}i \text{ and } \lambda=2 -\sqrt{3}i$  respectively. 


## 4.1.28
Find all the eigenvalues of the matrix $A$ over the complex numbers $\mathbb{C}$, where
$$
A = \begin{bmatrix*}[r] 2 & -3 \\ 1 & 0 \end{bmatrix*} .
$$
Give bases for each of the corresponding eigenspaces.

We can express the eigenvalues as solutions to the equation
$$
\begin{align}
A \vec{v} = \lambda \vec{v} \\
\implies(A-\lambda I)\vec{v} = 0 \\
\implies \det(A-\lambda I) = 0
\end{align}
$$
This gives us the following:
$$
\begin{align}
\det \left( \begin{bmatrix}
2-\lambda & -3 \\
1 & -\lambda
\end{bmatrix} \right)=0\\
(2-\lambda)(-\lambda) +3 = 0\\
\lambda^{2}-2\lambda + 3= 0 \\
\end{align}
$$
The solutions to this are imaginary, expressed as:
$$
\begin{align}
\lambda=1\pm \sqrt{ 2 }i \\
\end{align}
$$

We can now calculate the eigenvectors that these represent with the augmented matrixes:
$$
\begin{bmatrix}
2-(1+\sqrt{ 2 }i) & -3  & | & 0\\
1 & -(1+\sqrt{ 2}i) & | & 0
\end{bmatrix}
$$
and 
$$
\begin{bmatrix}
2-(1-\sqrt{ 2 }i) & -3  & | & 0\\
1 & -(1-\sqrt{ 2}i) & | & 0
\end{bmatrix}
$$
We can now (finally) solve for the eigenvectors that form a basis for the new eigenspace. 

We can see that these correspond to the matrices
$$
\begin{align}
\begin{bmatrix}
1 & -(1-\sqrt{ 2 }i) \\
0 & 0
\end{bmatrix} \\
\text{ and }   \\
\begin{bmatrix}
1 & -(1+\sqrt{ 2 }i) \\
0 & 0
\end{bmatrix}
\end{align}
$$
as we can apply row operations that reduce a single row to zero by subtracting values specifically chosen to match the value in that column that we want to be zero. 

These matrixes correspond to the eigenvectors
$$
\begin{bmatrix}
1 \\ 1-\sqrt{ 2 }i
\end{bmatrix} \text{ and }   \begin{bmatrix}
1  \\
1+\sqrt{ 2 }i
\end{bmatrix}
$$



## 4.1.35

A) Show that the eigenvalues of the $2 \times 2$ matrix
$$
A = \begin{bmatrix*}[r] a & b \\ c & d \end{bmatrix*} 
$$

are the solutions to the quadratic equation $\lambda^2 - \text{tr}(A)\lambda + \text{det}(A) = 0$, where $\text{tr}(A)$ is the trace of $A$. (See page 162.)

by definition, $tr(A) = a+b$ and $\det(A) = ad-bc$.
We can show generally for any matrix that eigenvalues follow the following properties.
$$
\begin{align}
A\vec{v}=\lambda \vec{v}\\
(A-\lambda I)\vec{v}=0 \\
\det(A-\lambda I)=0 \\
\det \left( \begin{bmatrix}
a-\lambda & b \\
c  & d-\lambda
\end{bmatrix} \right) =0 \\
(a-\lambda)(d-\lambda)-(cb)=0 \\
ad-\lambda a - \lambda d + \lambda^{2}-bc = 0 \\
\lambda^{2}-(a+d)\lambda+ad-bc = 0
\end{align}
$$
we can now rewrite this as 
$$
\lambda^{2}-tr(A)+\det(A)=0
$$


B) Show that the eigenvalues of the matrix $A$ in part (a) are
$$
\lambda = \frac{1}{2}(a+d \pm \sqrt{(a-d)^2 + 4bc}). 
$$
We can show generally for any matrix that eigenvalues follow the following properties.

We found in A that $\lambda^{2}-(a+d)\lambda+ad-bc = 0$

We can see that this follows the general form of the quadratic formula. We can write this out it out as
$$
\lambda= \frac{-(-a-d)\pm \sqrt{ (-a-b)^{2}-4(ad-bc) }}{2}
$$

$$
\begin{align}
\lambda= \frac{(a+d)\pm \sqrt{ (a^{2}+d^{2}+2ad)-4(ad-bc) }}{2} \\
= \frac{(a+d)\pm \sqrt{ a^{2}+d^{2}-2ad-4bc) }}{2} \\
= \frac{(a+d)\pm \sqrt{ (a-d)^{2}-4bc) }}{2} \\
\end{align}
$$
This has proven the relation.


C) Show that the trace and determinant of the matrix  in part (a) are given by
$$
\text{tr}(A) = \lambda_1 + \lambda_2 \text{ \ \ and \ \ } \text{det}(A) = \lambda_1\lambda_2 
$$
where $\lambda_1$ and $\lambda_2$ are the eigenvalues of $A$.

We can show that $tr(A) =$ $a+d$.
we can write $\lambda_{1}+\lambda_{2}$ as
$$
\begin{align}
\frac{(a+d)+ \sqrt{ (a-d)^{2}-4bc) }}{2} + \frac{(a+d)- \sqrt{ (a-d)^{2}-4bc) }}{2} \\
= \frac{2(a+d)}{2} +\frac{\sqrt{ (a-d)^{2}-4bc) }}{2} - \frac{\sqrt{ (a-d)^{2}-4bc) }}{2} \\
= a+d = tr(A)
\end{align}
$$
we can show similarly

$$
\det(A) = ad-bc
$$
and
$$
\begin{align}
\lambda_{1}\lambda_{2} = \frac{(a+d)- \sqrt{ (a-d)^{2}-4bc) }}{2}\frac{(a+d)+ \sqrt{ (a-d)^{2}-4bc) }}{2} \\
= \frac{1}{4}\left( (a+d)^{2}-((a-d)^{2}-4bc) \right) \\
= \frac{1}{4}((a+d)^{2}-(a-d)^{2}+4bc)) \\
= \frac{1}{4} (a^{2}+d^{2}+2ad-(a^{2}+d^{2}-2ad)-4bc) \\
= \frac{1}{4} (a^{2}+d^{2}+2ad-a^{2}-d^{2}+2ad-4bc) \\
= \frac{1}{4}(2ad+2ad-4bc) \\
= ad-bc
\end{align}
$$
Thus we have proven that $\lambda_{1}\lambda_{2}=\det(A)$

## 4.1.36
Consider again the matrix $A$ in Exercise 4.1.35. Give conditions on $a, b, c, \text{and } d$ such that $A$ has
A) two distinct real eigenvalues, 
B) one real eigenvalue, and 
C) no real eigenvalues. 

For all the responses, take the quadratic formula as 
$$
\frac{-b_{q}\pm \sqrt{ b_{q}^{2}-4a_{q}c_{q} }}{2a_{q}}
$$
For any eigenvalue, $Det(A-\lambda I)=0$.
This simplifies to $(a-l)(d-l)-(bc)$. We can expand this to
$$
(ad-bc)-(a+d)\lambda+\lambda^{2}=0
$$
$Det(A)=(ad-bc)$
Let $\det(A)=c_{q}, -(a+d)=b_{q},1=a_{q}$

there are two distinct real eigenvalues if $b_{q}^{2}-4a_{q}c_{q}>0$.
This means that $(a+d)^{2}-4\det(A)>0$.

There is one distinct solution if $(a+d)^{2}-4\det(A)=0$.
And there are no real eigenvalues if $(a+d)^{2}-4\det(A)<0$.

## 4.1.38
Let $a$ and $b$ be real numbers. Find the eigenvalues and corresponding eigenspaces of
$$
A = \begin{bmatrix*}[r] a & b \\ -b & a \end{bmatrix*} 
$$
over the complex numbers.

We can write this as solutions to
$$
\begin{align}
A\vec{v}=\lambda \vec{v}\\
(A-\lambda I)\vec{v}=0 \\
\det(A-\lambda I)=0 \\
\det \left( \begin{bmatrix}
a-\lambda & b \\
-b  & a-\lambda
\end{bmatrix} \right) =0 \\
(a - \lambda)^{2}+b^{2}=0 \\
a^{2}-2a \lambda +\lambda^{2}+b^{2}=0  \\
\lambda^{2} +(-2a)\lambda+ (a^{2}+b^{2})=0\\

\lambda=  \frac{2a\pm\sqrt{ 4a^{2}-4(a^{2}+b^{2}) }}{2} \\
\text{let }\lambda_{1}=  \frac{2a+\sqrt{ 4a^{2}-4(a^{2}+b^{2}) }}{2} \\
\text{let }\lambda_{2}=  \frac{2a-\sqrt{ 4a^{2}-4(a^{2}+b^{2}) }}{2}
\end{align}
$$
we can find our eigenvectors with
$$
\begin{bmatrix}
a-\lambda & b & | & 0 \\
-b & a-\lambda & | & 0\\
\end{bmatrix}
$$
we can now reduce this with $R_{1}\to \frac{R_{1}}{b}$ and $R_{2}\to \frac{R_{2}}{-b}$
$$
\begin{bmatrix}
-\frac{\lambda-a}{b} & 1 & | & 0 \\
1 & \frac{\lambda-a}{b} & | & 0\\
\end{bmatrix}
$$
We can now reduce this with
$$
\begin{align}
R_{1}\to R_{1}-\frac{-\lambda-a}{b}R_{2}  \\
\begin{bmatrix}
0 & 1-\frac{(\lambda-a)(-\lambda-a)}{b} & | & 0 \\
1 & \frac{\lambda-a}{b} & | & 0\\
\end{bmatrix}
\end{align}
$$
let $k = 1-\frac{(\lambda-a)(-\lambda-a)}{b}$
this is
$$
\begin{bmatrix}
0 & k \\
1 & \frac{\lambda-a}{b}
\end{bmatrix}
$$
We can now do $R_{1}\to R_{1}-k\left( \frac{b}{\lambda-a} \right)R_{2}$
This yield the final matrix
$$
\begin{bmatrix}
0 & 0 \\
1 & \frac{\lambda-a}{b}
\end{bmatrix}
$$
we can write this for both lambdas found to get our final eigenvectors:
$$
\begin{bmatrix}
0 & 0 \\
1 & \frac{\lambda_{1}-a}{b}
\end{bmatrix}

\text{ and }  

\begin{bmatrix}
0 & 0 \\
1 & \frac{\lambda_{2}-a}{b}
\end{bmatrix}
$$


## 4.2.14
Compute the following determinant using cofactor expansion along any row or column that seems convenient:
$$
\begin{vmatrix*}[r]
2 &  0 & 3 & -1 \\
1 &  0 & 2 &  2 \\
0 & -1 & 1 &  4 \\
2 &  0 & 1 & -3
\end{vmatrix*}. 
$$

By the cofactor expansion, we can write this recursively as every element in column 2 times the determinant of the matrix generated by removing that elements row and column.

I choose column 2 for this cofactor expansion. This means the determinant can be expressed as 
$$
-0 \times  \det \begin{bmatrix}
1 & 2 & 2 \\
0 & 1 & 4 \\
2 & 1 & -3
\end{bmatrix} +
0 \det \begin{bmatrix}
2 & 3 & -1 \\
0 & 1 & 4 \\
2 & 1 & -3
\end{bmatrix} - (-1)\det \begin{bmatrix}
2 & 3 & -1 \\
1 & 2 & 2 \\
2 & 1 & -3
\end{bmatrix} + 0 \det \begin{bmatrix}
2 & 3 & -1 \\
1 & 2 & 2 \\
0 & 1 & 4
\end{bmatrix}
$$

$$
\begin{align}
= 1\det \begin{bmatrix}
2 & 3 & -1 \\
1 & 2 & 2 \\
2 & 1 & -3
\end{bmatrix} \\
= 1 (2(-6-2)-3(-3-4)-1(1-4)) \\
= 1(-16+21+3) \\
= 8
\end{align}
$$

## 4.2.42
Prove Theorem 4.3(f):
$\textit{Theorem 4.3(f):}$ Let $A = [a_{ij}]$ be a square matrix. If B is obtained by adding a multiple of one row (column) of $A$ to another row (column), then $\text{det} \, B = \text{det} \, A$. Note:  You may use parts (a)-(e) of Theorem 4.3 in your solution, but not any results that appear after Theorem 4.3 in the textbook. 

We can take the elementary matrix corresponding to this addition, called $E$. We express this as $EA=B$. If $\det(EA)=\det(A)$, then $\det(\mathbf{B})=\det A$.


$E$ is the elementary matrix corresponding to the ERO $C_{n}\to C_{n}+aC_{m}$ for any $n\text{ and } m$. 
in the $2\times 2$ case we can represent $E$ as 
$$
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}\xrightarrow {C_{2}\to  C_{2}+C_{1}}\begin{bmatrix}
1 & 1 \\ 0  & 1
\end{bmatrix}
$$

for both possible column addition EROs, we get 
![[Pasted image 20240227092747.png]]
depending on the columns being swapped. The determinant of this matrix is 1. In general, this matrix can be generated by taking the identity $I$ and performing a single addition of one row to another in $I$. For any addition ERO, there will always be a zero on one diagonal of any submatrix in $I$. In the identity, $ad=1$. Given that there will always be a zero in the diagonal, $bc=0$. Thus, $ad-bc$ for this submatrix will always be 1. Therefore, $\det(E)=1$.

because $B=EA$, $\det B=\det EA = \det(E)\det(A)=1 \det(A) = \det A$


## 4.2.54
Suppose $A$ and $B$ are $n \times n$ matrices. If $B$ is invertible, prove that $\text{det}(B^{-1}AB) = \text{det}(A)$.
we can use properties of the determinant to show that 
$\text{det}(B^{-1}AB) =\det(B^{-1})\det A)\det(B)$
By definition, $\det(B^{-1})=\frac{1}{\det(B)}$
so this expression simplifies to 
$$\begin{align}
\frac{1}{\det(B)}\det(B)\det(A) \\
= \det(A)
\end{align}
$$

## 4.2.56
A square matrix $A$ is called $\textbf{\textit{nilpotent}}$ if $A^m = O$ for some $m > 1$. Find all possible values of $\text{det}(A)$ if $A$ is nilpotent.

Note:  The word $\textit{nilpotent}$ comes from the Latin $\textit{nil}$, meaning "nothing," and $\textit{potere}$, meaning "to have power." A nilpotent matrix is thus one that becomes "nothing"---that is, the zero matrix---when raised to some power.


We can say that $\det(A^{m})=\det(A)^{m}$
$A^{m}= 0$ for some m, then
$\det(A)^{m}=0$
For any value $\det(A)<1$.
$$
\lim_{ m \to \infty } \det(A)^{m}=0
$$
This means that any matrix with determinant less than 1 can be nilpotent. 
(if we restrict m to not be infinity, then only matrices whose determinants are zero are nilpotent. This could still be any matrix that takes $\mathbb{R}^{n}$ to $\mathbb{R}^{n-k}\,\forall \, k \leq n \in \mathrm{Re}$).
