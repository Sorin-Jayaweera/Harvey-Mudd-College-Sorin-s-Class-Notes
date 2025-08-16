
$$
\begin{align}
M_{0}\left( \frac{ 1+\frac{x^{2}}{2} }{x+\frac{x^{3}}{6}}-\frac{1}{x} \right)  \\
= M_{0} \frac{\left( x+\frac{x^{3}}{2} - x+\frac{x^{3}}{6} \right)}{x^{2}+\frac{x^{4}}{6}} \\
= M_{0} \frac{6\left( \frac{x^{3}}{3} \right)}{6x^{2}+x^{4}} \\
= M_{0} \frac{2 x^{3} }{6x^{2}+x^{4}} \\
= M_{0} \left( \frac{2x}{6+x^{2}} \right)
\end{align}
$$



A complex number $z$ may be expressed either in Cartesian form as $z = x + i y$ or in polar form as $z = r e^{i\phi} = r(\cos\phi + i \sin\phi)$. For example, $i = e^{i \pi/2}$, $1-i = \sqrt{2} \, e^{-i\pi/4}$ 


(b) Deduce trigonometric identities for $\sin(3\theta)$ and $\cos(3\theta)$ in terms of $\sin\theta$ and $\cos\theta$ using $(e^{i\theta})^3$.

$$
\begin{align} 
 & \text{ let } 3\theta = \phi \\
 & r(\cos \phi+i\sin \phi)=r e^{i\phi}  \\
 & = re^{3i\theta}=re^{(i\theta )^{3}}  \\
 & = r(\cos\theta+i\sin\theta)^{3}\\
 & \text{ thus } \\
 & r(\cos(3\theta)+i\sin(3\theta))=r(\cos(\theta)+i\sin(\theta))^{3}
\end{align}
$$
This implies that
$$
\begin{align}
\cos 3\theta = (\cos\theta+i\sin\theta)^{3}-i\sin(3\theta) \\
\sin 3\theta = (\cos\theta+i\sin\theta)^{3}-\cos(3\theta) \\
\end{align}
$$

  

(c) Evaluate (i) $\sqrt{1+i}$, (ii) $\ln(1+i)$, (iii) $\tan(1+i)$.

$$
\begin{align}
 & i) \sqrt{ 1+i }  =\sqrt{ e^{i\pi/4} } 
   & = e^{i\pi/8} \\
 & ii) \ln(1+i)= \ln\left( e^{\frac{i\pi}{4}} \right) & =\frac{i\pi}{4} \\
 & iii) \tan(1+i)= \tan(e^{i\pi/4}) \\
 &  =\tan\left( \cos \frac{\pi}{4}+i\sin\left( \frac{\pi}{4} \right) \right) \\
 & =\tan \left( \frac{\sqrt{ 2 }}{2}+i\sqrt{ \frac{2}{2} } \right)  \\
 &  & =\tan\left( \frac{\sqrt{ 2 }}{2} (1+i) \right)
\end{align}
$$

$$
\begin{align}
 & i) \sqrt{ 1+i }  =\sqrt{ e^{i\pi/4} } 
   & = e^{i\pi/8} \\
 & ii) \ln(1+i)= \ln\left( e^{\frac{i\pi}{4}} \right) & =\frac{i\pi}{4} \\
 & iii) \tan(1+i)= \tan(e^{i\pi/4}) \\ \\
 & =\frac{\sin(e^{i\pi/4})}{\cos(e^{i\pi/4})} \\
 & = \frac{\frac{e^{i\theta}-e^{-i\theta}}{2}}{\frac{e^{i\theta}+e^{-i\theta}}{2}} \\
 & = \frac{e^{ie^{i\pi/4}}-e^{ie^{i\pi/4}} }{e^{ie^{i\pi/4}}+e^{ie^{i\pi/4}} } \\

\end{align}
$$

Problem 4 — orthonormal basis
Find the coefficients
$$
 a_0, b_0, b_1, c_0, c_1, c_2
$$
 such that

$\{ a_0, b_0 + b_1 t, c_0 + c_1 t + c_2 t^2 \}$

form orthonormal polynomials on $(0,1)$ using the inner product

$$ \langle f,g\rangle = \int_0^1 f(t) g(t)\,\mathrm{d}t $$

we can set $a_{0}=1$, $b_{0}=0,b_{1}=1,c_{0}=0,c_{1}=0,c_{2}=1$. This makes an orthonormal polynomial on the inner product.

We can use gramn-schmidt to make the orthonormal basis.

Lets set the first basis vector to be $v_{1}=a_{0}=1$
Then, 
$$
\begin{align}
v_{2} & =t-\frac{\left<t,1 \right>}{1,1})(1) \\
 & =t- \frac{1}{2}
\end{align}
$$
We can now find $v_{3}$
$$
\begin{align}
v_{3} & =t^{2}-\frac{\left< t^{2},t-\frac{1}{2} \right>}{\left< t-\frac{1}{2},t-\frac{1}{2} \right> } \left(t-\frac{1}{2}\right)- \frac{\left< t^{2},1 \right> }{\left< 1,1 \right> }1 \\
 & =t^{2}-\frac{\int_{0}^{1} t^{3}-\frac{1}{2}t^{2}dt}{\int_{0}^{1} \left( t-\frac{1}{2} \right)^{2}dt}\left( t-\frac{1}{2} \right) - \frac{\int_{0}^{1} t^{2}dt}{1}1 \\
 & =t^{2}-\frac{\frac{1}{4}-\frac{1}{6}}{\frac{1}{24}}\left( t-\frac{1}{2} \right) - \frac{1}{3} \\
 & =t^{2}-2t-\frac{4}{3}
\end{align}
$$

This gives us three vectors to be an orthonormal basis:
$$
\begin{align}
v_{1} = 1 \\
v_{2} = t-\frac{1}{2} \\
v_{3} = t^{2}-2t-\frac{4}{3}
\end{align}
$$






Let $v1 = a0$.
Now, for the next vector we must subtract the parallel component.

$$
\begin{align}
v_{2}  & = b_{0}+b_{1}t - \frac{<b_{0}+b_{1}t,a_{0}>}{<a_{0},a_{0}>} \\
 & =b_{0}+b_{1}t - \frac{\int_{0}^{1} (b_{0}+b_{1}t)(a_{0})dt}{\int_{0}^{1}a_{0}^{2} dt}  \\
 & =b_{0}+b_{1}t - \frac{a_{0}b_{0}+\frac{a_{0}b_{1}}{2}}{a_{0}^{2}} \\
 & =b_{0}+b_{1}t-\frac{b_{0}}{a_{0}}+\frac{b_{1}}{2a_{0}} \\
 v_{2}& =b_{0}\left( 1-\frac{1}{a_{0}} \right)+b_{1}\left( t+\frac{1}{2a_{0}} \right)
\end{align}
$$

