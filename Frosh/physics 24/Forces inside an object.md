  Recall:
	Tension is constant in different sections of string when its massless. But ropes have mass

Photo elastic materials can directly image stress ($\frac{force}{area}$). What is happening inside the objects?
hint: were basically doing introduction to differential equations.

Especially in engineering design, we want to be able to understand forces and stress internal to a structure to find where weak spots may be. While this is a difficult problem, we can do this more simply in 2d.

## How to solve a separable, 1st order, ordinary, differential equation with known initial value


#seperable_differential_equation: if you can factor a differential equation to some form $$
\frac{d y}{dx} = f(x)g(x)
$$
This makes it nice, because you can just do $\frac{d y}{g(x)} = f(x) dx$
#first_order: one derivative 
#ordinary:no partial derivatives
known initial value: knowing $y(x=a)=b$ and want to solve y(x) for all x

$$
\begin{align}
\frac{1}{g(y)}d y= f(x)dx \\
\int_{y(a)}^{y(x)} \frac{1}{g(y')} \, dy' = \int_{a}^{x} f(x') \, d' 
\end{align}$$
the $y'\text{ and } x'$ are dummy variables, they won't appear on the next line because it's a definite integral. the part we care about is the $y(x)$ from the integral that we solve for

We know when x = a, y(x)=b
We will get a function $y(x)=\text{ stuff }$

Examples:
$$
\begin{align} 
\text{ what is w in terms of u with initial condition w(0) = 1}\\
\frac{dw}{du} = wu^{2}+w \\
\frac{dw}{du}=w(u^{2}+1) \\
\frac{dw}{w}=(u^{2}+1)du \\
\int_{w(0)}^{w(u)} \frac{1}{w'}  \, dw' = \int_{o}^{u} (1+u'^2) \, du'   \\
\ln(w(u))-\ln(w(0))=\left( \frac{u^{3}}{3}+u \right)-\left( \frac{0^{3}}{3}+0 \right)  \\
u(0)=1, \ln(1)=0,\text{ we can simplify: }\\
w(u)=e^{ \frac{u^{3}}{3}+u } 
\end{align}
$$

We can apply this to physics. 
![[Pasted image 20240206102230.png]]
![[Pasted image 20240206102245.png]]

Imagine a rope with two unequal masses attached on either end. If you wrap the rope without knots around a relatively smooth surface, it can hold the two masses! There is a really impressive demonstration video of a guy in some snowy area where he is attached to a rope, the rope goes across a spherical gerder, and there is a weight on the other end of the rope. The weight is released, the guy falls far, but as the weight wraps around the gerder the man stops and is suspended.
$$
\begin{align}
\frac{dt}{d\theta} = \mu_{s}T(\theta) \text{ with  }T(0)=m_{1}g
\frac{1}{T}d T=\mu_{s}d\theta \\
\int_{T(0)}^{T(\theta)} \frac{1}{T'}  \, dT'=\int_{0}^{\theta} \mu_{s} \, d\theta' \\
\ln(T(\theta))-\ln(T(0))=\mu_{s}(\theta-0) \\
\ln\left( \frac{T(\theta)}{T(0)} \right) = e^{ \mu_{s}\theta } \\
T(\theta)=m_{1}ge^{ M_{s}\theta }  
\end{align}
$$

What is the tension in a massive rope with uniform mass with a mass hanging off of it that is stationary? ($\lambda=\frac{m_{r}}{l}$)
$A=0$
$Mg+m_{r}g=T_{top}$
$Mg=T_{bot}$
The point on the rope at the top has to carry the entire mass, the point at the bottom has to carry the least mass.

![[Pasted image 20240206103655.png]]
If we have a constant acceleration within each little cut section of the rope.
Slice at $x$ and slice at $x+dx$ (+x direction is down the rope).
The force net is $0$ as acceleration is zero,
$$\begin{align}
dm=\lambda dx \\
T(x+dx)-T(x)+(dm)g = 0 \\
T(x+dx)-T(x)=-(dm)g \\
T(x+dx)-T(x)=-g\lambda(x)dx \\
\frac{T(x+dx)-T(x)}{dx}=-g\lambda(x)\\ \\
\frac{dT}{dx}=-g\lambda(x)
\end{align}
$$
We know tension at the top and bottom of the rope, as $T(L)=Mg\text{ and } T(0)=\left( m_{r}+M \right)g$
We can now solve this system:

$\int_{T(L)}^{T(x)} dT'=\int_{L}^{x} -g\lambda(x') \, dx'$
we know that $\lambda(x)=\frac{m_{r}}{L}x$
$$
\begin{align}
T(x)-T(L)=-\frac{gm_{g}}{L}(x-L) \\
T(x)=T(L)-\frac{gm_{g}}{L}(x-L) \\
T(x)=Mg+m_{r}G\left( 1-\frac{x}{l} \right) \\

\end{align}
$$
**This only works if acceleration is the same at each point in the rope**. If we have a rope that is moving circularly, acceleration is not the same. 

See previous: [[Springs, Rods, and Ropes]]
