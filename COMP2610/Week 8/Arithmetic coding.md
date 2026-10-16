# Motivation
[[Shannon-Fano-Elias coding|SFE coding]] is very useful, but problems start to arise when you want to code whole sequences of codewords, rather than just individual ones. Because the bound $\left\lceil  \log_{2} \frac{1}{p_{i}}  \right\rceil+1$ is for each INDIVIDUAL block, doing that N times quickly introduces alot of extra bits. 

## Overview 
We aim to encode a sequence of outcomes $x_{1},\dots,x_{n}$, via finding the symbol interval for $x_{1},\dots,x_{n}$We then want to output a binary string corresponding to the chosen interval. Our output will look like the first $\ell(x_{1},\dots,x_{n})$ bits of the midpoint of the interval.

Some properties we have with arithmetic coding are that we do not compute a symbol coding for $X$ and concat, or explicitely code for all length $N$ sequences at once. Additionally, we dont have to assume independence for all elements in the alphabet of the ensemble $X$.


# Computing the interval for sequences 
Say we want to encode $x_{1},x_{2}$
Ideally, we'd want to encode $p(\mathbf{x})$ for all possible $\mathbf{x}$ of length 2, and then find the interval for $p(x_{1}x_{2})$

The main idea is to write $p(x_{1}x_{2})=p(x_{1})p(x_{2}|x_{1})$ via the chain rule
Additionally, $p(\cdot|x_{1})$ is just another probability distribution, so we can compute intervals similar to [[Shannon-Fano-Elias coding|SFE coding]]. Therefore, **we can find an interval for** $p(x_{2}|x_{1})$ within the interval for $x_{1}$

### Example 
Suppose $\mathcal{A}=\{ a,b,c \}$, and $p(a)=0.25,\quad p(b)=0.5\quad p(c)=0.25$

Suppose the first symbol we want to code is $b$. 

First, we divide the overall interval $[0,1]$ into places for $a,b,c$
![[Pasted image 20261016185008.png|302]]


From here, we compute $p(a|b)$, $p(b|b)$, $p(c|b)$
We now slice up the interval for $b$ according to these. 
![[Pasted image 20261016185151.png|335]]

### Ending the stream 

We use the symbol $\square$ to symbolise the end of a message. 
We assign to it some probability that makes sense 
$p(\square)$ is the probability of seeing an empty string, $p(\square|a)$ is the probability of seeing just the string $a$

Implicitly we think of $ab$ as being $ab \square$

### Example including ending the stream 
Suppose $\mathcal{A}=\{ a,b,c ,\square\}$, and $p(a)=0.25,\quad p(b)=0.5\quad p(c)=0.15\quad p(\square)=0.1$
Like with SFE coding, we slice $[0,1)$ into three subintervals 

![[Pasted image 20261016194626.png|325]]

Supposing $p(\cdot|b)=p(\cdot)$
![[Pasted image 20261016194837.png]]




# Generating codewords 
We end up with the final interval $[u,v)$, and as per [[Shannon-Fano-Elias coding|SFE coding]], we use the first $\ell(x_{1},\dots,x_{n})$ bits of $\frac{u+v}{2}$. Remember that $\ell(x_{1},\dots,x_{n})$ is given by $\lceil \log_{2} \frac{1}{p(x_{1}x_{2}\dots x_{n}) }\rceil+1$
This guarantees that all strings starting with the codeword are within the interval, similarly to SFE. 
Formally:

$$\begin{aligned}
&u \leftarrow 0.0,\quad v \leftarrow 1.0,\quad p \leftarrow v - u \\
&\textbf{for } n = 1, 2, \ldots \\
&\qquad L_n(a_i \mid x_{<n}) = \sum_{i'=1}^{i-1} p(x_n = a_{i'} \mid x_{<n}) \\
&\qquad U_n(a_i \mid x_{<n}) = \sum_{i'=1}^{i} p(x_n = a_{i'} \mid x_{<n}) \\
&\qquad v \leftarrow u + p \cdot U_n(x_n \mid x_{<n}) \\
&\qquad u \leftarrow u + p \cdot L_n(x_n \mid x_{<n}) \\
&\qquad p \leftarrow v - u \\
&\qquad \textbf{if } x_n = \square \text{, terminate} \\
&\text{Output first } \ell(x_1 \ldots x_N) = \lceil \log_2 1/p \rceil + 1 \text{ bits of } (u+v)/2
\end{aligned}$$
