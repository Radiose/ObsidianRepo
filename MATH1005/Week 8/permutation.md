## permutation
This occurs when order matters in selection. IE, {1,2,3} is not the same as {2,1,3}
There are n! ways to arrange n distinct objects in a list
 
## r-permutations
There are 
$$P(n,r) = \frac{n!}{(n-r)!}$$
distinct ways to arrange r out of n objects. An example of this would be how many ways to get 3 people in a class of 10? $P(10, 3)$

### [[theorem]]
If A and B are [[set]]s with |A| = r and |B| = n, then the number of [[Injective Function|injective]] functions from $f:A \to B$ is P(n,r). This is because we are selecting r elements in the domain to map to n elements in the codomain, and for a function to be [[Injective Function|injective]], it must map one to one. 


![[Pasted image 20260429120349.png]]

Note that $n^r$ will denote the quantity of functions that exist from a [[set]] of size r to a set of size n.
