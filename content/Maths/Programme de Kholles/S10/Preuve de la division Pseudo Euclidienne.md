
**Unicité**
Soient $((q, r), (q', r')) \in (\mathbb{R}_{+} \times \mathbb{Z})^2$ fq
Alors, 
$$
\left\{
\begin{array}{ll}
x = a q + r \\
r \in [0, a[
\end{array}
\right.

\text{ et }

\left\{
\begin{array}{ll}
x = a q' + r' \\
r' \in [0, a[
\end{array}
\right.
$$

Ainsi
$$
\begin{align}
a(q-q') &= r' - r \\
a |q-q'| &= |r' - r| \\
\underbrace{ |q-q'| }_{ \in \mathbb{N} } &= \frac{|r' - r|}{a}
\end{align}
$$
D'où, selon l'encadrement:
$$
\left\{
\begin{array}{ll}
0 \leqslant r' < a \\
-a > -r \leqslant 0
\end{array}
\right.
\implies |r'-r| < a
\implies \frac{|r' - r|}{a}<1
\implies \frac{|r' - r|}{a} = 0
$$
Donc $|q - q'| = 0$, d'où $q = q'$ et $r = r'$.

**Existence**
Posons $E = \left\{ q \in \mathbb{Z} | aq \leqslant x \right\}$
- C'est une partie de $\mathbb{Z}$
- Non vide, car
	- Si $x \geqslant 0, 0 \in E$
	- Sinon, si $x<0$
		- Utilisons le caractère archimédien de $\mathbb{R}$ pour:$\left\{ \begin{align}a \leftarrow a \\y \leftarrow x \end{align}\right.$
			- Alors $\exists n \in \mathbb{N}:na>|x|$ fixons un tel $n$
		- Alors $na > |n|  \implies na > -x \implies -na > x \implies -n \in E$
- Majorée
	- Utilisons de nouveau le caractère archimédien de $\mathbb{R}$ pour $\left\{ \begin{align}a \leftarrow a \\y \leftarrow x \end{align}\right.$
		- Alors $\exists n \in \mathbb{N} : na > |x|$
	- Montrons que $n$ majore $E$. Soit $q \in E$ fq.
$$
\begin{align}
&qa \leqslant x \leqslant |x| &< na \\
\text{donc } &q &< n \\
\text{donc } q \leqslant n
\end{align}
$$
E admet donc un pgE, $q_{x} = \max E$, posons donc $r_{x} = x - q_{x}a$
Par construction, $q_{x} \in \mathbb{Z}, n_{x} \in \mathbb{R}$
De plus, $x = q_{x}a +r_{x}$
$$
\left\{ \begin{align}
q_{x}\in E \implies q_{x}a \leqslant x \implies 0 \leqslant x - q_{x}a = r_{x}  \\
x_{x} = \max E \implies q_{x} + 1 \not\in E &\implies (q_{x}+1)a > x \\
 &\implies a > x-q_{x}a \\
&\implies a>r_{x}
\end{align}
\right.
$$

Soient $x \in \mathbb{R}$ et $a \in \mathbb{R}_{+}^*$
$$
\exists ! (q, r) \in \mathbb{Z} \times \mathbb{ R} : \left\{ \begin{align}
x = aq + r \\
r \in [0, a[
\end{align} \right.
$$
