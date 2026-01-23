![[Pasted image 20251108094547.png|500]]
## a)
The cone is azimuthally symmetric, so we can pick any arbitrary rotational axis slicing straight across the flat circular base of the cone through the center of that base, and any axis that is perpendicular to it while still parallel to the surface of the base. The third axis is rotation about the line from the base of the cone to the fixed point tip. 

## b) 
The inertia tensor is defined as having
$$
\begin{align} 
\mathscr{\left| r \right| ^{2}} & =(x^{2}+y^{2}+z^{2}) \\

\mathcal{I}_{ij} & = \iiint_{vol} dm (\mathscr{r} ^{2}\delta _{ij}- \mathscr{r} _{i} \mathscr{r} _{j)} &  \\
\end{align}
$$

### Radially

We can now slog through finding the components.
To make the calculations easier, I define
$$
\begin{align}
x = r\cos\theta \\
y = r\sin\theta
\end{align}
$$

$$
\begin{align}
\mathcal{I}_{ij} = m\int_{\theta=0} ^{2\pi}\int_{z=0}^{h}\int_{r=0}^{\frac{R}{h}z}  (r^{2}\delta _{ij}   - r_{i}r_{j}) \,  r \, dr \,  d\theta \, dz 
\end{align}
$$


First, I will start with the diagonals:
#### Diagonal Components
##### $\mathcal{I}_{x x}$:
$$
\begin{align}
\mathcal{I}_{x x}  & =m \int_{\theta=0}^{2\pi} \int_{z=0}^{h} \int_{r=0}^{\frac{R}{h}z} r^{3} -   r^{3}\cos ^{2}\theta \, dr \,  dz\, d\theta \\
\mathcal{I}_{xx}  & =m   \int_{\theta=0}^{2\pi} \int_{z=0}^{h} \int_{r=0}^{\frac{R}{h}z} r^{3}(1- \cos ^{2}\theta)dr \,  dz\, d\theta  \\ \\
\mathcal{I}_{xx}  & = m\int_{\theta=0}^{2\pi}  (1-\cos ^{2}\theta) \int_{z=0}^{h} \frac{r^{4}}{4}\bigg|_{0}^{\frac{R}{h}z} \, dz \, d\theta  \\
\mathcal{I}_{xx}  & = m\frac{1}{4}\left( \frac{R}{h} \right) ^{4 }\int_{\theta=0}^{2\pi}  (1-\cos ^{2}\theta) \int_{z=0}^{h} z^{4} \, dz \, d\theta   \\
\mathcal{I}_{xx}  & = m\frac{1}{4}\left( \frac{R}{h} \right) ^{4 }\int_{\theta=0}^{2\pi}  (1-\cos ^{2}\theta) \int_{z=0}^{h} z^{4}  \, dz \, d\theta \\
\mathcal{I}_{xx}  & = m\frac{1}{4}\left( \frac{R}{h} \right) ^{4 } \frac{h^{5}}{5}  \int_{\theta=0}^{2\pi}  (1-\cos ^{2}\theta)d\theta  \\
\end{align}
$$

$$
\begin{align}
\mathcal{I}_{x x}  & = m \frac{1}{4}\left( \frac{R}{h} \right) ^{4 } \frac{h^{5}}{5}  \int_{\theta=0}^{2\pi}  (1-\cos ^{2}\theta)  d\theta \\
& =  m\frac{1}{4}\left( \frac{R}{h} \right) ^{4 } \frac{h^{5}}{5}   \left( \theta-\frac{\sin ^{3}\theta}{3} \right) \bigg|_{0}^{2\pi}\\
& =  m\frac{1}{4}\left( \frac{R}{h} \right) ^{4 } \frac{h^{5}}{5}   (2\pi) \\ \\
\mathcal{I}_{xx} & =\frac{\pi R^{4}hm}{10} 
\end{align}
$$

