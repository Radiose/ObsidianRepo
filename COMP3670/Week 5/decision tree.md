Each leaf on the [[tree]] is a [[logical connective]] AND of the decisions on the path to it, and each class is the OR of the leaves. 

![[Pasted image 20260827094301.png]]

![[Pasted image 20260827094507.png]]
The above sentence is the classifier


The idea is that with each question, we narrow down the region of feature space we are in.

Leaves [[partition]] the feature space, they do not overlap and cover everything. This is similar to the [[Histogram classification]], but now we choose our partition using data.

Trees give us categorical features instead of numerical ones, and they are also interpretable. 

# The [[hypothesis set]]

The classification and regression tree algorithm (CART) is where every question has the form $x_{j}<\alpha$ for coordinate $j$ and threshold $\alpha$.

Every region is thus a rectangle with sides parallel to the axis and $\mathcal{H}=$ {classifiers constant on each cell of an axis aligned rectangular partition}

With trees of unlimited depth, $\mathcal{H}$ is enormous, so such a model is **unfalsififiable**
