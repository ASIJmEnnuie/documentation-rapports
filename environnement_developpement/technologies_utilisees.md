# Technologies utilisées

## Client:

* [Sass](http://sass-lang.com) (Syntactically Awesome StyleSheets) est un métalangage compilé de génération dynamique de feuilles de style en cascade (_CSS_). Il permet de simplifier grandement le développement du code _CSS_ notamment par l'utilisation de variables ou de fonctions.


* [Sass-JSON-vars](https://github.com/vigetlabs/sass-json-vars) afin de pouvoir importer des données au format _JSON_ dans les feuilles de style _Sass_. Cela apporte l'avantage de pouvoir partager des constantes entre le code _Sass_ correspondant à l'apparence de l'application web, et le code _JavaScript_ correspondant à son comportement. Les variables exploitées sont stockées dans le fichier [evASIon/client/src/ressources/data/parameters.json](https://github.com/ASIJmEnnuie/evASIon/blob/master/client/src/ressources/data/parameters.json).


* [npm](https://www.npmjs.com) pour la récupération des différents modules, ainsi que leurs dépendances, nécessaires au développement du projet. En voici une liste non exhaustive:

  * [Babel](https://babeljs.io) afin de pouvoir programmer en _JavaScript ES2015_, indispensable lorsqu'on utilise le framework _ReactJS_.

  * [Webpack](https://webpack.github.io/docs/) qui est un "module bundler" (génère une représentation statique à partir de modules et de leurs dépendances) permettant une approche modulaire du projet. Couplé à babel, c'est par son biais que l'on "compile" le code _JavaScript ES2015_ en code _JavaScript_ interprétable par tous les navigateurs (ces derniers n'ont pas encore incorporé toutes les nouveautés de cette version).

  * [ReactJS](https://facebook.github.io/react/index.html) qui est le framework que nous avons choisi d'utiliser pour le développement de l'interface web du projet.
  En effet, développé par Facebook, il permet le développement rapide d'application web monopage, via la création de composants dépendant d'un état et générant une page (ou portion) HTML à chaque changement d'état.
  _ReactJS_ est une bibliothèque qui ne gère que l'interface de l'application, considéré comme la vue dans le modèle MVC. ([cf wikipédia](https://fr.wikipedia.org/wiki/React_(JavaScript))

  * [Material-UI](http://www.material-ui.com#/) est une librairie _JavaScript_ constituée d'une liste de composants _ReactJS_ implémentant les [spécifications matérial design de Google](https://material.io/guidelines/material-design/introduction.html). Elle nous a permis de débuter le projet avec une liste importante de composants pré-faits (boutons, barres de navigation, ect ...) réduisant grandement le temps de développement du projet.

  * [JSON-Loader](https://github.com/webpack/json-loader) est un plugin de webpack permettant d'importer des données de fichiers locaux au format _JSON_. Cette librairie nous était necessaire afin de partager des données entre le code _Sass_ et _JavaScript_. Dans le cas normal, la récupération de ce type de données nécessiterait l'utilisation d'_AJAX_. Ces données serait par conséquent uniquement récupérées à l'exécution du script. En passant par _webpack_, cela présente l'intérêt d'être récupéré à la compilation.

  * [Nuka-Carousel](https://github.com/FormidableLabs/nuka-carousel) est une librairie permettant la génération de carrousels sous la forme de composants _ReactJS_. Nous avons essayés plusieurs librairies proposant les mêmes fonctionnalités, telle que [React Slick](https://github.com/akiran/react-slick), avant de fixe notre choix. En effet, elle présente l'avantage d'être facile d'utilisation et aisément personnalisable.  

  * [StompJS](http://jmesnil.net/stomp-websocket/doc/) et [SockJS-client](https://github.com/sockjs/sockjs-client) afin d'assurer la connexion entre le client _JavaScript_ et le serveur _Java_. Ces librairies permettent de communiquer à l'aide de _websockets_ utilisant le protocole _STOMP_. Pour de plus amples informations, veuillez vous référer au document [documentation-rapports/percee_technique/websockets.md](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/percee_technique/websockets.md)


* [gulp](http://gulpjs.com) pour l'automatisation de tâches:
  * compilation des fiches de style écrites en _Sass_ vers du _CSS_

  * compilation du code _JavaScript_ à l'aide de _Webpack_

  * minification des fichiers _JavaScript_, _HTML_ et _CSS_

  * actualisation de la page web (nécessite l'ajout d'une extension sur le navigateur web) lors de la sauvegarde des fichiers de développement


## Serveur:

  * [maven](https://maven.apache.org) est un logiciel de gestion et d'automatisation de projet Java. Il est basé sur le concept de Project Object Model (POM) qui permet de réunir dans un même fichier (pom.xml) la description d'un projet avec ses dépendances et les directives à suivre pour les installer, telles que la structure, les versions ou encore les bibliothèques souhaitées.

	Pour Evasion, Maven nous a permis de faciliter l'automatisation de la compilation et du déploiement du serveur, ainsi que de gérer toutes les dépendances et les plugins nécéssaires au projet afin que tous les membres du groupe aient les mêmes technologies et les mêmes versions tout au long du développement.


  * [spring-boot](http://projects.spring.io/spring-boot) est une solution du framework Java _Spring_ permettant la création autonome d'applications nécessitant très peu de configuration. Nous avons plus particulièrement utilisé _Spring Data JPA_ qui donne la possibilité d'utiliser facilement des applications nécessitant l'usage de technologies d'accès aux données.


  * [PostgreSQL](https://www.postgresql.org/) est un système de gestion de bases de données relationnelles objet. Il nous a permis d'implémenter nos données selon un [schéma relationnel](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/conception_BD/modeleBD.md) que nous avons dû définir.

	Notre choix de SGBD s'est tout d'abord porté sur [MySQL](https://www.mysql.fr/) mais nous avons rencontré des problèmes de dépendances au lancement du projet. Nous avons également testé [MariaDB](https://mariadb.com/), une alternative à MySQL développée après son rachat, mais les résultats n'étaient pas plus concluants.


## Ensemble du projet:

* [docker](https://www.docker.com/what-docker) permet d'automatiser le déploiement d'applications dans des conteneurs logiciels. Il peut empaqueter une application et ses dépendances dans un conteneur isolé, qui pourra être exécuté sur n'importe quelle machine Linux, MacOS ou Windows. Ceci permet d'étendre la flexibilité et la portabilité d’exécution d'une application ([cf wikipedia](https://fr.wikipedia.org/wiki/Docker_(logiciel)).

  Dans notre cas, docker a permis à tous les développeurs d'avoir aisément un environnement de développement identique, et de déployer rapidement des serveurs (web, base de données).

  C'est à partir d'un fichier portant le nom Dockerfile que l'on peut créer un container _docker_. Au sein de ce dernier, des mots clés permettent de définir l'ensemble des paramètres du container, comme les ports utilisées, ou encore les commandes exécutées au lancement.


* [docker-compose](https://docs.docker.com/compose/) est une extension de docker permettant de définir et de démarrer des applications docker "multi-container". Les containers peuvent ainsi partager des fichiers ou un domaine de diffusion (au niveau réseau). Cela permet également de démarrer en une seule fois l'ensemble des containers docker d'un projet.

  De plus, les commandes bash de docker étant souvent assez longues et complexes, docker-compose nous permet par le biais d'un fichier docker-compose.yml de définir de manière beaucoup plus intuitive la configuration d'exécution des containers (redirection de ports, définition des répertoires partagées entre la machine hôte et le container, ect ...)

  Merci de vous référer au fichier [containers_docker.md](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/environnement_developpement/containers_docker.md) pour de plus amples informations sur l'utilisation et la configuration de docker au sein de ce projet.
