## Contribution
Vous êtes libre de contribuer au contenu du [site Régional du réseau des AMAP de Haute-Normandie](http://reseau-amap-hn.com/), la condition est d'avoir sur compte Github.com.

Pour contribuer en [créant un ticket](https://github.com/amaphn/reseau-amap-hn.com/issues), ou en modifiant directement un fichier depuis l'interface de Github. 

Documentation sur le sujet :

 - [Copier un dépôt](https://help.github.com/articles/fork-a-repo/)
 - [About pull requests](https://help.github.com/articles/about-pull-requests/)

## Publication d'un article

### 1. Créer un fichier .md dans le dossier "post"

Les fichier d'articles sont de simples fichier texte dont l'extension doit être .md  
Les noms de fichiers ne doivent comporter de caractères spéciaux (é,",&, etc.) ni d'espace. Seul
les chiffres, lettres et signe le séparateur `-` sont autorisé.

Les articles seront affiché par ordre alphabétique inversé, vous pouvez utiliser des chiffres au debut de nom du fichier suivi d'un tiret de soulignemement `_`. Par exemple `2013-09-24_le-titre-de-mon-article.md` ou `1_mon-article.md`.

### 2. Paramètres
Un paramètre d'article est composé d'un mot-clé, suivi d'un signe deux-points `:` et d'une valeur. Par exemple `Titre: Le titre de mon article`.

Ils doivent toujours ce situer au début du fichier avant le marqueur `----`. Ils sont exploiter par le système pour afficher automatiquement certaines informations, améliorer l'affichage et le améliorer le référencement des articles.

**Liste des paramètres**

Paramètre | Format | Description
------------- | -------------------- | ---- 
`Title`         | texte moyen          | Paramètre obligatoire - Titre de l'article
`Short_title`   | texte court          | Titre court de l'article, exploiter notamment pour l'affichage sous forme de liste des articles
`Date`          | JJ/MM/AAAA HH:MM:SS  | Date de publication de l'article
`Author`        | texte	cout            | Nom de l'auteur de l'article
`Cover`         | nom de fichier image | Image de couverture de l'article
`summary`       | texte long           | Résumé de l'article 	

`Published`			| boolean		| Indique que l'article ne doit pas être affiché sur le site
`License`		| url					| Nom et adresse de la license sous laquelle est publié l'article
`Slug`			| texte format url		| Adresse de remplcacement de l'article

**Exemple**

	Title: Les AMAP de Haute&#x2011;Normandie soutiennent la ferme des Bouillons
	Short_title: Protégeons la ferme des Bouillons
	Date: 2013/06/05 : 06:44:19
	Author: [Le Réseau des AMAP de Haute&#x2011;Normandie](contact@reseau-amap-normandie.com)
	Cover: la-ferme-des-bouillons.jpg
	summary: Le Réseau des Amap de Haute-Normandie ne peut que soutenir l’Association de Protection de la Ferme des Bouillons à Mt St Aignan. En effet, les Amap ont dans leurs fondements même la préservation d’une agriculture de proximité d’où leur nom Association de Maintien de l’Agriculture Paysanne.
	Draft: true
	Credit: [Creative commons BY-SA](http://creativecommons.org/licenses/by-sa/3.0/deed.fr)
	Slug: protegeons-la-ferme-des-bouillons
	----


### 3. Le contenu de l'article
Le marquage sémantique et de présentation est basé sur la syntaxte de marquage [Markdown](http://daringfireball.net/projects/markdown/).
Vous touverez une référence complète de la syntaxte à cette adresse [http://michelf.ca/projets/php-markdown/syntaxe/](http://michelf.ca/projets/php-markdown/syntaxe/)

#### 3.a Usage de base de markdown
Markdown permet de faire pas mal de chose, mais nous allons nous attaché à vous décrire les quelques marqueurs principaux.

Marqueur                       | exemple | rendu | description 
--- | --- | --- | --- 
Créer un paragraphe          | | | Deux sauts de paragraphe
Créer un saut de ligne forcé | | | Deux espaces en fin de ligne + un aut de paragraphe
Mettre dut texte en italique | `*texte en italique*` | *texte en italique* | 
Mettre du texte en gras      | `**texte en gras**` | **texte en gras** |
Inserer un hyperlien         | `[Texte du lien](http://google.com "Titre du lien")` | [Texte du lien](http://google.com "Titre du lien") | Le texte `[]` et le titre du lien `""`sont optionnels
Inserer une adresse email    | `[Texte du mail](mailto:ziopod@gmail.com "Titre du mail")` | [Texte du mail](mailto:ziopod@gmail.com "Titre du mail")| Règles similaire au marqueur de lien
Insérer une image            | `![Un chat sur le dos](http://placekitten.com/g/70/70 "Mon chat")` | ![Un chat sur le dos](http://placekitten.com/g/70/70 "Mon chat")| Règles similaire au marqueur de lien
Insérer un titre de niveau 2 | `## Exemple de titre de niveau 2`| <h2>Exemple de titre de niveau 2</h2> | Pour diminuer le niveau, ajouter des signes dièse `#`, 2 dièses pour un titre de niveau 2, 3 dièses pour un titre de niveau 3, 4 dièses pour un titre de niveau 4, etc. (jusqu'au niveau 6). Le titre de niveau 1 est généralement géré par le système
Insérer une citation         | ` > Une citation` | <blockquote>Une citation</blockquote> | Un signe "plus grand que" `>` + un espace + vptre texte
Créer une liste à puce       | ` - un élément de liste` | <li>un élément de liste</li> | un signe "séparateur" `-` + un espace + votre texte
Créer une liste numérotée    |` 1. Un élément de liste` | <ol><li>Un élément de liste</li></ol> | Un chiffre + un point + un espace + votre texte


#### 3.b Ajouter des images
Pour utiliser vos propre images, ajoutez les dans le dossier `post/images`.  
Pour insérer une image dans un article utilisez l'adresse `/content/type-de-contenu/images/nom-de-l-image.jpg`.

Par exemple `![Tomates et basilic font bon ménage](/content/post/images/plants-de-tomates-et-basilic.jpg)`

#### 3.c Ajout de médias externe
Vous pouvez insérer du contenu provenant d'autres services, comme des vidéos, des images ou du contenu "riche".  

Par exemple voici une image provenant de Wikimedia externe : 
<pre>
![Bourgeons, fleurs et fruits de citron sur la même plante](https://upload.wikimedia.org/wikipedia/commons/7/75/Citrus_limonum_3.JPG)</pre>

Ce qui donneras : 

![Bourgeons, fleurs et fruits de citron sur la même plante](https://upload.wikimedia.org/wikipedia/commons/7/75/Citrus_limonum_3.JPG)

Vous pouvez également intégrer du "code incorporé" provenenant de divers services et réseaux sociaux d'internet.

Chaque service (Vimeo, Youtube, Tweeter, etc.) proposent un code d'intégration destiné au partage de contenu.
Voici par exemple le code d'intégration copier depuis une video de chez Vimeo : 
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


Un autre exemple avec du contenu provenant de tweeter : 
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
