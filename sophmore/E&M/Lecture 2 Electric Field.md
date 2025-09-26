The Force on a point charge = the charge of that point $\times$ the electric field at that point.

$$
\begin{align}
\vec{E}=\frac{1}{4\pi \epsilon_{0}} \frac{\delta}{r^{2}}\hat{r}
\end{align}
$$

![[Pasted image 20240828091029.png|300]]
The field tapers off by $r^{3}$, so the arrows get dramatically smaller everywhere.

If we have a more complicated body, we have to add up all of the electric fields from the point charges, but make the body continuous instead of discrete.
![[Pasted image 20240829094715.png|300]]
We have a surface that looks like a potato, and take small chunks out of it. We draw the $\vec{r}$ to the field point that we want to calculate. The Field at that point is the integral $\int d\vec{E}$
$$
\begin{align}
d\vec{E}=\frac{dq}{r\pi\epsilon_{0}r^{2}}\hat{r}
\end{align}
$$


![[Pasted image 20240829094729.png|300]]
Note, the $\hat{r}$ is a function based on what part of the surface is being integrated.

![[Pasted image 20240829095042.png]]

Lets work through an example.
![[Pasted image 20240829095523.png|300]]
Lets use cylindrical coordinates because of the symmetries of rotation. Cartesian would also work here. 

![[Pasted image 20240829101808.png]]
![[Pasted image 20240829101836.png]]
![[Pasted image 20240829102442.png]]
This requires doing a trig substitution.
$$
\begin{align}
\tan \theta=\frac{z}{r}\implies_{1}+\frac{z^{2}}{r^{2}}=1+\tan \theta \\
\frac{dz}{d\theta}=r\sec ^{2}=?dz=\frac{r}{\cos ^{2}\theta}d\theta \\
\int \frac{dz}{\left( 1+\frac{z^{2}}{r^{2}} \right)^{3/2}} \,  \\
= \int \frac{rd\theta}{\cos ^{2}\theta\left( 1+\frac{\sin ^{2}\theta}{\cos ^{2}\theta} \right)^{3/2}} \, \left(\frac{ \cos ^{3}\theta}{\cos^{3}\theta} \right) \\
= r\int \cos\theta d\theta  
\end{align}
$$
We get the final result that 
$$
\begin{align}
\vec{E}_{line}=\frac{\lambda}{2\pi\epsilon_{0}}\hat{r}
\end{align}
$$

See previous: [[Lecture 1 Overview]]
See next: [[Lecture 3 Gauss's law]]
