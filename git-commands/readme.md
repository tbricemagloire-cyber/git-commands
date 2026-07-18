# commandes git

- liste des commandes git

## git init
- permet d'initialiser un repertoire

## git add [.]
- permet d'ajouter un fichier ou des modifications dans le stagging

## git commit -m
- permet d'enregistrer une modification en local
  le message est important

## git push
- permet de poucer les modifications en ligne sur github 

## git status
- permet de verifier le statut du repertoire
- permet de lister les modifications a traiter

## git log 
- permet de lister les modifications en local

## git branch
- permet de creer une branche

## git checkout 
- permet de passer d'une branche a une autre
- permet de se deplacer d'une branche a une autre
- avec l'option -b checkout va creer la branche si elle n'existe pas

##git remote add origin (URL)
- sert à lier ton dépôt Git local à un dépôt distant
-git remote : gère les dépôts distants.
-add : ajoute un nouveau dépôt distant.
-origin : est le nom donné à ce dépôt distant (c'est une convention, tu pourrais l'appeler autrement).
-Après cette commande, ton dépôt local sait que le dépôt distant nommé origin correspond à cette URL.
-Tu peux ensuite envoyer ton code avec :

##git push -u origin main/master selon le nom de ta branche.
-Le -u enregistre origin/main (ou origin/master) comme branche distante par défaut. 
-Ensuite, tu pourras simplement faire :

##git push

et

##git pull
sans avoir à préciser origin main à chaque fois.


## git pull
- permet de recuperer mes modifications distantes c'est à dire sur github

## git rebase
- permet de recuperer les modifications de la branche main
- les modifications de la branche main sont placees en dessous des modifications de la branche courante 
- les modifications de la branche courante sont placees au dessus des modifications de la branche main

## git reset
- permet de supprimer un commit
- permet de revenir a un commit precis defini par son identifiant
- attention a utiliser avec precaution

## git diff
- permet de comparer 2 commits

## git clone
- permet de recuperer un fichier perdu a travers le lien sur github

##git remote remove origin ou ##git remote rm origin


supprime le dépôt distant nommé origin de ton dépôt local.
Cela signifie que Git oublie simplement l'adresse du dépôt distant. Cette commande :
❌ ne supprime pas ton projet local ;
❌ ne supprime pas le dépôt sur GitHub/GitLab ;
✅ supprime uniquement la référence origin dans la configuration de ton dépôt local.
Exemple
Avant :
git remote -v
Affiche :
origin  https://github.com/utilisateur/projet.git (fetch)
origin  https://github.com/utilisateur/projet.git (push)
Tu exécutes :
git remote remove origin
Puis :
git remote -v
N'affichera plus rien (ou les autres dépôts distants s'il y en a).
Quand l'utiliser ?
Tu t'es trompé d'URL.
Tu veux connecter ton projet à un autre dépôt GitHub.
Tu souhaites repartir avec une nouvelle configuration du dépôt distant.
Ensuite, tu peux ajouter un nouveau dépôt distant avec :
git remote add origin NOUVELLE_URL


##git remote set-url origin NOUVELLE_URL

-sert à modifier l'URL d'un dépôt distant existant sans le supprimer.
Différence avec les autres commandes
-git remote add origin URL ➜ ajoute un nouveau dépôt distant.
-git remote remove origin ➜ supprime le dépôt distant.
-git remote set-url origin NOUVELLE_URL ➜ change simplement son adresse.
Exemple
Supposons que origin pointe vers :
https://github.com/brice/ancien-projet.git
Tu veux qu'il pointe vers :
https://github.com/brice/nouveau-projet.git
Tu exécutes :
git remote set-url origin https://github.com/brice/nouveau-projet.git
Pour vérifier le changement :

##git remote -v

Tu verras la nouvelle URL.
En pratique : si origin existe déjà, il est préférable d'utiliser git remote set-url plutôt que de faire remove puis add, car c'est plus simple et le résultat est le même.




