![[Pasted image 20250226115814.png]]

For an complex  function to be analytic, it must satisfy the Cauchy-Riemann condition. That is, if we take 
$f(z=x+iy)=u(x,y)+i\nu(x,y)$
$$
\begin{align}
\lim_{ dx,dy \to 0 } \frac{f(x+\delta x,y+\delta y)-f(x,y)}{i\delta y+\delta x}
\end{align}
$$
, the function must satisfy the Cauchy Riemann condition:
$$
\begin{align}
\frac{ \partial u }{ \partial x } = \frac{ \partial \nu }{ \partial y }   \\
\frac{ \partial \nu }{ \partial x }  = - \frac{ \partial u }{ \partial y } 
\end{align}
$$

## A) 
First, lets express our function in terms of $u\text{ and } \nu$:
$$
\begin{align}
e^{ikz}= e^{ik(x+iy)} = e^{ikx}e^{-ky} \\

\end{align}
$$
We can separate these into their real and imaginary components:
$$
\begin{align}
e^{ikx}=\cos(kx)+i\sin(kx) \\
\end{align}
$$
Which gives us
$$
\begin{align}
e^{ikz}=\underbrace{ e^{-ky}\cos(kx) }_{ u }+i\underbrace{ \sin(kx)e^{-ky} }_{ v }
\end{align}
$$
We can now check:
$$
\begin{align}
  \frac{ d u}{d x }  & \stackrel{?}{=}  \frac{ d \nu}{d y }  \\
  -ke^{-ky}\sin(kx)  & = -k\sin(kx)e^{-ky}
\end{align}
$$
We can also check the alternate condition:
$$
\begin{align}
\frac{ d \nu}{d x }  & \stackrel{?}{=}  -\frac{ d u}{d y }  \\
-ke^{-ky}\cos(kx) & =-k\cos(kx)e^{-ky}
\end{align}
$$
Therefore, both of the Cauchy Riemann conditions are fulfilled and the function is analytic.

## B
$$
\begin{align}
\frac{1}{z} = \frac{1}{x+iy}
\end{align}
$$
We can use difference of squares:
$$
\begin{align}
\frac{1}{x+iy} \frac{x-iy}{x-iy}  \\
= \frac{x-iy}{x^{2}+y^{2}} \\
\text{ which can be separated into } \\
\underbrace{ \frac{x}{x^{2}+y^{2}} }_{ u } - i \underbrace{ \frac{y}{x^{2}+y^{2}} }_{ \nu }
\end{align}
$$
We can now use the cauchy riemann test:

$$
\begin{align}
\frac{ d u}{d x } \stackrel{?}{=}   \frac{ d \nu}{d y }  \\
\frac{(x^{2}+y^{2})-2x^{2}}{(x^{2}+y^{2})^{2}}= -\frac{(x^{2}+y^{2})-2y^{2}}{(x^{2}+y^{2})^{2}} \\
2(x^{2}+y^{2})=2x^{2}+2y^{2}
\end{align}
$$
This is true.
We can check the other condition:
$$
\begin{align}
\frac{ d u}{d y } \stackrel{?}{=}  -\frac{ d \nu}{d x } \\
\frac{2xy}{(x^{2}+y^{2})^{2}}\stackrel{?}{=}  \frac{2xy}{(x^{2}+y^{2})^{2}} 
\end{align}
$$
This is also true, so the function is analytic. 

## C)
We can write out our function $\sqrt{ z }$ in polar as 
$$
\begin{align}
\sqrt{ re^{i\theta} }
\end{align}
$$
We have $r=\sqrt{ x^{2}+y^{2} }$ and $\theta = \tan ^{-1}\left( \frac{y}{x} \right)$


This gives us 
$$
\begin{align}
\sqrt{ z } = \sqrt{ \sqrt{ (x^{2}+y^{2}) }e^{i\tan ^{-1}(\frac{y}{x})} }
\end{align}
$$
We now have a way to represent this as a product of two functions and apply the Cauchy-Riemann conditions:
$$
\begin{align}

= \left( x^{2}+y^{2} \right) ^\frac{1}{4} (e^{i \frac{1}{2} \tan ^{-1}(\frac{y}{x})}) \\
= (x^{2}+y^{2})^{\frac{1}{4}} [i \sin \left( \frac{1}{2} \tan ^{-1}(\frac{y}{x}) \right) + \cos \left( \frac{1}{2} \tan ^{-1}(\frac{y}{x}) \right) ]
\end{align}
$$
We can now separate this into two functions, $u\text{ and } \nu$, and relabel terms:

