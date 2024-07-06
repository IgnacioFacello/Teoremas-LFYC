# Definición
La integración es la operación "Inversa" a la [[Derivada|derivación]]. 
Es decir: Sea
- $I\subset\Bbb R$
- $f:I\to\Bbb R$
- $F:I\to\Bbb R$

$F$ es una antiderivada o primitiva de $f$ en $I$ si
$$f(x)=F'(x)$$

> Cabe destacar que las primitivas no son únicas, si $F$ es la primitiva de $f$ entonces $F(x)+c$, para cualquier $c\in\Bbb R$.

----
----
# Integral indefinida

Dados
- $I\subset\Bbb R$
- $f:I\to\Bbb R$

Llamamos integral indefinida de $f$ al conjunto de todas las primitivas de $f$ y denotamos
$$\int f(x)\ dx$$

**Observaciones**
1) El símbolo $\int$ se llama integral y $dx$ se llama diferencial (de x)
	- Además denotamos por diferencial de una función $F$ a $d(F(x))=F'(x)\ dx$

## Propiedades
1) $\int 0\ dx=c$
2) $\int a*f(x)\ dx=a*\int f(x)\ dx$, $\forall a\in\Bbb R$
3) $\int (f\pm g)(x)\ dx = \int f(x)\ dx \pm \int g(x)\ dx$

# Integral definida
Sea $f:[a,b]\to\Bbb R$ una función continua y tal que $f(x)\geq 0$. Queremos saber cuál es el área definida por la curva de $f$, el eje de las $x$ y las rectas $x=a$ y $x=b$. Para esto utilizamos la integral definida de f:
$$\int^{b}_{a} f(x)\ dx$$

**Observaciones**
1) Para el caso $a=b$ se define $\int^{a}_{z} f(x)\ dx=0$
2) La integral definida se puede extender a funciones que tomen valores positivos y negativos, escribiendo f$(x)=f^{+}(x)-f^{-}(x)$ con $f^{+}(x)=max(f(x),0)\geq 0$ y $f^{-}(x)=max(-f(x),0)\geq 0$ y haciendo 
$$\int^{b}_{a} f(x)\ dx=\int^{b}_{a} f^{+}(x)\ dx-\int^{b}_{a} f^{-}(x)\ dx$$
3) También se puede extender la definición a funciones continuas en $[a,b]$ salvo un número finito de discontinuidades y siempre que $f$ esté [[acotada]] en $[a,b]$

## Propiedades
1) Si $f\geq 0$ en $[a,b]$ ==> $\int^b_af(x)\ dx \geq 0$ 
2) $\int^b_ac*f(x)\ dx =c*\int^b_af(x)\ dx$ $\forall c\in\Bbb R$
3) $\int^b_a(f\pm g)(x)\ dx = \int^b_af(x)\ dx \pm \int^b_ag(x)\ dx$ 
4) Si $d\in [a,b]$, $\int^b_af(x)\ dx=\int^b_df(x)\ dx+\int^d_af(x)\ dx$
5) Si $f\leq g$ en $[a,b]$ entonces $\int^b_af(x)\ dx\leq \int^b_ag(x)\ dx$

----
----
# Cálculo de integrales

## Método de sustitución
Sean:
- $f:(d,e)\to\Bbb R$
- $g:(a,b)\to(d,e)$

Derivables en su dominio. Entonces
%% Entonces, si $F$ es una primitiva de $f$ en $(d,e)$, $H(x)=(Fog)(x)$ es primitiva de $h(x)=f(g(x))*g'(x)$ en $(a,b)$. O sea, %%

$$\int f(g(x))*g'(x)=F(g(x))+c$$
Con $F(x)$ cualquier primitiva de $f$, $c\in\Bbb R$ y $\forall x\in (a,b)$

## Método de integración por partes
Sean
- $f'$ y $g'$ funciones continuas 

$$\int f(x)*g'(x)\ dx=f(x)*g(x)-\int f'(x)*g(x)\ dx$$

> Mnemotécnica:
> $u=f(x)$ y $du=f'(x) dx$
> $v=g(x)$ y $dv=g'(x) dx$
> $$\int u\ dv=u*v-\int v*du$$

----

## Método de substitución para definidas
Sean:
- $f:(d,e)\to\Bbb R$
- $g:(a,b)\to(d,e)$

