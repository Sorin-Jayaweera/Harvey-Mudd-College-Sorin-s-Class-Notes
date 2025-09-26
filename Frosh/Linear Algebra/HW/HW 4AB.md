## Exercise 3.3.40
Find a sequence of elementary matrices $E_1, E_2, \dots, E_k$ such that $E_k \cdots E_2E_1A = I$, where
$$ 
A = \begin{bmatrix*}[r] 2 & 4 \\ 1 & 1 \end{bmatrix*}. 
$$     
Use this sequence to write both $A$ and $A^{-1}$ as products of elementary matrices.

Using the property that $A^{-1}A=I$, $E_{k}\dots E_{2}E_{1}=A^{-1}$
**We want to find the EROs that go from the identity matrix to** $A^{-1}$. 

We can represent this as
$(A|I)\to (I|A^{-1})$
$$
\begin{align}
\begin{bmatrix}
2 & 4  & | & 1 & 0\\
1 & 1 & | & 0 & 1
\end{bmatrix}\xrightarrow {R_{1}\to  R_{1}-2R_{2}}\begin{bmatrix}
0 & 2  & | & 1 & -2\\
1 & 1 & | & 0 & 1
\end{bmatrix}\xrightarrow {R_{1}\to \frac{R_{1}}{2} }\begin{bmatrix}
0 & 1  & | & \frac{1}{2} & -1\\
1 & 1 & | & 0 & 1
\end{bmatrix} \\
\xrightarrow {R_{2}\to  R_{2}-R_{1}}\begin{bmatrix}
0 & 1  & | & \frac{1}{2} & -1\\
1 & 0 & | & -\frac{1}{2} & 2
\end{bmatrix} 
\end{align}
$$
This gives us the matrix $$A^{-1}=\begin{bmatrix} \frac{1}{2} & -1 \\
-\frac{1}{2} & 2
\end{bmatrix}$$
To do these steps, we applied the EROs $$
\begin{align}
E_{1}&=R_{1}\to  R_{1}-2R_{2} \\
E_{2}&=R_{1}\to  \frac{R_{1}}{2} \\
E_{3}&=R_{2}\to  R_{2}-R_{1}
\end{align}
$$


# TODO
## Exercise 3.3.41

Prove Theorem 3.13 for the case of $AB = I$.
Theorem 3.13:} Let $A$ be a square matrix. If $B$ is a square matrix such that either $AB = I$ or $BA = I$, then $A$ is invertible and $B = A^{-1}$.

Note that this means that an equivalent definition of the matrix inverse is: an \textbf{inverse} of an $n\times n$ matrix $A$ is an $n\times n$ matrix $A'$ with the property that $$AA' = I \textit{ or } A'A = I.$$
B

## Exercise 3.5.10
Suppose $S$ consists of all points in $\mathbb{R}^2$ that are on the $x$-axis or the $y$-axis (or both).
($S$ is called the $\textit{union}$ of the two axes.)
Is $S$ a subspace of $\mathbb{R}^2$? Why or why not?

## Exercise 3.5.20
 Give bases for $\text{row}(A)$, $\text{col}(A)$, and $\text{null}(A)$, where

$$ A = \begin{bmatrix*}[r]
2 & -4 & 0 & 2 & 1 \\
-1 & 2 & 1 & 2 & 3 \\
1 & -2 & 1 & 4 & 4
\end{bmatrix*} 
$$
## Exercise 3.5.38
Give the rank and nullity of the following matrix from Exercise 20:
$$
A = \begin{bmatrix*}[r]
        2 & -4 & 0 & 2 & 1 \\
        -1 & 2 & 1 & 2 & 3 \\
        1 & -2 & 1 & 4 & 4
\end{bmatrix*} $$

## Exercise 3.5.46
Answer the following question by considering the matrix with the given vectors as its  columns:
Do $\begin{bmatrix*}[r] 1 \\ -1 \\ 3\end{bmatrix*}, \begin{bmatrix*}[r] -1 \\ 5 \\ 1 \end{bmatrix*}, \begin{bmatrix*}[r]1 \\ -3 \\ 1 \end{bmatrix*}$ form a basis for $\mathbb{R}^3$?

We can simplify this using ERO's (I'm using the simplified representation instead of matrix multiplication for each step, as they lead to the same result).
$$
\begin{align}
\begin{bmatrix}
1 & 0 & 1 \\
-1 & 5 & -3 \\
3 & 1 &  1\\
\end{bmatrix}\xrightarrow {R_{1}\to R_{1}+R_{2}} \begin{bmatrix}
0 & 5 & -2 \\
-1 & 5 & -3 \\
3 & 1 & 1
\end{bmatrix}\xrightarrow {R_{3}\to R_{3}+3R_{2}}
\begin{bmatrix}
0 & 5 & -2 \\
-1 & 5 & -3 \\
0 & 16 & -8
\end{bmatrix}\xrightarrow {R_{2}\to R_{2}-R_{1}}
 \\
\begin{bmatrix}
0 & 5 & -2 \\
-1 & 0 & -1 \\
0 & 16 & -8
\end{bmatrix}\xrightarrow {R_{3}\to \frac{R_{3}}{8}} \begin{bmatrix}
0 & 5 & -2 \\
-1 & 0 & -1 \\
0 & 2 & -1
\end{bmatrix}\xrightarrow {R_{1}\to R_{1}-2R_{3}}\begin{bmatrix}
0 & 1 & 0 \\
-1 & 0 & -1 \\
0 & 2 & -1
\end{bmatrix}\xrightarrow {R_{3}\to R_{3}-2R_{1}} \\
\begin{bmatrix}
0 & 1 & 0 \\
-1 & 0 & -1 \\
0 & 0 & -1
\end{bmatrix}\xrightarrow {R_{2}\to R_{2}-R_{3}}\begin{bmatrix}
0 & 1 & 0 \\
-1 & 0 & 0 \\
0 & 0 & -1
\end{bmatrix}\xrightarrow {\stackrel{R_{2}\to -R_{2}}{R_{3}\to -R_{3}} }\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}\xrightarrow {R_{1}\leftrightarrow R_{2}} \\
= \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$
This gives us three basis vectors $\hat{x}\,\hat{y}\,\hat{z}$ that are linearly independent, and can therefore be scaled independently to define all of $\mathbb{R}^{3}$ 

## Exercise 3.5.62
 Prove that an $m \times n$ matrix $A$ has rank 1 if and only if $A$ can be written as the outer product $\mathbf{u} \mathbf{v}^T$ of a vector $\mathbf{u}$ in $\mathbb{R}^m$ and $\mathbf{v}$ in $\mathbb{R}^n$.

## Exercise 3.5.63
 If an $m \times n$ matrix $A$ has rank $r$, prove that $A$ can be written as the sum of $r$ matrices, each of which has rank 1.
$\textit{Hint:}$ Find a way to use Exercise 3.5.62.
