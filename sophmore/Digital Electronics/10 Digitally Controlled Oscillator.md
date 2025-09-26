![[Pasted image 20250220140954.png]]


Fractions are fixed point or floating point ( scientific notation)

## Fixed point:
We choose how many bits are integer vs fraction
01101100 => 0110.1100 =>
$$
\begin{align}
2^{2}+2^{1}+2^{-1}+2^{-2} = 6.75
\end{align}
$$
But we could change where the decimal is. 
We have some notation. We us
$Ua.b$ as an unsigned number with $a$ integer bits and $b$ fractional bits.
EX: 
![[Pasted image 20250220142114.png]]

![[Pasted image 20250220141623.png]]
![[Pasted image 20250220141827.png]]

Floating point can represent a wider overall range but with less precision, takes care of overflow, but takes more gates and bits to store data.

![[Pasted image 20250220142558.png]]
![[Pasted image 20250220142715.png]]We know that the leading bit is always one, so we can leave off the leading digit as long as we remember to add it on. 

We store the exponent as the actual exponent (i.e. 7) + a bias, which was decided to be 127. 
![[Pasted image 20250220142934.png]]