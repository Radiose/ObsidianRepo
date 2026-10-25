# Dirichlet distribution
![[Dirichlet distribution]]


# Generating code 
The process is almost identical to the one outlined in [[Arithmetic coding#Generating codewords]]
We outline how to create the intervals. 
We fix the probability for end of stream, say $p(\square)=0.15$

We then split up $p(a)=0.425,p(b)=0.425$ Our counts of each are $(1,1)$

when given the first element, say $b$, we get counts $(1,2)$, giving $p(a|b)=0.85 \times \frac{1}{1+2}=0.28$, and $p(b|b)=0.85 \times \frac{2}{3}=0.57$

From here, we split up the $b$ interval. 
$ba$ =$[0.425, 0.425 +0.425*0.28)$
$bb$ width = $[0.425, 0.425+0.425*0.57)$ 
