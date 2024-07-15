---
tags:
  - flashcards
---
03. [[division-casos-pr|Lema 3]] Supongamos $f_i:D_{f_i}\subseteq\omega^n\times\Sigma^{}*m\to\Sigma^*, i=1,\dots,k$ son funciones $\Sigma$-pr tales que $D_j\cap D_i=\emptyset$ para todo $i\neq j$. Entonces $\bigcup^k_{i=1} f_i$ es $\Sigma$-pr.
04. [[caracterización-conjunto-enumerable|Proposición 4]] Sea $S\subseteq\omega^{n}\times\Sigma^{*m}$ un conjunto no vacío. Entonces son equivalentes:
	(1) $S$ es $\Sigma$-enumerable
	 	(es decir) Existe $F:\omega\to\omega^{n}\times\Sigma^{*m}$ tal que $Im(F) = S$ y  las $F_{(i)},\ i=1,\dots,n+m$ son $\Sigma$-computables.
	(2) Hay un programa $\mathcal P\in Pro^{\Sigma}$ tal que:
	 	(a) Para cada $x\in\omega$, tenemos que $\mathcal P$ se detiene partiendo desde el estado $||x||$ y llega a un estado de la forma $((x_1,\dots,x_n),(\alpha_1,\dots,\alpha_m))$ tal que $(x_1,\dots,x_n,\alpha_1,\dots,\alpha_m)\in S$
	 	(b) Para todo $(x_1,\dots,x_n,\alpha_1,\dots,\alpha_m)\in S$ hay un $x\in\omega$ tal que $\mathcal P$ se detiene partiendo desde el estado $||x||$ y llega a un estado de la forma $((x_1,\dots,x_n),(\alpha_1,\dots,\alpha_m))$
	(Caso n=2, m=1)
?
03. 
<!--SR:!2024-07-18,3,250-->