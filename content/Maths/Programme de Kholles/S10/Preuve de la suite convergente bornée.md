Soit $u \in \mathbb{K}^{\mathbb{N}}$ convergente.
Posons $\ell = \lim u$
Appliquons la définition de la convergence pour $\varepsilon \leftarrow 1$
$$
\exists N_{1}\in \mathbb{N}: \forall n \in \mathbb{N}, n \geqslant N_{1} \implies |u_{n}-\ell| \leqslant 1
$$
Fixons un tel $N_{1}$
Posons alors $M = \max\left\{ |u_{0}|, |u_{1}|, |u_{2}| \dots |u_{N_{1}}|, |\ell|+1 \right\}$, qui est bien défini, car toute partie finie, non vide d'un ensemble totalement ordonné (ici $(\mathbb{R}, \leqslant)$) admet un pgE.

Soit $n \in \mathbb{N}$ fq.
	- Si $n \in [[0, N_{1}]], |u_{n}| \in \left\{ |u_{0}|, |u_{1}|, |u_{2}| \dots |u_{N_{1}}|, |\ell|+1 \right\}$ donc $|u_{n}| \leqslant M$
	- Sinon, 
$$
\begin{align}
n> N_{1} &\implies |u_{n} - \ell| \leqslant 1 \\
&\implies |u_{n}| - |\ell| \leqslant 1 \\
 & \implies |u_{n}| \leqslant 1+ |\ell| \leqslant M
\end{align}
$$
Ainsi, $\forall n \in \mathbb{N}, |u_{n}| \leqslant M$. 


Caractérisation séquentielle de la borne $\sup A$

$$
\sigma = \sup A \iff \left\{ 
\begin{array}{ll}
\sigma \text{ majore } A \\
\exists (a_{n})\in A^{\mathbb{N}} : (a_{n}) \text{ converge vers } \sigma
\end{array}
\right.
$$

Définition du caractère archimédien
$$
\forall a \in \mathbb{R}_{+}^*, \forall y \in \mathbb{R}, \exists n \in \mathbb{ N}:na > |y|
$$


Soient, $(A, B) \in \mathcal{P}(\mathbb{R})^2$ fq. A est dense dans b ssi
$$
\left\{ \begin{align}
 A \subset B \\
\forall (u, v) \in \mathbb{ R}^2, B \cap]u, v[ \neq \emptyset \implies A \cap ]u, v[ \neq \emptyset
\end{align} \right.
$$

$$
\text{A dense dans B} \iff \left\{ 
\begin{array}{ll}
A \subset B \\
\forall b \in B, \forall \varepsilon \in \mathbb{R}_{+}^*, \exists a \in A : (a_{n}) | b-a| < \varepsilon
\end{array}
\right.
$$

Soit $u \in \mathbb{K}^{\mathbb{N}}$ fq.
U converge vers $\ell$ si

$$\forall \varepsilon \in \mathbb{R}_{+}^*, \exists N \in \mathbb{ N}, n \geqslant N \implies | u_{n} - \ell| < \varepsilon$$

$$
\forall \alpha \in ]0,1[, \exists N \in \mathbb{N}: n\geqslant N \implies |1-\alpha||\ell|\leqslant |u_{n}| \leqslant |1+\alpha|
$$

$$
\forall (x, y) \in C^2, x < y \implies [x, y] \subset C
$$


