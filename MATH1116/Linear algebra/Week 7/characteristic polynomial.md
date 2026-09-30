if $\lambda$ is an [[eigenvalue]] of $T$, then its geometric multiplicity, defined as $\dim(E(\lambda,T))$, with its algebraic multiplicity is defined as $\dim(G(\lambda,T))$.

The characteristic polynomial of $T$, which has eigenvalues $\lambda_{1},\dots,\lambda_{m}$ with algebraic multiplicities $d_{1},\dots,d_{m}$ is defined as 
$$\chi_{T}(z):=(z-\lambda_{1})^{d_{1}}\dots(z-\lambda_{m})^{d_{m}}$$
Note additionally that $deg(\chi_{T}(z))=\dim(V)$


# Theorem 
View $A \in Mat_{n \times n}$, so $A \in \mathcal{L}(\mathbb{F}^n)$, and additionally we require $\mathbb{F}$ to be [[algebraically closed field|algebraically closed]].
Then, $\chi_{A}(z)=\det(zI-A)$

### Proof 
via [[Jordan normal form#Theorem 2]], there must exist a Jordan basis for $A$, so call this basis $\alpha$ of $\mathbb{F}^n$.
$\det(A)=\det([A]_{\alpha})$. Call $J:= [A]_{\alpha}$ (its [[Jordan normal form]]).
The  diagonal entries of $J$ are the eigenvalues of A. The number of times they appear is  the algebraic multiplicity of each. 
If we write the coordinates of the vectors in the Jordan basis as columns to form a square matrix $E$ then via the [[change of base matrix]] formula, we get $J=E^{-1}AE$, with $J$ upper triangular. 

So:
$\chi_{A}(Z)=\det(zI-J)$ - because the determinant of an upper triangular matrix is the product of its diagonal entries which are $(z-\lambda I)$
$=\det(zI-E^{-1}AE)$ by the choice of $E$.
$=\det(E^{-1}(zI-A)E)$
$=\det(E)^{-1}\det(zI - {A})$ via the multiplicity of the determinant. 


![[Cayley Hamilton theorem]]