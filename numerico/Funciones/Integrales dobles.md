# Integradas dobles en rectángulos
## Volumen debajo de una superficie
Sea $Q=[a,b]\ \mathsf x\ [c,d]$ un rectángulo en $\mathbb R^2$ y $f:Q\rightarrow \mathbb R$ no negativa.

Para obtener el volumen debajo de la gráfica de una [[Funciones de varias variables|función de varias variables]] $f$ podemos dividir el rectángulo $Q$ en sectores cada vez más pequeños y calcular el volumen de los "pilares" desde 0 hasta la función. Este procedimiento es muy parecido al de las derivadas en $\mathbb R$

![[Pasted image 20211110094318.png]]

Para realizar dicho procedimiento usamos una "doble suma de Rieman"

$$\sum^{m}_{i=1}\sum^{n}_{j=1}f(x_{ij},y_{ij})\Delta x_i\Delta y_j$$

## Definición
Dado una partición $P=\{Q_{ij} \mid 1 \leq i \leq m,1 \leq n \leq n\}$ de un rectángulo $Q\in\mathbb R^2$ definimos la norma de la partición $P$ como la mayor longitud de las diagonales de los sub-rectángulos $Q_{ij}$ y la denotamos $||P||$.

Sea $Q$ un rectángulo en $\mathbb R^2$ y $f:Q\rightarrow\mathbb R$, la integral doble de $f$ sobre el rectángulo $Q$ es

$$\iint_{Q}f(x,y)dA=\lim_{||P||\rightarrow 0}\sum^{m}_{i=1}\sum^{n}_{j=1}f(x_{ij},y_{ij})\Delta x_i\Delta y_j$$

Si este límite existe. En tal caso, $f$ se dice integrable sobre $Q$.

-----------------------------------------------------------

**Observaciones**
1. En la def de integral doble pedimos $f$ no negativa, pero la def sigue siendo válida si $f$ es negativa o cambia de signo
2. Se puede demostrar que si $f$ es continua en $Q$ ==> $f$ es integrable sobre $Q$. 
	- Más aun, si $f$ es acotada y continua en $Q$, excepto por una cantidad **finita** de curvas **suaves** entonces $f$ es integrable sobre $Q$ . 
3. Si $f\geq0$ e integrable sobre $Q$ ==> $\iint_Q f(x,y) dA$ = volumen entre la gráfica y $Q$
4. A veces denotamos $\iint_Q f(x,y) dxdy$ en lugar de $\iint_Q f(x,y) dA$

## Integrales Iteradas
Para resolver más fácilmente las integradas dobles usamos las integrales iteradas.
$$\int^{b}_{a}\bigg( \int^{d}_{c} f(x,y)\ dx \bigg) dy=\int^{b}_{a}\int^{d}_{c} f(x,y) dxdy $$

### Teorema de Fubini
Si $f$ es continua en el rectángulo $Q=[a,b]\ \mathsf x\ [c,d]$, entonces

$$\iint_Q f(x,y) dA =\int^{b}_{a}\int^{d}_{c} f(x,y) dxdy=\int^{d}_{c}\int^{b}_{a} f(x,y) dydx$$

# Integradas dobles en regiones generales
Sea

## Integrales de tipo 1

## Integrales de tipo 2