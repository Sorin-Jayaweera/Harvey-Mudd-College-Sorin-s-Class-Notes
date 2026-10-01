![[Pasted image 20260409211157.png]]

The energy is exactly $\hbar \omega$ for the simple harmonic oscillator here. 

The energy from $l=0$ to $l=1$ 
$$
\begin{align}
\Delta E = \frac{l\hbar^{2}}{I} = \frac{\hbar^{2}}{I}
\end{align}
$$

Where 
$I = \mu r_{0}^{2}$, so $r_{0} = \sqrt[]{ \frac{I}{\mu} }$

We can set these equal and shove 
$$
\begin{align}
I = \frac{\hbar^{2}}{\Delta E} \\
r_{0} = \sqrt[]{  \frac{\hbar^{2}}{\mu \Delta E} } 
\end{align}
$$

We can assume that $\mu$ is on the order of the nuclear mass $M_{n}$, but we can easily get $\mu$ here anyways
$$
\begin{align}
\mu = \frac{m_{c} m_{o} }{m_{c} +m_{o} }
\end{align}
$$

This energy difference is
$$
\begin{align}
\Delta E = h\nu
\end{align}
$$
$$
\begin{align}
\Delta E &  = 1.15* 10^{11} * 6.626 * 10^{-34} \\
 & = 7.62 * 10^{-23} J \\
\end{align}
$$
The mass of carbon is
$$
\begin{align}
 & \frac{12 g}{6.02 * 10^{23}} \\
 & = 1.99 \cdot 10^{-26}kg
\end{align}
$$
Similarly, the mass of oxygen is
$$
\begin{align}
2.6*10^{-26}kg
\end{align}
$$

this gives us
$$
\begin{align}
\mu = 1.09 * 10^{-26}
\end{align}
$$
$$
\begin{align}
r_{0}  & = \sqrt[]{  \frac{\hbar^{2}}{\mu \Delta E} }  \\
 & = 1.15 * 10^{-10} m \\
 & = 1.15 A
\end{align}
$$
where $A$ is aangstrom, i don't know the latex and have to rush to finish the pset lol.



![[Pasted image 20260409211207.png]]

$$
\begin{align}
\hat{L}_{x} = \frac{\hat{L}_{+} +\hat{L}_{-} }{2}
 \\
\hat{L}_{y} = \frac{\hat{L}_{+} -\hat{L}_{-} }{2i}\end{align}
$$
The expectation value $\left< \hat{L}_{x} \right>$ is
$$
\begin{align}
 & \braket{ l m\mid  \hat{L}_{x} |lm} \\
 & = \frac{1}{2} \braket{ lm | \hat{L}_{+}+\hat{L}_{-}  |lm } \\
 & = \frac{1}{2} \braket{ lm | \hat{L}_{+} | lm } + \frac{1}{2} \braket{ lm | \hat{L}_{-} | lm  }    \\
 & = 0
\end{align}
$$
We can see this because raising the state changes the ket, but not the bra. 

The same for $\left< \hat{L}_{y} \right>=0$

## $\Delta \hat{L}_{x}$

We can now look at
$$
\begin{align}
\left< \hat{L}_{x} ^{2} \right> = 
 & \braket{ l, m\mid  \hat{L}_{x}\hat{L}_{x}  |lm}  \\
 & \frac{1}{4}\braket{ lm | (\hat{L}_{+}+\hat{L}_{-}  )(\hat{L}_{+}+\hat{L}_{-}  )| l,m}  \\
& \frac{1}{4}\braket{ lm | \hat{L}_{+} \hat{L}_{-} +\hat{L}_{- }\hat{L}_{+} + \cancelto{ 0 }{ \hat{L}_{+}^{2} + \hat{L}_{-}^{2} }   | l,m} 
\end{align}
$$

