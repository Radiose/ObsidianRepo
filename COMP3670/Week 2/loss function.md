A loss function $l$ assigns to each pair a non negative number, being the price of predicting $h(\mathbf{x})$.
$l((\mathbf{x},y),h)\geq {0}$
The choice of $l$ follows the type of the outcome. 
# squared loss 
For continuous cases, we use the squared loss 
$l(\mathbf{x},y)h)=(y-h(\mathbf{x}))^2$


# Binary loss 
For discrete, we can use the binary loss 
$l((\mathbf{x},y)h)=\mathbb{1}\{ h(\mathbf{x})\not=y \}$

out of sample error
This is what enables us to determine the expected loss under a joint distribution $P$
