	title: Les types contenu
---

Le système de gestion de contenu (FlatFile) utilise divers types de contenu. Chaque type de donnée possède des fonctionnalités et caractèristiques spécifiques.
<!--more-->

 - [Standard](#standard)
 - [Évenements](#evenements)
 - [Petites annonces](#petites-annonces)

## Les métas données standard {#standard}
Les métas données standard peuvent être utilisées sur n'importe quel type de contenu.


### Titre

<pre>
	title: Voici un titre par exemple</pre>

La méta titre est importante, c'est le titre de votre article pour les agents utilisateur; elle permettra aux machines de comprendre le contenu de article et de présenter correctement votre article.  
Par exemple cela permet d'afficher du contenu sur les onglet d'un navigateur et de favoriser la mise en avant de mot-clefs pour les moteurs de recherche.

### Description
<pre>
	description: Cette description résume bien le contenu de mon article.</pre>

Un court résumé du contenu de votre article. La description est capitale pour la présentation de votre article dans les moteurs de recherche. Elle permet également de présenter l'article de façon élégante dans les index de contenu (sur la page d'index d'un blog ou sur une page d'archive par exemple).

### Auteur
<pre>
	author_name: Ziopod
	author_url: ziopod@gmail.com</pre>

Les informations d'auteur seront insérées dans l'entête HTML de la page.  
Le nom de l'auteur et un lien (email ou web) pourrons être insérés automatiquement en pied de page d'un article.

### Licence
<pre>
	license_name: Creative Commons BY 4.0
	license_url: http://creativecommons.org/licenses/by/4.0/</pre>

Les informations de licence seront inserées dans l'entête HTML de la page.
Vous permet de spécifier la licence d'usage du contenu diffusé. 

### Mise en avant
<pre>
	featured: true</pre>

Cette méta données permet d'indiquer la mise en avant de certain contenu. Ce sera particulièrement utile pour certains articles de blog que l'on veut conserver sur la page d'accueil par exemple.  
Remarquez qu'il n'est pas nécessaire de présciser une valeur pour cette méta donnée.

### Date de publication
<pre>
	date: </pre>

Date de publication, utilise si vous n'utilisez pas les date en prefixe de nom de fichier. Elle auras la priorité sur la date en prefixe de fichier.

### Titre court
<pre>
	tinytitle: Un titre court</pre>

Vous permet de présicer un titre court alternatif, utile pour un affichage compact des données, ou pour le partage sur les réseau sociaux.

## Les métas données pour les évenements {#evenements}

### Date de début d'événement
<pre>
	startdate: 14-03-2015 8:30</pre>

Permet d'afficher et de classer les événements par date. Si aucune date de début n'est spécifier, la date de publication sera utilisé comme date de début d'évenement. L'évément sera automatiquement archivé le lendemain de la date de début.

### Date de fin d'événenemt
<pre>
	enddate: 14-03-2015 18:30</pre>

Permet d'afficher une période d'évenement (du "temps" au "temps"). L'événement sera automatiquement archivé les lendemain de la date de fin de l'évenement.

### Location
<pre>
	location: Centre Malraux, Rouen</pre>

Permet d'afficher le lieu de la rencontre.

## Les métas données pour les petites annonces {#petites-annonces}

### Lien vers une fiche de l'annuaire
<pre>
	directory: amap-campus</pre>

Indiquez le **slug** (identifiant unique) de la fiche d'annuaire pour lier l'annonce à une entrée de l'annuaire. 

[&#10094; Sommaire de la documentation]({{base_url}}docs/index)