A lightning review of partial differential equations.

We've seen the maxwell equations, the Schrödinger equation, etc. 

We usually use separation of variables to solve ordinary differential equations.

Lets take a prototypical equation.
$$
\begin{align}
y''(x)+P(x)y' + Q(x)y = R(x)
\end{align}
$$
We are worried about nonlinearities. $R(x)$ is a forcing term. If $P,Q$ have a power series expansion that works around the point we care about, $x_{0}$. 
It is the point where we can make the equation legal without setting one of them to zero. 

In many equations, this isn't true - a singular point. 

There are also regular singular points, where we have
$\left( x-x_{0} \right)P(x)$ has a convergent series and $(x-x_{0})^{2}Q(x)$ also has a convergent series. If this is the case, we can look for a series expansion of the solution functions, which we will do. 

If these don't converge, it is a lot harder.

For example: 
Bessel's equation looks like
$$
\begin{align}
x^{2}y''+xy'+(x^{2}-n^{2})y=0
\end{align}
$$
We have to put it in the nice form, so we divide by $x^{2}$
$$
\begin{align}
y'' + \frac{1}{x}y' + \left( 1-\frac{n^{2}}{x^{2}} \right)y = 0 
\end{align}
$$
This has a singular point at $x=0$. If we multiply $\frac{1}{x}$ by $(x-x_{0})$, then we have a nice thing. Similarly, we have a nice part for $\left( 1-\frac{n^{2}}{x^{2}} \right)(x-x_{0})^{2}$.

We have this centered at 0 where it would explode. 


We define DDSHO
$$
\begin{align}
y''+ 2\beta y'+\omega_{0}^{2}y=\frac{F(x)}{m}
\end{align}
$$
where $\beta=\frac{b}{m}$.




what about
$$
\begin{align}
y''+ \frac{\alpha}{x}y' + \frac{\beta}{x^{2}}y=0
\end{align}
$$
This is really stupid simple to solve. It is called an equidimensional equation, since everything has the same dimension. 
Lets guess $y=x^{P}$.

This would become
$$
\begin{align}
p(p-1)x^{p-2} + \frac{\alpha}{x}px^{p-1} + \frac{\beta}{x^{2}}x^{p} = 0 \\
x^{p-2}\left[ p(p-a)+p\alpha+\beta \right] = 0 
\end{align}
$$
This is a quadratic equation to solve for the power of an equidimensional equation, which has two linearly independent solutions. 


Another example: 
$$
\begin{align}
(1-x^{2})y'' - 2xy' + l(l+1)y = 0
\end{align}
$$
This has singular points at $x=\pm 1$. This is Legandre's equation from quantum mechanics, where we are solving for the polar angular equation (north to south pole).

## Sin and Cos
Lets work all the way through an equation:
$$
\begin{align}
y''+y=0
\end{align}
$$
We have two linearly independent equations. Lets choose (arbitrary numbers) that are linearly independent:
$$
\begin{align}
\alpha(0)=1 & &  \alpha'(0)=0 \\
\beta(0)=0 & &  \beta'(0) =1
\end{align}
$$
We have to have two pieces of information to carry forwards (imagine a ball frozen in space - you need to know its position and velocity to time evolve it). We could use different slopes but would just get a phase shift relative to the sin and cos solutions. And the amplitudes don't matter, as long as they are orthogonal - so zero and something. Just 1 is a nice number.

