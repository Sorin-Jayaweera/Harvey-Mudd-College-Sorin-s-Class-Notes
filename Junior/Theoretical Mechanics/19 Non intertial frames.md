## Transformations
We have nice new coordinate axes, but these are rotating along with the body over time, and we need to translate that back to the regular space frame so that we can describe the equations of motion. 

$$
\begin{align}
\left( \frac{ d \vec{r}}{d t } _{\text{ inertial }}  \right) = \vec{\omega}\times \vec{r}, \left( \frac{ d \vec{r}}{d t } _{\text{ rotating }}  \right) =0 
\end{align}
$$

If we have something that is moving outside of the rotating frame, we'll have a velocity transformation
$$
\begin{align}
\vec{v}_{\text{ inertial }}  & = \vec{v}_{\text{ rotating }} + \vec{V} \\
 & = \vec{v}_{\text{ rotating }} +  \vec{\omega} \times \vec{r}
\end{align}
$$

So in general,
$$
\begin{align}
\frac{ d \vec{r}}{d t }_{\text{ inertial }}  = \frac{ d \vec{r}}{d t } _{\text{ rotating }}  + \vec{\omega}\times \vec{r} 
\end{align}
$$

If we don't have a rigid body, but instead something moving away - this is how we will take account the relative motion.

This is just the velocity transformation, but we care about a lot of things. What about torque or momentum?

Take an arbitrary vector $\vec{A}$, and let it be constant in the rotating frame. On the ground we'll see it moving around, but in its frame it is stationary.

Therefore, it just has
$$
\begin{align}
\frac{ d \vec{A}}{d t } = \vec{\omega}\times \vec{A}
\end{align}
$$
Lets say that $\vec{A}$ has an angle $\theta$ off from vertical. 
$$
\begin{align}
\left| V_{A}  \right| = A\sin\theta \omega
\end{align}
$$
If the $A$ vector is changing, we just have to account for that incremental change.
$$
\begin{align}
d\vec{A}_{\text{ inertial }} = d\vec{A}_{\text{ transformation }} + d\vec{A}_{\text{ rotating frame }}  
\end{align}
$$
We now have a general equation to transform the rate of change for any vector $A$ as how much it is changing in its own frame plus the rotation.
$$
\begin{align}
\frac{ d \vec{A}}{d t }_{\text{ inertial }}  = \frac{ d \vec{A}}{d t } _{\text{ rotating }} + \vec{\omega}\times \vec{A} 
\end{align}
$$

We have a question though: Is the $\vec{\omega}\times \vec{A}$ in the inertial or rotating frame? The distinction between the inertial and rotating frame is in the time derivative. It doesn't matter which coordinate system we represent $\vec{A}$ in, it is the same vector. It only matters when we are asking how it will change in the future, $t+\Delta t$. 

## Pseudoforces
In an inertial frame,
$$
\begin{align}
\vec{F} = \frac{ d \vec{p}}{d t } 
\end{align}
$$

There are 'forces' that we see when we transform from inertial to non inertial frame.
$$
\begin{align}
\frac{ d \vec{P}}{d t }_{\text{ inertial }}  = 0 = \frac{ d \vec{p}}{d t } _{\text{ rotating }} + \vec{\omega}\times \vec{p} \\
\implies \frac{ d \vec{p}}{d t } _{\text{ rotating }} = -\vec{\omega}\times \vec{p}
\end{align}
$$
$$
\begin{align}
\frac{ d \vec{\mathscr{l} }}{d t }_{\text{ inertial }}  = 0 = \frac{ d \vec{\mathscr{l}}}{d t } _{\text{ rotating }} + \vec{\omega}\times \vec{\mathscr{l}} \\
\implies \frac{ d \vec{\mathscr{l}}}{d t } _{\text{ rotating }} = -\vec{\omega}\times \vec{\mathscr{l}}
\end{align}
$$

It is nice to treat these as pseudoforces. Note, they only show up in a co-rotating frame. If the thing is at rest, then there is a force equal to $\vec{\omega}\times \vec{p}$, but otherwise it doesn't exist. 

If angular momentum is conserved in the space frame, it is not conserved in the body frame because we have this pseudo-torque. 

## Dynamics of a point particle in a rotating reference frame

Lets imagine a point particle rotating around the an axis with speed $\omega$.
We want to find the equations of motion in the inertial frame, but expressing it in terms of the easy things to find from the rotating frame.

We have vectors:
$$
\begin{align}
\vec{r},\vec{r}_{rot} \\
\text{ with components in the rotating frame } \\
r_{i}',\dot{r}_{i} '  \\
\text{ and regular inertial frame } \\
r_{i} , \dot{r}_{i} 
\end{align}
$$



$$
\begin{align}
\mathscr{L} = T-U = \frac{1}{2}m \left| \vec{V}_{\text{ inertial }}  \right| ^{2} - u(\vec{r}) \\
\end{align}
$$
We know that
$$
\begin{align}
\vec{V}_{\text{ inertial }} = \left( \frac{ d \vec{r}}{d t }  \right)_{\text{ inertial }} = \left( \frac{ d \vec{r}}{d t }  \right)_{\text{ rotating frame }}  + \vec{\omega}\times \vec{r}
\end{align}
$$
(the rotating reference frame is the one that has the particle look stationary, since the frame is moving with the particle).
This gives us a really nice Lagrangian
$$
\begin{align}
\mathscr{L}  & = \frac{1}{2}m \left| \vec{V}_{\text{ rot }}+\vec{\omega} \times \vec{R}  \right| ^{2} - u(\vec{r}) \\
\mathscr{L}  & = \frac{m}{2}\left| \vec{V}_{\text{ rot }}  \right| ^{2} + \frac{\cancelto{  }{ 2 }m}{\cancelto{  }{ 2 }} \vec{v}_{\text{ rot }} (\vec{\omega}\times \vec{r})+ \frac{m}{2}\left| (\vec{\omega}\times \vec{r}) \right| -u(\vec{r}) \\
 \mathscr{L}& = \frac{m}{2} \left| \vec{V}_{rot}  \right| ^{2} + m \vec{v}_{rot} (\vec{\omega}\times \vec{r}) + \frac{m}{2}\omega^{2}r^{2} - \frac{m}{2}(\vec{\omega}\cdot \vec{r})^{2}-u(\vec{r})