We know that
$$
\begin{align}
\hat{L}_{-} \ket{l,m} = \sqrt[]{ l(l+1) - m(m-1)}\hbar \ket{l,m-1}  
\end{align}
$$
And that
$$
\begin{align}
\hat{L}_{+} = \sqrt[]{ l(l+1)- m(m+1) }\hbar\ket{l,m+1}   
\end{align}
$$

Therefore,
$$
\begin{align}
 & \braket{ lm | \hat{L}_{+} \hat{L}_{-}|lm  }  \\
 & = \sqrt[]{ l(l+1)-m(m-1) } \hbar \braket{ lm | \hat{L}_{+} |l,m-1 } \\
 & = \sqrt[]{ l(l+1)-m(m-1) }\sqrt[]{ l(l+1)-(m-1)(m) }  \hbar^{2}\braket{ lm | |l,m }   \\
 & =( l(l+1)-m(m-1)) \hbar^{2}
\end{align}
$$
And
$$
\begin{align}
 & \braket{ l,m | \hat{L}_{-} \hat{L}_{+} |lm }  \\
 & = \sqrt[]{ l(l+1)-m(m+1) } \hbar\braket{ l,m | \hat{L}_{-} |l,m+1 }  \\
 & = \sqrt[]{ l(l+1)-m(m+1) } \sqrt[]{ l(l+1)- (m+1 )(m) } \hbar^{2} \\
 & = ( l(l+1)- m(m+1)) \hbar^{2}
\end{align}
$$

The expectation value is therefore
$$
\begin{align}
\left< \hat{L}_{x} ^{2} \right> = \hbar^{2}\left( \frac{l(l+1)-m(m-1) }{4} + \frac{l(l+1)-m(m+ 1) }{4} \right) \\
\end{align}
$$

The $m$ bits combine
$$
\begin{align}
m(m-1) - m(m+1) \\
m( m-1 -m-1 ) \\
-2m
\end{align}
$$
so we get
$$
\begin{align}
\left< \hat{L}^{2}_{x}  \right>  & = \frac{2l(l+1)-2m}{4}
\end{align}
$$
This gives us
$$
\boxed{
\begin{align}
\Delta \hat{L}_{x} =  \frac{2l(l+1)-2m}{4}
\end{align}
}
$$

## $\Delta \hat{L}_{y}$

$$
\begin{align}
\left< \hat{L}_{x} ^{2} \right> = 
 & \braket{ l, m\mid  \hat{L}_{x}\hat{L}_{x}  |lm}  \\
 & \frac{1}{4i^{2}}\braket{ lm | (\hat{L}_{+}-\hat{L}_{-}  )(\hat{L}_{+}-\hat{L}_{-}  )| l,m}  \\
& -\frac{1}{4}\braket{ lm | -\hat{L}_{+} \hat{L}_{-} -\hat{L}_{- }\hat{L}_{+} + \cancelto{ 0 }{ \hat{L}_{+}^{2} + \hat{L}_{-}^{2} }   | l,m}  \\
& \frac{1}{4}\braket{ lm | \hat{L}_{+} \hat{L}_{-} +\hat{L}_{- }\hat{L}_{+} | l,m} 
\end{align}
$$
We can see that this is the same as $\hat{L}_{x}^{2}$, so

$$
\boxed{
\begin{align}
\Delta \hat{L}_{y} =  \frac{2l(l+1)-2m}{4}
\end{align}
}
$$





![[Pasted image 20260409211215.png]]

## A
We know that $\hat{L}_{z}$ commutes with $\hat{P}^{2}$. The potential only depends on $x$ and $y$, so any actions on $z$ don't matter which order they are done in. Therefore, the Hamiltonian commutes with $\hat{L}_{z}$. 

## B
For convenience, I'll label eigenstates of $\hat{H}$ as $\ket{e}$, eigenstates of $\hat{P}^{2}$ as $\ket{P}$, eigenstates of $\hat{L}_{z}$ as $\ket{l}$, and eigenstates of $\hat{p}_{z}$ as $\ket{p}$


We want to find

