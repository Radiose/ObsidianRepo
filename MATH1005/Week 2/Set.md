Set
A set is a collection of elements. 
This cannot be understood as a definition, because we dont know what a collection or element is. It is an intuitive [[Statement]].

The notation $a \in S$ is read as 'a is an element of s'
$a \not \in s$ is 'a is not an element of s'

![[Axiom of extensionality]]

Methods for describing a set
There are many methods for describing a set 

Language:$\emptyset$ is the set with no elements 
$\mathbb{Z}_{\ge_{0}}$ is the set of non negative integers 
$\mathbb{N}$ is the set of positive integers. $0 \not \in \mathbb{N}$ and $0 \in \mathbb{Z}_{\ge_{0}}$
Let $\mathbb{Z}$ denote the set of integers
Let $\mathbb{Q}$ denote the set of rational numbers - ratio of integers - quotients 
$\mathbb{R}$ denotes the set of real numbers 

Sufficient detail is required for sets. You must specify until there is no room for error. 


Eg let p denote the set of al programs 
vs 
let p denote the set of programs written in the language c that accept no input from the user and will run to completion without a run time error in finite time - still need model of computer, and what is a program.

![[set roster notation]]


![[set builder notation]]

In mathematical context, there is usually a type of object you are thinking about. This object can be described as 


$s = \{ x\in \mathbb{Z} |x^2+2x-15=0\}$
S is equal to the set of all integers x for which $x^2+2x-15=0$ 

![[subset]]
![[Proper subset]]



Let a and b be sets. We say that A equals b , written A =B when $a \subset b$ and $b \subset a$
$A = B \iff(x \subset b\land b\subset a)$


any variable in [[set builder notation]] is local only. You cannot apply it to other sets. 


To prove that something is a proper subset of something else, prove that all elements of the subset are in the set, then prove that there exists at least one element of the set that is not in the subset. 



Making new sets from old sets 
the Union of a and b, denotes $a \cup b$ is the set 
$x \in U | (x \in A)\lor(x\in B)$

$a \cap b$ is denoted by $\{x \in U|(x \in a)\land (x \in b)\}$

$a /b =\{ x \in B|(x \in U)|(x \in B)\land(x \not\in B) \}$

The complement of a is all the elements of the universe that are not in a.
$x \in u | x \not\in a$, as is denoted $A^c$


the symmetric difference of A and B, denoted $A\triangle B$ is the set of all elements that are not in both A and B. its notation is $\{ x \in U | (x \in A)\oplus(x \in B) \}$
