# Definición
El estándar IEEE 754 se usa para representar de manera compacta números reales con decimales en una computadora.
Para un número $x$ con $n$ dígitos enteros y $m$ dígitos fraccionales 
$$x=0.d_{1} \ d_{2}\ \dots \ d_{m-1} \ d_{m}\mathsf x10^e$$
su representación en **punto flotante** $(\beta,t,L,U)$ es
$$x=\mathcal m*\beta^e$$
con $m$ (la mantisa) tal que
$$\mathcal m=\pm0. d_{1}\ d_{2}\ \dots \ d_{t}$$
es decir, $\mathcal m$ es una aproximación a $x$ [[Cálculo de error#Truncado|truncada]] o [[Cálculo de error#Redondeo|redondeada]] a $t$ dígitos.
$\beta$ es la base de $x$ y $1/\beta\leq |\mathcal m| < 1$. $e$ es el exponente tq $L \leq e \leq U$.

# Errores de redondeo
Para la representación $\bar r$ en un sistema de punto fijo $(\beta,t,L,U)$ del número real $r$, tenemos que:
$$\bbox[10px,border:0.5px solid red]{\Delta \bar r\leq\frac12\beta^{e-t}}$$
$$\bbox[10px,border:0.5px solid red]{\delta\bar r=\frac12\beta^{1-t}}$$

# Operaciones aritméticas

## Suma

