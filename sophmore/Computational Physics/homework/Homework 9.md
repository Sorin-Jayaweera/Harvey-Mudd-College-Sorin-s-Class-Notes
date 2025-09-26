![[Pasted image 20250401092927.png|700]]

We know that Area is the derivative of Volume. This tells us:
$$
\begin{align}
\frac{ d V}{d x } =nC_{n} r^{n-1}=S_{n} r^{n-1}
\end{align}
$$
This tells us
$$
\begin{align}
c_{n} = \frac{S_{n}}{n} \\
S_{n} = nc_{n} 
\end{align}
$$

$$
\begin{align}
S_{n} = \frac{A}{r^{n-1}} \\
r^{n } = \frac{v}{C_{n}} \\
r^{n-1} = \frac{r^{n}}{r} = \frac{v}{C_{n}r } \\
S_{n} = \frac{AC_{n}r}{v}
\end{align}
$$


![[Pasted image 20250401092940.png|700]]
We can write out our integral:

$$
\begin{align}
2\pi \int_{0}^{\infty} e^{-a(n_{1}^{2}+n_{2}^{2}+\dots+n_{k} ^{2})}r^{n-1}dr \\
= 2\pi \int_{0}^{\infty} dn_{1} e^{-an_{1}^{2}} \int_{0}^{\infty}dn_{2}   e^{-an_{2}^{2}} \dots\int_{0}^{\infty}dn_{3} \,   e^{-an_{k} ^{2}} r^{n-1} 
\end{align}
$$
Each of these individually evaluates to $\sqrt[]{ \frac{\pi}{\alpha} }$, so we have the product of $n$ copies of $\sqrt[]{ \frac{\pi}{a} }$.
If I call the variable that is counting the dimension $n$ instead of $k$, (OOPS)
We have
$$
\begin{align}
\int_{0}^{\infty} e^{-\alpha r^{2}}s_{n} r^{n-1}dr= \left( \frac{\pi}{\alpha} \right)^{\frac{n}{2}}
\end{align}
$$


![[Pasted image 20250401092947.png|700]]
We can represent our function as similar to the gamma function by recognizing that the two forms look similar.
$$
\begin{align}
\Gamma(n) = \int_{0}^{\infty} x^{n-1}e^{-x} dx
\end{align}
$$
We can write out: 

$$
\begin{align}
s_{n}\int_{0}^{\infty} e^{-ar^{2}}r^{n-1}dr = \int_{0}^{\infty} x^{n-1}e^{-x}dx
\end{align}
$$
We can define 
$$
\begin{align} 
ar^{2}=x \\  
r= \left( \frac{x}{\alpha} \right)^{\frac{1}{2}}\\
2\alpha r dr = dx 
\end{align}
$$
This lets us substitute into the equation to get
$$
\begin{align}
s_{n} \int_{0}^{\infty} e^{-x} \left( \frac{x}{\alpha} \right)^{\frac{n-1}{2}} \frac{1}{2\alpha r}dx
\end{align}
$$
We can pull out the constants, and this looks like a gamma function:
$$
\begin{align}
=\frac{s_{n}}{2\alpha} \alpha^{\frac{1}{2}} \frac{1}{\alpha^{\frac{n-1}{2}}} \int_{0}^{\infty} e^{-x}x^{\frac{n-1}{2}} \left( \frac{1}{x} \right)^{\frac{1}{2}} dx \\
= \frac{s_{n}}{2} \frac{1}{\alpha^{\frac{1}{2}}\alpha^{\frac{n-1}{2}}}\int_{0}^{\infty} e^{-x} \frac{x^{\frac{n-1}{2}}}{x^{\frac{1}{2}}} dx  \\
= \frac{s_{n}}{2} \frac{1}{\alpha^{\frac{n}{2}}}\int_{0}^{\infty} e^{-x}x^{\frac{n-2}{2}} \\
= \frac{s_{n}}{2} \frac{1}{\alpha^{\frac{n+1}{2}}}\int_{0}^{\infty} e^{-x}x^{\frac{n}{2}-1}  \\
= \frac{s_{n}}{2} \frac{1}{a^{\frac{n}{2}}}\Gamma \left( \frac{n}{2} \right)
\end{align}
$$
We therefore have the expression
$$
\begin{align}
\frac{s_{n}}{2} \frac{1}{\alpha^{\frac{n}{2}}}\Gamma\left( \frac{n}{2} \right) = \left( \frac{\pi}{\alpha} \right)^{\frac{n}{2}}
\end{align}
$$

