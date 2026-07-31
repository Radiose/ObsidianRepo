Any [[set]] S, along with two operations ${\oplus}$ and ${\otimes}$ and two members $0_{\oplus}$ and $1_{\otimes}$ of S, which satisfy the corresponding versions of [[algebraic and order axioms]] 1-9, is called a field. 

A field typically is described as a set $\mathbb{F}$ that contains two [[Binary operation]]s.
$+:\mathbb{F} \times \mathbb{F} \to \mathbb{F}$ and $\cdot\ \  \mathbb{F} \times \mathbb{F} \to \mathbb{F}$
 ![[algebraic and order axioms#Algebraic axioms]]
 The smallest possible field is $\mathbb{F}_{2}=\{ 0,1 \}$, where addition is defined as $1+1=0$

More generally, if $p$ is a prime number, then $\mathbb{F}_{p}=\{ 0,1,\dots,p-1 \}$ can be turned into some field.
Operations $a+b=a+b\ mod(p)$ and $a \times b=a\cdot b \ mod(p)$
Example $\mathbb{F}_{3}=\{ 0,1,2 \}$ $2+2=1$, $1+2=0$
Sometimes you can have non prime fields. $\mathbb{F}_{4}$ is possible if you add two extra elements that behave like third [[Roots of unity]], then we can assemble a field. 

## Formal polynomials 
If $\mathbb{F}$ is a field, then $\mathbb{F}[x]$, the set of formal polynomials, is not a field. 
Formal polynomials are expression of the form $a_{0}+a_{1}x+\dots+a_{n}x^n$.
$a(x)b(x):=\sum_{m=0} \sum_{i=0}^n a_{n}b_{n-i}x^n$. These are not fields, as multiplicative inverses cannot occur (negative exponents cannot exist).

# Theorem 1
If $\mathbb{F}$ is a field, $a \in \mathbb{F}$, then 
i) $0$ is unique 
ii) $1$ is unique
iii) $-a$ is unique for each $a\ s.t \ \  a+(-a)$ 
iv) $a^{-1}$ is the unique element such that $a^{-1}\times a=1$
v)$a \times 0=0$
vi)$-1 \times a=-a$