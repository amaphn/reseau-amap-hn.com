---
title: Docs / Les fichiers de contenu
---

**Sommaire**

 - [Le fichier de contenu](docs/fichiers-de-contenu#le-fichier-de-contenu)
 - [Les types de contenus](docs/fichiers-de-contenu#types-de-contenus)
 - [Lier des données](docs/fichiers-de-contenu#lier-des-donnees)

## Le fichier de contenu {#le-fichier-de-contenu}

Les fichiers de contenu vous permette de publier du contenu sur votre site (page, article, événement, etc.); ce sont de simple fichier texte que vous éditez avec n'importe quel editeur de texte, vous devez simplement changer l'extension du nom de fichier `.txt` (texte brut) par l'extension `.md` (Markdown).

Les fichiers de contenu sont constitué de deux parties séparés par un triple tirets séparateur `---`. La zone avant les tirets est appelé *avant-propos*, la zone en dessous des tirets est appelé *corps du contenu* ou plus simplement *contenu*.

Voici un exemple de fichier de contenu : 

~~~
    title: Bonjour, voici mon premier article
    summary: C'est un extrait d'Alice au pays de Merveilles.
    author: Ziopod@gmail.com
    ---

# Alice in Wonderland

The rabbit-hole went straight on like a tunnel for some way and then dipped
suddenly down, so suddenly that Alice had not a moment to think about stopping
herself before she found herself falling down what seemed to be a very deep
well.

~~~

L'*avant propos* est composé d'une série de variables/valeurs. Chaque variable commence par deux ou quatres espaces, le nom de la variable, le signe deux points `:` puis la valeur.

[Plus d'informations sur l'avant-propos](docs/l-avant-propos) {.btn .btn-cta}

Sous le séparateur de méta `---` viens le *contenu* du fichier, ici vous pouvez utiliser du [balisage Markdown](https://fr.wikipedia.org/wiki/Markdown) at ajouter des média pour enrichir la présentation du contenu.

[Liste des marqueurs Markdown](docs/markdown) {.btn .btn-cta}

## Types de contenus {#types-de-contenus}

Les cotenus du site peuvent être de plusieurs types (article de blog, page, agenda, etc.). Chaque type est distingué par un repertoire portant le nom du type en anlgais et au pluriel. Les types possibles sont les pages `pages`, les articles de blog `posts` et les événements `events`.

~~~
| content
	| pages
	| posts
	| events
~~~

Lors de leur affichage, chaque type auras un traitement spécifique. Par exemple les articles de blog pourrons être affichées par liste paginée, et certain articles pourrons être affichés mis en avant (affiché en Une sur la page d'accueil).

Au sein de chaque repertoire de type de contenu, il est possible de créer d'autres répertoires pour gérer d'autres contenus (images, fichiers pdfs, etc.).

### Images
Si vous avez besoin d'insérer des images dans vos article, vous pouvez créer un répertoire `images` dans votre dossier de type dans lequel vous placerez les images pour vos articles. Il vous suffiras ensuite [d'inserer l'image](docs/markdown#images) lors de la rédaction de votre article.

<pre>
| content
	| posts
		| images
			presentation.jpg</pre>

### Draft
Ce répertoire vous permet de placer des articles en mode "brouillon", il ne serons visible sur le site que par les personnes ayant un accès editeur. Cela est particuliérement utile si vous voulez contrôler en situation le rendu de votre article avant sa publication.

<pre>
| content
	| posts
		| draft
			2015-06-23_la-permaculture-et-les-agriculteurs-paysans.md</pre>

### Personnalisé
Il est possible de créer n'importe quel sous repertoire, cela vous permet par exemple de gérer des catégories et sous catégories pour la présentation de vos articles.

<pre>
| content
	| posts
		| recettes
			2015-04-03_tarte-au-citron.md</pre>


## Lier des données {#lier-des-donnees}

Vous avez la possibilité de créer des hyperliens entre différents contenu de votre, ou d'insérer des images dans vos contenu.
Vous devrez y faire référence à l'aide d'un lien relatif.  

### Liens vers un autre contenu 

Par exemple, imaginons que nous ayons deux articles dans notre blog :

<pre>
| content
	| posts
		2015-06-21_des-agrumes-en-normandie.md
		2015-04-03_tarte-aux-citronx.md</pre>

Dans notre article sur les agrumes en Normandie, nous voulons faire référence à une recette de tarte au citron que nous avons également publié. Nous pourrons écrire : 

<pre>
la production d'agrumes est suffisante pour faire de très belles
[recettes de tartes aux citrons](/tarte-aux-citrons) maisons</pre>

La syntaxe Markdonw `[Texte de votre lien](url-de-votre-lien)` nous permet de [créé un hyperlien](docs/markdown#hyperliens), l'adresse relative `/tarte-aux-citrons` est le *slug* qui fait référence a l'article `2015-04-03_tarte-aux-citrons.md` présent dans notre dossier `posts` . L'URL généré par lors du rendu sera `http://domaine.com/post/tarte-aux-citron` .

Pour faire référence à une article dans un sous repertoire, par exemple : 

<pre>
| content
	| posts
		2015-06-21_des-agrumes-en-normandie.md
		| recettes
			2015-04-03_tarte-aux-citronx.md</pre>

Il vous suffira d'indiquer le sous repertoire dans l'adresse : 
<pre>
[recettes de tartes aux citrons](/recettes/tarte-aux-citrons)</pre>

Si vous voulez faire référence à un contenu situé dans un repertoire supérieur, par exemple : 
<pre>
| content
	| pages
		informations.md
	| posts
		2015-06-21_des-agrumes-en-normandie.md</pre>		

Il suffit d'utiliser l'indicateur de dossier parent `../`, par exemple depuis l'article "Des agrumes en Normandie" : 
<pre>
N'hesitez pas à [nous contacter](../pages/informations) pour plus d'informations.</pre>

### Insérer une image

Pour inserer une image dans votre contenu vous utilisez le balisage Markdown `![Description de votre image](url-de-votre-image)`.
De la même manière que pour les hyperliens, vous devez présicer l'adresse URL de l'image.  
Pour un contenu classé de cette manière : 
<pre>
|content
	| posts
		2015-06-21_des-agrumes-en-normandie.md
		| images
			citrons-de-normandies.jpg</pre>

Pour afficher l'image du citrons de Normandie dans notre article nous insérerons l'image de cette façon :
<pre>
![Des citrons en Normandie](/images/citrons-de-normandie.jpg)
Oui, des citrons peuvent belle et bien pousser en Normandie.
</pre>

### Lier d'autres médias

Vous avez bien entendu la possibilité de faire des liens vers des média externes.  
Par exemple voici un lien vers une image externe : 
<pre>
![Bourgeons, fleurs et fruits de citron sur la même plante](https://upload.wikimedia.org/wikipedia/commons/7/75/Citrus_limonum_3.JPG)</pre>

Ce qui donneras : 

![Bourgeons, fleurs et fruits de citron sur la même plante](https://upload.wikimedia.org/wikipedia/commons/7/75/Citrus_limonum_3.JPG)

Vous pouvez également intégrer du "code incorporé" provenenant de divers services et réseaux sociaux d'internet.

Le code d'intégration copier depuis une video de chez Vimeo par exemple : 
<pre>
&#x3C;iframe
 src=&#x22;https://player.vimeo.com/video/111693630?color=8DC798&#x26;byline=0&#x26;portrait=0&#x22;
 width=&#x22;744&#x22;
 height=&#x22;419&#x22;
 frameborder=&#x22;0&#x22;
 webkitallowfullscreen mozallowfullscreen allowfullscreen&#x3E;
&#x3C;/iframe&#x3E;
</pre>

Donnera : 

<iframe
	src="https://player.vimeo.com/video/111693630?color=8DC798&byline=0&portrait=0"
	width="744"
	height="419"
	frameborder="0"
	webkitallowfullscreen mozallowfullscreen allowfullscreen>
</iframe>


Ou pourquoi pas un tweet : 
<pre>
&#x3C;blockquote class=&#x22;twitter-tweet&#x22; data-cards=&#x22;hidden&#x22; lang=&#x22;fr&#x22;&#x3E;
&#x3C;p lang=&#x22;fr&#x22; dir=&#x22;ltr&#x22;&#x3E;A &#x3C;a href=&#x22;https://twitter.com/hashtag/Dijon?src=hash&#x22;&#x3E;#Dijon&#x3C;/a&#x3E; :
l&#x26;#39;&#x3C;a href=&#x22;https://twitter.com/hashtag/AMAP?src=hash&#x22;&#x3E;#AMAP&#x3C;/a&#x3E; des
&#x3C;a href=&#x22;https://twitter.com/hashtag/Bourroches?src=hash&#x22;&#x3E;#Bourroches&#x3C;/a&#x3E; f&#xEA;te ses 10 ans
&#x3C;a href=&#x22;https://twitter.com/hashtag/agriculture?src=hash&#x22;&#x3E;#agriculture&#x3C;/a&#x3E;
&#x3C;a href=&#x22;http://t.co/XoMVIcBWks&#x22;&#x3E;http://t.co/XoMVIcBWks&#x3C;/a&#x3E;
&#x3C;a href=&#x22;http://t.co/vnvadSxRt2&#x22;&#x3E;pic.twitter.com/vnvadSxRt2&#x3C;/a&#x3E;
&#x3C;/p&#x3E;
&#x26;mdash; France3 Bourgogne (@F3Bourgogne) &#x3C;a href=&#x22;https://twitter.com/F3Bourgogne/status/609769411877175296&#x22;&#x3E;13 Juin 2015&#x3C;/a&#x3E;&#x3C;/blockquote&#x3E;
&#x3C;script async src=&#x22;//platform.twitter.com/widgets.js&#x22; charset=&#x22;utf-8&#x22;&#x3E;&#x3C;/script&#x3E;</pre>

Donnera : 

<blockquote class="twitter-tweet" data-cards="hidden" lang="fr">
<p lang="fr" dir="ltr">A <a href="https://twitter.com/hashtag/Dijon?src=hash">#Dijon</a> :
l&#39;<a href="https://twitter.com/hashtag/AMAP?src=hash">#AMAP</a> des
<a href="https://twitter.com/hashtag/Bourroches?src=hash">#Bourroches</a> fête ses 10 ans
<a href="https://twitter.com/hashtag/agriculture?src=hash">#agriculture</a>
<a href="http://t.co/XoMVIcBWks">http://t.co/XoMVIcBWks</a>
<a href="http://t.co/vnvadSxRt2">pic.twitter.com/vnvadSxRt2</a>
</p>
&mdash; France3 Bourgogne (@F3Bourgogne) <a href="https://twitter.com/F3Bourgogne/status/609769411877175296">13 Juin 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

 
 [&#10094; Sommaire de la documentation](docs/index)