
First, lets think of an example from last class - the bead on a rotating hoop. If we change to the inertial frame in lock step with the rotation, then we'll have a normal force 
$$
\begin{align}
F_{in} =- N\sin\theta  = -m\omega^{2}R\sin\theta
\end{align}
$$
Then we can fix the Lagrangian expression by appending
$\mathscr{L} = T-U -m\omega^{2}R\sin\theta$


## Coordinates



If the Hamiltonian is time independent, then 
$H = T+U$.

We have the more general expression, for definitionally the Hamiltonian as,
$$
\begin{align}
\sum_{k}^{} \frac{ \partial \mathscr{L} }{ \partial \dot{q}_{k}  } \dot{q}_{k}  - \underbrace{ (T-U) }_{ \mathscr{L} }
\end{align}
$$
$H=T+U$ if 
$$
\begin{align}
\sum_{k}^{} \frac{ \partial \mathscr{L} }{ \partial \dot{q}_{k}  } \dot{q}_{k} = 2T 
\end{align}
$$

Lets do a transformation for 3d that takes
$(x,y,z)$ as functions of $(q_{1},q_{2},q_{3})$.

Lets define one coordinate system
$$
\begin{align}
r_{1}(t)  & = x(t)  = f_{1}(q_{1}(t),q_{2}(t),q_{3}(t),\cancelto{ 0 }{ t })\\
r_{1}(t)  & = y(t)  = f_{2}(q_{1}(t),q_{2}(t),q_{3}(t),\cancelto{ 0 }{ t })\\
r_{1}(t)  & = z(t)  = f_{3}(q_{1}(t),q_{2}(t),q_{3}(t),\cancelto{ 0 }{ t })
\end{align}
$$


One easy example of this is 
$$
\begin{align}
x = r\sin\theta \cos \phi \\
y = r\sin\theta \sin \phi \\
z = r\cos\theta
\end{align}
$$

Our kinetic energy in this new coordinate system is
$$
\begin{align}
T = \frac{1}{2} (\dot{r}_{1} ^{2} + \dot{r_{2}}^{2}+ \dot{r_{3}}^{2} ) = \frac{m}{2 } \sum_{n=1}^{3} \dot{r}_{n} ^{2} 
\end{align}
$$

We can write that generally
$$
\begin{align}
\dot{r_{n}}  & = \frac{ \partial f_{n}  }{ \partial q_{1} } \dot{q_{1}} + \frac{ \partial f_{n}  }{ \partial q_{2} } \dot{q_{2}} + \frac{ \partial fn }{ \partial q_{3} } \dot{q_{3}} + \cancelto{ 0 }{ \frac{ \partial fn }{ \partial t }  } \\
 & = \sum_{i=1}^{3}  \frac{ \partial f_{n}  }{ \partial q_{i}  } \dot{q_{i} }
\end{align}
$$
so

$$
\begin{align}
T = \frac{m}{2} \sum_{n=1}^{3} \left( \sum_{i=1}^{3} \frac{ \partial f_{n}  }{ \partial q_{i}  } \dot{q_{i} }  \right)\left( \sum_{i=1}^{3} \frac{ \partial f_{n}  }{ \partial q_{i}  } \dot{q_{i} }  \right)
\end{align}
$$

We can simplify this as long as we keep track of the cross terms

$$
\boxed{
\begin{align}
T = \frac{m}{2} \sum_{nij }^{3} \frac{ \partial f_{n}  }{ \partial q_{i}  } \frac{ \partial f_{n}  }{ \partial q_{j}  } \dot{q_{i} }\dot{q_{j} } 
\end{align}
}
$$
Remember this, we will come back to it. 

This accounts for 27 terms, since for each of the three j's there are three ns, and for each there are three i's. 

Remember the overall goal: we're trying to find when
$$
\begin{align}
\sum_{k}^{} \frac{ \partial T }{ \partial \dot{q}_{k}  } \dot{q_{k} } = 2T 
\end{align}
$$

