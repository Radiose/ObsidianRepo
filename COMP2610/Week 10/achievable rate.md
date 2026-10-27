Ideally, we want to consider [[rate of block code|rates]] of transmission which we can guarantee small error.
In particular, achievable rates act as a sort of analytic tool to guarantee arbitrarily small errors.
# definition 
A rate $R$ over a channel $Q$ is said to be achievable if $$\forall\epsilon>0 \quad \exists(N,K)\text{ and decoder}\quad : \frac{K}{N}\geq R\ \  \land \ \ p_{BM}=max_{\mathbf{s}_{in}}(P(\mathbf{s_{out}}\not=\mathbf{s}_{in}| \mathbf{s}_{in}))< \epsilon$$
