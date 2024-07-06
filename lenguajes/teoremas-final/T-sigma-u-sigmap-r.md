---
tags:
  - lfyc-c-IX
---
> **Proposición 21** $T^{n,m}$ es $(\Sigma\cup\Sigma_p)$-recursiva.
?

- - - 
Sale directo por el *lema de minimización*. Este lema nos dice que dado un predicado $P$ $\Sigma$-e.c. con $D_P$ $\Sigma$-e.c. entonces $M(P)$ es $\Sigma$-e.c.. Y si $M(P)$ es $\Sigma$-e.c. entonces es $\Sigma$-r.

Por definición $T^{n,m}=M({Halt}^{n,m})$.  Probamos anteriormente que ${Halt}^{n,m}$ es $(\Sigma\cup\Sigma_{p})$-recursiva y tenemos que
$$
D_{Halt^{n,m}}=\omega^{n+1}\times\Sigma^{\ast m}\times{Pro^{\Sigma}}
$$
Entonces por el lema de la minimización tenemos que $T^{n,m}$ es $\Sigma$-r.