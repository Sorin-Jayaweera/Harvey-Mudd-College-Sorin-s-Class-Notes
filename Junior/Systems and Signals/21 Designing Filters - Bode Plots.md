We can make bode plots by analyzing our $X(j\omega)$ expression.
![[20251113_103037.jpg]]

This is huge. This tells us how we can build filters to perform different behaviors. We have zeros as the numerator and poles as the denominator. 

![[20251113_104453.jpg]]

If the region of convergence contains the $j\omega$ axis, it is stable, otherwise unstable. If it lies on the right half plane entirely, it is causal. If it involves the left half plane, it is non causal. 


Aside: Unilateral Laplace transform
We are assuming that we have a right sided signal where it is 0 before $t=0$
![[Pasted image 20251113105117.png]]
