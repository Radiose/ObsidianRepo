---
aliases:
  - inclusion-exclusion principle
  - the sum rule
  - the product rule
---
set counting 
There are some rules for determining the [[cardinality]] of [[set]]s. 
## inclusion exclusion
$|A \cup B| = |A|+|B|-|A \cap B|$
## The sum rule
If A is a finite set partitioned into $\{ A_{1} ,A_{2}\dots A_{m}\}$
then $|A|=|A_{1}|+|A_{2}|\dots+|A_{m}|$

## The product rule 
if $A_{1},A_{2}\dots A_{m}$ are finite sets, then $|A_{1}\times A_{2} \times \dots \times A_{m}| = |A_{1}| \times |A_{2}|\dots \times |A_{m}|$
The [[Cartesian product]] of $A_{1}\dots A_{m}$ has a cardinality equivalent to the right hand side of the rule. 
### [[set counting|the product rule]] via a construction principle 
Suppose $S$ is a finite set, and we wish to determine its [[cardinality]]. We can do so, by specifying a multistage procedure for *constructing* an element of S, ensuring that the procedure has certain properties. 
The procedure must be as such:
At each stage we make a choice
If we make a difference choice at any stage, we will construct a different element of S. 
Every element of S can be constructed via the procedure. 

Suppose our process has $n$ stages. For each $i \in \{ 1,2,\dots ,n \}$, let $s_{i}$ denote the set of different choices we can make at stage $i$. Then, each element of $S_{1}\times S_{2}\dots \times S_{n}$ records the choices we made at one iteration of our procedure. 

The properties we require of our procedure then ensure that there is a [[Bijective|bijection]] between S and the [[Cartesian product]] $S_{1}\times S_{2}\times\dots \times S_{n}$. It follows from the product rule, that $|S| = |S_{1}|\times |S_{2}|\times\dots \times|S_{n}|$

#### scenario 
A hacker has learned the user ID of an important person. They want to brute force. The password will follow these rules:
12 characters long
must contain: 4 digits with repetition allowed 
two upper case characters with repetition allowed 
four lower case characters with repetition allowed 
two symbols chosen from the set $\{$ @,$,%,&,!,* $\}$ with repetition allowed. 
S denotes the set of all possible passwords. What is the [[cardinality]] of S?
