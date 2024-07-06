# Definición
Funciones $f$ de $n$ variables es una regla $f : \mathbb R^n \rightarrow \mathbb R$ que asigna a cada $n$-tupla $\bar x=(x_1,\dots ,x_n)$ un **único** número real $f(\bar x)=f(x_1,\dots ,x_n)$
	
---
## Dominio
$Dom(f)$ es el subconjunto de $\mathbb R^n$ tal que:
$$Dom(f)=\{\forall\bar x \in \mathbb R^n \mid f(\bar x)\quad está\quad bien\quad definida\}$$

---
## Rango
$Im(f)$ es el subconjunto de $\mathbb R$ tal que:
$$Im(f)=\{\forall y\in \mathbb R \mid \exists\bar x \in Dom(f)\quad con\quad f(\bar x) = y\}$$

Es importante primero racionalizar la definición de $f$ para poder definir el rango. 

---
## Grafica
El gráfico de $f(\bar x)$ es el subconjunto de $R^{n+1}$ dado por:
$$G(f)=\{(\bar x, f(\bar x)) \in \mathbb R^{n+1} \mid \bar x \in Dom(f)\}$$
Donde $(\bar x, f(\bar x)) = (x_1,x_2,\dots,x_n,f(\bar x))$

- **Solo podemos graficar funciones en $n=1$ (Curvas en el plano) y $n=2$ (Superficies en el espacio)**

---
---
# Límite y continuidad
## "Bola"
Llamamos bola abierta de centro $\bar a$ y radio $r$ al conjunto 
$$B(\bar a,r)=\{\bar x \in \mathbb R^n \mid ||\bar x - \bar a|| < r\}$$
Decimos que la bola es cerrada si
$$B(\bar a,r)=\{\bar x \in \mathbb R^n \mid ||\bar x - \bar a|| \leq r\}$$
Tenemos la "corteza" una bola si
$$B(\bar a,r)=\{\bar x \in \mathbb R^n \mid ||\bar x - \bar a|| = r\}$$

Para n = ... la bola abierta $B(\bar a, r)$ es
 - 1 ==> $B(\bar a, r)$ es el intervalo abierto centrado en a y de "radio" r
 - 2 ==> $B(\bar a, r)$ es un disco abierto con centro $\bar a$ y de radio r
 - 3 ==> $B(\bar a, r)$ es una esfera con centro $\bar a$ y de radio r

---
## Límite
Sea $a\in\Bbb R^n$ y $f:Dom(f)\to\Bbb R$ definida en un dominio que incluye puntos arbitrariamente cercanos a $\bar a$. Decimos que
$$\lim(\bar x\to\bar a)f(\bar x)=L$$
Si cuando nos acercamos por cualquier dirección al punto $\bar a$ $f$ se acerca a $L$. 

### Evaluación de Límite
Como ahora estamos considerando dimensiones mayores la cantidad de formas de aproximarnos a un valor se vuelve infinita y el concepto de "límite por derecha/izquierda" deja de tener sentido.

Ejemplos de formas de aproximarse al punto $a$:
![[Pasted image 20211207164835.png]]

Para poder evaluar límites en puntos debemos establecer 'reglas' que aten ambos valores entre sí o mantengan uno de los dos como constante.
![[Pasted image 20211207165028.png]]

Por ejemplo. En rojo tenemos el límite $\lim_((x,0)\to (0,0))$ y en verde el límite $\lim_((x,x)\to (0,0))$. Estas reglas nos ayudan a definir la dirección por la que nos aproximamos al punto.

---
## Continuidad
Decimos que $f$ es continua en un punto $\bar a$ si
- $\bar a \in Dom(f)$
- $\lim_{\bar x\to\bar a} = f(\bar a)$

**Observación**:
Valen las [[Funciones|propiedades de las funciones continuas]]] en $\Bbb R\to\Bbb R$.

---
---
# Derivación
Podemos derivar funciones de varias variables si fijamos todas las variables que no nos interesan y las consideramos constantes.

---
## Derivadas parciales
Sean:
- $f:Dom(f)\subseteq\Bbb R^n\to\Bbb R$
- $\bar a=(a_1,a_2,\dots ,a_n)\in\Bbb R^n$

Y suponemos que $B(\bar a,r)\subset Dom(f)$ para algún $r>0$

$$\frac{\partial f}{\partial x_j}(a_1,a_2,\dots ,a_n)=f_{x_j}(a_1,a_2,\dots ,a_n)$$

Es la derivada parcial de $f$ en $x_j$ y se calcula derivando $f$ considerando como variable de derivación solo a $x_j$ y todas las demás como constantes.

