### 1
Show that $U = e^{A}$ is unitary if and only if $A$ is anti-Hermitian, $A^{\dagger} = -A$.

If $U$ is unitary, then we see that
$$
\begin{align}
e^{A^{\dagger}}e^{A}=\hat{\mathbb{I}} \\

\end{align}
$$
We have the property of powers where this becomes
$$
\begin{align}
e^{A^{\dagger}+A}=I \\
\end{align}
$$
This is only true if $A^{\dagger}+A=0\implies A^{\dagger}=-A$
All solutions for $A^{\dagger}=-A$ are anti Hermitian, so this is an if and only if statement.
## 2

For which values of $\alpha$ are the following matrices invertible? Find the inverses whenever possible. (You may do this analytically or by using code, or both!)


$$
\begin{equation*}

    A = \begin{pmatrix}

      1 & \alpha & 0 \\

      \alpha & 1 & \alpha \\

      0 & \alpha & 1

    \end{pmatrix}

    \qquad\qquad

    B = \begin{pmatrix}

      0 & 1 & \alpha \\

      1 & \alpha & 0 \\

      \alpha & 0 & 1

    \end{pmatrix}

\end{equation*}$$
For $A$ to be invertible, each of its vectors must be linearly independent. By the Spectral Theorem, this is equivalent to the determinant of $A$ being non zero.
We must therefore satisfy
$$
\begin{align}
0=\det{(A)} \\ \\
\text{ which we can calculate } \\
=1 (1-\alpha^{2}) - \alpha (\alpha-0) + 0  \\
= 1-2\alpha^{2} \\
\implies 2\alpha^{2}=1, \alpha=\pm\sqrt{ \frac{1}{2} }
\end{align}
$$
We can not have $a=\pm\sqrt{ \frac{1}{2} }$, but any other value is invertible.

We can do the same for $B$
$$
\begin{align}
0 = \det{(B)} \\
= 0 + 1 + \alpha(-\alpha^{2}) \\
1= \alpha^{3} \\
\alpha= 1 
\end{align}
$$


Thus, we can have any value $a\neq 1$

We can now go about finding the inverses
$$
\begin{align}
A = \begin{pmatrix}
1 & \alpha & 0 & | & 1 & 0 & 0 \\
\alpha & 1 & \alpha  & | & 0 & 1 & 0\\
0 & \alpha & 1 & | & 0 & 0 & 1
\end{pmatrix}
\end{align}
$$

$$
\begin{align}
A = \begin{pmatrix}
1 & \alpha & 0 & | & 1 & 0 & 0 \\
0 & 1-\alpha^{2} & \alpha  & | & -\alpha & 1 & 0\\
0 & \alpha & 1 & | & 0 & 0 & 1
\end{pmatrix}\to   \\
\begin{pmatrix}
1 & \alpha & 0 & | & 1 & 0 & 0 \\
0 & 1 & \frac{\alpha}{1-\alpha^{2}}  & | & -\frac{\alpha}{1-\alpha^{2}} & \frac{1}{1-\alpha^{2}} & 0\\
0 & \alpha & 1 & | & 0 & 0 & 1
\end{pmatrix}\to  \\
\end{align}
$$

