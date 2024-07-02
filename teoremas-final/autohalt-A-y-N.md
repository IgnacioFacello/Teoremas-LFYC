---
tags:
  - lfyc-c-IIX
  - review
---
> **Lema 17** Supongamos que $\Sigma\supseteq\Sigma_p$. Entonces $$A=\{\mathcal{P}\in{Pro}^{\Sigma}:{AutoHalt}^{\Sigma}(\mathcal{P})=1\}$$ es $\Sigma$-r.e. y no es $\Sigma$-r. Mas aun, el conjunto $$N=\{\mathcal{P}\in{Pro}^{\Sigma}:{AutoHalt}^{\Sigma}(\mathcal{P})=0\}$$ no es $\Sigma$-r.e.

 - - - 
Sea $$P=\lambda{t\mathcal{P}}\left[{Halt}^{0,1}(t,\mathcal{P},\mathcal{P})\right]$$
> 'El programa termina en t pasos partiendo de si mismo?'

, como ${Halt}^{0,1}$ es $(\Sigma\cup\Sigma_p)$-p.r. es también $\Sigma$-p.r. ya que suponemos $\Sigma\supseteq\Sigma_p$. Por lo tanto se puede ver que $P$ es $\Sigma$-p.r. y por el *lema de la minimización acotada* tenemos que $M(P)$ es $\Sigma$-r. Además se puede ver que $D_{M(P)}=A$, lo que implica que A es $\Sigma-r.e$..
