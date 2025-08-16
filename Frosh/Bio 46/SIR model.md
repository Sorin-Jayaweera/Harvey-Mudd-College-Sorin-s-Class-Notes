SIR: susceptible, infected, recovered.

First, some definitions:
#epidemiology: the study of the distribution and causes of disease in populations.
#endemic: an infectious disease that is present at a baseline level in a population
#epidemic: an increase and spread of an infectious disease through a population
#pandemic: an epidemic that spans multiple regions.


Infectious diseases can spread via several ways, such as
1) Environmental source (eg Cholera, tetanus)
2) Direct person-to-person (influenza, Sars-covid, gonorrhea)
3) Vector-borne (eg. malaria, Lyme)

We use mathematical models to see what happens to a population


## SIR Model:
susceptible, infectious, recoverable compartment model:
We are trying to understand what happens during an epidemic. 
![[Pasted image 20240219091904.png|300]]


![[Pasted image 20240219091820.png|300]]
![[Pasted image 20240219092330.png|300]]
(yellow is recovered).

SIR is a "compartment model".
let
$$
\begin{align} \\
N = \text{ Total population size } \\
S =\text{ Number of susceptible people } \\
I = \text{ Number of infected people } \\
R = \text{ Number of recovered people } \\
\text{ There do not exist people outside of these groups } \\
S+I+R=N
\end{align}
$$
This is a logical one way process, $S\to I\to R$.
We can conceptually model this as a differential equation.
![[Pasted image 20240219093450.png|300]]
![[Pasted image 20240219093838.png|300]]

![[Pasted image 20240219093825.png|300]]
In the beginning of an outbreak, $\frac{N}{S}$ is close to one and an outbreak is going to start. $\frac{b}{\gamma}=R_{0}$. If $R_{0}>1,\text{ the infection will spread. If } R_{0}<1\text{ The infection will die }$

