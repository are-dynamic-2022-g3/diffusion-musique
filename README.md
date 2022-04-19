# Diffusion musique

ARE DYNAMIC 2021-2022 -- ARNOUX Constance, BAITICHE Chanez, TEBBAL Anès

## Résumé
### Version française

*Résumé de quelques lignes la méthode que vous avez suivie pour le réaliser et les résultats marquants que vous avez obtenus*

Nous nous sommes inspirés de la méthode de Naming Game pour ce projet. Dans un premier temps nous avons créé un groupe et un graphe. Nous avons ensuite déterminé les auditeurs initiaux puis nous avons simulé une dynamique de diffusion. Nous avons alors observé des résultats et enfin nous avons testé des alternatives et modifié certains paramètres. Nous avons pu constater 

Nous avons choisi de nous intéresser à la diffusion d’une musique sur YouTube au sein d’une population. Lorsqu’un artiste sort une musique, celle-ci n’est pas instantanément écoutée par tous, il y a plusieurs facteurs qui entrent en jeu. D’un côté il y a les caractéristiques de l’artiste comme son âge, sa nationalité, son sexe ou sa popularité en fonction de son nombre d’abonnés sur les réseaux sociaux. De l’autre il y a les caractéristiques du publique qui son l’âge moyen, la nationalité ou le sexe. Notre travail consistera donc à étudier la propagation d’une musique sur YouTube en fonction de son artiste et du public visé.

### English version

We chose to look at the diffusion of a music on YouTube within a population. When an artist releases a music, it is not instantly listened to by all, there are several factors that come into play. On the one hand there are the characteristics of the artist such as his age, nationality, gender or his popularity according to his number of subscribers on social networks. On the other hand there are the characteristics of the public which is the average age, the nationality or the sex. Our work will therefore consist in studying the propagation of a music on YouTube based on its artist and the targeted audience.

## Présentation de l'équipe
|( ͡° ͜ʖ ͡°)| ಠ_ಠ | (´・ω・｀) | 
|-----|--|--|
|C.Arnoux |	A. Tebbal |	C. Baitiche |

## Description synthétique du projet

**Problématique :** En quoi un.e artiste, grâce à ses musiques, est apprécié.e par un type de public particulier?

**Hypothèse principale :** La musique d'un artiste ayant beaucoup d'abonnés sur Youtube est plus diffusée que celle d'un artiste ayant moins d'abonnés.

**Hypothèses secondaires :** Plus un artiste a d'abonnés, plus le nombre d'étapes avant que le consensus ne soit atteint est grand.

**Objectifs :** Observer la diffusion d'une musique d'un.e artiste dans différents groupes d'individus.

**Critère(s) d'évaluation :** 
**Artiste:** Age, sexe, nationalite, nombre d'abonnés sur Youtube.

**Public:** Age, sexe, nationalite.

## Présentation structurée des résultats

Présentation du choix de modélisation, des outils, du code et des résultats (tableaux, courbes, animations...) (**avec une analyse critique**).

Nous avons selectionné 13 artistes qui sont sur Youtube et nous en avons fait un tableau. Pour chaque artiste nous avons repertorié leur nationnalité, leur âge, leur sexe et leur nombre d'abonnés sur Youtube. Ce tableau est trié en fonction du nombre d'abonnés sur Youtube par ordre croissant. Un artiste est ensuite tiré aléatoirement pour une expérience.

<img width="260" alt="image" src="https://user-images.githubusercontent.com/99737912/163581711-be90382e-8647-4104-b654-d91b1f49164a.png">
 Voici le tableau des artistes.

Nous avons choisi de représenter par un graphe un échantillon de population de nb_personnes qui représente les utiliseurs de Youtube. Chaque sommet correspond ainsi à une personne et les arêtes sont les liens au sein du groupe. Les étiquettes sont les identifiants de chaque individu. 