We can rearrange to get
$$
\begin{align}
s_{n}  & =2 \left( \frac{\pi}{\alpha} \right)^{\frac{n}{2}} \alpha^{\frac{n}{2}} \frac{1}{\Gamma\left( \frac{n}{2 } \right)} \\
 & =\frac{2\pi^{\frac{n}{2}}}{\Gamma\left( \frac{n}{2 } \right)} 
\end{align}
$$

We can rearrange for $C_{n}$. We know that
$$
\begin{align}
c_{n} = \frac{S_{n}}{n} \\
S_{n} = nc_{n} 
\end{align}
$$
This gives us
$$
\begin{align}
C_{n} = \frac{2\pi^{\frac{n}{2}}}{n\Gamma\left( \frac{n}{2} \right)}
\end{align}
$$
We can check with $n=2$ and $n=3$, since we know $A(2)=2\pi r,V(2)=\pi r^{2}$ and 
$A(3)=4\pi r^{2}, V(3) = \frac{4}{3}\pi r^{3}$

Our expression yields:
$$
\begin{align}
A(2) = S_{n}r^{n-1} \\
=\frac{2\pi^{\frac{n}{2}}}{\Gamma\left( \frac{n}{2} \right)} r^{n-1} \\
=\frac{2\pi}{\Gamma(1)}r \\
= 2\pi r
\end{align}
$$
$$
\begin{align}
V(2) = C_{n}r^{n} \\
=\frac{2\pi}{2}r^{2} \\
= \pi r^{2}
\end{align}
$$
This agrees for 2 dimensions.
$$
\begin{align}
A(3) = \frac{2\pi^{\frac{3}{2}}}{\Gamma\left( \frac{3}{2} \right)}r^{2} \\
= \frac{4\pi^\frac{3}{2}}{\sqrt[]{ \pi } }r^{2} \\
=  4\pi r^{2}
\end{align}
$$
$$
\begin{align}
V(3) = \frac{4\pi}{3}r^{3}
\end{align}
$$
These two also work.

Now we can find the parameters for a 6 dimensional sphere.
$$
\begin{align}
S_{n}(6) &  = \frac{2\pi^{3}}{\Gamma(3)} \\ 
  & =\frac{2\pi^{3}}{2} \\ 
 & =\pi^{3} \\

C_{n}  & = \frac{\pi^{3}}{6}
\end{align}
$$



![[Pasted image 20250401092955.png|700]]
We can simulate a sphere of radius 1.

I get that the volume of the 6 dimensional sphere is ~ 5.1. 

The coefficient $C$ = 5.1677. 

We see (for only 1 simulation at each point, so it looks somewhat messy), a trend of decreasing error. I would have to do more simulation to find if it is linear in log log.
![[Pasted image 20250407173732.png]]




![[Pasted image 20250401093006.png|700]]
We can do a change of variables:
$$
\begin{align}
\lambda = \frac{2\pi c}{\omega},  \\
\omega = \frac{2\pi c}{\lambda}\\ \\
d \lambda= -\frac{2\pi c}{\omega^{2}} d\omega\\
 \frac{- \omega^{2} d\lambda}{2\pi c } = d\omega  \\
 
\end{align}
$$

