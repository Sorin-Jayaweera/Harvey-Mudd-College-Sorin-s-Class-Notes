Names:  Sorin Jayaweera, Cam Warmerdam, Sam Wheeler

collaborators: Elliot Bobrow/Alexa Rosenberg

# Exercise 3.1.38
Let $$
A = \begin{bmatrix*}[r]
        \text{cos}\;\theta & -\text{sin}\;\theta \\
        \text{sin}\;\theta & \text{cos}\;\theta
    \end{bmatrix*}.
$$
1) Show that  $$
A^2 = \begin{bmatrix*}[r]
                \text{cos}\;2\theta & -\text{sin}\;2\theta \\
                \text{sin}\;2\theta & \text{cos}\;2\theta
            \end{bmatrix*}$$     
We can write out $AA$ as 
$$
\begin{bmatrix*}[r]
        \text{cos}\;\theta & -\text{sin}\;\theta \\
        \text{sin}\;\theta & \text{cos}\;\theta
\end{bmatrix*}\begin{bmatrix*}[r]
        \text{cos}\;\theta & -\text{sin}\;\theta \\
        \text{sin}\;\theta & \text{cos}\;\theta
    \end{bmatrix*}
$$
We can now do the matrix multiplication and get
$$
\begin{bmatrix}
\cos^2\theta-\sin^2\theta & -2\sin\theta \cos\theta \\
2\cos \theta \sin\theta & -\sin^2\theta+\cos^2\theta
\end{bmatrix}
$$
We an now use following known trig identities to simplify:
$$
\begin{align}
\cos {2\theta}=\cos^2\theta-\sin^2\theta \\
\sin 2\theta = 2\sin\theta \cos\theta \\
\end{align}
$$
using this to simplify each entry, this makes the matrix
$$
\boxed{
\begin{bmatrix}
\cos 2\theta & -\sin 2\theta \\
\sin 2\theta &  \cos 2\theta
\end{bmatrix}
}
$$

1) Prove, by mathematical induction, that
$$
A^n = \begin{bmatrix*}[r]
\text{cos}\;n\theta & -\text{sin}\;n\theta \\
\text{sin}\;n\theta & \text{cos}\;n\theta
\end{bmatrix*}
$$for $n \geq 1$.

We have proven this for the case $n=1$ in part 1. Assume the statement is true for some number N. We can show that $A^{n+1} = \begin{bmatrix}\cos((n+1)\theta)&-\sin((n+1)\theta)\\sin((n+1)\theta)&\cos((n+1)\theta)\end{bmatrix}$ 
$A^{n+1}=AA^{n} =$
$$
\begin{bmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{bmatrix}\begin{bmatrix}
\cos n\theta & -\sin n\theta \\
\sin n\theta & \cos n\theta
\end{bmatrix}
$$
$$
= \begin{bmatrix}
\cos\theta \cos n\theta  -\sin\theta \sin n\theta &-\cos\theta \sin n\theta-\sin\theta \cos n\theta \\
\sin\theta \cos n\theta +\cos\theta \sin n\theta &-\sin\theta \sin n\theta+\cos\theta \cos n\theta  
\end{bmatrix}
$$


The trig identities from before generalize to
$$
\begin{align}
\cos ({(n+1)\theta})=\cos\theta \cos n\theta  -\sin\theta \sin n\theta \\
\sin ((n+1)\theta) = \sin\theta \cos n\theta +\cos\theta \sin n\theta 
\end{align}
$$
## this is a large step to assume trig generalizes to this, have to prove it. 



# 3.2.18

Prove Theorem 3.2.(e)-(h):

Theorem 3.2:} Let $A$, $B$, and $C$ be matrices of the same size and let $c$ and $d$ be scalars. Prove the following facts: 

For all following statements, let $A=\begin{bmatrix}a_{1}&a_{2}\\a_{3}&a_{4}\end{bmatrix}$ , and let B follow the same construction.
e) $c(A + B) = cA + cB$
We can write this as
$$
c \left( \begin{bmatrix}
a_{1} & a_{2} \\
a_{3} & a_{4}
\end{bmatrix}+
\begin{bmatrix}
b_{1} & b_{2} \\
b_{3} & b_{4}
\end{bmatrix} \right) = 
c \left( \begin{bmatrix}
a_{1}+b_{1} & a_{2}+b_{2}\\a_{3}+b_{3} & a+b_{4} 
\end{bmatrix} \right) $$
$$
=\begin{bmatrix}
c(a_{1}+b_{1}) & c(a_{2}+b_{2})\\c(a_{3}+b_{3}) & c(a+b_{4} )
\end{bmatrix}
$$
Which by the distributive property of regular numbers $=$ 
$$
\begin{bmatrix}
ca_{1}+cb_{1} & ca_{2}+cb_{2} \\
ca_{3}+c b_{3} & ca_{4}+c b_{4}
\end{bmatrix}
$$
we can now separate this into two matrixes
$$
\begin{bmatrix}
ca_{1} & ca_{2} \\
ca_{3} & ca_{4}
\end{bmatrix}+
\begin{bmatrix}
cb_{1} & cb_{2} \\
cb_{3} & c b_{4}
\end{bmatrix}
$$
We can now multiply by $\frac{c}{c}$ and get
$$
c \begin{bmatrix}
a_{1} & a_{2} \\
a_{3} & a_{4}
\end{bmatrix}
+
c\begin{bmatrix}
b_{1} & b_{2} \\
b_{3} & b_{4}
\end{bmatrix} = cA+cB
$$
Thus we have proven E.

