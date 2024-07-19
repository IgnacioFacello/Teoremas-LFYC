---
tags:
  - flashcards
---
09. [[intersección-conjuntos-efectivamente-enumerables|Lema 9]] Sean $S_1,S_2\subseteq\omega^n\times\Sigma^{*m}$ conjuntos $\Sigma$-efectivamente enumerables. Entonces $S_1\cap S_2$ es $\Sigma$-efectivamente enumerable
10. [[lemma-cuantificación-acotada|Lema 10]] Sea $\Sigma$ un alfabeto finito. Sea $P:S\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m\to\omega$ un predicado $\Sigma$-p.r., con $S,S_1,\dots,S_n\subseteq\omega$ y $L_1\dots,L_m\subseteq\Sigma^*$ no vacío.
	 Supongamos $\bar S\subseteq S$ es $\Sigma$-pr. Entonces $$\lambda x\vec x\vec\alpha\left[(\forall t\in\bar{S})_{t\leq x} P(t,\vec x,\vec\alpha)\right]$$ es $\Sigma$-pr.
?
09. Suponemos no vacío. Iteramos en $\omega^2$, generando valores de $S_1$ y $S_2$ y devolviendo el valor generado si es el mismo y $e_0$ caso contrario.
10. Extendemos el predicado a $\omega\times\dots$ agregando $C_1$ fuera de $\bar S$. Creamos una productoria desde 0 hasta $x$ usando la extensión $\bar{P}$
<!--SR:!2024-07-21,2,250-->