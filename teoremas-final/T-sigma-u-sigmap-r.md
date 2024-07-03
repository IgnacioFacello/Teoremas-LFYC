---
tags:
  - lfyc-c-IX
  - "#review"
  - flashcards
---
> $T^{n,m}$ es $(\Sigma\cup\Sigma_p)$-recursiva.

- - - 
Sale directo por el *lema de minimización*. Este lema nos dice que dado un predicado $P$ $\Sigma$-e.c. con $D_P$ $\Sigma$-e.c. entonces $M(P)$ es $\Sigma$-e.c.. Y si $M(P)$ es $\Sigma$-e.c. entonces es $\Sigma$-r.

Por definición $T^{n,m}=M({Halt}^{n,m})$. Notar que
$$
D_{T^{n,m}}=\{
(\vec{x},\vec{\alpha},\mathcal{P})\in\omega^{n}\times\Sigma^{\ast m}\times{Pro^{\Sigma}}:\mathcal{P}\text{ termina partiendo desde el }
\}
$$
Probamos anteriormente que ${Halt}^{n,m}$ es $\Sigma\cup\Sigma_{p}$-r y tenemos que
$$
D_{Halt^{n,m}}=\omega^{n+1}\times\Sigma^{\ast m}\times{Pro^{\Sigma}}
$$
Entonces por el lema de la minimización tenemos que $T^{n,m}$ es $\Sigma$-r.