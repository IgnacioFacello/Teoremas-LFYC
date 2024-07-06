# Definicion
Dadas $f_i\ :\mathbb R \rightarrow\mathbb R$, $i = 1,\dots ,n$, llamamos funcion [[Vectores|vectorial]] a la funcion $f\ :\mathbb R \rightarrow\mathbb R^n$ dada por 

$$f(t)=(f_1(t),f_2(t),\dots ,f_n(t))$$

Los $f_i$ se llaman funcion cordenados de $f$.

---
### Dominio
El dominio de $f$ es 

$$Dom(f)=\bigcap_{i=1}^{n}Dom(f_i)$$  

(La interseccion de los dominios)

---
### Imagen
La imagen de la función vectorial $f(t)\Bbb R\to\Bbb R^n$ es el conjunto de $\mathbb R^n$ definido por

$$Im(f)=\{(y_1\dots y_n)\in \mathbb R^n\mid \exists t\in Dom(f)\quad tq\quad f(t)=(y_1\dots y_n)\}$$

- Se llama curva en el plano/espacio a la imagen de $f(t)$ en $\mathbb R^2$/$\mathbb R^3$

---
### Limite 

$$\lim_{t\rightarrow c} f(t)=(\lim_{t\rightarrow c}f_1(t),\lim_{t\rightarrow c}f_2(t),\dots ,\lim_{t\rightarrow c}f_n(t))$$
siempre que los limites $\lim_{t\rightarrow c}f_i(t)$ $\forall i \in [1;n]$

$f(t)$ es continua si todas sus funciones coordenadas son continuas

---
---
### Derivacion
Siempre que todas las funciones coordenadas de $f(t)$ sean derivables en $a$. La derivada de $f$ en $a$ es:

$$f'(a)=\lim_{h\rightarrow 0}\frac{f(a+h)-f(a)}{h}$$
tambien es cierto que podemos derivar por cordenada

$$f(t)=(f'_1(t),f'_2(t),\dots ,f'_n(t))$$


#### Reglas
Sean $f(t)$ y $g(t)$ funciones vectoriales y $\phi (t)$ una funcion convencional
1) $$(f(t)\pm g(t))'=f'(t) \pm g'(t)$$
2) $$(k*f(t))'=k*f'(t)$$
3) $$(\phi (t) * f(t) )'= \phi' (t) * f(t)+\phi (t) * f'(t)$$
4) $$\langle f(t), g(t)\rangle'=\langle f'(t), g(t)\rangle + \langle f(t), g'(t)\rangle$$
5) $$(f(\phi (t)))' = f'(\phi (t)) * \phi' (t)$$

---
#### Interpretación
![[Pasted image 20211020101322.png]]
La derivada de una funcion vectorial $f$ en un punto $a$ se puede interpretar como el vector que representa la direccion(direccion del vector) y velocidad(tamaño del vector) de $f$ en a
- $f(t)$ es la posicion en el tiempo t.
- $f(a+h)-f(a)$ es el vector que va desde el punto $f(a)$ al punto $f(a-h)$.
- $\frac{f(a+h)-f(a)}{h}$ es un vector paralelo al anterior.
- Conforme $h\rightarrow 0$, $\frac{f(a+h)-f(a)}{h}$ se aproxima al vector tangente a la curva de $f()$ en $a$.
- 


---