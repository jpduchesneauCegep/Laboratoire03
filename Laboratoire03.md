# Laboratoire 03 - Docker-Compose


 - Le but de se laboratoire est de mettre en place un environement de développement pour un site Web conprenant des pages statiques et également un site Wordpress.
 - L'environnement doit comprendre trois services (Conteneurs) :
     - Nginx avec le site Web racine
     - WordPress 
     - MySQL
  - Le site Web doit avoir une page index.php situé à la racine de votre serveur Web (localhost:2022). Cette page doit présenter votre équipe et avoir un lien vers le site WordPress qui est situé à l'URL suivant : wordpress/index.php

- Le laboratoire s'effectue en groupe de 2.

 - Le temps alloué est de 2 séances. La remise est pour le 18 janvier 2022 minuit.

Vous devez fournir sur Léa ou par un adresse d'un dépôt GitLab:

- Un dépot git conprenant les branches suivantes : 
    - Le **main** (master) représente ce qui serait en production après que votre client autorise la mise en production.
    - Le travail sur les fonctionnalités et les correctifs sont effectuées dans leur propre branche nomé au nom de la fonctionnalité. Lors des fusions, ne supprimer pas les branches.
    - Les branches de fonctionnalité ou de correctif ne sont pas fusionnés directement dans master lorsque le travail est terminé ; elles sont fusionnés dans une branche nommée **develop**
    - Votre dépôt doit contenir l'ensemble des fichiers nécessaires au projet.
    - Il doit égelement contenir un fichier .gitignore.
    - Je veux pouvoir historiser votre travail. C'est le rôle des commits. Faites-en plus que moins 
    
- Le fichier docker-compose.yml qui est dans votre dépôt doit permettre de mettre en place l'ensemble de votre environnement de développment avec ses services, ses volumes (en bind mounting) et son propre réseau virtuel.
    - Voici un exemple des sections que doit comprendre votre fichier docker-compose :
        ```Dockerfile

        version: '3'
        
        services :
          ServeurWeb:
            image:
            command:
            environnement:
            volumes: 
        
          ServeurBD:
         
          ServeurWorPress:

        volumes :
          db-data: 
          www-data:
          wordpress:

        networks :
          MonSiteWeb:
        ```
    - Bien-sur, vous devez aussi fournir les fichiers dockerfile nécessaire.
    
- Une vidéo d'environ 5 mins (Maximum 10 mins) :
  - Explication de votre fichier docker-compose et des fichier dockerfile.
  - Démonstration que le site fonctionne
  - Démonstration que vous êtes sur un réseau virtuelle séparé.
  

À se rappeler :

- Vous aurez besoin d'un volume persistant pour la base de données et pour le serveur Web.
- Il faut passer les informations de la base de données à Wordpress et à MySQL par des variables d'environnement


Références à lire :

- [Git Cheatsheet ](https://ndpsoftware.com/git-cheatsheet.html#loc=local_repo;)pour bien comprendre les différentes état de GIt
- [Les branches avec Git - Les branches en bref](https://git-scm.com/book/fr/v2/Les-branches-avec-Git-Les-branches-en-bref)
- [GIT, GitFlow et l’intégration continue pour les nuls](https://jp-lambert.me/git-gitflow-et-lint%C3%A9gration-continue-pour-les-nuls-a0b2f0b7c788)

- https://hub.docker.com/_/mysql
- Outils d'enregistrement : OBS, Screencast-o-matic, etc.

