
## Review:
The TISE in 3d for a central potential 
$$
\begin{align}
V(r)= \frac{-ze^{2}}{4\pi\epsilon_{0}r}
\end{align}
$$
$$
\begin{align}
\left[ -\frac{\hbar^{2}}{2mr^{2}}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right)+ \frac{\vec{L}^{2}_{op} }{2mr^{2}} - \frac{ze^{2}}{4\pi\epsilon_{0}r} \right] \psi(r,\theta,\phi)=E\psi(r,\theta,\phi)
\end{align}
$$We separate into two functions
$$
\begin{align}
Y_{n,l,ml} (r,\theta,\phi)= R_{n,l}(r)Y_{l,ml} (\theta,\phi)
\end{align}
$$


We found the Spherical harmonics that have nice eigenvalues. 

Ultimately we got to an expression for the energy eigenvalues,

$$
\begin{align}
E_{n} =-\frac{z^{2}}{2ma_{0}^{2}} \frac{1}{n^{2}} = -\frac{z^{2}e^{4}m}{2(r\pi\epsilon_{0})^{2}\hbar^{2}} \frac{1}{n^{2}}
\end{align}
$$
This is using the definition that 
$$
\begin{align}
a_{0}= \frac{4\pi\epsilon_{0}\hbar^{2}}{me^{2}} \\
a = \frac{a_{0}}{z}
\end{align}
$$
where $z$ is the number of protons

Lets talk more about 
## Quantum Numbers
A set of numbers that uniquely specify the wavefunction for an electron.

We need to specify three things to define our wavefunction: $n,l,m_{l}$. 

We have the restriction that $n \geq l+1$. 
given $l$, $n$ can be $l+1,l+2,\dots$
given $n,l$ can be $0,1,\dots,n-1$.

$n$ is linked to the total energy $E_{n}$. 

Summary:
$n=1,2,3$
$l=0,1,2,\dots,n-1$
$m_{l}=-l,-l+1,\dots,l-1,l = 0 \pm 1 \pm 2\dots\pm l$




## Energy Eigenfunctions

We have the radial eigenfunction
$R_{n_{l},l}= \frac{U_{n,l}(r)}{r}=\underbrace{  N_{n,l} }_{ \text{ normalizaiton } }\underbrace{ r^{l} }_{ r\to 0 \text{ behavior } }\underbrace{ e^{\frac{-zr}{na_{0}}} }_{ r\to \infty \text{ behavior } }\underbrace{ F_{n-(l+1)} }_{ \text{ Polynomial } }$
For example:
$$
\begin{align}
z=1 \\
R_{2,1}=\frac{1}{\sqrt[]{ 3 } } \left( \frac{1}{2a_{0}} \right) ^{\frac{3}{2}} \frac{r}{a_{0}}e^{\frac{-r}{2a_{0}}} \text{ , note: } F_{0} (x)=1 
\end{align}
$$

## Normalization
To normalize we integrate over all of space
$$
\begin{align}
\iiint _{\text{ all space }} \psi ^{*}\psi dv = 1 \\
\to   \int_{\phi=0}^{2\pi} \int_{\theta=0}^{\pi} \int_{r=0}^{\infty} \psi ^{*}\psi r^{2}\sin\theta \, dr \, d\theta \, d\phi
\end{align}
$$
By convention, we will separately normalize the radial and angular parts:

We have $\lvert R \rvert^{2}dr$ as the linear probability density
$$
\begin{align}
\int_{r=0}^{\infty} R_{n,l} (r)^{*}R_{n,lU} (r) r^{2} dr =1
\end{align}
$$

And the angular probability density
$$
\begin{align}
\int_{0}^{2\pi} \int_{0}^{\pi} Y_{l,ml} ^{*}Y_{l,ml} \sin\theta d\theta d\psi = 1
\end{align}
$$

## Experiments
We want to observe the changes in energy when an electron goes from an excited n down to the ground.

It can go from the 2nd state to the first, 3rd to 1st, etc. The photon energy would be
$$
\begin{align}
E_{\gamma} = E_{nh}-E_{nl}= \frac{hc}{\lambda}=h\nu \\
\lambda= \frac{hc}{E_{nh} -E_{nl} } \\
= \frac{91.15 \frac{nm}{z}}{\frac{1}{h_{l} ^{2}}- \frac{1}{n_{h^{2}} }}  
\end{align}
$$
Hydrogen has $z=1$
We can make a table of transitions for hydrogen:
$$
\begin{align}
\begin{bmatrix}
n_{l}  & n_{h}  & \lambda(nm) & | & \text{ color } \\
2 & 3 & 656.3 & | & \text{ red } \\
2 & 5 & 486 & | & \text{ cyan } \\

\end{bmatrix}
\end{align}
$$