**Observación**:
Que $f$ sea derivable en $\bar a$ no indica que $f$ es continua en dicho punto . Sin embargo, si todas las derivadas parciales de $f$ en $\bar a$ son continuas podemos garantizar que $f$ sea continúa en $\bar a$

#### Teorema de la continuidad
Sean:
- $f:Dom(f)\subseteq\Bbb R^n\to\Bbb R$
- $\bar a\in Dom(f)$
- $B(\bar a, r)\subset Dom(f)$ para algún $r>0$

Si existen todas las derivadas parciales de $f$ y son continuas para todo $\bar x\in B(\bar a,r)$ ==> $f$ es continua en para todo $\bar x\in B(\bar a,r)$.

### Interpretación geométrica 
- La positividad de $f_{x_j}(\bar a)$ nos indica la tasa de crecimiento de $f$ en $\bar a$ cuando nos movemos dejando fijas todas las coordenadas de $f$ menos $x_j$.

#### Vector tangente
Para una superficie en $\Bbb R^3$, el vector tangente en el punto $(a,b)$ se calcula con respecto a una de las curvas dadas por $(x,b,f(x,b))$ y $(a,y,f(a,y))$. De modo que en $(a,b)$ el vector tangente a la primera curva es $(1,0,f_x(a,b))$ y el vector tangente a la segunda es $(0,1,f_y(a,b))$.

**Observación**:
Sea $\Gamma(x)=(x,b,f(x,b))$, $(1,0,f_x(a,b))$ es la derivada de $\Delta (x)$ evaluada en $a$.

---
## Derivadas de orden $n$
La principal diferencia con respecto a la derivación de funciones $\mathbb R\rightarrow \mathbb R$ es que con las funciones de varias variables podemos derivar con respecto a una variable en particular. En general, en una función $\mathbb R^2\rightarrow \mathbb R$ hay $n^2$ posibles derivadas de orden $n$.

Por ejemplo, con $n=2$, tenemos 4 posibles derivadas
- $f_{xx}=\frac{af}{ax}(\frac{af}{ax})=\frac{a^2f}{a^2x}$
- $f_{xy}=\frac{af}{ax}(\frac{af}{ay})=\frac{a^2f}{axay}$
- $f_{yy}=\frac{af}{ay}(\frac{af}{ay})=\frac{a^2f}{a^2y}$
- $f_{yx}=\frac{af}{ay}(\frac{af}{ax})=\frac{a^2f}{ayax}$

Si la derivada segunda implica mas de una variable decimos que es cruzada

### Derivadas cruzadas
Sea:
- $f:Dom(f)\subseteq\mathbb R^2\rightarrow \mathbb R$
- $\bar a \in Dom(f)$

Si las funciones $f_{xy}$ y $f_{yx}$ ambas continuas en $B(\bar a, r)\subseteq Dom(f)$ para algún $r>0$ entonces:
$$f_{xy}(\bar x)=f_{yx}(\bar x),\forall\bar x\in B(\bar a, r)$$


---
## Derivada direccional
Si:
- $f : \mathbb R^n \rightarrow R$
- $B(\bar a, r) \subseteq Dom(f)\qquad r > 0$
- $\bar u$ vector unitario[^1]

Llamamos derivada direccional de $f$ hacia $\bar u$ en $\bar a$ como 
$$D_{\bar u}f(\bar a)=\lim_{h \rightarrow 0}f\frac{(\bar a+h\bar u)-f(\bar a)}{h}$$

%%Una forma más útil de esta ecuación es:
$$D_{\bar u}f(\bar a)=\langle \nabla f(\bar a),\bar u \rangle=\frac{\partial f}{\partial x_1}(\bar a)*u_1+\frac{\partial f}{\partial x_2}(\bar a)*u_2+\dots+\frac{\partial f}{\partial x_n}(\bar a)*u_n*$$%%

**Observaciones**:
1. Si el vector $\bar u$ no es unitario, entonces el vector $\bar v = \frac{\bar u}{||u||}$ es unitario y tiene la misma dirección que $\bar u$
2. Si tomamos $\bar u = e_i = (0,\dots,0,1,0,\dots,0)$, entonces $D_{\bar u}f(\bar a)=\frac{af}{ax_1}(\bar a)$.

---
## Definición $D_{\bar u}f(\bar x)$ por gradiente
- $f : Dom(f) \subseteq R^n \rightarrow R$
- $\frac{af}{ax_i}(\bar x)$ existen y son continuas $\forall \bar x \in B(\bar a,r) \subseteq Dom(f)$, $\forall i = 1 \dots n$
- $\bar u = (u_1,\dots,u_n)$ vector unitario

