$\chi_{T}(T)=0$, where $\chi_{T}$ is the [[characteristic polynomial]] of $T$.

### Proof 
It is enough to consider the restriction $S:=T_{G(\lambda,T)}$ of $T$ to each [[generalised eigenspace]]
$U:= G(\lambda,T)$ satisfies $\chi_{T}(S)=0$

let $d =\dim(U)$ be the algebraic multiplicity of $\lambda$, then $\chi_{T}(z)$ has a factor $q(z):=(z-\lambda)^d$. 
We notice that $S-\lambda I$ is a [[nilpotent operator]] on $U$, because $U=G(\lambda,T)=\ker(T-\lambda I)^{\dim(v)}$

Hence, $(S-\lambda I)^d=0$, because $d=\dim(U)$. We then get $q(S)=(S-\lambda I)^d=0$
And since $q(z)$ is a factor of $\chi_{T}(z)$, we get $\chi_{T}(S)=0$
