
Binary: 
0000
0001
0010
0011
...

Sign magnitude binary: most significant bit is the magnitude, 0 = + 1 = -.

Thus, 6 = 0110, -6 = 1110. 

However, addition doesn't work here, adding these two would get 10001 $\neq 17$. Instead, we have the 2's compliment, where the most significant bit is a negative number.

Then, -6 = $1010$ $-8+2=6$.
To take the two's compliment, flip all the bits and add one.
6 = $0110$, so -6 = $1001+1=1010$. 
0110
1010
Extending a number if its unsigned would be
1111 (15) = 00001111.

But signed, 1111 (-1) = 11111111 (-1). 
To extend a signed number, look at the most significant bit. Put zeros in front, if its a 1 put ones in front. 