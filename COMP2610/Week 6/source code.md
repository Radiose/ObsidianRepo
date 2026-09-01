# Motivation 
This is a process for assigning names to outcomes. The names are typically expressed by strings of binary symbols. 
We denote the set of all finite binary strings by $\{ 0,1 \}^+ :=\{ 0,1,00,01,10\dots \}$
# Definition 
Given an [[ensemble]] $X$, the function $c: \mathcal{A}_{X} \to \{ 0,1 \}^+$ is  a source code for $X$. 
The number of symbols in $c(x)$ is the length $l(x)$ of the codeword for $X$. The extension of $c$ is defined as $c(x_{1},\dots,x_{n}=c(x_{1})\dots c(x_{n})$

**Example**:

- The code $c$ names outcomes from $\mathcal{A}_X = \{\texttt{r}, \texttt{g}, \texttt{b}\}$ by $c(\texttt{r}) = 00$, $c(\texttt{g}) = 10$, $c(\texttt{b}) = 11$
- The length of the codeword for each outcome is 2.
- The extension of $c$ gives $c(\texttt{rgrb}) = 00100011$

# Types of codes 
let $X$ be an [[ensemble]], and $c: A_{X}\to \{ 0,1 \}^+$. 
We say $c$ is a
#### uniform code 
this is when $l(x)$ is the same for all $x \in A_{X}$

#### variable length code 
otherwise 

Another important criteria for codes is whether the original symbol $x$ can be unambiguously determined given $c(x)$. We say $c$ is a 

#### Lossless code 
if, for all $x_{1},x_{2}\in A_{X}$, we have $x_{1} \not=x_{2}$ implies $c(x_{1}) \not=c(x_{2})$
Note that this is just [[Injective Function|injectivity]]
#### Lossy code 
otherwise 


**Examples**: Let $\mathcal{A}_X = \{\texttt{a}, \texttt{b}, \texttt{c}, \texttt{d}\}$

1. $c(\texttt{a}) = 00$, $c(\texttt{b}) = 01$, $c(\texttt{c}) = 10$, $c(\texttt{d}) = 11$ is **uniform lossless**
2. $c(\texttt{a}) = 0$, $c(\texttt{b}) = 10$, $c(\texttt{c}) = 110$, $c(\texttt{d}) = 111$ is **variable-length lossless**
3. $c(\texttt{a}) = 0$, $c(\texttt{b}) = 0$, $c(\texttt{c}) = 110$, $c(\texttt{d}) = 111$ is **variable-length lossy**
4. $c(\texttt{a}) = 00$, $c(\texttt{b}) = 00$, $c(\texttt{c}) = 10$, $c(\texttt{d}) = 11$ is **uniform lossy**
5. $c(\texttt{a}) = -$, $c(\texttt{b}) = -$, $c(\texttt{c}) = 10$, $c(\texttt{d}) = 11$ is **uniform lossy**

