
![[Pasted image 20260331210721.png]]

To find $\left< E \right>$, we can do
$$
\begin{align}
\braket{ \alpha|\hat{H} | \alpha } 
\end{align}
$$
Separating this out by components,
$$
\begin{align}
\left< E \right>  & = \frac{\left< p_{x} ^{2} \right> }{2m}+ \frac{1}{2}m\omega^{2} \left< x^{2} \right>  \\
 & = \frac{(\Delta p_{x} )^{2}+ \left< p_{x} ^{2} \right> }{2m}+ \frac{1}{2}m\omega^{2} [(\Delta x)^{2}+\left< x \right> ^{2}]
\end{align}
$$
eq 7.50 page 257

In an energy eigenstate:
$$
\begin{align}
\left< E \right> = \frac{(\Delta p_{x} )^{2}}{2m} + \frac{1}{2}m\omega^{2} (\Delta x)^{2}
\end{align}
$$


The coherent state $\ket{\alpha}= e^{-\frac{\left| \alpha \right|^{2}}{2}} \sum_{n=0}^{\infty} \frac{\alpha^{n}}{\sqrt[]{ n! }} \ket{n}$

We know that for the coherent state, 
$$
\begin{align}
\left< x \right> = \sqrt[]{ \frac{\hbar}{2m\omega} } 2 \left|  \alpha \right| \cos(\omega t+\delta)
\end{align}
$$
and that
$$
\begin{align}
\left< p_{x}  \right> = - \sqrt[]{ \frac{m\omega \hbar}{2} }2 \left| \alpha \right| \sin(\omega t+\delta)
\end{align}
$$
$$
\begin{align}
\left< x^{2} \right> = \frac{\hbar}{2m\omega} [\alpha(t)^{2} + \alpha ^{*}(t)^{2} + 2\left| \alpha(t) \right|^{2} +1] \\
\left< p_{x} ^{2} \right> = \frac{m\omega \hbar}{2} [2 \left| \alpha(t) \right| ^{2}+1-\alpha(t)^{2}-\alpha ^{*}(t)^{2}]
\end{align}
$$
(page 266)
This gives
$$
\begin{align}
(\Delta x)^{2} = \frac{\hbar}{2m\omega} \\
(\Delta p_{x} )^{2} = \frac{m\omega \hbar}{2}
\end{align}
$$
We can just plug and chug,
$$
\begin{align}
\left< E \right>  & = \frac{(\Delta p_{x} )^{2}}{2m} + \frac{1}{2}m\omega^{2} (\Delta x)^{2} \\
 & = \frac{\omega \hbar}{4} + \frac{1}{4}\omega \hbar  \\
 \left< E \right> & =  \frac{\hbar\omega}{2}
\end{align}
$$


![[Pasted image 20260331210729.png]]

We have the series expansion
$$
\begin{align}
\hat{T}(a_{x} \mathbf{i})= 1- \frac{i \hat{p}_{x} a_{x} }{\hbar} - \frac{\hat{p}^{2}_{x}a^{2}_{x}  }{2\hbar^{2}} + \dots \\
\hat{T}(a_{y} \mathbf{j})= 1- \frac{i \hat{p}_{y} a_{y} }{\hbar} - \frac{\hat{p}^{2}_{y}a^{2}_{y}  }{2\hbar^{2}} + \dots
\end{align}
$$
If we apply successive translations in different directions, they don't change anything. We can plug these into
$$
\begin{align}
\hat{T}(a_{y} \mathbf{j})\hat{T}(a_{x} \mathbf{i})=\hat{T}(a_{x} \mathbf{i})\hat{T}(a_{y} \mathbf{j})
\end{align}
$$
to see that
$$
\begin{align}
\left( 1- \frac{i \hat{p}_{x} a_{x} }{\hbar} - \frac{\hat{p}^{2}_{x}a^{2}_{x}  }{2\hbar^{2}} + \dots  \right)\left(1- \frac{i \hat{p}_{y} a_{y} }{\hbar} - \frac{\hat{p}^{2}_{y}a^{2}_{y}  }{2\hbar^{2}} + \dots\right)= \left( 1- \frac{i \hat{p}_{y} a_{y} }{\hbar} - \frac{\hat{p}^{2}_{y}a^{2}_{y}  }{2\hbar^{2}} + \dots \right) \left( 1- \frac{i \hat{p}_{x} a_{x} }{\hbar} - \frac{\hat{p}^{2}_{x}a^{2}_{x}  }{2\hbar^{2}} + \dots  \right)
\end{align}
$$

We can keep terms up to second order
$$
\begin{align}
\left( 1- \frac{i\hat{p}_{y} a_{y}}{\hbar} - \frac{\hat{p}^{2}_{y}a_{y} ^{2} }{2\hbar^{2}} - \frac{i\hat{p}_{x} a_{x} }{\hbar} - \frac{\hat{p}^{2}_{x} a_{x} }{2\hbar^{2}} - \frac{\hat{p}_{x} a_{x} \hat{p}_{y} a_{y} }{\hbar^{2}} \right)= \left( 1- \frac{i\hat{p}_{y} a_{y}}{\hbar} - \frac{\hat{p}^{2}_{y}a_{y} ^{2} }{2\hbar^{2}} - \frac{i\hat{p}_{x} a_{x} }{\hbar} - \frac{\hat{p}^{2}_{x} a_{x} }{2\hbar^{2}} - \frac{\hat{p}_{y} a_{y} \hat{p}_{x} a_{x} }{\hbar^{2}} \right)
\end{align}
$$
We can see that all the terms are the same except for the very last, so this becomes
$$
\begin{align}
\hat{p}_{x}a_{x} \hat{p}_{y} a_{y} = \hat{p}_{y} a_{y}  \hat{p}_{x}a_{x}  
\end{align}
$$
Dividing by constants and rearranging
$$
\begin{align}
\hat{p}_{x} \hat{p}_{y} = \hat{p}_{y} \hat{p}_{x} \\
\hat{p}_{x} \hat{p}_{y} - \hat{p}_{y} \hat{p}_{x} =0 \\
[\hat{p}_{x},\hat{p}_{y}  ]= 0
\end{align}
$$


