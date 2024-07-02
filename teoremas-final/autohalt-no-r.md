---
tags:
  - lfyc-c-IIX
  - "#review"
---
> **Lema 15** Supongamos $\Sigma\supseteq\Sigma_p$. Entonces ${AutoHalt}^\Sigma$ no es $\Sigma$-recursivo.

 - - - 
Lo probaremos por el absurdo. Supongamos que ($\ast$) ${AutoHalt}^\Sigma$ es $\Sigma$-recursivo, entonces existe un macro
$$
[IF\ {AutoHalt^{\Sigma}}(W1)\ GOTO\ A1]
$$
Sea $\mathcal{P}_0$ el siguiente programa 
$$
\begin{aligned}
L1\ & [IF\ {AutoHalt^{\Sigma}}(P1)\ GOTO\ L1]
\end{aligned}
$$
Notar que
- $\mathcal{P}_0$ termina partiendo desde $\parallel{\mathcal{P}_0}\parallel$ sii ${AutoHalt}^{\Sigma}(\mathcal{P}_0)=0$ 

lo cual contradice la suposición inicial ($\ast$).
