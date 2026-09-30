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
$=\det(E)^{-1}\det(zI - {A})\det(E)$ via the multiplicity of the determinant. 
$=\det(zI-A)$



![[Cayley Hamilton theorem]]

# Applications of characteristic polynomials 

We define the [[trace]] and [[The determinant|determinant]] as the sum and product respectively of the eigenvalues of a [[linear operator]] $T$. Each eigenvalue is repeated according to its multiplicity.

# Theorem  
Suppose $T \in \mathcal{L}(V)$, then let $n:=\dim(V)$. Then, $tr(T)$ equals the negative of the coefficient of $z^{n-1}$ of $T$.
### Proof 
Suppose $\lambda_{1},\dots,\lambda_{n}$ are each the [[eigenvalue]]s of $T$, with each [[eigenvalue]] repeated according to its multiplicity. Then by definition the [[characteristic polynomial]] of $T$ equals $(z-\lambda_{1})\dots(z-\lambda_{n})$
Then, we can expand it as $z^n-(\lambda_{1}+\dots+\lambda_{n})z^{n-1}+\dots+(-1)^n(\lambda_{1}\dots \lambda_{n})$


# Theorem 2 
[[The determinant]] $\det(T)$ equals $(-1)^n$ times the constant term of the characteristic polynomial of $T$.

### Proof 
see theorem above. 

# Corollary 
An operator $T \in \mathcal{L}(V)$ is invertible $\iff$ its determinant is non zero 
### Proof 
Suppose $T \in \mathcal{L}(V)$, the operator is invertible if and only if $0$ is not an [[eigenvalue]] of $T$, which if it was, would imply non injectivity thus non bijectivity. This only happens if and only if the product of eigenvalues is not $T$, so if $\det(T)\not=0$.

# Theorem 3 
[[The determinant]] and [[trace]] of any linear operator is equal to the determinant and trace of its [[matrix]] presentation. 

# Proof 
This can be simply shown by the [[Jordan normal form]] of a map having the same det and tr as the operator. 

# Theorem 4 
suppose $T \in \mathcal{L}(V)$, then the characteristic polynomial of $T$ equals $\det(zI-T)$
### Proof 
If $\lambda,z \in \mathbb{C}$, then it can be shown from the equality $$-(T-\lambda I)=(zI-T)-(z-\lambda)I$$
that $\lambda$ is an eigenvalue of $T$, if and only if $z-\lambda$ is an eigenvalue of $(zI-T)$ (read RHS as $T-\lambda I$).
The equation also implies that  $$\ker(T-\lambda I)^{\dim(V)}=\ker((zI-T)-(z-\lambda)I)^{\dim(V)},$$which shows the multiplicity of $\lambda$ as an [[eigenvalue]] of $T$ equals the multiplicity of $z-\lambda$ as an eigenvalues of $zI-T$.

Let $\lambda_{1},\dots,\lambda_{n}$ denote the eigenvalues of $T$, repeated according to multiplicity. Thus for $z \in \mathbb{C}$, the paragraph above shows that the eigenvalues of $zI-T$ are $z-\lambda_{1},\dots,z-\lambda_{m}$ similarly repeated due to multiplicity. 

$\det(zI-T)$ is by definition these values, so $\det(zI-T)=(z-\lambda_{1}),\dots,(z-\lambda_{m})$ which is the [[characteristic polynomial]].

