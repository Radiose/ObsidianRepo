# Discrete

The probability [[Density function]] is obtained from a frequency histogram by normalising it. This is done via dividing the vertical axis via the total number of outcomes. 

![[Pasted image 20260503154800.png]]

The area under the curve, or the [[Definite integral]] of this would evaluate to 1.


![[Cumulative probability distribution function]]

![[Uniform density and distribution]]
### Combining frequency and distribution
Some more interesting densities and distributions are obtained by considering events with which combine several outcomes. 
Tossing two coins:
$(T+H)(T+H)$
$TT+TH+HT+HH$
Consider the events: No heads, One head. Two heads

These can be written as these [[subset]]s of the sample space 
$\{ TT \}, \{ TH,HT \},\{ HH \}$
These can be put into the [[Density function]]
![[Pasted image 20260503155834.png|404]]

We can get the [[Density function]] via dividing by the y value by the total amount of outcomes(4)
![[Pasted image 20260503160001.png|398]]

We can then get the [[Cumulative probability distribution function|distribution function]]
![[Pasted image 20260503160145.png|415]]


# Continuous 

A [[Random variable]] $X$ is continuous if there exists some [[function]] $f_{X}:\mathbb{R} \to \mathbb{R}_{+}$, called its probability [[Density function]], such that $\mathbb{P}(a \leq X \leq b)=\int_{a}^b f_{X}(x)dx$ for all $a \leq b$.

Note that $f_{X}(x)>0$ and $\int_{-\infty}^\infty f_{X}(x)dx=1$. There is no **probability mass function**. 
Additionally, note that to simply approximate, we use [[Numerical integration]] . This is because the majority of functions have no exact formula or antiderivative(at least those in machine learning). 


![[The normal distribution]]