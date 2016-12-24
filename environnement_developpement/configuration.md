# Configuration de l'environnement de développement

## Responsables
* [Thibault THEOLOGIEN](https://github.com/MacBootglass) (partie client)

## Technologies utilisées

* [npm](https://www.npmjs.com) pour la récupération des différents modules, ainsi que leurs dépendances, nécessaires au développement du projet. En voici une liste non exhaustive:
  * [Babel](https://babeljs.io) afin de pouvoir programmer en _JavaScript ES2015_, indispensable lorsqu'on utilise le framework _ReactJS_.
  * [Webpack](https://webpack.github.io/docs/) qui est un "module bundler" (génère une représentation statique à partir de modules et de leurs dépendances) permettant une approche modulaire du projet. Couplé à babel, c'est par son biais que l'on "compile" le code _JavaScript ES2015_ en code _JavaScript_ interprétable par tous les navigateurs (ces derniers n'ont pas encore incorporé toutes les nouveautés de cette version).
  * [ReactJS](https://facebook.github.io/react/index.html) qui est le framework que nous avons choisi d'utiliser pour le développement de l'interface web du projet.
  En effet, développé par Facebook, il permet le développement rapide d'application web monopage, via la création de composants dépendant d'un état et générant une page (ou portion) HTML à chaque changement d'état.
  _ReactJS_ est une bibliothèque qui ne gère que l'interface de l'application, considéré comme la vue dans le modèle MVC. (cf [wikipédia](https://fr.wikipedia.org/wiki/React_(JavaScript))
  * [Material-UI](http://www.material-ui.com#/) est une librairie _JavaScript_ constituée d'une liste de composants _ReactJS_ implémentant les [spécifications matérial design de Google](https://material.io/guidelines/material-design/introduction.html). Elle nous a permis de débuter le projet avec une liste importante de composants pré-faits (boutons, barres de navigation, ect ...) réduisant grandement le temps de développement du projet.


* [gulp](http://gulpjs.com) pour l'automatisation de tâches:
  * compilation des fiches de style écrites en _Sass_ vers du _CSS_
  * compilation du code _JavaScript_ à l'aide de _Webpack_
  * minification des fichiers _JavaScript_, _HTML_ et _CSS_
  * actualisation de la page web (nécessite l'ajout d'une extension sur le navigateur web) lors de la sauvegarde des fichiers de développement


* [docker](https://www.docker.com/what-docker)


* [docker-compose](https://docs.docker.com/compose/)
Parler du compilator + du fait qu'il n'y ait pas de container docker pour la partie java + limite les problèmes d'installation sur la machine hôte (gulp + sass + npm + nodejs ...)


* [maven]()


* [spring-boot]()


* [postgresql]()


## Exécution du projet

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

Vous pouvez maintenant vous connecter à l'adresse http://localhost:9090.
