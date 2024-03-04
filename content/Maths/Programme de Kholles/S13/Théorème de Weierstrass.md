>[!tip] Théorème de Weierstraß
>L'image d'un segment par une fonction continue sur ce segment est un segment
>Soient $(a, b) \in \mathbb{R}^2$ tels que $a < b$ et $f: [a, b] \to \mathbb{R}$
>Si $f \in \mathcal{C}^0([a, b], \mathbb{R})$ alors $\exists (x_{1}, x_{2}) \in \mathbb{R}^2 : f([a, b]) = [f(x_{1}), f(x_{2})]$

Démonstration

**Étape 1:** Montrons que $f([a, b])$ est majoré
Par l'absurde, supposons que $f([a, b])$ n'est pas majoré
Alors $\forall A \in \mathbb{R}, \exists x \in [a, b] : f(x) > A$  (\*)
Soit $n \in \mathbb{N}$ fq.
Appliquons (\*) pour $A \leftarrow n$:
$\exists x \in [a, b] : f(x) > n$, et fixons un tel $x$ que l'on note $x_{n}$
Nous venons de créer la suite $(x_{n})_{n \in \mathbb{N}} \in [a, b]^{\mathbb{N}}$ qui vérifie:
$$
\left. 
\begin{align}
\forall n \in \mathbb{N}, f(x_{n}) \geqslant n \\
\lim_{ n \to \infty } n =  +\infty
\end{align}
\right\} \underbrace{ \implies }_{ \text{théorème de divergence par minoration} } f(x_{n}) \xrightarrow[n \to +\infty]{} + \infty
$$

$(x_{n})_{n \in \mathbb{N}}$ est bornée (à valeurs dans $[a, b]$ donc, selon le théorème de Bolzanno-Weierstraß)
$$
\exists \ell \in \mathbb{R} : \exists \varphi : \mathbb{N} \to \mathbb{N} : \text{strict. croissante tel que } (x_{\varphi(n)})_{n \in \mathbb{N}} \text{ tend vers } \ell
$$
Donc, en passant à la limite : $\forall n \in \mathbb{N}, a \leqslant x_{\varphi(n)} \leqslant b \implies a \leqslant \ell \leqslant b \implies \ell \in [a, b]$

Par continuité de $f$ sur $[a, b]$, donc en $\ell$, $(f(x_{\varphi(n)}))_{n \in \mathbb{N}}$ converge vers $f(\ell)$.

Or $$
\left\{ \begin{array}{ll}
 (f(x_{\varphi(n)}))_{n \in \mathbb{N}} \text{ est une sous suite de } (f(x_{n}))_{n \in \mathbb{N}} \\
f(x_{n}) \xrightarrow[n \to + \infty]{} + \infty
\end{array}\right.$$

donc $(f(x_{\varphi(n)}))_{n \in \mathbb{N}}$, tend vers $+ \infty$, ce qui est absurde, donc $f$ est majorée.
On fait de même pour la minoration.

**Étape 2:** Montrons que $f([a, b])$ admet un pge et un ppe.
Montrons donc que $f([a, b])$ admet une borne sup, qui, puisque c'est une valeur atteinte, deviendra un max.
$$
f([a, b]) \text{ est } \left\{ \begin{array}{ll}
 \text{ une partie de } \mathbb{R} \\
\text{ non vide car contient } f(a) \\
\text{majorée d'après l'étape 1}
\end{array}\right.
$$
$f([a, b])$ admet donc une borne supérieure $\sigma$.
Appliquons la caractérisation séquentielle de la borne supérieure:
$$
\exists (y_{n})_{n \in \mathbb{N}}, \in f([a, b])^{\mathbb{N}} : (y_{n}) \text{ converge vers } \sigma
$$
$$
\forall n \in \mathbb{N}, y_{n} \in f([a, b]) \implies \exists x_{n} \in [a, b] : f(x_{n} ) = y_{n}
$$
Fixons un tel $x_{n}$ pour tout $y_{n}$.
On a donc construit $(x_{n})_{n \in \mathbb{N}} \in [a, b]^{\mathbb{N}} : f(x_{n}) \xrightarrow[n \to +\infty]{} \sigma$
De plus, $(x_{n})$ est bornée (à valeurs dans $[a, b]$) donc, selon le théorème de Bolzanno Weierstrasß:
$$
\exists \ell \in \mathbb{R} : \exists \varphi : \mathbb{N} \to \mathbb{N} : \text{strict. croissante tel que } (x_{\varphi(n)})_{n \in \mathbb{N}} \text{ tend vers } \ell
$$
Donc, en passant à la limite : $\forall n \in \mathbb{N}, a \leqslant x_{\varphi(n)} \leqslant b \implies a \leqslant \ell \leqslant b \implies \ell \in [a, b]$

Par continuité de $f$ sur $[a, b]$, donc en $\ell$, $(f(x_{\varphi(n)}))_{n \in \mathbb{N}}$ converge vers $f(\ell)$.
Or,
$$
\left\{ \begin{array}{ll}
 (f(x_{\varphi(n)}))_{n \in \mathbb{N}} \text{ est une sous suite de } (f(x_{n}))_{n \in \mathbb{N}} \\
f(x_{n}) \xrightarrow[n \to + \infty]{} \sigma
\end{array}\right.
$$
Par unicité de la limite, $\sigma = f(\ell)$.
On montre de même qu'il existe $\ell' \in [a, b]: f(\ell') = \inf f([a, b])$
Ainsi, $f(\ell) = \max f([a, b])$ et $f(\ell') = \min f([a, b])$

**Étape 3:**
Montrons que $f([a, b]) = [f(\ell'), f(\ell)]$.
Par la construction précédente, $\forall y \in f([a, b]), y \in [f(\ell'), f(\ell)]$.
Ainsi, $f([a, b]) \subset [f(\ell'), f(\ell)]$.

Réciproquement, l'image par la fonction continue $f$ du segment $[a, b]$ qui est un intervalle est un intervalle:
$$
\left. 
\begin{align}
f([a,b]) \text{ est un intevalle} \\
f(\ell) \in f([a, b]) \\
f(\ell') \in f([a, b])
\end{align}
\right\} 
\implies
[f(\ell'), f(\ell)] \subset f([a,b])
$$
D'où $[f(\ell'), f(\ell)] = f([a,b])$

