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
### Caso h=R(f,G) (combo 1)
> Usando la hipótesis inductiva se obtienen las macros necesarias
> Luego realizar un programa que según el primer caractér de la variable de recursión realize la G apropiada  
> Para el caso alfabético y numérico cambiar la variable de resultado segun sea apropiado

<div style="page-break-after: always;"></div>

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

<div style="page-break-after: always;"></div>

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
