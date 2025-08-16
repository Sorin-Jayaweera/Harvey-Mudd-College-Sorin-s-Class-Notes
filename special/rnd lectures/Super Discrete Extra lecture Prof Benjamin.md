
## Way to elegantly find the parity of ${N\choose{k}}$
Look at Pascals triangle. Initially the numbers look to be powers of two, and there is a geometrical pattern (Serpinski's triangle)

We are trying to count the number of odd numbers in the Nth row of the triangle. 
There are N choose k numbers in a row of pascals triangle

#### Claim: 
The number of odd numbers in row N of Pascal's triangle is $2^n$ where n is the binary expansion of the row

ie 83 = 64 + 16 + 2 + 1
the binary representation is 1010011, which has 4 1's in it. therefore, there are 2^4 = 16 odd numbers!
if $\gamma$ = a/b, a = br, 
lemma: r is $$
\frac{even}{odd} = even, \frac{odd}{odd} = odd
$$
#### strategy: 
determine the parity of N choose K, then count the Ks that make N choose k odd

Lemma 1: Even choose Odd = even.
First, observe that $$
\begin{bmatrix}
n \\
k
\end{bmatrix}
= n \times\begin{bmatrix}
n-1 \\
k-1
\end{bmatrix}
$$
I.e. 10 choose 3 is even.
How many binary strings of length 10 with three 1s?
There are no palindromes in the binary string as K is odd, so one side has odd number of 1s and the other has even.
Any string has a paired string, so the number of strings must be even. They always come in pairs! No algebra!


Lemma 2: Otherwise, if N is odd or K is even, N choose K has the same parity as $\frac{n}{2}\choose{\frac{k}{2}}$ 
We can use this fact to determine if it is even or odd by recursively checking lemma 1 or taking the next iteration of lemma 2 until a base case

Proof: 

$$
{n\choose{k}} = \frac{(N-1) \dots (N-L+1)}{1\times{3}\times\dots} \times {\frac{n}{2}\choose{\frac{k}{2}}}
$$
we can do a palindromic proof, any palindrome has a one in the center of the binary string
$$
{11\choose{5}} = {\frac{11-1}{2}\choose{\frac{5-1}{2}}}
$$
note that for a computer (base 2) to divide a number by two, it just has to shift bits to the right and trash the rightmost bit.
Therefore, we can easily compute:

ie ${99\choose{52}} =$ 
|1100011|  . a binary number is odd if it ends in a 1, otherwise even. Thus, delete everything until 
|0110100|  . there is even / even or even/odd (yields even) or number/zero (yields odd).

if at any point there is 0 choose 1 it is zero, but 1 choose 1, 1 choose 0, 0 choose 0 all yield 1. 
$$
\begin{matrix}
a & b & c \\
d  & e & f \\
g & h & i \\

\end{matrix}
$$ 
## Way to count the number of trees and word
the number of labeled trees and words of length (n-2) 
where a word has digits up to 10.

Prufer's Algorithm. 
remove the smallest leaf, and identify the node it is on. That is the first number, get rid of the leaf. Then the next smallest leaf, write what it is connected to, delete, etc.

Only this labeled tree can produce this sequence


## matrix tree theorem
given a labeled tree, how man spanning trees does it have?
*a spanning a tree is a connected undirected graph with no cycles*

write a matrix where its rows and columns where the first number is the degree of the node and then write the adjacent points. 
After writing the whole matrix, remove any two rows and take the determinant of the new matrix. The absolute value of that is the number of spanning trees.    

## determined ants
4 ants starting on one side of a graph and want to end at a destination.
Every and MUST go to a different morsel. 
How many ways can an ant get to the end destination? The path is described by a 4x4 matrix where the I,J entry is the number of paths an ant can take to get to entry J.  

## Fibonacci greatest common divisor
What is the greatest common divisor of 20 and 90? 10.
For Fib(20), Fib(90)? Fib(10).


