# Self punctuating property 
This is a property of some [[uniquely decodable]] codes, where the code will automatically be readable purely just by looking for the first possible codeword. Example is $C_{3}=\{ 0,10,110,111 \}$

# Prefix code
A codeword $\mathbf{c} \in \{ 0,1 \}^+$ is said to be a prefix of another codeword $\mathbf{c}'\in \{ 0,1 \}^+$ if there exists a string $\mathbf{t}\in \{ 0,1 \}^+$ such that $\mathbf{c'}=\mathbf{ct}$  

Basically, can you create $\mathbf{c'}$ by gluing something to the end of $\mathbf{c}$?

A code $C=\{ \mathbf{c}_{1},\dots,\mathbf{c}_{I} \}$ is a prefix code if for every codeword $\mathbf{c}_{i}\in C$, there is no prefix of $\mathbf{c}_{i}$ in $C$.

Note that prefix code $\implies$ [[uniquely decodable]], but the converse doesn't hold. 
