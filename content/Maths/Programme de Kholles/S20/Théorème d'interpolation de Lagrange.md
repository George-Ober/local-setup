
> [!Tip] Théorème d'interpolation de lagrange
> Il existe une unique solution de degré $\leqslant n$ au problème d'interpolation de lagrange, et elle s'exprime de la manière suivante
> $$L_{i} = \prod_{\substack{j=0\\j \neq i}}^{n} \frac{X - a_{j}}{a_{i} - a_{j}}$$
> $$P = \sum_{i=0}^{n}b_{i}L_{i}$$

**Démonstration**
*Unicité*
Supposons qu'il existe $(P, Q) \in \mathbb{K}_n[X]^{2}$ solutions du problème d'interpolation.

Alors $\forall i \in [ \! [ 0, n ] \!], \tilde{P}(a_{i}) = \tilde{Q}(a_{i}) = b_{i}$ 

Posons $H = P - Q$, alors, $\forall i \in [ \! [ 0, n ] \!], \tilde{H}(a_{i}) = \tilde{P}(a_{i}) - \tilde{Q}(a_{i}) = 0$.

De plus, $\deg H = \deg(P-Q) \leqslant \max \left\{ \deg P, \deg Q \right\}$

Donc $H$ est un polynôme de degré $\leqslant n$ avec $\lvert [ \! [ 0, n ] \!] \rvert = n+1$ racines.

Donc $H$ est le polynôme nul.

*Existence*
Soit $i \in [ \! [ 0, n ] \!]$ fq
Notons $L_{i}$ une solution de degré $\leqslant n$ au problème $Pb_{i}$ suivant:
$$
\left\{ \begin{array}{ll}
\tilde{P}(a_{0}) = 0 \\
\vdots \\
\tilde{P}(a_{i-1}) = 0 \\
\tilde{P}(a_{i}) = 1 \\
\tilde{P}(a_{n}) = 0 \\
\vdots \\
\tilde{P}(a_{n}) = 0
\end{array} \right.
$$
On remarque que $(a_{0},\dots ,a_{i-1}, a_{i+1},\dots, a_{n})$ sont $n$ racines deux à deux distinctes de $L_{i}$. Or $L_{i}$ est de degré $\leqslant n$ et n'est pas le polynôme nul (car $\tilde{L_{i}}(a_{i}) = 0$) donc $(a_{0},\dots ,a_{i-1}, a_{i+1},\dots, a_{n})$ sont les *seules* racines de $L_{i}$.

Dès lors, 
$$
\exists c \in \mathbb{K}^{*} : L_{i} = c\prod_{\substack{j=0 \\ j\neq i}} ^{n}(X-a_{j})
$$
Pour trouver le $c$, remarquons que
$$
\begin{align*}
\tilde{L_{i}}(a_{i}) = 1 &\iff c\prod_{\substack{j=0 \\ j\neq i}} ^{n}(a_{i}-a_{j}) = 1\\
&\iff c = \prod_{\substack{j=0 \\ j\neq i}} ^{n}\left( \frac{1}{a_{i}-a_{j}} \right)
\end{align*}
$$
Ainsi, s'il existe une solution au problème $Pb_{i}$ c'est nécéssairement
$$L_{i} = \prod_{\substack{j=0 \\ j\neq i}} ^{n}\left( \frac{{X-a_{j}}}{a_{i}-a_{j}} \right)$$

Réciproquement, cette solution est correcte puisque
$$\forall k \in [ \! [ 0, n ] \!], k \neq i,  \tilde{L_{i}}(a_{k}) = \prod_{\substack{j=0 \\ j\neq i}} ^{n}\left( \frac{{\overbrace{ a_{k}-a_{j} }^{ =0 }}}{a_{i}-a_{j}} \right) = 0$$
Et
$$\tilde{L_{i}}(a_{i}) = \prod_{\substack{j=0 \\ j\neq i}} ^{n}\left( \frac{{a_{i}-a_{j}}}{a_{i}-a_{j}} \right) = \prod_{\substack{j=0 \\ j\neq i}} ^{n} 1 = 1$$.

Posons donc $P = \sum_{i=0} ^{n} b_{i}Li$.

Alors, par construction,
$$
\forall k \in [ \! [ 0, n ] \!], \tilde{P}(a_{k}) = \sum_{i=0} ^{n}\left(  b_{i} \prod_{\substack{j=0 \\ j\neq i}} ^{n}\left( \frac{{a_{k}-a_{j}}}{a_{i}-a_{j}} \right) \right) = \sum_{i=0} ^{n}\left(  b_{i} \delta_{ki} \right) = b_{k} \delta_{kk} = b_{k}
$$
Nous avons donc construit une solution unique au problème d'interpolation de Lagrange