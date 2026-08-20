Lets go back to the example from lecture 1:
![[Pasted image 20260820171410.png|233]]
We have $2^8$ hypotheses. If we make $\mathcal{H}$ to include all functions $\mathcal{X}\to \{ 0,1 \}$, this gives us an unfalsifiable function. This is because this $\mathcal{H}$ shatters all 8 points.

Now suppose some domain expert tells us that whenever the first variable = 1, the outcome is always the same regardless of the other two. 

We now update our hypothesis set using our prior information. 
$\mathcal{H}'=\{ h:h(1,x_{2},x_{3})\text{is constant in }(x_{2},x_{3}) \}$. This is now falsifiable as well. We have bought low bias at low complexity using prior information. 

Most prior information is not as useful as it was in this previous example. What we have to do instead is to use prior information to build a collection of candidate models $\mathcal{M}_{1},\mathcal{M}_{2\dots}\mathcal{M}_{m}$ in $\mathcal{H}$ and then let data choose one. This is model selection. Note that model, and hypothesis set are the same thing.
