

>[!tip] Symétrie des diviseurs d'un entier non nul
>Soit $a \in \mathbb{Z}^{*}$
>$\mathcal{D}(a) = \mathcal{D} (-a) = \mathcal{D} (\lvert a \rvert ) \text{ et }\forall d \in \mathcal{D}(a), -d \in \mathcal{D}(a)$



$$
\mathcal{D}(a) \subset [ \! [ -\lvert a \rvert , \lvert a \rvert ] \!]
$$

$$
\begin{array}{l}
 (i)  & \forall d \in \mathbb{Z}, a \mid b  & \implies b \mid d \\
(ii)  & \forall d \in \mathbb{Z}^{*}, ad \mid bd  & \implies a \mid d \\
(iii)  & \forall (d, u, v) \in \mathbb{Z}^{3}\left. \begin{array}{ll}
d \mid a \\
d \mid b
\end{array}
\right\}  & \implies d \mid ua+vb
\end{array}
$$


$$
\begin{array}{ll}
(i) & \forall a \in \mathbb{Z}, a \wedge 0 = \lvert a \rvert  \\
(ii) & \forall a \in \mathbb{Z}, a \wedge 1 = 1
\end{array}
$$


Soient $(a, b) \in \mathbb{Z}^{2}$ tels que $a \mid b$

Alors $a \wedge b = \lvert a \rvert$

>[!tip] Lemme d'Euclide
>Soient $(a, b,c, d) \in \mathbb{Z}^{4}$ tels que $a = bc+d$
>Alors:
>$\mathcal{D}(a) \cap \mathcal{D}(b) = \mathcal{D}(b) \cap \mathcal{D}(d)$
>$a \wedge b = b \wedge d$


>[!tip] Proposition 2.23 : Diviseurs du PGCD
>Soient $(a, b) \in \mathbb{Z}^{2}$. Alors $\mathcal{D(a\wedge b) = \mathcal{D}(a) \cap \mathcal{ D} (b)}$


>[!tip] Lemme 2.6 : Égalités de PGCD
>Soient $(m, M) \in \mathbb{Z}^{2}$. Alors $$m \wedge M = m \wedge (M - m)$$






Caractérisation du pgcd

$$
\left[ \forall n \in \mathbb{Z}, n \mid a \text{ et } n \mid b \iff n \mid d \right]  \iff a \wedge b = d
$$

$$
a\mathbb{Z} \cap b\mathbb{Z} = (a \vee b)\mathbb{Z}
$$

$$
\left[ \forall n \in \mathbb{Z}, a \mid n \text{ et } b \mid n \iff d \mid n \right]  \iff a \vee b = d
$$


$$
p \in \mathcal{P}, \forall k \in [ \! [ 1, p-1] \!], p \mid \binom{p}{k}
$$
$m \in \mathbb{N}^{*}, (a_{1}, a_{2}, a_{3}, \dots a_{m}) \in \mathbb{Z}^{m}$

$$
p \mid \prod_{i = 1}^{m} a_{i} \iff \exists i_{0} \in [ \! [1, m ] \!]: p \mid a_{i_{0}}
$$

>[!tip] Propriété: critère de primalité
>Soit $n \in \mathbb{N}^{*}$ tq $n \geqslant 2$
>$$n \in \mathcal{P} \iff \text{ aucun diviseur dans } [ \! [ 2, \lfloor \sqrt{ x } \rfloor] \!]$$

>[!tip] Caractérisation de la valuation p-adique de $n \in \mathbb{Z}^{*}$
>$$\nu_{p}(n) = k_{0} \iff \exists m \in \mathbb{Z} : \left\{ \begin{array}{\ll} n = p^{k_{0}}m \\ m \wedge p =1\end{array} \right.$$

>[!tip] Définition Famille propre nulle
>Une famille propre nulle d'entiers naturels indexés par les nombres remiers est une application 
>$\alpha:\left|\begin{array}{ll} \mathcal{P} &\to \mathbb{N} \\ p &\mapsto \alpha_{p} \end{array}\right.$
>Notée comme une famille de valeurs $(\alpha_{p})_{p \in \mathcal{P}}$ qui a la propriété que $\left\{ p \in \mathcal{P} \mid \alpha_{p} \neq 0 \right\}$ est fini.
>Elle a un nombre fini de termes non nuls.
>Pour une telle famille, on peut donc définir, en notant $(p_{1}, \dots p_{N})$ les nombres tels que
>$$\left\{ p_{1}, \dots p_{N} \right\} \neq \left\{ p \in \mathcal{P} \mid \alpha_{p} \neq 0 \right\}$$
>On définit $$\prod_{p \in \mathcal{P}} p ^{\alpha_{p}} = \prod_{i=1}^{N} p_{i} ^{a_{i}}$$


>[!tip] Décomposition en facteurs premiers
>Soit $n \in \mathbb{Z}^{*}$ alors $(\nu_{p}(n))_{p \in \mathcal{P}}$ est une famille presque nulle d'entiers naturels indexés par l'ensemble $\mathcal{ P}$ des nombres premiers.
>$$n = \varepsilon \prod_{p \in \mathcal{P}} p ^{\nu_{p}(n)}$$
>De plus $(\nu_{p}(n))_{p \in \mathcal{P}}$ est l'unique famille presque nulle vérifiant cette relation