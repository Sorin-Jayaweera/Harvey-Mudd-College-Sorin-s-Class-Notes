
![[Pasted image 20260318223537.png]]
We can write
$$
\begin{align}
\bra{n} \hat{a}^{\dagger}\hat{a} \ket{n}  & = c^{*}_{-}c_{-} \braket{ n-1 | n-1 }  \\
n  & = c^{*}_{-} c_{-}  \\
c_{-}  & = \sqrt[]{ n }  \\
\hat{a}\ket{n}  & = \sqrt[]{ n } \ket{n-1} 
\end{align}
$$


![[Pasted image 20260318223546.png]]

![[Pasted image 20260318224345.png]]

For $n=0$,
$\ket{0}= 1\ket{0}$
For $n=1$
$$
\begin{align}
\ket{n}= \frac{a^{\dagger}}{\sqrt[]{ 1! }}\ket{0} \\
 & = \frac{1}{\sqrt[]{ 1! } }\ket{0+1}  \\
 & = 1 \ket{1} 
\end{align}
$$
For an arbitrary $n$ greater than $1$
$$
\begin{align}
 \frac{(a^{\dagger})^{n}}{\sqrt[]{ n! } } \ket{0}  & = \sqrt[]{ 1 } \frac{(a^{\dagger})^{n-1}}{\sqrt[]{ n! } }\ket{1} \\ \\
 & = \sqrt[]{ 2 } \sqrt[]{ 1 } \frac{(a^{\dagger})^{n-2}}{\sqrt[]{ n } !}\ket{2}  \\
& = \frac{\sqrt[]{ k}!}{\sqrt[]{ n } !} (a^{\dagger})^{n-k}\ket{k} 
\end{align}
$$
for the special case of $k=n$, this gets up to
$$
\begin{align}
\frac{\sqrt[]{ n }!}{\sqrt[]{ n }}(a^{\dagger})^{0}\ket{n} \\
 & = \ket{n}   
\end{align}
$$

![[Pasted image 20260318224141.png]]

state has $\ket{0}\text{ and } \ket{1}$ superposition, and we'll have a cos something for expectation value
we have the state
$$
\begin{align}
\ket{\psi} = \frac{1}{\sqrt[]{ 2 } }(\ket{0} + e^{i\phi}\ket{1})
\end{align}
$$

We can use the average value of momentum at time zero to work out the phase difference between $\ket{0} \text{ and } \ket{1}$.

We can write $\hat{p}_{x}$ in terms of $\hat{a}$ and $\hat{a}^{\dagger}$.

![[Pasted image 20260326131645.png]]

If $\left< \hat{p}_{x} \right>=0$ at $t=0$, we can write
$$
\begin{align}
0 &  = \bra{\psi} \hat{p}_{x} \ket{\psi}  \\
 & = \frac{1}{\sqrt[]{ 2 } }(\bra{0} +\bra{1} ) \hat{p}_{x} (\ket{0} +\ket{1} ) \\
 & = \frac{1}{\sqrt[]{ 2 } } ((\bra{0} + \bra{1} )\hat{p}_{x} \ket{0} +(\bra{0} + \bra{1} )\hat{p}_{x} \ket{1} )  \\
 & = \frac{-1}{\sqrt[]{ 2 } } \sqrt[]{ \frac{m\omega \hbar}{2} }  \bigg( (\bra{0} +\bra{1}  ) (\hat{a}-\hat{a}^{\dagger} )\ket{0} +(\bra{0} +\bra{1}  ) (\hat{a}-\hat{a}^{\dagger}) \ket{1}  \bigg)   
 \end{align}
$$


$\hat{a}\ket{n}=\sqrt[]{ n }\ket{n-1}$
$a^{\dagger}\ket{n}=\sqrt[]{ n+1 }\ket{n+1}$

$$
\begin{align}
\hat{a}\ket{0} &  = 0 \\
\hat{a} \ket{1}  & = 1 \ket{0} \\
\hat{a}^{\dagger} \ket{0}  & =  1\ket{1}  \\
\hat{a}^{\dagger}\ket{1}  & = \sqrt[]{ 2 } \ket{2} 
\end{align}
$$
we can decompose the terrible
$$
\begin{align}
 \bigg( (\bra{0} +\bra{1}e^{-i\phi}  ) (\hat{a}-\hat{a}^{\dagger} )\ket{0} +(\bra{0} +\bra{1}e^{-i\phi}  ) (\hat{a}-\hat{a}^{\dagger}) \ket{1}e^{i\phi}  \bigg)   
