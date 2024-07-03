---
tags:
  - lfyc-c-IIX
---
> **Lema 17** Supongamos que $\Sigma\supseteq\Sigma_p$. Entonces $$A=\{\mathcal{P}\in{Pro}^{\Sigma}:{AutoHalt}^{\Sigma}(\mathcal{P})=1\}$$ es $\Sigma$-recursivamente enumerable y no es $\Sigma$-recursivo. Mas aun, el conjunto $$N=\{\mathcal{P}\in{Pro}^{\Sigma}:{AutoHalt}^{\Sigma}(\mathcal{P})=0\}$$ no es $\Sigma$-recursivamente enumerable.
?

---
> P es el predicado 'El programa termina en t pasos partiendo de si mismo'
> M(P) es 'Mínimo t para el cual se cumple P'
> Claramente M(P) tiene como dominio los programa que terminan partiendo de si mismos

Sea $$P=\lambda{t\mathcal{P}}\left[{Halt}^{0,1}(t,\mathcal{P},\mathcal{P})\right]$$
, como ${Halt}^{0,1}$ es $(\Sigma\cup\Sigma_p)$-p.r. es también $\Sigma$-p.r. ya que suponemos $\Sigma\supseteq\Sigma_p$. Por lo tanto se puede ver que $P$ es $\Sigma$-p.r. y por el *lema de la minimización acotada* tenemos que $M(P)$ es $\Sigma$-recursivo. Además se puede ver que $D_{M(P)}=A$, lo que implica que A es $\Sigma$-r.e..
 - - -
Por otro lado, si suponemos que ($\ast$) $N$ es $\Sigma$-r.e. Como 
- $C_{k}^{n,m},n,m,k\in\omega$ es $\Sigma$-r..
Entonces las funciones $C_{0}^{0,1}|_{N}$ y $C_{1}^{0,1}|_{A}$ son $\Sigma$-recursivas ya que $A$ y $N$ son $\Sigma$-r.e.. Luego, por el *lema de division por casos para funciones recursivas* $${AutoHalt}^{\Sigma}=C_{0}^{0,1}|_{N}\cup{C}_{1}^{0,1}|_{A}$$ será $\Sigma$-recursivo. La suposición ($\ast$) nos lleva a un resultado que contradice el *lema 15* y por lo tanto $N$ no es $\Sigma$-r.e.
 - - - 
Finalmente supongamos que ($\ast$) $A$ es $\Sigma$-recursivo.
Por el teórico sabemos que si $S_1,S_2\in\omega{n}\times\Sigma^{\ast m}$ son $\Sigma$-recursivas, entonces $S_1\cup{S_2}$, $S_1\cap{S_2}$ y $S_1-S_2$ también lo son. Entonces
$$N=(\Sigma^{\ast}-A)\cap{Pro}^{\Sigma}$$ también deber´a serlo, lo cual contradice lo que probamos anteriormente y por lo tanto $A$ no es $\Sigma$-recursivo.