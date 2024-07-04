---
tags:
  - lfyc-c-IV
---
> **Lema 8** Sea $\Sigma$ un alfabeto finito. Si $f:\omega\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m\to\omega$ es $\Sigma$-pr, con $S_1,\dots,S_n\subseteq\omega$ y $L_1,\dots,L_m\subseteq\Sigma^*$ no vacíos, entonces la función $\lambda xy\vec x\vec\alpha\left[\sum_{t=x}^{t=y}f(t,\vec x,\vec\alpha)\right]$ es $\Sigma$-pr
?

Para mejorar la legibilidad vamos a tomar
$$
S_1\times\dots\times S_n\times L_1\times\dots\times L_m={S_{1..n}}\times{L_{1..m}}
$$

---
> Pasamos la sumatoria a la forma convenida para la recursion (primer parámetro es el recursivo)

Sea 
$$
G=\lambda tx\vec x\vec\alpha\left[\sum_{i=x}^{i=t}f(i,\vec x,\vec\alpha)\right]
$$
Luego tenemos que 
$$
\lambda xy\vec x\vec\alpha\left[\sum_{t=x}^{t=y}f(t,\vec x,\vec\alpha)\right] = 
G\circ\left[p_2^{n+2,m},p_1^{n+2,m},p_3^{n+2,m},\dots,p_{n+2+m}^{n+2,m}\right]
$$
por lo tanto basta con probar que $G$ es $\Sigma$-pr. 

---
> Buscamos funciones h y g tales que G=R(h,g)

Primero, notemos que
$$
\begin{align}
G(0,x,\vec x,\vec\alpha) &= \begin{cases}
	0 & si\ x>0 \\
	f(0,\vec x,\vec\alpha) & si\ x=0
\end{cases} \\
G(t+1,x,\vec x,\vec\alpha) &= \begin{cases}
	0 & si\ x>t+1 \\
	G(t,x,\vec x,\vec\alpha)+f(t+1,\vec x,\vec\alpha) & si\ x\leq t+1
\end{cases}
\end{align}
$$
Es decir que si definimos
$$
\begin{align}
	h : \omega\times{S_{1..n}}\times{L_{1..m}}&\to\omega\\
	(x,\vec x,\vec\alpha)&\to \begin{cases}
	    0 & si\ x>0 \\
	    f(0,\vec x,\vec\alpha) & si\ x=0
    \end{cases} \\ 
	g : \omega^{3}\times{S_{1..n}}\times{L_{1..m}}&\to\omega \\
	(A,t,x,\vec x,\vec\alpha)&\to \begin{cases}
	    0 & si\ x>t+1 \\
	    A+f(t+1,\vec x,\vec\alpha) & si\ x\leq t+1
    \end{cases} \\ 
\end{align}
$$
tenemos que $G=R(h,g)$. Solo queda probar que $h$ y $g$ son $\Sigma$-pr. 

---
> Vamos a definir h y g por casos y usar el lema de division por casos para probar que son pr

Sean
$$
\begin{align}
D_1&= \{(x,\vec x,\vec\alpha)\in\omega\times{S_{1..n}}\times{L_{1..m}}
: x\gt0\} \\
D_2&= \{(x,\vec x,\vec\alpha)\in\omega\times{S_{1..n}}\times{L_{1..m}}
: x=0\} \\
H_1&= \{(z,t,x,\vec x,\vec\alpha)\in\omega^3\times{S_{1..n}}\times{L_{1..m}}
: x\gt t+1\} \\
H_2&= \{(z,t,x,\vec x,\vec\alpha)\in\omega^3\times{S_{1..n}}\times{L_{1..m}}
: x\leq t+1\}
\end{align}
$$
Notar que
$$
\begin{align}
	h &= 
		C_0^{n+1,m}|_{D_1} \cup 
		\lambda x\vec x\vec\alpha[f(0,\vec x,\vec\alpha)]|_{D_2} \\
	g &= 
		C_0^{n+3,m}|_{H_1} \cup 
		\lambda Atx\vec x\vec\alpha[A + f(t+1,\vec x,\vec\alpha)]|_{H_2} \\
\end{align}
$$
Ya que $f$ es $\Sigma$-p.r. y 
$$
\begin{align}
	\lambda x\vec x\vec\alpha[f(0,\vec x,\vec\alpha)] &= 
		f\circ\left[C_0^{n+1,m},p_2^{n+1,m},\dots,p_{n+1+m}^{n+1,m}\right]
	\\
	\lambda Atx\vec x\vec\alpha[A + f(t+1,\vec x,\vec\alpha)] &= 
		\lambda xy[x+y]\circ\left[p_1^{n+3,m},f\circ\left[
			Succ\circ{p_2}^{n+3,m},p_4^{n+3,m},\dots,p_{n+3+m}^{n+3,m}
		\right]\right]
\end{align}
$$
tenemos que $\lambda x\vec x\vec\alpha[f(0,\vec x,\vec\alpha)]$ y $\lambda Atx\vec x\vec\alpha[A + f(t+1,\vec x,\vec\alpha)]$ son $\Sigma$-p.r. y por el [[division-casos-pr|lemma de división por casos]] , si demostramos que $D_1,D_2,H_1,H_2$ son $\Sigma$-p.r. entonces $h$ y $g$ también lo serán. 

---
> Falta probar que los conjuntos son pr. Hacemos esto con el lema de Dominio pr para definir pertenencia al conjunto rectangular.

Veamos el caso $H_1$ y los demás son análogos. Dado que $f$ es $\Sigma$-pr entonces $D_f=\omega\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m$ es $\Sigma$-p.r., lo cual nos dice que los conjuntos $S_1,\dots,S_n,L_1,\dots,L_m$ también lo son y por lo tanto 
$$R=\omega^3\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m$$
es $\Sigma$-p.r.. Notar que
$$
\chi^{\omega^{n+3}\times\Sigma^{*m}}_{H_1} = \left[
	\chi^{\omega^{n+3}\times\Sigma^{*m}}_R \land 
	\lambda Atx\vec x\vec\alpha[ x\gt t+1 ]
\right]
$$
es conjunción de dos predicados $\Sigma$-p.r. por lo cual $H_1$ es $\Sigma$-p.r.