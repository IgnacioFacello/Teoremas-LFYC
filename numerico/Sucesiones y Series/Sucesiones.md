# Definición
>Conjuntos de la forma $(a_1,a_2,a_3... a_n),(a)_{n=1}^\infty,(a_n)$ compuestos por elementos "$a$" que siguen alguna regla

### Pueden ser:
- Crecientes ($a_n \leq a_{n+1}$)
- Estrictamente crecientes ($a_n < a_{n+1}$)
- Decrecientes ($a_n \geq a_{n+1}$)
- Estrictamente decrecientes ($a_n > a_{n+1}$)
Si solo es creciente o decreciente decimos que es __monótona__

### Cotas
Decimos que una sucesión $\{a_n\}$ es
1. Acotada inferiormente si $\exists M_i$ tq $M_i\geq a_n$ $\forall n\in\Bbb N$
2. Acotada superiormente si $\exists M_s$ tq $M_s\leq a_n$ $\forall n \in\Bbb N$
3. Acotada si $\exists M\in\Bbb R$ tq $|a_n|< M$ $\forall n\in\Bbb N$

**Observación**:
Se pueden definir cotas para todo conjunto de números reales y las cotas NO son únicas, por ejemplo para el caso de $\{(-1)^n\}$

##### Supremo e ínfimo
Sea $A\subset\Bbb R$, $A\neq\emptyset$
- Si $A$ es acotada sup, la menor cota superior se llama supremo de $A$ y se denota $sup(A)$
- Si $A$ es acotada inf, la mayor cota inferior se llama ínfimo de $A$ y se denota $inf(A)$

Además
- Si $sup(A)\in A$, decimos que es el *máximo* de $A$
- Si $inf(A)\in A$, decimos que es el *mínimo* de $A$


---
---
# Limite
Valor al que tienden los términos de la sucesión conforme se agregan elementos a esta.

Si este valor $l$ existe y no es $\infty$ decimos que la sucesión **converge** en $l$

$$\lim_{n\to \infty}a_n=l \quad  o \quad a_n \operatorname*{\rightarrow}_{n\to \infty} l$$

Si los términos de $(a_n)$ crecen indefinida decimos que la sucesión es **no convergente**
$$a_n \operatorname*{\rightarrow}_{n\to \infty} \infty$$

### Relación entre el límite de funciones y sucesiones
Si $\lim_{x\to \infty}f(x)=l$ y $a_n=f(n)$ $\forall x\geq n_0$, para algún $n_0\in\Bbb N$, entonces
$$\lim_{n\to \infty}a_n=l$$

>Si una sucesión y una función son iguales a partir de un cierto punto y $\lim_{x\to \infty}f(x)=l$, entonces $a_n$ converge en $n$

### Teorema del sandwich para sucesiones
Sea
- $a_n\leq b_n\leq c_n$ $\forall n\geq n_0$
- $\lim_{n\to \infty}a_n=\lim_{n\to \infty}c_n=l$

Entonces 
$$\lim_{n\to \infty}b_n=l$$

---
### Propiedades
Sean $\{a_n\}$ y $\{b_n\}$ convergentes y $c\in\Bbb R$

( i ) $\lim_{n\to \infty}(a_n \pm b_n)= \lim_{n\to \infty}(a_n) \pm \lim_{n\to \infty}(b_n)$

( ii )$\lim_{n\to \infty}(c * a_n)= c * \lim_{n\to \infty}(a_n)$

( iii ) $\lim_{n\to \infty}(a_n * b_n)= \lim_{n\to \infty}(a_n) * \lim_{n\to \infty}(b_n)$

( iv ) Si $\lim_{n\to \infty}(b_n) \neq 0 \Rightarrow \lim_{n\to \infty}(\frac{a_n}{b_n})=\frac{\lim_{n\to \infty}(a_n)}{\lim_{n\to \infty}(b_n)}$

---
---
# Subsucesiones
> Sucesiones contenidas dentro de otras

Ej: 
Sea $(n)$ la sucesión de números naturales, entonces $(2n)$ es la subsucesión de $(n)$ de números pares

### Definición
Una subsucesión $\{a\}$ es una sucesión de la forma $\{a_{n_1},a_{n_2},a_{n_3},\dots \}={a_{n_j}}^{\infty}_{j=1}$ donde los $n_j\in\Bbb N$ y cumplen $n_1<n_2<n_3<\dots$

## Teoremas
- #### 1 
Toda subsucesión de una sucesión convergente es convergente y ambas tienen el mismo límite.
- #### 2 - Bolzano-Weiertrass
Toda sucesión acotada tiene al menos una subsucesión convergente

---
---
# Teoremas
- ### 1
Sea $(a_n)$ tq $\lim_{n \to \infty}(a_n) = a$ y $f$ una función continua en dicho a.

$$\lim_{n\to \infty}f(a_n) = f(a) \qquad (= f(\lim_{n\to \infty}(a_n)))$$
- ### 2
Si $(a_n)$ es convergente $\Rightarrow$ es acotada. Pero si $(a_n)$ es acotada, no necesariamente converge
- ### 3
	- Si $(a_n)$ creciente y acotada sup $\Rightarrow (a_n)$ converge y $lim_{n\to \infty}(a_n) = sup(a_n)$  
	-  Si $(a_n)$ decreciente y acotada inf $\Rightarrow (a_n)$ converge y $lim_{n\to \infty}(a_n) = inf(a_n)$  
- ### 4
  Toda subsucesión de una sucesión convergente es convergente y además los límites son iguales