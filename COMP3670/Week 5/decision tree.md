---
aliases:
  - CART
---
Each leaf on the [[tree]] is a [[logical connective]] AND of the decisions on the path to it, and each class is the OR of the leaves. 

![[Pasted image 20260827094301.png]]

![[Pasted image 20260827094507.png]]
The above sentence is the classifier


The idea is that with each question, we narrow down the region of feature space we are in.

Leaves [[partition]] the feature space, they do not overlap and cover everything. This is similar to the [[Histogram classification]], but now we choose our partition using data.

Trees give us categorical features instead of numerical ones, and they are also interpretable. 

# The [[hypothesis set]]

The *classification and regression tree algorithm* (CART) is where every question has the form $x_{j}<\alpha$ for coordinate $j$ and threshold $\alpha$.

Every region is thus a rectangle with sides parallel to the axis and $\mathcal{H}=$ {classifiers constant on each cell of an axis aligned rectangular partition}

With trees of unlimited depth, $\mathcal{H}$ is enormous, so such a model is **unfalsifiable**. Thus, constraining the depth of a tree is a model, and [[model selection]] parameter is the degree of constraint. 


# Building the tree 
The goal with building a tree is to create splits that are able to make regions as pure as possible IE as close as possible to containing a single class.

 For a region $R$ containing $N_0(R)$ and $N_1(R)$ points of each class, let $p = N_1(R)/(N_1(R) + N_0(R))$ be the proportion of points in class one. The **impurity** of $R$ is $I(R) = \xi(p, 1-p)$, where $\xi$ must satisfy
	- $\xi(0,1) = \xi(1,0) = 0$: a region with one class only is **pure**
	- $\xi$ is largest at $p = \frac{1}{2}$: an evenly split region is **maximally impure**
	- $\xi$ increases on $[0, \frac{1}{2}]$ and decreases on $[\frac{1}{2}, 1]$
 Three standard choices:
	- **entropy**: $\xi(p, 1-p) = -p\log p - (1-p)\log(1-p)$ ( related to [[entropy (information theory)|entropy]])
	- **Gini**: $\xi(p, 1-p) = 2p(1-p)$
	- **misclassification**: $\xi(p, 1-p) = \min(p, 1-p)$


![[Pasted image 20260827102724.png]]

The three functions above only differ in how sharply they peak. 
Entropy and Gini functions are preferred in practice, as they are able to keep highly rewarding splits that misclassification does not. 

Splitting a region $R$ at coordinate $j$ and threshold $\alpha$ produces $R^j_{\alpha^+}$ and $R^j_{\alpha^-}$. The impurity drop is the impurity we had, minus the impurity we are left with. Mathematically,
$$
\Delta_R(j, \alpha) = I(R) - \dfrac{N(R_{\alpha,-}^j)}{N(R)} I(R_{\alpha,-}^j) - \dfrac{N(R_{\alpha,+}^j)}{N(R)} I(R_{\alpha,+}^j)
$$


Note that this is not the same as [[Empirical risk minimisation]]. We are assigning a score for a region, and our search is [[greedy algorithm|greedy]]. The tree returned is not the best in $\mathcal{H}$, but instead just the one that the procedure happens to build.


# An example 
Take the data collection below 
![[Pasted image 20260827104155.png]]

$N=12$ points, $d=2$ types.
We use the Gini impurity, $I(R)=2p(1-p)$, and stopping rule $s=2$, so no split may have fewer than $2$ points in a leaf.
Our candidate thresholds are the midpoints between consecutive observed values of a feature ($\{ 0,1,2,4,6 \}$), so here they would be $\{0.5, 1.5, 3, 5\}$.

We use CART 

### Step 1 
At the root, $N_{1}=5,N_{0}=7$ (the quantities of each type), so $p=\frac{5}{12}$ and $I$(root)=$2 \cdot \frac{5}{12} \cdot \frac{7}{12} = \frac{35}{72}$
Now try every candidate split and compute the impurity drop.

![[Pasted image 20260827104729.png]]

Above we can see the split with the best is the binary question $x_{1}\leq 1.5$
This gives us the following distribution 
![[Pasted image 20260827104943.png]]


we repeat this process a couple more times 
![[Pasted image 20260827105015.png]]


Finally, we are left with the three unclassified points. Because $s=2$, we cannot go any further, as we would have a single node by itself. Thus, we classify the region by the majority label. 
![[Pasted image 20260827105147.png]]



# Overfitting 
$S=1$ is the fully grown tree. Note that $E_{in}=0$. This leads to an overfitted model, which should not be used ever. 


# The tree hypothesis 

$\hat{h}$ is a [[partition]] of the feature space into axis aligned boxes, each labelled by the majority class of the training points inside it. The boxes are [[greedy algorithm|greedily]] chosen to separate the classes as fast as possible.

It is a histogram rule, whos grid was based on data rather than scaling. 

Strengths:
interpretability, categorical variables, no scaling of features needed, automatic disregard of irrelevant variables 

Weaknesses: boundaries are staircases, so diagonal boundary is explained badly
The tree is very unstable - change an observation and the split near the root may flip and change the entire tree below - this is a symptom of high [[variance]].



# Bagging 
Our rule with high variance and low bias is highly susceptible to the sample. A solution is to average many rules.

Our solution is to make $B$ new samples, via drawing $N$ observations from $\mathcal{D}$ with replacement. Each has the size of $\mathcal{D}$, but some observations appear twice, and other not at all.
Fit the rule on each bootstrap sample and let the $B$ classifiers vote. This is called bagging. 
Bias is unchanged, but variance is substantially reduced. 

![[Pasted image 20260827143023.png]]

With this, we can define a new term 

# Random forest 
random forest
Grow a large number of fully grown [[decision tree]]s, each on a bootstrap sample $\mathcal{D}$, and each restricted to consider **only a random subset of the variables at every split**. Classify by majority vote.

Our sources of randomness are are the bootstrap 