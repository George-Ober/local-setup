>[!quote] Définition
>En coordonnées cylindriques d'axe $Oz$, on définit le **moment d'inertie** par rapport à l'axe $Oz$ d'un point $M$ de coordonnées $(r, \theta, z)$
>
>$$J_{(Oz)}(M) = mr^{2} \implies L_{(Oz)} = J_{(Oz)}(M) \dot{\theta}$$


>[!tip] Théorème scalaire du moment cinétique pour un solide
>Dans un référentiel $\mathscr R$ galiléen, pour un solide en rotation autour d'un axe fixe
>
>$$J_{(Oz)} \ddot{\theta} = \sum_{i}\mathcal{M}_{(Oz)}(\vec{f_{i}})$$

### Énergie cinétique d'un solide en rotation
On modélise le solide par un ensemble de points matériels $M_i$ de masse $m_i$ repérés en co-ordonnées cylindriques d'axe $(O_{z}):M_i(r_i,\theta_i,z_i).$ On a vu au paragraphe 3.2 que le moment d'inertie du solide par rapport à $(O_z)$ vaut alors $J_{(O_{z})}=\sum_im_ir_i^2$. Par ailleurs, on a vu dans le chapitre Cinématique $du$ solide qu'un point $M_i$ quelconque du solide est en mouvement circulaire de rayon $r_i$ à la vitesse angulaire commune $\dot{\theta}$. Sa vitesse est donc $\overrightarrow{\nu_i}=r_i\dot{\theta}\overrightarrow{u_{\theta_i}}$ et son énergie cinétique $E_c(M_i)=\frac12m_i\nu_i^2=\frac12m_ir_i^2\dot{\theta}^2.$

 L'énergie cinétique du solide est obtenue par sommation de l'énergie cinétique de chacun des
 points qui le constituent :

$$
E_c=\sum_iE_c(M_i)=\sum_i\frac12m_ir_i^2\dot{\theta}^2=\frac12\left(\sum_im_ir_i^2\right)\dot{\theta}^2,
$$
 où on reconnaît l'expression du moment d'inertie du solide $:J_{(o_z)}=\sum_im_ir_i^2.$
 
 >[!tip] Un solide de moment d'inertie $J_{(Oz)}$ en rotation autour d'un axe fixe $(O_{z})$ à la vitesse angulaire $\dot{\theta}$ possède l'énergie cinétique :
 >$$E_c=\frac12J_{(Oz)}\dot{\theta}^2.$$

C'est bien l'énergie cinétique que l'on a trouvée au paragraphe 8 lors de la détermination de l'intégrale première du mouvement. Il s'agissait alors d'un cas particulier de la loi de l'énergie cinétique pour un solide en rotation que l'on va établir dans le paragraphe suivant.
Remarque On peut mémoriser l'expression de l'énergie cinétique d'un solide en rotation autour de l'axe $(O_{z})$ à partir de celle, bien connue, d'un solide en translation rectiligne sur l'axe $(O_{x}):E_c=\frac12m\dot{x}^2$. Il suffit de remplacer la masse par le moment d'inertie et la vitesse linéaire par la vitesse angulaire.

![[Puissance d'une force appliquée à un solide en rotation]]

![[Pendule pesant]]