$$D_{\bar u}f(\bar a)=\langle \nabla f(\bar a),\bar u \rangle = \frac{af}{ax_1}(\bar a)u_1 + \dots + \frac{af}{ax_n}(\bar a)u_n $$

---
## Planos tangentes
El plano tangente a la gráfica de $f$ en el punto $(a,b,f(a,b))$ se define como el plano que pasa por $(a,b,f(a,b))$ y que está generado por los vectores $(1,0,f_x(a,b))$ y $(0,1,f_y(a,b))$.

- ### Ecuación vectorial
Sea $f(a,b)$ una función parcialmente derivable, la Ecuación vectorial del plano tangente a $f$ en el punto $(a,b)$ es:
$$S=\{(a,b,f(a,b))+r(1,0,f_x(a,b))+t(0,1,f_y(a,b))\in \mathbb R^2\mid r,t \in \mathbb R\}$$

- ### Ecuación normal
Sabemos que el vector $(1,0,f_x(a,b))\ \mathsf x\ ((0,1,f_y(a,b) = (-f_x(a,b),-f_y(a,b),1)$[^2] es perpendicular al plano tangente. Luego la ecuación normal del plano es:
$$\langle (x,y,z)-(a,b,f(a,b))\ ,\ (-f_x(a,b),-f_y(a,b),1)\rangle = 0$$

- ### Ecuación cartesiana
$$z=f(a,b)+(x-a)f_x(a,b)+(y-b)f_y(a,b)$$


---
## Gradiente $\nabla$
Si:
- $f : Dom(f) \subseteq R^n \rightarrow R$
- $\bar a \in Dom(f)$
- $\exists \frac{af}{ax_i}(\bar a)\qquad \forall i=1,\dots,n$

Llamamos gradiente de f en $\bar a$ al vector $\nabla f(\bar a)=(\frac{af}{ax_1}(\bar a),\dots,\frac{af}{ax_n}(\bar a))$

El gradiente es el vector que indica la dirección de mayor crecimiento de la función en un punto.

#### Máximo crecimiento/decrecimiento
Si:
- $f : Dom(f) \subseteq R^n \rightarrow R$
- $\bar a \in Dom(f)$
- $\frac{af}{ax_i}(\bar x)$ existen y son continuas $\forall \bar x \in B(\bar a,r) \subseteq Dom(f)$, $1 \leq i \leq n$
- $\nabla f(\bar a) \neq (0,\dots,0)$

Entonces:
1. El vector $\bar u = \frac{\nabla f(\bar a)}{||\nabla f(a)||}$ da la dirección unitaria de máximo crecimiento de $f$ en $\bar a$
2. El vector $\bar u = \frac{-\nabla f(\bar a)}{||\nabla f(a)||}$ da la dirección unitaria de máximo **de**crecimiento de $f$ en $\bar a$


---
## Regla de la cadena

### Caso 1 $\ \ x(t)\ \ \ y(t)$
Sea
- $f : Dom(f) \subset \mathbb R^n \rightarrow \mathbb R$
- $\bar a \in Dom(f)$ 

y tq $f_{x_1}, \dots ,f_{x_n}$ existen y son continuas en $B(\bar a_1, \bar r_1)$ para algún $r_1 > 0$.

Para $1\leq i \leq n$ y un intervalo $I\subset \mathbb R$, sean 
- $x_i\ :\ \mathbb R$ funciones derivables $\forall t \in I$ 
- y tal que $(x_1(t),\dots ,x_n(t)) \in B(\bar a_1, \bar r_1) \forall t \in I$. 

Entonces, la función $g(t)=f(x_1(t),\dots ,x_n(t))$ es derivable $\forall t \in I$ y además

$$\frac{dg}{dt}(t)=\frac{af}{ax_1}(x_1(t),\dots ,x_n(t)*x_1^`(t)+ \frac{af}{ax_2}(x_1(t),\dots ,x_n(t)*x_2^`(t)+\dots + \frac{af}{ax_n}(x_1(t),\dots ,x_n(t)*x_n^`(t)$$


### Caso 2 $\ \ x(s,t)\ \ \ y(s,t)$
Sea 
- $f : Dom(f) \subset \mathbb R^2 \rightarrow \mathbb R$ , 
- $\bar a \in Dom(f)$ 
 
y tq $f_x(x,b)$ y $f_y(a,y)$ existen y son continuas en $B(\bar a_1, \bar r_1)$ para algún $r_1 > 0$.

Sean 
- $x\ :\ Dom(x) \subset \mathbb R^2 \rightarrow \mathbb R$ 
- $y\ :\ Dom(y) \subset \mathbb R^2 \rightarrow \mathbb R$ 

dos funciones con sus derivadas parciales continuas en $B(\bar a_0, \bar r_0)$ para algún $r_0 > 0$ y tal que 
- $(x(s,t),y(s,t))\in B(\bar a_1, \bar r_1)\qquad \forall (s,t)\in B(\bar a_0, \bar r_0)$.

Entonces, la función definida por $g(s,t)=f(x(s,t),y(s,t))\qquad \forall (s,t) \in B(\bar a_0, \bar r_0)$ tiene derivadas parciales dadas por
- $$\frac{ag}{as}(s,t)=\frac{af}{ax}(x(s,t),y(s,t))*\frac{ax}{as}(s,t) + \frac{af}{ay}(x(s,t),y(s,t))*\frac{ay}{as}(s,t)$$
- $$\frac{ag}{at}(s,t)=\frac{af}{ax}(x(s,t),y(s,t))*\frac{ax}{at}(s,t) + \frac{af}{ay}(x(s,t),y(s,t))*\frac{ay}{at}(s,t)$$

---
---
# Curvas y superficies de nivel
Son como una impresión del gráfico en el plano(Curvas) o el espacio(Superficie).
## Curva de nivel
Sea
1. $k\in\mathbb R$ 
2. $f:Dom(f)\subseteq\mathbb R^2\rightarrow \mathbb R$

Llamamos curva de nivel k de f al subconjunto de $Dom(f)$ definido por 

$$C_k=\{(x,y)\in Dom(f)\mid f(x,y)=k\}$$

($C_k$ puede ser $\emptyset$, puntos aislados o una curva)

**Observación**: Si $d\in Dom(f)$ entonces existe al menos una curva o superficie de nivel que pasa por $p$

---
#### Recta tangente a la curva
Dado
- $f:Dom(f) \subseteq \mathbb R^2 \rightarrow \mathbb R$
- $k \in \mathbb R$
Sea 
- $\gamma$(gamma) una curva en $C_k$

Es decir que 
1. $\gamma(t)=(x(t),y(t)) \in C_k$ y definimos $\gamma(t_0)=(x_0,y_0)$ 
2. $f(x(t),y(t))=k$ $\forall t \in I$ ($I \subset \mathbb R$). 

Gamma es una función $\gamma : I \rightarrow \mathbb R^2$ tal que $f(\gamma(t)) = k$ $\forall\ t\in I$.

Por la [[Funciones de varias variables#Regla de la cadena|regla de la cadena]] tenemos que:

$$\frac{af}{ax}(x(t),y(t))*x'(t)+\frac{af}{ay}(x(t),y(t))*y'(t)=0\quad\forall t \in I$$
En particular para algún $t_0\in I$
$$\frac{af}{ax}(x(t_0),y(t_0))*x'(t_0)+\frac{af}{ay}(x(t_0),y(t_0))*y'(t_0)=0\quad\forall t \in I$$
$$\biggl\langle\ \biggl(\frac{af}{ax}(x(t_0),y(t_0)),\frac{af}{ay}(x(t_0),y(t_0))\biggr),(x'(t_0),y'(t_0))\ \biggr\rangle=0$$
O sea
$$\langle \nabla f(x_0,y_0),\gamma'(t_0)\rangle=0$$

Luego, si $\nabla f(x_0,y_0) \neq 0$ entonces $\nabla f(x_0,y_0)$ es perpendicular al vector tangente a la curva $\gamma$ y, por lo tanto, es tangente a la curva de nivel de $f$ que pasa por $(x_0,y_0)$

**Conclusión**:
El vector $(-\frac{af}{ay}(x_0,y_0),\frac{af}{ax}(x_0,y_0))$ (que es perpendicular a $\nabla f(x_0,y_0)$) es ==tangente== a la curva que pasa por $(x_0,y_0)$ 

---
### Recta tangente a la curva
La recta tangente a la curva de nivel de $f:Dom(f) \subseteq \mathbb R^2 \rightarrow \mathbb R$ que pasa por $(x_0,y_0)$ está definido como
$$(x,y)=(x_0,y_0)+t\biggl(-\frac{af}{ay}(x_0,y_0),\frac{af}{ax}(x_0,y_0)\biggr),\ con\ t\in\mathbb R$$


---
## Superficie de nivel
Sea
1. $k\in\mathbb R$ 
2. $f:Dom(f)\subseteq\mathbb R^3\rightarrow \mathbb R$

Llamamos superficie de nivel $k$ de $f$ al subconjunto de $Dom(f)$ definido por 

$$S_k=\{(x,y,z)\in Dom(f)\mid f(x,y,z)=k\}$$

### Plano tangente a la superficie
La ecuacion normal del plano tangente a la superficie de nivel en $(x_0,y_0,z_0)$ es
$$\langle (x,y,z)-(x_0,y_0,z_0),\nabla f(x_0,y_0,z_0) \rangle=0$$

ya que $\nabla f(x_0,y_0,z_0)$

---
---
# Máximo y mínimo ($\mathbb R^2$)
Sea:
- $f:Dom(f)\subseteq\mathbb R^2\rightarrow \mathbb R$
- $(x_0,y_0) \in Dom(f)$

#### Definición
**Local**
- Máximo
$f$ tiene un máximo local (o relativo) en $(x_0,y_0)$ si existe una bola centrada en $(x_0,y_0)$ tal que $f(x_0,y_0)\geq f(x,y)$ $\forall (x,y)\in B$. $f(x_0,y_0)$ es el máximo local de $f$
- Mínimo
$f$ tiene un mínimo local (o relativo) en $(x_0,y_0)$ si existe una bola centrada en $(x_0,y_0)$ tal que $f(x_0,y_0)\leq f(x,y)$ $\forall (x,y)\in B$. $f(x_0,y_0)$ es el máximo local de $f$

**Absoluto**
Si las desigualdades anteriores se cumplen $\forall (x,y)\in Dom(f)$ decimos que $f$ tiene un máximo/mínimo absoluto en $(x_0,y_0)$

---
## Encontrar extremos
Teorema p109

### Puntos críticos
Si la función tiene un extremo local en $(x_0,y_0)$ entonces 
$$\nabla f(x_0,y_0)=(0,0)$$
Llamamos a $(x_0,y_0)$ "==punto crítico=="

Además, si se cumple que $\nexists f_x(x_0,y_0)$ o $\nexists f_y(x_0,y_0)$, llamamos a $(x_0,y_0)$ "==punto singular==".

---
### Discriminante
Suponemos que 
- las derivadas parciales de orden 1 y 2 de $f$ son continuas en $B((x_0,y_0),r)$ 
- y que $\nabla f(x_0,y_0)=(0,0)$.

Sea $D\dot=D(x_0,y_0)=f_{xx}(x_0,y_0)f_{yy}(x_0,y_0)-[f_{xy}(x_0,y_0)]^2$[^3]

Entonces:
1. Si $D > 0$ y $f_{xx} > 0$ (o $f_{yy} > 0$) ==> $f$ tiene un mínimo local en $(x_0,y_0)$.
2. Si $D > 0$ y $f_{xx} < 0$ (o $f_{yy} < 0$) ==> $f$ tiene un máximo local en $(x_0,y_0)$.
3. Si $D < 0$, entonces $f$ tiene un punto silla[^4] en $(x_0,y_0)$.
4. Si $D = 0$, no se puede asegurar nada.

**Observación**

$$D\ \dot =\ Det\begin{bmatrix}f_{xx}(x_0,y_0)&f_{xy}(x_0,y_0)\\f_{xy}(x_0,y_0)&f_{yy}(x_0,y_0) \end{bmatrix}=f_{xx}(x_0,y_0)f_{yy}(x_0,y_0)-f_{xy}(x_0,y_0)f_{xy}(x_0,y_0)$$

La matriz $H(x_0,y_0) = \begin{bmatrix}f_{xx}(x_0,y_0)&f_{xy}(x_0,y_0)\\f_{xy}(x_0,y_0)&f_{yy}(x_0,y_0) \end{bmatrix}$ se llama *hessiana* de $f$ en $(x_0,y_0)$ y su determinante se llama *hessiano* (o discriminante) de $f$ en $(x_0,y_0)$.



[^1]: Vectores de longitud 1. $\bar u = (u_1,\dots,u_n) \in \mathbb R^n$ es un vector unitario si $||\bar u|| = 1$
[^2]: [[Vectores#Producto vectorial|Producto vectorial]]
[^3]:$[f_{xy}(x_0,y_0)]^2 = 0$ (ya que $(x_0,y_0)$ es un punto crítico)
[^4]:Parece un mínimo por un eje y un máximo por otro. [Wikipedia](https://es.wikipedia.org/wiki/Punto_de_silla) 