$$
\begin{align*}
F(x) = 
\int_a^x \arctan(\sqrt{t + 1}) dt
&= \
\left[ t \cdot \arctan(\sqrt{t + 1}) \right]_a^x &&- \int_a^x t\cdot \frac{1}{(\sqrt{t+1})^2 + 1} \cdot \frac{1}{2\sqrt{t+1}}dt\\
&= \left[ (t+2) \cdot \arctan(\sqrt{t + 1}) \right]_a^x &&- \int_a^x (t + 2) \frac{1}{t+2} \frac{1}{2\sqrt{t+1}}dt\\
&= \left[ (t+2) \cdot \arctan(\sqrt{t + 1}) \right]_a^x &&- \int_a^x \cancel{(t + 2)} \frac{1}{\cancel{t+2}} \frac{1}{2\sqrt{t+1}}dt\\
&= \left[ (t+2) \cdot \arctan(\sqrt{t + 1}) \right]_a^x &&- \int_a^x \frac{1}{2\sqrt{t+1}}dt\\
&= \Big[ (t+2)B \cdot \arctan(\sqrt{t + 1}) \sqrt{t + 1} \Big]_a^x \\
\vec \imath
\end{align*}
$$


Comment écris-tu le plan cartésien usuel? $(O, \vec \imath, \vec \jmath)$ ou $(O, \vec i, \vec j)$?

$$
\begin{array}
a & b & c & d \\
a & b \\
d \\
c \\

\end{array}
$$



>[!tip] Caractérisation séquentielle de la borne supérieure
>$$
\sigma = \sup A \iff
\left\{
\begin{array}{ll}
\sigma \in M(A) \\
\exists x \in A^{\mathbb{N}} : x \text{ converge vers } \sigma
\end{array}
\right.$$



En effet, on retrouve ici les vecteurs cartésiens usuels $(O, \vec{i}, \vec{j}, \vec{k})$ que l'on utilise pour dénoter la base des systèmes de coordonnées

Soit $n \in \mathbb{N}$ fq. on retrouve ici notre problème
$$
f:\left| \begin{array} {ll}
	]- \infty, 0[ &\to  \mathbb{R}_{+}^* \\
t &\mapsto \psi(t)
\end{array} \right.
$$

Posons donc $\psi:\left|\begin{array}{ll} \mathcal{C}^{\infty}(\mathbb{R}, \mathbb{R}) &\to \mathbb{R} \\ f &\mapsto f(0) \end{array}\right.$ l'application, qui a toute fonction associe sa valeur en zéro

$$
\vec{v} : \left\{ \begin{array}{ll}
 \dot{r} \\
r^{2}\dot{\theta} \\
\end{array}\right.
$$

$$
\vec{a} : \left\{ \begin{array}{ll}
\ddot{r} - r\dot{\theta}^2 \\
\cancel{ \frac{1}{r} \frac{d}{dt} (r^2 \dot{\theta}) }
\end{array}\right.
$$

Démonstration
Soit $A$ une partie non vide de $\bar{\mathbb{R}}$
- Si $A = \emptyset$, $M(\emptyset) : \bar{\mathbb{R}}$, or $\bar{\mathbb{R}}$ admet un plus petit élément, qui est $-\infty$, donc $\emptyset$ admet une borne supérieure qui est $-\infty$.
- Si $A = \{ -\infty \}$, $M(A) = \bar{\mathbb{R}}$, or, $\bar{\mathbb{R}}$ admet un ppe qui est $-\infty$ donc $A$ admet une borne supérieure qui est $-\infty$.
- Si $+\infty \in A$, $M(A) = \{ +\infty \}$, or $\{  + \infty \}$ admet un ppe qui est $+\infty$ donc $A$ admet une borne supérieure qui est $+\infty$.
- Sinon, $A \neq \emptyset$ et $+\infty \not\in A$ et $\exists a_{0} \in A \cap R$.
Posons $A_{0} = A \cap ]-\infty, a_{0}]$ et $A_{1} = A \cap [a_{0}, +\infty[$
On a donc, $A = A_{0} \cup A_{1}$.
Puisque $a_{0} \neq +\infty$ et $a_{0} \in \mathbb{R}$, $A_{1} \neq \emptyset$..


|$u_{n}$| $v_{n}$|$\lim_{ n \to \infty }(u + v)_{n}$|
|---|---|---|
|$n$|$-n+3$|$3$|


> [!important] Définition
> La primitive de $f$ qui s'annule en $a$ se note:
> $$
> \int_{a}^{x} f(t) \, dt
> $$

