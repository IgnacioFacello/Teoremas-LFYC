# Modelos matemáticos
Descripciones de problemas "de la vida real". 
- Se generan estudiando las características de los problemas que representan

No son representaciones exactas de la realidad
- Los problemas más complejos se simplifican

Surgen dos maneras de simplificar
- Soluciones analíticas:
	- Muchas simplificaciones
	- Pueden diferir mucho de la realidad
- **Soluciones numéricas**
	- Aproximaciones numéricas del problema
	- Se pueden estudiar los errores que se producen y como afectan a la precisión de la solución

> **Problemas numéricos**:
> Claras y nada ambiguas descripciones de la conexión funcionar entre datos de entrada y salida. Estos datos consisten en un conjunto finito de cantidades reales

---
---
# Órdenes de convergencia
Sea $\{x_n\}$ una sucesión de números reales que converge a $x_*$
## Tasa lineal
La tasa de convergencia de $\{x_n\}$ es (al menos) **lineal** si 
- existe una constante $c$ tal que $0<c<1$ 
- y un $N\in\Bbb N$
tales que
$$|x_{n+1}-x_*|\leq c|x_n-x_*| \ \text{ para todo }\ n\geq N$$
## Tasa superlineal
La tasa de convergencia de $\{x_n\}$ es (al menos) **superlineal** si 
- existe una sucesión $\{\varepsilon_n\}$ que converge a 0
- y un $N\in\Bbb N$
tales que
$$|x_{n+1}-x_*|\leq \varepsilon_n|x_n-x_*| \ \text{ para todo }\ n\geq N$$

## Tasa cuadrática
La tasa de convergencia de $\{x_n\}$ es (al menos) **lineal** si 
- existe una constante positiva $c$  
- y un $N\in\Bbb N$
tales que
$$|x_{n+1}-x_*|\leq c|x_n-x_*|^2 \ \text{ para todo }\ n\geq N$$

---
---
# Notación $\mathcal O$ grande y $\mathcal o$ chica
Esta notación se usa para comparar la velocidad de convergencia de sucesiones y funciones
## Notación $\mathcal O$ grande
Sean $\{x_n\}$ $\{\alpha_n\}$ dos sucesiones distintas. Se dice que 
$$x_n=\mathcal O(\alpha_n)$$
si existe
- una constante $C>0$ 
- y $r\in\Bbb R$ 
tales que $|x_n|\leq C|\alpha_n|$ para todo $n\geq r$.

## Notación $\mathcal o$ chica
Se dice que
$$x_n=\mathcal o (\alpha_n)$$
si existe una sucesión $\{\varepsilon_n\}$ 
- que converge a 0, con $\varepsilon_n \geq 0$ 
- y un $r\in\Bbb N$ 
tales que $|x_n|\leq\varepsilon_n |\alpha_n|$ para todo $n\geq r$. Intuitivamente, esto dice que 
$$\lim_{n\to\infty}(\frac{x_n}{\alpha_n})=0$$

## Para funciones en infinito
$$f(x)=\mathcal O (g(x)) \ \text{cuando}\ x\to\infty$$
si existe $C>0$ y $r\in\Bbb R$ tal que $|x_n|\leq C|\alpha_n|$ para todo $x\geq r$.

Análogamente,
$$f(x)=\mathcal o (g(x)) \ \text{cuando}\ x\to\infty$$
si 
$$\lim_{n\to\infty}(\frac{f(x)}{g(x)})=0$$
## Para funciones en $x_0$
$$f(x)=\mathcal O (g(x)) \ \text{cuando}\ x\to x_0$$
si existe $C>0$ y $r\in\Bbb R$ tal que $|f(x)|\leq C|g(x)|$ para todo $x$ en el entorno de $x_0$.

Análogamente
$$f(x)=\mathcal o (g(x)) \ \text{cuando}\ x\to x_0$$
si 
$$\lim_{n\to x_0}(\frac{f(x)}{g(x)})=0$$