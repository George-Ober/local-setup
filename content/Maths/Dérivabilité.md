

Soient $A \in \mathcal{P}(\mathbb{R})$,  $a \in \bar{\mathbb{R}}$, $a$ est un point adhérent à $A$ s'il existe 


Soit $f \in \mathcal{C}^{0}(I, \mathbb{R})$ Si $f$ est bijective de $I$ sur $J = f(I)$ alors sa bijection réciproque est continue sur $J$.


Soit $f: I \to \mathbb{R}$ continue, alors


$f$ est strictement monotone sur $I$ ssi $f$ est injective


>[!tip] Proposition : Approximation Linéaire au premier ordre
>Si $f$ est dérivable en $a$, il existe $\varepsilon : I \to \mathbb{R}$ telle que
>$$
\forall x \in I, f(x) = f(a) + f'(a)(x-a) + (x-a)\varepsilon(x)$$
> et
>$$
\lim_{ x \to a } \varepsilon(x) = 0 = \varepsilon(a)$$


>[!tip] Proposition : Soit $I$ un intervalle ouvert, $a\in I$ et $f:I\to\mathbb R$ dérivable en $a$.
>Alors si $f$ admet un extrémum local en $a$, on a $f'(a)=0$.



$$
\therefore c \in ]x+h, x[ : f'(c)(x+h-x) = \underbrace{ f(x+h) }_{ f(c)\times h } - f(x)
$$
alors
$$
\begin{align}
c = (x + h) - \theta h & \iff c - x = (1-\theta) h  \\
 & \iff \theta = \frac{c-(x+h)}{-h}
\end{align}
$$
Par construction:
$$
\begin{align}
c \in ]x+h, x[  & \implies x + h < c < x \\
 & \implies 0 <c-(x+h) < -h \\
 & \implies 0 < \frac{c - (x+h)}{-h} < 1 \\
 & \implies \theta \in ]0, 1[
\end{align}
$$
Ainsi, en posant $\theta = \frac{(x+h)-c}{h}$, on a $\theta \in ]0, 1[$ et $c = (x+h) - \theta h$




Soit $\alpha > 1$ fq. Alors :
$$
\alpha x < (1+x)^{\alpha} - 1^{\alpha} < \alpha 2 ^{\alpha - 1} x
$$


Soit $I$ un intervalle de $\bar{\mathbb{R}}$ et $f:I\to \mathbb{R}$ continue sur $I$, dérivable sur $\overset{\circ}{I}$.

- $\forall x \in I, \forall h \in \mathbb{R}^{*}$ tel que $h+x \in I$
	- $\exists \theta \in]0,1[ : f(x+h) - f(x) = f'(x+\theta h)\cdot h$
-  $\forall (x, y) \in I^{2}$ tel que $x \neq y$,
	- $\exists c \in ]x, y[:f(x)-f(y) = (x-y)f'(c)$
- $\forall (x, y) \in {\overset{\circ}{I}}^{2}$
	- $\exists c \in ]x, y[:f(x)-f(y) = (x-y)f'(c)$
 

$$
\lim_{ x \to +\infty } \frac{(\ln x)^\alpha}{x^\beta}, (\alpha, \beta) \in (\mathbb{R}_{+}^*)^2
$$
