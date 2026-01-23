Last time, we discovered the inertia tensor, where 
$$
\begin{align}
\mathcal{I}_{ij} & = \iiint_{vol} dm (\mathscr{r} ^{2}\delta _{ij}- \mathscr{r} _{i} \mathscr{r} _{j}) &  \\
[\mathcal{I}_{ij}] & =kg\cdot m^{2} \\
\end{align}
$$

For instance, if we had a cube of side length $a$, density $\rho$, and pinned a corner at the origin. 
$\mathscr{r^{2}}=(x^{2}+y^{2}+z^{2})$

$$
\begin{align}
\mathcal{I}_{xy}  & = \iiint -xy \, dm \\
 & =\frac{1}{4}\rho a^{5}
\end{align}
$$
If we throw a box in the air in uniform gravity, the gravity doesn't apply any net torque about the box's center of mass. $\vec{R}\times \vec{F}=0$, since $\vec{R}=\vec{0}$, or since there is a balance of torques for all points around the center of mass. 

The biggest and smallest moment of inertia are good axes, but the middle one is unstable. 

All of today is about symmetries and principle axes. 
When you have something that is perfectly symmetric in two dimensions, then two eigenvalues are degenerate.


When we throw a thing, it can change how fast it is spinning and along which axes, even though angular momentum is conserved. 

## Moment of Inertia
Lets define the inertia tensor as $\mathscr{I}$, with $\vec{\omega}\text{ and } \vec{L}$ vectors.
Lets define the matrix representation of $\mathscr{I}$ as $\mathcal{I}$ with $\mathbb{w},\mathbb{L}$ as vector components of $\mathscr{I}$.

### Inertial Frame
Lets take a box and spin it around any arbitrary axis. 

In the inertial frame, we have 
$$
\begin{align}
\underbrace{ \mathcal{I} }_{ \text{ inertial frame } } = \begin{pmatrix}
I_{xx} & I_{xy}  & I_{xz} \\
\vdots  & \ddots & \vdots \\
I_{zx}  & \dots & I_{zz} \\
 \end{pmatrix}
\end{align}
$$
We have that
$$
\begin{align}
\mathcal{I} \hat{e}_{i} = \lambda_{i} \hat{e}_{i}
\end{align}
$$
($\hat{e}_{i}$ are the eigenvectors).

In the body frame of the box, we define new coordinates $\hat{x}',\hat{y}',\hat{z}'$ that are the eigenvectors of this matrix. The components of these eigenvectors are the directions in the inertial frame. In the body frame, it would just be identities:$\begin{pmatrix}1\\0\\0\end{pmatrix}$, because they are the axes themselves. Don't get confused during coordinate transformations. 

Inertia tensors are physical things. Different bases of $\mathcal{I}$ will get different elements, but the inertia tensor $\mathscr{I}$ is the physical thing which $\mathcal{I}$ is the projection of into a matrix form. 


## Angular Momentum
Lets  find Angular Momentum in the inertial and body frames.

$$
\begin{align}
\mathbb{L}= \mathcal{I} \mathbb{w} = \begin{pmatrix}
I_{x x}  & I_{x y}  & I_{xz} \\
\vdots & \vdots & \vdots 
\end{pmatrix} \begin{pmatrix}
\omega_{x} \\ \omega_{y}  \\ \omega_{z} 
\end{pmatrix} = \begin{pmatrix}
L_{x} \\ L_{y} \\ L_{z} 
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
L_{x}   & = I_{xx}\omega_{x} + I_{xy} \omega_{y} + I_{xz} \omega_{z}  \\
L_{y} & = \dots \\
L_{z}  & = \dots  \\ 
\text{  In any}  & \text{ basis, we can write $\vec{L}$}\\
\vec{L}  & = L_{x} \hat{x} + L_{y} \hat{y}+L_{z} \hat{z} \\
 & =L_{x}'\hat{x}' + L_{y}'\hat{y}' + L_{z}'\hat{z}' 
\end{align}
$$

The physical vector $\vec{L}$ in any basis 

