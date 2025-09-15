
When we have nonorthogonal basis 
$\hat{x} \text{ and }  \hat{l}$, and are finding kinetic energy we replace $v^{2}$ with
$$
\begin{align} \\  
\vec{v}_{m} \cdot \vec{v}_{m}   & =  \\
 &= (\dot{x}\hat{x}+\dot{l}\hat{l}) \cdot  (\dot{x}\hat{x}+\dot{l}\hat{l}) \\
 & = \dot{x}^{2}+\dot{l}^{2} + 2\dot{x}\dot{l}\, \hat{x}\cdot \hat{l}
\end{align}
$$

a variable is cyclic if it doesn't show up in the Lagrangian. 
if $x$ is cyclic, 
$$
\begin{align}
p_{x}  = \frac{ \partial \mathscr{L} }{ \partial \dot{x} } =m\dot{x}
\end{align}
$$
is conserved, since
$$
\begin{align}
\frac{d}{dt} \frac{ \partial \mathscr{L} }{ \partial \dot{x} } = \frac{ \partial \mathscr{L} }{ \partial x } = 0
\end{align}
$$


## Noethers theorem:
For every continuous symmetry of the action, there exists a corresponding conserved quantity.
$$
\begin{align}
S = \int_{t_{i} }^{t_{f} } \mathscr{L} dt
\end{align}
$$
For instance, imagine a ball falling in uniform gravity. If I move it right or left and let go, it'll fall in the same way (gravity is up and down, nothing depends on x) - so there is translational symmetry. 


## Applying Noethers Theorem
1) Identify a continuous symmetry of the system
2) choose a coordinate $q_{i}$ that parametrizes that symmetry
3) the generalized momentum $p_{i}= \frac{ \partial \mathscr{L} }{ \partial \dot{q}_{i} }$





What is conserved if
$$
\begin{align}
\frac{ \partial \mathscr{L} }{ \partial t } = 0? 
\end{align}
$$
We can write out
$$
\begin{align}
\frac{d}{dt} \mathscr{L} = \frac{ \partial \mathscr{L} }{ \partial q } \frac{ d q}{d t } + \frac{ \partial \mathscr{L} }{ \partial \dot{q} } \frac{ d \dot{q}}{d t }  +\cancelto{ 0 }{  \frac{ \partial \mathscr{L} }{ \partial t }  }
\end{align}
$$
We can use the definition of the legrangian to simplify this
$$
\begin{align}
\frac{d}{dt} \frac{ \partial \mathscr{L} }{ \partial \dot{q} } \dot{q} + \frac{ \partial \mathscr{L} }{ \partial \dot{q} } \frac{d}{dt} \dot{q} \\
\end{align}
$$
This looks like the product rule
$$
\begin{align}
\frac{ d \mathscr{L}}{d t } = \frac{d}{dt} \left( \frac{ \partial \mathscr{L} }{ \partial \dot{q} }  \dot{q}\right)
\end{align}
$$
Which leads us to
$$
\begin{align}
\frac{d}{dt} \left( \left[ \frac{ \partial \mathscr{L} }{ \partial \dot{q} } \dot{q}- \mathscr{L} \right] \right)=0
\end{align}
$$
This inner term is the Hamiltonian!

In N dimensions, if $\mathscr{L}(q_{1},q_{2},\dots,q_{n},\dot{q}_{1},\dot{q}_{2},\dots \dot{q}_{n})$
$$
\begin{align}
H = \sum_{i} p_{i} \dot{q}_{i}  
\end{align}
$$

## Time Symmetry
There must be a continuous time symmetry for something to be time invariant, or where time changing won't change the dynamics of your free variables.