# ppnum_git

 
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
5) faire des modif ( en ouvrant le fichier avec un éditeur de texte ou le bloc note + penser à le sauvegarder )
6) git add leNomDuFichier 
7) git commit -m  'le message de commit qui donne la raison de vos modifications '

=======

git log pour vérifier le commit

répéter pour avoir plusieurs commits 

git status pour vérifier l'état
