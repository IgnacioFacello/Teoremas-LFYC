---
tags:
  - flashcards
---
01. [[caracterización-conjunto-pr|Proposición 1]] Un conjunto S es $\Sigma$-pr sii es el dominio de alguna función $\Sigma$-pr. (Solo caso composición)
02. [[neumann-v-godel-c1|Teorema 2]] Si h es $\Sigma$-recursiva entonces es $\Sigma$-computable (Caso $h=R(f,\mathcal{G})$)
?
01. Predecesor de la caracteristica tiene dominio S. Prueba por Inducción. Caso 0 trivial. Caso inductivo composición requiere generalizar las funciones coordenada, dar característica para la intersección  de sus dominios y definir la función característica para el dominio de la composición.
02. Inducción. Tenemos macros para $f$, y $G_a$ para todo caractér $a$ del alfabeto. Comenzamos calculando f y luego hacemos recursion inversa sobre la palabra. Hacemos un if-tree tal que se ejecute la funcion G correcta segun el caractér de la palabra.
<!--SR:!2024-07-25,7,250-->