##### $\mathcal{I}_{yy}$:
$$
\begin{align}
\mathcal{I}_{y y}  & = m\int_{\theta=0}^{2\pi} \int_{z=0}^{h} \int_{r=0}^{\frac{R}{h}z} r^{3} -   r^{3}\sin ^{2}\theta \, dr \,  dz\, d\theta \\
\end{align}
$$
Using the result from before, this collapses to
$$
\begin{align}
\mathcal{I}_{y y} & = \frac{m}{4}\left( \frac{R}{h} \right) ^{4 } \frac{h^{5}}{5}  \int_{\theta=0}^{2\pi}  (1-\sin ^{2}\theta)d\theta   \\
& = \frac{m}{4}\left( \frac{R}{h} \right) ^{4 } \frac{h^{5}}{5}   \left[ \left( \theta-\frac{\cos ^{3}\theta}{3} \right)\bigg|_{\theta=0}^{2\pi}   \right] \\
 & = \frac{m}{4}\left( \frac{R}{h} \right) ^{4 } \frac{h^{5}}{5}  \left[ 2\pi - \frac{1}{3}+\frac{1}{3} \right]  \\
 & = \frac{m}{10} \pi R^{4}h
\end{align}
$$
##### $\mathcal{I}_{zz}$:
$$
\begin{align}
\mathcal{I}_{ij}  & =m \int_{\theta=0} ^{2\pi}\int_{z=0}^{h}\int_{r=0}^{\frac{R}{h}z}  (r^{2}   - z^{2}) \,  r \, dr \,  d\theta \, dz \\
 & = m\int_{\theta=0} ^{2\pi}\int_{z=0}^{h}\int_{r=0}^{\frac{R}{h}z}  r^{3}-z^{2}r \, dr \,  d\theta \, dz \\
 & =m\int_{\theta=0} ^{2\pi}\int_{z=0}^{h} \frac{r^{4}}{4}-\frac{z^{2}r^{2}}{2} \bigg|_{r=0}^{\frac{R}{h}z} \\
& =m\int_{\theta=0} ^{2\pi}\int_{z=0}^{h} \frac{\left( \frac{R}{h} \right)^{4}z^{4}}{4}-\frac{z^{4}\left( \frac{R}{h} \right)^{2}}{2} dz \, d\theta\\
& =m\left[ \frac{\left( \frac{R}{h} \right)^{4}}{4}-\frac{\left( \frac{R}{h} \right)^{2}}{2} \right]\int_{\theta=0} ^{2\pi}\int_{z=0}^{h} z^{4} dz \, d\theta \\
& =m\left[ \frac{\left( \frac{R}{h} \right)^{4}}{4}-\frac{\left( \frac{R}{h} \right)^{2}}{2} \right]\int_{\theta=0} ^{2\pi} \frac{h^{5}}{5} \, d\theta \\
\end{align}
$$


$$
\begin{align}
\mathcal{I}_{zz}  & = \frac{2\pi m h^{5}}{25} \left[ \frac{\left( \frac{R}{h} \right)^{4}}{4}-\frac{\left( \frac{R}{h} \right)^{2}}{2} \right] \\
 & =\frac{2\pi m}{25}\left[ \frac{R^{4}h}{4}- \frac{R^{2}h^{4}}{2} \right]
\end{align}
$$

#### Off diagonals


$$
\begin{align}
\mathcal{I}_{ij}  & = m\int_{\theta=0} ^{2\pi}\int_{z=0}^{h}\int_{r=0}^{\frac{R}{h}z} - r_{i}r_{j} \,  r \, dr \,  d\theta \, dz  & i\neq  j
\end{align}
$$
##### $I_{xy}$:

$$
\begin{align}
\mathcal{I}_{xy} &  = m \int_{\theta=0}^{2\pi} \int_{z=0}^{h} \int_{r=0}^{\frac{R}{h}z} -r^{3}\cos\theta  \sin\theta  \, dr\, dz\, d\theta \\
 & =-m\int_{\theta=0}^{2\pi}\cos\theta \sin\theta \int_{z=0}^{h} \frac{\left( \frac{R}{h}z \right)^{4}}{4} dz\,  d\theta\\
