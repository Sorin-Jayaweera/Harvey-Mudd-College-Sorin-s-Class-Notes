






During this exam, you may use your notes, your past homework, your textbook, and the notes that the Math 73 instructors have been posting on our course Sakai site. You should not use any other sources (e.g., another textbook or a math website) to help you craft your solutions. All calculations should be done by hand; you should not use any computational tools for calculation (e.g., WolframAlpha). You should neither receive nor give any assistance, and you should not discuss any aspect of this exam with anyone other than the Math 73 instructors until one week after the due date. Keep in mind that this exam should be used as a vehicle to demonstrate your understanding of the material in this course. You should therefore justify all claims and examples and strive for clarity, cohesiveness, and transparency in your solutions. We expect your solutions to be both neat and well-written. Partial credit is available for every problem on the exam, so it is in your best interest to attempt each problem! It is better to submit an incomplete solution than no solution at all, in which case you could explain, for example, what you were trying to do and why you think your solution is incomplete. Just try your best! You have 2 hours to complete this exam. You do not have to complete the exam in one sitting: you can break these two hours up into increments in a way that best suits your needs. A PDF copy of your completed exam is due via Gradescope by noon Pacific Time on Sunday, February 18. Your exam submission may be handwritten or typed. In either case, make sure that your work is legible and that any pictures or scans are in focus.

I verify that I have read all the instructions above, and will abide by the HMC Honor Code. I did not spend more than two hours (or my adjusted accommodations time) on this exam. 

Your Signature: Sorin Jayaweera

![[Pasted image 20240216125311.png]]
To begin, I'll reduce this matrix to a nicer form using EROs.

$$
\begin{bmatrix}
1 & 1 & -1 & -1 \\
1 & -1 & 1 & 1  \\
-1 & 1 & 1 & -1
\end{bmatrix}\xrightarrow {\stackrel{R_{2}\to  R_{2}-R_{1}}{R_{3}\to  R_{3}+R_{1}} }
\begin{bmatrix}
1 & 1 & -1 & -1 \\
0 & -2 & 2 & 2 \\
0 & 2 & 0 & -2
\end{bmatrix}
\xrightarrow {R_{3}\to  \frac{R_{3}}{2}}
\begin{bmatrix}
1 & 1 & -1 & -1 \\
0 & -2 & 2 & 2 \\
0 & 1 & 0 & -1
\end{bmatrix}
$$
$$
\xrightarrow {\stackrel{R_{1}\to  R_{1}-R_{3}}{R_{2}\to  R_{2}+2R_{3}} }\begin{bmatrix}
1 & 0 & -1 & 0 \\
0 & 0 & 2 & 0 \\
0 & 1 & 0 & -1
\end{bmatrix}
\xrightarrow {R_{2}\to  \frac{R_{2}}{2}}
\begin{bmatrix}
1 & 0 & -1 & 0 \\
0 & 0 & 1 & 0 \\
0 & 1 & 0 & -1
\end{bmatrix}
$$
$$
R_{3}\leftrightarrow R_{2}
\begin{bmatrix}
1 & 0 & -1 & 0 \\
0 & 1 & 0 & -1\\
0 & 0 & 1 & 0 \\
\end{bmatrix} \xrightarrow {R_{1}\to  R_{1}+R_{3}}
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & -1\\
0 & 0 & 1 & 0 \\
\end{bmatrix}
$$
This matrix is now in reduced row echelon form. 

The column space is given by the columns associated with the leading terms in  
$$
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & -1\\
0 & 0 & 1 & 0 \\
\end{bmatrix}
$$
This means that the basis for the column space is
$$
\boxed{\left\{ \begin{bmatrix}
1 & 1  & -1\\
1 & -1  & 1\\
-1 & 1  & 1\\
\end{bmatrix} \right\} }
$$
 We can see that
  $$
\boxed{\text{ the dimension of Col(A) = 3 }
}
$$
Now I want to find the basis for the Null space. To do this, I write out the augmented matrix:
$$
\begin{bmatrix}
1 & 0 & 0 & 0  & | & 0\\
0 & 1 & 0 & -1 & | & 0\\
0 & 0 & 1 & 0  & |  & 0 \\
\end{bmatrix} 
$$
In equation form is thus:
$$
x_{2}=x_{4}
$$
We can parameterize this now.
$$
\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}\\x_{4}
\end{bmatrix}=x_{4}\begin{bmatrix}
0\\1\\0\\1
\end{bmatrix}
$$
 This gives the null space as
  $$
