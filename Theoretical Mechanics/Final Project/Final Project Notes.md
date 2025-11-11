Midterm 1:
https://drive.google.com/file/d/1Eb_YAcQPxAT_mvUitD4e71ya-d4oYTOh/view

![[Pasted image 20251108154127.png]]


$\odot$ sun
$\oplus$ earth
$*$ asteroid

In regular x, y coordinates, our Lagrangian is given by 
$$
\begin{align}
\mathscr{L}  & = \frac{1}{2}m_{\odot}(\dot{x}_{\odot }^{2} + \dot{y} _{\odot } ^{2} ) + \frac{1}{2}m_{\oplus } (\dot{x}_{\oplus } ^{2}+\dot{y}_{\oplus } ^{2}) + \frac{1}{2} m_{*} (x_{*}^{2}+y_{*}^{2}  ) + \frac{G M_{\odot }M_{\oplus}}{r_{\odot \oplus } } + \frac{GM_{\odot *}}{r_{\odot *} } + \frac{GM_{\oplus }M_{*}}{r_{\oplus *} }   \\
\text{ where } \\
r_{ab}  & = \sqrt[]{ (x_{a} -x_{b} )^{2}+(y_{a} -y_{b})^{2} } 
\end{align}
$$




To transform from constant $\begin{pmatrix}x\\y\end{pmatrix}$ to the rotating frame, we use the transformation
$$
\begin{align}
\begin{pmatrix}
x\\y 
\end{pmatrix} = \begin{pmatrix}
\cos\theta  & -\sin\theta \\
\sin\theta & \cos\theta
\end{pmatrix} \begin{pmatrix}
x' \\ y'
\end{pmatrix}
\end{align}
$$
This gives us the following generalized coordinates in the rotating frame.
$$
\begin{align}
x  & = x'\cos\omega t-y'\sin\Omega t \\
\dot{x}  & = \dot{x}'\cos \Omega t- \dot{y}'\sin\Omega t - x' \Omega \sin \Omega t - y'\Omega \cos \Omega t  \\
y  & = x'\sin\Omega t + y' \cos \Omega t \\
\dot{y}  & = \dot{x}'\sin \Omega t + \dot{y}'\cos \Omega t + x'\Omega \cos \Omega t - y'\Omega \sin \Omega t
\end{align}
$$

This gives us 
$$
\begin{align}
T  & = \frac{1}{2}\mu_{\odot,\oplus } a^{2}\Omega^{2}+T_{m} = \frac{1}{2}\mu_{\odot,\oplus } a^{2}\Omega^{2} + \frac{1}{2}m (\dot{x}'^{2}+\dot{y}'^{2}) + \frac{1}{2}m \Omega^{2}(x'^{2}+y'^{2})+ m\Omega(x' \dot{y}' - \dot{x}'y')    \\
\mathscr{r}_{*} &  = \sqrt[]{ (x'+fa)^{2}+y'^{2} }  \\
\mathscr{r} _{\oplus }   & = \sqrt[]{ (x' - (1-f)a)^{2}+y'^{2} } 
\end{align}
$$


Because $\mu_{\odot,\oplus}a^{2}\Omega^{2}\text{ and } \frac{Gm*m\oplus}{a}$ are constant, they don't change the Lagrangian.
Therefore, we get
$$
\begin{align}
\mathscr{L}  = \frac{1}{2}m(\dot{x}'^{2}+\dot{y}')^{2} + \frac{1}{2}m \Omega^{2}(x'^{2}+y'^{2}) + m\Omega(x'\dot{y}'-\dot{x}'y')+ \frac{GM_{\odot }m_{*}  }{\mathscr{r} _{\odot } } + \frac{Gm_{\oplus } m_{*} }{r_{\oplus } }
\end{align}
$$


$$
\begin{align}
\mathcal{H} = \frac{1}{2}m(\dot{x}'^{2} + \dot{y}'^{2}) - \frac{1}{2}m \Omega^{2}(x'^{2}+y'^{2} ) - \frac{GM_{\odot}M}{r_{\odot} } - \frac{GM_{*}M}{r_{e} }   
\end{align}
$$