& =-\frac{m}{20}\int_{\theta=0}^{2\pi}\cos\theta \sin\theta R^{4}h\,   d\theta \\
 & = -\frac{m R^{4}h}{20} \left( \frac{1}{2} \sin ^{2}\theta \right)\bigg|_{\theta=0}^{2\pi} \\
 & = 0  
\end{align}
$$
##### $\mathcal{I}_{xz}$:
$$
\begin{align}
\mathcal{I}_{xz}  & = -m\int_{\theta=0} ^{2\pi}\int_{z=0}^{h}\int_{r=0}^{\frac{R}{h}z}  z\cos\theta \,  r \, dr \,  d\theta \, dz  \\
& = -\frac{m}{2}\left( \frac{R}{h} \right)^{2}\int_{\theta=0} ^{2\pi}\int_{z=0}^{h}  z^{2}\cos\theta \,  d\theta \, dz  \\
\end{align}
$$
We see that this integral depends on 
$$
\begin{align}
\int_{0}^{2\pi} \cos\theta = 0
\end{align}
$$
so $\mathcal{I}_{xz}=0$:

##### $\mathcal{I}_{yz}$
$$
\begin{align}
\mathcal{I}_{ij}  & = m\int_{\theta=0} ^{2\pi}\int_{z=0}^{h}\int_{r=0}^{\frac{R}{h}z} - z \sin\theta \,  r^{2} \, dr \,  d\theta \, dz 
\end{align}
$$
This depends on 
$$
\begin{align}
\int_{0}^{2\pi} \sin\theta=0
\end{align}
$$
so $\mathcal{I}_{yz}=0$.


The matrix must be symmetric, so $\mathcal{I}_{xy}=\mathcal{I}_{yx}, \mathcal{I}_{xz}=\mathcal{I}_{zx}, \mathcal{I}_{yz}=\mathcal{I}_{zy}$

## End of problem
This gives us finally the matrix


$$
\begin{align}
\mathcal{I}= \begin{bmatrix}
\frac{\pi mR^{4}h}{10} & 0  & 0 \\
 0&  \frac{\pi mR^{4}h}{10} &  0\\
 0&  0& \frac{2\pi m}{25}\left[ \frac{R^{4}h}{4}- \frac{R^{2}h^{4}}{2} \right]
\end{bmatrix}
\end{align}
$$
$$
\boxed{
\begin{align}
\mathcal{I} = \pi mR^{2} \begin{bmatrix}
\frac{R^{2}h}{10} & 0 & 0  \\
0 & \frac{R^{2}h}{10} & 0  \\
0 & 0 & \frac{R^{2}h}{50}-\frac{h^{4}}{25}
\end{bmatrix}
\end{align}
}
$$


![[Pasted image 20251108094556.png|500]]




## a
Instead of considering the periodically triangular structure of Toblerone chocolate which i was doing initially (pictured below), I am considering the cartridge (thanks Conner). 
![[Pasted image 20251108144347.png|300]] 

$$
\begin{align} 
\mathscr{\left| r \right| ^{2}} & =(x^{2}+y^{2}+z^{2}) \\

\mathcal{I}_{ij} & = \iiint_{vol} dm (\mathscr{r} ^{2}\delta _{ij}- \mathscr{r} _{i} \mathscr{r} _{j}) &  \\
\end{align}
$$
For principle axes, the inertia matrix is diagonal so $\mathcal{I}_{zx}=\mathcal{I}_{zy} = 0$.

This leaves just the $\mathcal{I}_{zz}$ term
$$
\begin{align}
\mathcal{I}_{zz}   & = \iiint_{vol} r^{2} - z^{2} \, dm  \\
 & = M\iiint_{vol} x^{2}+y^{2} 
\end{align}
$$
Let the height of the bar be denoted $h$. 
We can evaluate this.
![[Pasted image 20251108150043.png|300]]

