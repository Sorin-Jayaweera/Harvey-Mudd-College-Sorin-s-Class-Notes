![[Pasted image 20251201130831.png]]

![[Pasted image 20251201130843.png]]
![[Pasted image 20251201131051.png]]

## Towards statistical mechanics

Lets consider the shape of a 1-D Pendulum in Phase space. If we start with a box of particles similar trajectories in a circle, those closer in will complete their 'orbit' faster, and further ones slower (same speeds, different lengths). This will sheer the box until it eventually spreads over the whole circle.
![[Pasted image 20251201145824.png|500]]

If we have two 1-D pendulums, then we'll need 4 dimensions to represent them, so lets generally call the area of this box "volume".

In Stat mech, we consider the probability of finding a trajectory in any given cell
$$
\begin{align}
\text{ Prob } = \frac{\Delta \overbrace{ N}^{ \# \text{ of trajectory pts } }}{\Delta \underbrace{ V }_{ \text{ phase space volume } }}
\end{align}
$$
We call this the Phase Space Density $\rho$.

If we generalize to N-D, ($N=2\times \#DoF$)

in 2D we have a circle with

|                                             | 2D                  | 3D                        | N-D                                |
| ------------------------------------------- | ------------------- | ------------------------- | ---------------------------------- |
| <br>A random example of an Enclosed Surface | $x^{2}+y^{2}=R^{2}$ | $x^{2}+y^{2}+z^{2}=R^{2}$ | $\sum_{i=1}^{N}x _{i}^{2} = R^{2}$ |
| "Surface Area"                              | $[m]$               | $[m^{2}]$                 | $[m^{n-1}]$                        |
| "Volume"                                    | $[m^{2}]$           | $[m^{3}]$                 | $[m^{n}]$                          |

In our Phase space, we want to know the probability of finding a trajectory in each cell - the volume is the enclosed volume of one of those cells. 

$[\Delta V ]=[x][p] = [L]$ (angular momentum)
Because of QM we set the minimum at $\frac{\hbar}{2}$. 


In general the phase space density $\rho$ will vary spatially. If we know $\rho$, we can ask what the probability of momentum being between some range would be, because we just have to add up all the $\rho$ for those boxes.

## Equilibrium Statistical Mechanics
$$
\begin{align}
\frac{ d \rho}{d t } =0
\end{align}
$$
This assumes that $\rho$ is uniform throughout space. However, each trajectory is still moving - so the aggregate doesn't depend on time, but we can still have problems. Starting with a uniform $\rho$ everywhere, we would have a big problem if the area of each trajectory expanded. If the warping of our "volumes" (where each radius moves faster or slower) changes the volume, then we no longer have a $\rho$ - but then we wouldn't be in equilibrium. We will show that the volume of any given shape is preserved as we play through time along these trajectories, by using Hamiltonian Mechanics. 



### How do sets of initial conditions evolve over time?
Lets make a set of trajectories and draw the volume between them at two time points

Any points that start within that volume must end within, because trajectories can not cross in phase space AND be unique. 

![[Pasted image 20251201152444.png]]
### Liouville's Theorem
While the boundary bounding a set of points in phase space will, in general, deform - the enclosed volume is constant. All points that lie within must still lie within. 


### 2D "Proof" of Liouville's Theorem
Imagine that we have an arbitrary phase space shape "bob" with volume "volume". How much does the volume change in a time $dt$?  There is a nice geometric intuition here. If we just track points on the boundary than we can see how the volume changes. 

Lets take a trajectory that is moving in phase space with an abstract velocity called $\vec{v}$ (how fast it is traveling in phase space, so $\dot{q}\hat{q}+\dot{p}\hat{p}$).

normal to our surface is a vector $\vec{n}$. If we go perpendicular to that (or just, you know, parallel to the surface) then that trajectory is just moving along the boundary - so it wouldn't change the volume.  The only thing that matters, then, is the velocity normal to the surface. $V$

If the chunk has an incremental length along the side $dA$ and a velocity $v_{\mid\mid}$, then it expands by a volume $dA V_{| |}dt$

We can find the overall change in volume of the surface
$$
\begin{align}
dVol = \underbrace{ \oint  }_{ \text{ surface } } dA V_{| |} dt
\end{align}
$$
This is a spatial integral, so we can pull out $dt$
$$
\begin{align}
\frac{ d \text{ Vol }}{d t } = \oint dA (\vec{v}\cdot \vec{N}) = \oint \vec{v} \cdot \overbrace{ (dA \hat{n}) }^{ \vec{dA} }
\end{align}
$$


Lets look back to ENM Green's theorem:
$$
\begin{align}
\oint_{\text{ surface }}  \vec{E} \cdot d\vec{A} = \int_{\text{ volume }}^{} (\vec{\nabla}\cdot \vec{E})dv
\end{align}
$$
We have similarly
$$
\begin{align}
\int_{\text{ surface }}^{} \vec{v}\cdot d\vec{A} = \int_{\text{ volume }}^{} (\vec{\nabla}\cdot \vec{v})dv
\end{align}
$$
$$
\begin{align}
\frac{ d \text{ vol }}{d t }  & = \int_{\text{ vol }}^{} (\vec{\nabla}\cdot \vec{v})dv \\
 & = \int_{ \text{ volume }}^{} \left[\left( \frac{ \partial  }{ \partial x } \hat{x} + \frac{ \partial  }{ \partial y } \hat{y} \right) \cdot ( \dot{x} \hat{x} + \dot{y} \hat{y}) \right]dV' \\
 & = \int_{}^{} \left(  \frac{ \partial \dot{x} }{ \partial x } + \frac{ \partial \dot{y} }{ \partial y }  \right)d v'
\end{align}
$$



$$
\begin{align}
\frac{ d \text{ Vol }}{d t } = \int_{\text{ vol }}^{} \left[ \frac{ \partial  }{ \partial q } \dot{q} + \frac{ \partial  }{ \partial p } \dot{p} \right]dV' 
\end{align}
$$
Note that
$$
\begin{align}
\dot{q} = \frac{ \partial H }{ \partial p }  \\
\dot{p} = - \frac{ \partial H }{ \partial q } 
\end{align}
$$
So we have
$$
\begin{align}
\frac{ d \text{ vol }}{d t } = \int \left[  \frac{ \partial^{2}H }{ \partial q \partial q } - \frac{ \partial^{2}H }{ \partial p\partial q  }  \right] dV
\end{align}
$$

If we plug in one of the most common Hamiltonians, we don't get continuous derivatives that we can successively take, so the expression is $0$.
$$
\begin{align}
H = \frac{p^{2}}{2m} + \frac{GMm}{r}
\end{align}
$$


For some Hamiltonians, when you take $\frac{ \partial H }{ \partial p }$ you still have $p$ and $r$ in it.
$$
\begin{align}
H = \frac{P_{\phi} ^{2}}{2mr^{2}} + u
\end{align}
$$
However, it doesn't matter the order that we take these derivatives, it gets the same answer - so
$$
\begin{align}
\frac{ d \text{ vol }}{d t } = 0
\end{align}
$$
 always.


 



