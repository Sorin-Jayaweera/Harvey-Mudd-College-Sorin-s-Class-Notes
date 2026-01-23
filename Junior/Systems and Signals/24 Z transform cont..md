
## Initial Questions:
### How are Poles in Butterworth filters spaced?
Butterworth filters have poles spaced evenly around a circle (of some radius). If the order is $n$,  the number of poles $2n$ - a second order Butterworth has $4$ poles.

In continuous time, we saw that the $\mathscr{L}$aplace transform was a general tool for the Fourier transform. Similarly, in discrete time, the $\mathbb{Z}$ transform is an extension of the Discrete Time Fourier Transform. 

The order of the filter is the order of the polynomial. For instance,
$$
\begin{align}
\frac{1}{s+1} & \text{ first order } \\
\frac{1}{s^{2}+2s+1 } & \text{ second order } \\
\end{align}
$$


### Question: How are filters used in the real world
We have examples of filtering pretty much everywhere. To listen to radio, you have to filter for a specific range of frequencies, and then shift them down to basically DC so that we can listen to them. 

If you go to a concert room and find the impulse response, then you can model how an orchestra would sound.  

Convolutional neural nets are just a bunch of filters with variable parameters. 

Car suspension systems have an input of the bumpiness of terrain. Depending on the speed that you're traveling, the suspension will behave differently - you want it to be a lowpass filter. If it amplified high frequencies, then you would be shot out of the car seat!

Sunglasses are lowpass filters to block UV. 

### Question:  Are filters put in real time or post?
Both! You often have to filter data in real time to get rid of signals that will alias with your sampling frequency, because it is impossible to get rid of them post data collection. Once you get data, then there are a lot of things you can do to it with filters - as long as you've made sure the core data is high quality.

For post data collection, you can use information from the *future*, for instance: weener filter.


## Cont. from Z transform
See previous lecture [[23 Z transform]]

### Example: $x[n] = r^{n}\cos(\omega_{0}n)u[n]$

$$
\begin{align}
\tilde{x}[n]  = \cos(\omega_{0}n)u[n]  & \leftrightarrow  \frac{1-\cos(\omega_{0})z^{-1}}{1-2\cos(\omega_{0})z^{-1}+z^{-2}} & \left| z \right| > 1 \\
 z_{0}^{n}x[n]  & \leftrightarrow  X\left( \frac{z}{z_{0}} \right) & \left| z_{0} \right| \cdot R \\
r^{n}\cos(\omega_{0}n)u[n] & \leftrightarrow  \frac{1- r\cos(\omega_{0})z^{-1}}{1-2r\cos(\omega_{0})z^{-1}+r^{2}z^{-2}} & \left| z \right| > r
\end{align}
$$

Note, the region of convergence $\left| z_{0} \right|\cdot R$ is the magnitude of the $z$ times the region of convergence of the previous thing. Lets say in the complex plane, we have convergence when magnitude of number is greater than one. If we multiply it by $2^{n}$, we make it less stable. The region of convergence will decrease in coverage - so the region will be for things greater than magnitude $2$. 

We used the second property to write the third property - we multiplied by $\frac{1}{r^{-1}}\to r$.


### Example: $x[n] = nu[n]$
$$
\begin{align}
u[n] & \leftrightarrow   \frac{1}{1-z^{-1}},  & \left| z \right| <1 \\
nx[n] & \leftrightarrow   -z \frac{ d X(z)}{d z }  & , R \\
n u[n] & \leftrightarrow   -z \frac{ d }{d z } \left\{ \frac{1}{1-z^{-1}} \right\}  \\
 & =-z \frac{-1 (z^{-2})}{(1-z^{-1})^{2}} \\
 & = \frac{z^{-1}}{(1-z^{-1})^{2}}, & \left| z \right| <1
\end{align}
$$


## How to inverse $\mathbb{Z}$ transform?
There are *three* methods here! Woohoo z transform!

### Method 1: Contour integration
$$
\begin{align}
x[n] = \frac{1}{2\pi j} \oint X(z)z^{n-1}dz
\end{align}
$$
See notes in the folder: "Sophmore/computational physics" for how to do this.

### Method 2: table and properties
Far faster, and works with rational $z$ transforms.

Note for the following examples that
$$
\boxed{
\begin{align}
a^{n}u[n]  & \leftrightarrow   \frac{1}{1-az^{-1}}  & \left| z \right| > \left| a \right|  \\
-a^{n}i[-n-1]  & \leftrightarrow   \frac{1}{1-a z^{-1}} & \left| z \right| < \left| a \right| 
\end{align}
}
$$


#### Example:
$$
\begin{align}
Z(z) = \frac{3- \frac{5}{6}z^{-1}}{\left( 1-\frac{1}{4}z^{-1} \right)\left( 1-\frac{1}{3}z^{-1} \right)} & \left| z \right| > \frac{1}{3}
\end{align}
$$
This expands into
$$
\begin{align}
X(z) = \frac{1}{1- \frac{1}{4}z^{-1}} + \frac{2}{1-\frac{1}{3}z^{-1}}
\end{align}
$$
The left term converges for $\left| z \right|> \frac{1}{4}$, and the right term for $\left| z \right| > \frac{1}{3}$.

