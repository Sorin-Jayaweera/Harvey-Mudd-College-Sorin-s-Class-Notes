We have 3 Euler Angles: $\theta,\phi,\psi$, which we use to define a location in three-D space. These will help us write out Euler's equations with torque, since the torque will rarely be oriented along directions of motion. 

We have precession, spin, and nutation corresponding to those three. 
## Aligning with the Body Frame

1) Rotate CCW around $\hat{z}$ by $\phi$,
2) Rotate CCW around $\hat{\text{ LON }}$ (line of nodes) by$\theta$
3) Rotate CCW around $\hat{z}'$ by $\psi$.


## Writing T
We have easily kinetic energy $T$ as a function of $\omega$ in the body frame, but lets write this in terms of $\phi,\theta,\psi$.
$$
\begin{align}
T = \frac{1}{2} \lambda_{1} \omega_{x'} ^{2} + \frac{1}{2} \lambda_{2} \omega_{y'} ^{2} + \frac{1}{2} \lambda_{3} \omega_{z'} ^{2}
\end{align}
$$
Our goal is to write
$$
\begin{align}
T = T(\theta,\phi,\psi,\dot{\theta},\dot{\phi},\dot{\psi})
\end{align}
$$
This way, we can calculate the gross thing once, but have a nice easy transform from the inertial frame.

### Infinitesimal Rotations


The rotations for finite angles are non commutative, but they do commute if the rotations are infinitesimal. 
$$
\begin{align}
R_{y}(\delta\theta) \circ  R_{x} (\delta\theta)
\end{align}
$$

smth smth I didn't understand, $\vec{\omega}= \frac{d}{dt}\alpha$.

Lets decompose components onto the $\hat{x}', \hat{y}', \hat{z}'$ basis. 

Lets take advantage of this vector property of rotations.

For example; If we wanted to take $\vec{\omega}_{\phi}$ (precession), lets take the projection onto the basis vectors

$$
\begin{align}
\vec{\omega}_{\phi} &  = \omega_{\phi x'} \hat{x}'+\omega_{\phi y'} \hat{y}' + \omega_{\phi z'} \hat{z}' \\
\vec{\omega}_{\theta} &  = \dots \\
\vec{\omega}_{\psi}  & = \dots \\
\end{align}
$$
Our goal is to write
$$
\begin{align}
\omega_{x'} = \omega_{\phi x'} + \omega_{\theta x'} + \omega_{\psi x'}  \\
\omega_{y'} = \omega_{\phi y'} + \omega_{\theta y'} + \omega_{\psi y'}  \\
\omega_{z'} = \omega_{\phi z'} + \omega_{\theta z'} + \omega_{\psi z'} 
\end{align}
$$
For $\psi:$
$$
\begin{align}
\vec{\omega}_{\psi} = \dot{\psi} \hat{z}'
\end{align}
$$

For $\theta:$
$$
\begin{align}
\vec{\omega}_{\theta} = \dot{\theta}\vec{LON}
\end{align}
$$
$\omega_{\theta}$ points at an angle $\psi$ down along the $x',\,y'$ frame.
$$
\begin{align}
\vec{\omega}_{\theta} = \dot{\theta}\cos \phi \hat{x}'- \dot{\theta}\sin \phi  \hat{y}'
\end{align}
$$
The $z'$ component is zero.

For $\phi:$
$$
\begin{align}
\vec{\omega}_{\phi}  & = \dot{\phi} \hat{z} \\
 & = \dot{\phi}\cos\theta \hat{z}'+ \dot{\phi}\sin\theta \sin  \psi\hat{x}'+ \dot{\phi} \sin\theta \cos \psi \hat{y}'
\end{align}
$$
So finally,
$$
\boxed{
\begin{align}
\vec{\omega}  = \, &  \underbrace{ (\dot{\theta}\cos \psi+\dot{\phi}\sin\theta \sin \psi ) }_{ \omega_{x}  } \hat{x}' \\
 &+\underbrace{  (-\dot{\theta}\sin \psi+\dot{\phi}\sin\theta \cos \psi)  }_{ \omega_{y}  }\hat{y}' \\
 & + \underbrace{ (\dot{\psi}+ \dot{\phi}\cos\theta) }_{ \omega_{z}  }\hat{z}'
\end{align}
}
$$

We can now plug that in nicely to our $T$ expression from the body frame:
$$
\begin{align}
T = \frac{1}{2} \lambda_{1} \omega_{x'} ^{2} + \frac{1}{2} \lambda_{2} \omega_{y'} ^{2} + \frac{1}{2} \lambda_{3} \omega_{z'} ^{2}
\end{align}
$$

Lets think about how we could simplify this for an axisymmetric body, where $\lambda_{1}=\lambda_{2}$, which we'll call $\lambda$.

$$
\begin{align}
\omega_{xy}'^{2} = \omega_{x}'^{2}+ \omega_{y}'^{2} 
\end{align}
$$
$$
\begin{align}
T = \frac{1}{2} \lambda(\dot{\theta}^{2}+\dot{\phi}^{2}\sin ^{2}\theta)+ \frac{1}{2}\lambda_{3}(\dot{\psi}+ \dot{\phi}\cos\theta)^{2}
\end{align}
$$



