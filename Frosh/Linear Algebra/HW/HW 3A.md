,mn2.R.9
Find the point of intersection of the following lines, if it exists.
$$
\begin{bmatrix*} x \\ y \\ z \end{bmatrix*} = \begin{bmatrix*} 1 \\ 2 \\ 3 \end{bmatrix*} + s \begin{bmatrix*} 1 \\ -1 \\ 2 \end{bmatrix*} \text{ and } \begin{bmatrix*} x \\ y \\ z \end{bmatrix*} = \begin{bmatrix*} 5 \\ -2 \\ -4 \end{bmatrix*} + t \begin{bmatrix*} -1 \\ 1 \\ 1 \end{bmatrix*}
$$
For simplicity, lets translate this into a typical system of two equations.
we want to find the intersection of
x = 1 + s = 5-t
y = 2-s = -2+t
z = 3+2s = -4+t

We can rewrite these equations as
s+t=4
s+t=4
2s-t=-7
We can express these new rules in a matrix
$$
\begin{bmatrix}
1 & 1 & | & 4 \\
2 & -1 & | & -7\\
0 & 0 & | & 0\\
\end{bmatrix}
\xrightarrow {R_{2}\to R_{2}-2R_{1}}
\begin{bmatrix}
1 & 1 & | & 4 \\
0 & -3 & | & -15
\end{bmatrix}\xrightarrow {R_{2}\to \frac{R_{2}}{1}}
$$
$$
\begin{bmatrix}
1 & 1 & | & 4 \\
0 & 1 & | & 5
\end{bmatrix} \xrightarrow {R_{1}\to R_{1}-R_{2}}
\begin{bmatrix}
1 & 0 & | & -1 \\
0 & 1 & | & 5
\end{bmatrix}
$$
This gives us S = -1 and T = 5
Thus, the lines intersect at 

$$
\boxed{
\begin{align}

x = 0\\
y = 3\\
z = 1\\

\end{align}
}
$$

 2.3.13
 Describe the span of the vectors $\begin{bmatrix*}[r] 2 \\ -4 \end{bmatrix*}, \begin{bmatrix*}[r] -1 \\ 2 \end{bmatrix*}$ (a) geometrically and (b) algebraically.
a)  Geometrically, we have two vectors where one is a multiple of the other. That means that these two vectors lie on the same line, and can only define points on that line.

 b) we can find the span of the two vectors by representing them as a matrix:
 $$
\begin{bmatrix}
2 & -1 \\
-4 & 2
\end{bmatrix}
$$
If we do the simple ERO,
$R_{2}\to R_{2}+2R_{1}$
$$
\begin{bmatrix}
2 & -1 \\
0 & 0
\end{bmatrix}
$$
We see that we end with a row of all zeros. This is in echelon form. We know that we have 1 leading variable, so the maximum span of this matrix is $\boxed{\mathbb{R}^{1}}$. This is a linearly dependent set, as $\vec{v}_{2} = -\frac{1}{2}\vec{v}_{1}$. 


 2.3.22
 Determine if the set of vectors $\begin{bmatrix*}[r] 2 \\ -1 \\ 3 \end{bmatrix*}, \begin{bmatrix*}[r] -1 \\ 2 \\ 3 \end{bmatrix*}$ is linearly independent.
