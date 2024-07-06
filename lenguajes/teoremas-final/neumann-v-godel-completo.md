---
tags:
  - "#lfyc-c-I"
  - lfyc-c-IIX
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
### Caso h=M(P) (combo 8)
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
### Caso h=R(f,G) (combo 1)
> Usando la hipótesis inductiva se obtienen las macros necesarias
> Luego realizar un programa que según el primer caractér de la variable de recursión realize la G apropiada  
> Para el caso alfabético y numérico cambiar la variable de resultado segun sea apropiado
#### (Alfabético)
Supongamos $h=R(f,\mathcal G)$ con
$$
\begin{align}
f &:S_1\times\dots\times S_{n}\times L_1\times\dots\times L_{m}\to\Sigma^*\\
\mathcal G &: S_1\times\dots\times S_{n}\times L_1\times\dots\times L_{m}\times \Sigma^*\times \Sigma^*\to\Sigma^*
\end{align}
$$
elementos de $R^\Sigma_k$. Sea $\Sigma=\{a_1,\dots,a_r\}$. Por (\*) hay macros que computan las funciones $f$ y $\mathcal G_a\quad a\in\Sigma$. 
Damos el siguiente programa que computa su recursion:
$$
\begin{align}
&[P\overline{m+3}\gets f(N1,\dots,N\overline{n},P1,\dots,P\overline{m})]\\
L\overline{r+1}\ & IF\ P\overline{m+1}\ BEGINS\ a_1\ GOTO\ L\bar 1\\
& \vdots \\
& IF\ P\overline{m+1}\ BEGINS\ a_r\ GOTO\ L\bar r\\
& GOTO\ L\overline{r+2} \\
L1\ & P\overline{m+1}\gets {}^\curvearrowright P\overline{m+1} \\
& [P\overline{m+3}\gets \mathcal G_1(N1,\dots,N\overline{n},P1,\dots,P\overline{m},P\overline{m+2},P\overline{m+3})]] \\
& P\overline{m+2}\gets P\overline{m+2}.a_1 \\
& GOTO\ L\overline{r+1} \\
&\vdots \\
Lr\ & P\overline{m+1}\gets {}^\curvearrowright P\overline{m+1} \\
& [P\overline{m+3}\gets \mathcal G_r(N1,\dots,N\overline{n},P1,\dots,P\overline{m},P\overline{m+2},P\overline{m+3})]] \\
& P\overline{m+2}\gets P\overline{m+2}.a_r \\
& GOTO\ L\overline{r+1} \\
L\overline{r+2}\ & P1\gets P\overline{m+3}
\end{align}
$$
#### (Numérico)
Muy similar al caso anterior, **solo requiere realizar un cambio de variables para el resultado**.
Supongamos $h=R(f,\mathcal G)$ con
$$
\begin{align}
f &:S_1\times\dots\times S_{n}\times L_1\times\dots\times L_{m}\to\omega\\
\mathcal G &: \omega\times S_1\times\dots\times S_{n}\times L_1\times\dots\times L_{m}\times \Sigma^*\to\omega
\end{align}
$$
elementos de $R^\Sigma_k$. 

