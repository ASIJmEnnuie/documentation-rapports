# Technologies utilisées

## Client:

* [npm](https://www.npmjs.com) pour la récupération des différents modules, ainsi que leurs dépendances, nécessaires au développement du projet. En voici une liste non exhaustive:
  * [Babel](https://babeljs.io) afin de pouvoir programmer en _JavaScript ES2015_, indispensable lorsqu'on utilise le framework _ReactJS_.
  * [Webpack](https://webpack.github.io/docs/) qui est un "module bundler" (génère une représentation statique à partir de modules et de leurs dépendances) permettant une approche modulaire du projet. Couplé à babel, c'est par son biais que l'on "compile" le code _JavaScript ES2015_ en code _JavaScript_ interprétable par tous les navigateurs (ces derniers n'ont pas encore incorporé toutes les nouveautés de cette version).
  * [ReactJS](https://facebook.github.io/react/index.html) qui est le framework que nous avons choisi d'utiliser pour le développement de l'interface web du projet.
  En effet, développé par Facebook, il permet le développement rapide d'application web monopage, via la création de composants dépendant d'un état et générant une page (ou portion) HTML à chaque changement d'état.
  _ReactJS_ est une bibliothèque qui ne gère que l'interface de l'application, considéré comme la vue dans le modèle MVC. ([cf wikipédia](https://fr.wikipedia.org/wiki/React_(JavaScript))
  * [Material-UI](http://www.material-ui.com#/) est une librairie _JavaScript_ constituée d'une liste de composants _ReactJS_ implémentant les [spécifications matérial design de Google](https://material.io/guidelines/material-design/introduction.html). Elle nous a permis de débuter le projet avec une liste importante de composants pré-faits (boutons, barres de navigation, ect ...) réduisant grandement le temps de développement du projet.


* [gulp](http://gulpjs.com) pour l'automatisation de tâches:
  * compilation des fiches de style écrites en _Sass_ vers du _CSS_
  * compilation du code _JavaScript_ à l'aide de _Webpack_
  * minification des fichiers _JavaScript_, _HTML_ et _CSS_
  * actualisation de la page web (nécessite l'ajout d'une extension sur le navigateur web) lors de la sauvegarde des fichiers de développement


## Serveur:

  * [maven]()


  * [spring-boot]()


  * [postgresql]()


## Ensemble du projet:

* [docker](https://www.docker.com/what-docker) permet d'automatiser le déploiement d'applications dans des conteneurs logiciels. Il peut empaqueter une application et ses dépendances dans un conteneur isolé, qui pourra être exécuté sur n'importe quelle machine Linux, MacOS ou Windows. Ceci permet d'étendre la flexibilité et la portabilité d’exécution d'une application ([cf wikipedia](https://fr.wikipedia.org/wiki/Docker_(logiciel)).

  Dans notre cas, docker a permis à tous les développeurs d'avoir aisément un environnement de développement identique, et de déployer rapidement des serveurs (web, base de données).

  C'est à partir d'un fichier portant le nom Dockerfile que l'on peut créer un container _docker_. Au sein de ce dernier, des mots clés permettent de définir l'ensemble des paramètres du container, comme les ports utilisées, ou encore les commandes exécutées au lancement.


* [docker-compose](https://docs.docker.com/compose/) est une extension de docker permettant de définir et de démarrer des applications docker "multi-container". Les containers peuvent ainsi partager des fichiers ou un domaine de diffusion (au niveau réseau). Cela permet également de démarrer en une seule fois l'ensemble des containers docker d'un projet.

  De plus, les commandes bash de docker étant souvent assez longues et complexes, docker-compose nous permet par le biais d'un fichier docker-compose.yml de définir de manière beaucoup plus intuitive la configuration d'exécution des containers (redirection de ports, définition des répertoires partagées entre la machine hôte et le container, ect ...)

  Merci de vous référer au fichier [containers_docker.md](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/environnement_developpement/containers_docker.md) pour de plus amples informations sur l'utilisation et la configuration de docker au sein de ce projet.