$$
\begin{align}
\begin{pmatrix}
1 & 0 & -\frac{\alpha^{2}}{1-\alpha^{2}} & | & 1+\frac{\alpha^{2}}{1-\alpha^{2}} &-\frac{\alpha^{2}}{1-\alpha^{2}} & 0 \\
0 & 1 & \frac{\alpha}{1-\alpha^{2}}  & | & -\frac{\alpha}{1-\alpha^{2}} & \frac{1}{1-\alpha^{2}} & 0\\
0 & 0 & 1-\frac{\alpha^{2}}{1-\alpha^{2}} & | & -\frac{\alpha}{1-\alpha^{2}} & -\frac{\alpha}{1-\alpha^{2}} & \frac{1-\alpha^{2}}{1-2\alpha^{2}}
\end{pmatrix}\to   \\\text{ simplifying }\\
\begin{pmatrix}
1 & 0 & -\frac{\alpha^{2}}{1-\alpha^{2}} & | & \frac{1}{1-\alpha^{2}}& -\frac{\alpha^{2}}{1-\alpha^{2}} & 0 \\
0 & 1 & \frac{\alpha}{1-\alpha^{2}}  & | & -\frac{\alpha}{1-\alpha^{2}} & \frac{1}{1-\alpha^{2}} & 0\\
0 & 0 & \frac{1-2\alpha^{2}}{1-\alpha^{2}} & | & -\frac{\alpha}{1-\alpha^{2}} & -\frac{\alpha}{1-\alpha^{2}} & \frac{1-\alpha^{2}}{1-2\alpha^{2}}
\end{pmatrix}\to   \\
\end{align}
$$


$$
\begin{align}
\begin{pmatrix}
1 & 0 & -\frac{\alpha^{2}}{1-\alpha^{2}} & | & \frac{1}{1-\alpha^{2}}& -\frac{\alpha^{2}}{1-\alpha^{2}} & 0 \\
0 & 1 & \frac{\alpha}{1-\alpha^{2}}  & | & -\frac{\alpha}{1-\alpha^{2}} & \frac{1}{1-\alpha^{2}} & 0\\
0 & 0 & 1 & | & -\frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} & -\frac{\alpha-\alpha^{3}}{1-2\alpha^{2}+\alpha^{4}} & \frac{(1-\alpha^{2})^{2}}{(1-2\alpha^{2})^{2}}
\end{pmatrix}\to  
\end{align}
$$


$$
\begin{align}
\begin{pmatrix}
 1 & 0 & 0 & | & \frac{1}{1-\alpha^{2}}- \frac{\alpha^{2}}{1-\alpha^{2}}\left( \frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} \right)& -\frac{\alpha^{2}}{1-\alpha^{2}}-\frac{\alpha^{2}}{1-\alpha^{2}}\left( \frac{\alpha-\alpha^{3}}{1-2\alpha^{2}+\alpha^{4}} \right) & -\frac{\alpha^{2}}{1-\alpha^{2}}\frac{(1-\alpha^{2})^{2}}{(1-2\alpha^{2})^{2}} \\1 & 0 & 0 & | & 
 -\frac{\alpha}{1-\alpha^{2}}+\frac{\alpha}{1-\alpha^{2}}\left( \frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} \right) & \frac{1}{1-\alpha^{2}}-\frac{\alpha}{1-\alpha^{2}}\left( \frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} \right) & -\frac{\alpha}{1-\alpha^{2}}\frac{(1-\alpha^{2})^{2}}{(1-2\alpha^{2})^{2}}\\1 & 0 & 0 & | & 
 -\frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} & -\frac{\alpha-\alpha^{3}}{1-2\alpha^{2}+\alpha^{4}} & \frac{(1-\alpha^{2})^{2}}{(1-2\alpha^{2})^{2}}
\end{pmatrix}  
\end{align}
$$

We can simplify this inverse matrix:
$$
\begin{align}
\begin{pmatrix}
 \frac{1}{1-\alpha^{2}}- \frac{\alpha^{2}}{1-\alpha^{2}}\left( \frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} \right)& -\frac{\alpha^{2}}{1-\alpha^{2}}-\frac{\alpha^{2}}{1-\alpha^{2}}\left( \frac{\alpha-\alpha^{3}}{1-2\alpha^{2}+\alpha^{4}} \right) & -\frac{\alpha^{2}}{1-\alpha^{2}}\frac{(1-\alpha^{2})^{2}}{(1-2\alpha^{2})^{2}} \\
 -\frac{\alpha}{1-\alpha^{2}}+\frac{\alpha}{1-\alpha^{2}}\left( \frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} \right) & \frac{1}{1-\alpha^{2}}-\frac{\alpha}{1-\alpha^{2}}\left( \frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} \right) & -\frac{\alpha}{1-\alpha^{2}}\frac{(1-\alpha^{2})^{2}}{(1-2\alpha^{2})^{2}}\\
 -\frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} & -\frac{\alpha-\alpha^{3}}{1-2\alpha^{2}+\alpha^{4}} & \frac{(1-\alpha^{2})^{2}}{(1-2\alpha^{2})^{2}}
