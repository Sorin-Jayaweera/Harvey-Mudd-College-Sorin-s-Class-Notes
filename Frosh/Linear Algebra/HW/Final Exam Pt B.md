![[Pasted image 20240427093747.png]]
I, Sorin Jayaweera, agree to the above digitally.

![[Pasted image 20240427094041.png]]
1)
We can find the effect of $D$ on the space $W$ by finding the effect on the basis vectors for $W$.  This output can be written in terms of the original basis in vector form as 

$$
\begin{align}
D(\sin(x))=\cos(x) \\
D(\begin{bmatrix}1\\0\end{bmatrix})=\begin{bmatrix}0\\1\end{bmatrix}
\end{align}
$$
Similarly, 
$$
\begin{align}
D(\cos(x))=-\sin(x) \\
D(\begin{bmatrix}
0\\1
\end{bmatrix}) = \begin{bmatrix}
-1 \\ 0
\end{bmatrix}
\end{align}
$$
We can see that the new representation of the space after transformation is 

$$
\begin{align}
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}\xrightarrow {becomes}   \begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix} \\
\text{ so, } \\
D_{\text{ as a matrix is }} \begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix}
\end{align}
$$

Because this output is linearly independent and has no null space, the transformation preserved all of $W$. $D$ is one to one and onto. The kernel being zero implies that this function is one to one.

2)
In part 1, I showed that the matrix representation of $D$ is
$$
\begin{align}
\begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix}
\end{align}
$$
By the fact that this has nonzero determinant $(\det=1)$, the fundamental theorem of invertible matrices shows that this matrix is invertible.

3)
First, writing $F(x)$ in terms of the basis as a vector,
$$
\begin{align}
3\sin x-5\cos x= \begin{bmatrix}
3\\-5
\end{bmatrix}
\end{align}
$$
Computing directly, $F'(x)=3\cos x+5\sin x$.
Using the matrix, we can write this as
$$
\begin{align}
\begin{bmatrix}
0  & -1 \\
1 & 0
\end{bmatrix}\begin{bmatrix}
3 \\ -5
\end{bmatrix} \\
= \begin{bmatrix}
(3*0)+(-5*-1)\\(3*1)+(-5*0)
\end{bmatrix} \\
= \begin{bmatrix}
5\\3
\end{bmatrix}
\end{align}
$$
Rewriting this as functions, this is $5 B_{1}+3B_{2}=5\sin x+3\cos x$
We can see that both methods of computation yielded the same result.






![[Pasted image 20240427094050.png]]
Suppose that $u+v=w$. Then it must hold true that
$$
\begin{align}
\left< u,w \right> = \left< u,u+v \right>
\end{align}
$$
By the properties of the inner product,:
$$
\begin{align}
\left< u,u+v \right>  & = \left< u,u \right> +\left< u ,v\right> \\
 & = \left| u \right| ^{2}+\left< u,v \right>  \\
 & =4-3 \\
 & =1  
\end{align}
$$
We can see that this agrees with the inner product $\left< u,w \right>=1$ 
The inner product being the same means that the relationship between $u$ and $w$ is the same geometrically. Because $u$ is the same between both $\left< u,u+v \right>\text{ and } \left< u,w \right>$, the only way for their relationship to be the same is if $w=v+u$. 
Therefore, by direct proof, $w=v+u$.


![[Pasted image 20240427094102.png]]
To make an orthogonal basis, I'll first choose arbitrarily the vector $x$. This is the first vector in the orthogonal basis.
To find $v_{2}$, this is
$$
\begin{align}
v_{2} & =b_{2}-\frac{\left< v_{1},b_{2} \right>}{\left< v_{1},v_{1} \right> }v \\
v_{2}  & = x  - \frac{\int_{0}^{1} (1)(x) \, dx }{\int_{0}^{1} (1)(1) \, dx }1 \\
 & =x- \frac{\frac{x^{2}}{2}\bigg|_{0}^{1}  }{x\bigg|_{0}^{1}  } \\
 & =x-\frac{\frac{1}{2}}{1} \\
