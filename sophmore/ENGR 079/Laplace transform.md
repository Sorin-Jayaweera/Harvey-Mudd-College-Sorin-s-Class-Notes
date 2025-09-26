The Laplace transform $L[]$ is an operator. Given some time-varying function f(t), the (one-sided) Laplace transform of f(t) is denote by $F(s)$, where $s$ is some complex variable.



$L[f(t)]=F(s)$
$L[f(t)]=\int_{0}^{\infty} f(t)e^{-st} \, dt=F(s)$
Lets do a nice example.
$L[1]=\int_{0}^{\infty}  1 * e^{-st}\, dt$

![[Pasted image 20240909191507.png]]
When we shift by $T$ in the time world, we multiply by $$
\begin{align}
e^{-sT}
\end{align}
$$in the Laplace world.

Feeding the derivative of a function into the Laplace gets
![[Pasted image 20240909191951.png]]

We also have an integration rule.
![[Pasted image 20240909192308.png]]
![[Pasted image 20240916101246.png]]
![[Pasted image 20240916101257.png]]
![[Pasted image 20240911170850.png]]
![[Pasted image 20240911170753.png]]

Final value theorem

![[Pasted image 20240920153313.png]]