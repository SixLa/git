 ### Commandes Unix
```ls``` => lister les fichiers 

```cd``` = changer de dossier ( ex: ```cd monDossier``` ) 

```touch``` : créer un fichier  ( ex: ```touch index.html``` ) 

```mkdir``` => créer un dossier ( ex : ```mkdir git-test``` )

```pwd``` => voir le dossier courant ( pour faire le lien entre le terminal et l'explorateur de fichiers )

```rm``` => supprimer un fichier / dossier ( avec le flag -r ) 
( ex : ```rm monFile.html``` / ex : ```rm -r monDossier```

### Commmandes git

``` git init``` initialiser un repository ( repo ) git

```git status``` pour voir l'état du dossier de travail ( vis à vis du stage )

```git log``` pour voir l'historique des commit

```git add <nomDeMonFichier>``` pour ajouter un fichier dans le **Stage** avant de pouvoir le commiter ( ex: ```git add index.html``` ) 
```git add --all ``` permet d'ajouter tous les fichiers du dossier dans lequel vous etes dans le **Stage**

```git commit -m 'mon message'``` pour l'ensemble des fichiers ajoutés avec ```git add```


:warning: pensez à renseigner vos informations via les commandes :warning: 
    
    git config --global user.email 'mon mail'
    git config --global user.name 'mon nom'
    
 Contexte
 ------
 
Git permet de **versionner** du code,c'est-à-dire créer des sauvegardes successives ( ce qu'on apppelle un commit ) qui permettent de conserver l'historique des modifications, donc l'évolution du projet, car chaque commit se rajoute à la suite des autres.

Un commit est le nom donné à une sauvegarde faite des modifications en cours.
Quand j'ai commité, il n'y a plus de modifications en cours, jusqu'à ce que je modifie de nouveau un fichier.


Analogie pour expliquer :
----

Imaginez une personne qui prend une photo d'elle même tous les matins pendant 20ans.


Chaque photo représente une légère variation de la veille.
En mettant par exemple une date derrière chaque photo, on peut retrouver quel était le visage de cet personne à 21 ans et 4jours par exemple.

Dans un cadre plus large, git permet également créer une histoire (succession de commits ) constituée de commits faits par différentes personnes d'une même équipe.
L'idée étant que plusieurs personnes pourront s'occuper de travailler sur la même application sans se marcher sur les pieds, et avec un moyen de rassembler ( fusionner ) leurs travaux, pour que chacun récupère les modifications faites par les autres.

Si on reprend le principe de l'album photo, un projet web serait représenté par une famille entière, et l'album sera alors composée de photo de toutes les personnes qui ont posé chaque jour.

Dans un projet, tout le monde ne travaille pas tout le temps sur ce projet, les contributions pourront être irrégulières ou pas, ce n'est pas un problème en soi. 

---
 
Git ne fait qu'observer les fichiers présents dans le **dossier de travail**. On appelle le dossier de travail : le working directory ( vous trouverez des réferences à cette appelation dans les sujet en anglais.

L'espace réservé dans lequel on va préparer les fichiers pour pouvoir les commiter s'appelle le **Stage**.

Il s'agit d'un marquage que git va opérer pour dire qu'il sont prêt au commit.

Je peux avoir envie de travailler sur 3 fichiers mais vouloir n'en sauvegarder les modifications que d'un.

La commande ```git add <nomdefichier>``` permet au fichier en question d'être préparé par git pour faire partie du commit.

Analogie :

J'écris une lettre ( un fichier )

Je dispose d'une enveloppe pour poster ma lettre.
Tant que l'enveloppe est ouverte, je peux y rajouter d'autres lettres, une photo, ou je peux reprendre et la modifier.

Le stage c'est l'enveloppe, tant qu'elle est ouverte.

Quand j'ai décidé que j'étais prêt à poster l'enveloppe, je la ferme.
L'enveloppe refermée ne pourra plus voir les lettres qu'elle contient modifiées, on vient de faire un commit.


Travail en local ( sur le poste de travail uniquement )
----

Les autres commandes ( git ) sont sur la ressource indiquée : 

1) créez un dossier 
2) se déplacer dans le dossier
3) initialiser un repo git
4) créer un fichier 
5) apporter des modifications au fichier en écrivant quelque chose dedans ( en ouvrant le fichier avec un éditeur de texte ou le bloc note + penser à le sauvegarder )
6) ajouter au stage votre fichier 
7) faites un commit de vos modifications
8) répéter les opération 5) à 7) pour avoir plusieurs commits 


