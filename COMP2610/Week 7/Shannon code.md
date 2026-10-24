Relating to [[compression]], if we pick lengths $\ell_{i}=\log_{2} \frac{1}{p_{i}}$, we get optimal code lengths. 
But, $\log_{2} \frac{1}{p_{i}}$ is not always in integer form. 

So, we define Shannon codes 
# Definition 
Given an [[ensemble]] $X$ with $\mathcal{P}_{X}=\{ p_{1},\dots,p_{I} \}$, define codelengths $$\ell_{i}= \lceil  \log_{2} \frac{1}{p_{i}} \rceil  $$ (the ceiling denoting the smallest integer not smaller than $x$, so $[2.1]=3$)
This allows us to prove something extremely significant, being the source coding theorem for symbol codes. 

