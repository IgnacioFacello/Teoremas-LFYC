---
tags:
  - lfyc-c-IV
---
> Sea $\Sigma$ un alfabeto finito. Si $f:\omega\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m\to\omega$ es $\Sigma$-pr, con $S_1,\dots,S_n\subseteq\omega$ y $L_1,\dots,L_m\subseteq\Sigma^*$ no vacíos, entonces la función $\lambda xy\vec x\vec\alpha\left[\sum_{t=x}^{t=y}f(t,\vec x,\vec\alpha)\right]$ es $\Sigma$-pr

---
> G da vuelta xy en la función original

Sea 
$$
G=\lambda tx\vec x\vec\alpha\left[\sum_{i=t}^{i=x}f(i,\vec x,\vec\alpha)\right]
$$

Luego tenemos que 
$$
\lambda xy\vec x\vec\alpha\left[\sum_{t=x}^{t=y}f(t,\vec x,\vec\alpha)\right] = 
G\circ\left[p_2^{n+2,m},p_1^{n+2,m},p_3^{n+2,m},\dots,p_{n+2+m}^{n+2,m}\right]
$$
por lo tanto basta con probar que G es $\Sigma$-pr (1).
Primero notemos que:
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
Es decir que podemos definir
$$
\begin{align}
	h &= \lambda x\vec x\vec\alpha\left[\begin{cases}
		0 & si\ x>0\\
		f(0,\vec x,\vec\alpha) &si\ x=0
	\end{cases}\right] \\
	g &= \lambda Atx\vec x\vec\alpha\left[\begin{cases}
		0 & si\ x>0\\
		A+f(t+1,\vec x,\vec\alpha) &si\ x=0
	\end{cases}\right] \\
\end{align}
$$
tales que $G=R(h,g)$. Solo queda probar que $h$ y $g$ son $\Sigma$-pr.
Sean:
$$
\begin{align}
D_1&= \{(x,\vec x,\vec\alpha)\in\omega\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m
: x\gt0\} \\
D_2&= \{(x,\vec x,\vec\alpha)\in\omega\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m
: x=0\} \\
H_1&= \{(z,t,x,\vec x,\vec\alpha)\in\omega^3\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m
: x\gt t+1\} \\
H_2&= \{(z,t,x,\vec x,\vec\alpha)\in\omega^3\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m
: x\leq t+1\}
\end{align}
$$
Luego
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
y por el lemma de [[division-casos-pr|funciones por casos]] son ambas $\Sigma$-pr