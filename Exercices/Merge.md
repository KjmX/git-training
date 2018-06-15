# Merge

*dur�e: 10 min*

## D�finition 

Une merge fusionne deux historiques ensemble. 

## Avant de d�marrer 

Regarder la config de git, et rep�rer la ligne `merge.ff= XXXX` (true ou false)
Si elle est � false, on va la passer � true. 

`git config merge.ff true`

## En pratique

Cr�er et atteindre une branche 'a-merger' depuis le master.
Modifier le fichier Index.html en y ajoutant la ligne:
`<!--Index-->`

Commiter ce changement avec le message "Index"

Atteindre le master, et de l� cr�er et atteindre une branche "cible-merge". 
V�rifier que la branche ne comporte pas le commit "Index" dans son historique. 

Modifier le fichier Error.html en y ajoutant la ligne 
`<!--Error-->`

Commiter ce changement avec le message "Error". 


On va � pr�sent merger la branche "a-merger" dans la branche "cible-merge". 
Observer l'historique de la branche "cible-merge". 

Jouer la commande `git merge a-merger`


