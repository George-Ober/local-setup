Calculons $E^{i,j}(n,p) \times E^{k,l}(p,q)$.
Soient $(r, s) \in [ \! [ 1, n] \!] \times [ \! [ 1, q ] \!]$ fq
$$
\begin{align}
\left[ E^{i,j} \times E^{k,l} \right] _{rs}  & = \sum_{t = 1}^{n}E^{i,j}_{r,t} E^{k,l}_{t,s} \\
 & =\sum_{t = 1}^{n} \delta_{ir} \delta_{jt} \delta_{kt} \delta_{ls} \\
 & = \delta_{jk} \delta_{ir} \delta_{ls}
\end{align}
$$

Ainsi, pour le calcul de $(E^{i,j})^{2}$, $q \leftarrow n$, $p \leftarrow n$, $k \leftarrow i$, $l \leftarrow j$.
Soient $(r, s) \in [ \! [ 1, n] \!]^{2}$ fq
$$
\left[  (E^{i,j})^{2} \right]_{rs} = \delta_{ir} \delta_{js} \delta_{ij} = \left\{ 

\begin{align}
\left[   E^{i,i} \right]_{rs} \text{ si } i = j  \\
\left[ 0_{n,n} \right] _{rs} \text{ si } i \neq j
\end{align}

\right.
$$