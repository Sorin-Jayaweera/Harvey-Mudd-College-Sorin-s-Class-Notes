## Questions for Gallicchio
I am very confused by the eigenstates and operators for angular momentum when shown in matrix form, even though it looks very clean in $\braket{  |  }$ notation.

What are the uses/physical correspondence to the raising and lowering operators? 

What is $j$ for the states as basis - dimension? Something weird? 

## Rotators Do Not Commute, and Neither Do Generators

Rotations don't commute. Generators make rotations, so they don't either. 

Commutator of two operators:
$$
\begin{align}
[\hat{J}_{x},\hat{J}_{y}  ]= i\hbar \hat{J}_{z}  \\

[\hat{J}_{z},\hat{J}_{x}  ]= i\hbar \hat{J}_{y}
\end{align}
$$
These tell us about eigenstates of angular momentum operators.
## 3.2 Commuting Operators

If rotations commute, then
$$
\begin{align}
[\hat{A},\hat{B}]\equiv  \hat{A}\hat{B} - \hat{B}\hat{A} = 0
\end{align}
$$

And they both have eigenvalues corresponding to an eigenstate 
If $\hat{A}\ket{a}=a\ket{a}$ then $\hat{B}\ket{a}=b\ket{a}$
so we relabel the state
$\ket{a,b}$


## 3.3 Eigenvalues and Eigenstates of Angular momentum

Angular momentum operators:
![[Pasted image 20260203113305.png]]


Raising and lowering operators have eigenvalues of $m+1 \text{ or } m-1$.

They just step up/down angular momentum by 1 unit of $\hbar$. 
## 3.4 Matrix elements of raising and lowering operators

We have a thing called $j$ (dimension?) which make all the basis states, and from those we generate the matrix representations of raising and lowering operators.

## 3.5 Uncertainty Relations and Angular Momentum

For non commutative operators we have
$$
\begin{align}
\Delta J_{x} \Delta J_{y} \geq  \frac{\hbar}{2} \left| \left< J_{z}  \right>  \right|   
\end{align}
$$
