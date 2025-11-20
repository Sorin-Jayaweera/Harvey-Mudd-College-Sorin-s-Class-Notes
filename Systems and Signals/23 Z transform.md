What the $\mathscr{L}\text{aplace }$ transform is for continuous time signals, the $\mathbb{Z}$ transform is for discrete time signals.  80% of the content is the same, but there are some key differences.


## 1) Definition
$$
\begin{align}
X(z) = \sum_{n=-\infty}^{\infty} x[n]z^{-n} \\
\end{align}
$$
Where does this idea come from?
$$
\begin{align}
z^{n}\to  h[n] \to  y[n]
\end{align}
$$
We have an eigenvalue property
$$
\begin{align}
y[n] = z^{n}*h[n] \\
= \sum_{k=-\infty}^{\infty} h[k]z^{n-k} \\
= z^{n} \underbrace{ \sum_{k=-\infty}^{\infty} h[k]z^{-k} }_{ H(z) }
\end{align}
$$
## 2) How to $\mathbb{Z}$ transform?

Plug in to the definition, or use another gosh dang look up table with rules breh
### Example: 
$$
\begin{align}
x[n]  & = a^{n}u[n] \\
z(z)  & = \sum_{n=-\infty}^{\infty} a^{n}u[n]z^{-n} \\
 & = \sum_{n=0}^{\infty} (a z^{-1})^{n} \\
 & = \frac{1}{1- az^{-1}} \text{ if } \left| az^{-1} \right| < 1 
\end{align}
$$
So 
$$
\begin{align}
a^{n}u[n] \stackrel{z}{\leftrightarrow  } \frac{1}{1- a z^{-1}}
\end{align}
$$

### Example:
Lets take a system with
$$
\begin{align}
x[n] = -a^{n}u[-n-1]
\end{align}
$$


$$
\begin{align}
X(z)  & = \sum_{n=-\infty}^{\infty} -a^{n}u[-n-1]z^{-n} \\
 & = - \sum_{n=-\infty}^{-1} a^{n}z^{-n},  & \text{ m=-n } \\
 & = -\sum_{m=1}^{\infty} a^{-m}z^{m} \\
 & = 1- \sum_{m=0}^{\infty} (a^{-1}z)^{m} \\
 & = 1- \frac{1}{1- a^{-1}z}  & \text{ if } \left| a^{-1}z \right| <1 \\
 & = \frac{1- a^{-1}z}{1-a^{-1}z} - \frac{1}{1-a^{-1}z} \\
 & = \frac{-a^{-1}z}{1-a^{-1}z} \\
 & = -\frac{1}{az^{-1}-1} \\
 & = \frac{1}{1-az^{-1}}
\end{align}
$$So we have
$$
\begin{align}
-a^{n}u[-n-1] \stackrel{z}{\leftrightarrow  }  \frac{1}{1-az^{-1}} &  &  \left| z \right| <a
\end{align}
$$
This has the same expression, but has a different region of convergence


### Example
Lets look at an impulse
$$
\begin{align}
x[n] = \delta[n] \\
X(z) = \sum_{n=-\infty}^{\infty} \delta[n]z^{-n}
\end{align}
$$
This has the sifting property, so we have $z^{0}=1$ 
$$
\begin{align}
\delta[n] \stackrel{z}{\leftrightarrow  } 1  &   & \text{ all z }
\end{align}
$$


### Example
$$
\begin{align}
x[n]  & = \cos(\omega_{0}n)u[n] \\
X(z)  & = \sum_{n=-\infty}^{\infty} \cos(\omega_{0}n)u[n]z^{-n} \\
 & = \sum_{n=0}^{\infty} \frac{1}{2}(e^{j\omega_{0}n}+ e^{-j\omega_{0}n}) z^{-n} \\
 & = \frac{1}{2} \sum_{n=0}^{\infty} (e^{j\omega_{0}}z^{-1})^{n} + \frac{1}{2} \sum_{n=0}^{\infty} (e^{-j\omega_{0}}z^{-1})^{n} \\
 & = \frac{1}{2} \frac{1}{1-e^{j\omega_{0}z^{-1}}} + \frac{1}{2} \frac{1}{1-e^{-j\omega_{0}}z^{-1}} & \text{ if } \left| z^{-1} \right| < 1 \\
 & = \frac{1}{2}  \frac{1- e^{-j\omega_{0}}z^{-1}+ 1-e^{j\omega_{0}}z^{-1}}{(1-e^{j\omega_{0}}z^{-1})(1-e^{-j\omega_{0}}z^{-1})} \\
 & = \frac{1}{2} \frac{2- z^{-1} \cdot_{2}\cos(\omega_{0})}{1- z^{-1}2\cos(\omega_{0})+z^{-2}}  \\
 & =\frac{1-\cos(\omega_{0})z^{-1}}{1-2\cos(\omega_{0})z^{-1}+z^{-2}}& \left| z \right| >1
\end{align}
$$

## Method 2: Table + Properties

Note that the region of convergence is *DIFFERENT* then before: If we have a zero at a pole, then we've increased the region of convergence. 


![[Pasted image 20251118104709.png]]
Table:
![[Pasted image 20251118104726.png]]

$$
\begin{align}
x[n] = \delta[n] + 3 \cdot 2^{n}u[n] - 2\cos(\omega_{0}n) u[n]
\end{align}
$$

Lets practice decomposing a signal with a table:
$$
\begin{align}
\delta[n]  & \leftrightarrow  1 &  \text{ all z } \\
2 \cdot 2^{n}u[n]  & \leftrightarrow  3 \cdot \frac{1}{1-2z^{-1}} & \left| z \right| > 2 \\
-2 \cdot \cos(\omega_{0}n)u[n]  & \leftrightarrow   -2 \frac{1-\cos(\omega_{0}z^{-1})}{1-2\cos(\omega_{0})z^{-1}+z^{-2}} & \left| z \right| >1
\end{align}
$$
So we get
$$
\begin{align}
X(z) = 1+ \frac{3}{1-2z^{-1}} - 2 \frac{1-\cos(\omega_{0})z^{-1}}{1-2\cos(\omega_{0})z^{-1}+ z^{-2}}
\end{align}
$$
This has the ROC $\left| z \right| > 2$ because all terms must converge.


Continue with lecture [[24 Z transform cont.]]
