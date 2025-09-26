## Hardware Description Languages

Instead of having to write out the individual gates for a 64 bit adder, we can just use behavioral languages and let the computer translate it into gates. 

We can translate the structural Verilog
and a1(n1,a,b);
or o1(y,n1,c);

Into behavioral Verilog
assign y = a&b | c;

The fancier we get, it'll be harder to tell exactly what hardware were getting. The biggest danger with HDL is to think of it like a computer program though - everything ties down to hardware. Don't write code that'll give you really weird stuff. 

We think of the hardware that we want, and find the most appropriate way to build it, either structurally or behaviorally.

Lets imagine we want to build a 64 bit adder. We have inputs $a[0] b[0] \text{ to }a[63] b[63]$. In structural verilog, we would  build this out of full adders, and internally write out each of those gates.


### Rules of Behavioral Verilog

In behavioral, we have a set of logic equations
$$
\begin{align}
 & \text{ and }  & \& \\
 & \text{ or } & | \\
 & \text{ xor }  & ^{‸} \\
 & \text{ not } & ∼ \\
 & \text{ add } & +
\end{align}
$$
We could write, for example,
assign y=a&b&c | a& ~b & ~c | ~a&~b&c | ~a & b & ~c ;
We could easily write this out in a series of gates, or this is a 3 input xor gate. The beauty of logic synthesis is that you give it what you want, and it will make the cheapest/fastest (or whatever other metric) circuit possible. We usually tell the tool what it should do and the timing constraint, and it makes the cheapest way to satisfy those. 

Behavioral verilog is case sensitive ($A\neq a$).
You can use your own gates:

module and3(
	input logic a,b,c,
	output logic y);
	assign y = a&b&c
endmodule

This could be a transistor level, gates implementation, whatever. Doesn't matter.
If we want to use this, we would write
and3(a,b,c,y), since we have to keep the order of the inputs from the module definition.

We have bitwise and reduction methods.
You can take two inputs $[3:0] a,b;$
and do $\text{ assign } y_{1}=\text{ a \& b }$ (bitwise)
or $\text{ assign }y_{2}=\text{ \&a }$ which performs $\&$ on every bit of $a$.
We also have conditionals, i.e.
assign y = s ? d1:d2 would have y = d1 if s is true, or y = d2 if s is false.


![[Pasted image 20250211141050.png|700]]

We have more operators that follow an order of operations

~ Not
$*$,/,%
+,-
<<,>>   shift
<<< , >>> arithmetic shift
<,<=,>,>= comparison
\==, !=, equality comparison
&
^
|
?:

The important thing to note is that ~ comes before & which is before ^.
We have ways of dealing with numbers where you define the number of bits, the base, and the value:
![[Pasted image 20250211142617.png|300]]

We have bit swizzling, where you can set a value equal to a set of appended bits
assign y = {$a[2:1]$,{3{$b[0]$}}, $a[0]$, 6'b100_010}
This would make y
$$
\begin{align}
a[2],a[1],a[0],b[0],b[0],b[0],a[0],1,0,0,0,1,0
\end{align}
$$