![[Pasted image 20260331210737.png]]
# TODO I HAVE NOT FIGURED IT OUT


We have the position momentum commutation relations for individual particles
$$
\begin{align}
[\hat{x}_{i},\hat{p}_{j}]= i\hbar \delta _{ij}
\end{align}
$$
(eq 9.19)
and that generators commute
$[\mathbf{\hat{p}}_{1},\mathbf{\hat{p}}_{2}]=0$ (eq 9.30)


$$
\begin{align}
[\hat{r}_{ni} , \hat{p}_{nj} ] = i\hbar \delta _{ij} \\
\end{align}
$$

We also have the multiparticle commutations
![[Pasted image 20260401112243.png|500]]




![[Pasted image 20260331210757.png]]
$$
\begin{align}
\frac{\hat{p}_{1}^{2}}{2m_{1}}+ \frac{\hat{p}_{2}^{2} }{2m_{2}} \stackrel{?}{=}  \frac{\hat{P}^{2}}{2M} + \frac{\hat{p}^{2}}{2\mu} \\
\frac{\hat{p}_{1}^{2}}{2m_{1}}+ \frac{\hat{p}_{2}^{2} }{2m_{2}} \stackrel{?}{=}  \frac{\hat{P}^{2}}{2(m_{1}+m_{2})} + \frac{\hat{p}^{2}}{2 \left( \frac{m_{1}m_{2}}{m_{1}+m_{2}} \right)}
\end{align}
$$

We can bring the left side to look more like this
$$
\begin{align}
\frac{m_{2}\hat{p}_{1}^{2} + m_{1} \hat{p}_{2}^{2}}{2(m_{1}m_{2})} \stackrel{?}{=}  \frac{(\hat{p}_{1}+\hat{p}_{2} )^{2}}{2(m_{1}+m_{2})} + \frac{\left( \frac{m_{2}\hat{p}_{1}-m_{1}\hat{p}_{2}}{m_{1}+m_{2}} \right)^{2}(m_{1}+m_{2})}{2(m_{1}m_{2})}
\end{align}
$$

I will simplify the right side now
$$
\begin{align}
\frac{m_{2}\hat{p}_{1}^{2} + 2m_{1} \hat{p}_{2}^{2}}{2(m_{1}m_{2})}  & \stackrel{?}{=}  \frac{\hat{p}_{1}^{2}+\hat{p}_{2}^{2}+2\hat{p}_{1}\hat{p}_{2}}{2(m_{1}+m_{2})} +\frac{(m_{2}\hat{p}_{1}-m_{1}\hat{p}_{2})^{2}}{m_{1}+m_{2}} \frac{1}{2m_{1}m_{2}}  \\

\end{align}
$$
We remove the denominator
$$
\begin{align}
m_{2}\hat{p}_{1}^{2}+m_{1}\hat{p}_{2}^{2} \stackrel{?}{=}   \frac{m_{1}m_{2}(\hat{p}_{1}^{2}+\hat{p}_{2}^{2}+2\hat{p}_{1}\hat{p}_{2})}{(m_{1}+m_{2})} + \frac{(m_{2}\hat{p}_{1}-m_{1}\hat{p}_{2})^{2}}{m_{1}+m_{2}} 
\end{align}
$$
We now get
$$
\begin{align}
((m_{1}m_{2}+m_{2}^{2})p_{1}\hat{^{2}} + (m_{1}^{2}+m_{1}m_{2})\hat{p}_{2}^{2}) \stackrel{?}{=}   m_{1}m_{2}(\hat{p}_{1}^{2}+\hat{p}_{2}^{2}+2\hat{p}_{1}\hat{p}_{2})+(m_{2}^{2}\hat{p}_{1}^{2}+m_{1}^{2}\hat{p}_{2}^{2}-2m_{1}m_{2}\hat{p}_{1}\hat{p}_{2})
\end{align}
$$
The cross term cancels
$$
\begin{align}
((m_{1}m_{2}+m_{2}^{2})p_{1}\hat{^{2}} + (m_{1}^{2}+m_{1}m_{2})\hat{p}_{2}^{2}) \stackrel{?}{=}   m_{1}m_{2}(\hat{p}_{1}^{2}+\hat{p}_{2}^{2})+(m_{2}^{2}\hat{p}_{1}^{2}+m_{1}^{2}\hat{p}_{2}^{2})
\end{align}
$$
We can see this is true
$$
\begin{align}

 ((m_{1}m_{2}+m_{2}^{2})p_{1}\hat{^{2}} + (m_{1}^{2}+m_{1}m_{2})\hat{p}_{2}^{2})  & \stackrel{?}{=} ((m_{1}m_{2}+m_{2}^{2})p_{1}\hat{^{2}} + (m_{1}^{2}+m_{1}m_{2})\hat{p}_{2}^{2}) \\
1  & =1  
\end{align}
$$
So this holds true!

