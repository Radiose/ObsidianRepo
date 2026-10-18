A discrete channel $Q$ will do 2 things
	1: Accept some input from $\mathcal{X}$
	2: Product some output from $\mathcal{Y}$

There is probability associated with various outputs given an input. This represents inherent noise, which could depend on the input. 

# Formally 
A discrete channel $Q$ consists of 
- An input alphabet $\mathcal{X}=\{ a_{1},\dots,a_{n} \}$
- An output alphabet $\mathcal{Y}=\{ b_{1},\dots,b_{n} \}$
- Transition probabilities $P(y|x)$
We can express the channel $Q$ as a [[matrix]]
$Q_{i,j}=P(y=b_{j}|x=a_{i})$
The probability of observing $b$ given we transmit $a$

**Example**: A channel $Q$ with inputs $\mathcal{X} = \{a_1, a_2, a_3\}$, outputs $\mathcal{Y} = \{b_1, b_2\}$, and transition probabilities expressed by the matrix

$$
Q = \begin{bmatrix} 0.8 & 0.5 & 0.2 \\ 0.2 & 0.5 & 0.8 \end{bmatrix}
$$

So $P(b_1 \mid a_1) = 0.8 = P(b_2 \mid a_3)$ and $P(b_1 \mid a_2) = P(b_2 \mid a_2) = 0.5$.

# Examples of channels 

There are many examples of channels 

## The binary noiseless channel 
This is probably the simplest channel. The received symbol is always equal to the transmitted symbol. Hence, the reference of noiseless.
$\mathcal{X}=\{ 0,1 \}$, $\mathcal{Y}=\{ 0,1 \}$
The transition matrix looks like $\begin{bmatrix}1 & 0 \\  0 & 1\end{bmatrix}$


## The noisy overlapping channel 
Even if there is uncertainty about the input, it may still be possible to infer what was transmitted. This example is a good showcase of that 
$\mathcal{X}=\{ 0,1 \} ,\ \mathcal{Y}=\{ a,b,c,d \}$ and $Q=\begin{bmatrix} 0.5  &  0 \\  0.5  &  0 \\  0  &  0.5  \\  0  &  0.5\end{bmatrix}$
What was transmitted over the channel if we receive $abba \ ddcd$?

## The binary symmetric channel 
Each symbol sent across a binary symmetric channel has a chance of being flipped to its counterpart. 
$(0 \to 1; 1\to 0)$

Decoding a message here relies on the probability of the bit being flipped, denoted $f$
for $\mathcal{X},\mathcal{Y}=\{ 0,1 \}$
The transition probabilities $Q = \begin{bmatrix}1-f  & f \\  f  &  1-f\end{bmatrix}$


## The Z channel 
Sometimes, symbols may be corrupted over the channel asymmetrically. 
The transition probabilities $Q=\begin{bmatrix}1  &  f  \\  0   &  1-f\end{bmatrix}$
[[Communication over noisy channels#Inferring probability|inferring our input]]: Clearly $P(x=1 \mid y=1) = 1$ but

$$
P(x=0 \mid y=0) = \frac{P(y=0 \mid x=0)\,P(x=0)}{\sum_{x' \in \mathcal{X}} P(y=0 \mid x')\,P(x')} = \frac{P(x=0)}{P(x=0) + f\,P(x=1)}$$

So $P(x=0 \mid y=0) \to 1$ as $f \to 0$, and goes to $P(x=0)$ as $f \to 1$