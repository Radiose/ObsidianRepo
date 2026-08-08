$U_{1},\dots,U_{m} \subset V$ and nonempty,
their sum is  $\{ \mathbf{u_{1}}+\dots+\mathbf{u}_{m}|\mathbf{u_{1}}\in U_{1},\dots, \mathbf{u}_{m}\in U_{m}\}$
In other words, the sum is the set of all possible elements of $U_{1},\dots,U_{m}$

# Theorem 1
if $U_{1},\dots,U_{m} \subset V$ are subspaces, then $U_{1}+\dots+U_{m}$ is a subspace. Additionally, it is the smallest [[vector subspace|subspace]] of $V$ containing $U_{1},\dots,U_{m}$. 


#### proof:

We verify that the sum $U_{1}+\dots+U_{m}$ is a subspace. 

Because $U_{1}\dots$ are all subspaces, $\mathbf{0}\in U_{1}+\dots+U_{m}$.

Also, each $\mathbf{u \in}U_{n}$ is closed under addition and scalar multiplication, thus [[vector subspace#Theorem|this theorem]] states that $U_{1}+\dots+U_{m}$ is a subspace of $V$.

Now we verify that $U_{1}+\dots+U_{m}$ contains $U_{1},\dots,U_{m}$. We can do this simply by creating some sum of $\mathbf{0}+\mathbf{0}+\dots+\mathbf{u}+\dots \mathbf{0}$ for any $\mathbf{u}$. 

Finally, we verify that any subspace of $V$ containing $U_{1},\dots,U_{m}$ must also contain $U_{1}+\dots+U_{m}$. 

We do this via induction, proving inductively that if $\mathbf{u,\mathbf{v}}\in V$, then $\mathbf{u+v}\in V$, then recursively add this new vector created from the sum to another until we have proven that $U_{1}+\dots+U_{m}$ must be in the vector subspace containing $U_{1},\dots U_{m,}$ (because any two vector can be added together via the theorem linked).

![[internal direct sum of subspaces]]
