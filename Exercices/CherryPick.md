# Cherry-pick

*dur�e: 15 / 20 min*

## D�finition 

Le cherry-pick permet de r�cup�rer un commit sp�cifique depuis une branch pour l'appliquer en tant que dernier commit d'une autre.


## En pratique:

Depuis master, cr�er et atteindre une branche 'cherry-pick-me'

A l'aide d'un �diteur de fichier, ins�rer dans Config.cs : 
`/// a config file`

Commiter ce changement avec le message "Modif Config.cs". 

A pr�sent modifier le contenu du fichier Settings.cs et y ins�rer 
`/// settings 1`

Commiter ce changement avec le message "Modif Settings.cs". 

__2 commits distincts doivent �tre visibles dans l'historique__

Afficher le log de la branche et rep�rer les lignes d�crivant les commits. Elles doivent ressembler � ceci : 

`commit __433411e842d6c46658982b74625b1ff5f64e7da2__
Author: Yann TERRAILLON <yann.terraillon@seloger.com>
Date:   Mon Jun 11 18:20:39 2018 +0200
	Modif Config.cs
`

Double-cliquer sur le hash du commit "Modif Config.cs" (en gras dans l'exemple pr�c�dent) pour le copier. 

Retourner sur la branche master et afficher l'historique avec un `git log`. 

Jouer la commande `git cherry-pick __433411e842d6c46658982b74625b1ff5f64e7da2__`

Regarder � nouveau l'historique du master.


## En cas de conflit:

Depuis master cr�er et atteindre une branche 'cherry-pick-issue'

Modifier le contenu du fichier Settings.cs et y ins�rer 
`/// settings 2`

Commiter ce changement avec le message "Modif Settings.cs for conflict". 

Cherry-picker le commit "Modif Settings.cs" depuis la branche 'cherry-pick-me'