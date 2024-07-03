---
tags:
  - lfyc-c-III
---
> **Teorema 5** Si $f: D_f\subseteq \omega^n\times\Sigma^{*m}\to\Sigma^*$ es $\Sigma$-[[paradigma-neumann|computable]] entonces $f$ es $\Sigma$-[[paradigma-godel|recursiva]]
?

---
> Clave 1 : Existe un programa $\mathcal P_0$ que computa a $f$
> Clave 2 : $E_{*1}$ y $T^{n.m}$ son $(\Sigma\cup\Sigma_p)$-r.
> Clave 3: proposición de independencia del alfabeto
> Usamos C1, C2 y la concatenación. $E_{*1}$ nos dice el resultado del programa y $T^{n.m}$ el numero de pasos necesarios para que termine. Con ambos podemos dar una función $(\Sigma\cup\Sigma_p)$-recursiva igual a $f$
> Luego por C3 tenemos que es $\Sigma$-r
## Caso alfabético $O=\Sigma^*$
Sea $\mathcal P_0$ un programa que compute a $f$. Primero veremos que $f$ es $(\Sigma\cup\Sigma_p)$-recursiva. Notar que
$$f=E_{*1}^{n,m}\circ[T^{n,m}\circ[p_1^{n,m},\dots,p_{n+m}^{n,m},C_{\mathcal P_0}^{n,m}],p_1^{n,m},\dots,p_{n+m}^{n,m},C_{\mathcal P_0}^{n,m}]$$
Como demostramos anteriormente, $E_{*1}$ y $T^{n,m}$ son $(\Sigma\cup\Sigma_p)$-r y por lo tanto $f$ también lo es.
Finalmente por la *proposición de independencia del alfabeto* tenemos que $f$ es $\Sigma$-r.
$$\tag*{$\blacksquare$}$$
