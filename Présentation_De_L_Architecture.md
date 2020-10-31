> **Ce document est voué à être modifié ou bien remplacer par un futur document plus complet.  
En effet celui-ci n'est là qu'à but d'information pour l'équipe**

# BUT DU DOCUMENT
-----

  Dans ce document il est possible de trouver l'ensemble des informations nécéssaires à la bonne comprhéension de chaque partie du projet.
  En effet ce document se décompose de la manière suivante : 
  
  - Méthode d'installation de la solution (sous XAMP ou Machine Virtuelle)
  - Présentation de l'arbre des dossiers
  - Présentation de chaque groupe de fichier
  - Règles de Développement à appliquer
  - Liens Utiles
  
# INSTALLATION DES OUTILS NECESSAIRES  
## 1/INSTALLATION DE XAMP

Pour ce qui concerne l'installation de XAMP, suivre le tutoriel suivant 
[Tutoriel installation XAMP](https://www.ionos.fr/digitalguide/serveur/outils/tutoriel-xampp-creer-un-serveur-de-test-local/).
Afin d'avoir la même version prendre la 3.2.4

## 2/INSTALLATION DE LA BASE DE DONNEES SQL
 Une fois XAMP ouvert, cliquez sur **start** à coté de **MySQL** pour démarrer le serveur  
 Ensuite cliquez sur **Admin** pour ouvrir la page d'administration de la base de donnée  
 Créez une nouvelle base de donnée prenomée webapp en **utf8mb4_general_ci**

### A/MODIFICATIONS A APPORTER
#### FICHIER SQL

Une fois fait, il faudra modifier quelques lignes du fichier permettant 
de remplir la base de données sur MySQL (fichier situé dans le dossier webapp situé sur le [projet original](https://github.com/HugoPetermann/Tidal-main/tree/master/webapp),
accesible ensuite au chemin suivant webapp>db>webapp.sql)

Dans ce fichier, il faudra changer les interclassements.  
Pour celà rechercher tous les **utf8mb4_0900_ai_ci** du fichier SQL et remplacer les par **utf8mb4_general_ci**  
Une fois fait, vous pouvez copier/coller le fichier dans l'onglet **Requête** de la base de données et **éxécuter** la requête

#### BASE DE DONNEES SQL

Comme vous avez pu le voir lors de l'ouverture de la page d'administration, il n'y a pas de demande de saisie d'un identifiant et d'un mot de passe.  
Il faut donc créer sur notre nouvelle base de données le compte permettant la connexion de notre site à la base de données  
Pour celà allez sur votre base de données **webapp**, puis dans l'onglet **Privilèges**  
Une fois fait cliquez sur **Ajoutez un compte utilisateur**  
Et remplissez les champs suivant :  
> Nomd'utilisateur: **debian-sys-maint**  
> Mot de passe : **aR7RIRZbiUZw3dYk**  
Cochez la case **Donner tous les privilèges sur la base de données webapp**  
Cochez la case **Privilèges globaux**  

## 3/INSTALLATION DE GITKRAKEN

Pour l'installation de GitKraken suivre ce  [lien](https://www.gitkraken.com/download)  
Le but de ce logiciel est de fournir une interface plus simple à comprendre en ce qui concerne les branches et les commandes propres à Git.  
Il sera expliqué dans plus bas comment l'utiliser.  

## 4/RECUPERATION DU DOSSIER DE DEVELOPPEMENT

Dans le dossier Git que vous clonerez sera déposer un fichier Zip contenantun dossier et son arborescance ainsi que les différents fichiers du projet.  
Il faudra le décompresser et mettre le dossier soit dans le fichier partagée avec la machine virtuelle soit dans **C:\xampp\htdocs** sur xamp.  

