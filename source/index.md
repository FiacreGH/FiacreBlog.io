---
layout: default
---

----------------------------------------------------------------------------------------------------------------------------------------------------------
**DEVELOPPEMENT DE PAGES WEB STATIQUES**
========================================
----------------------------------------------------------------------------------------------------------------------------------------------------------

##Comment utiliser sculpin comme outil de developpement

###les différentes étapes sont les suivantes:

* Installez sculpin sur vortre ordinateur sous linux

Ouvrez votre terminal puis, executez la commande: `wget https://download.sculpin.io/sculpin.phar`

Puis:  `chmod +x sculpin.phar`

Et pour finir:  `mv sculpin.phar ~/bin/sculpin`

Pour vérifier que sculpin est bien installé, tapez la commande:  `sculpin -version`

* Structure de votre repertoire de travail

Creer un repertoire dans votre dossier personel `~/Project` ou autre dependant de la distribution linux qui se trouve installée sur votre machine

Par exemple `~/Project/mkdir mon-premier-site-sculpin`

Puis dans ce repertoire vous creer le dossier ou seront mis vos fichiers sources; ce dossier se nomme `source`

Pour cela tapez cette commande: `mkdir source`

* Contenu de la source

Il s'agit du contenu de votre site, un fichier `*.md` doit être creé dans la source.

NB: ce fichier avec l'extension `.md`(md pour markdown) est celui a aprtir du quel sculpin vas generer du `*.html` lisible par les navigateurs

Obtenez plus d'info plus sur markdown regardez [ici](http://en.wikipedia.org/wiki/Markdown#Example).

Mettez du contenu dans votre fichier .md

Par exemple:

`---`

`---`

`# Hello World`

`Ceci est un contenu de test`

* Generation du code html

Pour générer le code html, assurez vous d'être dans le repertoire de votre site puis executez la commande:

`sculpin generate --watch --server`

NB: cette commande démarre un serveur qui permet d'afficher votre site en local (code html generee a partir du fichier .md).

Le code html génerée se place automatiquement dans un dossier creé par sculpin et nomé `output_dev`

Une fois le serveur lancé vous pourez voir votre site a cette adresse: `http://localhost:8000`

Vous avez donc le rendu il ne reste qu'à embelir votre site à present!

* Mise en page

--Pour l'ajout de theme nous procederons comme ce qui suit:
Créer un dossier dans la racine du projet avec la commande suivante: `mkdir -p app/config`
Créer le fichier `sculpin_kernel.yml` qui servira à personaliser le comportement de sculpin et y mettre le contenu suivant:

`sculpin_theme:`

        theme: yourname/themename

Maintenant, il faudrais créer un dossier qui contiendra le fichier de mise en page.
Pour cela taper la commande: `mkdir -p source/themes/yourname/yourtheme/_layouts`


--Pour la mise en page, nous allons faire l'usage de ["twig"](http://twig.sensiolabs.org/documentation) qui est un moteur de template et qui generera notre mise en forme.
Pour créer le fichier twig, placez vous dans l'emplacement:

 `/Project/mkdir mon-premier-site-sculpin/source/themes/yourname/yourtheme/_layouts`

  Puis exécutez la commande : `touch default.twig.html`

  Mettez ce contenu dans le fichier `touch default.twig.html`:

Très bientôt la suite!


#REALISATION: FIACRE SANKARA ( aidé par FUDRIOT) :)