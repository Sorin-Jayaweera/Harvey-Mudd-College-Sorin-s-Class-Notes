![[Pasted image 20250409121236.png]]

## A
We guess the solution $y=x^{r}$, and plug it into our equation
$$
\begin{align}
y' = rx^{r-1} \\
y'' = r(r-1)x^{r-2}
\end{align}
$$

This gives us
$$
\begin{align}
x^{2}r(r-1)x^{r-2} + (2\alpha+1)x rx^{r-1}+ 4 \beta x^{r} = 0 \\
\text{ this simplifies to } \\
x^{2}r^{2}x^{r-2}-x^{2}rx^{r-2} + (2\alpha+1)xrx^{r-1}+4\beta x^{r}=0
\end{align}
$$
This gives us
$$
\begin{align}
r^{2}x^{r}- rx^{r}+(2\alpha+1)rx^{r}+4\beta x^{r}=0 \\
x^{r}(r^{2}-r+(2\alpha+1)r+4\beta)=0 \\
x^{r}(r^{2} +2\alpha r+4\beta )=0
\end{align}
$$


R must solve the equation
$$
\begin{align} \\
r^{2}+2\alpha r +4\beta=0
\end{align}
$$

## B
if $\alpha=1$ and $\beta=-1$, we have the equation
$$
\begin{align}
r^{2}+2r-4=0
\end{align}
$$

The quadratic formula is
$$
\begin{align}
x= \frac{-b\pm  \sqrt[]{ b^{2}-4ac }}{2a} 
\end{align}
$$
Let $a=1,b=2,c=-4,\text{ and } x=r$.
This gives us
$$
\begin{align}
r =  \frac{-2\pm  \sqrt[]{ 4+16 } }{2} \\
r = \frac{-2\pm  \sqrt[]{ 20 } }{2} \\
r = \frac{-1\pm  \sqrt[]{ 5 }}{2} 
\end{align}
$$


## C
For there to be a single value of r, $b^{2}-4ac=0$. 

We have defined
$$
\begin{align}
b=2\alpha, a = 1, c = 4 \beta
\end{align}
$$
Thus, for r to be single valued,
$$
\begin{align}
(2\alpha)^{2}-4(4\beta)=0 \\
4\alpha^{2}=16\beta \\
\alpha^{2}= 4 \beta \\
\alpha=2\sqrt[]{ \beta } 
\end{align}
$$
## D

If $r$ has a single solution, 
$$
\begin{align}
r = -\alpha  \\
\end{align}
$$
Lets take the solution:
$$
\begin{align}
y & =x^{r}lnx \\
y'  & = (x^{r-1}) + rx^{r-1}\ln(x) \\
y''  & = (r-1)x^{r-2}+ rx^{r-2}+r(r-1)x^{r-2}\ln(x) \\
 & = rx^{r-2}-x^{r-2}+rx^{r-2}+r^{2}x^{r-2}\ln(x)-rx^{r-2}\ln(x) \\
 & =x^{r-2}(r-1+r+r^{2}\ln(x)-r\ln(x)) \\
 & = x^{r-2}(r^{2}\ln(x)+2r-r\ln(x)-1)
\end{align}
$$
We can stuffy this in to our equation to see if it holds:
![[Pasted image 20250411163653.png]]
Lets simplify each term at a time.
We showed that $r=-\alpha$

$$
\begin{align}
x^{2}y''(x) = x^{r}(\alpha^{2}\ln(x)-2\alpha+\alpha\ln(x)-1)   \tag{1} 
\end{align}
$$

$$
\begin{align}
(2\alpha+1)xy'(x) = (2\alpha+1)x^{r}+rx^{r}\ln x   \tag{2} 
\end{align}
$$

$$
\begin{align}
4\beta y =\alpha^{2}x^{r}\ln x   \tag{3} 
\end{align}
$$

We can add eqs. 2 and 3 to get
$$
\begin{align}
x^{r}\left(\alpha^{2}\ln x+ 2\alpha+1-\alpha\ln x \right)
\end{align}
$$
We can see that this is a negated version of eq 1, so the sum is zero.

Thus, $x^{r}\ln x$ is a solution to the differential equation. 

