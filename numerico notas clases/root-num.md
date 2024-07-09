# Clase 1
definiciones básicas y problemas que vamos a ver
repaso de conceptos matemáticos

Problemas requieren Modelos matematicos para ser resueltos
El diseño de estos se inspira en las caracteristicas de los Problemas
Requieren simplificaciones los cuales introducen inexactitudes
Hay distintos tipos, vamos a ver las numericas, para las cuales podemos medir su impacto

> #teorema 1 **(Valor intermedio para funciones continuas)**
> Sea $f$ continua en $[a,b]$ un intervalo cerrado. Sea $d$ un valor entre $f(a)$ y $f(b)$ entonces existe  $c\in[a,b]$ tal que $f(c)=d$ 

> #teorema 2 **(Valor medio)**
> Sea $f$ continua en $[a,b]$ y derivable en $(a,b)$. Entonces para todo par $x,c\in[a,b]$ se cumple que $${f(x) - f(c)\over x-c}=f'(\varepsilon)\quad$$ con $\varepsilon$ entre $x$ y $c$. 
> Esto nos dice que $f(x)=f(c)+f'(\varepsilon)*(x-c)$ 

> #teorema 3 **(Taylor)** 
> Si $f\in C^{(n)}[a,b]$ y existe $f^{(n+1)}(a,b)$ entonces para todo par $x,c\in[a,b]$ se tiene que $$f(x)=\sum^{n}_{k=0}\frac1{k!}f^{(k)}(c)*(x-c)^k+E_n(x)$$ donde $$E_n(x)=\frac{1}{(n+1)!}f^{(n+1)}(\varepsilon)(x-c)^{n+1}$$ para algún $\varepsilon$ entre $x$ y $c$. 

> #teorema 4 **(Taylor con resto integral)**
> Si $f\in C^{(n)}[a,b]$ y existe $f^{(n+1)}(a,b)$ entonces para todo par $x,c\in[a,b]$ se tiene que $$f(x)=\sum^{n}_{k=0}\frac1{k!}f^{(k)}(c)*(x-c)^k+R_n(x)$$ donde $$R_n(x)=\frac{1}{n!}\int^{x}_{c}f^{(n+1)}(t)(x-t)^{n}\ dt$$ para algún $\varepsilon$ entre $x$ y $c$. 

