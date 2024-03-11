Un pendule pesant est un solide de masse $m$ de forme quelconque mobile dans le champ de
 pesanteur terrestre autour d'un axe horizontal fixe ne passant pas par son centre de gravité $G$.

 On note $(O_{z})$ l'axe de rotation du solide, $G$ son centre de gravité et $J_{(O_z)}$ son moment d'inertie
 par rapport l'axe $(Oz)$. On repère la position du solide par l'angle $\theta$ que fait la droite $(OG)$ avec la verticale descendante $(Ox).$ On suppose que la liaison entre le solide et le référentiel terrestre est une liaison pivot parfaite d'axe $(Oz)$. Le solide est soumis à :

 - l'action exercée par la liaison pivot. On suppose cette
 liaison pivot idéale, ce qui implique que son moment par rapport àl'axe $(Oz)$ est nul'

- son poids vertical descendant qui s'applique au centre de gravité $G$. Son moment par rapport à $(Oz)$ est égal en module au produit $mg\times L$ où $L= d\sin \theta$ est le bras de levier représenté sur la figure 19.8. Cette force tend à ramener le pendule vers sa position d'équilibre. Le signe de son moment par rapportà $(Oz)$ est opposé à celui de $\sin\theta$. En effet, on voit sur la figure 19.8 que $\theta>0$, $\sin\theta>0$ et $\mathscr{M}_{(Oz)}<0$. Au final :

$$\mathcal{M}_{(Oz)}=-mgd\sin\theta.$$


On applique au solide la loi du moment cinétique par rapport àl'axe orienté $(O_{z})$ fixe dans le référentiel terrestre $\mathscr{R}$ supposé galiléen :

 $$\frac{\mathrm{d}L_{(O_{z})}}{\mathrm{d}t}=-mgd\sin\theta$$
Le moment cinétique de la barre est égal $L_{(Oz)}=J_{(Oz)}\dot{\theta}$ donc $\frac{\mathrm{d}L_{(Oz)}}{\mathrm{d}t}=J_{(Oz)}\ddot{\theta}.$ On injecte alors cette relation dans l'équation pour obtenir :

 
$$
J_{(Oz)}\ddot{\theta}=-mgd\sin\theta \iff \ddot{\theta}+\frac{mgd}{J_{(Oz)}}\sin\theta=0.
$$

Cette équation est du type $\ddot{\theta}+\omega_0^2\sin\theta=0$ avec $\omega_0=\sqrt{\frac{mgd}{J_{(oz)}}}$.Il s'agit de la même équation que celle que l'on a obtenue lors de l'étude du pendule simple.
 Les positions d'équilibre $\theta_{\mathrm{eq}_1}=0$ et $\theta_{\mathrm{eq}_2}=\pi$ permettent au moment du poids par rapport à
 $(O_{7})$ d'être égal à 0. Dans ces positions, la somme des moments des forces qui s'appliquent au pendule est nulle. On remarque que dans ce cas, le centre de gravité est sur une droite verticale partant du point d'attache $O$. En pratique, seule la position $\theta_{\mathrm{eq}_1}=0$ est réalisable car c'est la seule qui est stable.

>[!quote] Remarque
>On met en évidence une méthode qui permet de repérer expérimentalement la position du centre de gravité d'un solide. Si l'on utilise un autre point d'attache, on trouve une autre droite verticale. Le centre de gravité est alors à l'intersection des deux droites et on peut déterminer la distance $d.$

Lorsque les oscillations sont de faible amplitude au voisinage de la position d'équilibre
 $\theta_\mathrm{eq}=0,\sin\theta\simeq\theta$ et l'équation peut être linéarisée :

$$
\ddot{\theta}+\omega_0^2\theta=0\quad\mathrm{~ou~}\quad\omega_0=\sqrt{\frac{mgd}{J_{(Oz)}}}.
$$

On reconnaît une équation d'oscillateur harmonique dont les solutions sont des sinusoïdes de pulsation $\omega_0:$

$$
\theta(t)=\theta_m\cos\left(\omega_0t+\varphi_0\right).
$$

$\theta_m$ et $\varphi_0$ sont des constantes d'intégration que l'on détermine à partir des conditions initiales.
Étant donné que le solide oscille autour d'une position d'équilibre stable, il est normal de trouver des oscillations harmoniques pour les petites oscillations autour de cette position Ces oscillations présentent la propriété remarquable d'avoir une période indépendante de l'amplitude (isochronisme des petites oscillations). La mesure de cette période permet de déterminer la valeur de $J_{(Oz)}$, connaissant la position du centre de gravité, la masse du solide et la valeur de l'accélération de pesanteur.

