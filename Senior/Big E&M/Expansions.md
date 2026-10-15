

Lets imagine a region with a density of charges $\rho$. 

The field somewhere far away is
$$
\begin{align}
\int \frac{\underbrace{ \rho(x')dv' }_{ dq' }}{\left| \vec{x}-\vec{x}' \right| }
\end{align}
$$
![[Pasted image 20261013102714.png]]


We taylor expand and keep up to the second order
$$
\begin{align}
\frac{1}{\left| \vec{x}-\vec{x}' \right| } = \frac{1}{\left| \vec{x} \right| }+ \frac{ \partial  }{ \partial x'^{i} } \left( \frac{1}{\left| \vec{x}-\vec{x}' \right| } \right)\bigg|_{x'=0}^{} x'^{i} + \frac{1}{2} \frac{ \partial^{2} }{ \partial x'^{i} \partial x'^{j} } \left( \frac{1}{\left| \vec{x}-\vec{x}' \right| } \right)\bigg|_{x'=0}^{} x'^{i}x'^{j}  
\end{align}
$$

$$
\begin{align}
\frac{ \partial  }{ \partial x'^{i} } \frac{1}{\left| \vec{x}-\vec{x}' \right| } = -\frac{1}{2} \frac{2(x^{'}-x'^{i})}{((x^{j}-x'^{j})^{2})^{\frac{3}{2}}} (-1)
\end{align}
$$

Note that we have sums for three terms because we have repeated indices when we do the square

$$
\begin{align}
\frac{1}{((x^{j}-x'^{j})^{2})^{\frac{1}{2}} }    = \frac{x^{i}}{\left| \vec{x}^{3} \right| } 
\end{align}
$$
$$
\begin{align}
\frac{ \partial^{2} }{ \partial x'^{i}x'^{j} } \frac{1}{\left| \vec{x}-\vec{x}' \right| } = \frac{3x^{i}x^{j}- \left| \vec{x} \right| ^{2}\delta^{ij}}{\left| \vec{x} \right| ^{5}}
\end{align}
$$
$$
\begin{align}
\phi(x) = \frac{Q}{\left| \vec{x} \right| } + \frac{\vec{p}\vec{x}}{\left| \vec{x}^{3} \right| } + \frac{1}{6} \frac{3x^{i}x^{j}- x^{2}\delta^{i j}}{\left| \vec{x} \right| ^{5}} Q_{ij} + \dots
\end{align}
$$


$$
\begin{align}
Q  & = \int\rho(x')dV' \\
\vec{P}  & = \int \rho(x')\vec{x}'dV &  & \text{ the electric dipole } \\
Q_{ij}  & = \int \rho(x') (3x'^{i}x'^{j}- \left| \vec{x}' \right| ^{2}\delta^{i j})dV' &  & \text{ electric quadrapole }
\end{align}
$$

We did a taylor expansion around the origin, and wrote a series of terms. The first term is the total charge sitting at the origin, $\frac{Q}{r}$. This term is usually not there, since materials usually have no net charge. We have a term that falls by $\frac{1}{r^{2}}$ - a dipole. It isn't the electric charge, but the first moment (similar to moment of inertia). It is the average of $x$. It picks up polarity of the charge distribution (its a dipole going from $-$ to $+$ charges). The Quadrapole is the second moment, and is the deviation or variance or smth - its the average of $x^{2}$. 


Lets do a different expansion - spherical coordinates.



$$
\begin{align}
\phi(\vec{x}) = \int \frac{\rho(x')dV'}{\left| \vec{x}-\vec{x}' \right| }
\end{align}
$$

We wrote the expansion for this when we were working on green's functions somewhere. 

Lets write $x\to (r,\theta,\varphi)$ and $\vec{x}'\to (r',\theta',\varphi')$
$$
\begin{align}
\sum_{l=0}^{\infty} \sum_{m=-l}^{l} \frac{4\pi}{2l+1} \frac{1}{r^{l+1}} Y_{lm} (\theta,\varphi) \int\rho(x')r'^{l}Y^{*}_{lm} (\theta',\varphi' )dV'
\end{align}
$$

$$
\begin{align}
q^{*}_{11} = - \sqrt[]{ \frac{3}{8\pi} } (p^{x}-ip^{y})
\end{align}
$$
The power law dependences have to work.
$$
\begin{align}
Q_{ij} \leftrightarrow  q_{2m} 
\end{align}
$$
The trace of $Q$ as a matrix is 0 and it is symmetric, because the $\delta^{i j}$ gives $3$ when we sum over $i$ setting $i=j$, and the expression for $Q$ is equal if we exchange $i,j$. 

