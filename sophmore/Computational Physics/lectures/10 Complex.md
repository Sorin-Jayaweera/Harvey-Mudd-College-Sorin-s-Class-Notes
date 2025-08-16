Let $z=x+iy$
$$
\begin{align}
f(z)  & = u(x,y) + iv(x,y)  \\
\text{ if } \delta z  & = \delta x \\
f'(z)  & = \frac{ \partial u }{ \partial x }  + i \frac{d v}{dx}   \\
\text{ if } \delta z  & = \delta y \\
f'(z)  & = \frac{1}{i} \frac{ \partial u }{ \partial y }  + \frac{i}{i} \frac{ \partial v }{ \partial y }  \\
 & =\frac{ \partial v }{ \partial y } - i \frac{ \partial u }{ \partial y }  \\
\text{ therefore, } \\
\frac{ \partial u }{ \partial x } = \frac{ \partial v }{ \partial y }  & \text{ and }  \frac{ \partial v }{ \partial x } =- \frac{ \partial u }{ \partial y }  \\
\text{ this is called the  } \\
\text{ Cauchy-Riemann condition }
\end{align}
$$

For example,
$$
\begin{align}
f(z)=\underbrace{ z^{2}-x^{2} }_{ u }-\underbrace{ y^{2}+2xy }_{ v }i \\
\text{ we can check the conditions } \\
\frac{ \partial u }{ \partial x } \stackrel{?}{=}   \frac{ \partial v }{ \partial y } , 2x=2x \\
\frac{ \partial v }{ \partial x } \stackrel{?}{=} \frac{ \partial u }{ \partial y }, 2y=2y 
\end{align}
$$
So this satisfies it.
We have an easy function that doesn't satisfy this:
$f(z)=z^{*}=x-iy$
$1\neq-1$.

Any integer power of $z$ is differentiable.