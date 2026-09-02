# Motivation
[[K-Means algorithm]] requires us to choose the number of clusters ($k$) beforehand, but in many algorithms, we want to inspect data first, without choosing the final number of groups.
Hierarchical clustering allows us to construct a multiscale family of [[clustering|cluster]]s in one analysis.

# Agglomerative hierarchical clustering 
General overview:
1: Start with a singleton cluster per observation 
2: find the two closest clusters
3: merge them 
4: repeat until only one cluster remains 
A linkage rule is used to define the distance between clusters

### Linkage rules 
for nonempty clusters $\mathcal{A},\mathcal{B}$, 
$d_{single}(\mathcal{A},\mathcal{B})=min_{x \in \mathcal{A},y\in \mathcal{B}}\ \ \ d(x,y)$, with $d(x,y)$ being the [[Euclidian norm]]
$d_{complete}(\mathcal{A},\mathcal{B})=max_{x \in \mathcal{A}, y \in \mathcal{B}}\ \ d(x,y)$

Single linkage aims to look at the nearest cross cluster pair, and complete linkage looks at the furthest cross cluster pair. 

Average linkage uses every cross cluster pair, defined as $d_{average}(\mathcal{A},\mathcal{B})=\frac{1}{|\mathcal{A}||\mathcal{B}|}\sum_{x \in A}\sum_{y \in \mathcal{B}}d(x,y)$
A dendrogram displays the merge sequence and merge heights 
Cutting the dendrogram at a chosen height will result in a clustering. 
