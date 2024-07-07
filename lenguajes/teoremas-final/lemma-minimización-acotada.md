---
tags:
  - lfyc-c-VII
---
> Sean $n,m\ge0$. Sea $P:D_P\subseteq\omega\times\omega^n\times\Sigma^{*m}\to\omega$ un predicado $\Sigma$-pr. Entonces:
> (a) $M(P)$ es $\Sigma$-recursiva
> (b) Si hay una función $\Sigma$-pr $f:\omega^n\times\Sigma^{*m}\to\omega$ tal que $$M(P)(\vec x,\vec\alpha)=\min_t P(t,\vec x,\vec\alpha)\le f(\vec x,\vec\alpha)$$ para cada $(\vec x,\vec\alpha)\in D_{M(P)}$. Entonces $M(P)$ es $\Sigma$-pr.

---

$(a)$ Sea $$\bar P=P\cup (C_0^{n+1,m}|_{(\omega^{n+1}\times\Sigma^{*m})-D_P}):\omega\times\omega^{n}\times\Sigma^{*m}\to\omega$$ un predicado $\Sigma$-total, que ademas va a ser $\Sigma$-pr. 

Veamos primero que $M(P)=M(\overline P)$. Notar que para todo $(\vec x,\vec\alpha)\in\omega^{n}\times\Sigma^{*m}$
$$\{t\in\omega:P(t,\vec x,\vec\alpha)=1\}=\{t\in\omega:\bar P(t,\vec x,\vec\alpha)=1\}$$
Esto nos dice que $M(P)=M(\overline P)$, ya que:
- $D_{M(P)}=D_{M(\overline P)}$ 
	- Recordar que $D_{M(P)}=\{(\vec x,\vec\alpha)\in\omega^{n}\times\Sigma^{*m} :(\exists t\in\omega)\ P(t,\vec x,\vec\alpha)=1\}$
- y ademas  $M(P)(\vec x,\vec\alpha)=M(\overline P)(\vec x,\vec\alpha)$ para cada $(\vec x,\vec\alpha)\in D_{M(P)}$
	- $min\{t\in\omega:P(t,\vec x,\vec\alpha)=1\}=min\{t\in\omega:\bar P(t,\vec x,\vec\alpha)=1\}$

Ahora vemos que $M(\overline P)$ es $\Sigma$-*recursiva*. Sea k tal que $\bar P\in PR_k^{\Sigma}$. Dado que
- $\bar P$ es $\Sigma$-total y
- $PR_k^{\Sigma}\subseteq R_k^{\Sigma}$

Entonces tenemos que $M(\bar P)\in R_{k+1}^{\Sigma}$ y por lo tanto $M(P)$ es $\Sigma$-r.

---
$(b)$ Ya que $M(P)=M(\bar P)$, basta con probar que $M(\bar P)$ es $\Sigma$-*primitivamente recursiva*.
(1) Primero veamos que $D_{M(\bar P)}$ es $\Sigma$-p.r. Notar que
$$
\begin{align}
\chi_{D_{M(\bar P)}}^{\omega^{n+1}\times\Sigma^{*m}}
&=\lambda\vec x\vec\alpha
	\left[
		(\exists t\in\omega)_{t\leq f(\vec x,\vec\alpha)} P(t,\vec x,\vec\alpha)
	\right] \\
&=\lambda y\vec x\vec\alpha
	\left[
		(\exists t\in\omega)_{t\leq y} P(t,\vec x,\vec\alpha)
	\right] \circ \left[
		f,p_1,\dots,p_{n+m}
	\right]
\end{align}
$$
es claramente $\Sigma$-pr por el [[lemma-cuantificación-acotada|lema de cuantificación acotada]].
(2) Sea
$$
\begin{align}
P_1
&=\lambda t \vec x\vec \alpha\left[
	\bar P(t, \vec x,\vec \alpha) \land
	(\forall j\in\omega)_{j\leq t}\ j=t\ \lor\ 
		\lnot\bar P(j, \vec x,\vec \alpha)
\right]\\
\end{align}
$$
un predicado $\Sigma$-total y además $\Sigma$-p.r.. Notar que para $(\vec x,\vec \alpha)\in \omega^n\times\Sigma^{*m}$ tenemos que
$$
\begin{align}
P_1(t,\vec x,\vec \alpha)
&= 1\iff (\vec x,\vec \alpha)\in D_{M(\bar P)} \land t=M(\bar P)(\vec x,\vec \alpha) \\
\end{align}
$$
Esto nos dice que
$$
M(\bar P)= \left.\left(
	\lambda{\vec{x}\vec{\alpha}}\left[
		\prod^{f(\vec{x},\vec{\alpha})}_{t=0} t^{P_1(t,\vec{x},\vec{\alpha})}
	\right]
\right)\right|_{D_{M(\bar{P})}}
$$
Por lo que para ver que 