v_{2} & =x-\frac{1}{2}
\end{align}
$$
To compute the third basis vector $v_{3}$, this is
$$
\begin{align}
v_{3} & =b_{3}- \frac{\left< v_{2},b_{3} \right> }{\left< v_{2},v_{2} \right> }v_{2} - \frac{\left< v_{1},b_{3} \right> }{\left< v_{1},v_{1} \right> }v_{1} \\
 & =x^{2}- \frac{\int_{0}^{1} \left( x-\frac{1}{2} \right)(x^{2}) \, dx }{\int_{0}^{1} \left( x-\frac{1}{2} \right)^{2} \, dx }\left( x-\frac{1}{2} \right) - \frac{\int_{0}^{1} (x^{2})(1) \, dx }{\int_{0}^{1} (1) \, dx }(1) \\
 & =x^{2}- \frac{\int_{0}^{1} x^{3}-\frac{1}{2} x^{2}\, dx }{\int_{0}^{1} x^{2}-x+\frac{1}{4} \, dx }\left( x-\frac{1}{2} \right) - \frac{\int_{0}^{1} x^{2} \, dx }{\int_{0}^{1} 1 \, dx } \\
 & =x^{2}-\frac{\frac{x^{4}}{4}-\frac{1}{6}x^{3}\bigg|_{0}^{1}  }{\frac{x^{3}}{3}-\frac{x^{2}}{2}+\frac{1}{4}x\bigg|_{0}^{1}  }\left( x-\frac{1}{2} \right)- \frac{\frac{x^{3}}{3}\bigg|_{0}^{1}  }{x\bigg|_{0}^{1}  } \\
 & =x^{2}- \frac{\frac{1}{4}-\frac{1}{6}}{\frac{1}{3}-\frac{1}{2}+\frac{1}{4}}\left( x-\frac{1}{2} \right) - \frac{\frac{1}{3}}{1} \\ 
 & =x^{2}- \frac{\frac{1}{12}}{\frac{1}{12}}\left( x-\frac{1}{2} \right)-\frac{1}{3} \\
 & =x^{2}-x+\frac{1}{2}-\frac{1}{3} \\
 v_{3} & =x^{2}-x+\frac{1}{6}
\end{align}
$$
This gives us the new orthogonal basis as
$$
\begin{align}  
\left\{ 1,x-\frac{1}{2},x^{2}-x+\frac{1}{6} \right\}
\end{align}
$$
We must now normalize the basis. 
$$
\begin{align}
\text{ using }\left| v \right| =\sqrt{ \left< v,v \right>  }
\end{align}
$$
$$
\begin{align}
\left| 1 \right| =\sqrt{ \int_{0}^{1} 1 \, dx  } \\
= \sqrt{ 1 } \\
=1
\end{align}
$$
 so $1$ is already normalized.
 $$
\begin{align}
\left| x-\frac{1}{2} \right| = \sqrt{ \left< \left( x-\frac{1}{2},x-\frac{1}{2} \right) \right>  } \\
= \sqrt{ \int_{0}^{1} \left( x-\frac{1}{2} \right)^{2} \, dx  } \\
= \sqrt{ \int_{0}^{1} x^{2}-x+\frac{1}{4} \, dx  } \\
= \sqrt{ \frac{1}{3}-\frac{1}{2}+\frac{1}{4} } \\
= \sqrt{ \frac{1}{12} }
\end{align}
$$
Thus, to normalize the second basis vector, this is
$$
\begin{align} \\
\frac{x-\frac{1}{2}}{\sqrt{ \frac{1}{12} }} \\
= \sqrt{ 12 }\left( x-\frac{1}{2} \right)
\end{align}
$$

Now for the third basis vector:
$$
\begin{align}
\left| x^{2} -x+\frac{1}{6}\right|  = \sqrt{ \left< x^{2} -x+\frac{1}{6},x^{2} -x+\frac{1}{6} \right>  } \\
\text{ (evaluating the inner product first) } \\
\left< x^{2} -x+\frac{1}{6},x^{2} -x+\frac{1}{6} \right>  = \int_{0}^{1} \left( x^{2} -x+\frac{1}{6} \right)^{2} \, dx  \\
= \int_{0}^{1}x^{4}-x^{3}+\frac{x^{2}}{6}-x^{3}+x^{2}-\frac{x}{6}+\frac{1}{6}x^{2}-\frac{x}{6}+\frac{1}{36} \, dx  \\
= \int_{0}^{1} x^{4}-2x^{3}+\frac{8}{6}x^{2} -\frac{1}{3}x+\frac{1}{36} \, dx  \\
= \frac{1}{4}-\frac{2}{4}+\frac{8}{18}-\frac{1}{6}+\frac{1}{36} \\
= -\frac{1}{4}+\frac{4}{9}-\frac{5}{36} \\
= -\frac{9}{36}+\frac{16}{36}-\frac{5}{36} \\
= \frac{2}{36} \\
= \frac{1}{18}
\end{align}
$$
Thus, the third vector for the orthonormal basis should be
$$
\begin{align} \\
18(x^{2} -x+\frac{1}{6})
\end{align}
$$
Thus, an orthogonal (but not normal basis) is
$$
\begin{align}
1,x^{2}+\frac{1}{2},x^{2}-x+\frac{1}{6}
\end{align}
$$
and if I did my math correctly, this gives us the entire orthogonal + normalized basis as
$$
\begin{align}
1,\sqrt{ 12 }x^{2}+\frac{\sqrt{ 12 }}{2}, 18x^{2}-18x+\frac{1}{6}
\end{align}
$$
(not sure if you wanted it, but just in case).