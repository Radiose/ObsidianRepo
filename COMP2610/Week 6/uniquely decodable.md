[[source code|lossless code]] with ensure that when working with a single outcome, we can decode it uniquely. 

However, when dealing with variable length codes, it is useful to require the following:

### Uniquely decodable 
A code $c$ for $X$ is uniquely decodable if no two strings from $\mathcal{A}_{X}^+$ have the same codeword,
$\forall \mathbf{x},\mathbf{y}\in A_{X}^+$, $\mathbf{x}\not=\mathbf{y}\implies c(\mathbf{x})\not=c(\mathbf{y})$


# Self punctuating property 
This is a property of some [[uniquely decodable]] codes, where the code will automatically be readable purely just by looking for the first possible codeword. Example is $C_{3}=\{ 0,10,110,111 \}$

Prefix codes
A codeword $\mathbf{c} \in \{ 0,1 \}^+$ is said to be a prefix of another codeword $\mathbf{c}'\in \{ 0,1 \}^+$ if there exists a string $\mathbf{t}\in \{ 0,1 \}^+$ such that $\mathbf{c'}=\mathbf{ct}$  

Basically, can you create $\mathbf{c'}$ by gluing something to the end of $\mathbf{c}$?