$$
\begin{align}
i \sqrt{ x^{2}+y^{2} } \sin\left( \frac{1}{2}\tan ^{-1}\left( \frac{y}{x} \right) \right)+ \sqrt{ x^{2}+y^{2} }\cos\left( \frac{1}{2}\tan ^{-1}\left( \frac{y}{x} \right) \right)
\end{align}
$$
We can see that this is
$$
\begin{align}
\underbrace{ r^\frac{1}{2} \cos\left( \frac{1}{2}\theta \right) }_{ u }+ i\underbrace{ r^{\frac{1}{2}}\sin\left( \frac{1}{2}\theta \right) }_{ \nu }
\end{align}
$$

The conditions are
$$
\begin{align}
\frac{ d u}{d x } =\frac{ d \nu}{d y } \\
\frac{ d u}{d y } =-\frac{ d \nu}{d x }  \\ 
\end{align}
$$
To compute this, we will have to use the product rule and chain rule:
$$
\begin{align}
\frac{ d u}{d x }  & =r^{\frac{1}{2}} \frac{ d }{d x }\sin \frac{1}{2}\theta + \frac{1}{2r}\sin\left( \frac{1}{2}\theta \right)\frac{ d r}{d x }  \\
\frac{ d \nu}{d y }  & = r^{\frac{1}{2}} \frac{ d }{d y } \sin\left( \frac{1}{2}\theta \right) + \sin\left( \frac{1}{2}\theta \right) \frac{1}{2r}\frac{ dr}{d y } 
\end{align}
$$


This looks gross. We can simplify this by finding $\frac{ d u}{d r },\frac{ d u}{d \theta },\frac{ d \nu}{d r },\frac{ d \nu}{d \theta }$. Then we can use the chain rule to compute each combination.

$$
\begin{align}
\frac{ d u}{d r } = \frac{1}{2}r^{\frac{-1}{2}}\cos\left( \frac{1}{2}\theta \right) \\
\frac{ d u}{d \theta } = \frac{-1}{2}r^{\frac{1}{2}} \sin\left( \frac{1}{2}\theta \right)
\end{align}
$$
Similarly for $\nu:$
$$
\begin{align}
\frac{ d \nu}{d r } = \frac{1}{2}r^{\frac{-1}{2}}\sin\left( \frac{1}{2\theta} \right) \\
\frac{ d \nu}{d \theta } = \frac{1}{2}r^{\frac{1}{2}}\cos\left( \frac{1}{2}\theta \right)
\end{align}
$$
We can use the chain rule with either $r$ or $\theta$. To make this easier, I'll choose components with the same trig function. To do this, we have to find the derivatives of $r\text{ and } \theta$:

$$
\begin{align}
\frac{ dr }{d x }  = \frac{1}{2\sqrt{ x^{2}+y^{2} }}(2x)\\
\frac{ dr }{d y }  = \frac{1}{2\sqrt{ x^{2}+y^{2} }}(2y)
\end{align}
$$
and 
$$
\begin{align}
\frac{ d \theta}{d x } = \frac{1}{\left( 1+\frac{y^{2}}{x^{2}} \right)} \frac{-y}{x^{2}}   \\
\frac{ d \theta}{d y } = \frac{1}{\left( 1+\frac{y^{2}}{x^{2}} \right)} \frac{1}{x}  \\
\end{align}
$$
Now we can use the chain rule:
$$
\begin{align}
\frac{ d u}{d x } = \frac{ d u}{d r } \frac{ d r}{d x } \\
\frac{ d \nu}{d y } = \frac{ d \nu}{d \theta } \frac{ d \theta}{d y } 
\end{align}
$$
(these both have cosine components).


This gives us (ugh finally!):
$$
\begin{align}
\frac{ d u}{d x }  = \left( \frac{1}{2}r^{\frac{-1}{2}}\cos\left( \frac{1}{2}\theta \right)  \right) \left( \frac{1}{2\sqrt{ x^{2}+y^{2} }}(2x) \right)  \\
\frac{ d \nu}{d y } = \left( \frac{1}{2}r^{\frac{1}{2}}\cos\left( \frac{1}{2}\theta \right) \right) \left( \frac{1}{\left( 1+\frac{y^{2}}{x^{2}} \right)} \frac{1}{x}  \right) 
\end{align}
$$

We can see that most components cancel out, so we get
$$
\begin{align}
r^{\frac{-1}{2}} \frac{x}{r} \stackrel{?}{=}   r^{\frac{1}{2}} \frac{1}{x} \frac{1}{\left( 1+\left( \frac{y}{x} \right)^{2} \right)}
\end{align}
$$

