>[!tip] Passage à la limite dans l'inégalité
>Soient $(u, b) \in \mathbb{R}^{\mathbb{N}}$
>
>Si $$
\left\{ \begin{array}{ll}
 \exists N \in \mathbb{N}: \forall n \in \mathbb{N}, n\geqslant N \implies u_n \geqslant 0 \\
u \text{ converge} 
\end{array}\right.$$
>
>Alors $\lim_{ n \to \infty }u_{n} \leqslant 0$.
>
>Si $$
\left\{ \begin{array}{ll}
 \exists N \in \mathbb{N}: \forall n \in \mathbb{N}, n\geqslant N \implies u_{n} \leqslant v_{n}  \\
u \text{ et } v \text{ convergent}
\end{array}\right.$$
>
>Alors $\lim_{ n \to \infty }u_{n} \leqslant \lim_{ n \to \infty } v_{n}$

Démonstration:
1. L'hypothèse $\exists N \in \mathbb{N} : \forall n \in \mathbb{N}, n \geqslant N \implies u_{n} \leqslant 0$  permet d'affifrmer que $u$ et $|u|$ coïncident à partir d'un certain rang.
Par ailleurs, la convergence de $u$ et la continuité de $|\cdot|$ sur $\mathbb{R}$ (donc en $\lim u$), donne $|u|$ converge vers $|\lim u|$.
Le caractère asymptotique de la limite permet de conclure que $u$ et $|u|$ ont la même limite.
Donc $\lim u = |\lim u| \geqslant 0$
2. $\exists N \in \mathbb{N} : \forall n \in \mathbb{N}, n\geqslant N \implies u_{n} \leqslant v_{n} \implies u_{n} - v_{n} \leqslant 0$