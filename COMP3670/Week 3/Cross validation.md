*This* is a method for [[model selection]] using varying splits of validation sets to rotate the role of data. 

![[Pasted image 20260820183222.png]]

We split it into $k$ equal folds, and average the $k$ scores $E_{cv}(\mathcal{M}_{i})=\frac{1}{k} \sum_{j=1}^k E_{val}^{(j)}(\mathcal{M}_{i})$, an estimate of $E_{out}$ for model $\mathcal{M}_{i}$.



In practice:
Every sample is used for training and for validation. Average out $k$ reduces the [[variance]] of the models, which makes comparisons more reliable. 
However, we need to note that these $k$ scores are not [[Independent event|independent]], so getting a [[Hoeffdings inequality]] score is more difficult.