\end{pmatrix}  
\end{align}
$$

Which becomes
$$
\begin{align}
\begin{pmatrix}
\frac{1}{1-\alpha^{2}}\left( 1- \frac{\alpha^{3}-\alpha^{4}}{1+2\alpha^{2}+\alpha^{4}} \right) & -\frac{\alpha^{2}}{1-\alpha^{2}} \left( 1+ \frac{\alpha-\alpha^{3}}{1-2\alpha^{2}+\alpha^{4}} \right) & \frac{-\alpha^{2}-\alpha^{4}}{1-4\alpha^{2}+4\alpha^{4}} \\
\frac{\alpha}{1-\alpha^{2}}\left( 1+ \frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} \right) & \frac{1}{1-\alpha^{2}}\left( 1-\frac{a^{2}-a^{4}}{1+2\alpha^{2}+\alpha^{4}} \right)  & 
-\frac{\alpha-\alpha^{3}}{1-4\alpha^{2}+4\alpha^{4}} \\
-\frac{\alpha-\alpha^{3}}{1+2\alpha^{2}+\alpha^{4}} & - \frac{\alpha-\alpha^{3}}{1-2\alpha^{2}+\alpha^{4}} & \frac{1-2\alpha^{2}+\alpha^{4}}{1-4\alpha^{2}+4\alpha^{4}}
\end{pmatrix}
\end{align}
$$







We can do the for the matrix B:

$$
\begin{align}
B= \begin{pmatrix}
0 & 1 & \alpha \\
1  & \alpha & 0 \\
\alpha & 0 & 1
\end{pmatrix}
\end{align}
$$
We can row reduce
$$
\begin{align}
\begin{pmatrix}
0 & 1 & \alpha & |  & 1 & 0 & 0 \\
1 & \alpha & 0 & | & 0 & 1 & 0 \\
\alpha & 0 & 1 & | & 0 & 0 & 1
\end{pmatrix} \\
\to   \\
\begin{pmatrix}
0 & 1 & \alpha & | & 1 & 0 & 0 \\
1 & \alpha & 0 & | & 0 & 1 & 0 \\
0 & -\alpha^{2} & 1 & | & 0 & -\alpha & 1
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
\begin{pmatrix}
0 & 1 & \alpha & | & 1 & 0 & 0 \\
1 & 0 & -\alpha^{2} & | & 0 & 1 & 0 \\
0 & 0 & \alpha^{3} & | & 0 & -\alpha & 1
\end{pmatrix} \\
\begin{pmatrix}
0 & 1 & \alpha & | & 1 & 0 & 0 \\
1 & 0 & -\alpha^{2} & | & 0 & 1 & 0 \\
0 & 0 & 1 & | & 0 & -\frac{1}{\alpha^{2}} & \frac{1}{\alpha^{3}}
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
\begin{pmatrix}
0 & 1 & 0 & | & 1 & -\frac{1}{\alpha} & -\frac{1}{\alpha^{2}} \\
1 & 0 & 0 & | & 0 & 0 & \frac{1}{a} \\
0 & 0 & 1 & | & 0 & -\frac{1}{\alpha^{2}} & \frac{1}{\alpha^{3}}
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
\begin{pmatrix} 
1 & 0 & 0 & | & 0 & 0 & \frac{1}{a} \\
0 & 1 & 0 & | & 1 & -\frac{1}{\alpha} & -\frac{1}{\alpha^{2}} \\
0 & 0 & 1 & | & 0 & -\frac{1}{\alpha^{2}} & \frac{1}{\alpha^{3}}\\
\end{pmatrix}
\end{align}
$$