By consequence of the original equation,
$$
\begin{align}
y'''+y'=0
\end{align}
$$
let $\eta = y'$
$\eta '' + n=0$.

Then $\alpha'(x)$ has to be a linear combination of the two independent solutions, $c \alpha(x) + d \beta(x)$
$$
\begin{align}
\alpha'(0)=0 = d \cancelto{ 0 }{ \beta(0) } \\
\alpha'(x)= d \beta(x)
\end{align}
$$
Similarly, 
$$
\begin{align}
\beta'(0)=1 = f + 0g\\
\beta'(x) = \alpha + g \beta(x) \\
\beta''(x)= \alpha'(x)+g \beta'(x) \\
-\beta(x)= d \beta(x)+ g \beta'(x) \\
\therefore g=0 \\
\end{align}
$$
We now have
$$
\begin{align}
\beta'(x)= \alpha(x) \\
\alpha'(x) = d \beta(x) \\
\alpha''(x) = -\alpha(x) = d \beta'(x)
\end{align}
$$

At $x=0$, $-1=d$.

How do we prove $\alpha^{2}+\beta^{2}=1$?
We can take a derivative and show that it is 0, then its a constant.

$$
\begin{align}
2\alpha \alpha' + 2\beta \beta'= c  \\
\text{ recall that } d=-1,  \\
\alpha\ = - \beta(x) \\
\beta' = \alpha(x)  \\
\text{ so the derivative is } \\
2\alpha(-\beta) + 2 \beta(a) = 0
\end{align}
$$
Therefore, $\alpha^{2}+\beta^{2}=1$ is true everywhere. 


Lets move on to 
## Wronskian

$$
\begin{align}
y'' = A(x)y' + B(x)y
\end{align}
$$
Suppose that $f(x),g(x)$ solve the differential equation. 

The Wronskian is $w=fg'-f'g$. 
We can take the derivative: $\frac{ d w}{d x }$. It smells faintly like the bilinear concomitant thing...

$$
\begin{align}
\frac{ d w}{d x }  & = f'g' + fg'' - f''g - f'g'\\
 & =  fg'' - f''g  \\
\end{align}
$$
But, each of the $A(x)\text{ and } B(x)$ are solutions. We can plug those in and see what we get. 

$$
\begin{align}
\frac{ d w}{d x }  & = f[Ag' + Bg] - [Af'+Bf]g \\
 & = A(x)[fg'-f'g]
\end{align}
$$
This is the Wronskian itself: $A(x)w(x)$
in other words,
$$
\begin{align}
\frac{1}{w} \frac{ d w}{d x } = A(x)
\end{align}
$$
This is the logarithmic derivative,
$$
\begin{align}
\frac{ d ln(w)}{d x } = A(x) \\
ln(w) = \int A(x)dx \, +\,  C
\end{align}
$$
$$
\begin{align}
W(x)= C e^{\int A(x)dx}
\end{align}
$$
So what? What can we use this for?

This is called Abel's formula. In essence, it is a way of getting a second solution if you already know the first. 

Lets take a DE to play with:
$$
\begin{align}
x^{2}y''+ 2xy' -2y = 0 \,  & (x>0)
\end{align}
$$
The first thing for us to show is that
$y_{1}(x)=x$ is a solution, and second is to use Abel's formula to find $y_{2}$.

The first is easy to verify by just plugging it in.
Next:
$$
\begin{align}
y''= \underbrace{ -\frac{2}{x} }_{ A(x) }y' + \frac{2}{x^{2}}y
\end{align}
$$
$w(x)= c e^{\frac{-2}{x}dx} = c xe^{-2}$

$w = fg'=f'g$. We have one solution. We have

$$
\begin{align}
x y_{2}' - y_{2} = \frac{C}{x^{2}}
\end{align}
$$
We can now solve this:

$$
\begin{align}
x^{2} \frac{ d }{d x } \left( \frac{y_{2}}{x} \right) = \frac{c}{x^{2}} \\
d \left(  \frac{y^{2}}{x} \right) =\frac{c}{x^{4}}dx \\
\frac{y_{2}}{x} = \int \frac{C}{x^{4}}dx = -\frac{C}{3} \frac{1}{x^{3}} + c' \\
y_{2} = -\frac{c}{3} \frac{1}{x^{2}} + \cancelto{ 0 }{ xc' }
\end{align}
$$

