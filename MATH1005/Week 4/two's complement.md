---
{}
---
two's complement 
We fix a number of bits, say *t* to use for each integer. A string of *t* bits $d_{1} d_{2}\dots d_{t}$ is interpreted as a number in one of two ways, depending on the value of $d_{1}$.
if $d_{1}$ = 0, then the bit string (1$d_{2}d_{3}\dots d_{t}$) represents $(d_{2}d_{3}\dots d_{t})_{2}-2^{t-1}$. This is equivilanet to negative \[$(e_{2}e_{3}\dots e_{t})+001_{2}$]
where 
e, if $d_{1}=0$, is one or if $d_{1}=1$, then its zero. 

so $0000$ is 0
$1000$ is -8, (0111) = 7 + 1 = 8 so -8
$1001$ is $110$ = 6 + 1 = 7 so -7
$1101$ = $010$  = 2 + 1 = 3 so -3

This can be done with all other lengths of bit strings following the same process

Using the twos complement approach with 8 bits, we can represent all integers in -128 ... 127.

The addition process for positive numbers in binary works no matter whether the numbers are positive or negative 

to accomplish x-y: find the representation of -y from [[two's complement]], then add x and -y

adding 1-bit numbers 
1 + 1 = 1 0
1 + 0 = 0 1
0 + 1 = 0 1
0 + 0 = 0 0

[[logical connective]] can produce this. If you want the carry bit, run it through the *and* gate. 
If you want the result, run it through the *xor* gate. 

Therefore, to add two one bit numbers, you can use a type of circuit called a half adder. 
![[Pasted image 20260316203120.png]]


Adding 3 one bit numbers 

The result of 3 bits can either be 0,1, 2 or 3. These can be represented with two bits still. 

A full adder is used for this. This circuit takes 3 bits in, output 2 out.


![[Pasted image 20260316203950.png]]

diagram of a cascade of full adders to do addition of 4 bit integers 


We can use the cascade of full adders to subtract 4 bit integers as well.

This is very neat, because we can throw away the carry bit in the most significant part of the addition. 