\end{align}
$$

$$
\begin{align}
\mathscr{L} = \frac{m}{2}\sum_{k}^{} \dot{r}^{2}_{k} + m \sum_{k}^{} \dot{r}_{k}' (\vec{\omega}\times \vec{r})_{k} + \frac{m}{2}\omega^{2} \sum_{k}^{} r_{k} '^{2} \\- \frac{m} 
{2}\left( \underbrace{ \sum_{k}^{} \omega_{k} r_{k} 'U }_{ \vec{\omega}\cdot \vec{r} } \right) \sum_{j}^{} \omega _{j}r'_{j} - u(r)
\end{align}
$$
(all that as one equation).

$$
\begin{align}
\frac{ \partial \mathscr{L} }{ \partial  \dot{r}_{i} ' }  & = \frac{n}{2} \sum_{k}^{} \frac{ \partial  }{ \partial  \dot{r}_{i}' } (\dot{r}_{k} ^{2})+ m \sum_{k}^{} (\vec{\omega}\times \vec{r})k \underbrace{ \frac{ \partial  }{ \partial  \dot{r}_{i}' } \dot{r}_{k}' }_{ \delta _{ik} }   \\
 & = m \sum_{k}^{} \dot{r}_{k} \delta _{ik} + m \sum_{k}^{} (\vec{\omega}\times \vec{r}) \delta_{ik} \\
 & = m \dot{r}_{i}' + m (\vec{\omega}\times \vec{r})_{i} 
\end{align}
$$
$$
\begin{align}
\frac{d}{dt} \frac{ \partial \mathscr{L} }{ \partial\dot{r}_{i} } = m\ddot{r}_{i}' + m(\dot{\vec{\omega}}\times \vec{r})_{i} + m(\vec{\omega}\times \vec{v}_{rot} )_{i} = \frac{ \partial \mathscr{L} }{ \partial r_{i} ' } \\  
\end{align}
$$
We now have
$$
\begin{align}
m \ddot{\vec{r}} = - \underbrace{ \vec{\nabla}u }_{ \text{real forces}} - \underbrace{ m(\dot{\vec{\omega}}\times \vec{r}) }_{ \text{ Euler term } } - \underbrace{ 2m(\vec{\omega}\times \vec{v}_{rot} ) }_{ \text{ Coriolis force } } - \underbrace{ m\vec{\omega}\times(\vec{\omega}\times \vec{r}) }_{ \text{ Centrifugal force } }
\end{align}
$$
All of these together are Pseudoforces that arise from taking the rotating frame. Thinking of them as forces lets up think in a typical Newtonian way. We can say $F=ma$, as long as we remember that in addition to the actual forces, we have these pseudo forces from the rotating coordinate frame. 

Lets think about each of these. 

## Euler Term
We are often in a situation where $\dot{\omega}=0$, so this is typically ignored.
Lets imagine that we are on a merry go round which turns on. As we start to spin up into a circle, we fall backwards opposite the direction that it spins. Relative to the rotating thing, we fall backwards. 

## Centrifugal Term
The earths rotation is very constant, we aren't speeding up. This term is for constant speed $\vec{\omega}$.

On earth, we feel gravity going radially inwards as a real force, but the rotation of the earth makes us feel a constant outwards force (not radially out, but perpendicular to the $\vec{\omega}$).

If we imagine hanging a ball from a string, it won't pull straight down to the center of the earth - it will hang very slightly offset because of this.  There are tricky cross product things to do, but we get
$$
\begin{align}
\left| \vec{F}_{c}  \right| = m\omega^{2}R_{\oplus } 
\end{align}
$$
where $R_{\oplus}$ is the radius of the earth. 

$$
\begin{align}
\frac{F_{c}}{F_{grav} }= \frac{m\omega^{2}R_{\oplus }}{m\underbrace{ \frac{GM_{\oplus }}{R_{\oplus }^{2}}   }_{ g }} \\
\frac{F_{c}}{F_{g}} = \frac{\omega^{2}R_{\oplus }^{3}}{GM_{\oplus } } \approx 0.003
\end{align}
$$
This is how much g varies. At the north pole, $g\approx 9.83 \frac{m}{s^{2}}$, whereas at the equator $g = 9.81 \frac{m}{s^{2}}$.

Because of this, the earth is very slightly oblong. This deviation in radius 
$$
\begin{align}
\frac{\delta R}{R_{\oplus } } \approx 0.003
\end{align}
$$
corresponds to $\delta R\approx 20km$.
This is a rough calculation to get the order of magnitude. 
There is a $40km$ difference between the radius of the north pole vs the equator.

## Coriolis Force
Say we have a carousel rotating counterclockwise. If we have a velocity that points radially outwards in the rotating frame, then we'll feel a force clockwise 90 degrees accelerating it. In an inertial perspective, someone near the center of the turn table has a small velocity, but further out things are turning really fast. If we roll out to a larger radius, we send it to a region with a faster rotational velocity. 


