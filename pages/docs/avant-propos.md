    title: Avant propos
    ---
    
Avant toute chose il convient de présenter les méthodes et technologies choisies pour l'édition du contenu rédactionnel du site du réseau régionnal des AMAP de Normandie.

## Motivations
Les choix technologique et logiciels sont guidés par les critères suivant.

### Simplicité d'usage.
La volonté de ne pas créer de barrière elitistes à la gestion du contenu éditoriale et la maintenance technique du système de publication. Ces choix doivent s'accomoder d'une participation collaborative, accèssible au plus de personnes possible.

### Périnnité de la technologie
Limité la maintenance et l'entretien du système permet de focalisé les ressources sur les points les plus importants de la publication de contenu; à savoir, la mise en place et la tenue d'ne stratégie de communication, la création et la publication de conten.

### Consommation technologique sobre
Limité la consommation de ressource par une technologie peu gourmande simple à faire fonctionner sur les serveur web les plus courant.


## Solutions techniques et de gestion du contenu
Afin d'apporter la meilleur réponse possible à ces exigences, les solutions suivantes ont été choisies : 

### Coté "technique"

- Serveur web : Debian/Apache;
- Code logique : PHP, Fichier plat (pour la gestion du contenu editorial), MySQL (pour la gestion des données de l'annuaire);
- Versionnage : GIT;
- Logiciel : Framework Kohana (Paradigme de programmation MVVM), Mustache (gestion des templates).

### Code "éditorial" :

 - Annuaire des AMAP et des producteurs : Interface web;
 - Gestion editoriale : [Fichiers plat](https://fr.wikipedia.org/wiki/Base_de_donn%C3%A9es_orient%C3%A9e_texte);
 - Edition Web : [Markdown](https://fr.wikipedia.org/wiki/Markdown);
 - Collaboration editoriale : [GIT](https://fr.wikipedia.org/wiki/Git) (solution populaire pour faire de la [gestion de version](https://fr.wikipedia.org/wiki/Gestion_de_versions)).
 
 
 ## En pratique
 
Dans la suite de la documentation nous nous attacherons à vous guider pour l'usage pratique des technologies de publication et d'édition. Il conviendras de vous familiariser vous même avec le concept de base des technologies employé (référez-vous aux liens données plus haut).
 
 [&#10094; Sommaire de la documentation](docs/index)
 