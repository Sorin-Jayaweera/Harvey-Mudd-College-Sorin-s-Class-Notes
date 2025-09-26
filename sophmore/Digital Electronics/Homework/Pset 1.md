![[Pasted image 20250121194701.png]]
$$
\begin{align}
\begin{bmatrix}
Power  & Value \\
0 & 1 \\
1 & 2 \\
2 & 4  \\
3 & 8 \\
4 & 16 \\
5 & 32 \\
6 & 64 \\
7 & 128 \\
8 & 256 \\
9 & 512 \\
10 & 1024 \\
11 & 2048 \\
12 & 4096 \\
13 & 8192 \\
14 & 16384 \\
15 & 32768 \\
16 & 65536
\end{bmatrix}
\end{align}
$$
![[Pasted image 20250121194957.png]]
10 A
11 B
12 C
13 D
14 E
15 F
1) 
1101
01111101000
$428_{10}$ = 110101100
$$
\begin{align}
65261_{10}=1111111011101101_{2}
\end{align}
$$

2) 
$2^{3}+1=9$
$2^2++2^5+2^6$ = 100
$6*64+5*8+4=428$
$$
\begin{align}
11*16^3+14*16^{2}+14*16+15=48879_{10} \\
= 1011111011101111
\end{align}
$$
3) 
	1) 9
	2) 64
	3) 1 A C
	4) 11
	5) C8
	6) 3E8

* I realized just after finishing this that I could have done it much simpler by breaking base 16 into 4 digits in base two, and base 8 into 3 digits. That is silly, but oh well. 

![[Pasted image 20250121203425.png]]

$69_{10}$) sign-magnitude = 01000101

two's compliment format = 01000101

$-2_{10}$) sign-magnitude = 10000010
two's compliment format = 11111110

$-37_{10}$) sign-magnitude = 10100101  
two's compliment format = 1011011
 

![[Pasted image 20250121203440.png]]
$100100_{2}$ is -28
$011111$ is 31

![[Pasted image 20250121203508.png]]
-4
31

![[Pasted image 20250121203459.png]]
Binary:
unsigned)
	 Positive: 11111111   = 255
	 Most Negative: 00000000 = 0
2's compliment)
	Positive: 011111111 = 127
	Most Negative: 10000000 = -128
Sign Magnitude)
	Positive: 011111111 = 127
	 Most Negative: 11111111 = -127


![[Pasted image 20250121210746.png]]
 $$
\begin{align}A \\

  & 1010  &  10\\
+ & 0111  & + 7 \\
 =  & 10001 & = 17
\end{align}
$$

$$
\begin{align}
B \\
 & 00101111 = 32+8+4+2+1 & =47 \\
 & 101111  & = 47
\end{align}
$$

![[Pasted image 20250121210754.png]]
$$
\begin{align}
A \\
 1010& &  -6 \\
 0111&  & + 7 \\
 =0001&  & =1
\end{align}
$$

![[Pasted image 20250121222217.png]]
$$
\begin{align}
y=(\tilde{a}+\tilde{b}+\tilde{c})
\end{align}
$$
$$
\begin{align}
nand \, \, \, g_{1}(y_{1},a,b,c)
\end{align}
$$
![[Pasted image 20250123224653.png]]
3) Impact on Society Research and write a paragraph about how digital systems have transformed another discipline of engineering within your lifetime. Provide quantitative data about at least one specific impact, such as cost, reliability, etc. Cite your sources.

One of the most notable applications of digital systems is in remote patient health monitoring. These devices range from using smartphones for digital/long distance doctor visits to having active health monitering devices - watches tracking heart rate, water content, easy to use home kids for blood pressure, etc. Wearable devices for health modeling are "an emerging research domain that offers an integrated approach for continuous monitoring and profiling of diseases and health conditions at multiple spatial resolutions." (https://ojphi.jmir.org/2024/1/e60261). Beyond aiding the treatment of currently known symptom-disease relatoins, they are also aiding in research - "potential of [sensors and their data] representative digital biomarkers for certain diseases and conditions is currently shaping an exciting discovery pipeline." (Bent B, Wang K, Grzesiak E, et al).

According to Folio3, a digital health provider, personal health monitoring advancements have decreased ER visits by up to 70 %, improves patient compliance by up to 42%, and saves an annual $6 billion in U.S. healthcare.

Within hospitals there are new tools that allow for precise surgery, automated patient care, etc. Digital systems have and continue to revolutionize the modern health care industry.






5) AI Question (Optional) This question must be solved by AI. You may start by photographing or pasting in the prompt below. Report what the AI produces, whether you believe it is accurate or a hallucination, and whether the solution is similar, better, or worse than what you would have done yourself in a reasonable amount of time. If you are unsatisfied with the initial answer, explain how you modified the prompt and whether you obtained better results. a) Convert the following numbers to base 10: 11001002 , BEEF16 . b) What is the most positive unsigned 8-bit number? c) What is the most positive 2’s complement 8-bit number? d) Sketch a CMOS transistor-level diagram for a 4-input NOR gate. (When I asked this in August 2024, the first answer ChatGPT gave me was incorrect, and when I reminded it of the function of a NOR gate, it revised the answer to be correct.)