\end{align}
$$

$$
\begin{align}
(\bra{0} + \bra{1} e^{-i\phi})(-1\ket{1} )+ (\bra{0} +\bra{1}e^{-i\phi} )(\ket{0}e^{i\phi} - \sqrt[]{ 2\ket{2}  }e^{i\phi} )
\end{align}
$$


Because we have the common $\frac{1}{\sqrt[]{ 2 }}$ terms on each bra and ket pair, we'll get
we have an $e^{i\phi}$ from the $\ket{1}$ term that went down to $\ket{0}$, and an $e^{-i\phi}$ term from the $\ket{0}$ that went up to $\ket{1}$ and now hit the $\bra{1}e^{-i\phi}$ term - the others are all orthogonal
$$
\begin{align}
\frac{1}{2}(e^{i\phi}- e^{-i\phi})
\end{align}
$$
Which looks like 
$$
\begin{align}
i\sin \phi
\end{align}
$$
Therefore, we have 
$$
\boxed{
\begin{align}
\left< \hat{p}_{x}  \right> = \sqrt[]{ \frac{m\omega \hbar}{2} } \sin \phi
\end{align}
}
$$
![[Pasted image 20260330092958.png]]
So we have
$\sin \phi=1$ since there is no time dependence in the expectation value at t = 0 (??? this feels weird)
$\phi=\frac{\pi}{2}$.

The state is therefore
$$
\boxed{
\begin{align}
 & \frac{1}{\sqrt[]{ 2 } }\ket{0} + \frac{1}{\sqrt[]{ 2 } }e^{\frac{\pi}{2}}\ket{1}  \\
 & = \frac{1}{\sqrt[]{ 2 } }\ket{0} + \frac{i}{\sqrt[]{ 2 } }\ket{1} 
\end{align}
}
$$

We can time evolve the state with
$$
\begin{align}
 & e^{-i \frac{E}{\hbar}t}\left( \frac{1}{\sqrt[]{ 2 } }\ket{0} + \frac{i}{\sqrt[]{ 2 } }\ket{1}  \right) \\
 & = \frac{1}{\sqrt[]{ 2 } }e^{\frac{i\omega}{2} t}\ket{0} + \frac{i}{\sqrt[]{ 2 } }e^{\frac{3}{2} \omega t} \ket{1}  \\
 & = \frac{1}{\sqrt[]{ 2 } }e^{\frac{i\omega}{2}t}\left( \ket{0}+ i e^{\omega t}\ket{1}   \right)
\end{align}
$$
We can just tack on this phase to our expectation value calculation from earlier, to get
$$
\begin{align}
\boxed{
\begin{align}
\left< \hat{p}_{x}  \right>(t) = \sqrt[]{ \frac{m\omega \hbar}{2} } \sin \left( \frac{\pi}{2}+\omega t \right)
\end{align}
}
\end{align}
$$


![[Pasted image 20260324162635.png]]



![[Pasted image 20260318224153.png]]

![[Pasted image 20260322152716.png|300]]
We can apply Ehrenfest's theorem to see if the relation holds.  
$$
\begin{align}
\frac{d}{dt} \left< x \right>  & \stackrel{?}{=} \frac{1}{m} \left< p_{x}   \right>\\ \\
  -A\omega \sin(\omega t+\delta)  & = -m\omega \frac{A}{A}\sin(\omega t+\delta) 
\end{align}
$$
and
$$
\begin{align}
\frac{d}{dt} \left< p_{x}  \right>  & \stackrel{?}{=}   \frac{i}{\hbar} \bra{\psi} [\hat{H},\hat{p}_{x} ]\ket{\psi} 
\end{align}
$$
![[Pasted image 20260330095021.png]]

The commutation between $\hat{H}$ and $\hat{p}_{x}$ is
$$
\begin{align}
 & \left( \hat{a}^{\dagger}\hat{a}+\frac{1}{2} \right)(\hat{a}-\hat{a}^{\dagger}) -(\hat{a}-\hat{a}^{\dagger})\left( \hat{a}^{\dagger}\hat{a}+\frac{1}{2} \right) \\
 & = \hat{a}^{\dagger}\hat{a}(\hat{a}-\hat{a}^{\dagger})- (\hat{a}-\hat{a}^{\dagger})(\hat{a}^{\dagger}\hat{a}) \\
 & = \hat{a}^{\dagger}\hat{a}\hat{a} - \hat{a}^{\dagger}\hat{a}\hat{a}^{\dagger} - (\hat{a}\hat{a}^{\dagger}\hat{a}-\hat{a}^{\dagger}\hat{a}^{\dagger}\hat{a}) \\
 & = \hat{a}^{\dagger}\hat{a}\hat{a} - \hat{a}^{\dagger}\hat{a}\hat{a}^{\dagger} - \hat{a}\hat{a}^{\dagger}\hat{a}+\hat{a}^{\dagger}\hat{a}^{\dagger}\hat{a}