We can write these two vectors in a matrix and manipulate them:
$$
\begin{bmatrix}
2 & -1 \\
-1 & 2 \\
3 & 3
\end{bmatrix}
\xrightarrow {\begin{align}
R_{3}\to R_{3}+3R_{2} \\
R_{1}\to R_{1}+2R_{2}
\end{align}}
\begin{bmatrix}
0&3 \\
-1&2 \\
0&9
\end{bmatrix} \xrightarrow {R_{2}\to -R_{2}}\begin{bmatrix}
0&3 \\
1&-2 \\
0&9
\end{bmatrix} \xrightarrow {R_{2}\leftrightarrow R_{1}}\begin{bmatrix}
1&-2 \\ 
0&3 \\
0&9
\end{bmatrix} 
$$
$R_{3}\to R_{3}-3R_{2}$
$$
\begin{bmatrix}
1 & -2 \\
0 & 3 \\
0 & 0
\end{bmatrix} \xrightarrow {R_{2}\to \frac{1}{3}R_{2}}\begin{bmatrix}
1 & -2 \\
0 & 1 \\
0 & 0
\end{bmatrix}\xrightarrow {R_{1}\to R_{1}+2R_{2}}
\begin{bmatrix}
1 & 0 \\
0 & 1 \\
0 & 0
\end{bmatrix}
$$
We can see that there are two leading variables, and one empty row. This means that the span of the set of vectors is $\boxed{\mathbb{R}^{2}}$. This makes sense, as with only two vectors we can only define a plane at maximum. The vectors are thus independent.



2.3.26
Determine if the set of vectors $\begin{bmatrix*}[r] -2 \\ 3 \\ 7 \end{bmatrix*}, \begin{bmatrix*}[r] 4 \\-1 \\ 5 \end{bmatrix*}, \begin{bmatrix*}[r] 3 \\ 1 \\ 3 \end{bmatrix*}, \begin{bmatrix*}[r] 5 \\ 0 \\ 2 \end{bmatrix*}$ is linearly independent.

Geometrically, the set is required to be linearly dependent. The Vectors are all in $\mathbb{R}^{3}$, but there are 4 vectors. If any set of three were linearly independent, the fourth must be defined by the remaining three, meaning that it is a dependent. To prove this, 
We can represent the vectors in a matrix
$$
\begin{bmatrix}
-2 & 4 & 3 & 5 \\
3 & -1 & 1 & 0 \\
7 & 5 & 3 & 2
\end{bmatrix}
\xrightarrow {R_{1}\to R_{1}+R_{2}}
\begin{bmatrix}
1 & 3 & 4 & 5 \\
3 & -1 & 1 & 0 \\
7 & 5 & 3 & 2
\end{bmatrix} 
\xrightarrow {\begin{align}
R_{2}\to R_{2}-3R_{1} \\
R_{3}\to R_{3}-7R_{1}
\end{align}}
\begin{bmatrix}
1 & 3 & 4 & 5 \\
0 & -10 & -11 & -15 \\
0 & -16 & -25 & -33
\end{bmatrix} 
$$

$$
\xrightarrow {R_{3}\to R_{3}-R_{2}-2R_{1}}
\begin{bmatrix}
1 & 3 & 4 & 5 \\
0 & -10 & -11 & -15 \\
0 & 0 & -24 & -38
\end{bmatrix} 
\xrightarrow {R_{2}\to R_{2}+3R_{1}}
\begin{bmatrix}
1 & 3 & 4 & 5 \\
0 & 1 & 1 & 5 \\
0 & 0 & -24 & -38
\end{bmatrix}
$$
$$
\xrightarrow {R_{1}-3R_{2}}
\begin{bmatrix}
1 & 0 & 1 & -10 \\
0 & 1 & 1 & 5 \\
0 & 0 & -24 & -38
\end{bmatrix}
\xrightarrow {R_{3}\to R_{3}+2R_{1}}
\begin{bmatrix}
1 & 0 & 1 & -10 \\
0 & 1 & 1 & 5 \\
0 & 0 & -22 & -18
\end{bmatrix}
\xrightarrow {R_{3}\to \frac{R_{3}}{2}}
\begin{bmatrix}
1 & 0 & 1 & -10 \\
0 & 1 & 1 & 5 \\
0 & 0 & -11 & -9
\end{bmatrix}
\xrightarrow {R_{3}\to R_{3}+12R_{2}}
$$
$$
\xrightarrow {R_{3}\to R_{3}+12R_{2}}
\begin{bmatrix}
1 & 0 & 1 & -10 \\
0 & 1 & 1 & 5 \\
0 & 0 & 1 & 51
\end{bmatrix}
\xrightarrow {\begin{align}
R_{2}\to R_{2}-R_{3} \\
R_{1}\to R_{1}-R_{3}
\end{align}}
\begin{bmatrix}
1 & 0 & 0 & -61 \\
0 & 1 & 0 & -46 \\
0 & 0 & 1 & 51
\end{bmatrix}
$$
We can see that we have the first three vectors defining $\mathbb{R}^{3}$, while having a free variable in the last vector. This means that the set of 4 vectors, each in $\mathbb{R}^{3}$ is linearly dependent.


