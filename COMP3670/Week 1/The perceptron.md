This is one of the simplest ML models 
We fix the [[hypothesis set]] accordingly:
$\mathcal{H}$ = the set of linear threshold functions. 

Binary [[classification]]: $\mathcal{Y}=\{ +1,-1 \}$, features $\mathbf{x}=(x_{1},\dots,x_{n}) \in \mathcal{X}=\mathbb{R}^n$= all [[vector]]s of $n$ real numbers. 

Each hypothesis in $\mathcal{H}$ has the form $h_{w}(x) =\text{sign}(w_{1}x_{1}+w_{2}x_{2}+\dots+w_{n}x_{n}+w_{0})$ - we take in some weighted sum of the inputs, and output according to the sign. $+1$ if sign > 0 and -1 if      sign $\leq 0$. $\mathbf{w}=(\mathbf{w}_{0},\mathbf{w}_{1}\dots+\mathbf{w_{n}})$. 

We formally define $\mathcal{H}=\{ h_{w}:w_{0},w_{1}\dots w_{n}\in \mathbb{R} \}$, or the set of all possible weights. 
$|\mathcal{H}|=\infty$.
