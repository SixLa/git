 
ls => lister les fichiers 
cd = changer de dossier ( avec le nom de dossier en plus ) 
touch : créer un fichier  ( ex: touch index.html ) 
mkdir => créer un dossier ( ex : mkdir git-test )
pwd => voir le dossier courant
rm => supprimer un fichier 


pensez à renseigner vos informations via les commandes :
    
    git config --global user.email 'votre mail'
    git config --global user.name 'mon nom'
    
 =====  travail en local ( sur le poste de travail uniquement )

les autres commandes ( git ) sont sur la ressource indiquée : http://rogerdudler.github.io/git-guide

1) créez un dossier ( avec mkdir )
2) cd leNomDuDossierCréé
3) git init
4) créer un fichier ( touch nomDeFichier.html )
5) apporterdes modifications au fichier en écrivant quelque chose dedans( en ouvrant le fichier avec un éditeur de texte ou le bloc note + penser à le sauvegarder )
6) git add leNomDuFichier 
7) git commit -m  'le message de commit qui donne la raison de vos modifications '

=======

git log pour vérifier le commit

répéter pour avoir plusieurs commits 

git status pour vérifier l'état


========= faire le lien avec github ====

- créez un repo
- récupérer la commande exposée par github quand vous avez créé votre repo
( celle qui fait git remote add origin en https, pas ssh )

- lancez la dans le terminal uniquement quand vous êtes bien dans le dossier de travail de tout à l'heure

vérifiez avec git remote -v



========= jouer avec le serveur =====

/!\ modifiez toujours la même ligne pour les commits à venir pour ce tp ( ligne 1 typiquement )

1) créer une nouvelle branche avec 
git branch 'nomDeMaBranche'
2) aller sur la nouvelle branche avec la commande git checkout 'leNomDeMaBranche'
3) faites des modifications sur votre fichier
4) add + commit et vérifier avec git log
5) revenez sur la branche master avec  la commande git checkout master en vérifiant avec git log que le commit fait sur l'autre branche n'existe pas sur master
6) refaites un nouveau commit sur master ( en modifiant un fichier + add + commit ) et vérifiez que ce commit est ok avec git log
7) tentez de fusionner les deux branches, en faisant un git merge NomDeMABranche via master
8) résolvez les conflits 
9) commitez pusher


================ RESOURCES ==========

rappel des commandes utiles : 
https://www.hostinger.fr/tutoriels/commandes-git/

description du workflow et des commandes :
https://www.hostinger.fr/tutoriels/tuto-git/
divisée en articles assez complets : https://carlchenet.com/category/debuter-avec-git/

les branches :
https://carlchenet.com/debuter-avec-git-partie-4-les-commits-et-les-branches/
avec la doc officielle ( pour comprendre la théorie derrière, peut aider à structurer la compréhension ) : https://git-scm.com/book/fr/v2/Les-branches-avec-Git-Les-branches-en-bref

cours OpenClassrooms :
https://openclassrooms.com/fr/courses/1233741-gerez-vos-codes-source-avec-git

git expliqué avec des schémas visuels ( et rappel des commandes )
https://blog.lesieur.name/comprendre-et-utiliser-git-avec-vos-projets/
https://marklodato.github.io/visual-git-guide/index-fr.html


slides :
https://raspberry-pi.fr/cours/slides-git.html#/10/1

vidéos :
https://www.grafikart.fr/tutoriels/git-presentation-1090
