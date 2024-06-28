---
tags:
  - lfyc-c-III
---
> Si $f: D_f\subseteq \omega^n\times\Sigma^{*m}\to O$ es $\Sigma$-[[paradigma-neumann|computable]] entonces $f$ es $\Sigma$-[[paradigma-godel|recursiva]] 

---
## Caso alfabético $O=\Sigma^*$
Sea $\mathcal P_0$ un programa que compute a $f$. Primero veremos que $f$ es $(\Sigma\cup\Sigma_p)$-recursiva. Notar que
$$f=E_{*1}^{n,m}\circ[T^{n,m}\circ[p_1^{n,m},\dots,p_{n+m}^{n,m},C_{\mathcal P_0}^{n,m}],p_1^{n,m},\dots,p_{n+m}^{n,m},C_{\mathcal P_0}^{n,m}]$$
Como demostramos anteriormente, E\* y T son $(\Sigma\cup\Sigma_p)$-r y por lo tanto f también lo es.
Finalmente por el teorema de independencia del alfabeto tenemos que f es $\Sigma$-r $\square$.
## Caso numérico $O=\omega$
Idem con E#
