# Definición
> Son las sumatorias de $n=1$ a $\infty$ de los elementos de alguna [[Sucesiones|sucesión]].

Dada una sucesión de números reales llamaremos serie de términos $a_n$ a $$\sum^{\infty}_{n=1}a_n$$
y suma parcial $s_k$ de la serie $\sum^{\infty}_{n=1}a_n$ a la sumatoria hasta $k$
$$\sum^{k}_{n=1}a_n$$

Definimos convergencia para una serie como el valor al que tiende dicha serie y denotamos 
$$S =\sum_{n=0}^{\infty}(a_n) = l \qquad \Rightarrow \qquad S\ converge\ en\ l$$

o lo que es lo mismo
$$\lim_{k\to\infty}s_k=\lim_{k\to\infty} \sum^{k}_{n=1}a_n$$

si este límite no existe o es $\pm\infty$ decimos que la serie de $a_n$ es divergente

---
### Series alternantes
Son aquellas series cuyos términos son positivos y negativos alternadamente


---
## Propiedades
Si $\sum_{n=1}^{\infty}(a_n)$ y $\sum_{n=1}^{\infty}(b_n)$ son convergentes y $c\in \mathbb R$ $\Rightarrow$ $\sum_{n=1}^{\infty}(a_n \pm b_n)$ y $\sum_{n=1}^{\infty}(c*a_n)$ también convergen y:
- $\sum_{n=1}^{\infty}(a_n \pm b_n)$ = $\sum_{n=1}^{\infty}(a_n) \pm \sum_{n=1}^{\infty}(b_n)$
- $\sum_{n=1}^{\infty}(c*a_n) = c*\sum_{n=1}^{\infty}(a_n)$

## Criterios de divergencia

---
### Criterio de la divergencia
Si $\sum^{\infty}_{n=1}a_n$ converge, entonces $lim_{n\to\infty}a_n=0$. Equivalentemente, si $lim_{n\to\infty}a_n\neq 0$ o $\nexists\ lim_{n\to\infty}a_n$ la serie diverge.
>Si la sucesión no tiende a 0, la serie diverge

**Importante**
La recíproca no se cumple. Es decir que si el límite de la sucesión es 0 no podemos asegurar que la serie converja. Un ejemplo de esto es la [[Series#Series importantes|serie armonica]]

---
### Criterio de comparación
Si $0\leq a_n\leq b_n$, $\forall n\geq n_0$, entonces:
- Si $\sum^{\infty}_{n=n_0}b_n$ converge ==> $\sum^{\infty}_{n=n_0}a_n$ converge. 
- Equivalentemente, si $\sum^{\infty}_{n=n_0}a_n$ diverge ==> $\sum^{\infty}_{n=n_0}b_n$ diverge. 

---
### Criterio de comparación en el límite
Sean $\sum^{\infty}_{n=1}b_n$, $\sum^{\infty}_{n=1}a_n$ series de términos positivos. Entonces

$(\ I\ )$ Si $\lim_{n\to\infty}\frac{a_n}{b_n}\dot =c>0$ entonces $\sum^{\infty}_{n=n_0}a_n$ converge <==> $\sum^{\infty}_{n=n_0}b_n$ converge

$(\ II\ )$ Si $\lim_{n\to\infty}\frac{a_n}{b_n}=0$ entonces $\sum^{\infty}_{n=n_0}b_n$ converge ==> $\sum^{\infty}_{n=n_0}a_n$ converge
	- Equivalentemente, si $\sum^{\infty}_{n=n_0}a_n$ diverge ==> $\sum^{\infty}_{n=n_0}b_n$ diverge

$(\ III\ )$ Si $\lim_{n\to\infty}\frac{a_n}{b_n}=\infty$ entonces $\sum^{\infty}_{n=n_0}b_n$ diverge ==> $\sum^{\infty}_{n=n_0}a_n$ diverge
	- Equivalentemente, si $\sum^{\infty}_{n=n_0}a_n$ converge ==> $\sum^{\infty}_{n=n_0}b_n$ converge
	
---
### Criterio de la integral
Sea $f$ una función 
- continua
-  positiva
-  decreciente

en $[1,\infty )$. Si $a_n=f(n)$, entonces

$$\sum^{\infty}_{n=1}a_n\ \ converge\iff\int^{\infty}_1f(x)\ dx\ \ converge $$

**Observaciones**
1. No es cierto en general que $\sum^{\infty}_{n=1}a_n=\int^{\infty}_1f(x)\ dx$
2. No es necesario iniciar la serie o la integral en $n=1$

---
### Criterio para series alternantes
Sea
- $a_n\geq a_{n+1}> 0$ $\forall n$
- $\lim_{n\to\infty}a_n=0$

Entonces

$$\sum^{\infty}_{n=1}(-1)^na_n\ \ converge$$

---
### Criterio del cociente
Sean
- $a_n\neq 0$ $\forall n\geq n_0$
- $r=\lim_{n\to\infty}\vert\frac{a_{n+1}}{a_n}\vert$

$(\ I\ )$ Si $r<1$, entonces la serie $\sum^{\infty}_{n=1}a_n$ converge absolutamente

$(\ II\ )$ Si $r>1$, entonces la serie $\sum^{\infty}_{n=1}a_n$ diverge

$(\ III\ )$ Si $r=1$, entonces no se puede asegurar nada

---
### Criterio de la raíz
Sea
- $r\dot =\lim_{n\to\infty}\sqrt[n]{\vert a_n\vert }$

$(\ I\ )$ Si $r<1$, entonces la serie converge absolutamente

$(\ II\ )$ Si $r>1$, entonces la serie diverge

$(\ III\ )$ Si $r=1$, entonces no se puede asegurar nada

---
---
# Convergencia
Para una serie $\sum^{\infty}_{n=1}a_n$ decimos que
- Converge absolutamente. Si $\sum^{\infty}_{n=1}|a_n|$ converge.
- Converge condicionalmente. Si $\sum^{\infty}_{n=1}a_n$ converge pero $\sum^{\infty}_{n=1}|a_n|$ no.


---
---
### Series relevantes
- Serie geométrica 
	Dado $r\in\Bbb R$, la serie
$$\sum_{n=0}^{\infty}(r^n) = 1 + r + r^2 +\ ...$$
	Se llama serie geométrica. Además, converge solo si $|r| < 1$ y el valor al que converge es $\frac{1}{1-r}$ 
- Serie Armónica  
$$\sum_{n=1}^{\infty}(\frac{1}{n}) = 1 + \frac{1}{2} + \frac{1}{3} +\ ...$$
	- Esta serie diverge 
- Serie p  $\sum_{n=1}^{\infty}(\frac{1}{n^p}) = \frac{1}{1^p} + \frac{1}{2^p} +\ ...$
	- Converge si y solo si $p>1$