\begin{bmatrix}
0\\1\\0\\1
\end{bmatrix}
$$
We can see that $\boxed{dim(n u l l) = 1}$.


![[Pasted image 20240216125320.png]]

By definition, $proj_{u}(w)=\frac{W\cdot U}{U\cdot U}\vec{U}$ 
We can write $W\cdot U=(w_{1},w_{2})\cdot(1,1)=w_{1}+w_{2}$
We can write $U\cdot U=(1,1)\cdot(1,1)=2$
This we simplify the expression to $\boxed{\left( \frac{w_{1}+w_{2}}{2} \right) \vec{u}}$
this equals $\begin{bmatrix}\left( \frac{w_{1}+w_{2}}{2} \right)\\ \left( \frac{w_{1}+w_{2}}{2} \right)\end{bmatrix}$. Let this be denoted as R.
We can now write $proj_{v}(proj_{u}(w))$ as
$$proj_{v}(\begin{bmatrix}\left( \frac{w_{1}+w_{2}}{2} \right)\\ \left( \frac{w_{1}+w_{2}}{2} \right)\end{bmatrix})$$
By definition, this is 
$$
\frac{R\cdot V}{V\cdot V}\vec{V}
$$
$R\cdot V=\begin{bmatrix}\left( \frac{w_{1}+w_{2}}{2} \right)\\ \left( \frac{w_{1}+w_{2}}{2} \right)\end{bmatrix}\cdot \begin{bmatrix}-1\\1\end{bmatrix}$
$R\cdot V=-\left( \frac{w_{1}+w_{2}}{2} \right)+\left( \frac{w_{1}+w_{2}}{2} \right)=0$
This tells us that R and V are perpendicular to each other for all choices of $w_{1}\text{ and } w_{2}$.From this, we can infer that U and V are perpendicular to each other. The projection of any nonzero vector that isn't on the line defined by V will fall onto the line defined by U, so if that new vector is perpendicular to V then U is perpendicular to V. 


(This is explained briefly instead of using a full mathematical proof, as that is what the prompt asks).
![[Pasted image 20240216125329.png]]

We can write out  vectors in the null space  of A as $N_{n}$, and every vector in the row space of A as $A^{T}y$. 
We can write with the hint that $N_{n}\cdot\vec{v} = N^{T}\vec{v}$
We can rewrite $\vec{v}$ as $A^{T}y$. 
This makes the previous statement
$$\begin{align}

N_{n}\vec{v} &= N_{n}\cdot A^{T}y \\
&= N^{T}A^{T}y \\
&= (AN)^{T}Y
\end{align}
$$
By the definition of the nullspace, $AN = 0$, so $N_{n}\cdot \vec{v} = 0$. 
By the property of dot products, this means every vector in the nullspace is orthogonal to every vector in Row(A).




$$

$$



Previous proof:
We can represent that $A\vec{X}=0$ for every vector in $A$. Denoting each row in A as $R$ and column as $C$, using the inner product representation of matrix multiplication this becomes $C_{1}\vec{X}+C_{2}\vec{X}+\dots C_{n}\vec{X}=0$. We can express this as 
$$\begin{align}
0&=R_{1}^{T}\vec{X}+R_{1}^{T}\vec{X}+\dots+R_{n}^{T}\vec{X}  \\
&= R_{1}\cdot \vec{X}+R_{2}\cdot \vec{X}+\dots+R_{n}\cdot\vec{X}
\end{align}$$
By properties of the dot product,
$= \vec{X}\cdot(R_{1}+R_{2}+\dots+R_{n})$
Because Row(A) is a linearly independent set, there do not exist any constants that could make the term $R_{1}+R_{2}+\dots+R_{n}=0$. Thus, 
we can break up the previous expression into:
$$
\begin{align}
0 = R_{1}\cdot \vec{X} \\
0 = R_{2}\cdot \vec{X} \\
0 = R_{k}\cdot \vec{X} \\
\end{align}
$$
By definition, vectors in the Null(A) satisfy the equation $A\vec{X}=0$. Also, every vector in Row(A) is linearly independent, meaning that there do not exist constants $c_{1}\dots c_{k}$ such that $0=c_{1}R_{1}+\dots c_{k}R_{k}$.. 

Recall that $a\cdot b = \left| A \right|\left| B \right|\cos\theta$ where $\theta$ is the angle between the two vectors.
This implies that every vector in $Row(A)$ is orthogonal to every vector in the null space.