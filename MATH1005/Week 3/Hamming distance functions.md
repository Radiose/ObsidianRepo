---
{}
---
Hamming distance [[function]]s 
Let B = {0,1} and $n \in \mathbb{N}$ 

we defined a set $B_{n} = {B \times B \dots B}$ n times
And a function $H_{n}: B_{n}\times B_{n} \to \mathbb{Z}_{\ge_{0}}$ by the rule 
$H_{n}(s,t)$ = the number of coordinate bit positions, where s and t differ. 

This function takes two bit strings of the same length. It tells the amount of coordinates that the bit strings differ 

An infinite number of strings, and an infinite number of functions H have both been defined. For each positive integer n, $B_{n}$ is the set of n-tuples of binary digits (bits). So, for example (0,1,1,0,0,1)$\in B_{6}$ 



Consider the [[relation]] $H_{3}\subset B_{3}\times B_{3}$. This relation will be present between bitstrings that differ in exactly one position. If you think about this geometrically, these organise into a cube in three dimensions, and from here, there will be relations between those that are separated by 1 x, y or z value. 



This is applicable to parallel computing. You solve things parallelly. The act of CPUs communicating to each other is a big challenge. A hypercube is not a bad model for this.