We can see that  
$$
\begin{align}
\frac{ \partial T }{ \partial \dot{q}_{k}  } \dot{q}_{k} = \frac{ \partial  }{ \partial \dot{q}_{k}  } \left[ \frac{m}{2}\sum_{ni}^{} \frac{ \partial f_{n}  }{ \partial p_{i}  } \frac{ \partial f_{n}  }{ \partial q_{j}  } \dot{q}_{1} \dot{q}_{2}   \right]
\end{align}
$$
We know that our $x,y,z$ were time independent ($t$ is not in the function,  and they don't depend on $\dot{q_{n}}$ (aka holonomic) ) so this simplifies to

$$
\begin{align}
\frac{m}{2} \sum_{nij}^{}  \frac{ \partial f_{n}  }{ \partial q_{i } } \frac{ \partial f_{n}  }{ \partial q_{j}  } \frac{ \partial  }{ \partial \dot{q}_{k}  } ( \dot{q}_{1} \dot{q}_{2} ) \\
= \frac{m}{2} \sum_{n i j}^{} \frac{ \partial f_{n}  }{ \partial q_{i}  } \frac{ \partial f_{n}  }{ \partial q_{j}  } \left[ \frac{ \partial  \dot{q}_{i}  }{ \partial \dot{q}_{k} } \dot{q_{j} } + \dot{q}_{i} \frac{ \partial \dot{q}_{j}  }{ \partial \dot{q}_{k}  }  \right] 
\end{align}
$$


We know that
$$
\begin{align}
\frac{ \partial \dot{q_{i} } }{ \partial \dot{q}_{i}  } = 1 \text{ because ofc} \\
\text{ and }   \\
\frac{ \partial \dot{q}_{i}  }{ \partial \dot{q}_{\text{ not i }}  } = 0 
\end{align}
$$
This looks like a Kronecker delta

$$
\begin{align}
\frac{ \partial \dot{q}_{i}  }{ \partial \dot{q}_{k}  } = \begin{cases}
1 \text{ if } i == k \\
0 \text{ if } i \neq  k
\end{cases}
\end{align}
$$
We can simplify now with
$$
\begin{align}
\frac{ \partial  T }{ \partial \dot{q}_{k}  } = \frac{m}{2} \sum_{n i j}^{ } \frac{ \partial f_{n}  }{ \partial qi } \frac{ \partial f_{n}  }{ \partial q_{j}  } \bigg[ \delta_{ik} \dot{q}_{j} + \dot{q}_{i} \delta_{jk}  \bigg]   \\
\end{align}
$$

This simplifies down to
$$
\begin{align}
\frac{m}{2} \sum_{n j}^{} \dot{q}_{j}  \frac{ \partial f_{n}  }{ \partial q_{j}  }  \left( \sum_{i}^{} \delta_{ik}  \frac{ \partial f_{n}  }{ \partial q_{i}  }  \right) + \frac{m}{ 2} \sum_{n i}^{}\frac{ \partial f_{n}  }{ \partial q_{i}  } \dot{q}_{i} \sum_{j}^{} \frac{ \partial f_{n}  }{ \partial q_{j}  } \delta_{jk} 
\end{align}
$$
Which we can simplify to be
$$
\begin{align}
\frac{ \partial T }{ \partial \dot{q}_{k}  }  = \frac{m}{2} \sum_{nj}^{} \dot{q}_{j}  \frac{ \partial f_{n}  }{ \partial q_{j}  } \frac{ \partial f_{n}  }{ \partial q_{k}  }  + \frac{m}{2} \sum_{nj}^{} \dot{q}_{j} \frac{ \partial f_{n}  }{ \partial q_{j}  }  \frac{ \partial f_{n}  }{ \partial q_{k}  } 
\end{align}
$$
so
$$
\begin{align}
\frac{ \partial T }{ \partial \dot{q}_{k}  } = m \sum_{nj}^{} \dot{q}_{j} \frac{ \partial f_{n}  }{ \partial q_{j}  } \frac{ \partial f_{n}  }{ \partial q_{k}  }  
\end{align}
$$

Woah! Lets compare this to the boxed equation above!
$$
\begin{align}
\sum_{k}^{} \left( \frac{ \partial T }{ \partial \dot{q}_{k}  }  \right)\dot{q}_{k}  \stackrel{?}{=}  2T
\end{align}
$$
$$
\begin{align}
m \sum_{njk }^{} \frac{ \partial f_{n}  }{ \partial q_{j}  } \frac{ \partial f_{n}  }{ \partial q_{k}  } \dot{q}_{j} \dot{q}_{k}  = 2T
\end{align}
$$

Therefore - $H=2T-(T-U)=T+U$