\end{align}
$$
$$
\begin{align}
\hat{a}^{\dagger}(\hat{a}\hat{a}+\hat{a}^{\dagger}\hat{a}-\hat{a}\hat{a}^{\dagger}) - \hat{a}\hat{a}^{\dagger}\hat{a}
\end{align}
$$
We know that $[\hat{a},\hat{a}^{\dagger}]=1$, and conversely that $[\hat{a}^{\dagger},\hat{a}]=-1$

$$
\begin{align}
\hat{a}^{\dagger}(\hat{a}\hat{a} - 1) - \hat{a}\hat{a}^{\dagger}\hat{a} \\
\hat{a}^{\dagger}\hat{a}\hat{a}-\hat{a}\hat{a}^{\dagger}\hat{a}-\hat{a}^{\dagger} 
\end{align}
$$
which looks like
$$
\begin{align}
 & (\hat{a}^{\dagger}\hat{a}-\hat{a}\hat{a}^{\dagger})\hat{a} - \hat{a}^{\dagger}  \\
 & = -\hat{a}-\hat{a}^{\dagger} \\
 & =- (\hat{a}+\hat{a}^{\dagger})
\end{align}
$$
With constants, we have
$$
\begin{align}
[\hat{H},\hat{p}_{x} ]=-\left( \hbar \omega \right)\left( i\sqrt[]{ \frac{m\omega \hbar}{2} }  \right)(\hat{a}+\hat{a}^{\dagger})
\end{align}
$$
![[Pasted image 20260330100606.png]]

$$
\begin{align}
\hat{x}\sqrt[]{ \frac{2m\omega}{\hbar} } = (\hat{a}+\hat{a}^{\dagger})
\end{align}
$$
so
$$
\begin{align}
 & [\hat{H},\hat{p}_{x} ] = - i\hbar \omega\sqrt[]{ \frac{m\omega \hbar}{2} } \sqrt[]{ \frac{2m\omega}{\hbar} } \hat{x}  \\
 & = -i \hbar \omega m\omega \hat{x} \\
 & = -i \hbar m \omega^{2}\hat{x}
\end{align}
$$

Finally we can check
![[Pasted image 20260330102022.png]]

$$
\begin{align}
\frac{d}{dt} \left< p_{x}  \right>  & \stackrel{?}{=}   \frac{i}{\hbar} \bra{\psi} [\hat{H},\hat{p}_{x} ]\ket{\psi} 
\end{align}
$$
because we have $\frac{i}{\hbar}$, the $i\hbar$ just goes to $-1$.
$$
\begin{align}
\frac{d}{dt} \left< p_{x}  \right> \stackrel{?}{=} -m\omega^{2}\left< \hat{x} \right> 
\end{align}
$$

$$
\begin{align}
\frac{ d }{d t } \left< p_{x}  \right> = m\omega^{2}A\cos(\omega t+\delta)
\end{align}
$$
Which is indeed $m\omega^{2}\left< \hat{x} \right>$

Thus, both parts of Ehrenfest's theorem are satisfied.


![[Pasted image 20260318224204.png]]

![[Pasted image 20260401091014.png|300]]

We have the ground state in a simple harmonic oscillator given as
$$
\begin{align}
\braket{ x | 0 } = \left( \frac{m\omega}{\pi \hbar} \right)^\frac{1}{4}e^{-m\omega \frac{x^{2}}{2\hbar}}
\end{align}
$$
from pg 255 eq 7.44
We can find the probability of landing within this area as


$$
\begin{align}
& \int_{-x_{0}}^{x_{0}} \psi ^{*}\psi \\  
 & = \left( \frac{m\omega}{\pi \hbar} \right)^\frac{1}{2}\int_{-x_{0}}^{x_{0}} e^{-m\omega \frac{x^{2}}{\hbar}}dx \\
\end{align}
$$

