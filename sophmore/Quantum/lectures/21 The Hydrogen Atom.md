Lets write out the time independent Schrödinger equation:
$$
\begin{align}
\left[ -\frac{\hbar^{2}}{2mr^{2}}\frac{ \partial  }{ \partial r } \left( r^{2} \frac{ \partial  }{ \partial r } \right)+ \frac{L_{op}^{2} }{2mr^{2}}+V(r) \right]\psi=E\psi 
\end{align}
$$
We have a generic central potential $V(r)$

Lets assume that we are in an eigenstate with
$$
\begin{align}
\psi(r,\theta,\phi)= R(r)Y_{l,ml} (\theta,\phi)
\end{align}
$$
We'll put this as our $\psi$.
We have
$$
\begin{align}
-\frac{\hbar^{2}}{2mr^{2}}Y_{l,m_{l} } \frac{ \partial  }{ \partial r } \left( r^{2} \frac{ \partial  }{ \partial r }  \right) R(r) + \frac{l(l+1)\hbar^{2}}{2mr^{2}}Y_{l,ml}R(r)+Y_{l,ml}R(r)V(r) = E Y_{l,m_{l} }R(r)   
\end{align}
$$
We can simplify this by writing
$$
\begin{align}
-\frac{\hbar^{2}}{2mr^{2}}\frac{ d }{d r } \left( r^{2} \frac{ d }{d r } R(r) \right) + \frac{l(l+1)\hbar^{2}}{2mr^{2}}R(r)+V(r)R(r)=ER(r)
\end{align}
$$

We can specify the coulomb potential as hydrogenic, which has some number of protons $z$ and stripped away all but 1 electron.
$$
\begin{align}
V(r)=\frac{-ze^{2}}{4\pi\epsilon_{0}r}
\end{align}
$$
Think of this as having charge $-e$ from the electron and $+ze$ for the protons, so overall charge $-ze^{2}$

We plug that into our differential equation
$$
\begin{align}
\frac{-\hbar^{2}}{2mr^{2}} \frac{ d }{d r } \left( r^{2}\frac{ d R}{d r }  \right)+ \frac{l(l+1)\hbar^{2}}{2mr^{2}}R-\frac{ze^{2}}{4\pi\epsilon_{0}r}R=ER
\end{align}
$$
We can simplify the $\frac{1}{r^{2}}\frac{ d }{d r }r^{2} \frac{ d }{d r }$ term 

$$
\begin{align}
\frac{1}{r^{2}} \frac{ d }{d r } \left( r^{2} \frac{ d R}{d r }  \right) = \frac{1}{r}\left[ 2 \frac{ d R}{d r } +r \frac{ d ^{2}R}{d r^{2} }  \right]  \\
= \frac{1}{r} \left[ \frac{ d R}{d r } +\frac{ d R}{d r } +r \frac{ d^{2} R}{d r^{2} }  \right]  \\
= \frac{1}{r} \left[ \frac{ d R}{d r } +\frac{ d }{d r } \left( r \frac{ d R}{d r }  \right) \right] 
\end{align}
$$

Which becomes

$$
\begin{align}
\frac{1}{r} \frac{ d }{d r } \left[ R+r \frac{ d R}{d r } \right] , \, \,  U(r)=r R(r) \\
\frac{1}{r}\frac{ d }{d r } \left[ \frac{ d }{d r } (rR) \right] = \frac{1}{r} \frac{ d ^{2}}{d r^{2} } (rR)
\end{align}
$$
We plug this in now:

$$
\begin{align}
-\frac{\hbar^{2}}{2m} \frac{ d ^{2}}{d r^{2} } U(r) + \frac{l(l+1)\hbar^{2}}{2mr^{2}}U(r)- \frac{ze^{2}}{4\pi\epsilon_{0}r}U(r)= EU(r) \\
\frac{-\hbar^{2}}{2m} \frac{ d ^{2}}{d r^{2} } U(r)+ \underbrace{ \left[ \frac{l(l+1)\hbar^{2}}{2mr^{2}}- \frac{ze^{2}}{4\pi\epsilon_{0}r} \right] }_{ V_{\text{ eff(r) }} } U(r ) = EU(r)
\end{align}
$$

This looks familiar...

$$
\begin{align}
-\frac{\hbar^{2}}{2m}\frac{ d ^{2}}{d r^{2} } U(r)+ V_{eff}(r)U(r)=EU(r) 
\end{align}
$$
Bazoonga! We can use some intuition as to what the energy solutions are going to be. 

![[Pasted image 20250317235124.png]]

## Effective Potential $V_{\text{ eff }}(r)$
![[Pasted image 20250310102850.png]]

some algebra I missed (my fault)

$$
\begin{align}
\frac{ d ^{2}U}{d r^{2} } - \frac{l(l+1)u}{r^{2}}+ 2 \frac{ze^{2}m}{4\pi\epsilon_{0}\hbar^{2}} \frac{1}{r}U= -\frac{2mE}{\hbar^{2}}U
\end{align}
$$
lets define
$$
\begin{align}
a = \frac{r\pi\epsilon_{0}\hbar^{2}}{ze^{2}m}=\frac{a_{0}}{z}
\end{align}
$$
($m$ is the mass of the electron that is bound)
$a_{0}$ is the Bohr radius

We can also simplify the right side by saying
$$
\begin{align}
-\frac{2mE}{\hbar^{2}}= \frac{1}{\lambda^{2}a^{2}} \\
E = -\frac{\hbar^{2}}{2ma^{2}} \frac{1}{\lambda^{2}}
\end{align}
$$
where $\lambda$ is a dimensionless constant.

![[Pasted image 20250310104216.png]]