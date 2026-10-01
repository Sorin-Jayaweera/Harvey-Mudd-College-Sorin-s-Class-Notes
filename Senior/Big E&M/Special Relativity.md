
>[!danger]+ Big Ideas
>We have 4 vector objects $k^{\mu}$ which must satisfy $k^{\mu'}=\Lambda k^{\mu}$
>where $\Lambda$ is the lorentz transformation satisfying
>$\hat{\Lambda}^{-1}\eta \hat{\Lambda}= \eta$ 
>where $\eta$ = $\begin{bmatrix}-1&0&0&0\\0&1&0&0\\0&0&1&0\\0&0&0&1\end{bmatrix}$ 
>The lorentz transformation as a matrix represents a hyperbolic rotation (if the movement is only on two axis - 1 space and time), and can be written as a sum or a matrix in two equivalent ways:
>$X^{\nu'}= \sum_{N=0}^{3}\Lambda^{\mu'}_{\mu}x^{\mu}=\Lambda^{\mu'}_{\mu}x^{\mu}$
>$=\Lambda_{0}^{1'}x^{0}+ \Lambda_{1}^{'}x^{1} + \dots$ 


---
If we have a moving object with its personal frame $\Theta'$ and a lab frame which is static $\Theta$, then we can transform between the coordinates
$$
\begin{align}
\underbrace{ x }_{ x^{1'} }'  & = \gamma_{v} (x-Vt) = \gamma_{v} \left( \underbrace{ x }_{ x^{1} }- \frac{V}{c} \underbrace{ ct }_{ x^{0} } \right)  \\
y' & =y \\
z' & =z \\
ct' & = \gamma_{v} \left( \underbrace{ ct }_{ x^{0} }- \frac{V}{c} \underbrace{ x }_{ x' } \right)
\end{align}
$$
Lets define $\frac{V}{c}= \beta_{V}$
as a matrix, we can write this as
$$
\begin{align}
\begin{pmatrix}
x^{0'}\\ x^{1'} \\ x^{2'} \\ x^{3'}
\end{pmatrix} = \begin{pmatrix}
\gamma_{v}  & - \beta \gamma_{v}  & 0 & 0 \\
-\beta \gamma_{v}  & \gamma_{v}  & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix} \begin{pmatrix}
x^{0}\\ x^{1}\\ x^{2}\\ x^{3}
\end{pmatrix}
\end{align}
$$

As short hand, we just write
$$
\begin{align}
\begin{pmatrix}
x^{0'}\\ x^{1'}
\end{pmatrix} = \gamma_{v} \begin{pmatrix}
1 & -\beta \\ -\beta & 1
\end{pmatrix} \begin{pmatrix}
x^{0}\\x^{1}
\end{pmatrix}
\end{align}
$$
This looks like the rotation matrix, but because we have two negative signs on the off diagonals its a hyperbolic rotation instead of a circular one. It looks like
$$
\begin{align}
\begin{pmatrix}
x' \\
y'
\end{pmatrix} =  \begin{pmatrix}
\cosh \xi & \sinh \xi \\
\sinh \xi & \cosh \xi
\end{pmatrix}
\end{align}
$$
---

We have momentum 4-vector
$$
\begin{align}
P = m\underbrace{ U }_{ \text{ energy } }^{\mu}
\end{align}
$$
$U = \gamma_{v}mc^{2}$

$$
\begin{align}
P^{\mu'} & = \lambda^{\mu'}_{\mu} P^{\mu} \\
P^{\mu} & = (P^{0},P^{1}, P^{2}, P^{3}) \\
 & = \left( \underbrace{ m \gamma_{v} }_{ \frac{U}{c} }c,\underbrace{  m \gamma_{v} \vec{V} }_{ \vec{P} }  \right)
\end{align}
$$

