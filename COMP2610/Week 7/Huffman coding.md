This is the most "optimal" form of symbol coding. 

The basic idea is to take the two least probable symbols in the alphabet, prepend bits $0,1$ to the current codeword of symbols, combine the two symbols into a meta-symbol and repeat. 

# Formally 
Let $X$ be an [[ensemble]] with alphabet $\mathcal{A}$

1: If $\lvert \mathcal{A} \rvert=2$, return $C=\{ 0,1 \}$
2: Else, let $a,a' \in \mathcal{A}$ be the least probable symbols.
3: Let $\mathcal{A}'=\mathcal{A} \setminus \{ a,a' \}\cup \{ aa' \}$
4: Let $\mathcal{P}'=\mathcal{P}-\{ p_{a},p_{a'} \}\cup \{ p_{aa'} \}$, where $p_{aa'}=p_{a}+p_{a'}$
5: Compute $C'=HUFFMAN(\mathcal{A}',\mathcal{P}')$
6: Define $C$ by the following:
	$c(a)=c'(aa')0$
	$c(a')=c(aa')1$
	$c(x)=c'(x)$ for $x \in \mathcal{A}$
7: return $C$


![[Pasted image 20261014105023.png|425]]


# Use cases
There are certain pros and cons of [[Huffman coding]].

The pros are mainly that it produces [[prefix code]]s automatically, the algorithm is simple to understand and compute. Additionally, [[Huffman coding]] is provably optimal, as in and other [[uniquely decodable]] code $C'$ will have $L(C_{huff},X)\leq L(C',X)$

However, we assume a fixed distribution of symbols, and the extra bit given by the [[source coding theorem for symbol codes]] means that for small entropy, codes can be close to $2\times$ that.
