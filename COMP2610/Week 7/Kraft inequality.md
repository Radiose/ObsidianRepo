# Motivation 
Suppose that you wanted to get [[prefix code]]s with fixed lengths.

![[Pasted image 20260922173957.png]]

this is the overall image of the lengths you can have in total (up to 4). 

# Definition 
For an [[prefix code]] $C$, its codeword lengths $\{ \ell_{1},\dots,\ell_{I} \}$ satisfy
$$\sum_{i_=1}^I 2^{-\ell_{i}}\leq {1}$$
Conversely, if the set $\{ \ell_{1},\dots,\ell_{I} \}$ satisfy the above inequality, then there must exist a [[prefix code]] $C$ with those codeword lengths. 

# Implications

![[Pasted image 20260922175009.png]]

Suppose you wanted to choose $0$ as a code. Then, you cannot choose anything to the right of it.  All the ones that start with $0$ cannot be used (in red, and also include the length 2 and 3).

The other implication is that if a given code has lengths that satisfy [[Kraft inequality]], then we can construct a code with the following:
Pick the first node at depth $\ell_{1}$, and using it as the first codeword, we remove all descendants of the node. 
Then repeat again and again. 