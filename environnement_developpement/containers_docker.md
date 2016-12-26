# Containers docker

Plusieurs containers _docker_ ont été créées au cours de ce projet, dans le but d'uniformiser l'environnement de développement, et de simplifier le déploiement des applications.

Ainsi, à l'aide d'une unique commande, l'ensemble des dépendances sont téléchargées, le client est compilé puis déployé vers un serveur web local. Un serveur de base données est également créé et des données de test y sont automatiquement injectées.

Voici l'ensembles des containers _docker_ qui ont été conçus au cours du projet (les noms données correspondent aux répertoires contenant les fichiers Dockerfile):

* [compilator](https://github.com/ASIJmEnnuie/evASIon/tree/master/compilator)

  Un intérêt majeur à l'utilisation de _docker_ est de réduire au maximum les problèmes d'installation des logiciels liés au développement sur la machine du développeur. En effet, pour la partie client du projet, bon nombre de logiciels sont nécessaires à la compilation (_Sass_, _NodeJS_, _NPM_, _gulp_).
  Or, un certain nombre de problèmes d'installation, notamment liées au versions desdits logiciels, sont apparus au cours du projet. La création d'un container _docker_ nous abstrayant de ces problèmes c'est donc imposées d'elle même.


* [database](https://github.com/ASIJmEnnuie/evASIon/tree/master/database)

  Ce container permet uniquement l'exécution d'un serveur de base de données _postgesql_ sur le port __5432__. Lors de la première exécution, des tables sont créées par le biais du fichier [evASIon/database/scripts/creation.sql](https://github.com/ASIJmEnnuie/evASIon/blob/master/database/scripts/creation.sql) et des données insérées à partir du fichier [evASIon/database/scripts/insertions.sql](https://github.com/ASIJmEnnuie/evASIon/blob/master/database/scripts/insertions.sql).


* [client](https://github.com/ASIJmEnnuie/evASIon/tree/master/client)

  Ce container permet l'exécution d'un serveur web _nginx_ contenant l'ensemble des fichiers, compilés à partir du container compilator, contenus dans le répertoire evASIon/client/dist

Il est bon de noter que, bien que tous ces containers _docker_ soient exécutables d'un bloc depuis la racine du projet, il est possible en cas de besoin de les démarrer séparément depuis leurs dossiers respectifs. Par exemple, si l'on exécute la commande `docker-compose up` depuis le dossier client, cela lancera uniquement le serveur web contenant la partie client.

Aucune configuration _docker_ n'a été définie pour la partie du serveur _Java_. Il serait bon d'envisager, dans le futur, de palier à ce problème. Cela nous permettrait de nous abstraire totalement d'une installation autre que celle de _docker_. Le serveur _Java_ serait également lancé en même temps que les autres parties du projet.
