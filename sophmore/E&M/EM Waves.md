## What is a wave
We have a new differential forms which imply changing / propagating electromagnetic waves.

$$
\begin{align}
\vec{\nabla}\cdot \vec{E}=0 \\
\vec{\nabla}\times  \vec{E}=-\frac{ \partial \vec{B} }{ \partial t} \\
\vec{\nabla}\cdot \vec{B}=0 \\
\vec{\nabla}\times  \vec{B}=\mu_{0}\epsilon_{0}\frac{ \partial \vec{E} }{ \partial t }  
\end{align}
$$
Which leads to the result
$$
\begin{align}
\nabla^{2}\vec{E}=\mu_{0}\epsilon_{0} \frac{ \partial^{2} }{ \partial t^{2} }\vec{E} 
\end{align}
$$
We learned about waves propagating following the form
$$
\begin{align}
\frac{ \partial^{2}\vec{y} }{ \partial x^{2} } =\frac{1}{v^{2}}\frac{ \partial y^{2} }{ \partial t^{2} } 
\end{align}
$$
so the waves propagate at speed $\frac{1}{\sqrt{ \mu_{0}\epsilon_{0} }}=c$.

For a positive direction-propagating wave, the solution looks like $H(x,t)=h(x-vt)$ (recall that velocity is a vector).

The coupling that allows this to propagate is that changing electric fields cause changing magnetic fields. The Laplacian gives us some measure of the curvature of space in our field. 

## Properties of EM waves
Let $$
\begin{align}
\vec{E}(x,y,z,t)=\vec{E_{0}}f(x-ct) \text{ where } \vec{E}_{0}\text{ is a direction vector }
\end{align}
$$
$\vec{E}_{0}=E_{0}x \hat{x}+E_{0}y \hat{y} + E_{0}z \hat{Z}$.
We know that the divergence of this electric field needs to be equal to zero.
$$
\begin{align}
\vec{\nabla}\cdot \vec{E}=0\text{ because we have  } \rho=0 \\
\implies \frac{ \partial E_{x} }{ \partial x } +\frac{ \partial E_{y} }{ \partial x } + \frac{ \partial E_{z} }{ \partial z }=0 
\end{align}
$$
For simplicity, lets assume that the field is only moving x, aka no change in the y and z direction. 

Lets choose a functional form that will make this more concrete. Imagine that we choose a simple sinusoid, $\vec{E}_{0}\sin(x-ct)$.
$$
\begin{align}
\frac{d}{dx}E_{0,x}\sin (x-ct)=0 \\
E_{0,x}\cos(x-ct) =0
\end{align}
$$

this must be valid at every point in space, so $E_{0,x}=0$. This tells us that EM waves are transverse (aka there can't be a component of the wave in the direction of propagation). Lets put E in the y direction.

take $\vec{\nabla}\times \vec{E}=-\frac{ \partial B }{ \partial t }$
$$
\begin{align}
\vec{\nabla}\times \vec{E}=\frac{ \partial  }{ \partial x } (E_{0}\hat{y}\sin(x-ct))\hat{z}=-\frac{ \partial B }{ \partial t } 
\end{align}
$$

$$
\begin{align}
\frac{ \partial B }{ \partial t }  & =\frac{ \partial  }{ \partial x } (E_{0}\sin(x-ct))(-\hat{z}) \\
\frac{ \partial B }{ \partial t }  & =E_{0}\cos(x-ct)(-\hat{z}) \\
\vec{B} & =\frac{E_{0}}{c}\sin(x-ct)(\hat{z})
\end{align}
$$

We have shown that the magnetic and electric fields point in two different directions, and have magnitude $B_{0}=\frac{E_{0}}{c}$.

By the finger version of the right hand rule, with a pointer finger in the direction of travel, the thumb is the direction of $B$ and middle finger in the direction of $E$.

We write out the wave a little more formally to make it nice:
$$
\begin{align}
\vec{E}=E_{0}\hat{y}\sin(kx-\omega t) \\
k = \text{ wave number } \frac{2\pi}{\lambda} \\
\omega=\text{ angular frequency }=\frac{2\pi}{P\text{ osc }}
\end{align}
$$
$$
\begin{align}\text{ this implies }
\frac{\omega}{k}=c
\end{align}
$$





