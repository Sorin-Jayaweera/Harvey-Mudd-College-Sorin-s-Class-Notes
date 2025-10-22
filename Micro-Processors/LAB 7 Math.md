Thing on MCU, thing on FPGA, they talk to each other. 

Accelerator for AES encryption


## Accelerator
A hardware algorithm that can run in parallel and saves power, runs faster

The SPI link (for it to actually accelerate) must be fast enough to allow the high speed computation between chips.


## Encryption
A and B send an encrypted message in cypher text (as opposed to plain text) so that only A and B can understand -- no one listening could decode it. 

How do we go from plain text (hello!) 


## MATH

We have fields, which are sets that are closed under addition and multiplication. 
There are identities: $a+0=a,a*1=a$
Fields have inverses. - so we have $a\text{ and } b$ as members in a set, such that $a+b=0,ab=1$. 

### Galois Field
Members are polynomials
coefficients are 0 or 1
We mod relative to primes

We have polynomials, for example
$x^{8}+x^{4}+x^{3}+x+1$
Because we only allow $0$ or $1$ coefficients, if we add together $x^{3}+x^{3}$ we carry over the 1 to get an $x^{4}$. 

Adding is an XOR of coefficients. $\times$ operator is a left shift of coefficients. 
This is really easy to implement as a logic system. 