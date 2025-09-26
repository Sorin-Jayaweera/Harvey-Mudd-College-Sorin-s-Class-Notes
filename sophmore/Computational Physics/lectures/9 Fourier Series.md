We leverage the fact that
$$
\begin{align}
\int_{0}^{L}\underbrace{ \sin\left( \frac{m\pi x}{L} \right) }_{ u_{m} }\underbrace{ \sin\left( \frac{n\pi x}{L} \right) }_{ u_{n} }dx = \begin{cases}
0, & n \neq m \\
\frac{L}{2} & n=m
\end{cases} = \frac{L}{2} \delta _{nm}
\end{align}
$$
Where we have that
$\left< u_{m},u_{n} \right> =1$

$$
\begin{align}
f(x) = a_{0} + \sum_{n=1}^{\infty} \left( a_{n}\cos\left( \frac{n\pi x}{L} \right) + b_{n}\sin\left( \frac{n\pi x}{L} \right) \right)  
\end{align}
$$
The trig functions are solutions to 
$$
\begin{align}
\frac{d ^{2}u}{dx^{2}} = \lambda u(x) \\
u'' = \lambda u
\end{align}
$$
Lets have two $u's \text{ and } \text{ two } \lambda's$
$$
\begin{align}
u_{1}''=\lambda_{1}u_{1} \\
u_{2}''=\lambda_{2}u_{2}
\end{align}
$$
Lets consider something that initially seems unmotivated:
$$
\begin{align}
(u_{1}^{*})u_{2}-u_{1}^{2}u_{2}''  & = \lambda_{1}^{*}u_{1}^{*}u_{2} - u_{1}^{*}\lambda_{2}u_{2} \\
 & = (\lambda_{1}^{*}-\lambda_{2})u_{1}^{*}u_{2}
\end{align}
$$
We can integrate this by parts
$$
\begin{align}
\int_{a}^{b}  u_{1}''^{*} u_{2}-u_{1}^{*}u_{2}''^{*} \ dx  = \int_{a}^{b} \left( \lambda_{1}^{*}-\lambda_{2} \right) u_{1}^{*}u_{2} \ dx \\
\underbrace{ \left[ u_{1}'^{*}u_{2} - u_{1}^{*}u_{2}' \right]  \bigg|_{a}^{b} }_{ \text{ bilinear concomitant } } - \int_{a}^{b} \cancelto{ 0 }{ \left[ (u_{1}^{*})' u_{2}' -(u_{1}^{*})' u_{2}'\right]  }dx = (\lambda_{1}^{*}-\lambda_{2})\int_{a}^{b} u_{1}^{*}u_{2} \ dx
\end{align}
$$
What if we make the condition that the basis function has to vanish.
Suppose $u_{n}(a)=0, u_{n}(b)=0$. This makes the bilinear concomitant zero. 

We could also make $u'_{n}(a) = 0, u'_{n}(b)=0$, or we can mix and match. 

If the bilinear concomitant is zero and $\lambda_{1}^{*}\neq \lambda 2$, then $\left< u_{1},u_{2} \right> =0$. 
If, on the other hand, we have $u_{1}=u_{2}$, then $\lambda_{1}^{*}-\lambda_{1}=0$, $\lambda_{1}^{*}=\lambda_{1}$, so $\lambda_{1} \text{ is real }$. For any functions that satisfy the conditions we had earlier (second derivatives being scaler multiples of the original function), then the basis functions are orthogonal and have real eigenvalues. This is general, and works for things more complicated than sin and cos!

>[!abstract]+  Side note
> This trick can get extended into three dimensional space where
$u_{1}\nabla^{2}u_{2}-u_{2}\nabla^{2}u_{1}$, where the governing integrations are second order - integrating by parts makes nice things fall out. 

Suppose
$$
\begin{align}
u(0)=0, u'(L)=0
\end{align}
$$
We can make the basis functions
$$
\begin{align}
 & u(0)=0 & \implies  & \sin(\lambda x) \\
 & u'(L)=0 & \implies  & \lambda \cos(\lambda L) = 0, \\
 &   & & \lambda L= \left( n+\frac{1}{2} \right)\pi \\
\end{align}
$$

$$
\begin{align}
u_{n}=\sin \left[ \frac{\left( n+\frac{1}{2} \right)}{L} \pi x \right] 
\end{align}
$$
We get
$$
\begin{align}
f(x)=\sum_{n=0}^{\infty} a_{n}\sin \left[ \left( n+\frac{1}{2} \right)\pi \frac{x}{L} \right] 
\end{align}
$$
If our $f(x)=x(L-x)$
We can find values of $a_{n}$ by summing
$$
\begin{align}
x(L-x)=\sum_{n=0}^{\infty} a_{n}\sin \left[ \left( n+\frac{1}{2} \right) \pi \frac{x}{L} \right] 
\end{align}
$$
We can leverage the property that, if $\lambda_{1}\neq \lambda_{2}$ (were talking about different eigenfunctions), then we should get zero.
We multiply by one of our basis functions, 
$$
\begin{align}
\sin \left[ \left( m+\frac{1}{2} \right)\pi \frac{x}{L} \right] 
\end{align}
$$

We can now integrate:
$$
\begin{align}
\int_{0}^{L} x(L-x)\sin \left[ \left( m+\frac{1}{2} \right) \pi \frac{x}{L}\right] dx = \underbrace{ \delta _{nm}a_{n} \frac{L}{2} }_{ \text{ from the orthogonality of } u_{m}\text{ and }  u_{n} }
\end{align}
$$

We get
$$
\begin{align}
\frac{1}{2}\int_{0}^{L} \sin ^{2} \left[ \left( m+\frac{1}{2} \right) \pi \frac{x}{L} \right] dx \\
\end{align}
$$
With the identity
$$
\begin{align}
\sin ^{2}\theta = \frac{1-\cos(2\theta)}{2}
\end{align}
$$
$$
\begin{align}
\frac{1}{2}\int_{0}^{L} 1 - \cos \left[ (2m+1)\pi \frac{x}{L} \right]\, dx  
\end{align}
$$












