# Exécution du projet

Afin de lancer le projet, il est nécessaire que les technologies suivantes soient à minima installées sur la machine hôte:

* [docker](https://www.docker.com/products/overview)
* [docker-compose](https://docs.docker.com/compose/install/)
* [java](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) (7 ou 8)
* [maven](https://maven.apache.org)

La première étape consiste à récupérer les sources du projet:
```bash
$ git clone https://github.com/ASIJmEnnuie/evASIon.git
```

L'étape suivante consiste à récupérer les dépendances de la partie client, à compiler cette partie, à lancer le serveur web ainsi que le serveur de base de données _postgresql_.
Toutes ces tâches sont exécutées à l'aide d'images _docker_:
```bash
$ mkdir evASIon/client/dist  # cette commande est facultative, mais préférable afin d'éviter des problèmes ultérieurs de droits d'accès
$ cd evASIon
$ docker-compose build  # cette étape peut être assez longue puisqu'elle nécessite le téléchargement de plusieurs images docker et l'installation de nombreuses dépendances pour l'image "compilator"
$ docker-compose up
```
Merci de vérifier que les ports __9090__ (serveur web), __8080__ (serveur java) et __5432__ (base de données) sont libres sur la machine hôte.

La dernière étape consiste à lancer le serveur java. Dans un nouveau terminal, exécutez les commande suivantes:

```bash
$ cd evASIon/server
$ mvn spring-boot:run
```

Vous pouvez maintenant vous connecter à l'adresse [http://localhost:9090](http://localhost:9090).
