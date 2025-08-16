Useful formulae:
Fourier transforms
$$
\begin{align}
\tilde{E}(kx,ky)=\int_{-\infty}^{\infty}dx \int_{-\int}^{\infty}dy E(x,y)e^{-ikxx}e^{-iky y}
\end{align}
$$

## Plane waves:
If we have a wave moving in any given direction, the wave will travel and appear to be a shifted copy of itself. We can draw a plane aligned with each maximum, and observe that it is moving forwards. 

For these plane waves, we can write a wave equation: $\vec{E}=E_{0}e^{i\vec{k}\cdot \vec{r}}$
$\left| \vec{K}=\frac{2\pi}{\lambda} \right|$
We can Fourier decompose this to be a wave traveling in the z direction (adding in the last term for a wave in z)
$$
\begin{align}
E(x,y) = \int_{-\infty}^{\infty}dk_{x} \int_{-\infty}^{\infty}  dk_{y} e^{i(k_{x}x+k_{y}y)}\lambda \tilde{E}(k_{x},k_{y}) e^{ik_{z}z}
\end{align}
$$
We have the wave number $\left| k \right|^{2}=k_{x}^{2}+k_{y}^{2}+k_{z}^{2}$
So we can plug into the formula
$$
\begin{align}

E(x,y) = \int_{-\infty}^{\infty}dk_{x} \int_{-\infty}^{\infty}  dk_{y} e^{i(k_{x}x+k_{y}y)}\lambda \tilde{E}(k_{x},k_{y}) e^{iz\sqrt{ k^{2}-k_{x}^{2}-k_{y}^{2} }}
\end{align}
$$
We can use the paraxial approximation for $k_{x},k_{y}\ll k$
$$
\begin{align}
\sqrt{ k^{2}-k_{x}^{2}-k_{y}^{2} } & =k\sqrt{ 1-\frac{kx^{2}}{k^{2}} -\frac{k_{y}^{2}}{k^{2}}} \\
 & =k\left( 1-\frac{k_{x}^{2}}{2k^{2}}-\frac{k_{y}^{2}}{2k^{2}} \right)  \\
 & =k-\frac{k_{x}^{2}+k_{y}^{2}}{2k}
\end{align}
$$
This simplifies the last term in the Fourier equation to be 

$$
\begin{align}

E(x,y) = \int_{-\infty}^{\infty}dk_{x} \int_{-\infty}^{\infty}  dk_{y} e^{i(k_{x}x+k_{y}y)}\lambda \tilde{E}(k_{x},k_{y}) e^{iz \left( k-\frac{k_{x}^{2}-k_{y}^{2}}{2k} \right)}
\end{align}
$$
the $izk$ part tells us about the overall phase, whereas the $\frac{k_{x}^{2}+x_{y}^{2}}{2k}$ term tells us about the spatial profile on the screen.

### Fraunhofer diffraction.



### Farfield limit
we have a source, some aperture, and a screen. If the source is close to screen, the distance that any wave going through the aperture is different (since it is proportionally small), so they are out of phase and we can't assume a plane wave. 

If we assume the source is far away, then going through the aperture now has spherical waves. We want to treat these as plane waves, so have to have the screen far away. The  distance must be much larger than the size of the aperture. 