![[Pasted image 20250409121249.png]]
Because the slab is only heated on 1 surface, I will treat this as a 1 dimensional heat transfer, so that the temperature will be uniform at any given slice down on the plane parallel to the top surface. 

The 1 dimensional heat equation is given by
$$
\begin{align}
c\rho \frac{ \partial u }{ \partial t } - \frac{ \partial  }{ \partial x } \left( k \frac{ \partial u }{ \partial x }  \right)= g(x,t)
\end{align}
$$
where $u(x,t)$ is the temperature, k is the thermal conductivity, and g is the power per unit volume.

We can make some initial assumptions about the rod, as listed on the web page for this class (Partial Differential equations simplifications and eq. 3)

to get
$$
\begin{align}
\frac{ \partial u }{ \partial t } = D \frac{ \partial^{2}u }{ \partial x^{2} } 
\end{align}
$$
Where $D$ is the thermal diffusivity $\frac{k}{c\rho}$. 

We have to set initial conditions of the material. Assuming that we start from a steady state:
$$
\begin{align}
u(x,0)=T_{1}
\end{align}
$$
We have two initial boundary conditions:
$$
\begin{align}
u(0,0) = T_{1} \\
u(0,t) = u(0,t+\tau) 
\text{ for all } N \in \mathbb{N}
\end{align}
$$

Assuming separation of variables, we can take
$$
\begin{align}
u(x,t) = X(x)T(t)T_{1}\\
\frac{ d u}{d t } = X(x)T'(t) \\
\frac{ d ^{2}u}{d x^{2} } = X''(x)T(t)
\end{align}
$$
This way, $X(x)\text{ and } T(t)$ are unitless.

