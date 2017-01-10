---
title: "Data Science expliqué à ma mère"
comments: false
---

# Introduction

Ma mère c'est souvent demandé ce que je faisait en tant que Data Sciencist, quelles étaient mes tâches quotidiennes, etc...Je vais donc essayer de donner ma vision de mon travail ici.

# Le Data Scientist

## Son rôle:
Le job du Data Scientist et d'explorer des données et informations pour en extraire de la valeur ou d'autres informations pertinentes.
On dit souvent que le Data Scientist est un expert combinant Statistiques, Informatique et expertises dans le domaine auquel les données appartiennent tout en étant bon en création de graphiques et visualisation.

Les compétences du Data Scientist sont presques toujours résumé à l'aide de ce diagramme:

![My helpful screenshot]({{site.baseurl}}/assets/Data_Science_VD.png)

En réalité il est difficile de posséder toutes ces capacités chez une personne et on regroupe souvent plusieurs data scientists aux compétences différentes au sein d'une même équipe.

## Pourquoi faire ?
L'intérêt du data scientist dans une entreprise varie beaucoup.

Dans une entreprise de vente en ligne, il va pouvoir analyser les actions des clients pour essayer de déterminer pourquoi ces derniers achetent ou n'achetent pas tel ou tel objet. Il va également pouvoir essayer de faire des liens entre les achats des différentes personnes pour que le site puissen suite proposer des produits personnalisé à chaque client.

Dans une entreprise qui s'occupe de l'acheminement du gaz, le data scientist va pouvoir analyser les données des capteurs qui donnent des informations sur l'état des conduits, les volumes transportés, la vitesse d'acheminement etc... pour ensuite pouvoir antciper d'éventuels accidents et catastrophes.

Dans le domaines bancaires il va pouvoir analyser les données des transactions des clients afin de déterminer plus facilement les cas de fraudes ou de vols d'informations clients (si un client Français achète soudainement pour 10 000€ de pizza depuis la Chine, il est possible que ce client ce soit fait voler ses informations bancaires)

# Mais concrétement ?

## Les données
Le premier problème auquel est confronté le data scientist est l'obtention des données. Sans elles, il ne peut pas faire grande choses.
Heureusement, il est de plus en plus facile d'en trouver de nos jours. Beaucoup d'entreprise ou d'institutions publiques en fournissent gratuitement. On appelle cela l'Open Data car il est alors possible de faire ce que l'on veut de ces données.

Il est également possible d'en obtenir via des compétitions organisé par des enterprises mais il est alors souvent interdit d'en faire un usage commercial.

Beaucoup de données peuvent également être récupéré d'internet comme des données de Twitter, Facebook, de site de d'informations ou encore de page internet classique mais il faut au préalable vérifier que le site autorise la récupération de ses pages web. On appelle cela le *Web Scraping*.

Enfin, la plupart du temps, les data scientist travaillent sur des données privées d'entreprise accumulé au fil du temps.

Mais d'où proviennent ces données ? Il faut savoir que de nos jours, les entrepries enregistrent presque tous ce qu'elles peuvent. Ainsi, sur la plupart des sites de commerces, il n'est pas rare que chaque action, clic d'un client sur le site web soit enregistré. Les objets possèdent également de plus en plus de capteurs qui enregistre beaucoup d'informations pour pouvoir ensuite les améliorer par exemple (les voitures possèdent de plus en plus de capteurs qui enregistre la position, la température de l'huile, la température du moteur,etc... afin de permettre ensuite aux constructeurs automobile de déterminer les failles les plus courantes).

ex images de données
![csv]({{site.baseurl}}/images/csv_example.jpg) 

![My helpful screenshot]({{site.baseurl}}/images/example_twitter.jpg)

## La préparation des données
Une fois les données récupérées, il faut alors les préparer avant de pouvoir les utiliser. Les données sont souvent loin d'être parfaites et il manque parfois des informations ou alors les données d'un même projet ne sont pas toutes au même format.
Il a donc presque toujours un gros travail de nettoyage qui consite à modifier les données pour qu'elles soient harmonisé et utilisable. 

En plus du travail de nettoyage, le data scientist est parfois ammené à créer de nouvelles données à partir de celles existantes afin de faciliter leur interprétation. Ces nouvelles données peuvent par exemple être créée en appliquant des formules de calcul sur des données existantes ou encore en séparant une donnée en deux. On appelle cela le *Feature Engineering*

Ce travail de préparation est la plupart du temps réalisé à l'aide de programmation.

# Le machine learning


{% highlight python %}

def show():
  print "test"

{% endhighlight %}

```python
s = "Python syntax highlighting"
print s
```


{% highlight ruby %}

def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end

{% endhighlight %}
