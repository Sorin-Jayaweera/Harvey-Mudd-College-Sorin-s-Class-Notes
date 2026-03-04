## P1
![[Pasted image 20260219195702.png]]
#### Bernoulli distribution: 
$$
\begin{align}
P(X=1)=p \\
P(X=0)=1-p \\
\end{align}
$$
PDF:
![[Pasted image 20260219200304.png|300]]
CDF:
![[Pasted image 20260219201144.png|300]]



This is a delta at each of the two binary choices. Those are the only possible two, so any other value on the graph is zero (do we need to show that it goes to inf, or just leave those two points only since that is the whole sample space?). The CDF just adds up the deltas that are to the left of whatever point. 

![[Pasted image 20260219195712.png]]
This shows the percentage that are $\leq 0.2$, which for large numbers is $0.2\%$.


![[Pasted image 20260219195717.png]]

$$
\begin{align}
p_{x} (X=k) = (1-p)^{k-1}p \\ 
k = 1,2,3,4,5
\end{align}
$$
This gives the CDF as
$$
\begin{align}
P_{x}= \sum_{k=0}^{x}p(1-p)^{k-1} 
\end{align}
$$
![[Pasted image 20260219211008.png|300]]



![[Pasted image 20260219195730.png]]

![[Pasted image 20260219210940.png|300]]



![[Pasted image 20260219195741.png]]

$$
\begin{align}
P(X=k) = \binom{n}{k} p^{k}(1-p)^{n-k} \\
\text{ for } k = 0,1,2,\dots n 
\end{align}
$$

![[Pasted image 20260219205205.png|300]]


![[Pasted image 20260219195748.png]]
![[Pasted image 20260219195759.png]]

![[Pasted image 20260219210825.png|300]]



## P2
![[Pasted image 20260219195826.png]]

![[Pasted image 20260219212510.png|300]]



$$
\begin{align}
P(\gamma_{\text{ lower }} \leq  x \leq \gamma_{\text{ upper }} ) = \frac{\gamma_{\text{ upper }}- \gamma_{\text{ lower }}  }{20}
\end{align}
$$


![[Pasted image 20260219195833.png]]

$$
\begin{align}
f_{X}(x;\lambda) = \begin{cases}
\lambda e^{-\lambda x}, x \geq  0 \\
0, x < 0
\end{cases} 
\end{align}
$$
$$
\begin{align}
F_{X}(x;\lambda) = \int_{0}^{x} \lambda e^{-\lambda x}dx
\end{align}
$$
PDFs:
![[Pasted image 20260219212932.png|600]]




CDFs:
![[Pasted image 20260219212901.png|600]]


![[Pasted image 20260219195839.png]]
![[Pasted image 20260219213955.png]]

![[Pasted image 20260219195850.png]]

![[Pasted image 20260219214325.png]]

![[Pasted image 20260219195859.png]]
For this I used $n_{\text{ samples }}=1000$, so that I could see what happened as the number of bins approached a significant portion of the number of samples

![[Pasted image 20260219215412.png]]

We can see the gaussian shape well for a medium number of bins, but loose coherence when we have too many bins and don't tell the story well with too few relative to the total number of data points. Because these are continuous distribution, we care about the ranges of values - so there is a notion of density. If we have too many bins, then data points can all fit neatly into their own category - so they don't stack neatly as they do when they are clumped. The PDF for each of these follow the shape of a pure continuous gussian, $\frac{1}{\sqrt[]{ 2\pi \sigma^{2} }}e^{\frac{-x}{2\pi\sigma^{2}}}$ (yes that was memorized) - but these are really discrete points that were sampled and stored in a bit representation. Counterintuitively, with more bins we see many more values with nothing but ALSO many values with abnormally high peaks  - i.e. we don't see any bins above 0.5 for the first two, but we see a few for the third. 



## 3 Discrete-valued scalar data 20 pts


![[Pasted image 20260219195918.png]]
I'm using a dataset on covid cases globally. The random variable is the percentage of population sick (i.e. pick a random country). There are many countries that fit into different bins for percentage of population sick.


![[Pasted image 20260219195925.png]]
![[Pasted image 20260222095235.png]]

The pmf seems far easier, because we can just make bins. Going from pmf to cdf is just a cumulative sum, so one line. Going backwards would be a pairwise difference, but getting all the data in a range feels more convoluted. It would just be bigger and bigger bins, so not that bad actually, just a little bit weirder.

![[Pasted image 20260219195932.png]]
![[Pasted image 20260222095911.png]]
![[Pasted image 20260219195938.png]]
Most countries had very small percentages of people who were sick - 60 percent of the population had under 20 percent sickness. There are some where basically everyone got sick, but i think that depends on population size - if its a tiny country (or had horrible regulation) the number is high.

![[Pasted image 20260219195944.png]]
I think that good events for this dataset are the chance that you had less than x% sick, which is just the CDF, or 0 % sick which is just the pmf at zero.

There is a 48% chance of getting under 11% of the population sick. There is a 23% chance of having negligibly few cases.

A better even for this question: What is the probability of falling between 0.2 and 0.4 % of the population? That seems really bad for the country.

There is a 19% chance of falling between 20 and 40 percent population infection.

## 4

![[Pasted image 20260219195954.png]]


![[Pasted image 20260219200000.png]]
It is easy to compute either, I copied my manual PMF code and modified it to be a manual CDF for fun. The other cdf function i had done was just a cumsum of pdf. 
![[Pasted image 20260222102845.png|300]]
![[Pasted image 20260222102852.png|300]]

![[Pasted image 20260222110644.png|300]]

![[Pasted image 20260219200006.png]]
Most of the audio has low power, so the cdf goes up really fast if we are looking at that. If we look at values, we see almost no extreme -1 or +1, and a lot centered close to zero. 
This also looks like there are more quiet moments in the recording, which would have near zero amplitude - normally this wouldn't have such a strong peak around zero(even though oscillations have to cross zero, it has values equally across the sine wave)


![[Pasted image 20260219200014.png]]


An event could be that the signal power is within the 1/2 power width. Because the signal is normalized from 0 to 1, (and getting power is squared), this is data above ~0.70.

![[Pasted image 20260222111839.png|300]]


0.73 % chance of getting a power >= $\sqrt[]{ 2 }$. This is funky data, but that looks real.