3.1.8
Compute $BB^T$ where

$$
B = \begin{bmatrix*}[r]
	4 & -2 & 1 \\
	0 & 2 & 3
\end{bmatrix*}. 

$$
We can express $B^T$ as 
$$
\begin{bmatrix}
4 & 0 \\
-2  & 2\\
1 & 3\\
\end{bmatrix}
$$
Thus, $BB^T$ is
$$
\begin{bmatrix*}[r]
	4 & -2 & 1 \\
	0 & 2 & 3
\end{bmatrix*}

\begin{bmatrix}
4 & 0 \\
-2  & 2\\
1 & 3\\
\end{bmatrix}
$$

We can rewrite this as


$$
\begin{bmatrix}
(4,-2,1)\cdot({4},-2,1) & (4,-2,1)\cdot(0,2,3) \\
(0,2,3)\cdot(4,-2,1) & (0,2,3)\cdot(0,2,3)
\end{bmatrix}
$$
$$
\boxed{BB^{T}
= \begin{bmatrix}
22 & -1 \\
-1 & 13
\end{bmatrix}
}
$$


3.1.18
 Let $A = \begin{bmatrix*}[r] 2 & 1 \\ 6 & 3 \end{bmatrix*}$.
Find $2 \times 2$ matrices $B$ and $C$ such that $AB = AC$ but $B \neq C$.
let $B = \begin{bmatrix}a_{1}&b_{1}\\c_{1}&d_{1}\end{bmatrix}$ and $C=\begin{bmatrix}a_{2}&b_{2}\\c_{2}&d_{2}\end{bmatrix}$

We can express this equality as 
$$
\begin{bmatrix*}[r] 2 & 1 \\ 6 & 3 \end{bmatrix*}\begin{bmatrix}a_{1}&b_{1}\\c_{1}&d_{1}\end{bmatrix} = \begin{bmatrix*}[r] 2 & 1 \\ 6 & 3 \end{bmatrix*}\begin{bmatrix}a_{2}&b_{2}\\c_{2}&d_{2}\end{bmatrix}
$$
Expanding this,
$$
\begin{bmatrix}
2a_{1}+c_{1} & 2b_{1}+d_{1} \\
6a_{1}+3c_{3} & 6b_{1}+3d_{1}
\end{bmatrix} = \begin{bmatrix}
2a_{2}+c_{2} & 2b_{2}+d_{2} \\
6a_{2}+3c_{2} & 6b_{2}+3d_{2}
\end{bmatrix}
$$
this gives us 4 equations
$$
\begin{align}
2a_{1}+c_{1}=2a_{2}+c_{2} \\
2b_{1}+d_{1}=2b_{2}+d_{2} \\
6a_{1}+3c_{1}=6a_{2}+3c_{2} \\
6b_{1}+3d_{1}=6b_{2}+3d_{2}
\end{align}
$$



I continued from this point on later, but something wasn't working properly with my matrix generating function. If you can find the mistake, I would be deeply grateful. 

we can now pick any arbitrary $a_{1},b_{1},c_{1},d_{1}$ and express these equations as two matrixes
let $a_{1}=1,b_{1}=1,c_{1}=2,d_{1}=2$, so matrix B is $\begin{bmatrix}1&1\\2&2\end{bmatrix}$ and AB is $\begin{bmatrix}4&4\\12&12\end{bmatrix}$
We can now use our equations:
$$
\begin{align}
4=2a_{2}+c_{2} \\
4=2b_{2}+d_{2} \\
2a_{2}+c_{2}=2b_{2}+d_{2}
\end{align}
$$
If we pick an arbitrary $a_{2}\text{ and } b_{2}\text{ and } c_{2}$, $a_{2}=2,c_{2}=0,b_{2}=2,d_{2}=0$
This simplifies to