Derivables en su dominio. Entonces si $u=g(x)$ vale que

$$\int^b_a f(g(x))*g'(x)=\int^{g(b)}_{g(a)} f(u)\ du$$

## Integración por partes para definidas
Sean $f'$ y $g'$ 
- Continuas en $(a,b)$ 
- Con un número finito de discontinuidades en $[a,b]$
- Acotadas

$$\int^b_a f(x)*g'(x)\ dx=(f(x)*g(x))|^b_a-\int^b_a f'(x)*g(x)\ dx$$

> Mnemotécnica:
> $u=f(x)$ y $du=f'(x) dx$
> $v=g(x)$ y $dv=g'(x) dx$
> $$\int^b_a u\ dv=u*v|^b_a-\int^b_a v*du$$

---
## Integración usando fracciones simples
Para integrar funciones que son cocientes de polinomios, es decir $\int\frac{P(x)}{Q(x)}$.
Se debe cumplir que:
- $gr(p) < gr(q)$
- El coeficiente del término de $q$ con la mayor potencia es 1

### Caso 1
$q$ es producto de polinomios de grado 1 y son todos distintos. O sea,
$$q(x)=(x-r_1)\dots (x-r_k),\ con\ r_j\neq r_i\ si\ j\neq i$$

Debemos buscar constantes $A_1,\dots, A_k$ (una por cada término) tales que:
$$\frac{p(x)}{q(x)}=\frac{A_1}{x-r_1}+\dots +\frac{A_k}{x-r_k}$$

Luego cada término $\frac{A_i}{x-r_i}$ es fácil de integrar

### Caso 2
$q$ es producto de polinomios de grado 1 todos iguales. O sea $q(x)=(x-r)^k$. En este caso debemos buscar constantes $A_1,\dots, A_k$ tales que
$$\frac{p(x)}{q(x)}=\frac{A_1}{x-r}+\frac{A_2}{(x-r)^2}+\dots +\frac{A_k}{(x-r)^k}$$

### Caso 3
$q$ es producto de polinomios de grado 1, algunos de los cuales se repiten.O sea
$$q(x)=(x-r_1)\dots (x-r_{i-1})(x-r_i)^{K_i}\dots (x-r_n)^{K_n}$$

