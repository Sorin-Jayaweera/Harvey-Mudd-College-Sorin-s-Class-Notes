Note the vector identity
$$
\begin{align}
(\vec{a}\times  \vec{b}) \cdot (\vec{a}\times \vec{b}) = \left| a \right|^{2} \left| b \right| ^{2} - (\vec{a}\cdot \vec{b})^{2}
\end{align}
$$
Today, we will think about rotations about an axis that changes where it is. Normally we could choose a fixed point or the center of mass and just find the moment of inertia, but if the axis changes then we have to deal with more.

We can write the kinetic energy for all chunks of mass over a large body as
$$
\begin{align}
T = \sum_{\alpha}^{} \frac{1}{2} \Delta m_{\alpha} \vec{\dot{r}}_{\alpha}^{2} \\
T = \sum_{\alpha}^{} \frac{1}{2} \Delta m_{\alpha} (\dot{\vec{R}}+\dot{\vec{\mathscr{r} _{\alpha} }})^{2} \\ \\

\end{align}
$$

where $R$ is the center of mass / any arbitrary point that we want to label (translation) and $\mathscr{r}$ is the vector from the center of mass to that particular chunk of mass (rotation).
$$
\begin{align}
\dot{\vec{r_{\alpha} }} = \dot{\vec{R}}+\dot{\vec{\mathscr{r} }}
\end{align}
$$
We have the assumption for rigid bodies that $\mathscr{r}$ is constant - the distance between the point and the center of mass is the same. It might be rotating about, but always the same distance - we aren't sheering or pulling or morphing the shape. 
$$
\begin{align}
\frac{d}{dt} \left| \mathscr{r}_{\alpha}   \right| =0
\end{align}
$$
Note again this is the *magnitude*, since the angle is rotating and doing complicated things. 

If we assume rotation about an arbitrary axis with motion vector $\vec{\omega}$, then $\dot{\mathscr{r}}_{\alpha} = \vec{\omega}\times \vec{\mathscr{r}_{\alpha}}$
So we get
$$
\begin{align} 
T = \sum_{\alpha}^{} \frac{1}{2} \Delta m_{\alpha} (\dot{\vec{R}}+ (\vec{\omega}\times  \vec{\mathscr{r}}_{\alpha}  ))^{2} 

\end{align}
$$

Therefore,
$$
\begin{align}
T = \frac{1}{2} \sum_{\alpha}^{} \Delta m_{\alpha} [\underbrace{ \left| \dot{R} \right| ^{2} }_{ T_{1} }+\underbrace{ 2\dot{\vec{R}}\cdot(\vec{\omega} \times   \vec{\mathscr{r} }_{\alpha} ) }_{ T_{2} }+ \underbrace{ (\vec{\omega}\times  \vec{\mathscr{r }}_{a} )\cdot(\vec{\omega}\times  \vec{\mathscr{r }}_{a} ) }_{ T_{3} }]
\end{align}
$$
Lets find these
$$
\begin{align}
T_{1} = \frac{1}{2}\sum_{\alpha}^{} \Delta m_{\alpha} \left| \dot{\vec{R}} \right| ^{2} \\
= \frac{1}{2} \left| R \right| ^{2} \sum_{\alpha}^{} m_{\alpha}  \\
= \frac{1}{2}M \left| \vec{V} \right| ^{2}  
\end{align}
$$
This is the linear velocity of the entire shape

We also have
$$
\begin{align}
T_{2} = \frac{1}{2} \sum_{\alpha}^{} \Delta m_{\alpha} 2 \dot{\vec{R}}\cdot(\vec{\omega}\times   \vec{\mathscr{r} }_{\alpha} ) \\
 = \dot{\vec{R}} \cdot \left( \sum_{\alpha}^{}  \right) \Delta m_{\alpha} (\vec{\omega} \times  \mathscr{\vec{r}_{\alpha} } ) \\
= \dot{\vec{r}} \cdot \left[ \vec{\omega}\times  \sum_{\alpha}^{} \Delta m_{\alpha} \vec{\mathscr{r}  }_{\alpha}  \right]
\end{align}
$$
Lets use the fact that
$$
\begin{align}
\mathscr{\vec{r}} = \vec{r}_{\alpha} - \vec{R}
\end{align}
$$
This gets us
$$
\begin{align}
T_{2}  = \dot{\vec{R}} \cdot \left[  \vec{\omega} \times  \sum_{\alpha}^{} (\Delta m_{\alpha} \vec{r}_{\alpha} )- \Delta m_{\alpha} \vec{R}\right] \\
\dot{\vec{R}}\cdot \left[ \vec{\omega} \times  \left\{ M\sum_{\alpha}^{} \underbrace{ \Delta m_{\alpha} \frac{\vec{r}_{\alpha}}{M} }_{ \vec{R}_{\text{ com }}  } - M \vec{R} \right\} \right] \\
T_{2} = M \dot{\vec{R}} \cdot [\vec{\omega}\times  (\vec{R}_{com} - \vec{R})] \\
\end{align}
$$
$T_{2}$ is all the cross terms between the rotation and translation energy. 
The cross terms vanish if any of three conditions are satisfied:
1) The special point is the center of mass, so $\vec{R}_{com}=\vec{R}$.
2) Not rotating, $\vec{\omega}=\vec{0}$.
3) No Translation, so $\dot{\vec{R}}=0$.

We have two good choices for where we want our reference point: 
1) Any fixed points that the object is rotating around
2) any points that are not rotating

$$
\begin{align}
T_{rot} &  = \frac{1}{2}\sum_{\alpha}^{} \Delta m_{\alpha} (\vec{\omega}\times   \vec{\mathscr{r} }_{\alpha} )\cdot(\vec{\omega}\cdot  \vec{\mathscr{r} }_{\alpha} ) \\

