Sorting algorithm
list of information and putting it an order according to some rule
let $N \in \mathbb{N}$ S be a set and $(x_{n})_{n\in \{ 1\dots N \}}$. 
This does not imply that all $x_{n}$s are different 

A **sorting algorithm** is a procedure for sorting a [[Sequence]] into increasing order according to some specified ordering rule.
Some examples of this is numerical, alphabetical etc. 
IE, it replaces $(x_{n})_{n \in \{1\dots N \}}$ with a  $(y_{n})_{n \in \{1\dots N \}}$
![[Index set]]

using [[Index permutation]]s allows 
- more precise algorithm specification
- items do not get moved, only their indices are affected
	- this is valuable when items are large or have variable storage length 
A reordering of a sequence x is a sequence y where $y_{n}=x_{\pi(n)}$ for some [[Index permutation]] $\pi$
$\pi = \begin{pmatrix}3,4,5,6 \\ 6,4,3,5\end{pmatrix}$ then if (a_n) = 7,9,11,13
	
then $(a_{\pi(n)})_{3\dots 6}=13,9,7,11$
- the indexes of the sequence $a_{n}$ have been rearranged

Least element algorithm 
This algorithm moves the element that is the smallest to the front - similar to ![[selection sort]] 

Trace it by:
Before table 
show smallest value and current comparison at every iteration 
show final table with swap 



merge sort 
Takes two sequences in S already ordered according to some rule
Combines them into a larger list