Response: 1. **1100100₂ (Binary to Decimal)**: To convert binary to decimal, we multiply each bit by the corresponding power of 2, starting from the right-most bit (the least significant bit):
    
    11001002=1×26+1×25+0×24+0×23+1×22+0×21+0×201100100_2 = 1 \times 2^6 + 1 \times 2^5 + 0 \times 2^4 + 0 \times 2^3 + 1 \times 2^2 + 0 \times 2^1 + 0 \times 2^011001002​=1×26+1×25+0×24+0×23+1×22+0×21+0×20
    
    This gives:
    
    =1×64+1×32+0×16+0×8+1×4+0×2+0×1= 1 \times 64 + 1 \times 32 + 0 \times 16 + 0 \times 8 + 1 \times 4 + 0 \times 2 + 0 \times 1=1×64+1×32+0×16+0×8+1×4+0×2+0×1
    
    =64+32+4=100= 64 + 32 + 4 = 100=64+32+4=100
    
    So, **1100100₂ = 100₁₀**.
    
2. **BEEF₁₆ (Hexadecimal to Decimal)**: Hexadecimal is a base-16 system, so we multiply each digit by the corresponding power of 16.
    
    BEEF16=B×163+E×162+E×161+F×160BEEF_{16} = B \times 16^3 + E \times 16^2 + E \times 16^1 + F \times 16^0BEEF16​=B×163+E×162+E×161+F×160
    
    Here:
    
    - B=11B = 11B=11 (in decimal)
    - E=14E = 14E=14 (in decimal)
    - F=15F = 15F=15 (in decimal)
    
    Now, we calculate:
    
    =11×163+14×162+14×161+15×160= 11 \times 16^3 + 14 \times 16^2 + 14 \times 16^1 + 15 \times 16^0=11×163+14×162+14×161+15×160
    
    =11×4096+14×256+14×16+15×1= 11 \times 4096 + 14 \times 256 + 14 \times 16 + 15 \times 1=11×4096+14×256+14×16+15×1
    
    =45056+3584+224+15=48979= 45056 + 3584 + 224 + 15 = 48979=45056+3584+224+15=48979
    
    So, **BEEF₁₆ = 48979₁₀**.
    

### b) What is the most positive unsigned 8-bit number?

An unsigned 8-bit number uses all 8 bits to represent a positive integer, so the largest number is when all bits are set to 1:

111111112=1×27+1×26+1×25+1×24+1×23+1×22+1×21+1×2011111111_2 = 1 \times 2^7 + 1 \times 2^6 + 1 \times 2^5 + 1 \times 2^4 + 1 \times 2^3 + 1 \times 2^2 + 1 \times 2^1 + 1 \times 2^0111111112​=1×27+1×26+1×25+1×24+1×23+1×22+1×21+1×20

This gives:

=128+64+32+16+8+4+2+1=255= 128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 = 255=128+64+32+16+8+4+2+1=255

So, the most positive unsigned 8-bit number is **255**.

### c) What is the most positive 2’s complement 8-bit number?

In 2’s complement, the most positive number is when the first (most significant) bit is 0, and all other bits are 1. This is equivalent to:

01111111201111111_2011111112​

Now, convert this to decimal:

011111112=1×26+1×25+1×24+1×23+1×22+1×21+1×2001111111_2 = 1 \times 2^6 + 1 \times 2^5 + 1 \times 2^4 + 1 \times 2^3 + 1 \times 2^2 + 1 \times 2^1 + 1 \times 2^0011111112​=1×26+1×25+1×24+1×23+1×22+1×21+1×20

This gives:

=64+32+16+8+4+2+1=127= 64 + 32 + 16 + 8 + 4 + 2 + 1 = 127=64+32+16+8+4+2+1=127

So, the most positive 2’s complement 8-bit number is **127**.

### d) Sketch a CMOS transistor-level diagram for a 4-input NOR gate:

To implement a 4-input NOR gate using CMOS technology, you will need 8 transistors (4 PMOS and 4 NMOS).

1. **PMOS Transistors**: The PMOS transistors are connected in parallel. Each PMOS transistor's source is connected to VDD (positive voltage), and the gates are connected to the inputs. The drains of the PMOS transistors are connected together and will go to the output.
    
2. **NMOS Transistors**: The NMOS transistors are connected in series. The source of each NMOS transistor is connected to ground (GND), and the gates are also connected to the inputs. The drains of the NMOS transistors are connected together and will go to the output.
    

The logic of the NOR gate is such that if all inputs are 0, the output is 1. If any input is 1, the output is 0. So, the PMOS transistors pull the output high when all inputs are low, while the NMOS transistors pull the output low when any input is high.

To summarize:

- 4 PMOS transistors are connected in parallel, with their sources connected to VDD.
- 4 NMOS transistors are connected in series, with their sources connected to GND.
- The output is taken from the drains of both the PMOS and NMOS transistors.

You can imagine a 4-input NOR gate as a combination of these two groups of transistors to form the logic, with PMOS transistors ensuring that the output is pulled high when the inputs are low, and NMOS transistors ensuring that the output is pulled low when any input is high.

Let me know if you'd like further explanation or a diagram!


Analysis of response: 
it got BEEF wrong, but did the 100 conversion correctly. The "most" positive and negative numbers in each form were also correct. The diagram for the NOR gate was also correct.


Answer: 
Time spent: 3 hours