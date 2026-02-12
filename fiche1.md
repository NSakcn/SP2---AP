Rayan Boina Boina - Enes Akcin

# **Mission 1 - Création d'un documentation avec  MkDocs et GitHub Pages**

## Première étape - Choix de l'éditeur MarkDown 

Pour ce qui est du choix de l'outil d'édition utilisé pour les documents en MarkDown, beaucoup de choix sont possible, offrant des avantages différents : 
- Mark Text *( Interface claire, léger, aperçu en direct)*
- Obsidian *( Idéal pour des prises de notes, très intéressant pour de l'organisation)*
- VS code *( Aperçu intégré, extensions puissantes)*
- Vim / Neovim *( Léger, minimaliste, personnalisable)*
- ... 

Notre choix à été naturellement **VS code** étant donné que c'est un outil que nous possédons tous, avec lequel nous sommes donc tous plus ou moins famillier. <br>
De plus il possède un système d'aperçu intégré et d'extensions correspondantes à nos attentes.

## Deuxieme étape - relier git à **VS code**

Comment relier VS code à son GitHub pour pouvoir mettre en place un versionning ainsi qu'un accès sur dépot distant ?
<br>
1. Premièrement, installer git : [dernière version de git](https://git-scm.com/)
2. Créer un dépot sur GitHub pour le projet
3. Se rendre dans son projet sur VS code
4. Ctrl + Shift + P puis taper git init, puis séléctionner son dépot créé en amont

Maintenant que votre projet VS code est relié à GitHub, il faut voir comment faire remonter nos versions ou mises à jour de projet jusqu'à GitHub :

1. Appuyez sur ce logo : <br><br> ![logo branche](logogit.jpg)
2. Pour "tracker" les documents dont vous voulez faire remonter les maj, positionnez vous dessus et cochez le "+" nommé "Stage changes"
3. Maintenant que les fichiers du projet son trackés, il faut faire remonter les maj, appuyez donc sur commit (le premier commit demande une connexion à GitHub)
4. Ensuite, il faudra décrire le commit puis appuyer sur commit
5. Appuyez sur Sinc Changes
6. Acceptez le fait de ramener la maj à la branche Main, le dépot est donc maintenant mis à jour avec donc un accès aux versions antérieures


## Troisième étape - Création d'un site statique avec **MkDocs** pour notre documentation


Créer un premier document yaml pour spécifier les information et la structure de notre site MkDocs
<br>
Par exemple :
<br>
`site_name: doc1` *nom du site* <br>
`docs_dir: SP2---AP` *repertoire de la documentation md*<br>
`theme: readthedocs` *thème par défaut MkDocs*<br>

Installer mkdocs dans le cmd : `py -m pip install mkdocs` <br>
, le fichier yaml doit se trouver au noeud précédent, une fois cela fait : `py -m mkdocs serve` pour déployer la documentation. <br>

Ici MkDocs nous à donc permis de créer un site statique local pour afficher de manière ordonnée notre documentation, hors nous souhaitons l'héberger avec GitHub Pages pour pouvoir la publier en ligne. 

## Quatrème étape - Héberger notre site statique sur **GitHub Pages**