So the new matrix 
$$
C = 
\begin{bmatrix}
2 & 2  \\
0 & 0
\end{bmatrix}
$$
We can check this with
Thus, the two matrixes B and C that work
$$
B=\begin{bmatrix}
1 & 2 \\
2 & 2
\end{bmatrix}
\, 
C=\begin{bmatrix}
2  & 2 \\
0  & 0
\end{bmatrix}
$$

This is the point that I had continued onto, using $a_{1}=1,b_{1}=2,c_{1}=3,d_{1}=4$,so matrix B is $\begin{bmatrix}1 & 2 \\3 & 4\end{bmatrix}$ and AB is $\begin{bmatrix}5&8\\15&24\end{bmatrix}$
With the new restrictions, we can find matrix C
$$
\begin{bmatrix}
2 & 0 & 1 & 0 & | & 5 \\
0 & 2 & 0 & 1 & | & 8 \\
6 & 0 & 3 & 0 & | & 15 \\
0 & 6 & 0 & 3 & | & 24
\end{bmatrix}
$$
This matrix contains redundant information, as $R_{1}=\frac{R_{3}}{3}\text{ and } R_{2}=\frac{R_{4}}{3}$ , so we can simplify what we have to work with and solve this through EROs.
$$\begin{bmatrix}
2 & 0 & 1 & 0 & | & 5 \\
0 & 2 & 0 & 1 & | & 8 \\
\end{bmatrix}
$$
We can parameterize $c_{2}\text{ as }S_{1}\text{ and } d_{2}\text{ as }S_{2}$
We have the newly compacted equations $2a_{2}+c_{2}=5,\,\,2b_{2}+d_{2}=8 \implies$
$$
\begin{align}
a_{2}=\frac{\left( -S_{1}+5 \right)}{2}  \\
b_{2}=\frac{\left( -S_{2}+8 \right)}{2} \\
c_{2}=S_{1} \\
d_{2}=S_{2} 
\end{align}
$$
This gives us the solution
$$
\boxed{
\begin{bmatrix}
a_{2} \\
b_{2} \\
c_{2} \\
d_{2}
\end{bmatrix} = S_{1}\begin{bmatrix}
\frac{-1}{2}\\0 \\1\\0
\end{bmatrix}+S_{2}\begin{bmatrix}
0\\\frac{-1}{2}\\0\\1
\end{bmatrix} + \begin{bmatrix}
\frac{5}{2}\\4\\0\\0
\end{bmatrix}
\forall (S_{1},S_{2}) \in \mathrm{Re}}
$$

We can pick new arbitrary $c_{2},d_{2}$ as long as $c_{2}\neq 3,d_{2}\neq 4$ as that would give us matrix D.

3.1.26
 Use the matrix-column representation of the product to write each column of $BA$ as a linear combination of the columns of $B$, where
  $$ A = \begin{bmatrix*}[r]
  1 & 0 & -2 \\
  -3 & 1 & 1 \\
  2 & 0 & -1
  \end{bmatrix*}
  \text{ \ and \ }
  B = \begin{bmatrix*}[r]
  2 & 3 & 0 \\
  1 & -1 & 1 \\
  -1 & 6 & 4
\end{bmatrix*}.
$$

We can express this with the outer product of
$$
      \begin{bmatrix*}[r]
            2 & 3 & 0 \\
            1 & -1 & 1 \\
            -1 & 6 & 4
\end{bmatrix*}
\begin{bmatrix*}[r]
            1 & 0 & -2 \\
            -3 & 1 & 1 \\
            2 & 0 & -1
        \end{bmatrix*}
        
$$
This is the grossly long matrix where each column is the sum of the multiples of each row in A times the vector in B to form AB as a linear combination of vectors from B. I'm not sure if this is valid notation.

