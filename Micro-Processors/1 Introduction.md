
The inside of a pin in a microcontroller.
We have to use a buffer to convert from range of voltages to discrete values to read as 0 or 1 (static discipline). We also have a write path controlled by a switch to enable or disable. 
![[Pasted image 20250826142002.png|300]]

Sometimes pins use open-drain, which needs an external pullup or pulldown resistor.
![[Pasted image 20250826142320.png|300]]

There are two types of parasitic things that we mainly worry about. 
Parasitic Capacitance  and Parasitic current leakage. 



Hi all,

I made some speculations in class that I only just got to work through carefully.

We were saying that we would like to switch from coordinates $$
\vec{r}_1 (x_1, y_1, z_1) and \vec{r}_2
$$ to instead using

$$
\vec{r} \equiv \vec{r}_2 - \vec{r}_1
$$
$$
\vec{R} \equiv A\vec{r}_1 + B\vec{r}_2
$$
If you try to take the kinetic energy

T(\vec{r}_1, \vec{r}_2}) = 1/2 m_1 |\vec{\dot{r}}_1|^2 + 1/2 m_2 |\vec{\dot{r}}_2|^2

and then solve for what \vec{r}_1 and \vec{r}_2 should be in terms of \vec{r} and \vec{R} (and therefore their time derivatives) you can write an expression for

T (\vec{r}, \vec{R})

that will involve A and B, and in particular will have a dot product between \vec{\dot{r}} and \vec{\dot{R}}. We can simplify our E-L equations by CHOOSING A & B to make that dot product vanish, which turns out to correspond to A = Cm_1 and B = Cm_2 for some new shared constant C. If we additionally choose C = m_1 + m_2, you find that this makes the conserved quantity \vec{p}_R = (m_1 + m_2) \vec{\dot{R}}, which is the momentum of the center of mass, and the kinetic energy becomes very simple

T = 1/2 (m_1 + m_2) |\vec{\dot{R}}|^2 + 1/2 \mu |\vec{\dot{r}}|^2

where \mu is the reduced mass m_1*m_2 / ( m_1 + m_2)

It's worth trying to work through it to see how it happens and where the mysterious reduced mass comes from! In words, these choices are the coordinate transformation that separates the dynamics into a center-of-mass degree of freedom and a relative separation degree of freedom! We'll have more to say about that in a few lectures