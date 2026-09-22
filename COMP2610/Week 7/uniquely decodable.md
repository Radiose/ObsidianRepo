[[source code|lossless code]] with ensure that when working with a single outcome, we can decode it uniquely. 

However, when dealing with variable length codes, it is useful to require the following:

### Uniquely decodable 
A code $c$ for $X$ is uniquely decodable if no two strings from $\mathcal{A}_{X}^+$ have the same codeword,
$\forall \mathbf{x},\mathbf{y}\in A_{X}^+$, $\mathbf{x}\not=\mathbf{y}\implies c(\mathbf{x})\not=c(\mathbf{y})$



![[prefix code]]