$$
\boxed{
\begin{bmatrix}
1  \begin{pmatrix}
   2\\1\\-1
   \end{pmatrix}

-3 \begin{pmatrix}
     3\\-1\\6
    \end{pmatrix}
+2 \begin{pmatrix}
     0\\1\\4
     \end{pmatrix}
,& 0 \begin{pmatrix}
2\\1\\-1
\end{pmatrix}
+1\begin{pmatrix}
3\\-1\\6
\end{pmatrix}
+0\begin{pmatrix}
0\\1\\4
\end{pmatrix},& -2\begin{pmatrix}
2\\1\\-1
\end{pmatrix}+1\begin{pmatrix}
3\\-1\\6
\end{pmatrix}-1\begin{pmatrix}
0\\1\\4
\end{pmatrix}
\end{bmatrix}
}
$$

 Writing this similarly but in a different fashion, 
 
$$
\boxed{
\begin{bmatrix}
2 \\
1 \\
-1
\end{bmatrix}\begin{bmatrix}
1 & 0 & -2\\
-3 & 1 & 1 \\
2 & 0 & -1 \\
\end{bmatrix} + \begin{bmatrix}
3 \\
-1 \\
6
\end{bmatrix}\begin{bmatrix}
1 & 0 & -2\\
-3 & 1 & 1 \\
2 & 0 & -1 \\
\end{bmatrix} +\begin{bmatrix}
0 \\
1 \\
4
\end{bmatrix}\begin{bmatrix}
1 & 0 & -2\\
-3 & 1 & 1 \\
2 & 0 & -1 \\
\end{bmatrix}

}
$$
 $$
= \begin{bmatrix}
-7 & 3 & -1 \\
6 & -1 & -4 \\
-11 & 6 & 4
\end{bmatrix}
$$



3.2.12
  Find the general form of $\text{span}(A_1, A_2, A_3, A_4)$, where
$$
  
A_1 = \begin{bmatrix*}[r]
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix*}, \ \
A_2 = \begin{bmatrix*}[r]
0 & 1 & 1 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{bmatrix*}, \ \
A_3 = \begin{bmatrix*}[r]
-1 & 0 & -1 \\
0 & 1 & 0 \\
0 & 0 & -1
\end{bmatrix*}, \ \
\text{ \ and \ }
A_4 = \begin{bmatrix*}[r]
1 & -1 & 1 \\
0 & -1 & -1 \\
0 & 0 & 1
\end{bmatrix*}.      
$$
Each matrix is a 3 by three, so we could rewrite the span of all 4 of these together as 
$Span(A_{1_{1}},A_{1_{2},A_{1_{3},}A_{2_{1}}\dots A_{3_{3}}})$
Where $A_{1_{1}}$ denotes the vector in column 1 from A1, and so on.
Because these are three by three matrixes, the maximum span they can contain is $\mathbb{R}^{3}$. We see that $A_{1}$ is the typical definition of the span $\mathbb{R}^{3}$. We can see that every other matrix's vectors lie in the span of $A_{1}$, so all vectors beyond those contained in $A_{1}$ are linearly dependent on the vectors that are in $A_{1}$. Thus, the general form of the span of all 4 $3\times 3$ matrixes is 
$$
\boxed{
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
 0& 0&1  
\end{bmatrix}
}
$$
If i misinterpreted this question and it wants us to find the span of each matrix,
We can se $A_{2}$ has span $\mathbb{R}^{2}$ as $R_{1}\to R_{1}-R_{2}$ yields the matrix $\begin{bmatrix}0 & 1 & 0 \\0 & 0 & 1 \\0 & 0 & 0\end{bmatrix}$
We can see that $A_{3}$ has span $\mathbb{R}^{3}$ as $R_{1}\to-R_{1},R_{1}\to R_{1}+R_{3},R_{3}\to-R_{3}$ yields the matrix $\begin{bmatrix}1&0&0\\0&1&0\\0&0&1\end{bmatrix}$

and $A_{4}$ has span $R_{3}$ as $R_{2}\to -R_{2},R_{1}\to R_{1}+R_{2},R_{1}\to R_{1}-2R_{3},R_{2}\to R_{2}-R_{3}$ yields the matrix
$\begin{bmatrix}1 & 0 &0\\0 & 1 & 0 \\0 & 0 & 1\end{bmatrix}$


