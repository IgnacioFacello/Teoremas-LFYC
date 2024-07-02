---
tags:
  - "#lfyc-c-I"
  - lfyc-c-IIX
  - "#review"
---
> Si h es $\Sigma$*-[[paradigma-godel|recursiva]]* entonces es $\Sigma$*-[[paradigma-neumann|computable]]*

---
Prueba por inducción 
> (\*) Caso k : si $h\in R^\Sigma_k$ entonces es $\Sigma$*-computable*

## Caso k = 0
> Altamente trivial

 Sea $h\in R^\Sigma_0$
 Sean los siguientes programas los que computan las funciones básicas del paradigma de godel:
- $Succ$ : $N1\gets N1+1$
- $Pred$ : $N1\gets N1\dot-1$
- $C_0^{0,0}$ : $N1\gets 0$
- $C_\epsilon^{0,0}$ : $P1\gets\varepsilon$
- $d_a\quad a\in\Sigma$ : $P1\gets P1.a$
- $p_j^{n,m}$ : $N1\gets N\overline{j}\quad j\in{1,\dots,n}$
- $p_j^{n,m}$ : $P1\gets P\overline{j-n}\quad j\in{n+1,\dots,n+m}$
## Caso k+1
Sea $h\in R^\Sigma_{k+1} - R^\Sigma_k$
### Caso h=M(P)
Por (\*) tenemos que el predicado $P:\omega\times\omega^n\times\Sigma^{*m}\mapsto\omega$ es $\Sigma$*-computable* y por lo tanto podemos tomar un macro:
$$[IF\ P(V1,\dots, V\overline{n+1}),W\bar1,\dots, W\overline{m}\ GOTO\ A1]$$
luego podemos utilizarlo para definir el siguiente programa
$$
\begin{align}
L2\ & [IF\ P(N\overline{n+1},\dots, N\overline{n}),P\bar1,\dots, P\overline{m}\ GOTO\ L1] \\
&N\overline{n+1}\gets N\overline{n+1} + 1 \\
&GOTO\ L2 \\
L1\ & N1\gets N\overline{n+1}
\end{align}
$$
que claramente calcula el $M(P)$ y por lo tanto es $\Sigma$*-computable*.
Si recibe un estado fuera del dominio de M(P) entonces nunca termina ya que el predicado nunca evalúa verdadero. 
CC en algún momento se hace verdadero, específicamente para el menor valor que lo satisface ,ya que empezamos desde 0 y vamos aumentando en 1, por lo tanto $N1$ va a contener el menor t que satisface el predicado.