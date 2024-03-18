
On considère un pendule pesant constitué d'un barreau fin et homogène de longueur $L$ et de masse $M$, relié à un bâti fixe par une liaison pivot d'axe $(Oz).$ On donne son moment d'inertie par rapport à $(Oz):$
$$
J_{(Oz)} = \frac{ML^{2}}{3}
$$
On note $\theta$ l'angle que fait le barreau avec la verticale descendante et on lâche le barreau sans vitesse initiale d'une position repérée par l'angle $\theta_0\simeq\pi.$
 1. Représenter le dispositif.
 2. Déterminer l'équation du mouvement.
 3. En déduire une intégrale première du mouvement.
 4. Rappeler les vecteurs position, vitesse et accélération du centre de gravité du barreau dans
 une base adaptée au problème. En déduire l'expression de l'accélération en fonction de $\theta,L$, $m$ et $g.$

 5. En déduire la force exercée par le bâtit sur le barreau au niveau de la liaison pivot.
 6. Conclure quant-à l'action mécanique de la liaison pivot.


## Solution
1. Le dispositif est représenté ci-dessous.
2. On étudie le mouvement du pendule dans le référentiel lié au bâti supposé galiléen. Le pendule est soumis à :
	- l'action du poids qui s'applique en $G$ (situé au milieu de la barre) et dont le moment par rapport à $Oz$ vaut :

		$$
		M_{Oz}=-Mg\times b=-Mg\frac L2\sin\theta,
		$$
		où $b=\frac L2\sin\theta$ est le bras de levier du poids dessiné sur la figure. On détermine le signe sur la figure en observant que le poids tend àramener le pendule vers la position $\theta=0$ donc exerce un couple négatif lorsque $\sin\theta>0.$
	
	- l'action de la liaison pivot d'axe $Oz$ dont le moment par rapport à $Oz$ est nul; - l'action de l'air que l'on néglige.
	 On applique le théorème du moment cinétique par rapport àl'axe $Oz$ fixe :
	
	$$
	J_{(Oz)}\ddot{\theta}=M_{Oz}\quad\Longrightarrow\quad\frac{ML^2}3\ddot{\theta}=-Mg\frac L2\sin\theta\quad\Longrightarrow\quad\ddot{\theta}+\frac{3g}{2L}\sin\theta=0.
	$$


3. On multiplie l'équation précédente par $\dot{\theta}$ et on l'intègre par rapport au temps et on obtient :
	
	$$
	\frac12\dot{\theta}^2-\frac{3g}{2L}\cos\theta=\mathrm{constante}.
	$$
	 À l'instant initial, cette équation devient :
	
	$$
	0-\frac{3g}{2L}\cos(\theta_0)=\mathrm{constante}\simeq-\frac{3g}{2L}\cos(\pi)=\frac{3g}{2L},
	$$
	
	ce qui donne la valeur de la constante d'intégration et au final permet de trouver une intégrale première du mouvement :
	
	$$
	\dot{\theta}^2-\frac{3g}L\cos\theta=\frac{3g}L.
	$$
	![[316cf7dede42d48704098b89830c8954_MD5.jpeg|200]]

4. Le centre de gravité décrit un mouvement circulaire de centre $O$ et de rayon $\frac L2$. Il est repéré en polaire par sa coordonnée angulaire $\theta$ de sorte que sur la base $(\overrightarrow{u_r},\overrightarrow{u_\theta}):$
	$$
	\left.\overrightarrow{OG}=\left(\begin{array}{c}\frac L2\\0\end{array}\right.\right);\quad\overrightarrow{v}=\left(\begin{array}{c}0\\\frac L2\dot{\theta}\end{array}\right);\quad\overrightarrow{a}=\left(\begin{array}{c}-\frac L2\dot{\theta}^2\\\frac L2\ddot{\theta}\end{array}\right).
	$$
 
	On peut écrire son accélération en fonction de $\theta$ en exprimant $\dot{\theta}^{2}$ et $\ddot{\theta}$ àl'aide des expressions trouvées aux questions précédentes :
	
	$$
	\overrightarrow{a}=-\frac L2\dot{\theta}^2\overrightarrow{u}_r+\frac L2\ddot{\theta}\overrightarrow{u}_\theta=-\frac L2\frac{3g}L\left(\cos\theta+1\right)\overrightarrow{u}_r-\frac L2\frac{3g}{2L}\sin\theta\overrightarrow{u}_\theta 
	$$
	 $=-\frac{3g}{4}\left(2\left(\cos\theta+1\right)\overrightarrow{u_r}+\sin\theta\overrightarrow{u_\theta}\right)$

5. Le principe fondamental de la dynamique appliquée à $G$ soumis à son poids età la force exercée par la liaison pivot donne :

	$$
	M\overrightarrow{a}=M\overrightarrow{g}+\overrightarrow{F}_{\mathrm{pivot}}\quad\Longrightarrow\quad\overrightarrow{F}_{\mathrm{pivot}}=M\overrightarrow{a}-M\overrightarrow{g}=M\overrightarrow{a}-Mg\left(\cos\theta\overrightarrow{u}_r-\sin\theta\overrightarrow{u}\overrightarrow{\theta}\right).
	$$
	 Finalement :
	
	$$
	\begin{aligned}
	\overrightarrow{F}_{\mathrm{pivot}}& =-\frac{3\boldsymbol{M}\boldsymbol{g}}4{\left(2\left(\cos\theta+1\right)\overrightarrow{u}_r+\sin\theta\overrightarrow{u}_\theta\right)}-\boldsymbol{M}\boldsymbol{g} \\
	&=-Mg\left(\left(\frac52\cos\theta+\frac32\right)\overrightarrow{u_r}-\frac14\sin\theta\overrightarrow{u_\theta}\right).
	\end{aligned}
	$$

6. La liaison pivot a une action mécanique complexe qui permet de maintenir la barre en rotation d'axe $Oz$. Sa résultante a une expression compliquée et impossible à connaître *à priori*. La seule chose que l'on peut dire sans hésiter est que son moment d'axe $Oz$ est nul lorsque qu'elle est idéale.

