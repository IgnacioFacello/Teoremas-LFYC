---
tags:
  - flashcards
---
07. [[caracterización-conjunto-enumerable|Proposición 4]] Sea $S\subseteq\omega^{n}\times\Sigma^{*m}$ un conjunto no vacío. Entonces son equivalentes:
	(1) $S$ es $\Sigma$-enumerable
	 	(es decir) Existe $F:\omega\to\omega^{n}\times\Sigma^{*m}$ tal que $Im(F) = S$ y  las $F_{(i)},\ i=1,\dots,n+m$ son $\Sigma$-computables.
	(2) Hay un programa $\mathcal P\in Pro^{\Sigma}$ tal que:
	 	(a) Para cada $x\in\omega$, tenemos que $\mathcal P$ se detiene partiendo desde el estado $||x||$ y llega a un estado de la forma $((x_1,\dots,x_n),(\alpha_1,\dots,\alpha_m))$ tal que $(x_1,\dots,x_n,\alpha_1,\dots,\alpha_m)\in S$
	 	(b) Para todo $(x_1,\dots,x_n,\alpha_1,\dots,\alpha_m)\in S$ hay un $x\in\omega$ tal que $\mathcal P$ se detiene partiendo desde el estado $||x||$ y llega a un estado de la forma $((x_1,\dots,x_n),(\alpha_1,\dots,\alpha_m))$
	(Caso n=2, m=1)
08. [[lemma-sumatoria|Lema 8]] Sea $\Sigma$ un alfabeto finito. Si $f:\omega\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m\to\omega$ es $\Sigma$-pr, con $S_1,\dots,S_n\subseteq\omega$ y $L_1,\dots,L_m\subseteq\Sigma^*$ no vacíos, entonces la función $\lambda xy\vec x\vec\alpha\left[\sum_{t=x}^{t=y}f(t,\vec x,\vec\alpha)\right]$ es $\Sigma$-pr
?
07. Hecho antes
08. Def G. Damos h y g. Damos conjuntos que separan por casos. Definimos h y g por casos. Probamos que los conjuntos son pr.
<!--SR:!2024-07-19,4,270-->