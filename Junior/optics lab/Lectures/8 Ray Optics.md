We've been thinking of wavefronts as surfaces of constant phase. 

Rays are the direction of increasing phase, so the direction that the wavefronts are propagating. (perpendicular to the wavefront plane).


We can build up matrix mechanics to analyze rays

![[Pasted image 20260218100848.png]]

## Straight Propagation 
If we just have a wave propagating, it would do
$\theta_{2}=\theta_{1}$
and
$y_{2}=y_{1}+\tan\theta d$
but if we have a small angle, this just becomes
$$
\begin{align}
\begin{bmatrix}
1 & d\\0 & 1
\end{bmatrix} \begin{bmatrix}
y_{1}\\\theta_{1}
\end{bmatrix} = \begin{bmatrix}
y_{1}+\delta_{1}d\\ \theta_{1}
\end{bmatrix} = \begin{bmatrix}
y_{2} \\ \theta_{2}
\end{bmatrix}
\end{align}
$$

## Planer Mirror
If we have a flat mirror, the event of reflection doesn't change anything - the optical axis is now going backwards, but its just as if it were going forwards. Thus, hitting a flat mirror just has the action
$$
\begin{align}
\begin{bmatrix}
1 & 0\\0 & 1
\end{bmatrix}
\end{align}
$$
## Spherical Mirror
Lets look at a spherical mirror now.

![[Pasted image 20260218101949.png|300]]

We can draw similar triangles for $\theta_{1}$ and $\theta_{2}$. We have a convention that the radius for a concave mirror like this is negative. 

$$
\begin{align}
\phi-\theta_{1}=-\theta_{2}-\phi \\
\theta_{2}=-2\phi+\theta_{1} \\
\theta_{2}\approx -2 \frac{y_{1}}{R}+\theta_{1} \\
\begin{bmatrix}
1 & 0 \\
\frac{2}{R} & 1
\end{bmatrix} \\
\end{align}
$$
## Refraction

Going from $n_{1}\to n_{2}$ on a flat interface:
$$
\begin{align}
y_{2}=y_{1} \\
n_{1}\sin\theta_{1}=n_{2}\sin\theta_{2} \\
n_{1}\theta_{1}=n_{2}\theta_{2} \\
\theta_{2} = \frac{n_{1}}{n_{2}} \theta_{1} \\
\begin{bmatrix}
1 & 0\\ 0  & \frac{n_{1}}{n_{2}}
\end{bmatrix}
\end{align}
$$



Going from $n_{1}\to n_{2}$ on a Spherical interface:
$$
\begin{align}
n_{1} \sin(\theta_{1} \phi)  & = n_{2} \sin(\theta_{2}+\phi) \\
n_{1} \theta_{1} + n_{1} \phi  & = n_{2} \theta_{2} + n_{2} \phi \\
n_{2}\theta_{2} = (n_{1}-n_{2})\phi + n_{1}\theta_{1}
\end{align}
$$
If we assume that $\phi$ is small,
$$
\begin{align}
\sin \phi = \frac{y_{1}}{R}
\end{align}
$$
So we just get
$$
\begin{align}
\theta_{2} = \frac{n_{1}-n_{2}}{n_{2}}\frac{y_{1}}{R} + \frac{n_{1}}{n_{2}}\theta_{1}
\end{align}
$$
So we get the matrix
$$
\begin{align}
\begin{bmatrix}
1 & 0 \\
\frac{n_{1}-n_{2}}{n_{2}} \frac{1}{R} &  \frac{n_{1}}{n_{2}}
\end{bmatrix}
\end{align}
$$

## Thin lens
We can just multiply the results for a concave vs a convex matrix to build it.
For instance, going through a converging lens we have
$$
\begin{align}
\begin{bmatrix}
1 & 0 \\
\frac{n_{2}-n_{1}}{n_{1}R_{2}} & \frac{n_{2}}{n_{1}}
\end{bmatrix}\begin{bmatrix}
1 & 0 \\
\frac{n_{1}-n_{2}}{n_{2}R_{2}} & \frac{n_{2}}{n_{1}}
\end{bmatrix}
\end{align}
$$
We get
$$
\begin{align}
\mathbf{ M} = \begin{bmatrix}
 1 & 0 \\
\frac{n_{2}-n_{1}}{n_{1}}\left( \frac{1}{R_{2}}- \frac{1}{R_{1}} \right) & 1
\end{bmatrix}
\end{align}
$$

We call the lower left element the $-\frac{1}{f}$, where $f$ is the focal length of the lens. 



