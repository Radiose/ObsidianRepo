IEEE half precision floating point 
this is the shortest standard 

$(-1)^s \times m \times 2^n$
the sign bit is left most
mantissa is at least one and is less than 2. Only store the decimals that come after the binary point. (1.44) = (44). 
The exponent n is stored in the 5 digits in between bits (14 to 10).

For example

0 00001 0000101010

first digit 0 - sign is positive 
00001 therefore exponent is  1-15 = -14

m = 0000010101 

therefore using IEE 
1 * 1.00000101010 $\times 2^{-14}$.
simplifying: 
(1+ $\frac{1}{672}$)*$2^{-14}$ 



