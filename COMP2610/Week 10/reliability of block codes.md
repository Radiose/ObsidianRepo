Say we want some encoder/decoder pair to send messages over a [[channel]] $Q$.

# Definition 
Given a channel $Q$, the probability of block error for a code is $$ p_{B}=P(s_{out}\not=s_{in})= \sum_{\mathbf{s}_{in}}P(\mathbf{s}_{out}\not= \mathbf{s}_{in}| \mathbf{s}_{in})P(\mathbf{s}_{in})$$Its maximum probability of block error is $$p_{BM}=max_{\mathbf{s}_{in}}P(\mathbf{s}_{out}\not= \mathbf{s}_{in}|\mathbf{s}_{in})$$Note that because $P(\mathbf{s}_{out}\not= \mathbf{s}_{in}|\mathbf{s}_{in})\leq p_{BM}$, we get that $p_{B}\leq \sum_{\mathbf{s}_{in}}P(\mathbf{s}_{in})=P_{BM}$
Thus, $p_{BM} \to 0 \implies p_{B} \to 0$


# achievable rate
![[achievable rate]]