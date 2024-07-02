---
tags:
  - lfyc-c-II
  - lfyc-c-IV
---
> **Proposición 4** Sea $S\subseteq\omega^{n}\times\Sigma^{*m}$ un conjunto no vacío. Entonces son equivalentes:
> (1) $S$ es $\Sigma$-enumerable 
> 	(es decir) Existe $F:\omega\to\omega^{n}\times\Sigma^{*m}$ tal que $Im(F) = S$ y  las $F_{(i)},\ i=1,\dots,n+m$ son $\Sigma$-computables.
> (2) Hay un programa $\mathcal P\in Pro^{\Sigma}$ tal que:
> 	(a) Para cada $x\in\omega$, tenemos que $\mathcal P$ se detiene partiendo desde el estado $||x||$ y llega a un estado de la forma $((x_1,\dots,x_n),(\alpha_1,\dots,\alpha_m))$ tal que $(x_1,\dots,x_n,\alpha_1,\dots,\alpha_m)\in S$ 
> 	(b) Para todo $(x_1,\dots,x_n,\alpha_1,\dots,\alpha_m)\in S$ hay un $x\in\omega$ tal que $\mathcal P$ se detiene partiendo desde el estado $||x||$ y llega a un estado de la forma $((x_1,\dots,x_n),(\alpha_1,\dots,\alpha_m))$

(Caso n=2, m=1)

--- 
> Por hipótesis existe una función que computa el conjunto S no vacío
> Podemos definir macros para sus coordenadas $\Sigma$-computables
> Las usamos para dar el programa que cumple con (a) y (b).

($(1)\implies(2)$) Dado que S no es vacío, tenemos por hipótesis tenemos que existe alguna función $F:\omega\to\omega^{2}\times\Sigma^{*1}$ tal que  $I_F=S$ y $F_{(i)}$ es $\Sigma$-computable para cada $i\in\{1,2,3\}$.
Luego, por la *Proposición de las Macros* tenemos que existen las siguientes Macros:
$$
\begin{align}
&[V2\gets F_{(1)}(V1)]\\
&[V2\gets F_{(2)}(V1)]\\
&[W2\gets F_{(3)}(V1)]\\
\end{align}
$$
Las cuales nos permiten dar el siguiente programa
$$
\begin{align} 
&[P3\gets F_{(3)}(N1)]\\
&[N2\gets F_{(2)}(N1)]\\
&[N1\gets F_{(1)}(N1)]\\
\end{align}
$$

Que claramente termina para todo estado $||x||, x\in\omega$ y ademas termina en algún estado de la forma $((x_1,x_2,y_1,\dots),(\alpha_1,\beta_1,\dots))$ tal que $(x_1,x_2,\alpha_1)\in S$.

<div style="page-break-after: always;"></div>

--- 
> Suponemos $P\in Pro^{\Sigma}$ cumple con (a) y (b) de 2. 
> Extraemos del mismo los i sub-programas que calculan las $F_{(i)}$
> Notar que las horquillas de los $n+m$ sub-programas resultante tienen las propiedades que hacen que enumere a S

($(2)\implies(1)$) Suponemos $P\in Pro^{\Sigma}$ cumple con (a) y (b) de 2. Sean:
$$
\begin{align}
	\mathcal P_1 &= \mathcal PN1\gets N1 \\
	\mathcal P_2 &= \mathcal PN1\gets N2 \\
	\mathcal P_{3} &= \mathcal PN1\gets P1 \\
\end{align}
$$
Las concatenaciones del programa con la instrucción que guarda en $N1$ la coordenada relevante. Usando estos programas podemos definir las $n+m$ funciones $\Sigma$-computables
$$
\begin{align}
	F_{(1)} &= \Psi^{1,0,\#}_{\mathcal P_1} \\
	F_{(2)} &= \Psi^{1,0,\#}_{\mathcal P_2} \\
	F_{(3)} &= \Psi^{1,0,*}_{\mathcal P_{3}} \\
\end{align}
$$
Tales que definen $F = [F_{(1)},F_{(2)},F_{(3)}]:\omega\to\omega^{2}\times\Sigma^{*1}$ que computa al conjunto $S$.

Por hipótesis el programa $\mathcal P$ termina para todo estado inicial $||x||, x\in\omega$ y ademas su estado final es de la forma $((x_1,x_2,y_1,\dots),(\alpha_1,\beta_1,\dots))$ tal que $(x_1,x_2,\alpha_1)\in S$.
Es decir cada programa $\mathcal P_i$ también termina para todo estado inicial $||x||, x\in\omega$ y la primera coordenada del estado al terminar contiene el i-esimo elemento de $(x_1,x_2,\alpha_1)\in S$, es decir que $I_F=S$.
$$\tag*{$\blacksquare$}$$