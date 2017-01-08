## Liste d’idées / Liste de fonctionnalités attendues

Vocabulaire :
* Activité : Lieu connu ou activité
* Événement : Événement créé par un utilisateur lié à une activité

Problématique: Application web proposant aux utilisateurs de créer et participer à des évènements liés à des activités culturelles

## Visualisation
* Page d'accueil post-connexion
* Interface de visualisation de toutes les activités
* Interface de visualisation de tous les évènements (qui contiendra le système de recherche d’événement)
* Interface de visualisation d’une activité: description sommaire / lien vers site web (officiel de préférence) / photos (nombre limité à définir) / événements liés / catégories associées
* Interface de visualisation d’un événement: nombre de personnes inscrites / possibilité de limiter le nombre de participants /description sommaire / potentiel lieu (lié à une activité ou juste point géographique) / potentiel prix / date et heure / potentiel lieu de rendez-vous
* Interface de création d’un événement
* Interface de création d’une activité

## Connexion
* Page d’accueil pré-connection
* Interface d’inscription sur page d’accueil (formulaire) : nom / email / mot de passe / date de naissance
* Interface de connection sur page d’accueil
* Interface de visualisation d’un profil utilisateur (ne contenant que les informations renseignées lors de l’inscription)
* Interface administrateur : suppression d’un utilisateur / suppression d’un événement / suppression d’une activité


## Gestion des événements et activités
* Système de recherche d’événements ou d’activité (résultat mis à jour en live)
* Différents critères (ex: Nom, lieux, prix, …)
* Différentes catégories (ex: Divertissement, Visite, Musique, …)
* Résultat de la recherche sous forme de listes
* Fonctionnalité de tri : selon certains critères définis (proximité, date,  …).
* Inscription par un utilisateur à un événement
* Désinscription par un utilisateur à un événement
* Ajout de catégories aux activités (pour les critères de recherche). Hiérarchisation des catégories
* Système de mise à jour des événements par le créateur de l’événement
* Système d’invitation à un événement par un utilisateur


## Idées futures
* Interface de modification d’un profil utilisateur
* Affichage d’informations supplémentaires liées à un événement après inscription de l’utilisateur
* Ajout d’informations facultatives sur les profils utilisateurs (à afficher) : photo / centres d’intérêts  / nombre d’amis / agenda (accessible aux amis)  / photos des événements passés / fil d’actualité
* Ajout de contacts / amis
* Interface de visualisation des contacts / amis
* Interface de recherche d’utilisateurs existants
* Système de recherche global au sein de l’application
* Permettre l’inscription / connexion à partir des réseaux sociaux * populaires (Facebook, Twitter, Google +)
* Vérification de la sécurité du mot de passe lors de l’inscription
* Vérification d’adresse mail à la création du compte
* Interface de visualisation des conditions générales d’utilisation
* Boîte à idées / tickets
* Système de signalement/formulaire d’informations erronées sur une activité
* Système de contrôle lors de l’ajout d’une activité, pour vérifier si l’activité n’existe pas déjà
* Système de signalement pour la mise à jour des activités
* Système de signalement d’événement non approprié, avec informations sur les causes de ce signalement à fournir


##  Fonctionnalités additionnelles
* Système d’ajout de collaborateurs à un événement
* Accès à la mise à jour d’événements par les collaborateurs de l’événements
* Pouvoir définir les événements en publics ou privés (seulement les personnes invitées pourront rejoindre l’évènement)
* Agenda personnel automatique (ajout des événements auquel l’utilisateur est inscrit)
* Historique de l’agenda et des événements
* Système de messagerie instantanée entre utilisateurs
* Système de messagerie instantanée sur les évènements
* Fonctionnalités hors ligne (mise en cache de l’application) : accès au profil / agenda / évènements inscrits
* Géolocalisation de l’utilisateur pour la création ou la recherche d’événements
* Ajout d’un affichage cartographique des emplacements des événements et de l’utilisateur, à l’issu d’une recherche d’événements
* Actualisation en temps réel des événements postés par les utilisateurs (pas besoin de rafraichir la page web)


* Suggestion d'événements personnalisés (en fonction des événements/lieux déjà visités, évènements de ses amis, …)
* Système de partage d’événements/activités à ses amis dans l’appli ou sur des réseaux sociaux
* Notification lors de modifications d’évènements et autres
* Ajout de commentaires/avis sur l’événement passé
* Place pour publicité
* Créer l’application mobile android, apple et windows phone (from scratch ou conversion à partir d’outils comme phonegap ?)
* Système de notes/étoiles sur les activités

## Précisions
* Le créateur d'un événement a les droits de suppression d'un événement, il peut ajouter des collaborateurs. De cette façon tous les collaborateurs ont le droit de modification de l'événement. Le créateur a également le statut de collaborateur.
* Système de signalement d'informations erronées ou fausses sur une activité, présenté sous forme de "formulaire" où l'on peut cocher les informations fausses, donner une précision, et donner l'information à mettre à la place. (genre google map)
* Lors de la suppression d’un compte utilisateur : demande sur ses événements créés : si il veut les supprimer ou passer ses droits de création à un collaborateur ou à un autre utilisateur.
* Par défaut, un événement créé sera associé à une activité “Autre”, et une activité créée sera associée à une catégorie “Autre”.
* La création d’une activité par un utilisateur est soumise à validation d’un administrateur, en attente de cette validation l’activité est créée mais a un statut “enAttenteDeValidation” pour ensuite passer à un statut “validée”
* Multilangue : Activités peuvent être créées dans plusieurs langues, ajout d’un attribut langue, si l’utilisateur choisit le site anglais alors si l’activité existe en anglais elle sera affichée en anglais, sinon ce sera la langue par défaut (à déterminée)
