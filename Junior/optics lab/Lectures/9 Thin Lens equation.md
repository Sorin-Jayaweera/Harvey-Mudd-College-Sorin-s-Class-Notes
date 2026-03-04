## Converging Lens
We got to the thin lens equation
$$
\begin{align}
\frac{1}{f} = \frac{1}{d_{0}}+ \frac{1}{di}
\end{align}
$$
There is a magnification
$$
\begin{align}
\frac{y_{i}}{y_{0} } = -\frac{d_{i}}{d_{0}}
\end{align}
$$


The focal point is only the place where a focus shows up when the $d_{0}$ is $\infty$. If the rays are parallel,$\frac{1}{d_{0}}\implies 0$ $\frac{1}{d_{i}}=\frac{1}{f}$ 

As the actual object is infinitely far away, diverging rays would miss the lens since small angles still make large differences as you go far - so the ones that hit have diverged so little that they are basically parallel. 

In that limit, the magnification goes to zero - so an image is infinitely small. Similarly, a collimated beam (near planar wavefronts) would be focused to a spot $f$ downstream. 

## Virtual Images
For a diverging lens, the thin lens equation still applies:
$$
\begin{align}
\frac{1}{f} = \frac{1}{d_{0}}+ \frac{1}{d_{i}}
\end{align}
$$
The image isn't going to be in focus anywhere after the camera, but they look like they converged before the lens (ray trace). Because they focus to a point before the lens, that focus point is a virtual image. 

We can do the same with a converging lens - if we have a larger positive $\frac{1}{d_{0}}$ (very small $d_{0}$) then $d_{i}$ will have to be negative to get to the focus. The rays diverge quite a bit -- even though the lens bends the rays inwards, its not enough to make them form a real image. There is still a virtual image happening before the lens. 



We can do matrix mechanics for a ray coming in at $d_{0}$, then hitting a lens with focus $f$, then traveling a distance $d_{i}$. 
$$
\begin{align}
 & \begin{bmatrix}
1 & d_{i} \\
0 & 1
\end{bmatrix}\begin{bmatrix}
1 & 0 \\
-\frac{1}{f} & 1
\end{bmatrix} \begin{bmatrix}
1 & d_{0} \\ 0 & 1
\end{bmatrix} \\
 & = \begin{bmatrix}
 1 & d_{i} \\
0 & 1
\end{bmatrix} \begin{bmatrix}
1 & d_{0} \\
-\frac{1}{f} & -\frac{d_{0}}{f}+1
\end{bmatrix} \\
 & \begin{bmatrix}
1- \frac{d_{i}}{f} & d_{0} - \frac{d_{i}d_{0}}{f}+d_{i} \\
-\frac{1}{f} & - \frac{d_{0}}{f}+ 1
\end{bmatrix}
\end{align}
$$
This tells us that
$$
\begin{align}
y_{i} = \left( 1- \frac{d_{i}}{f} \right)y_{0} + \theta _{i}\left( d_{0} - \frac{d_{i}d_{0}}{f} + d_{i} \right)
\end{align}
$$

If someone is infinitely far away, the rays from them are parallel - if they're closer than the rays are diverging a bit. We can imagine a "further than infinite away" by putting another converging lens in front of it. The image would form less than $f$ downstream - still downstream, but closer to the lens. 


A real image forms the image downstream of the lens.
A virtual image forms upstream of the lens, because rays angle out after the lens.

A real object is where light rays come from upstream and the rays spread out. 
A virtual object has light rays angled as if they are converging on (or if time reversed, diverging from) the "object". 


## How do camera lenses work? Eyes?
Our eyes can squish down or relax on the internal lens - curvier lenses focus closer. Let there be light!

If you are near sighted - you can can only see things that are close enough. Your eye ball is very long, so light converges too early (the material thickens). OR, your relaxed lens is still too powerful to get light, and focuses it earlier. 

What about being farsighted? 
You can see things far away, but have a "near point" where nothing can focus if it is closer. The relaxed lens of your eye focuses things further back than the retina. The natural relaxed lens is too flat, and/or the eyeball is too shallow. You can just squish down on the lens to get a better focal length - your muscles are just too weak to do it, you just can't use your relaxed eye to see things. There is a limit to how much you can squish, so the image is still too far away. 

For farsightedness, a converging lens is put super close to the eye - this makes a virtual image (from the point of view of the corrective lens) - which makes a real object on your eye lens, which makes a real image at your eye sensors. 


As you get older, things in your body become harder and less flexible. The squishing of the muscle for the lens of your eye doesn't bend light as well as it used to. 

## Abberation

The simple way is to use a curved mirror to focus in reflection instead of a refractive element - curved mirrors, not refractive lenses. Also, spheres are bad at the small angle approximation, parabolas are much better. 
How do we correct chromatic abberation 
