---
tags:
  - lfyc-c-V
---
> **Lema 10**  Sea $\Sigma$ un alfabeto finito. Sea $P:S\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m\to\omega$ un predicado $\Sigma$-p.r., con $S,S_1,\dots,S_n\subseteq\omega$ y $L_1\dots,L_m\subseteq\Sigma^*$ no vacío.  
> Supongamos $\bar S\subseteq S$ es $\Sigma$-pr. Entonces $$\lambda x\vec x\vec\alpha\left[(\forall t\in\bar{S})_{t\leq x} P(t,\vec x,\vec\alpha)\right]$$ es $\Sigma$-pr.
?

- - - 
> - P es $\Sigma$-p.r.
> - Definimos una version $\bar{P}$ que puede tomar cualquier x en omega
> - La usamos para definir a cuantificación como una productoria pr
> - Esto nos dice que la cuantificación es pr

Sea 
$$
\bar{P}=
	P|_{
		\bar{S}\times{S_1}\times\dots\times{S_n}\times{L_1}\times\dots\times{L_m}
	}
\cup
	{C^{1+n,m}_{1}}|_{
		(\omega-\bar{S})\times{S_1}\times\dots\times{S_n}\times{L_1}\times\dots\times{L_m}
	}
$$
Notar que $\bar{P}$ tiene dominio $\omega\times{S_1}\times\dots\times{S_n}\times{L_1}\times\dots\times{L_m}$ y es $\Sigma$-p.r.. Y luego, ya que
$$
\begin{aligned}
\lambda{x\vec x\vec\alpha}[(\forall{t}\in\bar{S})_{t\leq{x}}P(x,\vec x,\vec\alpha)] 
	&= \lambda{x\vec x\vec\alpha}\left[\prod^{t=x}_{t=0}\bar{P}(t,\vec x,\vec\alpha)\right]\\
	&= \lambda{xy\vec x\vec\alpha}\left[\prod^{t=y}_{t=x}\bar{P}(t,\vec x,\vec\alpha)\right] \circ \left[C_0^{1+n,m},p_1^{1+n,m},\dots,p_{1+n+m}^{1+n,m}\right]
\end{aligned}
$$
tenemos que $\lambda{x\vec x\vec\alpha}[(\forall{t}\in\bar{S})_{t\leq{x}}P(x,\vec x,\vec\alpha)]$ es $\Sigma$-p.r. 