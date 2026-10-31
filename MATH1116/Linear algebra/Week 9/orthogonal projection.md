# Definition 
Let $U \subset V$. The [[orthogonal vectors|orthogonal]] projection $P_{U}:V \to U$ is defined as follows:
Given $\mathbf{v}\in V$, we write it as $\mathbf{v}=\mathbf{u}+\mathbf{w}$ for $\mathbf{u}\in U$, $\mathbf{w}\in U^\perp$
Then, set $P_{U}(\mathbf{v})=\mathbf{u}$
We need to prove a lot of properties to do something with this.

# Theorem 
$(1):P_{U}$ is [[well defined expression|well defined]], and $P_{U} \in \mathcal{L}(V)$
$(2):P_{U}(\mathbf{u})=\mathbf{u}\quad \forall \mathbf{u}\in U$
$(3)$ : $P_{U}(\mathbf{w})=\mathbf{0}\quad \forall \mathbf{w}\in U^\perp$
$(4):Range(P_{U})=U$
$(5): \ker(P_{U})=U^\perp$ (the [[orthogonal complement]])
$(6):\mathbf{v}-P_{U}(\mathbf{v})\in U^\perp$
$(7):P_{U}^2=P_{U}$
$(8):\lVert P_{u}(\mathbf{v}) \rVert\leq \lVert \mathbf{v} \rVert$
$(9):\forall ONB \{ e_{1},\dots,e_{n} \}$ of $U$, $P_{U}(\mathbf{v})=\langle \mathbf{v},\mathbf{e}_{1} \rangle\mathbf{e}_{1}+\dots+\langle \mathbf{v},\mathbf{e}_{m} \rangle\mathbf{e}_{m}$

### Proof 
for fin dim case:
$(1):V= U \oplus U^\perp$, which implies well definiteness.
If $\mathbf{v}_{1}=\mathbf{u}_{1}+\mathbf{w}_{1}$ and $\mathbf{v}_{2}=\mathbf{u}_{2}+\mathbf{w}_{2}$, for $\mathbf{u}\in U,\mathbf{w}\in U^\perp$
Then $P_{U}(\mathbf{v}_{1}+\mathbf{v}_{2})=\mathbf{u}_{1}+\mathbf{u}_{2}=P_{U}(\mathbf{v}_{1})+P_{U}(\mathbf{v}_{2})$
Similarly, $\lambda \mathbf{v}_{1}=\lambda \mathbf{w}_{1}+\lambda \mathbf{u}_{1}$
$(2)$: $P_{U}(\mathbf{v})=\mathbf{v} \implies \mathbf{v}=\mathbf{u}+\mathbf{0}im$
$(3)$: Similar to $(2)$
$(4):$ follows from $(2)$
$(5):$ follows from $(3)$