---
Sea $\Sigma=\{a_1,\dots,a_r\}$. Por (\*) hay macros que computan las funciones $f$ y $\mathcal G_a\quad a\in\Sigma$. 
Damos el siguiente programa que computa su recursion:
$$
\begin{align}
&[N\overline{n+1}\gets f(N1,\dots,N\overline{n},P1,\dots,P\overline{m})]\\
L\overline{r+1}\ & IF\ P\overline{m+1}\ BEGINS\ a_1\ GOTO\ L\bar 1\\
& \vdots \\
& IF\ P\overline{m+1}\ BEGINS\ a_r\ GOTO\ L\bar r\\
& GOTO\ L\overline{r+2} \\
L1\ & P\overline{m+1}\gets {}^\curvearrowright P\overline{m+1} \\
& [P\overline{m+3}\gets \mathcal G_1(N\overline{n+1},N1,\dots,N\overline{n},P1,\dots,P\overline{m},P\overline{m+2})]] \\
& P\overline{m+2}\gets P\overline{m+2}.a_1 \\
& GOTO\ L\overline{r+1} \\
&\vdots \\
Lr\ & P\overline{m+1}\gets {}^\curvearrowright P\overline{m+1} \\
& [N\overline{n+1}\gets \mathcal G_r(N\overline{n+1},N1,\dots,N\overline{n},P1,\dots,P\overline{m},P\overline{m+2})]] \\
& P\overline{m+2}\gets P\overline{m+2}.a_r \\
& GOTO\ L\overline{r+1} \\
L\overline{r+2}\ & N1\gets N\overline{n+1}
\end{align}
$$
### Caso h=R(f,g) 
#### (Alfabético)
Supongamos $h=R(f,\mathcal g)$ con
$$
\begin{align}
f &:S_1\times\dots\times S_{n}\times L_1\times\dots\times L_{m}\to\Sigma^*\\
\mathcal g &: \omega\times S_1\times\dots\times S_{n}\times L_1\times\dots\times L_{m}\times \Sigma^*\to\Sigma^*
\end{align}
$$
$$
\begin{align}
&[P\overline{m+1}\gets f(N1,\dots,N\overline{n},P1,\dots,P\overline{m})]\\
L{3}\ & IF\ N\overline{n+1}\neq0\ GOTO\ L1\\
& GOTO\ L\overline{2} \\
L1\ & N\overline{n+1}\gets N\overline{n+1}-1 \\
& [P\overline{m+1}\gets \mathcal g(N\overline{n+1},N1,\dots,N\overline{n},P1,\dots,P\overline{m},P\overline{m+1})]] \\
& GOTO\ L\overline{3} \\
L2\ & P1\gets P\overline{m+1}
\end{align}
$$
#### (Numérico)
Supongamos $h=R(f,\mathcal g)$ con
$$
\begin{align}
f &:S_1\times\dots\times S_{n}\times L_1\times\dots\times L_{m}\to\omega\\
\mathcal g &: \omega\times\omega\times S_1\times\dots\times S_{n}\times L_1\times\dots\times L_{m}\to\omega
\end{align}
$$
$$
\begin{align}
&[N\overline{n+2}\gets f(N1,\dots,N\overline{n},P1,\dots,P\overline{m})]\\
L{3}\ & IF\ N\overline{n+1}\neq0\ GOTO\ L1\\
& GOTO\ L\overline{2} \\
L1\ & N\overline{n+1}\gets N\overline{n+1}-1 \\
& [N\overline{m+2}\gets \mathcal g(N\overline{n+1}, N\overline{n+2},N\overline{n+2},N1,\dots,N\overline{n},P1,\dots,P\overline{m})]] \\
& GOTO\ L\overline{3} \\
L2\ & N1\gets N\overline{n+2}
\end{align}
$$
### Caso Composición
Sea
- $h=f\circ[f_1,\dots.f_j,g_1,\dots,g_l]$ para $j,l\ge 0$ con
- $f_i:\omega^n\times\Sigma^{*m}\to\omega$ $i\in\{1,\dots,l\}$ y
- $g_i:\omega^n\times\Sigma^{*m}\to\Sigma^*$ $i\in\{1,\dots,l\}$. 

 Tenemos que $f, f_i, g_i\in R_k^\Sigma$ y por (\*) y por lo tanto tienen macros que las computan.
 Podemos dar el siguiente programa que claramente computa su composición:
$$
\begin{align}
& [N\overline{n+1}\gets f_1(N1,\dots,N\overline{n},P1,\dots,P\overline{m}) ] \\
& \qquad\vdots \\
& [N\overline{n+j}\gets f_j(N1,\dots,N\overline{n},P1,\dots,P\overline{m}) ] \\
& [P\overline{m+1}\gets g_1(N1,\dots,N\overline{n},P1,\dots,P\overline{m}) ] \\
& \qquad\vdots \\
& [P\overline{m+l}\gets g_l(N1,\dots,N\overline{n},P1,\dots,P\overline{m}) ] \\
& [N1\gets f(N\overline{n+1},\dots,N\overline{n+j},P\overline{m+1}\dots,P\overline{m+l})] \\
\end{align}
$$
