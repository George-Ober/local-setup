>[!tip] Théorème: Caractérisation des (ERH1)
>L'ensemble des solutions de l'équation $\forall n \in \mathbb{N}, u_{n+1} = au_{n}$
>Est la droite vectorielle des suites géométriques de raison $a$
>
>$$\left\{ \left( \lambda a^n \right) _{n \in \mathbb{N}} \mid \lambda \in \mathbb{K} \right\} = \text{Vect}\left\{ (a^n)_{n \in \mathbb{N}} \right\}$$

Démonstration:
Notons $\mathcal{S}$ l'ensemble des solutions
Soit $u \in \mathcal{S}$ fq.
$$
\begin{align}
\forall n \in \mathbb{N}, u_{n+1} = au_{n} &\implies \forall n \in \mathbb{N}, u_{n} = a^nu_{0} \\
 & \implies u = u_{0} \left( a^n \right) _{n \in \mathbb{N}} \\
 & \implies u \in \text{Vect}\left\{ (a^n)_{n \in \mathbb{N}} \right\} 
\end{align}
$$
Réciproquement, l'ensemble des suites géométriques de raison $a$ est solution de l'équation homogène.

>[!tip] Théorème: Résolution avec second membre
>L'ensemble des solutions de l'équation $\forall n \in \mathbb{N}, u_{n+1} = au_{n} + v_{n}$
>Est la droite affine $$\left\{ w + \lambda \left( a^n \right) _{n \in \mathbb{N}} \mid \lambda \in \mathbb{K} \right\}$$

Posons $w$ la suite définie par $$\left\{ \begin{array}{ll}
 w_{0} = 1 \\
\forall n \in \mathbb{N}, w_{n+1} = aw_{n} + v_{n} 
\end{array}\right.$$

$w$ est "évidemment solution de particulière de l'équation"

> Maintenant que nous disposons d'une solution particulière, et ayant observé que l'équation est linéaire, mettons en œuvre l'artillerie classique pour exprimer l'ensemble des solutions par l'habituelle technique.

$$
\begin{align}
\forall n \in \mathbb{N}, u_{n+1} = au_{n} + v_{n} & \iff \forall n \in \mathbb{N}, u_{n+1} - au_{n} = v_{n} \\
 & \iff \forall n \in \mathbb{N}, u_{n+1} - au_{n} = w_{n+1} - aw_{n} \\
 & \iff \forall n \in \mathbb{N}, (u-w)_{n+1} = a(u-w)_{n} \\
& \iff u-w \in \text{Vect}\left\{ \left( a^n \right) _{n \in \mathbb{N}} \right\}  \\
	 & \iff \exists \lambda \in \mathbb{K} : u-w = \lambda \left( a^{n} \right) _{n \in \mathbb{N}} \\
 & \iff \exists \lambda \in \mathbb{K} : \forall n \in \mathbb{N}, u_{n} = w_{n} + \lambda a^n \\
 & \iff  u \in \left\{ \left( w_{n} + \lambda a^n \right) _{n \in \mathbb{N}} \mid \lambda \in \mathbb{K} \right\} 
\end{align}
$$


