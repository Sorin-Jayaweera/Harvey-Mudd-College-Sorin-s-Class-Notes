There are 2 main concepts that we want to focus on. 
1) The distinction between continuous and discrete signals
2) Fourier Series vs Fourier transforms

There exist all 4 combinations between these two -continuous time Fourier series, a discrete time Fourier series, continuous time Fourier transforms, and discrete time Fourier transforms. 


## Signals
A signal is a function of 1 or more independent variables.
Examples: A pressure wave. Pressure at a position could be a function of time (speaking at a microphone).

We represent signals in the time domain or frequency domain usually (Fourier methods). 

If we know the behavior of basic signals really well, then if a more complex function is a linear combination of them, then the output is a linear combination of the simpler inputs. 

Take two inputs to a linear time invariant system. The outputs are just a combination of the individual function outputs. 
![[Pasted image 20250826100508.png]]

Really, passing any functions of basic signals makes the sum of the outputs on those basic signals. 
$$
\begin{align}
ax_{1}+bx_{2}\implies ay_{1}+by_{2}
\end{align}
$$



## Continuous Time Signals
We denote continuous time by  $x(t)$, whereas discrete time is $x[t]$. X is not defined if the argument $t$ is not an integer - its a "sample number". 

