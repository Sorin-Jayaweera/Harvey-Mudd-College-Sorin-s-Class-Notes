![[Pasted image 20250123133552.png]]
We can describe circuits in Verilog.

I.e. a not gate would be not g1(Y,a); The gate is a "not" titled g1 with output Y and input A. 

And would be and g2(y,a,b), and3 would be and g3(y,a,b,c).
This is what we call "structural Verilog". We could give equations describing this instead, with behavioral Verilog.


For logic gates, they have some cutoff for what is considered high and low, but they aren't ideal. 
![[Pasted image 20250123134806.png|300]]

If I tie two gates together, I want the output of one to be registered correctly by the input of another. They have some noise that is injected between. We typically define our logic level to cut off where the input uncertainty corresponds to a greater output uncertainty, so where the slope is -1 at the last point before the curve crosses the center. 
![[Pasted image 20250123135808.png|300]]

## Diodes and Making Logic Gates

Silicon as a tetrahedral lattice is an insulator. However, we can dope it with either Arsenic or Boron. Arsenic would have a hole where an electron is missing. 

An N type transistor allows current to flow through when current is applied. We have conductors on either side of an insulator - so this is a capacitor! Applying a voltage makes a charge on the other end, connecting the source and drain. 
![[Pasted image 20250123140923.png|300]]
Alternatively, we have pmos where applying a voltage turns off the switch. 

We can use this to make the first logic gate - Not.
![[Pasted image 20250123141224.png|300]]
Turning on A connects Y to Vdd and disconnects it from gnd. Turning it off disconnects Vdd and connects ground.

![[Pasted image 20250123141625.png|300]]
This is a nand gate.


Nmos is good at passing zeros, Pmost is good at passing ones. Mixing these makes fuzzy outputs.

To make an and gate, we connect a NAND gate and a NOT gate.

We always want to design the gate so that the nmos go from the output to ground and pmos go from power to output.
![[Pasted image 20250123142021.png|300]]
Even worse, gates work well when nmos are parallel and pmos in series or the other way around. 

Also note that a wire that isn't connected to Vdd or Gnd is floating, it can change etc - very bad.

## Power

There are two main sources of power consumption - static and dynamic. Dynamic comes from charging and discharging a capacitor. 
The power to charge and discharge a capacitor is $P=\frac{1}{2}cv^{2}$. If we are charging and discharging at frequency $f$, then we consume power $fp_{single}$. They aren't always turning on or off - a clock at every cycle would, but most don't. We add a term $\alpha \in [0,1]$, so $P_{dynamic}=\alpha fcV_{dd}^{2}$.

If ew have 
$$
\begin{align}
v_{dd}=0.8v, F=2Ghz, C = 5nf, \alpha=0.1, \text{ we get } \\
p = 0.64 W
\end{align}
$$
We also have a little bit of leakage. 
$$
\begin{align}
P_{static}=I_{leak}V_{dd}. \\
\text{ if } I_{leak}=100mA, P_{static} = 0.08w. \\
P_{tot} =P_{static}+P_{dynamic}=0.72w.
\end{align}
$$
Let's assume this is our cell phone with an $8W-hr$ battery. This could run for $\frac{8w-hr}{0.72w}=11 hrs$. If we aren't touching it, then the battery life would be $\frac{8W-hr}{0.08w}=100 hrs$.



