---
tags:
  - lfyc-c-IIX
---
> **Lema 17** Supongamos que $\Sigma\supseteq\Sigma_p$. Entonces $$A=\{\mathcal{P}\in{Pro}^{\Sigma}:{AutoHalt}^{\Sigma}(\mathcal{P})=1\}$$ es $\Sigma$-recursivamente enumerable y no es $\Sigma$-recursivo. Mas aun, el conjunto $$N=\{\mathcal{P}\in{Pro}^{\Sigma}:{AutoHalt}^{\Sigma}(\mathcal{P})=0\}$$ no es $\Sigma$-recursivamente enumerable.

---
> Clave 1: Definimos P en base a Halt que es $(\Sigma\cup\Sigma_p)$-pr. Y como $\Sigma\supseteq\Sigma_p$ entonces es $\Sigma$-pr
> Clave 2: **Lema de minimización acotada** nos dice que M(P) es $\Sigma$-pr
> Claramente M(P) tiene como dominio los programa que terminan partiendo de si mismos, es decir $A$
> Luego A es $\Sigma$-r.e. por ser dominio de una función $\Sigma$-r.

Sea $$P=\lambda{t\mathcal{P}}\left[{Halt}^{0,1}(t,\mathcal{P},\mathcal{P})\right]$$, como ${Halt}^{0,1}$ es $(\Sigma\cup\Sigma_p)$-p.r. es también $\Sigma$-p.r. ya que suponemos $\Sigma\supseteq\Sigma_p$. Por lo tanto se puede ver que $P$ es $\Sigma$-p.r. y por el *lema de la minimización acotada* tenemos que $M(P)$ es $\Sigma$-recursivo. Además se puede ver que $D_{M(P)}=A$, lo que implica que A es $\Sigma$-recursivamente enumerable.
 - - -
> Probamos por absurdo, definiendo AutoHalt en base a *division por casos* en N y A. 
> Llegamos a que AH es $\Sigma$-r lo cual es absurdo

Veamos ahora que N no es $\Sigma$-r.e., haremos la prueba por absurdo. Supongamos que ($\ast$) $N$ es $\Sigma$-recursivamente enumerable. Como $C_{k}^{n,m},n,m,k\in\omega$ es $\Sigma$-recursiva. Entonces las funciones $C_{0}^{0,1}|_{N}$ y $C_{1}^{0,1}|_{A}$ son $\Sigma$-recursivas ya que $A$ y $N$ son $\Sigma$-r.e.. 
Luego, notar que $${AutoHalt}^{\Sigma}=C_{0}^{0,1}|_{N}\cup{C}_{1}^{0,1}|_{A}$$ y por el *lema de division por casos para funciones recursivas* será $\Sigma$-recursivo. Vemos que la suposición ($\ast$) nos lleva a un resultado que contradice el [[autohalt-no-r|lema 15]] de los combos y por lo tanto $N$ no es $\Sigma$-r.e.
 - - - 
>  Nuevamente por absurdo, definimos N en base a A y contradecimos la conclusion anterior

Finalmente supongamos que ($\ast$) $A$ es $\Sigma$-recursivo y otra vez probemos lo contrario por absurdo.
Por el teórico sabemos que si $S_1,S_2\in\omega^{n}\times\Sigma^{\ast m}$ son $\Sigma$-recursivos, entonces $S_1\cup{S_2}$, $S_1\cap{S_2}$ y $S_1-S_2$ también lo son. Entonces $$N=(\Sigma^{\ast}-A)\cap{Pro}^{\Sigma}$$ también deberá ser $\Sigma$-recursivo, lo cual contradice lo que probamos anteriormente y por lo tanto $A$ no es $\Sigma$-recursivo.