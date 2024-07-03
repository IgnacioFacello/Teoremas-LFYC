---
tags:
  - lfyc-c-IIX
---
> **Lema 15** Supongamos $\Sigma\supseteq\Sigma_p$. Entonces ${AutoHalt}^\Sigma$ no es $\Sigma$-recursivo.
?
 
---
Lo probaremos por el absurdo. Supongamos que ($\ast$) ${AutoHalt}^\Sigma$ es $\Sigma$-recursivo por el *lema de las macros* entonces existe el macro
$$
[IF\ {AutoHalt^{\Sigma}}(W1)\ GOTO\ A1]
$$
 - - -
Sea $\mathcal{P}_0$ el siguiente programa 
$$
\begin{aligned}
L1\ & [IF\ {AutoHalt^{\Sigma}}(P1)\ GOTO\ L1]
\end{aligned}
$$
Notar que
- $\mathcal{P}_0$ termina partiendo desde $\parallel{\mathcal{P}_0}\parallel$ sii ${AutoHalt}^{\Sigma}(\mathcal{P}_0)=0$ 

Es decir, el programa termina partiendo de si mismo si y solo si no termina partiendo de si mismo, lo cual es un absurdo.