$$
\begin{align}
\bra{e,l,m}\ket{} 
\end{align}
$$


![[Pasted image 20260409211224.png]]

$$
\begin{align} \\
r  & = \sqrt[]{ x^{2}+y^{2}+z^{2} } \\ 
x  & = r\sin\theta \cos \phi \\
y  & = r\sin\theta \sin \phi \\
z  & = r\cos \theta
\end{align}
$$
We can rewrite this in spherical
$$
\begin{align}
\psi(r)  & = (x+y+z)f(r) = \sqrt[]{ r } f(r) \\
 & = (\sin\theta \cos \phi + \sin\theta \sin \phi + \cos\theta)rf(r)
\end{align}
$$
The $\cos\theta$ part can be represented by
$$
\begin{align}
Y_{1,0} = \sqrt[]{ \frac{3}{4\pi} } \cos\theta
\end{align}
$$
The $\sin\theta \sin \phi$ can be represented with
$$
\begin{align}
(Y_{11}+Y_{1,-1}  ) & =- \sqrt[]{ \frac{3}{8\pi} } \sin\theta(e^{i\phi}-e^{-i\phi}) \\
 & = -i\sqrt[]{ \frac{3}{4\pi} }  \sin\theta \sin\phi
\end{align}
$$
the $\sin\theta \cos \phi$ is just
$$
\begin{align}
(Y_{1,-1}-Y_{11})  &  = \sqrt[]{ \frac{3}{8\pi} } \sin\theta (e^{i\phi}+ e^{-i\phi})  \\
 & = \sqrt[]{ \frac{3}{4\pi} } \sin\theta \cos \phi
\end{align}
$$

Adding these just gives
$$
\begin{align}
\psi(r)  & = \sqrt[]{ \frac{4\pi}{3} } (Y_{1,-1}-Y_{1,1}+Y_{1,1}+Y_{1,-1} + Y_{1,0})r f(r) \\
 & = \sqrt[]{ \frac{4\pi}{3} } (2Y_{1,-1}+ Y_{1,0}  )rf(r)
\end{align}
$$
$$
\begin{align}
\hat{L}_{z} \ket{l,m} = m\hbar \ket{l,m} 
\end{align}
$$

When we measure $\hat{L}_{z}$, we can measure either $-\hbar$ $\frac{2}{3}$ of the time, or $-0$, $\frac{1}{3}$ of the time. 



![[Pasted image 20260409211232.png]]

We can act the parity operator on the state
$$
\begin{align}
Y_{lm} = \frac{(-1)^{l}}{2^{l}l!} \sqrt[]{ \frac{(2l+1)(l+m)!}{4\pi(l-m)!} } e^{im\phi} \frac{1}{\sin ^{m}\theta} \frac{d^{l-m}}{d(\cos\theta)^{l-m}}  \sin ^{2l}\theta 
\end{align}
$$
I will ignore all the constants and only look at how the parity operator acts on the coordinate filled portions of $Y_{lm}$, which I'll call $y_{lm}$ for now
$$
\begin{align}
Y_{lm} \propto e^{im\phi} \frac{1}{\sin ^{m}\theta} \frac{d^{l-m}}{d(\cos(\theta))^{l-m}} \sin ^{2l}(\theta)= y_{lm} 
\end{align}
$$

$$
\begin{align}
\hat{\Pi} y_{l,m} =   e^{im(\phi+\pi)} \frac{1}{\sin ^{m}(\pi-\theta)} \frac{d}{d(\cos(\pi-\theta))^{l-m}}\sin ^{2l}(\pi-\theta)
\end{align}
$$


We know that
$$
\begin{align}
e^{im\pi} = (-1)^{m}
\end{align}
$$
and 
$$
\begin{align}
\sin(\pi-\theta)= -\sin(\theta) \\
\cos(\pi-\theta)= -\cos(\theta) \\
\end{align}
$$