## Branches et conflits 

Contexte
------

Commandes
-----

```git branch maBranche``` pour créer une branche

```git checkout maBranche``` pour se déplacer sur une branche

```git merge maBranche```  pour merger la branche nommée sur la branche actuelle

Instructions
------

1) créez une branche
2) faites un commit sur master ( en modifiant la ligne 1 de votre fichier )
3) changez de branche 
4) nouveau commit sur la meme ligne 
5) mergez ensuite master sur votre branche
6) résolvez les conflits !
7) commitez :)




Faire le lien avec github 
------

- créez un repo
- récupérer la commande exposée par github quand vous avez créé votre repo ( le ```git remote add origin URLDeMonRepoCréé``` )
( celle qui fait git remote add origin en https, pas ssh )

- lancez la dans le terminal uniquement quand vous êtes bien dans le dossier de travail de tout à l'heure

vérifiez avec ```git remote -v```


===== faire un push =====

pour envoyer les commit sur le serveur, on fait un ```git push origin master```
Si vous avez créé une autre branche et que vous êtes dessus, il faudrait indiquer le nom de cette branche à la place de master



Jouer avec le serveur
-------

:warning: modifiez toujours la même ligne pour les commits à venir pour ce tp ( ligne 1 typiquement )

1) créer une nouvelle branche avec 
git branch 'nomDeMaBranche' ( remplacer le nom que vous souhaitez)
2) aller sur la nouvelle branche avec la commande git checkout 'leNomDeMaBranche'
3) faites des modifications sur votre fichier
4) add + commit et vérifier avec ```git log```
5) revenez sur la branche master avec  la commande git checkout master en vérifiant avec git log que le commit fait sur l'autre branche n'existe pas sur master
6) refaites un nouveau commit sur master et vérifiez que ce commit est ok avec git log
7) tentez de fusionner les deux branches, en faisant un git merge NomDeMaBranche via master
8) résolvez les conflits 
9) commitez pusher


RESSOURCES 
------

explication pas à pas :
- https://perso.liris.cnrs.fr/pierre-antoine.champin/enseignement/intro-git/

rappel des commandes utiles : 
- http://rogerdudler.github.io/git-guide
- https://www.hostinger.fr/tutoriels/commandes-git/

description du workflow et des commandes :
- https://www.hostinger.fr/tutoriels/tuto-git/
- divisée en articles assez complets : 
  - https://carlchenet.com/category/debuter-avec-git/

les branches :
- https://carlchenet.com/debuter-avec-git-partie-4-les-commits-et-les-branches/
- avec la doc officielle ( pour comprendre la théorie derrière, peut aider à structurer la compréhension ) : 
  - https://git-scm.com/book/fr/v2/Les-branches-avec-Git-Les-branches-en-bref

cours OpenClassrooms :
- https://openclassrooms.com/fr/courses/1233741-gerez-vos-codes-source-avec-git

git expliqué avec des schémas visuels ( et rappel des commandes )
- https://blog.lesieur.name/comprendre-et-utiliser-git-avec-vos-projets/
- https://marklodato.github.io/visual-git-guide/index-fr.html


slides :
- https://raspberry-pi.fr/cours/slides-git.html#/10/1
- http://slides.com/moji3000/git_presentation/fullscreen#/15

vidéos :
- https://www.grafikart.fr/tutoriels/git-presentation-1090
