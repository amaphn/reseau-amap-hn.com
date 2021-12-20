---
title: Docs / Gestion du contenu
description: Documentation sur le gestionnaire de contenu FlatFile
author: Ziopod
date: 2015/07/10
license: {"name":"Creative commons CC BY 4.0", "url":"http://creativecommons.org/licenses/by/4.0/"}
---

Le contenu éditoriale du site est géré par un gestionnaire de contenu sans base de données ([fichiers plat](https://fr.wikipedia.org/wiki/Base_de_donn%C3%A9es_orient%C3%A9e_texte)). Les données sont représentées sous formes de dossiers et de fichiers. Le document que vous consultez en ce moment est lui-même un fichier plat (Flatfile). Dans cette documentation, nous partirons du principe que vous êtes familier avec les bases de l'informatique (créer un dossier et un fichier, nommer un fichier, afficher et changer une extension de fichier, naviguer sur internet, etc.).

Dans cette rubrique nous verrons comment créer et organiser les fichiers du contenu editorial du site.

<!--more-->

**Sommaire**

 - [Gestion des fichiers textes](docs/gestion-du-contenu#gestion-des-fichiers-textes)
 - [Gestion des médias](docs/gestion-du-contenu#gestion-des-medias)
 - [Horodatage et tri des données](docs/gestion-du-contenu#horodatage)


## Gestion des fichiers textes {#gestion-des-fichiers-textes}

Flatfile permet de gérer les données de votre site internet sous forme de [fichiers texte](http://fr.wikipedia.org/wiki/Fichier_texte) (appelé aussi *fichier texte brut*). Ces fichiers supportent des [métadonnées](docs/metadonnees) et le language de balisage léger [Markdown](docs/markdown).   
Pour ajouter du contenu à votre site, il vous faut ajouter un fichier de donnée dans le dossier `content`. Ce fichier texte devras comporter l'extension `.md` (au lieu de l'habituelle extension `.txt`).

### Classer le contenu
Tout votre contenu sera géré dans un repertoire principal nommé `content`. Ensuite viennent des sous-repertoires permettant de classer les données par type; par exemple le dossier `pages` pour les pages uniques de votre site (comme la page "informations") ou le dossier `posts` pour les articles d'un blog.

Par exemple pour un article de blog, on créé le fichier de contenu suivant : 

<pre>
| content
	| posts
		2015-07-12_bonjour-je-suis-un-article.md</pre>

L'article sera automatiquement disponible à l'adresse structuré de cette manière : 

<pre>
	http://mon-comaine.com/post/bonjour-je-suis-un-article</pre>

La portion d'adresse situé juste après le nom de domaine permet de determiner automatiquement un type de données; dans notre exemple nous utilisons `post`, le fichier seras cherché dans le repertoire `posts` (au pluriel) et sera interprété comme une donnée de type `post` (donnée de type "article de blog").

L'identifiant unique de l'article (que l'on appel également "slug") est la portion d'adresse située après; dans notre exemple nous indiquons `bonjour-je-suis-un-article`, le fichier correspondant à ce nom sera cherché.

## Gestion des médias {#gestion-des-medias}

Vous pouvez bien entendu agrementer votre contenu texte de contenu média complémentaire (images, vidéos, etc.). Il est important de ter que pour des soucis de simplicité technique, seul les médias d'images et de fichiers (leger) à telecharger seronts gérer dans le dossier de contennu du site. Les médias plus lourds (vidéos, gros fichiers) devrons provenir de service internet tiers (Vimeo, Youtube, Dropbox, etc.).

Vous êtes libre de placer le contenu médias ou vous voulez. Mais pour plus de clarté et d'organisation nous classerons les médias dans un dossier portant le nom du type de média.

Par exemple, pour notre article précedent, nous placerons les fichiers dans un sous-dossier `images` :

~~~
| content
  | posts
    2015-07-12_bonjour-je-suis-un-article.md
    | images
      visuel-pour-mon-article.jpg
      document-a-telecharcher.pdf
~~~

Vous pourrez ensuites les insérer dans votre article à l'aide du marqueur [Markdown approprié](docs/markdown#medias).

### Format et taille des images

Le format conseillé est le JPG. 
La taille des images (en pixel) pour les **images de couverture** doit être 1188  pixels de large maximum et d'environs 400 pixels de hauteur. Les **images accompagnant le texte** doit ête de 879 pixels de large et d'envrons 300 pixels de hauteur.

## Horodatage et tri des données {#horodatage}

Vous remarquerez que dans l'exemple précédent, le nom du fichier possède une date `2015-07-12_`, c'est un prefixe de tri; En utilisant le signe `_` "tiret bas", vous indiquez à FlatFile un prefixe qui pourra servir à présicer une date de publication ou simplement modifier l'ordre de tri.

Par exemple, des fichiers nommées comme ceci s'afficherons dans l'ordre alphabétique: 

<pre>
| pages
	a-propos.md
	accueil.md
	informations.md</pre>

Si nous voulons changer l'ordre d'affichage, nous pouvons les nommer de cette manière : 

<pre>
| pages
	1_accueil.md
	2_a-propos.md
	3_informations.md</pre>

Pour des données de type blog, nous classerons les articles de cette manière : 

<pre>
| posts
	2014-12-12_bienvenue.md
	2015-01-01_bonne-annee.md
	2015-03-21_les-fleurs-du-printemps.md</pre>

Les prefixes de type date serons très utile pour afficher les articles par ordre de publication et pour mettre en place des fonctionnalités de tri; par exemple pour générer des archives chronologique, ou pour créer un gestionnaire d'événements. 


[&#10094; Sommaire de la documentation](docs/index)