## 3

Consider the infinite series $\displaystyle S = \sum_{n=1}^\infty \frac{1}{n(n+1)}$.

(a) Without explicitly summing the series, use an integral test to determine whether it converges.

We can model this with an integral that is always above the value of the sum. If this integral converges, then the sum converges. 

We can rewrite this with a continuous function that is always above as
$$
\begin{align}
\int_{1}^{\infty} \frac{1}{x(x+1)}dx \\
\end{align}
$$
We can use partial fractions to decompose this:
$$
\begin{align}
\int_{1}^{\infty} \frac{1}{x}-\frac{1}{x+1}dx
\end{align}
$$
This evaluates to
$$
\begin{align}
\lim_{ n \to \infty } ln(x)- ln(x+1)\bigg|_{1}^{n} \\
= \lim_{ n \to \infty } ln(n)-ln(n+1) - 0 + ln(2)  \\
\text{ we can note that } \\
\lim_{ n \to \infty } ln\left( \frac{n}{n+1}\right)\to  0 \\
\text{ so the integral converges to }\\
ln(2)
\end{align}
$$




Because the integral of the continuous function that is always above the values of the series converges to a value, to series must converge.
  
(b) Sum the series.

We can break this sum by partial fractions to be
$$
\begin{align}
\sum_{x=1}^{\infty} \frac{1}{x} - \frac{1}{x+1}
\end{align}
$$
We can break this into two sums:
$$
\begin{align}
\sum_{x=1}^{\infty} \frac{1}{x} - \sum_{x=1}^{\infty} \frac{1}{x+1}
\end{align}
$$
We see that the first sum is the harmonic series that doesn't converge. However, the second term might change this - it also doesn't converge, but combined they will limit each other.

We can write out the sums as
$$
\begin{align}
1  & + \frac{1}{2} + \frac{1}{3 }\dots \\
 & -\frac{1}{2} - \frac{1}{3 }- \dots \\
 & = 1
\end{align}
$$
The sum thus converges down to 1.


## 4
  

Use series expansion where appropriate to evaluate the following limits:

(a) $\displaystyle \lim_{x \to 0} \left( \frac{1}{\sin^2 x} - \frac{1}{x^2} \right)$
We can expand out the series for $\sin ^{2}(x)$ to get
$$
\begin{align}
\left( x-\frac{x^{3}}{6}+\frac{x^{5}}{120} \right) \left( x-\frac{x^{3}}{6}+\frac{x^{5}}{120} \right) \\
\text{ we can keep terms up to } x^6 \\
x^{2}-\frac{1}{3}x^{4} +\frac{x^{6}}{120}
\end{align}
$$


We can therefore write out for only the first two terms as
$$
\begin{align}
\lim_{ x \to 0 } \frac{1}{x^{2}-\frac{1}{3}x^{4}}-\frac{1}{x^{2}} \\
= \lim_{ x \to 0 } \frac{x^{2}-x^{2}+\frac{1}{3}x^{4}}{x^{4}-\frac{1}{3}x^{6}} \\
= \lim_{ x \to 0 } \frac{1}{3}x^{4} \left( \frac{1}{x^{4}-\frac{2}{3}x^{6}} \right) \\
=\lim_{ x \to 0 } \frac{1}{3} \left( \frac{1}{1-\frac{2x^{2}}{3}} \right) \\
=\frac{1}{3-2x^{2}} \\
\implies \frac{1}{3}
\end{align}
$$


Any successive terms containing $x$ would go to zero, so even if we included more terms from the Taylor series in the numerator, they would not contribute to the result.
  

