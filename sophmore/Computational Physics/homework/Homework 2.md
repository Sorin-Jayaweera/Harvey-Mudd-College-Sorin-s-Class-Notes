  

Use the Gram-Schmidt procedure to find an orthonormal set from $(1, -1, 1)$, $(-1, 0, 1)$, and $(2, -1, 2)$. You may do it by hand or with code.

We can normalize the first matrix
$$
\begin{align}
v_{1} & = \frac{\left( 1,-1,1 \right) }{\left< \left( 1,-1,1 \right),\left( 1,-1,1 \right) \right> }  \\
 & =\frac{1}{\sqrt{ 3 }}(1,-1,1) \\
v_{2} & = \frac{1}{\sqrt{ 2 }}(-1,0,1) \\
v_{3} & =(2,-1,2) - \frac{\left< (2,-1,2),(-1,0,1) \right>  }{\left< (-1,0,1),(-1,0,1) \right> }(-1,0,1) - \frac{\left< (2,-1,2),(1,-1,1) \right> }{\left< (1,-1,1),(1,-1,1) \right> }(1,-1,1)
\end{align}
$$
$$
\begin{align}
v_{3}  & = (2,-1,2) - \frac{5}{3}(1,-1,1) \\
 v_{3} & =\left\lvert    \left( \frac{1}{3},\frac{2}{3}, \frac{1}{3} \right) \right\rvert \\
 & =\frac{1}{\sqrt{ 6 }}\left( 1,2,1 \right) 
\end{align}
$$


<div style="background-color: #EFE; padding: 4px; font-size: 18px; font-weight: bold;">Problem 2 — Dirac delta functions</div>

(a) Show that

$$ \delta(f(x)) = \sum_{k=1}^m \frac{1}{|f'(x_k)|} \delta(x - x_k) $$

Where $x_k$ s are the $m$ roots of $f(x)$ ; that is, $f(x_k) = 0$ .


We know that $$
\begin{align}
\delta[k(x-x_{0})] = \frac{\delta(x-x_{0})}{\left| k \right| } \\ 
\text{ we can sum over each root if we have multpile}  \\
\text{ and rewrite using the equality }\\ \\
\sum_{k=1}^{m} \delta(f(x))
\text{ we can use the taylor sexpansion of f to simplify }  \\
f(x)=f(x_{k})+f'(x_{k})(x-x_{k}). \\
\text{ we know that } f(x_{k})=0,\text{ so this gets }\\
\sum_{k=1}^{n} \delta(f'(x)(x-x_{k}))   \\
\text{ we can now use the equality at the top }\\
= \sum_{k=1}^{m} \frac{\delta(x-x_{k})}{\lvert f'(x_{k}) \rvert }
\end{align}
$$
We can start by trying to simplify the side
$$
\begin{align}
\delta(f(x)) \\
\text{ we can rewrite f(x) as a taylor series } \\
 f(x)\sim f(x_{0})+f'(x_{0})(x-x_{0}) \\
\text{ which gives us } \\
\delta(f'(x_{0})(x-x_{0})) \\
\text{ we can use the property that } \\
\delta(k(x-x_{0}))=\frac{\delta(x-x_{0})}{\left| k \right| } \\
\text{ to write this as} \\
\frac{\delta(x-x_{0})}{\left| f'(x_{0}) \right| } \\
\text{ summing this for all zeros of f gives } \\
\delta(f(x))=\sum_{i=1}^{m} \frac{\delta(x-x_{k})}{\left| f'(x_{k}) \right| }
\end{align}
$$





$$
\begin{align}
\text{ we know that } \\
\int_{a}^{b} \delta(x^{2}-\pi^{2})\cos xdx \\
\text{ has the roots   }-\pi \text{ and }  \pi \\
\text{ we can use the previous result to rewrite as } \\
\frac{\cos(\pi)}{\left| 2\pi \right| }+\frac{\cos(-\pi)}{\left| (2\pi) \right| } \\
=-\frac{1}{\pi}
\end{align}
$$