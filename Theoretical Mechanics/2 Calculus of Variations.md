Lets work on the first problem in the pset. 

We have a thing falling with g from rest from z = 0
$$
\begin{align}
\ddot{z} = -g \\
\dot{z} = -gt \\
z = -\frac{1}{2}gt^{2}
\end{align}
$$

Lets write down the Lagrangian.
$\mathscr{L}(z,\dot{z},t)= T-U$
Here, this is
$$
\begin{align}
\mathscr{L}= \frac{1}{2}m\dot{z}^{2}- mgz
\end{align}
$$
Thus $T-U$ is kind of weird, its definitely not a conserved quantity. In some sense, this is only a function of time,


Lets take a legrangian and taylor expand around it, only keeping the first order terms
$$
\begin{align}
\mathscr{L}(z_{0}(t)\Delta z,\dot{z}_{0}(t) + \Delta \dot{z}(t), t  ) = \\
 \mathscr{L}(z_{0}(t),\dot{z_{0}},t) + \frac{ d \mathscr{L}}{d z } \Delta z(t) + \frac{ d L}{d \dot{z} } \Delta(\dot{z})(t)
\end{align}
$$
Lets find the minimum. At extrema, there will be no change (to first order) for any change in the path. So, we can write

$$
\begin{align}
\int_{t_{i} }^{t_{f} } \mathscr{L}(z_{0}+\Delta z, \dot{z}_{0} +\Delta z, t) dt - \int_{t_{i} }^{t_{f}} \mathscr{L}(z_{0},\dot{z_{0}},t)dt = \int_{t_{i} }^{t_{f} } \frac{ d L}{d z } \Delta z(t) + \frac{ d \mathscr{L}}{d \dot{z} } \Delta \dot{z} dt \\ 
\end{align}
$$
For the path that minimizes the action $S$, we have that the first order change is zero, so
$$
\begin{align}
0  & = S[z_{0} +z, \dot{z_{0}}+\Delta \dot{z},t]- S[z_{0},\dot{z_{0}},t]  \\
 & = \int_{t_{i}}^{t_{f}} \bigg[ \frac{ d \mathscr{L}}{d z }\Delta z + \frac{ d \mathscr{L}}{d \dot{z} }   \bigg] dt
\end{align}
$$

Lets massage this by doing a side tour. We have derivatives in both $\Delta z$ and $\Delta \dot{z}$. We can use integration by parts to *rewrite* this to be both in $\Delta z$.
$$
\begin{align}
\int_{t_{i} }^{t_{f} } A \frac{ d }{d t } (\Delta z)dt = A (\Delta Z)\bigg|_{t_{i} }^{t_{f} } \\
\int_{t_{i} }^{t_{f} } \frac{d}{dt} \left( \frac{ d \mathscr{L}}{d \dot{z} } \Delta z \right) dt  
\end{align}
$$
We want to manipulate this to take the derivative. Lets do the chain rule.
$$
\begin{align}
\int \frac{d}{dt} \left( \frac{ d \mathscr{L}}{d \dot{z} }  \right) + \frac{ d \mathscr{L}}{d \dot{z} } \frac{d}{dt} (\Delta z)dt
\end{align}
$$
We can do integration by parts:
UV - Vdu
$$
\begin{align}
\left( \frac{ d \mathscr{L}}{d \dot{z} }  \Delta z\right) \bigg|_{t_{i} }^{t_{f} } - \int_{t_{i} }^{t_{f} } \frac{ d }{d t } \left(  \frac{ \partial \mathscr{L} }{ \dot{\partial}z }  \right) \Delta z dt 
\end{align}
$$

At the endpoints, $\Delta z$ has to be zero - its an offset from the path, but the start and endpoints still have to agree. This cancels out the left portion. 

We can take the condition for zero from earlier to get
$$
\begin{align}
-\int_{t_{i} }^{t_{f} } \frac{d}{dt} \left( \frac{ d \mathscr{L}}{d \dot{z} }  \right)\Delta z dt = \int_{t_{i} }^{t_{f} } \frac{ d L}{d \dot{z} } \Delta \dot{z}dt
\end{align}
$$
Now we can go back to our action principle, and rewrite it in terms of just $\Delta z$ instead of $\dot{\Delta}z$. 