We can plug these in and define a constant $k$, since they can't change with either x or t for this to be true:
$$
\begin{align}
\frac{1}{D} \frac{T'}{T} = \frac{X''}{X} = -k^{2}
\end{align}
$$
We see that our surface temperature has periodic conditions, so both the time and position functions must be periodic. 

We have two constraints:
$$
\begin{align}
T' = -k^{2}D t \\
X'' = -k^{2}X
\end{align}
$$
We can start with the temperature dependent solution. We have the general solution
$$
\begin{align}
T(t) = C_{0}e^{-Dk^{2}t}
\end{align}
$$
We can now apply boundary conditions: 
$$
\begin{align}
T(t) = T(t+\tau) \\
C_{0}e^{-Dk^{2}t} = C_{0} e^{-Dk^{2}(t+\tau)}
\end{align}
$$
This tells us that
$$
\begin{align}
1 = \frac{e^{-Dk^{2}(t+\tau)}}{e^{-Dk^{2}t}} \\
1 = e^{-Dk^{2}\tau} \\
-Dk^{2}\tau = 2n\pi i
\end{align}
$$
We can now solve for $k$, our rate constant:
$$
\begin{align}
k = \sqrt[]{ \frac{-2n\pi i}{D\tau} }  \\
k=\sqrt[]{ -i} \sqrt[]{ \frac{2n\pi}{D\tau} }    \\
k=i^\frac{3}{2}\sqrt[]{ \frac{2n\pi }{D\tau} } 
\end{align}
$$

This gives us the time dependence as
$$
\begin{align}
T(t) = C_{0} e^{\frac{-2n\pi}{\tau} i^{3} }
\end{align}
$$
We can define $\omega = \frac{2\pi}{\tau}$
$$
\begin{align}
T(t) = C_{0}e^{-\omega ni  ^{3}}
\end{align}
$$

We can also find our spatial function:
$$
\begin{align}
X'' = -k^{2}x \implies X(x)= C_{1}e^{ikx}+C_{2}e^{-ikx} \\
\end{align}
$$
We know that $X(0)=1$, so
$$
\begin{align}
C_{1}+C_{2}=1
\end{align}
$$
We can assume that the temperature far away down the box will be 0 for some frequencies, and can apply a condition to get rid of either $A$ or $B$. We can expand as:

$$
\begin{align}
C_{1}e^{i^{\frac{5}{2}\sqrt[]{ \frac{2n\pi }{D\tau} } x}}+C_{2}e^{-i^{\frac{5}{2} }\sqrt[]{ \frac{2n\pi}{D\tau} }x } \\
=C_{1}e^{-i^{\frac{1}{2}} \sqrt[]{ \frac{2n\pi}{D\tau} } x}+C_{2}e^{i^{\frac{1}{2}}\sqrt[]{ \frac{2n\pi}{D\tau} } x}
\end{align}
$$
We don't want our equation to explode as $x\to \infty$, so $C_{2}=0$, and $C_{1}=1$ by the previous expression. 

We can write out our expression now:
$$
\begin{align}
U(x,t) = X(x)T(t)T_{1} \\
U(x,t)= \sum_{n=0}^{\infty} A_{n}T_{1}e^{-\sqrt[]{ \frac{2n\pi i}{D\tau} } x}e^{\omega n it} \\
\end{align}
$$

We can solve for each coefficient $A_{n}$. Using $U\left( 0, t<\frac{\tau}{2 } \right)=T_{1}$,
$$
\begin{align}
  \begin{cases}
1 & t\leq  \frac{\tau}{2} \\
-1  & \frac{\tau}{2} < t <\tau
\end{cases} = \sum_{n=0}^{\infty} A_{n}e^{i \omega n  t }
\end{align}
$$

We can solve this by multiplying by $e^{-i\omega mt}$ and integrating for all $m$. This will act as a delta function for when $n=m$:

$$
\begin{align}
\int_{0}^{\infty} e^{-i\omega nt} dt= A_{n} \int_{0}^{\infty} e^{i\omega t(n-m)}\\
\int_{0}^{\frac{\tau}{2}} e^{-i\omega nt} dt= A_{n} \int_{0}^{\frac{\tau}{2}} 1dt \\
-\frac{1}{i\omega nt}\left( e^{i\omega \frac{n\tau}{2}}-1 \right) = A_{n} \frac{\tau}{2} \\

\end{align}
$$
For $t\leq \frac{\tau}{2}$
$$
\begin{align}
A_{n} = \frac{2}{i\tau \omega n t}(e^{i\omega n \frac{\tau}{2}}-1)
\end{align}
$$
For $\frac{\tau}{2} < t<\tau$:
$$
\begin{align}
A_{n} = -\frac{2}{i\tau \omega nt}\left( e^{i\omega n \frac{\tau}{2}} -1 \right)
\end{align}
$$

We have now that

$$
\boxed{
\begin{align}
U(x,t)= \sum_{n=0}^{\infty} A_{n}T_{1}e^{-\sqrt[]{ \frac{2n\pi i}{D\tau} } x}e^{\omega n it}  \\
\text{ where } \\
A_{n} =  \frac{2}{i\tau \omega nt}\left( e^{i\omega n \frac{\tau}{2}} -1 \right)\times \begin{cases}
1  &  \text{ T\% } \tau < \frac{\tau}{2 }\\ -1 & T \% \, \tau > \frac{\tau}{2} 
\end{cases} 
\end{align}
}
$$

( $\%$ denotes modulo).




![[Pasted image 20250409121259.png]]
On the 5 surfaces of the cube, we have 0 potential. We can define 3 axis, $x,y,z$. Along the $x$ and $y$ axes we will have a periodic solution, with boundary conditions. Let $r$ be a three dimensional vector $[x,y,z]$. Assuming independence, we can perform a separation of variables.
$$
\begin{align}
V(r) = V_{0}\mathbb{X}(x) \mathbb{Y}(y)\mathbb{Z}(z)
\end{align}
$$
This way, we can have each function vary from $0$ to $1$, and map the result to $V_{0}$.

Along the $x$ and $y$ axes, we will have a periodic function that must go to zero at the boundaries. This gives us 
$$
\begin{align}
\mathbb{X}(x) = \sin\left( \frac{n\pi x}{L} \right) \\
\mathbb{Y}(x) = \sin\left( \frac{n\pi y}{L} \right)  \\
n \in \mathbb{N}
\end{align}
$$

Using the 3d differential equation,
$$
\begin{align}
\frac{X''(x)}{X(x)} + \frac{Y''(y)}{Y(y)} + \frac{Z''(z)}{Z(z)} = 0
\end{align}
$$
We can substitute in
$$
\begin{align}
\frac{X''}{X} = -\left( \frac{n\pi }{L} \right)^{2} \\
\frac{Y''}{Y} = -\left( \frac{n\pi }{L} \right)^{2} \\
\end{align}
$$

This gets us
$$
\begin{align}
Z''(z) = 2\left( \frac{n\pi }{L} \right)^{2} Z(z)
\end{align}
$$

$$
\begin{align}
Z''(z) = 2\left( \frac{n\pi}{L} \right)^{2}Z(z)
\end{align}
$$
Because we have the boundary condition $Z(0)=0$ and $Z(L)=1$, we write this out as
$$
\begin{align}
Z(z)=ae^{\frac{n\pi }{L}z} + be^{\frac{-n\pi }{L}z}
\end{align}
$$
To satisfy $Z(0)=0$, 
$$
\begin{align}
a+b =0  \\
\text{ to use the nice sinh, }\\
a = \frac{1}{2}, b = -\frac{1}{2}
\end{align}
$$

$Z(z) = \frac{e^{n\pi y}+e^{-n\pi y}}{2} =\sinh\left( \frac{2n\pi z}{L} \right)$

$\sinh$ does not satisfy  $Z(L)=1$ nicely though, since $\sinh(\pi)\approx 11.5$. To do this, we superpose orthogonal eigenfunctions.

$$
\begin{align}
V(r) = \sum_{n=1}^{\infty} c_{n}\sin\left( \frac{n\pi x}{L}  \right) \sin\left( \frac{n\pi y}{L} \right)\sinh\left( \frac{2n\pi z}{L} \right)
\end{align}
$$


At the back wall, this is
$$
\begin{align}
1 = \sum_{n=1}^{\infty} c_{n}\sin\left( \frac{n\pi x}{L}  \right) \sin\left( \frac{n\pi y}{L} \right)\sinh\left( \frac{2n\pi L}{L} \right)
\end{align}
$$

Which we know how to solve. We multiply by orthogonal functions and integrate. Here, that will be a double integral.

$$
\begin{align}
\sin\left( \frac{m\pi x}{L} \right)\sin\left( \frac{m\pi y}{L} \right) = \\ \sum_{m=1}^{\infty} \sum_{n=1}^{\infty} c_{n}\sin\left( \frac{m\pi x}{L} \right)\sin\left( \frac{m\pi y}{L} \right) \sin\left( \frac{n\pi x}{L}  \right) \sin\left( \frac{n\pi y}{L} \right)\sinh\left(2 n\pi\right)
\end{align}
$$

These m and $n$ functions are orthogonal, so we get
$$
\begin{align}
\int_{y=0}^{L}dy \int_{x=0}^{L}dx \sin\left( \frac{n\pi x}{L} \right) \sin\left( \frac{n\pi y}{L} \right) = \frac{c_{n}L^{2}}{4} \sinh(2n\pi)
\end{align}
$$
Evaluating this left side, we get
$$
\begin{align}
\left( \frac{L}{n\pi} \right)^{2}\cos\left( \frac{n\pi x}{L} \right) \cos\left( \frac{n\pi y}{L} \right)\bigg|_{x=0}^{L}\bigg|_{y=0}^{L}   = \frac{c_{n}L^{2}}{4}\sinh(2n\pi) 
\end{align}
$$

This becomes 
$$
\begin{align}
\left( \frac{L}{n\pi} \right)^{2} \bigg[ (\cos\left( n\pi\right)-1) ( \cos(n\pi)-1) \bigg] = \frac{c_{n}L^{2}}{4}\sinh(2n\pi) \\
\frac{4}{(n\pi)^{2}}\frac{ (\cos(n\pi)-1)^{2}}{\sinh(2n\pi)} = c_{n} 
\end{align}
$$


We see that when $\cos(n\pi)=1$, this is $0$. Thus, we only have odd $c_{n}$.

We have finally that
$$
\begin{align}
V(r) = \sum_{n \text{ odd }}^{} \frac{16V_{0}}{(n\pi)^{2}\sinh(n\pi)} \sin\left( \frac{n\pi x}{L} \right)\sin\left( \frac{n\pi y}{L} \right)\sinh\left( \frac{2n\pi z}{L} \right)
\end{align}
$$





