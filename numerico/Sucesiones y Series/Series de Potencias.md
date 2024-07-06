# Definición
Sean 
- $\{c_n\}^{\infty}_{n=0}$ una sucesión de números reales 
- $a\in\Bbb R$

Llamamos [[Series|serie]] de potencias centrada en $a$ a la serie de la forma
$$\sum_{n=0}^{\infty}c_n(x-a)^n = c_0+c_1(x-a)+c_2(x-a)^2+\ ...\ + c_n(x-a)^n$$

Estas series son generalizaciones de los polinomios y se utilizan para aproximar funciones o integrales.

---
---
# Radio de convergencia
Se llama Radio de Convergencia al valor $R$ que define el rango de valores de $x$ para los que la serie [[Sucesiones#Limite|converge]].

Sea R el radio de convergencia. Para toda serie de potencias se cumple *exactamente una* de las siguientes:
1. $R=0$ y la serie converge *solo* en $x=a$
2. $R=\infty$ y la serie es absolutamente convergente en $\forall\ x\in\mathbb R$
3. Existe un $R >0$ tal que la serie converge absolutamente $\forall\ x$ tq $|x-a|<R$ y es divergente $\forall x$ tq $|x-a|>R$

**Observación**:
Si la serie converge para algún $x_0\neq a$ entonces $r\geq |x_0-a|$ y si la serie diverge en $x_1$ entonces $R\leq |x_1-a|$. Esto nos sirve para aproximar el valor de $R$.

---
## Intervalo de convergencia
Llamamos intervalo de convergencia al conjunto $I=\{x\in\mathbb R\mid \sum^{\infty}_{n=0} c_n(x-a)^n\ converge\}$
- Si $R=0$, entonces $I=\{a\}$
- Si $R=\infty$, entonces $I=(-\infty,\infty)$
- Si $0<R<\infty$, entonces $I$ puede ser:
	> $\qquad (a-R,a+R)\qquad (a-R,a+R]\qquad [a-R,a+R)\qquad [a-R,a+R]$

---
## Criterio del cociente
Dada $\sum_{n=0}^{\infty}c_n(x-a)^n$ con $c_n\neq 0$ $\forall n \geq n_0$ y $R$ su radio de convergencia. Escribimos

$$L\ \dot =\lim_{n\rightarrow\infty}\frac{|C_{n+1}|}{|C_n|}$$

1. Si $0<L<\infty$, entonces $R=\frac1L$
2. Si $L=0$ entonces $R=\infty$
3. Si $L=\infty$ entonces $R=0$


>Podemos hacer sufrir a muchos matemáticos y decir que para todo $L$, $R=\frac1L$.

---
---
# Representación de funciones

Para cada $x$ tal que $\sum_{n=0}^{\infty}c_n(x-a)^n$ converge, la serie define una función $f(x)\ \dot =\sum_{n=0}^{\infty}c_n(x-a)^n$ cuyo dominio es el intervalo de convergencia.

## Funciones importantes
- $\frac{1}{1-x}=\sum_{n=0}^{\infty}x^n$

---
---
# Derivación e integración
Para la serie $\sum_{n=0}^{\infty}c_n(x-a)^n$ con $R>0$, la funcion $f\dot =\sum_{n=0}^{\infty}c_n(x-a)^n$ es derivable en el intervalo $(a-R,a+R)$.
1. $$f'(x)=\sum_{n=1}^{\infty}n*c_n(x-a)^{n-1}$$
2. $$\int f(x)\ dx=C+\sum_{n=1}^{\infty}\frac{c_n}{n+1}(x-a)^{n+1}$$

El radio de convergencia de 1 y 2 sigue siendo $R$.

$C$ se calcula evaluando 

---
---
# Series de Taylor
Si $f$ se puede representar como una serie de potencias centrada en $a$, es decir, si $f(x)\ =\sum_{n=0}^{\infty}c_n(x-a)^n$ $\forall x\in I$. 
Entonces:
$$c_n=\frac{f^{(n)}(a)}{n!}$$
Y la representación de $f$ centrada en $a$ es llamada la **serie de Taylor** centrada en $a$ :
$$f(x)\ =\sum_{n=0}^{\infty}\frac{f^{(n)}(a)}{n!}(x-a)^n + R_{n,a}(x)$$

Para poder representar a $f$ como serie de potencias es necesario que $f$ tenga derivadas de todos los ordenes en $a$.

**Observaciones**:
1. Para $a=0$ la serie $\sum_{n=0}^{\infty}\frac{f^{(n)}(0)}{n!}(x)^n$ se suele llamar *Serie de Maclaurin*

## Polinomio de Taylor
Sea $f$ tal que
- $f\in C^{(n)}[a,b]$
- existe $f^{(n+1)}(a,b)$

Para todo par $x,c\in [a,b]$ tenemos que la $n$-esima suma parcial de la serie de Taylor es el *Polinomio de Taylor* de $f$ en $a$.
$$T_{n,a}(x)=\sum_{i=0}^{n}\frac{f^{(i)}(a)}{i\ !}(x-a)^j$$

## Resto de Taylor
Como estamos tomando una suma parcial de la serie para armar el polinomio de Taylor, mientras más nos alejemos de $a$ mayor va a ser la diferencia entre el polinomio y la función original. Esta diferencia se llama el resto de Taylor de orden $n$ y se define como:
$$R_{n,a}(x)=f(x)-T_{n,a}(x)$$

Entonces está claro que 

$$f(x)=\sum_{n=0}^{\infty}\frac{f^{(n)}(0)}{n!}(x)^n \ \ \forall x\in (a-c,a-c) \iff \lim_{n\rightarrow\infty} R_{n,a} =0\ \ \forall x\in (a-c,a-c)$$

O lo que es lo mismo: La serie de Taylor para una función es igual a dicha función **solo si** el resto de la serie *tiende* a 0 conforme el grado aumenta.

### Fórmula de Lagrange para el resto
Sea
- $f$ tal que existen derivadas de orden $n+1$ en un intervalo abierto $I$
- $a\in I$

Entonces, para cada $x\in I$ existen $t$ entre $x$ y $a$ tq.

$$R_{n,a}(x)=\frac{f^{(n+1)}(t)}{(n+1)!}(x-a)^{(n+1)}$$

### Cálculo del error
Utilizando la fórmula de Lagrange obtenemos una fórmula que nos permite aproximar el error de un polinomio de Taylor

A partir de la fórmula $R_{n,a}(x)=\frac{f^{(n+1)}(t)}{(n+1)!}(x-a)^{(n+1)}$ podemos ver que dependiendo del intervalo al que pertenece $t$ se cumple una de las siguientes desigualdades
$$f^{(n+1)}(a) > f^{(n+1)}(t) > f^{(n+1)}(x)$$
$$f^{(n+1)}(x) > f^{(n+1)}(t) > f^{(n+1)}(a)$$

Luego $R_{n,a}(x) \geq f^{(n+1)}(x)$ o $R_{n,a}(x) \geq f^{(n+1)}(a)$