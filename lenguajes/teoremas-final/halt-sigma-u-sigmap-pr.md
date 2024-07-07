---
tags:
  - lfyc-c-IX
---
> **Lema 20** $Halt^{n,m}$ es $(\Sigma\cup\Sigma_p)$-recursiva
?

- - - 
Notar que 
$$
Halt^{n,m}= \lambda{xy}[x=y]\circ\left[
    i^{n,m},
    \lambda{\mathcal{P}}\left[n(\mathcal{P})+1\right]\circ
        {p_{(n+1)+(m+1)}^{n+1,m+1}}
\right]
$$
Sabemos que $i^{n,m}$ y $n(\mathcal{P})$ son $(\Sigma\cup\Sigma_p)$-recursivas por el teorico.