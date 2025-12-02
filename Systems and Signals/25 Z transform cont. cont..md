Online lecture.


>[!abstract]+ Questions

##### Why is Z a circle instead of a half plane?

Remember the definition of the z transform. The magnitude of the thing has a restriction, which keeps it in a radius.

For the Laplace transform, the real part has the restriction - not the magnitude. This is why the convergence areas are planes instead of circular radii.

##### What does $z^{-1}$ mean in the real world?
We saw last time that different powers of z correspond to time domain signals (see the polynomial expansion). The coefficient for $z^{-1}$ is the value for one time step in the future (a unit delay).

##### Region of Convergence
Multiplying a signal by something unstable that blows up would make the region of convergence shrink, or the opposite - if you multiply by a stable thing, the region of convergence would expand. 

In the real world, we're dealing with right sided systems usually. However, convergence tells you the stability of a system. A lot of systems have feedback, which changes stability. Convergence and regions of stability are very useful. 


## Interpreting the Z transform

Similar to the Laplace transform, we can write a rational polynomial:
$$
\begin{align}
X(z)  & = \frac{a_{0} z^{-m}+ a_{1} z^{-(m-1) + \dots + a_{m} }}{b_{0} z^{-n} + b_{1} z^{-(n-1)}+ \dots + b_{n}}  \\ 
 & = k \frac{\overbrace{ \Pi^{m}_{i=1} (1-c_{i}z^{-1}) }^{\text{ zeros  } c_{i}}}{\underbrace{ \Pi^{n}_{k=1} (1-p_{k}z^{-1}) }_{ \text{ poles  }p_k }} \\
 
\end{align}
$$

We can't have convergence anywhere that includes a pole, so we can make similar figures as from the Laplace transform.


For example:
$$
\begin{align}
X(z) = \frac{1+z^{-2}}{\left( 1- \frac{1}{2}z^{-1} \right)(1+z^{-1})(1-2z^{-1})}
\end{align}
$$
There are three poles here:
$\frac{1}{2}, -1, 2$. There are zeros at $\pm j$.

We know that the expansion will be something of the form
$$
\begin{align}
\frac{A}{1-\frac{1}{2}z^{-1}} + \frac{B}{1-z^{-1}} + \frac{C}{1-2z^{-1}} 
\end{align}
$$

If we sum all three terms, we could have a right sided signal with the region of convergence outside the circle (all things at radius beyond the furthest pole, here at 2).
![[Pasted image 20251129122750.png]]

If we use the innermost radius, we get a left sided signal
![[Pasted image 20251129122811.png]]
Or in between radius 1 and 2 (two sided)
![[Pasted image 20251129122943.png]]

Where the $A$ and $B$ term are right sided and the $C$ term is left sided.

The last option is between the innermost circle and the circle in the middle, which is also two sided. This has the $A$ as right sided, and the $B$ and $C$ terms as left sided.


## Z transform and the DTFT
By inspection we see a strong similarity between the $\mathbb{Z}$ transform and the DTFT.
$$
\begin{align}
X(z)  & = \sum_{n=-\infty}^{\infty} x[n]z^{-n} \\
X(e^{j\omega})  & = \sum_{n=-\infty}^{\infty} x[n]e^{-j\omega n}
\end{align}
$$
The $DTFT$ is the z transform evaluated at $z=e^{j\omega}$, so the DTFT is a special case of the $\mathbb{Z}$ transform, or the $\mathbb{Z}$ as a generalization of the DTFT. 

Graphically, we can evaluate the DTFT from the pole zero plot. 
$$
\begin{align}
\text{ For rational  }  \\
 X(z) 
 & =k \frac{\Pi_{i=1} ^{m}(z-c_{i})}{\Pi_{k=1} ^{n}(z-p_{k})}, \\
\left| X(e^{j\omega}) \right| = \left| k \right| \frac{\Pi_{i=1} ^{m}\left| e^{j\omega}-c_{i} \right| }{\Pi_{k=1} ^{n}\left| e^{j\omega}-[_{k}] \right| }
\end{align}
$$