We can define 
$$
\begin{align}
\mathscr{P}(\lambda)  d\lambda  & = P(\omega) d\omega\\
\mathscr{P} (\lambda)d\lambda   & =  \frac{\hbar}{4\pi^{2}c^{2}} \left( \frac{2\pi c}{\lambda} \right)^{3} \frac{1}{e^{\frac{(2\pi c\hbar)}{\lambda k_{B}T}}-1} \frac{-\left( \frac{2\pi c}{\lambda} \right)^{2}}{2\pi c}d\lambda  \\
 & = -\frac{ \hbar (2\pi c)^{2}}{\lambda^{5}} \frac{1}{exp\left( \frac{2\pi c\hbar}{\lambda k_{B}T} \right)-1}d\lambda \\
\mathscr{P}(\lambda)d\lambda  & = -\frac{ 2h\pi c^{2}}{\lambda^{5}} \frac{1}{exp\left( \frac{2\pi c\hbar}{\lambda k_{B}T} \right)-1}d\lambda
\end{align}
$$


![[Pasted image 20250401093016.png|700]]
Plotting the power (without extra constants) as just
$$
\begin{align}
\frac{1}{\lambda^{5}} \frac{1}{e^\frac{1}{\lambda T}-1}
\end{align}
$$

gets this power distribution:
![[Pasted image 20250406124214.png]]
(with 3 different "T" values).

This shows that long wavelengths correspond to relatively low power density - so if we only measure those long wavelengths we are missing most of the information. Even very different temperatures will converge to similar power levels at long wavelengths, so we can't distinguish between them well. Thus, long wave would be pretty useless for getting temperature information (unless the constants dramatically shift the locations of the peak and the spacing between power values at those high wavelengths).

![[Pasted image 20250401093032.png|700]]
I generate a list of 1000 walks that go for 1000 steps each, and average their distances to compare with the predicted curve. I assume that this should be enough to get a good understanding about the overall behavior, even with all the randomness. I am assuming that the random function I choose acts randomly - random.sample().

The average distance appears close to the prediction, but error bars (SEM = $\frac{\sigma}{\sqrt[]{ n_{\text{ random walks }} }}$) are really small and don't encapsulate the curve at the high step limit. Note though - the error relative to the number of steps is basically zero. That means the $\sqrt[]{ n }$ approximation is highly accurate.



![[Pasted image 20250406113701.png|400]]
![[Pasted image 20250406120111.png|400]]
![[Pasted image 20250406122236.png|400]]
Code:
```python
import numpy as np

import random as rd

import matplotlib.pyplot as plt
def getDist(x,y):

    return np.sqrt(x**2 + y**2)

  

getDistv = np.vectorize(getDist)

def randomWalk(numSteps):

    positionsList = np.array([[0,0]])

    nArr = np.arange(0,numSteps+1,1)

  

    for i in range(numSteps):

  

        step = rd.sample([[-1,0],[1,0],[0,-1],[0,1]],1)

        newCoordX = positionsList[-1][0] + step[0][0]  

        newCoordY = positionsList[-1][1] + step[0][1]

        newCoords = np.array([[newCoordX,newCoordY]])

        positionsList = np.append(positionsList,newCoords,axis=0)

  

    distArr = getDistv(positionsList[:,0],positionsList[:,1])

    return positionsList, distArr, nArr
numWalks = 1000

numSteps = 1000

posArrays = []

distArrs = []

nArrs = []

for i in range(numWalks):

    p,d,n = randomWalk(numSteps)

    posArrays.append(p)

    distArrs.append(d)

    nArrs.append(n)

fig = plt.figure()

ax = fig.add_subplot(projection="3d")

for i in range(numWalks):

    ax.scatter(posArrays[i][:,0],posArrays[i][:,1],nArrs[i])

ax.set_title("Walk over time")

ax.set_xlabel("X pos")

ax.set_ylabel("Y pos")

ax.set_zlabel("Step #")


  

fig,ax = plt.subplots()

  

for i in range(numWalks):

   ax.plot(distArrs[i])

  

ax.plot(np.sqrt(nArrs[i]),label = "sqrt(n)")

  

ax.plot(np.average(distArrs,axis=0),label= "average")

ax.set_title("Distance over time")

ax.set_xlabel("Step")

ax.set_ylabel("Distance")

ax.legend()
```