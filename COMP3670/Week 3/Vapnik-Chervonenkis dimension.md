---
aliases:
  - VC dimension
---
the VC dimension $d_{VC}(\mathcal{H})$ is the largest number of points that $\mathcal{H}$ can shatter. If $\mathcal{H}$ shatters sets of every size, then $d_{VC}(\mathcal{H})=\infty$.

This is some single integer summarising the complexity, or flexibility of some model ([[hypothesis set]]).

To show $d_{VC}\geq k$, exhibit one set of $k$ points labelled in all $2^k$ ways. 
to show $d_{VC}<k+1$, show that no set of $k+1$ points can be labelled in all ways. 

![[Pasted image 20260814085757.png]]

In general, complexity is related to the number of free parameters. This is not a theorem though, and there are counterexamples that exist. 


A model with infinite VC dimension is unfalsifiable. 
For every sample size, there are $n$ points that can be labelled by $\mathcal{H}$ in all $2^N$ possible ways. 
	OR: whatever the sample size, there is some data we may possibly observe such that whatever their labels, $\mathcal{H}$ contains a hypothesis that fits it perfectly. 
	
If the unknown distribution $P$ happens to concentrate all probability on this kind of unfalsifiable data, then the model is unfalsifiable. Since we do not know $P$, we cannot guarantee this is not the case, so we consider this model as unfalsifiable. 

Conversely, a VC dimension of less than infinity($d_{VC}(\mathcal{H})=v<\infty$) means that there are some datasets with $v+1$ points that $\mathcal{H}$ cannot fit: IE, the model can be refuted by data.



Sauers lemma
If $d_{VC}(\mathcal{H})=v<\infty$, then for every $N >v,$
$S(\mathcal{H},N)\leq(N+1)^v$.

The right side is some polynomial of degree $v$ in $N$. So either $\mathcal{H}$ shatters sets of every size and $S(\mathcal{H},N)=2^N$ IE doubles ate very new point, or $d_{VC}(\mathcal{H})=v<\infty$, and grows only polynomially. 


# Revisiting the generalisation gap:
![[VC bound]]
![[The fundamental theorem of statistical learning theory(binary loss)]]