This becomes
$$
\begin{align}
(-1)^{m} \frac{1}{ (-1)^{m} \sin ^{m}(\theta)} \frac{d}{d((-1)^{l-m}(\cos\theta)^{l-m})}\sin ^{2l}(\theta)
\end{align}
$$
This has just put a constant onto the original state $y_{lm}$, 

$$
\begin{align}
\lambda= \frac{(-1)^{m}}{(-1)^{m}(-1)^{l-m}} \\
\lambda= (-1)^{m-l}
\end{align}
$$
This is different from the expected result, but I don't know how to deal with the derivative with respect to cos, and I'm unfortunately low on time before this is due.



![[Pasted image 20260409211240.png]]

## a

We can break this up into 
$$
\begin{align}
Y_{11} = -\sqrt[]{ \frac{3}{8\pi} }  \sin\theta e^{i\phi} \ket{1,1} \\
Y_{1,-1} = \sqrt[]{ \frac{3}{8\pi} }  \sin\theta e^{-i\phi}\ket{1,-1} 
\end{align}
$$
The sum of these is
$$
\begin{align}
(Y_{11}+Y_{1,-1}  ) & =- \sqrt[]{ \frac{3}{8\pi} } \sin\theta(e^{i\phi}-e^{-i\phi}) \\
 & = -i\sqrt[]{ \frac{3}{4\pi} }  \sin\theta \sin\phi
\end{align}
$$
Therefore, 
$$
\begin{align}
\frac{1}{i }(Y_{11}-Y_{1,-1}  ) = \bra{\theta,\phi} \ket{\psi(0)} 
\end{align}
$$
The spherical harmonics are energy eigenstates of the Hamiltonian and have the same $E$
$$
\begin{align}
Y_{l,m}(t) = e^{-i \frac{E}{\hbar}t} Y_{l,m}(0) 
\end{align}
$$
Therefore, the time evolved $\psi$ has every component multiplied by the same spinning phase
$$
\begin{align}
\psi(t) = e^{- i\frac{E}{\hbar}t}\psi(0)
\end{align}
$$


## b

$$
\begin{align}
\hat{L}_{z} \ket{l,m} = m\hbar \ket{l,m} 
\end{align}
$$

We have an equal mixture of $Y_{1,1} \text{ and }  Y_{1,-1}$. This gives a 50-50 chance of either $\hbar$ or $-\hbar$ angular momentum. 

## c
$$
\begin{align}
\hat{J}_{x}  =  \frac{\hat{J}_{+} +\hat{J}_{-} }{2}
\end{align}
$$
We can apply the operator and do
$$
\begin{align}
\braket{ lm | \hat{J}_{x}|lm } 
\end{align}
$$
We can't raise the $Y_{1,1}$ state, nor can we lower the $Y_{1,-1}$ state - this just leaves us with what we started - the lowered $Y_{11}$ and the raised $Y_{1,-1}$. This is exactly what we started with, but with a factor of $\frac{1}{2}$. 

The eigenvalues of $\hat{J}_{+}$ are $\sqrt[]{ j(j+1)- m(m+1) }\hbar$ and $\hat{J}_{-}$ are $\sqrt[]{ j(j+1)-m(m-1) }\hbar$.

For the $Y_{1,-1}$ state being raised, this gives
$$
\begin{align}
\sqrt[]{ 1(2)-(-1(1)) }  & = \sqrt[]{ 2+1 } = \sqrt[]{ 3 } 
\end{align}
$$

For $Y_{1,1}$ being lowered, this is
$$
\begin{align}
\sqrt[]{ 1(2)-(1(-1)) } = \sqrt[]{ 3 } 
\end{align}
$$
We get $2\sqrt[]{ 3 }$ from these alone, but we have the factor of $\frac{1}{2}$.


Therefore, $\hat{L}_{x} = \frac{1}{2}(2)\hbar = \sqrt[]{ 3 }\hbar$

## d

![[Pasted image 20260410093900.png]]
