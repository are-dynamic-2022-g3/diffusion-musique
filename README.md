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

**Hypothèses secondaires :** Le public d'un.e artiste possède généralement des caractères en communs tels que l'âge, la nationalité ou encore le sexe.

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

<img width="289" alt="image" src="https://user-images.githubusercontent.com/99737912/163580743-9583fbbc-0bc5-4c98-a1ec-0266cf2c7036.png">

Voici un exemple de graphe avec 30 individus.

Nous avons ensuite considéré que certains individus diffusent la musique de l'artiste, ce sont des "influenceurs". Les autres peuvent écouter la musique mais ils ne peuvent pas la partager avec leurs voisins. Sur le graphe, les influenceurs sont en jaune. C'est l'étape 0 du graphe.

photo

En fonction du nombre d'abonnés de l'artiste, un certains nombre d'individus va écouter la musqiue. Si ces personnes sont des influenceurs, ils seront en orange, sinon ils seront en rouge. Ainsi chaque sommet orange peut partager la musique avec ses voisins. C'est l'étape 1 du graphe.

photo

La dynamique est lancée! Les voisins des influenceurs qui n'ont pas encore écouté la musique et qui décident de suivre l'influenceur vont l'écouter : ils sont en bleu sur le graphe. C'est l'étape 2 du graphe.

photo

Nous allons alors repéter l'expérience plusieurs fois. Nous considérons que lorsque pour tous les influenceurs qui ont écouté la musique et que pour hacun d'eux tout leurs voisins l'ont également écouté, alors le consensus est atteint. Plus personne d'autre n'écoutera la musique. 
Nous pouvons dès lors compter le nombre d'étapes à réaliser avant d'atteindre le consensus. Nous observons des premiers résultats sur le graphe ci-dessous avec en abscisse les identifiants des artistes, triés par ordre croissant selon leur nombre d'abonnés, et en ordonné la moyenne du nombre d'étapes avant que le consenus ne soit atteint.

<img width="283" alt="image" src="https://user-images.githubusercontent.com/99737912/163584016-bab612b8-3250-4dd5-a497-e63b2cb3fa46.png">

On constate une hausse globale du nombre d'étapes mais pas de façon linéaire. D'après notre hypothèse, celà s'expliquerait par le fait que les artistes avec plus d'abonnés seront écoutés par plus de monde, donc la diffusion de leur musique prendra plus d'étapes.

Nous avons par la suite refait un graphe dont l'axe des abscisses est le même que le graphe précédent. Cependant celui des ordonnés diffère, c'est la moyenne du nombre d'écoutes totales. Nous avons répété l'experience plusieurs fois et avons représenté la courbe moyenne obtenue pour tous les artistes.

<img width="280" alt="image" src="https://user-images.githubusercontent.com/99737912/163586052-7b8d7a11-fcab-44f8-a02e-facb592bc89d.png">

On remarque d'après cette courbe, et comme la précédente, que plus un artiste a d'abonnés sur Youtube, plus celui-ci sera écouté.
Notre hypothèse initiale est donc validée





![graphe sans moyenne](https://user-images.githubusercontent.com/99737912/162973615-42896e71-f47a-4f46-8b6e-7ed2c00d6be5.png)

![graphe moyenne](https://user-images.githubusercontent.com/99737912/162974667-ada68676-5f98-4765-b276-4860932646e5.png)

![graphe variance](https://user-images.githubusercontent.com/99737912/162974830-8bd86e42-94a7-456a-8814-14125454bf0e.png)

![macklemore0](https://user-images.githubusercontent.com/99737912/162973539-0f84686b-daa7-4b4b-acf3-c93790e99fa9.png)

![macklemore1](https://user-images.githubusercontent.com/99737912/162973410-f4459a06-bdc1-4bed-921c-3ee10ca5d551.png)

![macklemore2](https://user-images.githubusercontent.com/99737912/162973287-9d1e0206-f54e-4417-bf62-3f72ab454164.png)

![macklemore3](https://user-images.githubusercontent.com/99737912/162970477-968ebd3c-6874-4e34-a3ad-1727e22c4a66.png)

![tuerie3](https://user-images.githubusercontent.com/99737912/162973046-6d9bf32c-b835-4f3f-8f57-a6b078b09537.png)

![tuerie2](https://user-images.githubusercontent.com/99737912/162973156-6f672a3f-fcef-485f-9322-d1c3de37d92c.png)

![tuerie1](https://user-images.githubusercontent.com/99737912/162973220-d948c9c2-d3eb-452b-b9a2-18e46c676f35.png)


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
