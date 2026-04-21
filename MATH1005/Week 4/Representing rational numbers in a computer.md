Representing rational numbers in a computer 
Recall that a rational number is defined as 
$Q = \mathbb{Z} \times(\mathbb{Z} \setminus \{ 0 \})$
The [[set]] Q may be partitioned so that any elements $(n_{1}d_{1})$ and $n_{2}d_{2}$ of Q are in the same [[partition]] [[set]] iff $n_{1}d_{2}=n_{2}d_{1}$


$q = (-1)^s \times m \times b^n$
where 
$q \in \mathbb{Q}, \ q \not=0$
$b \in \mathbb{Z},\ b \ge 2$ -  the base 
s = 0 or 1, the sign bit 
$m \in \mathbb{Q}, \ 1 \le m \le b$ - the mantissa 
$n \in \mathbb{Z}$ - the exponent 

eg 23.5 = $(-1)^0 \times 2.35 \times 10^1$

The number of digits of m is called the precision.

![[IEEE half precision floating point]]