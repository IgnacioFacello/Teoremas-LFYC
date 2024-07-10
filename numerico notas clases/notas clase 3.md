# Clase 3
Un efecto no deseable en los algoritmos numéricos es la cancelación de dígitos significativos

> #definicion 1 Base de un numero 
> Sea $\beta\in\mathbb{N}$, $\beta\ge 2$, todo numero real $r$ puede ser escrito en la forma:$$(\pm d_n d_{n-1} \dots d_0 d_{-1}\dots)_{\beta}$$ donde $d_n,d_{n-1},\dots,d_0,d_{-1}\dots$ son números naturales entre 0 y $\beta-1$. El valor del número $r$ es: $$\pm d_n\beta^n+d_{n-1}\beta^{n-1}+\dots+d_0\beta^0+d_{-1}\beta^{-1}\dots$$

Las computadoras representan números en binario ya sea en punto fijo o flotante