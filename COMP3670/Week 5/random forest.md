Grow a large number of fully grown [[decision tree]]s, each on a bootstrap sample $\mathcal{D}$, and each restricted to consider **only a random subset of the variables at every split**. Classify by majority vote.

Our sources of randomness are are the bootstrap decorrelating the trees through data, and the random subset decorrelates them through the splits. Without the second device a single dominant variable would sit at the roots of nearly every tree, making them near copies of each other, which average doesnt do much with. 

The trees are **grown fully,** on purpose. They should have low bias, and the vote removes that variance. Collectively they do not overfit, so $\hat{h}$ is the majority opinion of many individually overfitted trees.

The price that is paid is that a forest is not interpretable.

# Example 
Going back to the [[decision tree#An example|this example]]. 

![[Pasted image 20260827144529.png]]




This is able to correctly classify the single point that the [[decision tree]] was not able to. 

What we can buy with a random forest is stability. Move one observation, the vote of hundreds of fully grown trees barely changes. Again, we pay for this variance reduction with interpretability. 

