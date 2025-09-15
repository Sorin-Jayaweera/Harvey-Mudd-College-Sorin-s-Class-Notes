
Lets do a basic problem. Consider throwing a mass $m$ into the air. The solution for height $z(t)= z_{0}+v_{0}t-\frac{1}{2}gt^{2}$

We know that this just looks like a parabola, quadratic in time.
This is normally easily solvable *by hand*, but that is not the case for most problems -- we use numerical integration. 
________________________________________________________

Lets look at some approaches. 

## Newtonian Approach
This is **NOT** a stable numerical scheme, but is good for an initial intuition. The errors get smaller with timestep and go to zero with continuity. However, there are better algorithms that perform well without going to infitesimal  timestep.  

We have an initial z and v. From there, we can integrate.
$$
\begin{align}
\ddot{z}=-g \\
\frac{ d ^{2}}{d t^{2} }z = \frac{ d }{d t } \left( \underbrace{ \frac{ d z}{d t }  }_{ V } \right) = -g 
\end{align}
$$
The mathematical trick is to call the inner $\frac{ d }{d x }$ "v"

$$
\begin{align}
\frac{ d z}{d t } =v \\
\frac{ d v}{d t } = -g
\end{align}
$$
We've replaced one second order differential equation with two coupled differential equations. We have one time derivative of two variables, instead of two time derivatives of one. 

We can divide into finite time steps $\Delta t$, which is integrable.

$$
\begin{align}
\Delta z & = \frac{ d z}{d t } \Delta t = v\Delta t \\
\Delta v  & =\frac{ d v}{d t } = -g\Delta t
\end{align}
$$

This always works, its **"Local"** - i.e. each t gets the forces and updates the position and velocity. This is why we have to specify the initial position and velocity. 

## Lagrangian Approach

This is VERY different, not subtly. 

Instead of the first velocity and position, lets take our boundary conditions to be the initial and final position. This is still enough information to get by. 

To do this, we consider different paths. 

### Definitions
The **Lagrangian** is a *scaler* that depends on the point along the path, given by
$$
\mathscr{L}(z,\dot{z},t) = \underbrace{ T }_{ kinetic }-\underbrace{ U }_{ potential }
$$
The lagrangian is different at each part of the field (region where we are considering paths). It could be negative.

We also define action as the integral of lagragians.
**Action**: 
$$
S = \int_{t_{i}}^{t_{f}} \mathscr{L}(z,\dot{z},t)dt
$$
We evaluate the action for each path to get a scaler, "ranking them". The smallest number is the actual one! Black magic!

The amazing thing is the rules of this game:
1) The true path will have the least action
	1) Its actually extremizing the action, but we don't care about that now. No maximums - only min.
2) The path that minimizes the action S satisfies the "Euler-Legrange" equation

The Euler-Legrange is
$$
\begin{align}
\frac{ d \mathscr{L} }{d z } = \frac{ d }{d t } \left( \frac{ d \mathscr{L} }{d \dot{z} }  \right)
\end{align}
$$
