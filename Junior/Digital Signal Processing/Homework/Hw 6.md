![[Pasted image 20260227155349.png]]

$$
\begin{align}
F_{X}(x)  & = \int_{-\infty}^{x} \lambda e^{-\lambda x'}dx' \\
 & = \int_{0}^{x} \lambda e^{-\lambda x'}dx' \\
 & = -e^{-\lambda x'}\bigg|_{0}^{x} \\
 & = 1-e^{-\lambda x}
\end{align}
$$

![[Pasted image 20260227155357.png]]

![[Pasted image 20260227160129.png|300]]

![[Pasted image 20260227155405.png]]
$$
\begin{align}
\frac{d}{dx}  UV  = U V' + VU' \\
\end{align}
$$

Assuming that I'm finding 
$$
\begin{align}
E(\lambda e^{-\lambda x}) & \\
 & =\int_{0}^{\infty} x\lambda e^{-\lambda x}dx \\
 & =  \left(- x e^{-\lambda x} - \frac{1}{\lambda}e^{-\lambda x} \right)\bigg|_{0}^{\infty}    \\
 & =  \frac{1}{\lambda}
\end{align}
$$

![[Pasted image 20260227155413.png]]
Var($X$) = $E[x^{2}]-E[X]^{2}$

$$
\begin{align}
 E[x^{2}]&= \int_{0}^{\infty} x^{2} \lambda e^{-\lambda x}dx \\
 & = -x^{2}e^{-\lambda x} - \frac{2x}{\lambda}e^{-\lambda x}  - \frac{2}{\lambda^{2}}e^{-\lambda x} \bigg|_{0}^{\infty}  \\
 & = \frac{2}{\lambda^{2}} 
\end{align}
$$
So we have
$\text{ Var }[x]= \frac{1}{\lambda^{2}}$


![[Pasted image 20260227155420.png]]

$$
\begin{align}
\rho_{xy} = \frac{\sigma_{xy}}{\sigma_{x}\sigma_{y}} 
\end{align}
$$
$\sigma_{xy}= E[(x-E[x])(Y-E[Y])]$
$\sigma_{x}^{2}= E[x^{2}]-E[x]^{2}$

## $\sigma_{z}$
Because $X_{1}$ and $X_{2}$ are independent,
$$
\begin{align}
\text{ Var }[Z]  & = \text{ Var }[X_{1}+2X_{2}] \\
 & = \text{ Var }[X_{1}]+ \text{ Var }[2X_{2}] \\
 & = \frac{1}{\lambda^{2}} + \frac{4}{\lambda^{2}} \\
 & = \frac{5}{\lambda^{2}}
\end{align}
$$
$Var[x]$ is nonlinear, so constant terms inside the argument pull out as squares.

This gives us that
$\boxed{\sigma_{z}= \frac{\sqrt[]{ 5 }}{\lambda}}$

## $\sigma_{y}$
$$
\begin{align}
\text{ Var }[Y]  & = \text{ Var }[X_{1}]+ \text{ Var }[X_{2}] \\
 & = \frac{2}{\lambda^{2}}
\end{align}
$$

## $\sigma_{yz}$ 
$$
\begin{align}
\sigma_{zy} & = E[(Z-E[Z])(Y-E[Y])]\\
\sigma_{zy}  & = E[ZY]-E[Z]E[Y]   \\
\end{align}
$$

Also, 
$$
\begin{align}
E[g(X)] = \int_{-\infty}^{\infty} g(x)f_{x}(x) dx
\end{align}
$$
where 
$$
\begin{align}
g(x) & =ZY \\
 & = (X_{1}-X_{2})(X_{1}+2X_{2}) \\
 & =X_{1}^{2}+2X_{2}X_{1}-X_{2}X_{1}-2X_{2}^{2} \\
 & = X_{1}^{2} + X_{1}X_{2} - 2X_{2}^{2}
\end{align}
$$

We can now find
$$
\begin{align}
E[ZY]  & = E[X_{1}^{2}]+ E[X_{1}]E[X_{2}] - 2 E[X_{2}^{2}] \\
 & = \frac{2}{\lambda^{2}} + \frac{1}{\lambda^{2}} - 2\frac{2}{\lambda^{2}} \\
 & = - \frac{1}{\lambda^{2}}
\end{align}
$$
Now we need
$$
\begin{align}
E[Z]E[Y]
\end{align}
$$
$$
\begin{align}
E[Y]  & = E[X_{1}-X_{2}] \\
 & =0
\end{align}
$$
So this is just zero. 

$\sigma_{yz}=-\frac{1}{\lambda^{2}}$

## $\rho_{yz}$

$$
\begin{align}
\rho_{yz} = \frac{\sigma_{yz}}{\sigma_{z}\sigma_{y}} 
\end{align}
$$
$$
\begin{align}
 & \frac{\left( -\frac{1}{\lambda^{2}} \right)}{\frac{2}{\lambda^{2}} \frac{\sqrt[]{ 5 }}{\lambda} } \\
 & =\frac{-1}{\lambda^{2}} \frac{\lambda^{3}}{2\sqrt[]{ 5 } } \\
 & = -\frac{\lambda}{2\sqrt[]{ 5 } }
\end{align}
$$


![[Pasted image 20260227155430.png]]
If we label heads as $+1$ and tails as $-1$, then can use the step as it is
$$
\begin{align}
f_{Z}(z) = 0.5\left(  \frac{1}{b-a}(u[x-a]-u[x-b])+ \lambda e^{-\lambda x} \right) 
\end{align}
$$


![[Pasted image 20260227155438.png]]

$$
\begin{align}
F_{Z}(z) = \int_{-\infty}^{\infty} f_{Z}(z)  
\end{align}
$$
We have three regions - before the uniform distribution, during it up to the end, and after it. I'll use X because I accidentally did all the work with x, and I'm too lazy to change it.

$$
\begin{align}
= \begin{cases}
0.5(\int_{0}^{x}  \lambda e^{-\lambda x} dx+ 0) & x<a) \\
0.5(\int_{0}^{a}  \lambda e^{-\lambda x} dx+ \int_{a}^{x} \frac{1}{b-a} + \lambda e^{-\lambda x}) dx & a<x<b) \\
0.5\left( \int_{0}^{a}  \lambda e^{-\lambda x}dx + \int_{a}^{b} \frac{1}{b-a} + \lambda e^{-\lambda x}dx + \int_{b}^{x} \lambda e^{-\lambda x}dx \right)  & b<x
\end{cases}
\end{align}
$$


## case 1
$$
\begin{align}
 & \int_{0}^{x} 0.5 \lambda e^{-\lambda x'}dx' \\
 & = -0.5 e^{-\lambda x'}\bigg|_{0}^{x}    \\
 & = 0.5 (1-e^{-\lambda x})
\end{align}
$$

## Case 2
$$
\begin{align}
 & 0.5\left(1- e^{-\lambda a} + \int_{a}^{x} \frac{1}{b-a} + \lambda e^{-\lambda x'}dx' \right) \\
 & =0.5\left( 1-e^{-\lambda a} + \frac{1}{b-a}x' \bigg|_{a}^{x} - e^{-\lambda x'} \bigg|_{a}^{x}   \right)\\
 & = 0.5\left(1- e^{-\lambda a} + \frac{x-a}{b-a} - e^{-\lambda x}+e^{-\lambda a} \right) \\
 & = 0.5 \left( 1+\frac{x-a}{b-a} - e^{-\lambda x} \right)
\end{align}
$$



## Case 3
$$
\begin{align}
 & = 0.5 \left(\underbrace{ 1 }_{ \text{ uniform } }+1-e^{-\lambda x} \right) \\
 & =0.5(2-e^{-\lambda x})
\end{align}
$$


This gives us
$$
\begin{align}
F_{Z}(z) = \begin{cases}
0.5 (1-e^{-\lambda z} ) & z<a \\
0.5\left( 1+\frac{z-a}{b-a}-e^{-\lambda z} \right) & a<z<b \\
0.5(2-e^{-\lambda z}) & b<z
\end{cases}  
\end{align}
$$


![[Pasted image 20260227155443.png]]

$$
\begin{align}
E[z]=\int_{-\infty}^{\infty} z f_{z} (z)dz
\end{align}
$$
$$
\begin{align}
f_{Z}(z) = 0.5\left(  \frac{1}{b-a}(u[x-a]-u[x-b])+ \lambda e^{-\lambda x} \right) 
\end{align}
$$
We can just separate this out - the uniform distribution just goes to its average value, and we found for the exponential
$$
\begin{align}
 & 0.5*\int_{a}^{b} \frac{1}{b-a}x dx + 0.5 * \int_{0}^{\infty}x \lambda e^{-\lambda x}dx \\
 & = \frac{1}{2}\left(\frac{a+b}{2} + \frac{1}{\lambda}\right)
\end{align}
$$

![[Pasted image 20260227155448.png]]

$$
\begin{align}
 \text{ Var }[z]&= 0.5*\int_{a}^{b} \frac{1}{b-a}x^{2} dx + 0.5 * \int_{0}^{\infty}x^{2} \lambda e^{-\lambda x}dx  \\
 & = \frac{1}{2}\left( \frac{b^{3}-a^{3}}{3(b-a)} + \frac{1}{\lambda^{2}} \right) \\
 & = \frac{1}{2}\left( \frac{a^{2}+ab+b^{2}}{3} + \frac{1}{\lambda^{2}} \right)
\end{align}
$$

(I looked up the $b^{3}-a^{3}$ expansion)


![[Pasted image 20260227155455.png]]

$$
\begin{align}
\sigma_{z_{1}z_{2}}  & = E[z_{1}z_{2}]-E[z_{1}]E[z_{2}]   \\
\end{align}
$$
Because we are dealing with the raw draws and not complicated functions built off of the draws, there is no correlation - 
$$
\begin{align}
E[z_{1}z_{2}]=E[z_{1}]E[z_{2}]
\end{align}
$$
so $\sigma_{z_{1}z_{2}}=0$
Therefore, $\rho_{z_{1},z_{2}}=0$


![[Pasted image 20260227155505.png]]

The chance of all draws is
$$
\begin{align}
\Pi_{i=1}^{n} \lambda e^{-\lambda x_{i} }  \\
\lambda^{n}\, \, \, \Pi_{i=1}^{n}\,  e^{-\lambda x_{i} }
\end{align}
$$
We can find $\lambda$ by minimizing the product

$$
\begin{align}
\frac{ d }{d \lambda } \lambda^{n} \Pi_{i=1}^{n} e^{-\lambda x_{i} }= 0
\end{align}
$$
We can simplify with the natural log, since multiplication of things with exponents is addition of the exponents, and ln pulls apart multiplication as addition, so this becomes
$$
\begin{align}
\frac{ d }{d \lambda } \ln (\lambda^{n})_{}  +\sum_{i=1} ^{n}-\lambda x_{i}  & =0  \\
\frac{ d }{d \lambda } \ln (\lambda^{n})-\lambda \sum_{i=1}^{n} x_{i}  & =0 \\
\frac{n}{\lambda}-\sum_{i=1}^{\infty} x_{i}  & =0 \\
\lambda & = \frac{n}{\sum_{i=1}^{n} x _{i}}
\end{align}
$$



![[Pasted image 20260227155512.png]]
$$
\begin{align}
f_{X}(x,\mu,\sigma^{2}) = \frac{1}{\sqrt[]{ 2\pi\sigma^{2} } } e^{- \frac{1}{2 \sigma^{2}}(x-\mu)^{2}} 
\end{align}
$$
We can do the same process as before. Lets start with the means
$$
\begin{align}
\frac{1}{\sqrt[]{ 2\pi\sigma^{2} } } \prod_{i=1}^{n} e^{- \frac{1}{2\sigma^{2}}(x_{i} -\mu )^{2}}
\end{align}
$$
We want to minimize this. Constants don't matter, we care about what minimizes
$$
\begin{align}
\prod_{i=1}^{n} e^{-(x_{i} -\mu)^{2}}
\end{align}
$$
So
$$
\begin{align}
 & \frac{ d }{d \mu } \prod_{i=1}^{n} e^{-(x_{i} -\mu)^{2}} & =0 \\
 & \frac{ d }{d \mu} \sum_{i=1}^{n} (x_{i} -\mu)^{2}  & = 0 \\
 & \frac{ d }{d \mu } \sum_{i=1}^{n}  & x_{i}^{2}+\mu^{2}-2x_{i}\mu  & = 0 \\
 & \sum_{i=1}^{n} 2\mu - 2x_{i} =0 \\
 & \sum_{i=1 }^{n} x_{i} = n\mu \\
\end{align}
$$

$$
\boxed{
\begin{align}
\mu = \frac{\sum_{i=1}^{n} x_{i} }{n} 
\end{align}
}
$$

This makes sense as the definition of the mean.

Lets do it for the standard deviation now:

$$
\begin{align}
\frac{1}{\sqrt[]{ 2\pi\sigma^{2} } } \prod_{i=1}^{n} e^{- \frac{1}{2\sigma^{2}}(x_{i} -\mu )^{2}}
\end{align}
$$

We can't chuck out the constants, but we still have some manipulation with the ln
$$
\begin{align}
\frac{d}{d \sigma} \left( - n\ln \sqrt[]{ 2\pi \sigma^{2} }  + \sum_{i=1}^{n} -\frac{1}{2 \sigma^{2}}(x_{i}-\mu )^{2} \right)  & = 0 \\
\frac{ d }{d \sigma } n\ln \sigma - \cancelto{ 0 }{ \ln \sqrt[]{ 2\pi }  }  - \frac{1}{\sigma^{3}}\sum_{i=1}^{n} (x_{i} -\mu)^{2}  & = 0 \\
\frac{n}{\sigma} - \frac{1}{\sigma^{3}} \sum_{i=1}^{n} (x_{i} -\mu)^{2}  & = 0 \\
\sigma^{2} = \frac{\sum_{i=1}^{n} (x_{i} -\mu)^{2}}{n}
\end{align}
$$
This is the definition of the variance, which also makes sense.

![[Pasted image 20260227155522.png]]

![[Pasted image 20260228154920.png]]


![[Pasted image 20260227155530.png]]
This looks to be the fewest deviations away from the F chord, so most likely from that.
![[Pasted image 20260228155047.png]]


![[Pasted image 20260227155538.png]]
The probabilities in order of C, F, G are

0.234, 0.195, 0.0314. The model for C maximizes the probability, even though F is closer to the center. 

![[Pasted image 20260227155549.png]]
![[Pasted image 20260301174959.png|300]]

![[Pasted image 20260227155557.png]]

![[Pasted image 20260301180206.png|300]]


Given that the previous was a c, 
C 0.4 F 0.3 G 0.3

This feels like the MAP values are the distance from the means to each peak of the amount of overlap if I integrate $C*G$ vs $C*F$.


![[Pasted image 20260227155630.png]]
4
