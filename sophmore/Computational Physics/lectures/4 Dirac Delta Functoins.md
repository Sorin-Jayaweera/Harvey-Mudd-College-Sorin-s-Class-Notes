
We can construct a simple function that is zero everywhere except 1 at $i=j$. 
$$
\begin{align}
\delta _{i,j}=  \begin{cases}
1 & i=j \\
0 & \text{ otherwise }
\end{cases}

\end{align}
$$
We could be a little more convoluted and do 3 
$$
\begin{align}
E_{ijk}=\begin{cases}
1 & ijk=123 \text{ or cyclic permutatoin } \\
-1 & ijk = 132 \text{ or '' } \\
0 & \text{ else }
\end{cases}
\end{align}
$$
These are useful when writing out sums, since you can turn on and off different terms in any method you want.


A generalized version of the function is the Dirac delta function, which has a big spike of width $\frac{1}{h}$ and height $h$. We then take the limit as the width goes to zero. This is the continuous version of the Dirac delta function. 

We write this as
$$
\begin{align}
\int_{a}^{b} \delta(x)dx=\begin{cases}
1 & a<0<b \\
-1 & b<0<a \\
0 & \text{ otherwise }
\end{cases}
\end{align}
$$
This is not a particularly smooth function.
We can write 
$$
\begin{align}
\int_{-\infty}^{\infty} f(x)\delta(x)dx=f(0)
\end{align}
$$
Or we can shift that by moving the input of the delta function.
Lets try something:
$$
\begin{align}
\int_{-\infty}^{\infty} f(x)\delta(k(x-x_{0}))dx=?
\end{align}
$$
We can set a new integration variable:
$$
\begin{align}
y=k(x-x_{0}) \\
dy=kdx \\
x=\frac{y}{x}+x_{0}
\end{align}
$$
We can rewrite the previous function
$$
\begin{align}
\int_{k(b-x_{0})}^{k(a-x_{0})} f\left( \frac{y}{x}+x_{0} \right)\delta(y) \frac{dy}{k} =\begin{cases}
k>0 & \frac{f(x_{0})}{k} \\
k<0 & -\frac{f(x_{0})}{-\left| k \right| } \\
\end{cases} \\
= \frac{f(x_{0})}{k}
\end{align}
$$
The delta function will kick on at y=0, leaving $f(x_{0})$. 

This gives us the general formula
$$
\begin{align}
\delta(k(x-x_{0})=\frac{\delta(x-x_{0})}{\left| k \right| }
\end{align}
$$
Let's move somewhere else. The normal distribution is given by
$$
\begin{align}
P(x)=\frac{1}{\sqrt{ 2\pi \sigma^{2} }}e^{-\left( \frac{(x-\mu)^{2}}{2\sigma^{2}} \right)}
\end{align}
$$
Because this is normalized, the area under the curve is 1. 

If we let the standard deviation come really close to 0, then we end up with a continuous spike instead of a sharp peak like in the Dirac delta function.

The height of the peak is $\frac{1}{\sigma \sqrt{ 2\pi }}$.


Lets move on another note:
$$
\begin{align}
I=\int_{-\infty}^{\infty} e^{-x^{2}}dx
\end{align}
$$
We don't usually know how to solve this, but we can square it:
$$
\begin{align}
I^{2}=\int_{-\infty}^{\infty} e^{-x^{2}}dx\int_{-\infty}^{\infty} e^{-y^{2}}dy 
\end{align}
$$
We can rearrange this and think about x and y as a point on the Cartesian plane:
$$
\begin{align}
\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} e^{-x^{2}-y^{2}}dxdy
\end{align}
$$
We add up over the whole plane. What if we use polar coordinates instead?
$$
\begin{align}
I^{2}=\int_{0}^{2\pi}  \int_{0}^{\infty} e^{-r^{2}}rdrd\theta
\end{align}
$$
This is an equivalent way of integrating. This is now an integral that we know how to perform:
let $u=r^{2},du=2rdr$
$$
\begin{align}
2\pi \int_{0}^{\infty} \frac{e^{-u}du}{2}  \\
\pi(-e^{-u}\bigg|_{0}^{\infty})  
\\ I^{2}=\pi
\end{align}
$$
Everywhere the function is greater than 1, so we have $I=\sqrt{ \pi }$