f) $(c + d)A = cA + dA$
we can write this as
$$
\begin{bmatrix}
(c+d)a_{1} & (c+d)a_{2} \\
(c+d)a_{3} & (c+d)a_{4}
\end{bmatrix}
$$
By the distributive property of numbers
$$
=\begin{bmatrix}
ca_{1}+da_{1} & ca_{2}+da_{2} \\
ca_{3}+da_{3} & ca_{4}+da_{4}
\end{bmatrix} = \begin{bmatrix}
ca_{1} & ca_{2} \\
ca_{3} & ca_{4}
\end{bmatrix}+\begin{bmatrix}
da_{2} & da_{2} \\
da_{3} & da_{4}
\end{bmatrix}
$$
which we can see as
$$
c \begin{bmatrix}
a_{1} & a_{2} \\
a_{3} & a_{4}
\end{bmatrix} + d\begin{bmatrix}
a_{1} & a_{2} \\
a_{3} & a_{4}
\end{bmatrix} = cA+dA
$$
so $(c+d)=cA+dA$. This has proven f.

g) $c(dA) = (cd)A$
we can write this as
$$
c \begin{bmatrix}
da_{1} & da_{2} \\
da_{3} & da_{4}
\end{bmatrix} = 
\begin{bmatrix}
cda_{1} & cda_{2} \\
cda_{3} & cda_{4}\
\end{bmatrix}=

c d \begin{bmatrix}
a_{1}&a_{2}\\a_{3}&a_{4}
\end{bmatrix}
$$
so we have proven g to be true.

h) $1A = A$
we can write this as
$$
1 \begin{bmatrix}
a_{1} & a_{2} \\
a_{3} & a_{4}
\end{bmatrix} =  \begin{bmatrix}
1a_{1} & 1a_{2} \\
1a_{3} & 1a_{4}
\end{bmatrix}
$$
by the identity property of regular numbers 
$$
=  \begin{bmatrix}
a_{1} & a_{2} \\
a_{3} & a_{4}
\end{bmatrix} = A
$$
so we have proven h to be true


# 3.2.28
Prove that if $AB$ and $BA$ are both defined, then $AB$ and $BA$ are both square matrices.

Theorem 1) We can see generally that a matrix $C = AB$ has the property that $C \text{ is an } m\times n \text{ matrix if A is an } m\times k_{1} \text{ matrix and B is a } k_{2}\times n \text{ matrix }$ if and only if $k_{1}=k_{2}$ 
This follows from the fact that matrixes are expressed as every combination of dot products along rows and columns. let $r_{1} \text{ and } r_{2}$ be rows of length n and $c_{1} \text{ and }  c_{2}$ be columns vectors of dimension n. By the definition of matrix multiplication,
$$
\begin{bmatrix}
r_{1} \\
r_{2} \\
\dots \\
r_{n}
\end{bmatrix} \begin{bmatrix}
c_{1} & c_{2} & \dots & c_{n}
\end{bmatrix} = \begin{bmatrix}
r_{1}\cdot c_{1} & r_{1}\cdot c_{2}  & \dots & r_{1}\cdot c_{n}\\
r_{2}\cdot c_{1} & r_{2}\cdot c_{2} & \dots & r_{2}\cdot c_{n} \\
\vdots &\vdots & \vdots & \vdots \\
r_{n}\cdot c_{1} & r_{n}\cdot c_{2} & \dots & r_{n}\cdot c_{n}
\end{bmatrix}
$$
Dot products by definition are only valid if $r_{n} \text{ and }  c_{n}$ have the same length when written out as row vectors, as this $r\cdot c = r_{1}c_{1}+r_{2}c_{2}+\dots r_{l}c_{l}$. This proves Theorem 1.
Using theorem 1, we can say that $AB$ will yield a $m\times n$ matrix and $BA$ will yield a $k_{1}\times k_{2}$ matrix. We are told that both must exist, so they must fulfil the requirement $k_{1}=k_{2}$ and $m=n$. This means $AB$ is $M\times M$, and $BA$ is $k_{1}\times k_{1}$. Therefore, AB and BA are both square matrixes.

# 3.2.34:
Prove that for any matrix $A$, $AA^T$ and $A^TA$ are symmetric matrices.

# 3.2.45
Prove that if $A$ and $B$ are $n \times n$ matrices, then $\text{tr}(AB) = \text{tr}(BA)$.

If $A\text{ and } B$ are square matrixes, then AB and BA are square matrixes, see Theorem 1 in the solution to 3.2.28. let A be constructed $$\begin{bmatrix}
a_{1,1}  & \dots  & a_{n,1} \\
\vdots  & \ddots & \vdots   \\
a_{1,n} & \dots & a_{n,n}
\end{bmatrix}
$$ and let B be constructed in the same way, $$
\begin{bmatrix}
b_{1,1}  & \dots  & b_{n,1} \\
\vdots  & \ddots & \vdots   \\
b_{1,n} & \dots & b_{n,n}
\end{bmatrix}
$$We can write the AB as 
$$

$$