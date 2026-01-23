We have a matrix representing the normal modes of our system
$$
\begin{align}
\mathbb{N}(t) = \begin{pmatrix}
x_{1}(t) \\ x_{2}(t)
\end{pmatrix} = \begin{pmatrix}
A_{+} \cos(\omega_{+} t)\\ A_{-} \cos(\omega_{-} t)\\ 
\end{pmatrix}
\end{align}
$$
It is nice to express this as a complex function, but where we could still recover this. Cos is the real component of $e^{i\omega t}$, so we write the complex mode matrix

$$
\begin{align}
\mathbb{N}' = \begin{pmatrix}
C_{+} e^{i\omega_{+} t} \\
C_{-} e^{i\omega_{-} t}
\end{pmatrix}
\end{align}
$$
Where $C_{+}=A_{+}e^{i\delta t}, \text{ and } C_{-}=A_{+}e^{i\delta t}$.

We rewrite $\mathbb{N}'(t)$ as
$$
\begin{align}
\mathbb{N}'(t) = C_{+} \begin{pmatrix}
1 \\0
\end{pmatrix} e^{i\omega_{+}t } + \begin{pmatrix}
0 \\1
\end{pmatrix} e^{i\omega_{-}t }
\end{align}
$$
where these functions are clearly just the basis functions.
For our original variables, we can write out $\mathbb{Z}(t)$.
$$
\begin{align}
\mathbb{Z}(t) = \begin{pmatrix}
z_{1}(t) \\ z_{2}(t)
\end{pmatrix} = \frac{C_{+}}{2} \begin{pmatrix}
1 \\ 1
\end{pmatrix}e^{i\omega_{+} t} + \frac{C_{-}}{2} \begin{pmatrix}
1 \\ -1
\end{pmatrix} e^{i\omega_{-} t}
\end{align}
$$
To go back to our actual values, we just have
$$
\begin{align} 
\mathbb{X}(t) = \begin{pmatrix}
x_{1} (t)\\x_{2}(t)
\end{pmatrix} = \ce{ Re }(\mathbb{Z}(t))
\end{align}
$$

What do we do when we can't guess the normal modes?

## Matrix approach
Our goal is to write the E-L equations as a vector equation, and solve for the eigenvectors.

Lets take our E-L equations from before
$$
\begin{align}
\ddot{x}_{1} = -kx_{1}-k'x_{1}+k'x_{2} \\
\ddot{x}_{2}  = -kx_{2} -k'x_{2}+k'x_{1}
\end{align}
$$


$$
\begin{align}
m \begin{pmatrix}
\ddot{x}_{1} \\ \ddot{x}_{2} 
\end{pmatrix} = - \begin{pmatrix}
k+k' -k'\\
-k'+ k+k'
\end{pmatrix} \begin{pmatrix}
x_{1} \\ x_{2}
\end{pmatrix}
\end{align}
$$
We can rewrite this in a nicer matrix way
$$
\begin{align}
\ddot{\mathbb{X}} -\frac{1}{m} \mathbb{K} \mathbb{X}
\end{align}
$$
We can solve this by guessing through an Ansatz.
Lets look at the slightly more complicated but nicer matrix $\mathbb{Z}$.
$$
\begin{align}
\ddot{\mathbb{Z}} = -\frac{1}{m} \mathbb{K} \mathbb{Z} 
\end{align}
$$
With the Ansatz $\mathbb{Z}(t) = \underbrace{ \mathbb{Z}_{0} }_{ \text{ constant from init conds } }e^{i\omega t}$

