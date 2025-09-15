Quick homework explanation:

We have the magnetic strength equation $M=M_{0}\left( \frac{\cosh B}{\sinh B} - \frac{1}{B} \right)$.

We can expand $$
\begin{align}coshx = 
\frac{e^{x}+e^{-x}}{2} \\
\sinh=\frac{e^{x}-e^{-x}}{2} \\
\cosh \approx 1 +\frac{x^{2}}{2!}+\frac{x^{4}}{4!}\dots
\end{align}
$$

We can analyze how this works for large and small B. Large B, this goes to $\frac{\frac{e^{x}}{2}}{\frac{e^{x}}{2}}\to 1, \frac{1}{b}\to 0,$ so we get $M=M_{0}$.

For small B, we can cancel terms in the Taylor expansion and show that it will go to zero.


Moving on to the lecture:

What is a vector space? 
1. There is a function, **addition** of vectors (+), so that v1+v2 is another vector.
2. There is a function, **multiplication by scalars**, denoted by juxtaposition, so that αv is a vector.
3. Vector addition is **commutative**: v1+v2=v2+v1.
4. Vector addition is **associative**: (v1+v2)+v3=v1+(v2+v3).
5. There is a **zero vector**, 0, such that v+0=v for all v.
6. Each vector v has an **additive inverse** v′ so that v+v′=0.
7. **Scalar multiplication is distributive I.**: (α+β)v=αv+βv.
8. **Scalar multiplication is distributive II.**: α(v1+v2)=αv1+αv2.
9. **Scalar multiplication is associative**: (αβ)v=α(βv).
10. **Multiplication by 1 leaves a vector unchanged**: 1v=v.

- Axiom 1 means that the vector space is closed under addition.
- The scalars may be real or complex (or quaternions…).

We have examples of vector spaces:
- Cubic polynomials, i.e. $c_{0}+c_{1}x+c_{2}x^{2}+c_{3}x^{3}$
- Set of real valued functions on $\left[ a \leq x \leq b \right]$
$af(x)\neq f(ax)$
$(a+b)f(x)=af(x)+bf(x)$

We have a notion of distance between vectors given by the inner product, typically defined as:
$$
\begin{align}
\left< \vec{a},\vec{b} \right> = \sum_{i=1}^{n}a_{i}b_{i}  \\
= \left( a_{1},a_{2},\dots,a_{n} \right) \begin{pmatrix}
b_{1}\\ b_{2} \\ \vdots \\ b_{n}
\end{pmatrix}
\end{align}
$$
$\left| \left| A \right| \right|=\sqrt{ \left< \vec{a},\vec{a} \right> }$

However, if the vector space is over the field of complex numbers,
$\left< \vec{a},\vec{b} \right> = \sum_{i=1}^{n}a_{i}^{*}b_{i}$
$$
\begin{align}let \\
a=\begin{pmatrix}
1 & i & -1 & -i
\end{pmatrix},   \\
b = \begin{pmatrix}
1 & e^{i\phi} & e^{2i\phi} & e^{3i\phi}
\end{pmatrix}\\
\left< a,a \right> = \sqrt{ (1,-i,-1,i) * \begin{pmatrix}
1 \\ i \\ -1 \\ -i
\end{pmatrix} \\ }
= 2 \\
\left< \vec{b},\vec{a} \right> = 1+ie^{-i\phi}-e^{-2i\phi}-ie^{-3i\phi} \\
= e^{-i\phi}\left( e^{i\phi}-e^{-i\phi} \right) +ie^{-i2\phi}(e^{i\phi}-e^{-i\phi}) \\
=e^{-i\phi}\cdot_{2}i\sin \phi+ie^{-2i\phi}(2i\sin \phi) \\
= 2\sin \phi(ie^{-2\phi}-e^{-2i\phi})
\end{align}
$$

Now, lets introduce some new notation: 
## Dirac Notation
We have a vector $\bra{\psi}$ and its complex conjugate $\ket{\psi}$.