3.2.14
Determine whether the given matrices are linearly independent:
$$

\begin{bmatrix*}[r] 1 & 2 \\ 4 & 3 \end{bmatrix*},
\begin{bmatrix*}[r] 2 & 1 \\ -1 & 0 \end{bmatrix*},
\begin{bmatrix*}[r] 1 & 1 \\ 1 & 1 \end{bmatrix*}. 

$$
We can simplify all and then write them in a larger matrix to find their dependency.
$$
\begin{bmatrix}
1 & 2 \\
4 & 2
\end{bmatrix} \xrightarrow {R_{2}-4R_{1}}\begin{bmatrix}
1 & 2 \\
0 & -6
\end{bmatrix} \xrightarrow {R_{2}\to \frac{R_{2}}{-6}}\begin{bmatrix}
1 & 2 \\
0 & 1
\end{bmatrix}\xrightarrow {R_{1}\to R_{1}-R_{2}}
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$
We can see that this matrix is independent and defines the entire span $\mathbb{R}^{2}$, so any other $2\times 2$ vector lies in it's span. If we had all three in a large set of vectors, that set would be linearly dependent. 
Now onto the next matrix:
$$
\begin{bmatrix}
2 & 1 \\
-1 & 0
\end{bmatrix}\xrightarrow {R_{2}\to -R_{2}}
\begin{bmatrix}
2 & 1 \\
1 & 0
\end{bmatrix} \xrightarrow {R_{1}\to R_{1}-2R_{2}}
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
\xrightarrow {R_{2}\leftrightarrow R_{1}}
\begin{bmatrix}
1&0 \\
0&1
\end{bmatrix}
$$
So the second matrix is also linearly independent by the same logic

$$
\begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}\xrightarrow {R_{2}\to R_{2}-R_{1}}
\begin{bmatrix}
1 & 1 \\
0 & 0
\end{bmatrix}
$$
We can see that this is only able to define a line, as $R_{2}$ is a multiple of $R_{1}$. Thus, the third matrix is linearly dependent.


3.2.24
If $B = \begin{bmatrix*}[r] a & b \\ c & d \end{bmatrix*}$ and $A = \begin{bmatrix*}[r]1 & -1 \\ -1 & 1 \end{bmatrix*}$,
find conditions on $a, b, c,$ and $d$ such that $AB = BA$. 

$$
\begin{bmatrix*}[r]1 & -1 \\ -1 & 1 \end{bmatrix*}
\begin{bmatrix*}[r] a & b \\ c & d \end{bmatrix*}$$

then $AB=BA$
We can also express the result of AB and BA as two matrixes
$$ AB= 
\begin{bmatrix}
a-c &b-d \\
c-a & d-b 
\end{bmatrix}
=BA =
\begin{bmatrix}
a-b & -a+b \\
c-d & -c+d
\end{bmatrix} \\
$$
This gives us the rules
$$
\begin{align}
a-c=a-b \\
b-d=b-a \\
c-a=c-d \\
d-b=d-c
\end{align}
$$
We can rewrite these as a  matrix after simplifying
$$
\begin{align}
b-c=0 \\
a-d=0 \\
d-a=0 \\
c-b=0
\end{align}
$$
We can write this as the following matrix and then solve. However, there is a much easier way: 

$$
\begin{bmatrix}
0 & 1 & -1 & 0 & | & 0 \\
1 & 0 &  0 & -1 &| & 0 \\
-1 & 0 & 0 & 1 & | & 0 \\
0 & -1 & 1 & 0 & | & 0 
\end{bmatrix}
$$
instead we can write 
$$
\begin{align}
b-c=c-b\\
a-d=d-a
\end{align}
$$
and get 
$$
\begin{align}
2c=2b\implies c=b\\
2a=2d \implies a=d \\
\end{align}
$$

Thus, for AB to equal BA, $c=b\text{ and } a=d$.
