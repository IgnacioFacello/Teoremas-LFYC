---
tags:
  - lfyc-c-IX
---
> $T^{n,m}$ es $(\Sigma\cup\Sigma_p)$-recursiva.

- - - 
Sale directo por el *lema de minimización*. Este lema nos dice que dado un predicado $P$ $\Sigma$-e.c. con $D_P$ $\Sigma$-e.c. entonces $M(P)$ es $\Sigma$-e.c..

Por definición $T^{n,m}=M({Halt}^{n,m})$. Notar que
$$
D_{T^{n,m}}=\{
(\vec{x},\vec{\alpha},\mathcal{P})\in\omega\times\Sigma^{\ast}\times{Pro^{\Sigma}}:\mathcal{P}\text{ termina partiendo desde el }
\}
$$