Imagine a straight line where each point has different error bars. We want to fit a curve to the line, so we want to minimize the difference between the values and the line's values. However, we want to weight small error bar data points more. This is called the $\chi^{2}$.
$$
\begin{align}
\chi^{2}=\sum_{i=1}^{N}\left[ \frac{y_{i}-(mx+b)}{\delta y_{i}} \right]^{2}
\end{align}
$$
in a good fit, $\chi^{2}\approx n$
We can make this a bit better by doing $\frac{\chi^{2}}{N-\# \text{ parameters }}$. The more parameters, the easier to fit data. If we have 2 points and two parameters (mx +b), then we can always fit a curve. Same if we have 3 points and a $\mathscr{P}_{3}$ polynomial. This is called the "reduced" $\chi^{2}$.

With a good curve we want to minimize the residuals and show that there appears to be random scattering between the points. If there is a pattern in the residuals, we're fitting the wrong type of curve. A good fit will have a $\chi^{2}\approx {1}$. If the value is far larger $(x\gg 1)$, we might not have a linear fit, or the error bars might be far smaller than they should be. If $\chi^{2}\ll 1$, then maybe our error bars are way too big.



$$
\begin{align}  
\text{ Youngs Equation: } \\
L = x \sqrt{ \frac{d}{n \lambda}-1 } \\
d = n \lambda \sqrt{ 1+m^{2} }\\
\delta d = \left| \frac{ \partial d }{ \partial m }  \right|\delta m 
\end{align}
$$