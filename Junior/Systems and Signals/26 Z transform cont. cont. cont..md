>[!abstract]+  Questions:
>Anticausal = the opposite direction of causal. A system that is on for times before zero, and turns off.
>Systems are stable if the region of convergence covers the unit circle



### Example $H(z) = \frac{1}{1-az^{-1}}$


![[Pasted image 20251202095250.png]]
We can find the magnitude and phase response graphically.

For magnitude, the numerator is $e^{j\omega}$ (was just $z$), so that magnitude $\frac{1}{\text{ distance from }e^{j\omega}\text{  to a }}$

When close to a pole or a zero, we expect to see a very dramatic phase or magnitude response. (note it can't explode to infinity - remember that we have the restrictions for region of convergence. It'll just get big).

If the point $a$ is very close to the unit circle, there will be a tiny sliver of the circle that changes from $0$ to $\pi$ and beyond super quickly, and the rest is really small. 


### Example
Lets put zeros on our circle and poles right next to them.
![[Pasted image 20251202095832.png]]

When we are far to the side of the circle, the distances to the poles and zeros is about the same, so the magnitude is going to be close to $\frac{1}{1}$. 

This is a band stop filter - at $\omega_{0}$ (the angle of the poles and zeros), we will have $0$ magnitude - but elsewhere basically $1$.
(note that the poles are inside the unit circle because we want the system to be stable and causal, so the region of convergence needs to include the unit circle and extend outwards).

## Using the $\mathbb{Z}$ transform

For a system to be stable, it must contain the unit circle.

The Z transform is really good at linear constant coefficient  difference (not differential, so this is discrete) equations.


### Example: Find $H(e^{j\omega})$ for a system described by $y[n]- \frac{1}{2}y[n-1] = x[n]$

$$
\begin{align}
Z\left\{ y[n] - \frac{1}{2}y[n-1] \right\} - z \left\{ x[n] \right\}  \\
Y(z) - \frac{1}{2}z^{-1}Y(z) = X(z) \\
H(z) = \frac{Y(z)}{X(z)} = \frac{1}{1-\frac{1}{2}z^{-1}}
\end{align}
$$
Note that this doesn't tell you the region of convergence. That is determined by other information about our system - if it is causal or stable.


### Counter Example: Find $h[n]$ for stable system described by $y[n]-2y[n-1]=x[n]$

$$
\begin{align}
Y(z) - 2z^{-1}Y(z) = X(z) \\
H(z) = \frac{Y(z)}{X(z)} = \frac{1}{1-2z^{-1}}
\end{align}
$$

Using our table of transforms, we have two possible entries:
$$
\begin{align}
a^{n}u[n] &  \leftrightarrow  \frac{1}{1-az^{-1}}, \left| z \right| > \left| a \right|  \\
-a^{n}u[-n-1]  & \leftrightarrow   \frac{1}{1-az^{-1}}, \left| z \right| < \left| a \right| 
\end{align}
$$

What should the region of convergence be?

Because this is a stable system, the ROC has to include the unit circle. The ROC is $\left| z \right|<2$ to contain it, so we get
$$
\begin{align}
h[n] = -2^{n}u[-n-1]
\end{align}
$$

### Aside: Unilateral Z transform
$$
\begin{align}
\mathscr{X} (z) &  = \sum_{n=0}^{\infty} x[n]z^{-n} \\
x[n] &  \leftrightarrow   \mathscr{X} (z)
\end{align}
$$
The unilateral and bilateral $\mathbb{Z}$ transforms are identical if $x[n]=0,n<0$.
This is useful for Linear constant coefficient difference equations with initial conditions. Because everything is right sided, you don't have to worry about the region of convergence - it's always just outside a unit circle. 


### Example: Causal LTI system described by $y[n]-\frac{1}{2}y[n-1]=x[n]$ with initial condition $y[-1]=-2$

![[Pasted image 20251202101737.png]]
This is a causal system, so we have outside of $\frac{1}{2}$ and outside of $1$ - the intersection of those two is $\left| z \right| > 1$.

This tells us that
$$
\begin{align}
y[n] = 2u[n]- 2 \left( \frac{1}{2} \right)^{n}u[n]
\end{align}
$$


## Summary of $\mathbb{Z}$ transform

What is the $\mathbb{Z}$ transform?
$X(z)= \sum_{n=-\infty}^{\infty}x[n]z^{-n}$

Taking the $\mathbb{Z}$ transform and inverse 
using the tables and properties, + partial fraction expansion (and binomial coefficients).

Interpreting $\mathbb{Z}$ transform
Region of convergence outside or inside a circle

When to $\mathbb{Z}$ transform?
$X(z)\to H(z)\to Y(z)=X(z)H(z)$

Finding the step response, stability, and linear constant coefficient difference equations. 

