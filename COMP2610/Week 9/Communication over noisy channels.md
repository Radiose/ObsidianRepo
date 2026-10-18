
# Overall goal 
![[Pasted image 20261018154134.png]]
somewhat to recreate this. What we have been working on, with [[the source coding theorem]], entropy as a lower bound etc is compression. 

# The fundamental problem of communication 

According to Claude Shannon, there is a fundamental problem is that of reproducing, at one point, either exactly or approximately a message selected at another point. 


# Encoder/Decoder pairs 
Suppose we have some set $\mathcal{S}=\{ 1,2\dots,S \}$ of possible messages. 
The sender, and receiver agree on what these are. 
As an example, use codewords created by [[Huffman coding]] on some ensemble. 

When we communicate, the sender must encode messages into some input alphabet $\mathcal{X}$
The receiver then receives some (possibly corrupt) element from some output alphabet $\mathcal{Y}$
The bits the sender sends, may or may not be the bits that the receiver receives. 

Formally, the encoder is denoted $enc:\mathcal{S}\to \mathcal{X}^N$, and $dec:\mathcal{Y}^N \to \mathcal{S}$

In some sense, source coding is already encoding a message, but we often need to add something in to our code for noise tolerance. 

An $N>1$ is representative of multiple uses of a channel.


![[Discrete channel]]

# Inferring probability 
Suppose we know $p(x)$, and given a particular output $y$ received over a channel $Q$, how likely was the input $x \in \mathcal{X}$ transmitted?
This is the **prime** use case for [[Bayes theorem|bayesian inference]].

Suppose $P(x=0) = P(x=1) = 0.5$. What are the probability that $x = 0$ was transmitted over a [[Discrete channel#The binary symmetric channel|binary symmetric channel]] $Q$ with $f = 0.1$ given that a $y = 0$ was received?

$$
P(x=0 \mid y=0) = \frac{0.9 \times 0.5}{0.9 \times 0.5 + 0.1 \times 0.5} = 0.9
$$

Similarly, $P(x=1 \mid y=1) = 0.9$.

What if $P(x=0) = 0.01$?

$$
P(x=0 \mid y=0) = \frac{0.9 \times 0.01}{0.9 \times 0.01 + 0.1 \times 0.99} \approx 0.0833.
$$
# Getting to it 
Suppose we know we have to communicate some message over a channel $Q$ and we want to build an encoder/decoder pair to send a message $\mathbf{s}$ over $Q$

Our reliability is measured as the probability of error, being the probability of $\mathbf{s}_{out }$ being different to $s_{in}$
$p(s_{out}\not=s_{in})=\sum_{\mathbf{s}}P(s_{out}\not=s_{in}|s_{in}=\mathbf{s})P(\mathbf{s}_{in}=\mathbf{s})$


### Example 
Consider a [[Discrete channel#The binary symmetric channel|binary symmetric channel]] $Q=\begin{bmatrix}1-f  &  f  \\  f  &   1-f\end{bmatrix}$ 
with $f=0.1$
Its base probabilities are $(p_{a},p_{b})=(0.5,0.5)$

$$\begin{aligned}
P(\mathbf{s}_{in} \neq \mathbf{s}_{out}) &= P(\mathbf{s}_{in} = \texttt{a}, \mathbf{s}_{out} = \texttt{b}) + P(\mathbf{s}_{in} = \texttt{b}, \mathbf{s}_{out} = \texttt{a}) \\
&= P(\mathbf{s}_{out} = \texttt{b} \mid \mathbf{s}_{in} = \texttt{a})\,P(\mathbf{s}_{in} = \texttt{a}) + \\
&\quad P(\mathbf{s}_{out} = \texttt{a} \mid \mathbf{s}_{in} = \texttt{b})\,P(\mathbf{s}_{in} = \texttt{b}) \\
&= P(y=1 \mid x=0)\,p_{\texttt{a}} + P(y=0 \mid x=1)\,p_{\texttt{b}} \\
&= f =0.1
\end{aligned}$$
Now suppose we encode $a \to 000$, $b \to 111$
To decode, we count the number of $1$s and $0$s and sell all the bits to the majority count to determine $\mathbf{s}$.
So $000,001,010,100$ all get set to $a$, and $111,110,101,011$ all get set to $b$
If the channel $Q$ is binary symmetric with $f = 0.1$ again

$$\begin{aligned}
P(\mathbf{s}_{in} \neq \mathbf{s}_{out}) &= P(\mathbf{y} \in B \mid 000)\,p_{\texttt{a}} + P(\mathbf{y} \in A \mid 111)\,p_{\texttt{b}} \\
&= [f^3 + 3f^2(1-f)]\,p_{\texttt{a}} + [f^3 + 3f^2(1-f)]\,p_{\texttt{b}} \\
&= f^3 + 3f^2(1-f) = 0.028
\end{aligned}$$
Our error has dropped, but our rate has also dropped, so instead of 1 bit communicating a symbol, 3 bits communicate one. 

The challenge is illustrated below 
![[Pasted image 20261018170912.png]]

Here, $R$ is the amount of bits per symbol, and the y axis as the error.