(b) $\displaystyle \lim_{x \to 0} \left( \frac{2}{x} + \frac{1}{1 - \sqrt{1 + x}} \right)$


We can build the Taylor series for the second term in the expression:
$$
\begin{align}
f(x) = \frac{2}{x}+\frac{1}{1-\sqrt{ 1+x }} \\
t(f(x)) = f(x) + \frac{f'(x)}{1}x + \frac{f''(x)}{2}x^{2}+\dots \\
\end{align}
$$

To not have to do horrible arithmetic, we can consolidate the function and make this simpler.
$$
\begin{align}
\frac{2-2\sqrt{ 1+x }+x}{x(1-\sqrt{ 1+x })}
\end{align}
$$
We can find the Taylor expansion for this much nicer object. Let $G(x)=\sqrt{ 1+x }$

We can use the nice property:
![[Pasted image 20250207184627.png]]
Where $n=\frac{1}{2}$. This yields
$$
\begin{align}
g(x)\approx 1 + \frac{1}{2}x + \frac{\frac{1}{2}\left( -\frac{1}{2} \right)}{2}x^{2} + \dots
\end{align}
$$
We can substitute this in to our $f(x)$.

This gets us
$$
\begin{align}
\lim_{ x \to 0 } \frac{2-2\sqrt{ 1+x }+x}{x(1-\sqrt{ 1+x })} \\
=\lim_{ x \to 0 } \frac{2-\left( 2+x-\frac{1}{4}x^{2} \right)+x}{x\left( 1-1+\frac{x}{2}-\frac{x^{2}}{8} \right)}
\end{align}
$$
Which simplifies down to
$$
\begin{align}
\lim_{ x \to 0 } \frac{\frac{1}{4}x^{2}}{x\left( \frac{x}{2}-\frac{x^{2}}{8} \right)} \\
=\lim_{ x \to 0 } \frac{1}{4} \frac{1}{\frac{1}{2}-\frac{x}{8}} \\
=\frac{1}{2}
\end{align}
$$

Any successive term from the Taylor series would have gone to zero, so the limit is just $\frac{1}{2}$.


(c) $\displaystyle \lim_{x \to 0} \left( \frac{1 - \cos k x}{1 - \cosh k x} \right)$. Are there any restrictions on the value of $k$?

We can write this out as the Taylor series for each function, and simplify. Writing only the inside function to be evaluated,

![[Pasted image 20250207204900.png]]
![[Pasted image 20250207205005.png]]

this becomes
$$
\begin{align}
\frac{1-\left( 1-\frac{x^{2}}{2}+\frac{x^{4}}{8}-\dots \right)}{1-\left( 1+\frac{x^{2}}{2}+\frac{x^{4}}{8}+\dots \right)} \\
=\frac{\frac{x^{2}}{2}-\frac{x^{4}}{8}+\dots}{-\frac{x^{2}}{2}-\frac{x^{4}}{8}-\dots} \\
f(x)= \frac{\left( \frac{1}{2}-\frac{x^{2}}{8}+\dots \right)}{\left( -\frac{1}{2}-\frac{x^{2}}{8}-\dots \right)} \\
\end{align}
$$
We can now apply the limit:
$$
\begin{align}
\lim_{ x \to 0 } f(x) = \frac{\frac{1}{2}}{-\frac{1}{2}} = -1 
\end{align}
$$
So the function approaches $-1$ as $x\to 0$.


## 5



We can expand this for every term up to $x^5$. This gets

$$
\begin{align}
x+xq+xq^{2} \\
 & = x+\frac{x^{3}}{2}+\frac{x^{5}}{24}+\frac{x^{5}}{5} - \frac{x^{3}}{6}-\frac{x^{5}}{12} + \frac{x^{5}}{120} \\
 & = x+\frac{x^{3}}{3}+\frac{x^{5}}{6}+O(7)
\end{align}
$$

