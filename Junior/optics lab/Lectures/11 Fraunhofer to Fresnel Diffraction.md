
If we assume that all the rays exiting slits are basically parallel when they hit a point on the detection plane (which is very far away), we'll have a phase shift between electric field contributions from neighbouring slits given by

$$
\begin{align}
\phi  & \equiv  kd \sin\theta \\
 & = \frac{2\pi}{\lambda} d \sin\theta
\end{align}
$$

We can write out the diffraction through an n-slit grating with slit separation d (each of the n slit s has a separation d from the previous)

$$
\begin{align}
u(\theta) \propto 1 + e^{ikd\sin\theta} + e^{ik 2d\sin\theta} + \dots e^{ik (n-1)d \sin \theta}
\end{align}
$$
This looks like 
$$
\begin{align}
1 + r + \dots + r^{N-1}, \text{ where } r = e^{ikd\sin\theta}
\end{align}
$$
We can add series
$$
\begin{align}
S  & =  1 & +r & &  +\dots  & & + R^{n-1}  \\
rs  & =   & r & &  + \dots  & & +  R^{N-1}  & &  + R^{N} 
\end{align}
$$
So
$$
\begin{align}
S-rs = 1-r^{N} \\
S = \frac{1-r^{N}}{1-r} \text{ for us,} \left| r \right| =1 
\end{align}
$$
So $S=0$ where $r^{N}=1$, but $r\neq 1$. 
S is at the max where $r=1$.
Let $r=1-\epsilon$
$$
\begin{align}
S & = \frac{1- (1-\epsilon)^{N}}{1-(1-\epsilon)} \\
 & \approx \frac{1-(1-N\epsilon)}{1-(1-\epsilon)}  \\
 & = \frac{N\epsilon }{\epsilon} \\
 & = N
\end{align}
$$
So the maxima of $\left| u(\theta) \right|$ for
$\sin\theta=0, \theta=0$ independent of $\lambda$ (all diffraction gratings have maximum straight through where $\theta=0$)
AND
where
$kd\sin\theta = 2N\pi$, $N \in \mathbb{N}$.
$$
\begin{align}
d\sin\theta = \lambda \text{ is  } 1^{\text{ st }} \text{ order max }
\end{align}
$$
so
$$
\begin{align}
\frac{2\pi}{\lambda}d \sin\theta = 2\pi,r\boldsymbol{\pi}.. \\
\sin\theta = \frac{\lambda}{d}
\end{align}
$$

We care about the resolution of a diffraction to show where the maximums are. This will have some width around the peaks - at what angle do you get the zeros?
$$
\begin{align}
kd\sin\theta = 2\pi \pm \frac{2\pi}{N} 
\end{align}
$$
$$
\begin{align}
\frac{2\pi}{\lambda}d \sin\theta = 2\pi \pm \frac{2\pi}{N} \\
\sin\theta = \frac{\lambda}{d}\pm  \frac{\lambda}{dN} 
\end{align}
$$
The closest that we can resolve two frequencies is where the peak intensity for one lines up with the zero of the peak intensity of the other. I.e. they both share the same center, but one takes just barely longer to resolve a maximum again. The offset in peak locations accumulate (to me this looks like harmonics in a Fourier series of two notes, which have weird spacings and can have peaks next to each other or on top or far away, whatever). This just has many peaks instead of peaks from one. 


The condition for wavelengths to be resolvable is that
$$
\begin{align}
\sin\theta = \frac{\lambda}{d}+ \frac{\lambda}{dN} = \frac{\lambda+ \Delta \lambda}{d}
\end{align}
$$
This is the zero next to a peak for $\lambda$ and a peak for $\lambda+\Delta \lambda$.

$$
\begin{align}
\frac{\lambda}{n}= \Delta \lambda \\
\mathscr{R} \equiv \frac{\lambda}{\Delta \lambda}= N
\end{align}
$$
The resolving power is better if the number is higher. $\frac{\lambda}{\Delta \lambda}$ is bigger when we can resolve higher wavelengths. N is the number of slits being hit

Lets go back to the diffraction integral. We can change our coordinate system so that the source and point are at $y=0$. and put the z plane exactly in the center - so that $x_{s}=-x_{p}$. 

$$
\begin{align}
\begin{cases}
\text{ S at } (x_{s} ,0,z_{s} ) \\
\text{ P at } (x_{p} ,0,z_{p} ) 
\end{cases} \\
\frac{x_{s}}{s_{0}}= -\frac{x_{p}}{r_{0}} \equiv \sin \delta  
\end{align}
$$
With the coordinate transform, we'll have to be careful about the bounds - each point on the plane that we choose will have a different coordinate. 
This gets rid of the linear terms (y = 0, $x_{s}-x_{p}=0$), so we just have
![[Pasted image 20260302104330.png]]

$$
\begin{align}
\iint_{A} = e^{\frac{ik}{2}(\frac{1}{s_{0}}+ \frac{1}{r_{0}})x^{2}\cos ^{2}\delta} e^{\frac{ik}{2}(\frac{1}{s_{0}}+ \frac{1}{r_{0}})y^{2}}dxdy
\end{align}
$$