$$
\begin{align}
r^{2}\stackrel{?}{=}   x^{2} \left(  1+ \left( \frac{y}{x} \right)^{2} \right) \\ 
r \stackrel{?}{=}   x \sqrt{ 1+\frac{y^{2}}{x^{2}} } \\
r =  \sqrt{ x^{2}+y^{2} }
\end{align}
$$
Therefore, $\sqrt{ z }$ is  analytic, since we've shown that $\frac{ d u}{d x }=\frac{ d \nu}{d y }$!



![[Pasted image 20250226115825.png]]

We can check the latter equality by evaluating the right side of the first equation:
$$
\begin{align}
\int_{0}^{1} \frac{dx}{1+x^{2}}=\int_{0}^{1} \frac{i}{2}\left[ \frac{1}{x+i}-\frac{1}{x-i} \right]  dx\\
= \frac{i}{2}\int_{0}^{1} \frac{1}{x+i} - \frac{1}{x-i} dx  \\
= \frac{i}{2} \int_{0}^{1} \frac{(x-i)-(x+i)}{x^{2}+1}dx \\
= \frac{i}{2} \int_{0}^{1} -\frac{2i}{x^{2}+1}dx \\
= \int_{0}^{1} \frac{1}{x^{2}+1} dx
\end{align}
$$

We see that this looks like $\sin\theta$, where we have a triangle with side lengths $x^{2},1,\text{ and } x^{2}+1$.

We can define $x=\tan\theta$, $dx=\sec ^{2}\theta d\theta$, $\theta=\arctan x$
We now have
$$
\begin{align}
\int \frac{\sec\theta^{2}}{1+\tan\theta ^{2}} d\theta \\
= \int 1d\theta \\
= \theta \\
= \arctan(x)\bigg|_{0}^{1} \\
=   
\end{align}
$$
$$
\begin{align}
= \frac{\pi}{4} - 0
\end{align}
$$
So we have found that 
$$
\begin{align}
\int_{0}^{1} \frac{1}{1+x^{2}}dx = \frac{\pi}{4}
\end{align}
$$

![[Pasted image 20250226115902.png|500]]
Using the approach above, we can show that $S=\frac{\pi}{4}$. 
$S=f(1)$. $f(0)=0$, since we know what the series is.  
Therefore, we have $\int_{0}^{1}f'(x)=S$

We can write the geometric sum for $f'(x)$ as
$$
\begin{align}
\sum_{n=0}^{\infty} (-1)^{n}(x)^{2n} \\
= \sum_{n=0}^{\infty} (-x^{2})^{n}
\end{align}
$$

This is a geometric series with $r=-x^{2},a=1$. Therefore, this becomes
$f'(x) = \frac{1}{1-(-x^{2})}=\frac{1}{1+x^{2}}$. 

We showed in problem 2 that 
$\frac{\int_{0}^{1}1}{1+x^{2}}dx =  \frac{\pi}{4}$ 

We can continue to simplify the original expression:

We have the original series (expanded) as
$$
\begin{align}
i - \frac{1}{2} -\frac{i}{3}+\frac{1}{4} +\frac{i}{5} - \frac{1}{6} - \frac{i}{7} + \frac{1}{8}+\dots
\end{align}
$$

We can simplify this by separating the function into parts. We know that the series $1-\frac{1}{3}+\frac{1}{5}-\dots$ converges to $\frac{\pi}{4}$, so we can pull out these terms and find the rest of the series
We get 
$$
\begin{align}
i \frac{\pi}{4} -\frac{1}{2}+\frac{1}{4}-\frac{1}{6}+\frac{1}{8}-\frac{1}{10}
\end{align}
$$
This later half sum looks like the McLaurin series for ln(1-x), which can be written as
$$
\begin{align}
(x-1)-\frac{(x-1)^{2}}{2}+\frac{(x-1)^{3}}{3}-\frac{(x-1)^{4}}{4}\dots
\end{align}
$$
However, our function looks to be the negated half half of this, getting
$$
\begin{align}
-\frac{x-1}{2} + \frac{(x-1)^{2}}{4} - \dots
\end{align}
$$

Here, we note that for our series we have $x=2$ to get 1 in the numerator. We get
$$
\begin{align}
\frac{i\pi}{4}-\frac{1}{2}\ln(2)
\end{align}
$$
Therefore, we have shown that the equality holds!



![[Pasted image 20250226115911.png]]
By the Cauchy residual theorem, we can equate the value of this integral to the sum $2\pi i$ times of the upper function's values at the poles (residuals).

