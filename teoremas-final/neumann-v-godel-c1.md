---
tags:
  - "#lfyc-c-I"
---
> **Teorema 2** Si h es $\Sigma$*-[[paradigma-godel|recursiva]]* entonces es $\Sigma$*-[[paradigma-neumann|computable]]*
?

---
Probaremos por inducción en k que

(\*)Si $h\in\mathrm{R}_{k}^{\Sigma}$, entonces $h$ es $\Sigma$-computable.

Sea $k=0$ y $h\in R_{k}^{\Sigma}$, notar que
$$
\begin{aligned}
Succ&=\Psi_{N1\gets N1+1}^{1,0,\#} \\
Pred&=\Psi_{N1\gets N1\dot{-}1}^{1,0,\#} \\
C_{0}^{0,0}&=\Psi_{N1\gets0}^{0,0,\#} \\
C_{\varepsilon}^{0,0}&=\Psi_{P1\gets\varepsilon}^{0,0,*} \\
d_{a}&=\Psi_{P1\gets P1.a}^{0,1,*}\text{ para todo }a\in\Sigma \\
p_{j}^{n,m}&=\Psi_{N1\gets N\overline{j}}^{n,m,\#}\text{ si }j\in\left\{ 1,\dots,n\right\} \\
p_{j}^{n,m}&=\Psi_{P1\gets P\overline{j-n}}^{n,m,*}\text{ si }j\in\left\{ n+1,\dots,n+m\right\}
\end{aligned}
$$

---
Supongamos (\*) vale para $k$, veremos que vale para $k+1$. Sea $h\in R_{k+1}^{\Sigma}-R_{k}^{\Sigma}$. Hay varios casos, pero solo vamos a probarlo para $h=R(f,\mathcal{G})$, con 
$$
\begin{aligned}
f&:S_{1}\times...\times S_{n}\times L_{1}\times...\times L_{m}\rightarrow\Sigma^{\ast} \\
\mathcal{G}_{a}	&:S_{1}\times...\times S_{n}\times L_{1}\times...\times L_{m}\times\Sigma^{\ast}\times\Sigma^{\ast}\rightarrow\Sigma^{\ast}\text{, }a\in\Sigma 
\end{aligned}
$$
elementos de $\mathrm{R}_{k}^{\Sigma}. Sea \Sigma=\{a_{1},...,a_{r}\}$. Por hipótesis inductiva, las funciones $f, \mathcal{G}_{a}, a\in\Sigma$ , son $\Sigma$-computables y por lo tanto podemos hacer el siguiente programa via el uso de macros
$$
\begin{array}{rl}
 & \left[\mathrm{P}\overline{m+3}\leftarrow f(\mathrm{N}1,...,\mathrm{N}\bar{n},\mathrm{P}1,...,\mathrm{P}\bar{m})\right]\\
\mathrm{L}\overline{r+1} & \mathrm{IF}\;\mathrm{P}\overline{m+1}\ \mathrm{BEGINS\ }a_{1}\text{ }\mathrm{GOTO}\;\mathrm{L}1\\
 & \ \ \ \ \ \ \ \ \ \ \ \ \vdots\\
 & \mathrm{IF}\;\mathrm{P}\overline{m+1}\ \mathrm{BEGINS\ }a_{r}\text{ }\mathrm{GOTO}\;\mathrm{L}\bar{r}\\
 & \mathrm{GOTO}\;\mathrm{L}\overline{r+2}\\
\mathrm{L}1 & \mathrm{P}\overline{m+1}\leftarrow\text{ }^{\curvearrowright}\mathrm{P}\overline{m+1}\\
 & \left[\mathrm{P}\overline{m+3}\leftarrow\mathcal{G}_{a_{1}}(\mathrm{N}1,...,\mathrm{N}\bar{n},\mathrm{P}1,...,\mathrm{P}\bar{m},\mathrm{P}\overline{m+2},\mathrm{P}\overline{m+3})\right]\\
 & \mathrm{P}\overline{m+2}\leftarrow\mathrm{P}\overline{m+2}.a_{1}\\
 & \mathrm{GOTO}\;\mathrm{L}\overline{r+1}\\
 & \ \ \ \ \ \ \ \ \ \ \ \ \vdots\\
\mathrm{L}\bar{r} & \mathrm{P}\overline{m+1}\leftarrow\text{ }^{\curvearrowright}\mathrm{P}\overline{m+1}\\
 & \left[\mathrm{P}\overline{m+3}\leftarrow\mathcal{G}_{a_{r}}(\mathrm{N}1,...,\mathrm{N}\bar{n},\mathrm{P}1,...,\mathrm{P}\bar{m},\mathrm{P}\overline{m+2},\mathrm{P}\overline{m+3})\right]\\
 & \mathrm{P}\overline{m+2}\leftarrow\mathrm{P}\overline{m+2}.a_{r}\\
 & \mathrm{GOTO}\;\mathrm{L}\overline{r+1}\\
\mathrm{L}\overline{r+2} & \mathrm{P}1\leftarrow\mathrm{P}\overline{m+3}
\end{array}
$$
Es fácil chequear que este programa computa h.

---
Ahora sea $h'\in R_{k+1}^{\Sigma}-R_{k}^{\Sigma}$. Supongamos $h'=R(f',\mathcal{G}')$ con
$$
\begin{aligned}
f'&:	S_{1}\times\dots\times S_{n}\times L_{1}\times\dots\times L_{m}\to\omega \\
\mathcal{G}'_{a}&:	\omega\times S_{1}\times\dots\times S_{n}\times L_{1}\times\dots\times L_{m}\times\Sigma^{*}\to\omega,a\in\Sigma 
\end{aligned}
$$
funciones de $R_{k}^{\Sigma}$ y sea $\Sigma=\{a_{1},\dots,a_{r}\}$. Nuevamente, por hipótesis inductiva las funciones $f',\mathcal{G}'_{a}, a\in\Sigma$  son $\Sigma$-computables y podemos hacer el siguiente programa via el uso de macros
$$
\begin{array}{rl}
 & \left[\mathrm{N}\overline{n+1}\leftarrow f(\mathrm{N}1,...,\mathrm{N}\bar{n},\mathrm{P}1,...,\mathrm{P}\bar{m})\right]\\
\mathrm{L}\overline{r+1} & \mathrm{IF}\;\mathrm{P}\overline{m+1}\ \mathrm{BEGINS\ }a_{1}\text{ }\mathrm{GOTO}\;\mathrm{L}1\\
 & \ \ \ \ \ \ \ \ \ \ \ \ \vdots\\
 & \mathrm{IF}\;\mathrm{P}\overline{m+1}\ \mathrm{BEGINS\ }a_{r}\text{ }\mathrm{GOTO}\;\mathrm{L}\bar{r}\\
 & \mathrm{GOTO}\;\mathrm{L}\overline{r+2}\\
\mathrm{L}1 & \mathrm{P}\overline{m+1}\leftarrow\text{ }^{\curvearrowright}\mathrm{P}\overline{m+1}\\
 & \left[N\overline{n+1}\leftarrow\mathcal{G}_{a_{1}}(N\overline{n+1},\mathrm{N}1,...,\mathrm{N}\bar{n},\mathrm{P}1,...,\mathrm{P}\bar{m},\mathrm{P}\overline{m+2})\right]\\
 & \mathrm{P}\overline{m+2}\leftarrow\mathrm{P}\overline{m+2}.a_{1}\\
 & \mathrm{GOTO}\;\mathrm{L}\overline{r+1}\\
 & \ \ \ \ \ \ \ \ \ \ \ \ \vdots\\
\mathrm{L}\bar{r} & \mathrm{P}\overline{m+1}\leftarrow\text{ }^{\curvearrowright}\mathrm{P}\overline{m+1}\\
 & \left[N\overline{n+1}\leftarrow\mathcal{G}_{a_{r}}(N\overline{n+1},\mathrm{N}1,...,\mathrm{N}\bar{n},\mathrm{P}1,...,\mathrm{P}\bar{m},\mathrm{P}\overline{m+2})\right]\\
 & \mathrm{P}\overline{m+2}\leftarrow\mathrm{P}\overline{m+2}.a_{r}\\
 & \mathrm{GOTO}\;\mathrm{L}\overline{r+1}\\
\mathrm{L}\overline{r+2} & \mathrm{N}1\leftarrow N\overline{n+1}
\end{array}
$$
Es facil ver que este programa computa a h'.