Graphically, lets think about each term. In the top, this is the distance from a point on the unit circle to the point $c_{i}$. Similarly, the denominator is the distance to each of the poles. 

$$
\begin{align}
\measuredangle  X(e^{j\omega}) = \measuredangle  k + \sum_{i=1}^{m} \measuredangle  (e^{j\omega}-c_{i})- \sum_{k=1}^{n} \measuredangle  (e^{j\omega}-p_{k})
\end{align}
$$
This tells us graphically why the magnitude and phase response is how it is. 


### Example: $H(z)= \frac{1}{1-az^{-1}}, \left| z \right|> \left| a \right|$

$$
\begin{align}
H(z) = \frac{z}{z-a} \\
H(e^{j\omega}) = \frac{e^{j\omega}}{e^{j\omega}-a}
\end{align}
$$
The magnitude of the numerator is always $1$, so we're just spinning around the complex plane in a circle. In the denominator, as we spin we are getting further and closer to $a$, we we have a cyclic magnitude that looks generally like a sin wave but with its own min and max. 

![[Pasted image 20251129124403.png]]
As we change the argument $a$, we change how stark the difference is proportionally throughout the traversal of the circle. 
We can also graphically see the phase (we are comparing the angle between the $x$ axis, the origin, and the point minus the angle from the x axis, the pole $a$, and the point). If the pole $a$ is close to $1$, then it will hit 90 degrees very quickly and make a strongly negative phase, and then slowly got to 180.
![[Pasted image 20251129124922.png]]



### Example: $H(z) = \frac{z^{2}}{(z+0.9j)(z-0.9j)}, \left| z \right| > 0.9$ 

We can get the rough shape for the magnitude here. The distance between the zeros is $1$, and the distance to the poles is close to $\sqrt[]{ 2 }$, and we have two so $\sim\sqrt[]{ 2 }\sqrt[]{ 2 }\approx2$, so $\frac{1}{2}$.
![[Pasted image 20251129125400.png]]

The poles are symmetric about zero, so the phase at $0$ is $0$. at $\frac{\pi}{2}$ its $0$, and the same at $\pi$ - the angles between each of the poles cancel out. The phase is symmetric, and will be very sharp:
![[Pasted image 20251129125533.png]]

## Z transform and LTI systems
A convolution in $n$ (time domain) is a product in the $\mathbb{Z}$.

![[Pasted image 20251129125652.png]]
If $H(z)$ is causal, the region of convergence is the exterior of a circle, including infinity. 

### Causality
If $H(z)$ is rational, then this is equivalent to saying that the ROC is outside the outermost pole, and the order of the numerator is $\leq$ the order of the denominator.
For example, 
$$
\begin{align}
H(z) = \frac{z}{z^{2}-1} \text{ has } \infty \in ROC \\
\text{ but } \\
H(z) = \frac{z^{3}}{z^{2}-1} \text{ has } \infty \cancelto{  }{ \in  }ROC
\end{align}
$$
### Stability
$H(z)$ is stable $\Leftrightarrow$ ROC includes the unit circle. 


If it is causal, rational $H_{z}$ is stable $\Leftrightarrow$ all poles are inside the unit circle.

#### Example: $H(z) = \frac{z-1}{(z-2)\left( z+\frac{2}{3} \right)\left( z-\frac{1}{3} \right)}$
We have three poles, at $2,-\frac{2}{3},\frac{1}{3}$.
If we have everywhere outside of the outermost, this is causal but unstable.  

If we have between $\frac{2}{3}$ and $2$, it is noncausal but stable. If we have between the innermost - $\frac{1}{3} \text{ and } \frac{2}{3}$ then it is noncausal AND unstable (yikes).
![[Pasted image 20251129130411.png]]


## When to $\mathbb{Z}$ transform?
Whenever we are dealing with frequencies, we want to use Fourier. The Z transform is useful when you want to find the step response, stability, or Linear Constant Coefficient Difference Equations.

Lets calculate the step response from a given system response. 
![[Pasted image 20251129130716.png|500]]
![[Pasted image 20251129130725.png|500]]
![[Pasted image 20251129130740.png|500]]



