---
title: "La Data Science expliquée à mes parents"
comments: false
---

# Introduction

Ma mère s'est souvent demandé ce que je faisais en tant que Data Scientist, quelles étaient mes tâches quotidiennes, etc... Je vais donc essayer de donner ma vision du travail que je fais.


# Le Data Scientist

## Son rôle:
Le travail du Data Scientist est d'explorer des données et informations pour en extraire de la valeur ou d'autres informations pertinentes.
On dit souvent que le Data Scientist est un expert combinant statistiques, informatique et expertises dans le domaine auquel les données appartiennent tout en étant bon en création de graphiques et visualisation.

Les compétences du Data Scientist sont presque toujours résumées à l'aide de ce diagramme:

![Data Science Diagram]({{site.baseurl}}/assets/Data_Science_VD.png)

En réalité il est difficile de posséder toutes ces capacités chez une personne et on regroupe souvent plusieurs Data Scientists aux compétences différentes pour former une bonne équipe.


## Pourquoi faire ?
L'intérêt du Data Scientist dans une entreprise varie beaucoup.

Dans une entreprise de vente en ligne, il va pouvoir analyser les actions des clients pour essayer de déterminer pourquoi ces derniers achétent ou n'achétent pas tel ou tel objet. Il va également pouvoir essayer de faire des liens entre les achats des différentes personnes pour que le site puisse ensuite proposer des produits personnalisé à chaque client.

Dans une entreprise qui s'occupe de l'acheminement du gaz, le Data Scientist va pouvoir analyser les données des capteurs qui donnent des informations sur l'état des conduits, les volumes transportés, la vitesse d'acheminement etc... pour ensuite pouvoir antciper d'éventuels accidents et catastrophes.

Dans le domaine bancaire il va pouvoir analyser les données des transactions des clients afin de déterminer plus facilement les cas de fraudes ou de vols d'informations clients (si un client Français achète soudainement pour 10 000€ de pizza depuis la Chine, il est possible que ce client ce soit fait voler ses informations bancaires).


# Mais concrètement ?

## Les données
Le premier problème auquel est confronté le Data Scientist est l'obtention des données. Sans elles, il ne peut pas faire grand chose.
Heureusement, il est de plus en plus facile d'en trouver de nos jours. Beaucoup d'entreprise ou d'institutions publiques en fournissent gratuitement. On appelle cela l'Open Data car il est alors possible de faire ce que l'on veut de ces données.

Il est également possible d'en obtenir via des compétitions organisées par des entreprises mais il est alors souvent interdit d'en faire un usage commercial.

Beaucoup de données peuvent également être récupérées d'internet comme des données de Twitter, Facebook, de site de d'informations ou encore de page internet classique mais il faut au préalable vérifier que le site autorise la récupération de ses pages web. On appelle cela le **Web Scraping**.

Enfin, la plupart du temps, le Data Scientist travaille sur des données privées d'entreprise, accumulées au fil du temps.

Mais d'où proviennent ces données ? Il faut savoir que de nos jours, les entreprises enregistrent presque tout ce qu'elles peuvent. Ainsi, sur la plupart des sites de e-commerces, il n'est pas rare que chaque action, clic d'un client sur le site web soit enregistré. Les objets possèdent également de plus en plus de capteurs qui enregistre beaucoup d'informations pour pouvoir ensuite les améliorer.(exemple: les voitures possèdent de plus en plus de capteurs qui enregistrent la position, la température de l'huile, la température du moteur,etc... afin de permettre ensuite aux constructeurs automobiles de déterminer les failles les plus courantes).


## La préparation des données
Une fois les données récupérées, il faut alors les préparer avant de pouvoir les utiliser. Les données sont souvent loin d'être parfaites et il manque parfois des informations ou alors les données d'un même projet ne sont pas toutes au même format.
Il a donc presque toujours un gros travail de nettoyage qui consiste à modifier les données pour qu'elles soient harmonisées et utilisables. 

En plus du travail de nettoyage, le Data Scientist est parfois ammené à créer de nouvelles données à partir de celles existantes afin de faciliter leurs interprétations. Ces nouvelles données peuvent par exemple être créée en appliquant des formules de calcul sur des données existantes ou encore en séparant une donnée en deux. On appelle cela le **Feature Engineering**


