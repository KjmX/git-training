# Merge

*dur�e: 10 min*

## Revert

Cr�e un commit qui est l'exact inverse de celui pr�cis� en param�tre.

### En pratique : 

Cr�er une branche 'fixes' depuis le master et l'atteindre.

Modifier le fichier Error.html en y ajoutant la ligne 
`<!--Error-->`

Commiter ce changement avec le message "Error".

Pusher. 

Faire un revert du dernier commit `git revert COMMITHASH`

Observer le r�sultat dans l'historique. 
Pusher et observer les fichiers modifi�s sur git.  

## Reset 

supprimer le(s) dernier(s) commit(s) (mets les changements dudit commit comme non commit�s)
`git reset HEAD~1` o� 1 est le nombre de commits depuis le dernier � supprimer. 

### En pratique : 

Depuis la branche 'fixes', jouer un `git reset HEAD~1` pour supprimer le commit de revert. 

Observer le statut des fichiers, et le log. 


## Clean

Supprime les fichiers et r�pertoires non traqu�s. 
`git clean -df` -d pour effacer les r�pertoires, -f pour effacer les fichiers. 


### En pratique :

Depuis la branche 'fixes' Ajouter un nouveau fichier nomm� "Exception.cs"

Observer le statut des fichiers.

Supprimer le fichier avec un `git clean -df`
Observer le statut des fichiers, et le log. 

V�rifier que le fichier Exception.cs n'est plus pr�sent.

## Checkout 

Supprime les changements apport�s � un fichier. 

`git checkout -- FILENAME` pour ne supprimer les changements que dans un seul fichier. 
`git checkout -- .` pour supprimer tous les changements. 

Note : ceci n'affecte pas les fichiers non inclus dans l'index git. (ceux-ci n�cessitent un clean)

### En pratique : 

Supprimer les changements qui ont �t� induits par le reset. 

Observer le statut des fichiers, et le log. 

## Amend

Change le dernier message de commit

### en pratique : 

Taper `git commit --amend` puis changer le message de commit. A noter : si le commit a d�ja �t� push�, cela change l'historique, et implique donc un push force

## Blame

Permet de savoir qui a modifi� quelle ligne dans un fichier.

### En pratique : 

Faire un `git blame Startup.cs` et observer le r�sultat. 


## Probl�mes rencontr�s fr�quemment : 

Mon git est dans un �tat bizarre  : 
- Checker avec un git status 
- Regarder dans la ligne de commande si on est pas dans un �tat de merge ou de rebase (auquel cas : git rebase --abort ou git merge --abort)

Les tags de validation de SL :
- Pb de validation/ push d'un commit cherry pick� 
- Reset de la branche et recommit pour mettre un tag correct