En este caso aplicamos los procedimientos de los casos [[Integrales#Caso 1|1]] y [[Integrales#Caso 2|2]]

### Caso 4
$q$ es producto de factores $(x-r_i)^{K_i}$ y/o polinomios de grado 2 sin raíces reales y que no se repiten.
$$q(x)=(x-r_1)^{K_1}\dots (x-r_n)^{K_n}(x^2+\alpha_1+\beta_1)\dots (x^2+\alpha_m+\beta_m)$$

En este caso $\frac pq$ se escribe como una suma donde por cada "factor lineal" aparecen tantos términos como indican los casos 1 y 2, y para cada "factor cuadrático" aparecen términos de la forma $\frac{Bx+C}{x^2+\alpha+\beta}$, con B y C constantes a encontrar.

**Observación**:
Para integrar términos de la forma $\frac{Bx+C}{x^2+\alpha+\beta}$ debemos hallar constantes $K_1$ y $K_2$ tales que
$$\frac{Bx+C}{x^2+\alpha+\beta}=K_1\frac{2x+\alpha}{x^2+\alpha+\beta}+K_2\frac{1}{x^2+\alpha+\beta}$$
Luego $K_1\frac{2x+\alpha}{x^2+\alpha+\beta}$ es fácil de integrar usando la sustitución $u =x^2+\alpha+\beta$

Y para integrar $\frac{1}{x^2+\alpha+\beta}$ debemos sustituir de modo que obtengamos algo de la forma 
$$\int\frac{1}{y^2+a^2}\ dy=\frac1a\ arctg(\frac ya)+c$$

---
---
# Integrales impropias
### Tipo 1
Funciones continuas con al menos un límite de integración no finito
Sea $a\in\Bbb R$
- Si $f$ es continua en $[a,\infty)$, definimos 
$$\int^{\infty}_af(x)\ dx=\lim_{t\to\infty}\int^{t}_af(x)\ dx$$
Si este límite existe y es finito. En tal caso decimos que $\int^{\infty}_af(x)\ dx$ converge, si no decimos que diverge.
- Si $f$ es continua en $(-\infty ,a]$, definimos 
$$\int^{a}_{-\infty}f(x)\ dx=\lim_{t\to-\infty}\int^{a}_tf(x)\ dx$$
- Si $f$ es continua en $\Bbb R$, definimos 
$$\int^{\infty}_{-\infty}f(x)\ dx=\int^{\infty}_{a}f(x)\ dx+\int^{a}_{-\infty}f(x)\ dx$$
Siempre que ambas integrales converjan. Esta definición vale para cualquier valor de $a$.

### Tipo 2
Funciones con límites de integración finitos pero con alguna asíntota en el intervalo.

- Sea $f$ continua en $[a,b)$ y $\lim_{x\to b^-}f(x)=\pm\infty$. Definimos
$$\int^b_af(x)\ dx=\lim_{t\to b^-}\int^t_af(x)\ dx$$ si este límite existe y es finito
- Sea $f$ continua en $(a,b]$ y $\lim_{x\to a^+}f(x)=\pm\infty$. Definimos
$$\int^b_af(x)\ dx=\lim_{t\to a^+}\int^b_tf(x)\ dx$$ si este límite existe y es finito
- Sea $c\in (a,b)$. Si $f$ es continua en $[a,c)\cup (c,b]$ y las integrales $\int^{c}_{a}f(x)\ dx$ y $\int^{b}_{c}f(x)\ dx$ existen y son finitas, definimos $$\int^{b}_{a}f(x)\ dx=\int^{c}_{a}f(x)\ dx+\int^{b}_{c}f(x)\ dx$$


## Criterio de comparación
Para las integrales difíciles de calcular podemos ver si la impropia converge o diverge utilizando la definición.

### Tipo 1
- Si $|f(x)\leq g(x)|\ \forall x\in[a,\infty )$ . Entonces 
$$\int^{\infty}_ag(x)\ dx\ \ converge \implies \int^{\infty}_af(x)\ dx\ \ converge$$
o equivalentemente
$$\int^{\infty}_af(x)\ dx\ \ diverge \implies \int^{\infty}_ag(x)\ dx\ \ diverge$$

- Si $|f(x)\leq g(x)|\ \forall x\in(\infty,a]$ . Entonces 
$$\int^a_{-\infty}g(x)\ dx\ \ converge \implies \int^a_{-\infty}f(x)\ dx\ \ converge$$
o equivalentemente
$$\int^a_{-\infty}f(x)\ dx\ \ diverge \implies \int^a_{-\infty}g(x)\ dx\ \ diverge$$

### Tipo 2
Sean $f$,$g$ funciones continuas en $[a,b)$ y tq $|f(x)|\leq g(x)\ \forall x\in [a,b)$ y $lim_{x\to b^-}f(x)=\pm\infty$. Entonces 
$$\int^b_{a}g(x)\ dx\ \ converge \implies \int^b_{a}f(x)\ dx\ \ converge$$
o equivalentemente
$$\int^b_{a}f(x)\ dx\ \ diverge \implies \int^b_{a}g(x)\ dx\ \ diverge$$


---
---
# Área entre dos curvas
Sea $f$ y $g$ 
- Funciones acotadas
- Con un número finito de discontinuidades
- $f(x)\geq g(x)$ $\forall x\in [a,b]$

Entonces, el área entre las gráficas de $f$ y $g$ y las rectas $x=a$ y $x=b$ es

$$A=\int^b_a(f(x)-g(x))\ dx$$


----
----
# Teoremas
## 1
Sea
- $f,g:[a,b]\to\Bbb R$
- Con $f$ continua
- $g$ tq $g(x)=f(x)$ $\forall x\in [a,b]$. Salvo algun $c\in[a,b]$

Entonces
$$\int^b_af(x)\ dx=\int^b_ag(x)\ dx$$

## 

---
---
# Teorema fundamental del cálculo
Sea:
- $f:[a,b]\to\Bbb R$ continua
- $F(x)=\int^x_af(t)\ dt$, $\forall x\in[a,b]$

Entonces
1) $F$ es derivable y $F'(x)=f(x)$ $\forall x\in (a,b)$. $F$ es primitiva de $f$
2) Si $G$ es una primitiva de $f$ en $[a,b]$, entonces $F\int^b_af(t)\ dt=G(b)-G(a)=G(x)|^b_a$ (Regla de Barrow)