We have
$$
\begin{align}
\frac{ d ^{2}}{d t^{2} } (\mathbb{Z}_{0} e^{i\omega t}) = -\frac{1}{m} \mathbb{K}\mathbb{Z}_{0} e^{i\omega t} \\
-\omega^{2} \mathbb{Z}_{0} e^{i\omega t}= -\frac{1}{m} \mathbb{K}\mathbb{Z}_{0} e^{i\omega t} \\
m\omega^{2}\mathbb{Z}_{0} = \mathbb{K}\mathbb{Z}_{0} 
\end{align}
$$
This is an eigenvalue (or eigenmode) equation.
Note that we have different $\omega$ for each normal mode.
$$
\begin{align}
x_{+} \begin{pmatrix}
1\\1
\end{pmatrix}, \omega_{+} = \sqrt[]{ \frac{k}{m} }  \\
x_{-} \begin{pmatrix}
1\\-1
\end{pmatrix}, \omega_{-} = \sqrt[]{ \frac{k+2k'}{m} }  \\
\end{align}
$$
We can solve the eigenvalue problem
$$
\begin{align}
\mathbb{K}\mathbb{Z}_{0} - m\omega^{2} \mathbb{Z}_{0} = 0 \\
(\underbrace{ \mathbb{K}-m\omega^{2}\mathbb{I} }_{ \mathbb{A} })\mathbb{Z}_{0} =0
\end{align}
$$
This is of the form $\mathbb{A}\mathbb{Z}_{0}=0$
We can solve this with
$$
\begin{align}
\mathbb{A}^{-1}\mathbb{A}\mathbb{Z}_{0} = \mathbb{A^{-1}}0 \\
\mathbb{Z}_{0} = \begin{pmatrix}
0\\0
\end{pmatrix}  
\end{align}
$$
We need a non invertible matrix
$$
\begin{align}
\det{(\mathbb{K}-m\omega^{2}\mathbb{I})}=0 
\end{align}
$$

Lets find the eigenvalues
$$
\begin{align}
\begin{pmatrix}
k+k'-m\omega^{2} & -k' \\
-k ' & k+k'-m\omega^{2}
\end{pmatrix}=0
\end{align}
$$
Taking the determinant yields 
$$
\begin{align}
(k+k'-m\omega^{2})^{2}-k'^{2}=0
\end{align}
$$
This is a difference of two squares, in the form $(a+b)(a-b)$ 
$$
\begin{align}
(k+k'-m\omega^{2}+k')(k+k'-m\omega^{2}-k' )=0
\end{align}
$$
This yields two different solutions for what $\omega$ can be (which should agree with what we found before)!

$$
\begin{align}
m\omega^{2} = k+2k' \\
\omega_{1} = \sqrt[]{  \frac{k+2k'}{m} }  = \omega_{-} \\
\end{align}
$$

We can plug in the values of $\omega$ to find for our eigenvectors.

For example
$$
\begin{align}
(\mathbb{K}-m\omega^{2}\mathbb{I})\begin{pmatrix}
a\\ b 
\end{pmatrix} = 0 \\
\begin{pmatrix}
\cancelto{}{k } + k' - \frac{\cancelto{  }{ m }(\cancelto{  }{ k }+2k')}{\cancelto{  }{ m }} & -k  \\
-k' & -k'
\end{pmatrix} \begin{pmatrix}
a\\ b
\end{pmatrix} = \begin{pmatrix}
0 \\0
\end{pmatrix} \\
k' \begin{pmatrix}
-1  & -1 \\ -1  & -1
\end{pmatrix} \begin{pmatrix}
a \\ b
\end{pmatrix} = \begin{pmatrix}
0 \\ 0
\end{pmatrix} 
\end{align}
$$
This gives us the equations
$-a -b=0$, so $a=-b$.

This is our eigenvector, $\begin{pmatrix}1 \\ -1\end{pmatrix}$

You can do the same thing with the other normal mode for $\begin{pmatrix}1\\1\end{pmatrix}$.

We now have the complex functions of time with any complex coefficients $A_{1},A_{2}$ as
$$
\begin{align}
\mathbb{Z}(t)= A_{1}\mathbb{Z}_{0} ^{1}e^{i\omega_{1} t}+ A_{2}\mathbb{Z} _{0} ^{2}e^{i\omega_{2} t} \\
\text{ where here, } \\
\mathbb{Z}_{0}^{1}= \frac{1}{2}\begin{pmatrix}
1\\-1
\end{pmatrix}, \omega_{1} = \sqrt[]{ \frac{k+2k'}{m} }  \\
\mathbb{Z}_{0}^{2}= \frac{1}{2}\begin{pmatrix}
1\\1
\end{pmatrix}, \omega_{2} = \sqrt[]{ \frac{k}{m} }  \\
\end{align}
$$
(note that the $\frac{1}{2}$ here is arbitrary, but we write it to match )


## Practice problem
Lets take three masses with 4 springs between them, all of mass $m$ and spring constant $k$. 

The legrangian for this is
$$
\begin{align}
U= \frac{1}{2}k(x_{3}^{2}+(x_{3}-x_{2})^{2}+(x_{2}-x_{1})^{2}+x_{1}^{2} ) \\
T = \frac{1}{2}m(\dot{x_{1}}^{2}+\dot{x_{2}}^{2}+\dot{x_{3}}^{2})  \\
\mathscr{L} = \frac{1}{2}m(\dot{x_{1}}^{2}+\dot{x_{2}}^{2}+\dot{x_{3}}^{2}) - \frac{1}{2}k(x_{3}^{2}+(x_{3}-x_{2})^{2}+(x_{2}-x_{1})^{2}+x_{1}^{2} ) 
\end{align}
$$
We can find the EL equations for these 
$$
\begin{align}
m\ddot{x_{1}} &  = \frac{1}{2}k(2x_{1}-2x_{2}+2x_{1})\\
m\ddot{x_{2}}  & = \frac{1}{2}k(2x_{2}-2x_{3}) \\
m\ddot{x_{3}}  & = \frac{1}{2}k(2x_{3} + 2x_{3} - 2x_{2})\\
\end{align}
$$

We can write these as a matrix form
$$
\begin{align}
\begin{pmatrix}
\ddot{x_{1}} \\ \ddot{x_{2}} \\ \ddot{x_{3}}
\end{pmatrix}
 = \frac{k}{2m} \begin{pmatrix}
4 & -2 & 0 \\
0 & 2 & -2 \\
0 & -2 & 4
\end{pmatrix} \begin{pmatrix}
x_{1}\\ x_{2}\\ x_{3}
\end{pmatrix}
\end{align}
$$

We can take this as the matrix equation
$$
\begin{align}
\ddot{\mathbb{X}} = \frac{k}{2m} \mathbb{K}
\end{align}
$$

