We have looked at the case of a free particle where there is zero potential energy everywhere. We wrote down the individual eigenstates with different $k$ (the wavenumber), which are states of exact momentum. To get a normalized function we had to take a sum over the range of k values with some function $A(k)$ which would tell us how much of each eigenstate to include.
$$
\begin{align}
\psi_{k}(x) = e^{\pm ikx} \\
\Psi(x,0) = \int_{-\infty}^{\infty} A(k)e^{ikx}dx
\end{align}
$$

Today we will consider a simple potential function for quantum scattering.

Take the potential function
$$
\begin{align}
V(x)=\begin{cases}
0 & x < 0 \\
v_{0}  &  x>0
\end{cases}
\end{align}
$$
Lets assume that a particle has energy greater than that potential function, and is traveling in the $+x$ direction. Classically, we would expect that the particle would pass over and slow down, but quantum mechanics predicts that there is also a chance of reflecting off the energy barrier.

We will focus today on a single momentum eigenstate.

$$
\begin{align}
\psi(x) = \begin{cases}
Ae^{ikx}+Be^{-ikx}, &  x<0 \\
Ce^{ik_{0}x}, & x>0
\end{cases}
\end{align}
$$
## Step potential
![[Pasted image 20250217101000.png|300]]

We know will have, 
$k=\frac{\sqrt{ 2mE }}{\hbar},x<0$
$k_{0}=\frac{\sqrt{ 2m(E-v_{0}) }}{\hbar},x>0$
We can write out the two continuities (value and slope)

$$
\begin{align}
\psi_{I} & =Ae^{ikx}+Be^{-ikx} \\
\psi'_{I} & =ikAe^{ikx}-ikBe^{-ikx}
\end{align}
$$
We also have in the second area
$$
\begin{align}
\psi_{II} & =Ce^{ik_{0}x}+De^{-ik_{0}x} \\
\psi'_{II} & =ik_{0}Ce^{ik_{0}x}-ik_{0}De^{-ik_{0}x}
\end{align}
$$
We can't apply the normalization condition, but we can do continuity.
$$
\begin{align}
1)  ~& A+B =C+D \text{, value continuity at x=0  } \\
2)  ~& ik(A-B) =ik_{0}(C-D) \text{ slope continuity at x=0 }
\end{align}
$$
We also have the probability current from long ago: $j_{x}=\frac{\hbar}{2mi}\left( \psi^{*}\frac{d \psi}{dx}-\psi \frac{d \psi^{*}}{dx} \right)$

We have to calculate this.
$$
\begin{align}
j_{I}= \frac{\hbar}{2mi}\left[ (A^{*}e^{-ikx}+B^{*}e^{ikx})(ikAe^{ikx}-ikBe^{-ikx}) - \left( Ae^{ikx}+Be^{-ikx} \right)\left( -ikA^{*}e^{-ikx}+ikB^{*}e^{ikx} \right)\right]
\end{align}
$$
This simplified so
$$
\begin{align}
 \frac{\hbar k}{2m}\left[ \left| A\right|^{2}(1+1)+\left|   B \right|^{2}(-1-1)  +\underbrace{ A^{*}B\left( -e^{-2ikx}+e^{2ikx} \right) +B^{*}A(0) }_{ 0 }\right]  \\
= \underbrace{ \frac{\hbar k}{m} \lvert A \rvert ^{2}  }_{ \text{ positive flow in region 1,  }J_{inc} }-\underbrace{ \frac{\hbar k}{m}\lvert B \rvert ^{2} }_{ J_{\text{ reflected }} } \\
J_{I}=j_{incident}-j_{\text{ reflected }} \\
  
\end{align}
$$

We can do the same in region II
$$
\begin{align}
j_{II}=\underbrace{ \frac{\hbar k_{0}}{n}\left| C \right| ^{2} }_{ j_{\text{ transmission }} }-\cancelto{ 0 \text{ for particle entering from left } }{ \frac{\hbar k_{0}}{m}\left| D \right| ^{2}U }
\end{align}
$$
We can't have a wave flowing to the left in region 2, since there is nothing to reflect off of.

We have the rate of probability flowing in - rate of flow out should be related to the reflected in some way.
$$
\begin{align}
R=\frac{j_{ref}}{j_{inc}} = \frac{\left| B \right| ^{2}}{\left| A \right| ^{2}} \\
T=\frac{j_{\text{ trans }}}{j_{inc}}=\frac{k_{0}}{k} \frac{\left| C \right| ^{2}}{\left| A \right| ^{2}} \\
R+T=1\\
\end{align}
$$

(This is the same as saying $j_{\text{ reflected }}+j_{\text{ transmitted }}=j_{inc}$)

We can get rid of the D's, and can simplify our continuity equations
$$
\begin{align}
A+B=C \\
A-B=\frac{k_{0}}{k}C \\
\text{ which can be added } \\
2A=C\left( 1+\frac{k_{0}}{k} \right) \\
\implies \left| C \right| ^{2}=\left| \frac{2A}{1+\frac{k_{0}}{k}} \right| ^{2}
\end{align}
$$
We now have our R and T

$$
\begin{align}
R=\frac{\left( k-k_{0} \right)^{2}}{\left( k_{1}+k_{0} \right) ^{2}} \\
T= \frac{k_{0}}{k} \frac{4}{\left( 1+\frac{k_{0}}{k} \right) ^{2}}
\end{align}
$$
This is extremely uncomfortable. This tells us that, in the limit that the barrier goes to zero the reflection goes to zero, but if we have any barrier than there is always some non zero probability of reflection.

What if we move the energy down so that its still above zero, but below $V_{0}$

This does have a bound region, so we can have a normalization condition.
We can write 
$$
\begin{align}
\psi_{I}=Ae^{ikx}+Be^{-ikx} \\
\Psi_{II}=Ce^{-\kappa x}+\cancelto{ 0 }{ De^{\kappa x} }
\end{align}
$$
$$
\begin{align}
j_{\text{ ref }}=\frac{\hbar k}{m}\left| B \right| ^{2} \\
j_{\text{ inc }} = \frac{\hbar k}{m} \left| A \right| ^{2}
\end{align}
$$
$$
\begin{align}
j_{II} = \frac{\hbar}{2mi}\underbrace{ \left( \psi^{*} \frac{d \psi}{dx} -\psi \frac{d \psi^{*} }{dx}  \right)  }_{ 0 }
\end{align}
$$
Although there is nonzero probability of finding the particle in the barrier, we don't have any probability flowing in that direction, 
$j_{\text{ trans }}=0$.