There is no z dependence, so this is just 
$$
\begin{align}
\mathcal{I}_{zz}  & = M h \int_{y=0 }^{\frac{\sqrt[]{ 3 }}{2}\left|a- x \right| } \int_{x=-a}^{a} x^{2}+y^{2} \,  dx \,  dy \\
 & =2Mh \int_{x=0}^{a} \int_{y=0}^{\frac{\sqrt[]{ 3 }}{2} a-x   }x^{2}+y^{2}\, dy\, dx  \\
 & =2Mh \int_{x=0}^{a} x^{2}\left( \frac{\sqrt{3}}{2}(a-x) \right)+\frac{\left( \frac{\sqrt[]{ 3 }}{2}(a-x) \right) ^{3}}{3} \, dx \\
 & =\frac{7Mha^{4}}{16 \sqrt[]{ 3 } } 
\end{align}
$$


## b 

There are two reflection symmetries in the system, corresponding to the equilateral if we let the Toblerone have pyramids. These are triangle/rectangular base and flip across the length, since the uneven top is still symmetric on either side of this plane.
![[Pasted image 20251108111753.png|300]]
![[Pasted image 20251108144125.png|300]]

If we assume that the Toblerone has not been eaten and is in a nice triangular prism and has no ridges, it is also rotationally symmetric 


These give two of the three axis. The third is rotation about the center line of the bar.

Depicted are all three rotations about the principle axes:
![[Pasted image 20251109134500.png|500]]






![[Pasted image 20251108094608.png|500]]
## a
The coordinates are of the three masses are given by the following:
$$
\begin{align}
\mathbf{R} & = a\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 2 \\
0 & 2 & 1
\end{pmatrix} \begin{pmatrix}
x\\ y \\ z
\end{pmatrix} \\
 & \text{ with } \\
\mathbf{M} & = \begin{pmatrix}m \\ m \\ m\end{pmatrix}
\end{align}
$$

$$
\begin{align} 
\mathscr{\left| r \right| ^{2}} & =(x^{2}+y^{2}+z^{2}) \\

\mathcal{I}_{ij} & = \iiint_{vol} dm (\mathscr{r} ^{2}\delta _{ij}- \mathscr{r} _{i} \mathscr{r} _{j}) &  \\
\end{align}
$$
We can find the easy diagonals by inspection:
$$
\begin{align}
\mathcal{I}_{xy}  & = \iiint_{vol} -xy\, dm \\
 & = -\sum_{i=1}^{3} \mathbf{R}_{x,i}\mathbf{R}_{y,i} m_{i}   \\
 & =0 
\end{align}
$$
Similarly,
$$
\begin{align}
\mathcal{I_{xz} } =- \sum_{i=1}^{3}R_{x,i} R_{z,i}m_{i}  =0 
\end{align}
$$

$$
\begin{align}
\mathcal{I} _{yz}  = 0 + 2a^{2} + 2a^{2} = -4ma ^{2}
\end{align}
$$

Now we can find the diagonals
$$
\begin{align}
\mathcal{I}_{yy}  & =  m\iiint_{vol} x^{2}+z^{2}  \\
 & =m (a^{2}+4a^{2}+a^{2}) \\
 & =6ma^{2}
\end{align}
$$

$$
\begin{align}
\mathcal{I}_{zz}  & = m \iiint_{vol} x^{2}+y^{2}  \\
 & = 6ma^{2}
\end{align}
$$

$$
\begin{align} 
\mathcal{I}_{xx} &  =  \iiint_{vol} y^{2}+z^{2}\\
\mathcal{I}_{xx}  & = m(a^{2}+4a^{2}+4a^{2}+a^{2}) \\
 & = 10ma^{2} 
\end{align}
$$

### Final Matrix

$$
\begin{align}
\mathcal{I}  & = \begin{bmatrix}
 10ma^{2} & 0 & 0 \\