From the table, we have the relevant entry
$$
\begin{align}
a^{n}u[n]\leftrightarrow  \frac{1}{1- az^{-1}}, & \left| z \right| > \left| a \right| 
\end{align}
$$
The region of convergence is $\left| z \right|> \frac{1}{3}$, which corresponds to this entry and not the $-a^{n}u[-n-1]$ entry. 
$$
\begin{align}
x[n] = \left( \frac{1}{4} \right)^{n}u[n]+ 2 \left( \frac{1}{3} \right)^{n} u[n]
\end{align}
$$
#### Example:
$$
\begin{align}
X(z)  & = \frac{36z^{2} - 10z}{12z^{2}-7+1},  & \frac{1}{4}<\left| z \right| \frac{<1}{3} \\
X(z)  & = \frac{3 - \frac{5}{6}z^{-1}}{1- \frac{7}{12}z^{-1}+ \frac{1}{12}z^{-2} } \\
 & = \frac{3- \frac{5}{6}z^{-1}}{\left( 1- \frac{1}{4}z^{-1} \right)\left( 1-\frac{1}{3}z^{-1} \right)} \\
 & = \frac{1}{1- \frac{1}{4}z^{-1}} + \frac{2}{1-\frac{1}{3}z^{-1}}
\end{align}
$$
Note here that we have $\left| z \right|> \frac{1}{4}$ and $\left| z \right|< \frac{1}{3}$.
Therefore, we get
$$
\begin{align}
x[n] = \left( \frac{1}{4} \right)^{n}u[n] - 2 \left( \frac{1}{3} \right)^{n}u[-n-1]
\end{align}
$$
#### Example: $X(z) = \frac{3-\frac{5}{6} z^{-1}}{\left( 1- \frac{1}{4}z^{-1} \right)\left( 1-\frac{1}{3}z^{-1} \right)}$ , $\left| z \right|< \frac{1}{4}$

$$
\begin{align}
x[n] = -\left( \frac{1}{4} \right)^{n}u[-n-1]- 2 \cdot \left( \frac{1}{3} \right)^{n} u[-n-1]
\end{align}
$$
### Method 3: Power Series expansion
This is time consuming but is really good for computing a few coefficients and can handle nonrational $\mathbb{Z}$ transforms.

#### Example: $4z^{2}+2+sz^{-1}$
$$
\begin{align}
X(z) = \sum_{n=-\infty}^{\infty} x[n]z^{-n}
\end{align}
$$
Lets think about expanding this into each of the terms
$$
\begin{align}
\dots+ x[-1]z^{1}+ x[0]z^{0} + x[1]z^{-1}
\end{align}
$$
The coefficient on the $z^{-n}$ term is $x[n]$. The number that multiplies each $z^{n}$ is telling you one point of the time domain signal. 
By inspection, $x[n]= [0\dots 0, 4,0,2,3,0\dots0]$

We are just reading the time values off of this power series.
$$
\boxed{
\begin{align}
x[n] = 4\delta[n+2]+ 2\delta[n] + 3\delta[n-1]
\end{align}
}
$$
This is an extremely simple case, lets look at one where there are an infinite number of nonzero samples.

#### Example: $X(z) = \frac{1}{1-az^{-1}}, \left| z \right|> \left| a \right|$
We can divide out to get
$$
\begin{align}
1 + az^{-1} + a^{2}z^{-2} + a^{3}z^{-3} \dots 
\end{align}
$$
Therefore, we have $x[n]=a^{n}u[n]$.

#### Example: $X(z) = \frac{1}{1-az^{-1}}, \left| z \right|<\left| a \right|$
This is the same term, but lets change the order when dividing:
$-az^{-1}+1$.

We get
$$
\begin{align}
-a^{-1}z-a^{-2}z^{2}-\dots
\end{align}
$$
Therefore, we have
$$
\begin{align}
x[n] = -a^{n}u[-n-1] 
\end{align}
$$
The only difference between these two is the order for which we divide. That's why swapping the order changes how 'sided' a signal is - one is marching forwards in time (more negative powers of z), and one marching backwards (more positive powers of z).

#### Example: $X(z)= \frac{3- \frac{5}{6}z^{-1}}{1 - \frac{7}{12}z^{-1}+ \frac{1}{12}z^{-2}}$
We can check this with long division for the power series expansion to get
$3+\frac{11}{12}z^{-1}+\dots$. We don't have to continue forever, but we can immediately see that
$x[0]=3$ and $x_{n+1}=\frac{11}{12}$. This is a good sanity check. 


### Summary:
To inverse $\mathbb{Z}$ transform, use partial fraction expansion, then use the table and properties. If you have 1 or 2 coefficients, you can use long division.  
Double check with power series expansion.

## Interpreting the Z transform

The region of convergence:

There are 4 types of region of convergence. 

* All: The entire $z$ plane, converging everywhere (except maybe $z=0,z=\infty$, either include or not)
	* Finite length signal, so zero off to $\pm\infty$, but has values
* Outside a circle: $\left| z \right|>r$ (could include or not include $z=\infty$)
	* right sided - zero until a time, and then always has a value
* Inside a circle: $\left| z \right|<r$ (could include or not include $z=0$)
	* Left sided - has a value until a time, and then always zero
* In one circle, outside another: $r_{0}<\left| z \right|<r_{1}$.
	* nonzero everywhere


Note: 
You need to check $z=0$ and $z=\infty$. 
The regions of convergence are circles, not strips (for Laplace it was strips).

