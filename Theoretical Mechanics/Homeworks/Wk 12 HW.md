
![[Pasted image 20251114161503.png]]




![[Pasted image 20251114162159.png]]

Let the blue arrows denote rocket boosters to rotate the rocket barrel.

We know that
$$
\begin{align}
\left( \frac{ d \vec{L}}{d t }  \right)_{\text{ inertial }} = \left( \frac{ d \vec{L}}{d t }  \right)_{\text{ rot }}  + \vec{\omega}\times \vec{L}  
\end{align}
$$

$\vec{L} = I\omega$
$\Gamma= I \alpha$
Because the rockets are exerting torque on the craft, we have
$$
\begin{align}
\frac{ d \vec{L}}{d t } = \Gamma
\end{align}
$$
Which we can plug in to get
$$
\begin{align}
\Gamma= \left( \frac{ d \vec{L}}{d t } \right)_{\text{ rot }}  + \vec{\omega}\times \vec{L}_{\text{ inertial }} 
\end{align}
$$

We also know that in the rotating frame
$$
\begin{align}
\vec{L} = \lambda_{1} \omega_{x'}\hat{x}'+ \lambda_{2}\omega_{y'}\hat{y}'+\lambda_{3}\omega_{z'} \hat{z}'  
\end{align}
$$
so we can calculate $\vec{\omega}\times \vec{L}$ as
$$
\begin{align}
\vec{\omega}\times \vec{L} & =  (\omega_{x'} \hat{x}'+ \omega_{y'} \hat{y}' + \omega_{z'}\hat{z}' ) \times (\lambda_{1} \omega_{x'}\hat{x}'+ \lambda_{2}\omega_{y'}\hat{y}'+\lambda_{3}\omega_{z'} \hat{z}')  \\
\end{align}
$$

which tells us
$$
\begin{align}
\left( \frac{ d \vec{L}}{d t }  \right)_{rot} = \lambda_{1} \dot{\omega}_{x'} \hat{x}' +\lambda_{2} \dot{\omega}_{y'} \hat{y}' +\lambda_{3} \dot{\omega}_{z'} \hat{z}' 
\end{align}
$$
Using $\lambda_{1}=\lambda_{2}$, we can write out the Euler equations with Torque

$$
\begin{align}
\lambda \dot{\omega}'_{x}   & = (\lambda-\lambda_{3})\omega'_{y} \omega'_{z}  + \Gamma_{x}   \\
\lambda \dot{\omega}'_{y}   & = (\lambda_{3}-\lambda)\omega'_{x} \omega'_{z} + \Gamma_{y}    \\
\lambda_{3} \dot{\omega}'_{z}   & = (\lambda-\lambda)\omega'_{x} \omega'_{y} + \Gamma_{z}
\end{align}
$$

$\Gamma$ is only oriented along the $z$ direction, so 
$$
\begin{align}
\lambda \dot{\omega}'_{x}   & = (\lambda-\lambda_{3})\omega'_{y} \omega'_{z} \\
\lambda \dot{\omega}'_{y}   & = (\lambda_{3}-\lambda)\omega'_{x} \omega'_{z} \\
\lambda_{3} \dot{\omega}'_{z}   & = \Gamma_{z}
\end{align}$$
So $\dot{\omega}_{z'} = \frac{\Gamma_{z}}{\lambda_{3}}$.

We can easily solve that part as
$$
\begin{align}
\omega_{z'} = \frac{\gamma_{z}}{\lambda_{3}}t 
\end{align}
$$


Lets solve for $\dot{\omega}_{x'}\text{ and } \dot{\omega}_{y'}\text{ to get } \omega_{x}\text{ and } \omega_{y}$:

$$
\begin{align}
\lambda \dot{\omega}_{x'} = (\lambda-\lambda_{3})\omega_{y'} \frac{\Gamma_{z}}{\lambda_{3}} \\
\lambda \dot{\omega}_{y'} = (\lambda_{3}-\lambda)\omega_{x'} \frac{\Gamma_{z}}{\lambda_{3}}
\end{align}
$$

So we have finally
$$
\begin{align}
\dot{\vec{\omega}} = \begin{pmatrix}
\frac{(\lambda-\lambda_{3})\omega_{y'}}{\lambda \lambda_{3}} \Gamma_{z} \\

\frac{(\lambda_{3}-\lambda)\omega_{x'}}{\lambda \lambda_{3}} \Gamma_{z}   \\
\frac{\Gamma_{z} }{\lambda_{3}}
\end{pmatrix}
\end{align}
$$
These are basically constants, so I'll rewrite this with $\mathcal{C}$
$$
\begin{align}
\mathcal{C} & = \frac{(\lambda-\lambda_{3})}{\lambda \lambda_{3}} \\
\end{align}
$$



$$
\begin{align}
\dot{\vec{\omega}} & =\begin{pmatrix}
\mathcal{C} \omega_{y'} \Gamma_{z} \\
-\mathcal{C}\omega_{x'} \Gamma_{z} \\
\frac{\Gamma_{z}}{\lambda_{3}}     
\end{pmatrix}
\end{align}
$$
Note for the future, the relation
$$
\begin{align}
\omega_{y'} = \frac{\dot{\omega}_{x'}}{\mathcal{C} \,  \Gamma_{z} } 
\end{align}
$$


We can simplify this with expressions that we do have (knowing that the torque is constant):
$$
\begin{align}
\ddot{\vec{\omega}} = \begin{pmatrix}
\mathcal{C}\dot{\omega}_{y'} \Gamma_{z}    \\
-\mathcal{C} \dot{\omega}_{x'}   \Gamma_{z} \\
0 
\end{pmatrix}
\end{align}
$$

We can replace expressions that we already have circularly
$$
\begin{align}
\ddot{\vec{\omega}} = \begin{pmatrix}
\mathcal{C}^{2}\omega_{x'}\Gamma_{z}^{2} \\
-\mathcal{C}^{2} \omega_{y'} \Gamma_{z}^{2} \\ 0
\end{pmatrix}
\end{align}
$$
Lets take the ansatz that our final differential equation will have the form
$$
\begin{align}
\mathbb{Z}(t)=\mathbb{Z}_{0} e^{i\omega t}
\end{align}
$$
Where $\omega_{x} = \mathrm{Re}\left\{ \mathbb{Z}(t) \right\}, \omega_{y}= \mathrm{Im}\left\{ \mathbb{Z}(t) \right\}$, 

We have the initial conditions for $\mathbb{Z}_{0}$
$$
\begin{align}
\mathbb{Z}_{0}  & = \begin{pmatrix}
\omega_{10} \hat{x}' \\
\omega_{20} \hat{y}' \\
0
\end{pmatrix}
\end{align}
$$

For the $X'$ component, we have
$\omega_{x'}=\cos(\mathcal{C}\, \Gamma_{z}t)$
We can also solve for $\omega_{y}$ with the expression from earlier, $\omega_{y'} = \frac{\dot{\omega}_{x'}}{\mathcal{C} \,  \Gamma_{z} }$
$$
\begin{align}
\frac{d}{dt} \omega_{x'}  & = \mathcal{C} \, \Gamma_{z} \sin(\mathcal{C} \, \Gamma_{z}t ) 
\end{align}
$$
So
$\omega_{y'}=\mathbb{Z}_{0,y} \mathbb{Z}_{0,x} \sin(\mathcal{C} \, \Gamma_{z}t )$




![[Pasted image 20251114161504.png]]




![[Pasted image 20251114161508.png]]




![[Pasted image 20251114161510.png]]





![[Pasted image 20251114161512.png]]





![[Pasted image 20251114161514.png]]



