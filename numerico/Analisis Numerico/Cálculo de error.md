# Fuentes de error
1. **Errores en los datos de entrada** (Frecuentemente inevitables). Estos tipos de errores pueden provenir de mediciones erróneas o al intentar representar un número real irracional con un número finito de dígitos.
2. **Errores de redondeo**. Aparecen cuando los cálculos se realizan usando un número finito de datos.
3. **Errores de truncamiento**. Aparecen cuando un proceso infinito es reemplazado con un proceso finito. Ej. Serie de Taylor y Polinomio de Taylor.
4. Errores humanos. Frecuentes y a veces difíciles de detectar.

---
---
# Cálculo de error
## Cálculo
Sea un número real $r$ (valor exacto) aproximado por otro número $\bar r$, se define el **error** por $r-\bar r$. Llamaremos respectivamente

- **Error absoluto**: $\Delta r=|r-\bar r|$
- **Error relativo**: $\delta r=\frac{\Delta r}{|r|}$
- **Error porcentual**:$100*\delta r$

## Redondeo y truncado
Ambas son formas de escribir un número de dígitos.
### Redondeo
La aproximación por redondeo a $n$ dígitos decimales $\tilde r$ de un número $r$ es un número de $n$ dígitos fraccionales que coinciden con los de $r$ si el dígito $(n+1)$ es 0,1,2,3 o 4. Por otro lado, si el dígito $(n+1)$ es 5,6,7,8 u 9, entonces para definir $\tilde r$ se suma una unidad al $n-$esimo digito de $r$.
El error que este método genera es:
$$|r-\tilde r|\leq \frac1210^{-n}$$
### Truncado
La aproximación por truncado a $n$ dígitos decimales $\bar r$ de un número $r$ es un número de $n$ dígitos fraccionarios que coinciden con los primeros $n$ dígitos fraccionarios de $r$.
El error que genera este método es:
$$|r-\bar r|\leq 10^{-n}$$
---
## Errores en las operaciones
### Suma
- $y = x_1 + x_2$ ; $\bar y = \bar x_1 + \bar x_2$
$$\bbox[10px,border:0.5px solid red]{
\Delta y \leq|x_1-\bar x_1|+|x_2-\bar x_2|
}$$
$$\bbox[10px,border:0.5px solid red]{\delta y=\frac{\Delta y}{|y|}\leq \frac{\Delta x_1+ \Delta x_2}{|x_1+x_2|}}$$

### Resta
- $y = x_1 - x_2$ ; $\bar y = \bar x_1 - \bar x_2$
$$\bbox[10px,border:0.5px solid red]{\Delta y\leq|(x_1-\bar x_1)-(x_2-\bar x_2)|}$$
$$\bbox[10px,border:0.5px solid red]{\delta y\leq \frac{\Delta x_1+ \Delta x_2}{|x_1-x_2|}}$$

### Producto
- $y = x_1 * x_2$ ; $\bar y = \bar x_1 * \bar x_2$
$$\bbox[10px,border:0.5px solid red]{\Delta y\leq|x_2|\Delta x_1+|x_1|\Delta x_2}$$
$$\bbox[10px,border:0.5px solid red]{\delta y\leq\delta x_1+\delta x_2}$$

### División
- $y = x_1 / x_2$ ; $\bar y = \bar x_1 / \bar x_2$
$$\bbox[10px,border:0.5px solid red]{\Delta y\leq\frac1{|x_2|}\Delta x_1+\frac{|x_1|}{|x_2^2|}\Delta x_2}$$
$$\bbox[10px,border:0.5px solid red]{\delta y\leq\delta x_1+\delta x_2}$$

---
# Cancelación de dígitos significativos

> **Dígitos significativos**
> El número $\bar a$ se aproxima al número real $a$ con $r$ dígitos significativos si
> $$\frac{\Delta a}{|a|}\leq 5*10^{-r}=\frac12*10^{1-r}$$

En los algoritmos numéricos se intenta evitar la gran cancelación de dígitos significativos que se produce en la resta de números próximos. Ej.

Sean $x_1=10.123455\pm 0.5*10^{-6}$ y $x_2=10.123789\pm 0.5*10^{-6}$.
Ambos tienen un error absoluto $\leq 0.5*10^{-6}$ y un error relativo $<0.5*10^{-7}$, por lo tanto, tienen 8 dígitos significativos.
Ahora bien, la resta $y=x_1-x_2=-0.000334\pm0.5*10^{-6}$ tiene un error absoluto pequeño; sin embargo, el error relativo
$$\frac{\Delta y}{|y|}\leq \frac{10^{-6}}{0.000334}<3*10^{-3}<5*10^{-3}$$
indica que tiene ***solo 3 dígitos significativos***


---
---
## Representación de números en computadora
Las computadoras utilizan como sistema de numeración el binario o el Hexadecimal. La conversión del sistema decimal a alguno de estos dos puede generar problemas.

Observaciones:
1. La mayoría de los números reales no pueden ser representados exactamente en cualquier base.
2. Aparecen errores de representación cuando un número es convertido de un sistema de numeración a otro.
3. Aparecen errores debido a que la computadora usa aritmética finita.

Los números reales suelen ser representados mediante el estándar de [[punto flotante]].
Al sistema de punto flotante $(\beta ,t,L,U)$ lo forman el conjunto de números normalizados en punto flotante en el sistema de numeración con base $\beta$ y $t$ dígitos para la parte fraccionaria. Es decir, números de la forma
$$x=m\beta^e$$
donde
$$m=\pm0.d_{-1}d_{-2}\cdots d_{-t}$$
con $d_{-i}\in\{0,\cdots, \beta-1\}$ para $i=1,2,\cdots,t$ con $d_{-1}\neq 0$ y $L\leq e\leq u$. Además, $\beta,e$ y $m$ se denominan *base*, *exponente* y *mantisa*, respectivamente. Es decir, $1/\beta \leq |m| < 1$. Ej. En el sistema $(10,9,-10,10)$
$$100,325215 = 0.100325215*10^{3}$$
$$0,000014758 = 0.14758*10^{-4}$$
