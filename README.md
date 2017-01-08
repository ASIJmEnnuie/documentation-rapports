# evASIon


## Projet

PAO "ASI J'm'ennuie" encadré par M.BAUCHER à l'INSA de Rouen

Équipe composée de :
* Enora Gicquel
* Morgane LEGROS
* Maëva SALLANDRE
* Thibault THEOLOGIEN

Présentation :
Le projet consiste à développer une application web de partage d'événements. evASIon est une plate-forme communautaire culturelle proposant aux utilisateurs la création d’événements quels qu’ils soient - musée, festival, concert, sport collectif, … - lorsqu’ils désirent trouver d’autres personnes avec qui partager leurs envies et loisirs.

Méthode :
* Le projet est dirigé par un cycle de développement en Y, qui consiste à effectuer en parallèle une Analyse fonctionnelle et une Analyse technique afin de passer à la Conception.
* La gestion de projet se fait à l'aide des [outils GitHub, Trello et Slack](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/environnement_developpement/outils.md).


## Analyse fonctionnelle

Le projet a été construit en partant de aucune base, et développé à l'aide de technologies nouvelles pour les membres de l'équipe.

Définition du projet
* Un [remue-méninge](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/analyse_fonctionnelle/brainstorming.md) s'est déroulé le 15/09/2016.
* A partir de celui-ci, une [Liste d'idées](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/analyse_fonctionnelle/liste_idees.md) a été créée.

Objectifs
* Les objectifs du projet sont définis dans le [Cahier de Charges](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/analyse_fonctionnelle/CDC.pdf) :
Création d'une plate-forme web, composée d'une interface d'accueil pour les utilisateurs non connectés permettant de s'inscrire ou de se connecter, puis d'une interface en ligne permettant d'accéder aux fonctionnalités de base de l'application.
Une interface administrateur devait également être mise en place.
* [Liste des exigences qualifiées](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/analyse_fonctionnelle/LEQ.pdf) a été faite à partir de la liste d'idées.
* [Versions](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/analyse_fonctionnelle/versions.md) : A partir de la liste des exigences qualifiées, des versions potentielles ont été définies. Nous avons décidé, en fonction des moyens et du temps disponibles dans ce projet de développer les versions 1 et 2.

Spécifications :
* [Cas d'utilisation](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/analyse_fonctionnelle/usecases.pdf) : Les principaux usecase ont été définis : S'inscrire sur le site / Créer un évènement / S'inscrire à un évènement / Créer une activité.
* DSE :
  * [Maquettes](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/maquettes/maquettes_V2.1.pdf)
* DSI :
  * [Modèle de domaine](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/diagrammes/modele_domaine/modele_domaine_v2.svg)
  * [Modèle de BD](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/conception_BD/modeleBD.md)
  * [Signatures BD](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/signatures.md)


## Analyse technique

Percées techniques :
* [Graphql-Relay](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/percee_technique/graphql-relay.md) ([dépôt](https://github.com/ASIJmEnnuie/PT_React))
* [Reactjs-materialui](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/percee_technique/reactjs-materialui.md) ([dépôt](https://github.com/ASIJmEnnuie/PT_GraphQL))
* [Websockets](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/percee_technique/websockets.md) ([dépôt](https://github.com/ASIJmEnnuie/PT_WebSockets))

Technologies non retenues :
* Graphql
* [Jhipster](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/analyse_technique/jhipster.md)


[Technologies utilisées](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/environnement_developpement/technologies_utilisees.md) :
* Client : Sass, Sass-JSON-vars, npm, Babel, Webpack, ReactJS, Material-UI, JSON-Loader, Nuka-Carousel, StompJS, gulp ;
* Serveur : Maven, Spring-boot, PostgreSQL, MySQL ;
* Ensemble du projet : docker, docker-compose.


## Conception

* [Conteners docker](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/environnement_developpement/containers_docker.md) : Utilisation d'un contener docker pour l'execution du projet.

* Projet : ([dépot evASIon](https://github.com/ASIJmEnnuie/evASIon)) reliant la partie client à la partie serveur.

* Tests : Nous n'avons pas eu le temps ni l'occasion de commencer à faire des tests sur ce projet.


## Produit final

Difficultés rencontrées :
* Temps
* De nombreux problèmes rencontrés pour la partie côté serveur : ...

Points positifs à retenir :
* Nous avons chacun progressé en apprenant de nouvelles technologies ;
* Ce projet nous a appris à faire face à de nouveau problème, et toujours repenser le projet afin d'avancer progressivement ;
* L'architecture du projet a été bien faite, avec la séparation de la partie serveur et de la partie client. L'automatisation de l'exécution du projet a également été un succès, ce qui permettait de faire abstraction de l'environnement de développement ;
* L'application a été développée selon un principe d'accessibilité (responsive design, multilangage, etc).

État final du projet :
* [Suivi projet](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/SuiviProjet.md)
* L'objectif final du projet était d'arriver à faire les versions 1 et 2, cet objectif n'a pas été atteint complétement, du fait que la connexion à la BD n'a pas abouti.

## Perspectives d'avenir

Fonctionnalités à développer en premier lieu :
* Connexion à la BD ;
* Créer l'interface administrateur ;
* Faire des tests.

Idées de développement du projet
* [Maquettes futures](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/maquettes/maquette_version_future/maquettes_Version_Future.pdf)
* [Liste d'idées](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/analyse_fonctionnelle/liste_idees.md)


## Annexes complémentaires

Compte-rendu de réunion :
* [Réunion de lancement](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_1.md)
* [Réunion 2](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_2.md)
* [Réunion 3](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_3.md)
* [Réunion 4](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_4.md)
* [Réunion 5](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_5.md)
* [Réunion 6](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_6.md)
* [Réunion 7](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_7.md)
* [Réunion 8](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_8.md)
* [Réunion 9](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_9.md)
* [Réunion 10](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_10.md)
* [Réunion 11](https://github.com/ASIJmEnnuie/documentation-rapports/blob/master/compte_rendu_reunions/CR_11.md)
