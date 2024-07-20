---
tags:
  - flashcards
---
15. [[autohalt-no-r|Lema 15]] Supongamos $\Sigma\supseteq\Sigma_p$. Entonces ${AutoHalt}^\Sigma$ no es $\Sigma$-recursivo.
16. [[autohalt-no-ec|Teorema 16]] Supongamos $\Sigma\supseteq\Sigma_p$. Entonces ${AutoHalt}^\Sigma$ no es $\Sigma$-e.c.
17. [[autohalt-A-y-N|Lema 17]] Supongamos que $\Sigma\supseteq\Sigma_p$. Entonces $$A=\{\mathcal{P}\in{Pro}^{\Sigma}:{AutoHalt}^{\Sigma}(\mathcal{P})=1\}$$ es $\Sigma$-recursivamente enumerable y no es $\Sigma$-recursivo. Mas aun, el conjunto $$N=\{\mathcal{P}\in{Pro}^{\Sigma}:{AutoHalt}^{\Sigma}(\mathcal{P})=0\}$$ no es $\Sigma$-recursivamente enumerable.
18. [[neumann-v-godel-c8|Teorema 18]] (Neuman vence a Godel)  Si $h=M(P)$ es $\Sigma$-recursiva entonces es $\Sigma$-computable
?
15. Absurdo. Programa que solo termina si no termina.
16. Tesis de church.
17. Iteración en $\omega^2$, generando programa y nro de pasos, devolver solo si termina en ese numero de pasos. Luego suponemos $N$ r.e., lo usamos para definir autohalt recursivo, lo cual contradice el lema 15. Luego no es r.e. y por lo tanto A tampoco es recursivo.
18. Iteración en $\omega$
<!--SR:!2024-07-27,7,250-->