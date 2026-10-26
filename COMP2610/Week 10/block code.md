# Motivation 
Suppose we wanted to communicate over some [[channel|noisy channel]] $Q$, and we want to build an encoder/decoder pair to reliably send a message $\mathbf{s}$ over $Q$.

We consider codes that make *repeated use* of a noisy channel in order to communicate a predefined set of messages $\mathcal{S}=\{ 1,2\dots,S \}$

Recall a general [[Communication over noisy channels#Encoder/Decoder pairs|encoder]]$$enc:\mathcal{S}\to X^N$$Equivalently, each $s \in S$ is mapped to a unique block of symbols $\mathbf{x}\in \mathcal{X}^N$
We can imagine there being $S$ unique codewords $\mathbf{x}_{1},\dots,\mathbf{x}_{s}$, with each having block length $N$.


# Definition 
Given a channel $Q$ with inputs $\mathcal{X}$ and outputs $\mathcal{Y}$, an integer $N>0$ and $K \in \mathbb{R}^+$, an $(N,K)$ block code for $Q$ is a list of $S=2^k$ codewords $$\mathcal{C}=\{ \mathbf{x}_{1},\dots,\mathbf{x}_{2^k} \}$$Where each $\mathbf{x}_{s}\in \mathcal{X}^N$ consists of $N$ symbols from $K$.

We parametrise $K=\log_{2}S$ for mathematical simplicity.