![image](https://user-images.githubusercontent.com/99737912/163725291-5c76e5c2-106d-45bc-bc56-54c5c8e2fecb.png)

Voici un exemple de graphe avec 30 individus.

Nous avons ensuite considéré que certains individus diffusent la musique de l'artiste, ce sont des "influenceurs". Les autres peuvent écouter la musique mais ils ne peuvent pas la partager avec leurs voisins. Sur le graphe, les influenceurs sont en jaune. C'est l'étape 0 du graphe.

![image](https://user-images.githubusercontent.com/99737912/163725310-e860ae21-39b7-4135-9592-8da10fb7659f.png)


En fonction du nombre d'abonnés de l'artiste, un certain nombre d'individu va écouter la musqiue. Si ces personnes sont des influenceurs, ils seront en orange, sinon ils seront en rouge. Ainsi chaque sommet orange peut partager la musique avec ses voisins. C'est l'étape 1 du graphe.

![image](https://user-images.githubusercontent.com/99737912/163725326-a33858a1-be82-430b-a343-57ddbdc5b9b4.png)


La dynamique est lancée! Les voisins des influenceurs qui n'ont pas encore écouté la musique et qui décident de suivre l'influenceur vont l'écouter : ils sont en bleu sur le graphe. C'est l'étape 2 du graphe.

![image](https://user-images.githubusercontent.com/99737912/163725333-c517fb85-9f7e-43b7-a9fc-e35c3029e420.png)

Nous allons alors repéter l'expérience plusieurs fois. Nous considérons que lorsque pour tous les influenceurs qui ont écouté la musique et que pour hacun d'eux tout leurs voisins l'ont également écouté, alors le consensus est atteint. Plus personne d'autre n'écoutera la musique. 
Nous pouvons dès lors compter le nombre d'étapes à réaliser avant d'atteindre le consensus. Nous observons des premiers résultats sur le graphe ci-dessous avec en abscisse les identifiants des artistes, triés par ordre croissant selon leur nombre d'abonnés, et en ordonné la moyenne du nombre d'étapes avant que le consensus ne soit atteint.

![image](https://user-images.githubusercontent.com/99737912/163725450-9a3579fa-fb71-47b9-a0f6-469c67ab9c2f.png)

On constate une hausse globale du nombre d'étapes mais pas de façon linéaire. D'après notre hypothèse principale, cela s'expliquerait par le fait que les artistes avec plus d'abonnés seront écoutés par plus de monde, donc la diffusion de leur musique prendra plus d'étapes. Au final, notre hypothèse secondaire est validée mais il existe plusieurs exeptions que nous remarquons sur la courbe: il y a des pics et des chutes brutales.


Nous avons par la suite refait un graphe dont l'axe des abscisses est le même que le graphe précédent. Cependant celui des ordonnés diffère, c'est la moyenne du nombre d'écoutes totales. Nous avons répété l'experience plusieurs fois et avons représenté la courbe moyenne obtenue pour tous les artistes.

![image](https://user-images.githubusercontent.com/99737912/163725410-918a6fac-666f-4de6-8570-e4b29f5603d2.png)

On remarque d'après cette courbe, et comme la précédente, que plus un artiste a d'abonnés sur Youtube, plus celui-ci sera écouté.
Notre hypothèse initiale est donc validée.


Après cela, nous avons réalisé une courbe représentant la variance du nombre d'étapes avant concensus pour chaque artiste.

![image](https://user-images.githubusercontent.com/99737912/163725415-40240d18-58a4-4d14-8a6d-06916460e172.png)

On remarque que pour un artiste de moins de 100000 abonnés la variance est presque nulle, on peut en déduire que les valeurs sont proches de la moyenne. la courbe de la variance est croissante puis décroisssante. Ce n'est donc pas le nombre d'abonnés qui définit la variance.

Pour toutes ces expériences, nous fixons certains paramètres. Voici leur valeur pour les images ci-dessus : 

<img width="570" alt="image" src="https://user-images.githubusercontent.com/99737912/163596491-81f486ba-ad62-4b43-b6d2-f66a9714dcec.png">

Si on les modifie, les résultats varient : plus nb_public est grand moins le graphe est lisible par exemple, d'où notre choix de le fixer à 30.
De plus, plus la proportion d'influenceurs est élevée et plus leur public écouteront la musique (parametres) plus la musique sera facilement diffusée dans le groupe. 
Par ailleurs, plus la proportion de liens entre les individus de nationnalités différentes est élevée plus le graphe est connecté. 



## Lien vers page de blog : <a href="blog.html"> C'est ici ! </a>

## Bibliographie :

- Wikipedia contributors. (2022, 27 mars). *Conan Gray.* Wikipédia. https://fr.wikipedia.org/wiki/Conan_Gray
- Wikipedia contributors. (2022, 9 février). *Macklemore.* Wikipédia. https://fr.wikipedia.org/wiki/Macklemore
- Wikipedia contributors. (2022, 10 avril). *Sting.* Wikipédia. https://fr.wikipedia.org/wiki/Sting
- Wikipedia contributors. (2022, 4 février). *Amy Macdonald.* Wikipédia. https://fr.wikipedia.org/wiki/Amy_Macdonald
- Wikipedia contributors. (2022, 11 avril). *Diam's.* Wikipédia. https://fr.wikipedia.org/wiki/Diam's
- Wikipedia contributors. (2022, 10 avril). *Renaud.* Wikipédia. https://fr.wikipedia.org/wiki/Renaud
- Wikipedia contributors. (2022, 9 avril). *Nena.* Wikipédia. https://fr.wikipedia.org/wiki/Nena
- Wikipedia contributors. (2022, 2 février). *Girl in red.* Wikipédia. https://fr.wikipedia.org/wiki/Girl_in_Red
- Wikipedia contributors. (2022, 21 mars). *Sen Senra.* Wikipédia. https://es.wikipedia.org/wiki/Sen_Senra
- Wikipedia contributors. (2022, 24 mars). *Ksuke.* Wikipédia. https://ja.wikipedia.org/wiki/KSUKE

**Carte mentale de vos mots-clés, en utilisant** <a href="https://framindmap.org/mindmaps/index.html">Framindmap </a> 

Liste de l'ensemble des ressources bibliographiques utilisées pour vos travaux. **<= Indiquez le canal utilisé pour les trouver (Google Scholar, sources wikipedia, ressources en ligne SU, ...)**