## Le Machine Learning
Très souvent, la dernière étape du processus d'analyse de données est de faire ce que l'on appelle du Machine Learning.
Chercher par soi-même ce que peuvent nous dire les données serait un travail très complexe et fastidieux, c'est pourquoi le machine learning est utilisé pour que l'ordinateur trouve lui-même une signification aux données ou trouve lui même les relations qui lient les données.

Le machine learning est séparé en deux groupes:

- Machine Learning Supervisé
- Machine Learning Non Supervisé

### Le Machine Learning Non Supervisé
Ce type de machine learning est utilisé lorsque que l'on a des données mais que l'on ne sait pas vraiment dans quelle direction aller, lorsque l'on en sait pas ce que l'on cherche.
Le Data Scientist va alors faire passer les données qu'il possède dans un algorithme (une suite d'opération et d'instruction) en espèrant que l'ordinateur va pouvoir trouver des choses intéressantes.
L'exemple le plus classique est celui du **clustering** où la machine va essayer de séparer les données en groupes.

Exemple de clustering:

- L'image du haut montre plusieurs points
- L'image du bas présente les groupes de points découverts après passage des données dans un algorithme de clustering

![kmeans]({{site.baseurl}}/images/kmeans.png)

Après le passage de l'algorithme, on se retrouve avec 3 groupes qu'il pourrait être judicieux de traiter séparément.


### Le Machine Learning Supervisé
A l'inverse du non supervisé, ce type de machine learning s'utilise lorsque l'on sait ce que l'on cherche.

Je vais essayer d'utiliser un example simple: 
Imaginons que nous avons 100 perroquets. Pour chaque perroquet nous avons:

1. L'age
2. Le sexe
3. La race
4. La couleur de la plume arrière gauche
5. Si oui ou non le perroquet a un/une partenaire
6. Si oui ou non le perroquet est intelligent

Les points 1 à 5 sont faciles à obtenir mais le point 6 est plus compliqué car il faut faire faire des tests aux perroquets.
Nous allons donc donner à notre algorithme de machine learning juste les données de 1 à 5 en lui disant : à partir de ces points, je veux que tu me trouves le lien avec le point 6. L'algorithme va donc tout faire pour obtenir le point 6 à l'aide des autres. Une fois que la machine aura appris du mieux qu'elle peut comment obtenir ce qu'on lui a demandé d'obtenir, elle va nous retourner une fonction que l'on appelle **modèle** que l'on va pouvoir réutiliser (N.B. : le machine learning non supervisé retourne aussi un modèle).

Grâce à ce modèle, lorsqu'un nouveau perroquet arrivera, il suffira de rapidement déterminer son âge, sexe, race, couleur de la plume arrière gauche et si il a un/une partenaire. On donnera ces informations au modèle qui nous dira alors si, d'après ce qu'il a appris, le perroquet est intelligent ou non permettant ainsi un gain de temps important.

### Complications
Le principal problème du machine learning supervisé est qu'il faut avoir des données avec déjà certains résultats. Résultats qui peuvent parfois être compliqués à obtenir.
De plus, il n'est pas toujours possible de prédire ce que l'on veut. Il est fort possible que pour notre exemple des perroquets, l'ordinateur n'arrive pas a trouver si le perroquet est intelligent en fonction des autres informations et dans ce cas il faut éventuellement trouver des données supplémentaires, supprimer des données non pertinentes ou (re)faire du feature engineering.

# Conclusion
Le travail du Data Scientist est en général cyclique. La plupart du temps il va récupérer des données, les traiter, et essayer de les exploiter grâce au machine learning par exemple mais si il n'obtient pas ce qu'il veut, il va recommencer en essayant de trouver de nouvelles informations qu'il va falloir retraiter puis re-exploiter.

C'est un travail qui peut sembler répétitif mais il est en réalité très varié car les données ne sont jamais les mêmes et il faut toujours s'adapter pour trouver le meilleur angle d'attaque. De plus, c'est toujours très gratifiant de découvrir ce qu'elles cachent et de réussir à construire un modèle qui permet de prédire ce que l'on veut.
Il est à noter qu'en général, le Data Scientist ne crée pas les algorithmes de machine learning qui servent entre autre à la prediction mais il les connaît, sait comment ils fonctionnent et se tient au courant des innovations pour choisir et adapter celui qui sera le plus performant pour son problème.