0 & 6ma^{2} & -4ma^{2} \\
0 & -4ma^{2} &6ma^{2}   \\
\end{bmatrix} \\
\mathcal{I}&=2ma^{2} \begin{bmatrix}
5 & 0 & 0 \\
0 & 3 & -2 \\
0 & -2 & 3
\end{bmatrix}
\end{align}
$$

## b
![[Pasted image 20251109134745.png|500]]

We found that
$$
\begin{align}
\mathcal{I}&=2ma^{2} \begin{bmatrix}
5 & 0 & 0 \\
0 & 3 & -2 \\
0 & -2 & 3
\end{bmatrix}
\end{align}
$$

The principle axes are the eigenvectors of this matrix, with the principle moments as the eigenvalues. 

We can solve this easily.
$$
\begin{align}
\det{\left(\begin{bmatrix}
5 & 0 & 0 \\
0 & 3 & -2 \\
0 & -2 & 3
\end{bmatrix} - \lambda I \right) } = 0 \\
\det{\begin{bmatrix}
5- \lambda & 0 & 0 \\
0 & 3-\lambda & -2 \\
0 & -2 & 3-\lambda
\end{bmatrix}} = 0
\end{align}
$$
This leads to
$(5-\lambda)[(3-\lambda)(3-\lambda)-4] = 0$
We see that $\lambda=5$ is the first eigenvalue. 
$$
\begin{align}
(3-\lambda)^{2}-4=0 \\
5-6\lambda+\lambda^{2}=0
\end{align}
$$

This is factorable into
$$
\begin{align}
(\lambda-1)(\lambda-5)=0
\end{align}
$$
And has two eigenvalue solutions - one is degenerate.
$$
\begin{align}
\lambda_{1}=1,\,  \lambda_{2}=5, \lambda_{3}=5
\end{align}
$$

Eigenvectors must satisfy
$$
\begin{align}
\begin{pmatrix}
5-\lambda & 0 & 0 \\
0 & 3-\lambda & -2 \\
0 & -2 & 3-\lambda
\end{pmatrix} \begin{pmatrix}
x \\ y \\ z
\end{pmatrix} = \vec{0}
\end{align} 
$$


For $\lambda_{1}$, this is
$$
\begin{align}
\begin{bmatrix}
4 & 0 & 0 \\
0 & 2 & -2 \\
0 & -2 & 2
\end{bmatrix}
\end{align}
$$

We get the expression
$$
\begin{align}
x=0 \\
y=z
\end{align}
$$
so 
$$
\begin{align}
E_{1} = \begin{pmatrix}
0  \\ 1 \\ 1
\end{pmatrix}
\end{align}
$$

For $\lambda_{2},\lambda_{3}$ this is
$$
\begin{align}
\begin{bmatrix}
0 & 0 & 0 \\
0 & -2 & -2 \\
0 & -2 & -2
\end{bmatrix}
\end{align}
$$
Which yields
$y=-z$.
$x$ can be anything. We must find two linearly independent eigenvectors 
so
$$
\begin{align}
E_{2} = \begin{pmatrix}
0 \\ 1 \\ -1
\end{pmatrix}
\end{align}
$$
A nice vector that is orthogonal to this is
$$
\begin{align}
E_{3}= \begin{pmatrix}
1\\0\\0
\end{pmatrix}
\end{align}
$$

This gives the basis for the principle axes of rotation as
$$
\begin{align}
\mathbb{B} = 2ma^{2}\begin{bmatrix}
0 & 0 & 1 \\
1 & 1 & 0 \\
1 & -1 & 0
\end{bmatrix}
\end{align}
$$
with principle moments of inertia 
$2ma^{2}\text{ and } 10ma^{2}$.

## c
![[Pasted image 20251109134800.png]]

The angular momentum is given by
$$
\begin{align}
\vec{L}  & = \mathcal{I}\mathbb{w} \\
 & = \begin{bmatrix}
0 & 0 & 1 \\
1 & 1 & 0 \\
1 & -1 & 0
\end{bmatrix} \begin{pmatrix}
0\\ 0 \\ \omega_{0}
\end{pmatrix} \\
 \vec{L}& = 2ma^{2}\omega_{0} \begin{pmatrix}
