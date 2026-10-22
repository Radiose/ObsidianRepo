---
aliases:
  - algebraically closed
---
A [[MATH1116/Linear algebra/Week 2/field|field]] is algebraically closed if 
$$\forall f(x)\in \mathbb{F}[x]\text{ with degree >=1},\ \exists \lambda \in \mathbb{F}:f(\lambda)=0$$
As an example, $\mathbb{R}$ is not algebraically closed, but $\mathbb{C}$ is. 
In fact any field that is not algebraically closed can be extended in a similar way to one that is. 

# Theorem 1
Over an [[algebraically closed field]], every [[linear operator]] on a finite dimensional vector space must have some [[eigenvalue]].

### Proof 
Suppose $V$ is a complex vector space with dimension $n>0$ and $T \in \mathcal{L}(V)$
Choose $\mathbf{v}\in V \setminus \{ \mathbf{0} \}$
Then, $\mathbf{v},T\mathbf{v},\dots,T^n \mathbf{v}$ is not linearly independent (dimension = $n$)
Thus, there exists $a_{i} \in \mathbb{C}$ such that $a_{0}\mathbf{v}+\dots+a_{n}T^n \mathbf{v}={0}$ with some nonzero $a_{i}$
Consider the polynomial $a_{1}z +\dots+a_{n}z^n$
Via the [[Fundamental theorem of algebra]], it must have some factorisation in the form $c(z-\lambda_{1})(x-\lambda_{2})\dots(z-\lambda_{n})$
Where $c \in \mathbb{C}\setminus \{ 0 \}$
Then, $0=a_{0}\mathbf{v}+\dots+a_{n}T^n\mathbf{v}=(a_{0}I+a_1T+\dots+a_{n}T^n)\mathbf{v}$
So $c(T-\lambda_{1}I)(T-\lambda_{1}I)\dots(T-\lambda_{m}{I})\mathbf{v}=0$
Thus, $T-\lambda_{j} I$ is not injective for at least some $\lambda_{i}$ thus it must have an eigenvalue. 
