---
title: Guide Markdown
---

Markdown est un système de balisage léger, il vous permet de marquer (balisé) votre texte afin de mettre en valeur son contenu. À titre d'exemple ce docuement est complément présenté en syntaxe Markdown.
<!--more-->

 - [Le titrage](docs/markdown#titrage)
 - [Le texte en emphases](docs/markdown#emphases)
 - [Paragraphes et retour à la ligne](docs/markdown#paragraphes)
 - [Les hyperliens](docs/markdown#hyperliens)
 	- [Les liens stylisés](docs/markdown#hyperliens-stylises)
 - [Les images](docs/markdown#images)
 - [Citations](docs/markdown#citations)
 - [Listes](docs/markdown#listes)
 - [Tableaux](docs/markdown#tableaux)


## Titrage {#titrage}

Les titrages permettent de contraster les informations de votre document. Ils jouent un rôle important dans la lisibilité d'un article, le texte qui constitue les titres seront prévilégié par les moteurs de recherche.  
Vous pouvez choisir parmis plusieurs niveau d'importance (de 1 à 6); par exemple un titre de niveau 1 sera utilisé le titre principale de l'article, un titre de niveau 2 sera choisi pour les intertitres.

		#  Un titre HTML h1 de niveau 1
		##  Un titre HTML h2 de niveau 2
		###  Un titre HTML h3 de niveau 3
		####  Un titre HTML h4 de niveau 4
		#####  Un titre HTML h5 de niveau 5
		######  Un titre HTML h6 de niveau 6

Ce qui donneras : 

#  Un titre HTML h1 de niveau 1
##  Un titre HTML h2 de niveau 2
###  Un titre HTML h3 de niveau 3
####  Un titre HTML h4 de niveau 4
#####  Un titre HTML h5 de niveau 5
######  Un titre HTML h6 de niveau 6

## Emphases {#emphases}

Les emphases permettent de mettre en valeur certains mots de vos textes, comme pour le titrage, cela auras un impact sur le référencement par les moteurs de recherche.
Il existe 3 niveau d'emphases, l'italique, le gras et le gras italique.

		Cette phrase contient *du texte en italique*
		Ici nous avons du **texte en gras**
		Exceptionnellement nous pouvons utiliser du ***texte en gras italique***

Ca qui donneras : 

Cette phrase contient *du texte en italique*  
Ici nous avons du **texte en gras**  
Exceptionnellement nous pouvons ***utiliser du gras italique***

## Paragraphes et retour à la ligne {#paragraphes}
Pour créer un paragraphe avec Mardown il vous faut saisir deux fois le caractère invisible "retour chariot" (touche "entrée" ↵).

	Ceci est premier paragraphe

	Ceci est un second paragraphe

Donneras : 

Ceci est premier paragraphe

Ceci est un second paragraphe

Il est possible de saisir des sauts de ligne afin de forcé le retour à la ligne d'une phrase sans pour autant créer un nouveau paragraphe. Pour créer un retour à la ligne vous devez saisir deux fois espace, puis un "retour chariot" (touche "entrée" ↵).

	Ceci est un retour  
	à la ligne

Donneras : 

Ceci est un retour  
à la ligne


## Hyperliens {#hyperliens}
Les hyperliens sont un élément essentiel de la publication sur internet, ils permettent de valoriser votre contenu en faisant référence à d'autres docuement publié sur internet. Plus un docuement est riches en référence, mieux il sera considéré comme un document de qualité par les moteur de recherche et par les internautes. Un lien est composé d'un texte et d'une adresse, le texte sera marqué à l'aide d'un `[` crochet ouvrant et d'un `]` crochet fermant, suivit imédiatement de l'adresse comprise entre une `(` parenthèse ouvrante et une `)` parenthèse fermante.

		[recettes de tartes aux citrons](http://www.750g.com/tarte-aux-citrons-r93553.htm)

Ce qui donneras

[recettes de tartes aux citrons](http://www.750g.com/tarte-aux-citrons-r93553.htm)

### Les adresse email
Pour afficher un lien vers une adresse email, encadrer l'adresse avec les signes `<` chevron ouvrant et `>` chevron fermant.

	<ziopod@gmail.com>


Donneras : 

<ziopod@gmail.com>

Il est à noter que de cette manière, l'adresse email sera encodée dans le source de la page, ce qui la rend un peu moins vulnérable aux [spambots](https://fr.wikipedia.org/wiki/Spambot).

### Liens simples
Il est possible de créer un lien en affichant l'adresse URL.

Par exemple : 

	<https://fr.wikipedia.org/wiki/Markdown>

Donneras: 

<https://fr.wikipedia.org/wiki/Markdown>

### Les liens stylisés {#hyperliens-stylises}
Vous avez la possibilité d'ajouter des marquages suplémentaires à vos liens afin de modifier leurs apparences. Juste après le signe `)` parenthèse fermante ajouter le mot-clef `.btn` entre `{}` crochet ouvrant et crochet fermant :

		[Ceci est un bouton](#){.btn}  
		ou	
		[Ceci est un bouton](#){.btn .btn-cta}

Ce qui donneras : 

[Ceci est un bouton](#){.btn}  
ou  
[Ceci est un bouton](#){.btn .btn-cta}

## Les images {#images}

La syntaxe pour insérer une image est très similaire à la syntaxe des liens, voici un exemple :

		![Logo de l'AMAPHN](image/default-logo.png)

Donneras : 

![Logo de l'AMAPHN](images/default-logo.png)

Notez la présence du point `!` d'exclamation avant le `[` crochet d'ouverture. Le texte entre les `[]` crochets représente le texte alternatif à l'image, il s'agit d'un décrivant l'image qui pourras être exploité par les [agent utilisateurs](https://fr.wikipedia.org/wiki/User-Agent) afin de comprendre le contenu de l'image.

Comme pour les [liens stylisés](#hyperliens-stylises) Vous pouvez également insérer des images dotée d'une légende en employant le mot-clef `.legend` : 

	![Image d'exemple](https://farm6.staticflickr.com/5134/5475817799_f375f2b757_b.jpg){.legend}
	*Des tomates de toutes les couleurs*

Donneras : 

![Image d'exemple](https://farm6.staticflickr.com/5134/5475817799_f375f2b757_b.jpg){.legend}
*Des tomates de toutes les couleurs*


## Les Citations {#citations}
Vous pouvez insérer des citations de cettes façon : 

	> L'essentiel est invisble pour les yeux

Donneras : 

 > L'essentiel est invisible pour les yeux

## Les listes {#listes}

Vous pouvez créer deux types de liste; les liste non-ordonnées (dont l'ordre n'as pas d'importance) et des listes ordonnées (dont l'ordre du contenu est important).

Un liste ordonnée, ce créée en saisissant un espace, puis le signe `-` trait d'union : 

	 - Farine de blè : 500g.
	 - Sel fin : 10 pincées 
	 - Eau : 32 cl.
	 - Levure de boulangerie : 8g.

Donneras : 

 - Farine
 - Sel
 - Eau
 - Levure

Un liste ordonnée, ce créée de la même manière, on remplaceras simplement le signe `-` trait d'union par des chiffres :

	1. Mélanger la farine le sel, la levure et l'eau
	2. Pétrir pendant 20 min.
	3. Laisser reposer 4 heures
	4. Cuire à 240° pendant 15 minutes

Donneras : 

 1. Mélanger la farine le sel, la levure et l'eau
 2. Pétrir pendant 20 min.
 3. Laisser reposer 4 heures
 4. Cuire à 240° pendant 15 minutes


## Les tableaux {#tableau}

Vous avez la possibilité de créer un tableau de cette manière :

	|Produit 				|Qté distribué 	|Tarif moyen
	|---					|---			|---
	|Panier de légumes 		|56 			|11.17€
	|Œufs de poules 		|19 			|2.50€
	|Fromage de chèvre 		|18 			|1.00€
	|Produits de la pomme 	|17 			|2.50€
	|Viande d'agneau 		|17 			|12.00€

Donneras : 

|Produit 				|Qté distribué 	|Tarif moyen
|---					|---			|---
|Panier de légumes 		|56 			|11.17€
|Œufs de poules 		|19 			|2.50€
|Fromage de chèvre 		|18 			|1.00€
|Produits de la pomme 	|17 			|2.50€
|Viande d'agneau 		|17 			|12.00€

 
 [&#10094; Sommaire de la documentation](docs/index)