
>[!abstract]+ Recall:Properties of Hermitian Operators
>Real eigenvalues: $A_{op}\psi _{n}(x)=a_{n}\psi _{n}(x), a_{n}\in \mathbb{R}^{}$
>Orthogonal eigenfunctions for non-degenerate eigenvalues
>(A degenerate eigenvalue is when two states have the same eigenvalue)
>The eigenfunctions are complete, meaning that any physical wave function can be written as 
>$$
>\begin{align}  \\
> \Psi(x) = \sum_{n}^{} c_{n}\psi _{n}(x) \text{ where } \\
>c_{n}=\int_{-\infty}^{\infty} \psi _{n}^{*}\Psi _{x} dx \\
>\end{align}
>$$


The probability of measuring eigenvalue $a_{n}$ is $P(a_{n})=\lvert c_{n} \rvert^{2}$

Now on to the lecture:
Rotations 90 degrees about orthogonal axes don't commute, as the order or rotations matters:


## Commutator
This is the difference applying the operators in order:
$$
\begin{align}
[A_{op}  ,B_{op}  ]=A_{op}  B_{op}  -B_{op}  A_{op}  
\end{align}
$$
To actually calculate it, we must apply to a state $\Psi$.

The commutator is found with:
$$
\begin{align}
\left[ A_{op},B_{op} \right] \psi =A_{op} (B_{op} \psi)-B_{op} (A_{op} \psi)
\end{align}
$$
We can choose any $\psi$ to get information, as they will apply equally to any.

For example:
Find the commutator:

$$
\begin{align}
\left[ x_{op} ,x_{op} ^{n} \right] \psi (x)=x_{op} (x^{n}_{op} \psi (x))-x_{op} ^{n}(x_{op} \psi(x))
\end{align}
$$
We define $x_{op}=x$
So we get
$$
\begin{align}
x(x^{n}\psi(x))-x^{n}x\psi(x) \\
= 0
\end{align}
$$
This is true in general: any commutator commutes with itself. Its the same operation, so it can be done any number of times and the order doesn't matter.

Lets do something more: Lets check that $\Pi_{op}$ (parity) commutes with the Hamiltonian of the simple harmonic oscillator: 
$H_{SHO}=-\frac{\hbar^{2}}{2m}\frac{ \partial  }{ \partial x^{2} }+\frac{1}{2m\omega_{0}^{2}x_{op}^{2}}$

$$
\begin{align}
\left[ H_{op} (x),\Pi_{op}  \right]\psi(x) = H_{op} (\psi (-x))-\Pi_{op} (H_{op} \psi(x)) \\
\end{align}
$$
Lets simplify the farthest right term 
$$
\begin{align}
\Pi_{op} (H_{op} \psi(x))=\Pi_{op} \left( -\frac{\hbar^{2}}{2m}\frac{ \partial^{2} }{ \partial x^{2} } +\frac{1}{2m\omega_{0}^{2}x^{2}} \right)\psi(x) \\
= \left( -\frac{\hbar^{2}}{2m}\underbrace{ \frac{ \partial^{2} }{ \partial (-x)^{2} } }_{ \text{ unchanged, -1*-1=1 } } +\frac{1}{2}m\omega_{0}^{2}\underbrace{ (-x)^{2} }_{ unchanged } \right) \psi(-x) \\
= H_{op} \Psi (-x)
\end{align}
$$
This is the same as our first term from our commutator expression, so the result is 0. The parity operator commutes with the parity operator. The important thing here is that the potential energy function was even, so it respects parity. 

There are many operators that don't commute:
$$
\begin{align}
\left[ X_{op} ,P_{op}  \right] \psi=x_{op} (p_{op} \psi)-p_{op} (x_{op} \psi)
\end{align}
$$
We know how to express the operators if talking about the basis of position:
$$
\begin{align}
= x \frac{\hbar}{i}\frac{d }{dx} \psi - \frac{\hbar}{i}\frac{d}{dx} (x\psi) \\
= \frac{\hbar}{i}\left( x\frac{d \psi}{dx} -\left( \psi+x\frac{ d \psi }{d x }  \right) \right) \\
= -\frac{\hbar}{i}\psi \\
[x_{op} ,p_{op} ] \psi= i\hbar \psi \\
[x_{op} ,p_{op} ] = i\hbar
\end{align}
$$
Whenever two Hermitian operators don't commute, the commutator tells us about the uncertainty of the measurements we would get from those operators. If we have two operators that do commute, we can simultaneously have a particle be in an eigenstate for both. But! If they don't commute, then we can never find a particle to be in an eigenstate of both operators. This gives us some range of possibilities that correspond to those operators.

Whenever we find two operators that commute with each other, we are guaranteed a set of eigenfunctions that are common - not all, but a complete set (it spans the space).

## Commuting operators
If $[A_{op},B_{op}]=0,$ there exists a set of eigenstates $\psi _{n}$ that are eigenstates of both operators $A_{op}\text{ and } B_{op}$
$A_{op}\psi=a_{n}\psi _{n}$
$B_{op}\psi _{n}=b_{n}\psi _{n}$
Simultaneously have solutions.
$$
\begin{align}
A_{op} (B_{op} \psi _{n})=A_{op} b_{n}\psi _{n}=a_{n}b_{n}\psi _{n} \\
B_{op} (A_{op} \psi _{n})=B_{op} a_{n}\psi _{n}=b_{n}a_{n}\psi _{n}
\end{align}
$$
 When commuters commute, it is always possible to find functions that are simultaneously eigenfunctions of both operators. This is true in both directions of implication.
Lets assume $[A_{op},B_{op}]=0$. Lets define $\psi _{n}:A_{op}\psi _{n}=a_{n}\psi _{n}$.

$B_{op}(A_{op}\psi _{n})=B_{op}(a_{n}\psi _{n})$
We use the fact that $[A_{op},B_{op}]$ commute:
$$
\begin{align}
A_{op} (B_{op} \psi _{n})=a_{n}(B_{op} \psi _{n})
\end{align}
$$
$B_{op}\psi _{n}\propto \text{ eigenstate of  } A_{op}$
Writing this out gives us
$B_{op}\psi _{n}=b_{n}\psi _{n}$
Low and behold - we've got this proportionality constant and named it $b_{n}$!




### Implications of commutation:
For example: 
$H_{\text{ free }}=-\frac{\hbar^{2}}{2m}\frac{ d ^{2} }{d x^{2} }, p_{op}=\frac{\hbar}{i}\frac{ d  }{d x }$
These commute because its just $p$ to some power. 
$$
\begin{align}
\psi _{k}=e^{ikx},  \\
H_{\text{ free }}e^{ikx} = -\frac{\hbar^{2}}{2m}(ik)^{2}e^{ikx}= \frac{\hbar^{2}k^{2}}{2m}e^{ikx}
\end{align}
$$
Recall that for an infinite square well,
$$
\begin{align}
\sin(kx) \text{ was a solution to } H_{\text{ free }}
\end{align}
$$
This is an eigenstate of $H_{\text{ free }}$ that is not an eigenstate of $p_{op}$. However, we can find a superposition of solutions that is an eigenstate of the momentum operator. 

This comes from the fact that there is some degeneracy here. There are two different momentum states (going left or right) that correspond to the same energy. 

Any time we have a non zero commutator, that implies an uncertainty principle. 
![[Pasted image 20250224105150.png]]
![[Pasted image 20250224105203.png]]