The poles are solutions to $x^{6}=-1=e^{i\pi}=e^{i\pi}e^{2n\pi i}$
$x=e^\frac{i\pi}{6}+e^{2n\pi \frac{i}{6}}$
We can integrate this as a closed path by moving along the real axis from $-\infty \text{ to } \infty$, and then finish with a large (up to infinite) arc. 
$$
\begin{align}
z=Re^{i\phi}, dz=Rie^{i\phi}d\phi \\
\int_{\text{ arc }}^{} \frac{Rie^{i\phi}d\phi}{R^{4}e^{ri\phi}+1} = \frac{1}{R^{3}}\int_{\text{ arc }} \frac{e^{i\phi}d\phi}{e^{4i\phi}+R^{-4}}
\end{align}
$$

We can see that as $R\to \infty$, this arc will have on contribution to our integral along a closed path
We therefore have the closed integral as just the value along the real axis. The closed path integral along an analytic function is zero, so the integral will equal $2\pi i \sum_{}^{}\text{ residues enclosed }$. For our semicircle, we'll include the discontinuities that are above the $x$ axis, so we will have to find the residues at $e^{\frac{i\pi}{6}},e^{\frac{3i\pi}{6}},e^{5\pi \frac{i}{6}}$ 

We have the Laurent expansion to find the residues.
$$
\begin{align}
\lim_{ z\to  z_{0} } \left[ (z-z_{0}) f(z) \right]   \\
\lim_{ z \to e^{\frac{i\pi}{6}} }  \frac{(z-e^{\frac{i\pi}{6}})}{z^{6}+1}
\end{align}
$$
This will go to $\frac{0}{0}$, so we can use L'hopital's rule. This becomes
$$
\begin{align}
\frac{1}{6z^{5}}= \frac{1}{6}(e^{-i\pi \frac{5}{6}})
\end{align}
$$
Our other residues are thus
$$
\begin{align}
\frac{1}{6}e^{-(i\pi \frac{15}{6})}\text{ and }  \frac{1}{6}e^{-(i\pi \frac{25}{6})}
\end{align}
$$
We get the sum of the residuals to be
$$
\begin{align}
\frac{1}{6} \left( e^{-i\pi \frac{5}{6}}+e^{-i\pi \frac{15}{6}}+e^{-i\pi \frac{25}{6}} \right)  \\
\frac{1}{6} \left( e^{-i\pi \frac{5}{6}}+e^{-i\pi \frac{1}{2}}+e^{-i\pi \frac{1}{6}} \right)  \\
\end{align}
$$

The value is thus 
$$
\begin{align}
\frac{1}{3}\pi i\left( e^{-i\pi \frac{5}{6}}+e^{-i\pi \frac{1}{2}}+ e^{-i\pi \frac{1}{6}} \right) \\
=\frac{1}{3}\pi e^{\frac{i\pi}{2}}\left( e^{-i\pi \frac{5}{6}}+e^{-i\pi \frac{1}{2}}+ e^{-i\pi \frac{1}{6}} \right) \\
= \frac{1}{3}\pi \left( e^{i\pi\left( \frac{3}{6} - \frac{5}{6} \right)}+e^{i\pi \left( \frac{1}{2}- \frac{1}{2} \right)}+e^{i\pi\left( \frac{3}{6}- \frac{1}{6} \right)} \right) \\
= \frac{1}{3} \pi\left( e^{\frac{-1}{3}i\pi}+1+e^{i\pi \frac{1}{3}} \right)  \\
\end{align}
$$


We have the following:
$$
\begin{align}
\sin\left( \frac{1}{3}\pi \right)= \frac{\sqrt{ 3 }}{2}\\
\sin\left( \frac{-1}{3}\pi \right)= -\frac{\sqrt{ 3 }}{2}\\
\cos\left( \frac{-1}{3}\pi \right)= \cos\left( \frac{1}{3}\pi \right)= \frac{1}{2}
\end{align}
$$

The sin components will cancel and the cosine will sum, so we get
$$
\boxed{
\begin{align}
=\frac{2\pi}{3} 
\end{align}
}
$$

```
import pandas
import numpy as np
from matplotlib import pyplot as plt
import scipy as scp

def f(x):
    return 1/(1+x**6)
  

i_allatonce = scp.integrate.quad(f,-np.inf,np.inf)[0]
bounds = (0,2,4,10,20,50,100,200,500,700,1000,1500,2000,3000,5000,8000,np.inf)
res = 2*np.array([scp.integrate.quad(f,bounds[i],bounds[i+1])[0] for i in range(len(bounds)-1)])

print(i_allatonce)
print(res.sum())
print(i_allatonce-res.sum())
```
returns:
2.0943951023931953 
2.094395102393195
4.440892098500626e-16


This agrees!


