---
title: "Data Science for dummies"
comments: true
---

# Introduction

My mother often asked me what I did as Data Scientist, what were my everyday tasks, etc... So I am going to try to explain my work.


# The Data Scientist

## His duty
The job of the Data Scientist is to exploer data and informations to extract from them some value or any other interesting patterns.
It is often said that the Data Scientist is an expert which combine statistics, IT and business expertise being also good in visualization and graphics creation.

The skills of the Data Scientist are often summarize with this diagram:

![Data Science Diagram]({{site.baseurl}}/assets/Data_Science_VD.png)

In reality, it is difficult to possess all these capacities in just one person and most of the time, we regroupe various Data Scientists with individual skills to create a team.


## But why ?
![But why gif]({{site.baseurl}}/images/giphy.gif)

The need for a Data Scientist change a lot according to the business of the company.

In a e-commerce company, he will be able to analyze the customers actions to determine why they buy or don't buy a particular object. He is also going to discover the links between the purchase of the various customers so that the website is then able to offer some personalized products to each customers.

In a gaz transmission company, the Data Scientist will be able to analyze the results of some sensors which records information about the state of the pipeline, the volume carried, the speed of transmission, etc... for then anticipate eventual accidents.

In the banking domain, he will be able to anlyze the data from the transaction of the customers to determine more easily frauds or personnal customers information (if a French customer suddenly buy for 10 000€ of pizza in a Shangaï restaurant, it is highly possible that the banking information of this customer have been robbed).

# In practice

## The data
The main issue for the Data Scientist is to obtain the data. Without them, he can't do anything. Hopefully, it is more and more easy to find them nowadays. A lot of companies or public institutions give theirs freely. It is called Open Data because it is then possible to do whatever you want from these data.

It is also possible to obtain them thanks to competitions often organized by companies mais if it often forbidden to use them for commercial purpose.

A lot of data can also be extracted from the web like for Twitter, Facebook, news website or classical web pages mais it is mandatory to verify that the websites allow the extraction of their webpage. This technic is called **Web Scraping**.

But most of the time, the Data Scientist works on private entreprise data which are stored over time.

But where these data come from ? Nowadays
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
