stars and bars 
This is the version of choose that you use when repetition is allowed. Choose will get you the amount of distinct [[subset]]s where each item can be picked at most once. Stars and bars will give you the amount of **[[multiset]]s** you can select. 

The method essentially asks, how many ways are there to $n$ indistinguishable items into $k$ indistinguishable bins.

The challenging bit here is understanding how it differs from the regular methods. 

$\frac{(r+n-1)!}{r! \times(n-1)!}$ is the formula where you are finding the amount of ways to combine $r$ stars into $n$ bins, or $n-1$ bars.

### Difficult problem:

If n is a positive integer, how many 5-tuples of integers from 1
through n can be formed in which the elements of the 5-tuple are
written in decreasing order?

First, we note that there is only one possible way that a multiset can be arranged to be decreasing. Secondly, we note that this question allows repetition, IE, that there can be multiple copies of an integer. 

Thus, we denote that there exists a [[Bijective|bijection]] between the amount of n tuples and the amount of [[multiset]]s present. Thus, the answer is n bins, and 5 stars. 




![[Pasted image 20260429120403.png]]
