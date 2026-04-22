---
{}
---
Basis of a column space

![[Column space]]
However, to make it become a basis, they must be [[linearly independent]]. Check the [[row echelon form]] to determine this. 

You must remember that the column space of the original vectors may not be the same as the column space of the [[row echelon form]]. If the first two columns in the REF have pivots in a set of 3, then take the first 2 columns of the original vectors, not the REF.

[[theorem]]
to find a basis of the column space of the [[Matrix]] A, one can take the following steps:
1 reduce A to a [[row echelon form]]
2 Identify the pivots inside of the REF, then pick the particular pivot columns in the original [[Matrix]] A.

**[[Row operations]] do not change [[linear relation]]s between the columns**. They change relations between the rows 

The dimension of the column space is equal to the number of pivots 
