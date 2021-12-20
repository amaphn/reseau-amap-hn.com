---
title: L'avant propos
---

Afin de mettre en valeur un contenu, vous pouvez spécifier des informations complémentaires dans l'*avant-propos* ("Front matter" en anglais ).

Ces informations permettrons par exemple d'afficher un résumé d'article et sa couverture sur la Une du site ou d'exploiter des fonctionnalités comme l'horodatage ou la génération automatique de liens vers les fiches de l'annuaire du site.

L'*avant-propos* permet également de fournir des informations riches au divers [agents utilisateurs](https://fr.wikipedia.org/wiki/User_agent). Par exemple cela permet de titrer l'onglet d'un navigateur ou de fournir des informations de résumé aux moteurs de recherches et aux fiches de partage des réseaux sociaux.

L'*avant-propos* est constitué de diverses données à spécifier avant les trois traits séparateur `---` du corps de l'article. Cahque données est composé d'un varaible et d'une valeur. Par exemple, vous pouvez spécifier une date de publication de cette manière : 

~~~
 date: 2018-11-14
~~~

**Liste des données de l'*avant-propos* :**
<!--more-->

 - [Standard](docs/l-avant-propos#standard)
 - [Évenements](docs/l-avant-propos#evenements)
 - [Petites annonces](docs/l-avant-propos#petites-annonces)

## Les données standard {#standard}
Les données standard peuvent être utilisées sur n'importe quel type de contenu.


### Titre
~~~
  title: Voici un titre par exemple
~~~

Le titre est important, ce titre sera exploité par les agents utilisateur. Par exemple cela permet d'afficher du contenu sur les onglet d'un navigateur et de favoriser la mise en avant de mot-clefs pour les moteurs de recherche.

### Extrait
~~~
  excerpt: Cette description résume bien le contenu de mon article.
~~~

Un court résumé du contenu. L'extrait est capital pour la présentation du contenu par les moteurs de recherche. Il permet également de présenter l'article de façon attirante dans les index de contenu (sur la page d'accueil, sur l'index d'un blog ou sur une page d'archive par exemple).

### Auteur
~~~
  author_name: Ziopod
  author_url: ziopod@gmail.com
~~~

Le nom de l'auteur et un lien (email ou web) seront crédités dans l'entête de la page HTML et pourrons être affichés automatiquement en pied de page d'un *article*.

### Licence
~~~
	license_name: Creative Commons BY 4.0
	license_url: http://creativecommons.org/licenses/by/4.0/
~~~

Vous permet de spécifier la licence d'usage du contenu diffusé. Les informations de licence seront inserées dans l'entête HTML de la page et pourrons être affiché automatiquement en pied de page d'un *article* ou d'une *page*.


### Mise en avant
~~~ 
  featured: true
~~~

Permet de mettre en avant un *article*. L'article sera épinglé sur la Une en page d'accueil.

### Date de publication
~~~
  date: 2018-12-01
~~~

Date de publication du contenu. À noter que cette variable auras la priorité sur les date spécifié en prefixe de nom de fichier.

### Titre court
~~~
  tinytitle: Un titre court
~~~

Vous permet de présicer un titre court alternatif, utile pour un affichage compact des données (lors de l'affichage sur la page d'accueil ou lors d'un partage sur les réseau sociaux).

## Les données pour les évenements {#evenements}

### Date de début d'événement
~~~
  startdate: 14-03-2015 8:30
~~~

Permet d'afficher et de classer les événements par date. Si aucune date de début n'est spécifier, la date de publication sera utilisé comme date de début d'évenement. L'évément sera automatiquement archivé le lendemain de la date de début.

### Date de fin d'événenemt
~~~
	enddate: 14-03-2015 18:30
~~~

Permet d'afficher une période d'évenement (du "temps" au "temps"). L'événement sera automatiquement archivé les lendemain de la date de fin de l'évenement.

### Location
~~~
 location: Centre Malraux, Rouen
~~~

Permet d'afficher le lieu de la rencontre.

## Les données pour les petites annonces {#petites-annonces}

### Lien vers une fiche de l'annuaire
~~~
  directory: amap-campus
~~~

Indiquez le **slug** (identifiant unique) de la fiche d'annuaire pour lier l'annonce à une entrée de l'annuaire. 

 
 [&#10094; Sommaire de la documentation](docs/index)