For the SHO, we use a potential function
$$
\begin{align}
\frac{1}{2}kx^{2} = \frac{1}{2}m \omega^{2}x^{2}
\end{align}
$$
We know that $E=\hbar \omega\left( n+\frac{1}{2} \right)$, so 
for the ground state$E=\frac{\hbar \omega}{2}$.
We can solve for where
$$
\begin{align}
\frac{1}{2}m\omega^{2}x^{2} = \hbar \frac{\omega}{2} \\
x = \sqrt[]{ \frac{\hbar}{m\omega} } 
\end{align}
$$

**I couldn't figure out the Usub and didn't know what the Error Function was, so I took a hit and looked up the integral on symbolab, knowing that I would dock points for it. Sorry! I am running out of time to submit and didn't want to loose everything else for not figuring out an integral that was easily computable online. **


$$
\begin{align}
 & = \frac{1}{2}\left( \frac{m\omega}{\pi \hbar} \right)^{\frac{1}{2}}\left( \sqrt[]{\frac{\pi\hbar}{ m\omega } } \right) erf\left( \sqrt[]{ \frac{m\omega}{\hbar} } x \right)\bigg|_{-x_{0}}^{x_{0}}   \\
 & = \frac{1}{2} \text{ erf }\left( \sqrt[]{ \frac{m\omega}{\hbar} } x  \right)\bigg|_{-x_{0}}^{x_{0}}   \\
 & = \frac{1}{2} \left( erf\left(\underbrace{  \sqrt[]{ \frac{m\omega}{\hbar} } \sqrt[]{ \frac{\hbar}{m\omega} }  }_{ 1 } \right)-erf\left(-1 \right) \right)
\end{align}
$$

$erf(1)=0.842$
$erf(-1)=-0.842$

So this just gets to 
$P(\text{ allowed })=0.842$
thus, 
$P(\text{ not classical})=0.158$


![[Pasted image 20260318224216.png]]

The ground state in each well is given by
$$
\begin{align}
\braket{ x | 0 } = \left( \frac{m\omega}{\pi \hbar} \right)^{\frac{1}{4}}e^{-m\omega \frac{x^{2}}{2\hbar}}  \\ 
\end{align}
$$

If we call the initial state $\ket{i}$ and the final state $\ket{f}$, then this is the same as asking
$$
\begin{align}
\braket{ f | i } 
\end{align}
$$

$$
\begin{align}
\int_{-\frac{L}{2}}^{\frac{L}{2}}  dx \braket{ f | x } \braket{ x | i }   
\end{align}
$$
because the initial function is zero outside the length $L$.

For the first ground state,
$$
\begin{align}
\omega_{0}=\sqrt[]{ \frac{g}{L} } 
\end{align}
$$
For the second ground state,
$$
\begin{align}
\omega & = \sqrt[]{ \frac{g}{4L} }  \\
 & = \frac{1}{2}\sqrt[]{ \frac{g}{L} }  \\
 & = \frac{1}{2} \omega_{0}
\end{align}
$$

Therefore, we have
$$
\begin{align}
  & \int_{-\frac{L}{2}}^{\frac{L}{2} }dx \left( \frac{m\omega_{0}}{\pi \hbar} \right)^{\frac{1}{4}}\left( \frac{m\omega}{\pi \hbar} \right)^\frac{1}{4}e^{-m\omega_{0} \frac{x^{2}}{2\hbar}}e^{-m\omega \frac{x^{2}}{2\hbar}} \\
 & = \left( \frac{m^{2}\omega\omega_{0}}{\pi \hbar} \right)^\frac{1}{4}\int_{-\frac{L}{2}}^{\frac{L}{2}} dx\,\,\,e^{-m\frac{x^{2}}{2\hbar}(\omega_{0}+\omega)}
\end{align}
$$
Using the appendix, 
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-ax^{2}} = \sqrt[]{ \frac{\pi}{a } } 
\end{align}
$$
Here, $a = \frac{m}{2\hbar}(\omega_{0}+\omega)$
So we have

$$
\begin{align}
 & \left( \frac{m^{2}\omega \omega_{0}}{\pi^{2} \hbar^{2}} \right)^{\frac{1}{4}}\sqrt[]{ \frac{2\hbar \pi}{m(\omega+\omega_{0})} }  \\
 & = \left(\frac{1}{2\pi^{2} \hbar^{2}}  m^{2} \frac{1}{2}\omega_{0}^{2} \right)^\frac{1}{4}\left( \frac{4\hbar^{2}\pi^{2}}{m^{2}\left( \frac{3}{2 }\omega_{0} \right)^{2}} \right)^\frac{1}{4}  \\
 & = \frac{2}{3}
\end{align}
$$