We have
$$
\begin{align}
0 = \int_{t_{i} }^{t_{f} } \left[  \frac{ d \mathscr{L}}{d z } - \frac{d}{dt} \left( \frac{ d \mathscr{L}}{d \dot{z} }  \right) \right]\Delta z \,  dt
\end{align}
$$
We can call the left side $f(t)$, and just say
$$
\begin{align}
0 = \int_{t_{i} }^{t_{f} } f(t)\Delta z(t)dt
\end{align}
$$
Must $f(t)$ integrate to zero? 

For any $f(t)$ we can surely make some $\Delta z(t)$ that make the whole system integrate to zero. BUT! This must evaluate to zero for *all* $\Delta z$ that are local.

If we have some value in $f(t)$, then we can choose some $\Delta z(t)$ that makes it not evaluate to zero. Therefore, the only case where there can be no conspiring bad actors that can choose anything is to set $f(t) = 0$.

This, this is what gives us the beautiful Euler-Lagrange equation.
$$
\boxed{
\begin{align}
\frac{ d \mathscr{L}}{d z } - \frac{d}{dt} \frac{ d \mathscr{L}}{d \dot{z} }  = 0
\end{align}
}
$$

This is really easy to extend into other dimensions, we would just add on another set of equation:
$$
\begin{align}
\frac{ d \mathscr{L}}{d x } - \frac{d}{dt} \frac{ d \mathscr{L}}{d \dot{x} }  = 0
\end{align}
$$
and so on for any variable. This gives us the entire equations of motion by just some simple derivatives. We will use this all the time. 


## Shortest path between two points

In a Euclidian space, we can prove that the shortest path between points is a line. We can extend this approach for geodesic spheres, etc. 

Lets do this.
![[Pasted image 20250827154643.png]]
We can see some analogies to the previous problem.
We have analogies
$$
\begin{align}
\begin{bmatrix}
\text{ Path } & z(t) & y(x) \\
\text{ "time" } & t & x \\
\text{ "Position" } & z & y \\
\text{ Slope } & \dot{z} & y' = \frac{ d y}{d x }  \\
\text{ Action } & S[z(t)] & S(y(x))
\end{bmatrix}
\end{align}
$$


We have tiny lengths of a segment 
$$
\begin{align}
ds = \sqrt[]{ dx^{2}+dy^{2} }  \\
ds = dx \sqrt[]{ 1+ \left( \frac{dy}{dx}  \right)^{2} } 
\end{align}
$$

Before we had $\int_{t_{i}}^{t_{f}}\mathscr{L}dt$, and now we have
$\int_{t_{i}}^{t_{f}}ds =   \int_{x_{i}}^{x_{f}} (1+y'^{2})^{\frac{1}{2}}ds$.

where $\mathscr{L}$ is now $(1+y'^{2})^{\frac{1}{2}}$.

The eqn:
$$
\begin{align}
\frac{ d \mathscr{L}}{d y } - \frac{ d }{d x } \left( \frac{ d \mathscr{L}}{d y' }  \right)=0 \\
0 = \frac{d}{dx} \left( \frac{1}{2}(1+y'^{2})^{\frac{-1}{2}}(2y') \right) \\
0 = \frac{d}{dx} \left( \frac{y'}{\sqrt[]{ 1+y'^{2} } } \right) \\
\frac{y'}{\sqrt[]{ 1+y'^{2} } } = D  & \text{ (constant) }
\end{align}
$$

This tells us that $$
\begin{align}
\frac{dy}{dx} = Constant 
\end{align}
$$
## Brachistochrone Problem

Lets find the optimal ramp to roll something down. This minimizes the travel time T.

$$
\begin{align}
T = \int_{x_{i} }^{x_{f} } dt = \int_{x_{i} }^{x_{f} } \frac{ds}{v}
\end{align}
$$
Lets solve the Brachistochrone problem!
