![[20261013_094002.jpg]]

Lets take a shell, ground one half, enforce no electric field at the other, and put a charge inside. What is the field in region $D$? Nasty. Lets map it. 

In $\Gamma_{2},E_{n}=0$. 

Don't ask us how to make $\frac{ \partial \phi }{ \partial n }=0$ in real life, do we look like experimentalists to you?

we have
$$
\begin{align}
\vec{\nabla}^{2}\phi = - 4\pi q \delta^{3}(x-x_{0})
\end{align}
$$

In 3D, we have 
$$
\begin{align}
\phi= \frac{q}{\left| x-x_{0} \right| }
\end{align}
$$

in 2D, we have
$$
\begin{align}
\phi=-q\ln (x-x')
\end{align}
$$
We can guess the complex solution
$$
\begin{align}
\Omega(z) = -q\ln z + \text{ stuff } \\
\phi = Re(-q\ln z)= -q\ln \left| z \right| 
\end{align}
$$

Lets try to take our nasty circle $D$ with $\Gamma_{1}$ and $\Gamma_{2}$ to the complex plane, with $\Gamma'_{1}$ as all real numbers above 0, $\Gamma'_{2}$ as all real numbers less than 0. The charge $q$ is located at point $i$ on this plane. 

The general conformal map is given as
$$
\begin{align}
t = \frac{az+b}{cz+d}
\end{align}
$$
We want the point $-1$ to correspond to the location $0$ in the new plane, and we want the point $1$ to correspond to infinity. 
$$
\begin{align}
\frac{z+1}{z-1}
\end{align}
$$
We can have a multiplicative constant that we choose - for instance
$$
\begin{align}
-i \frac{z+1}{z-1}
\end{align}
$$
to place the charge at point $i$. 

Circles have
$$
\begin{align}
z=e^{i\theta}
\end{align}
$$
where we have $0<\theta<\pi$ for $\Gamma_{2}$, and $\pi<\theta<2\pi$ for $\Gamma_{1}$.

$$
\begin{align}
t= -i \frac{e^{i\theta}+1}{e^{i\theta}-1}
\end{align}
$$
Lets call this $H(t)$. $\phi=\mathrm{Re}(H)$
![[Pasted image 20261013100555.png]]

We can apply a holomorphic transformation which is not conformal: 

$$
\begin{align}
\xi= t^{\frac{1}{2}}
\end{align}
$$
$$
\begin{align}
t=re^{i\theta} \\
t^{\frac{1}{2}=}\sqrt[]{ r } e^{i \theta/2}
\end{align}
$$
This rotates our axes. the charge $i$ goes to unit distance away at 45 degrees. $\Gamma_{1}''$ is the positive x axis, and $\Gamma_{2}''$ is the positive $y$ axis. Basically - all angles have been halved. 

Now we can use the method of images. We cancel the field with a $-q$ below the $x$ axis, and a $+q$ across the $y$ axis, and then a $-q$ below that to cancel again.
![[Pasted image 20261013100901.png]]


Now we just have to add each of these charges in lns and undo the conformal map.

The $+q$ in the left top plane is $-\xi_{0} ^{*}$, the one in the lower left plane is $-\xi_{0}$, the one in the lower right is $\xi ^{*}$, and the original $q$ is $\xi_{0}$. 

The negative charges are $-\ln$, so they go in the denominator of the log. We have

$$
\begin{align}
\ln  \frac{(\xi-\xi_{0})(\xi+\xi_{0}^{*})}{(\xi-\xi_{0}^{*})(\xi+\xi_{0})}
\end{align}
$$

We have 
$$
\begin{align}
H(t) = \chi(\xi(t)) = -q \ln \frac{(\sqrt[]{ t } -\xi_{0})(\sqrt[]{ t } +\xi_{0}^{*})}{(\sqrt[]{ t } -\xi_{0}^{*})(\sqrt[]{ t } +\xi_{0})}
\end{align}
$$

$$
\begin{align}
\phi=\mathrm{Re} \chi
\end{align}
$$
--- 