$$
\begin{align}
\vec{\omega} = \omega_{x} ' \hat{e}_{1} + \omega_{y} ' \hat{e}_{2} + \omega_{z} ' \hat{e}_{3}  \\
L = \mathcal{I} (\omega'_{x}\underbrace{ \mathcal{I} \hat{e}_{1} }_{ \lambda_{1}\hat{e}_{1} }+ \omega'_{y}\mathcal{I} \hat{e}_{2} + \omega'_{z} \mathcal{I}\hat{e}_{3}) \\
\vec{L} = \lambda_{1}\omega_{x} \hat{e}_{1} + \lambda_{2}\omega_{y}' \hat{e}_{2} + \lambda_{3}\omega'_{z} \hat{e}_{3}\\
\end{align}
$$
If we are asking for just one component, 
$$
\begin{align}
\mathbb{L}' &  = \mathcal{I}' \omega' \\
L_{x} '  & = I_{xx}'\omega_{x} ' + I_{xy}'\omega_{y} ' + I_{xz}'\omega_{z} '  
\end{align}
$$
In the nice body basis, however, the angular momentum should only be defined by the rotation about each axis there since all axes are orthogonal )(no cross terms). We only care about $\omega_{x}$ - so we get rid of the cross terms. 
$$
\begin{align}
\mathcal{I}' = \begin{pmatrix}
\lambda_{1} & 0 & 0 \\
 0 & \lambda_{2} & 0 \\
0 & 0 & \lambda_{3}
\end{pmatrix} 
\end{align}
$$
Lets think about energy
## $T_{rot}$
$$
\begin{align}
T_{rot}  = \frac{1}{2} \sum_{ij}^{} \omega _{i} \mathcal{I}_{ij}\omega _{i} \\
T_{rot} ' = \frac{1}{2} \sum_{i j}^{} \omega _{i}'\mathcal{I}_{ij}'\omega _{j}' 
\end{align}
$$
The rotational kinetic energy is a scaler, so it shouldn't matter what basis you use - they should get the same result. This is easiest with the body frame, since its only 3 terms (yay diagonals!). Note that this is a tricky argument - if we had a frame rotating in the same way as the object, obviously it would appear to have no rotation. We aren't really making a rotating frame, just rewriting our axis to nicer support representation in eigenmodes. 

$$
\begin{align}
 & = \frac{1}{2} [ \lambda_{1}\omega_{x}'^{2}+\lambda_{2}\omega_{y}'^{2}+\lambda_{3}\omega_{z}'^{2}]
\end{align}
$$

## Comparison

### In the inertial frame
$$
\begin{align}
\mathbb{L} = \begin{pmatrix}
L_{x} \\ L_{y} \\ L_{z} 
\end{pmatrix}\text{  is complicated} 
\end{align}
$$
$T_{rot}$ is complicated
$\mathcal{I}_{ij}$ changes with time. However, $\hat{x},\hat{y},\hat{z}$ are fixed and don't change with time.

### In the body frame
$$
\begin{align}
\mathbb{L}= \begin{pmatrix}
L'_{x} \\ L'_{y} \\ L'_{z} 
\end{pmatrix}= \begin{pmatrix}
\lambda_{1} \omega_{x}' \\ \lambda_{2} \omega_{y}' \\ \lambda_{3} \omega_{z}' 
\end{pmatrix} \text{ is easy }
\end{align}
$$

$T_{rot}$ is simple, because we only have three terms. $\frac{1}{2} [ \lambda_{1}\omega_{x}'^{2}+\lambda_{2}\omega_{y}'^{2}+\lambda_{3}\omega_{z}'^{2}]$.
$\mathcal{I}_{ij}$ are fixed in time.

The only bad thing is that $\hat{x}',\hat{y}',\hat{z}'$ are changing with time - it is not an inertial reference frame. 

## Principle axis from symmetry

If there exists a reflection symmetry, say from $x\to -x$, then the $\hat{x}$ direction is a principle axis. 

An object with continuous rotational symmetry has the symmetry axis as a principle axis. For one with this we could place two eigenvectors perpendicular on that plane arbitrarily, so they will have the same eigenvalues. 