T_{rot} &  = \frac{1}{2}\sum_{\alpha}^{} \Delta m_{\alpha} \bigg[ \vec{\omega}^{2} \left| \vec{\mathscr{r} }_{\alpha}  \right| ^{2} - (\vec{\omega}\cdot  \vec{\mathscr{r} }_{\alpha} )^{2} \bigg]   \\
\vec{\omega}\cdot  \vec{\mathscr{r}} & = \omega_{1} \mathscr{r}_{\alpha,1}+\omega_{2} \mathscr{r}_{\alpha,2}+\omega_{3} \mathscr{r}_{\alpha,5} \\
(\vec{\omega}\cdot  \vec{\mathscr{r}}_{\alpha} )  & = \sum_{i=1}^{3} \omega_{i} \mathscr{r}_{\alpha,i} \\
(\vec{\omega}\cdot  \vec{\mathscr{r}}_{\alpha} )^{2}  & = \left( \sum_{i=1}^{3}  \omega_{i} \mathscr{r} _{\alpha,i} \right)\left( \sum_{j=1}^{3}  \omega_{j}  \mathscr{r} _{\alpha,j} \right)  \\
 & = \sum_{ij}^{} \omega_{i} \omega_{j} \mathscr{r} _{\alpha,i} \mathscr{r} _{\alpha,j} \\
\left| \vec{\omega} \right| ^{2} &  = \vec{\omega}\cdot \vec{\omega}  \\
 & = \sum_{i=1}^{3} \omega_{i} \omega_{i} = \sum_{ij}^{} \omega_{i} \omega_{j} \delta_{ij}  
\end{align}
$$
Substituting in these simplifications, we get:
$$
\begin{align}
T_{rot}  & = \frac{1}{2} \sum_{\alpha}^{} \Delta m_{\alpha} \left[ \sum_{ij}^{} (\omega_{i} \omega_{j} \delta_{ij} \left| \mathscr{r} _{\alpha}  \right| ^{2} - \omega_{i} \omega_{j} \mathscr{r} _{\alpha,i} \mathscr{r} _{\alpha,j} ) \right] \\
 & = \frac{1}{2}\sum_{ij}^{} \omega_{i} \omega_{j} \sum_{\alpha} \Delta m_{\alpha} ( \left| \mathscr{r} _{\alpha} ^{2}\delta_{ij} - \mathscr{r} _{\alpha,i} \mathscr{r} _{\alpha,j}  \right| ) 
\end{align}
$$
This looks like moment of inertia, recall that this was:
$$
\begin{align}
I &  = \sum_{\alpha}^{} \Delta m_{\alpha} r_{\perp} ^{2} \\
T_{rot}  & = \frac{1}{2}I\omega^{2} 
\end{align}
$$

We now define a moment of inertia tensor, $\mathbf{I}_{ij}$.
$$
\begin{align}
\mathbf{I}_{ij} = \sum_{\alpha}^{} \Delta m_{\alpha} ( \left| \vec{\mathscr{r} }_{\alpha}\right|^{2} \delta _{ij}- \mathscr{r} _{\alpha i} \mathscr{r} _{\alpha j}    )
\end{align}
$$
In the continuous limit, this becomes
$$
\begin{align}
\iiint_{vol} \Delta m_{\alpha} (\left| \vec{\mathscr{r} }  \right| ^{2} \delta _{ij} - \mathscr{r} _{ i}\mathscr{r} _{j}  )  
\end{align}
$$


If we write a matrix to represent any arbitrary rotation between two axes $\mathbb{W}$ 
$$
\begin{align}
T_{rot} = \frac{1}{2} \sum_{ij}^{} \omega _{i} \mathbf{I}_{ij} \omega _{j} \\
= \frac{1}{2} \mathbb{W}^{T} \mathbf{I} \mathbb{W}
\end{align}
$$
How should we think about the inertia tensor, and how do we calculate it?
$$
\begin{align}
\mathbf{I } = \begin{pmatrix}
I_{xx}  &  I_{xy}  & I_{xz} \\
I_{yx}  &  I_{yy}  & I_{yz} \\
I_{zx}  &  I_{zy}  & I_{zz} \\
\end{pmatrix}
\end{align}
$$

$$
\begin{align}
I_{xx} =   \iiint dm (\left| \mathscr{r}  \right| ^{2})\underbrace{ \delta_{xx} }_{ 1 } -  \underbrace{ \mathscr{r} _{1} \mathscr{r} _{1}  }_{ xx }
\end{align}
$$
So we have 
$$
\begin{align}
I_{x x}  & = \iiint dm (x^{2}+y^{2}+z^{2}-x^{2}) \\
 & = \iiint dm r_{\perp} ^{2} 
\end{align}
$$
This is the typical moment of inertia for rotations about the x axis. Because of the delta function, we'll have zeros  on the non diagonal terms, so we have
$$
\begin{align}
\mathbf{I} = \begin{pmatrix}
\iiint dm \, (y^{2}+z^{2}) & \iiint -xy \, dm  & \iiint -xz\,  dm   \\
 \iiint -yx\, dm& \iiint dm \, (x^{2}+z^{2}) & \iiint -yz \, dm \\
 \iiint -zx\, dm& \iiint -zy\, dm & \iiint dm \, (x^{2}+y^{2})
\end{pmatrix}
\end{align}
$$
Note that this matrix is symmetric and real, so it is also Hermitian.

The normal modes of this rotational matrix tell us dynamics of rotation, in a similar way to how normal modes of $\mathbb{M}\text{ and } \mathbb{K}$ helped.