1 \\0 \\ 0
\end{pmatrix}
\end{align}
$$

With no external forces, the angular momentum will be conserved. Because this is in the principle axis coordinate system and each vector is orthogonal, there are no cross interaction terms for the momentum to transfer between, so both $\vec{l} \text{ and } \vec{\omega}$ will remain constant.



![[Pasted image 20251108094620.png]]
## a 
The ball rolls in a circular motion about the center of the circle, always at the same distance. This fixed point at the center is a useful reference frame because it is stuck and the motion is at a fixed radius away - rigid reference points with rotational symmetry are nice. The perpendicular axis to the plane placed at the center of the path circle  therefore makes sense as a principle axis. 


## b
When rolling without slipping, the ball has an instantaneous pivot point at the point of contact. However, to easily consider energy, I will translate this the be about the axis at the center with the parallel axis theorem.

The moment of inertia about this disks center of mass is $\frac{1}{2}MR^{2}$.


$$
\begin{align}
T  & = \frac{1}{2}I_{cm} \dot{\phi}^{2} + \frac{1}{2}Mv_{cm}^{2} \\
 & = \frac{1}{4}MR^{2} \dot{\phi}^{2} + \frac{1}{2}M\left( (R-\alpha)\dot{\phi} \right)^{2} \\
 & = \frac{1}{4}MR^{2}\dot{\phi}^{2} + \frac{1}{2}M(R-\alpha)^{2} \dot{\phi}^{2} \\
T & = \dot{\phi}^{2} \left( \frac{MR^{2}}{4} + \frac{MR^{2}}{2} + \frac{M\alpha^{2}}{2} - MR\alpha \right) \\
T & = \dot{\phi}^{2}M\left( \frac{3}{4}R^{2} +  \frac{\alpha^{2}}{2}- \alpha R\right)
\end{align}
$$


## c

The ball has gravitational potential about the center of mass, which is given by
$$
\begin{align}
U  & = mgh \\
 & = mg ( R-(R-\alpha) \cos \phi) \\
 & =mg( R- R\sin \phi+\alpha \cos \phi) \\
 & = mgR(1-\cos \phi) + mg\alpha \cos \phi
\end{align}
$$


This gives the Lagrangian as
$$
\begin{align}
\mathscr{L} = \dot{\phi}^{2}M\left( \frac{3}{4}R^{2} +  \frac{\alpha^{2}}{2}- \alpha R\right) - mgR(1-\cos \phi) - mg\alpha \cos \phi
\end{align}
$$

We can grab the $EL$ equations from this to find the frequency of oscillation. 




$$
\begin{align}
\frac{ \partial \mathscr{L} }{ \partial \phi }  & = \frac{d}{dt} \frac{ \partial \mathscr{L} }{ \partial \dot{\phi} } 
\end{align}
$$
$$
\begin{align}
\frac{ \partial \mathscr{L} }{ \partial \phi }  & =- Mg(R-\alpha)\sin \phi \\
\frac{d}{dt}  \frac{ \partial \mathscr{L} }{ \partial \dot{\phi} }  & = 2M\left( \frac{3}{4}R^{2}+\frac{\alpha^{2}}{2}-\alpha R \right)\ddot{\phi}
\end{align}
$$


So we have
$$
\begin{align}
\ddot{\phi } = \frac{-g(R-\alpha)}{\frac{3}{2}R^{2}+\alpha^{2}-2\alpha R} \sin \phi
\end{align}
$$


For small angles, we can approximate $\sin \phi=\phi$
This gives us an equation like
$$
\begin{align}
\ddot{\phi} = -\omega^{2}\phi
\end{align}
$$
so
$$
\begin{align}
\omega= \sqrt[]{ \frac{g(R-\alpha)}{\frac{3}{2}R^{2}+\alpha^{2}-2\alpha R} } 
\end{align}
$$





