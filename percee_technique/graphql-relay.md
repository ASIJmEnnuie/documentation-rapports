# Percée Technique sur *GraphQL* couplé à *Relay*

## Responsables
* [Maëva SALLANDRE](https://github.com/Lueva)
* [Enora GICQUEL](https://github.com/Kahmeset)

## Résumé
Suite à la réunion de lancement, nous avons pendant deux semaines réalisé une percée technique en utilisant *GraphQL* afin de tester la faisabilité du projet via cette technologie pour le côté serveur. Le but était de réaliser une vue toute simple d'une liste d'utilisateurs grâce à ce langage de requête, avec des données mises en dures dans le code dans un premier temps.   
Le framework *Relay* a été testé également, il permettait de faire communiquer *GraphQL* et *ReactJS* pour la récupération des données.  
Suite aux difficultés rencontrées et dû au fait que les technologies *GraphQL* et *Relay* ne soient à ce jour pas assez mûres (surtout pour une utilisation en Java), nous avons décidé d'abandonner ce langage de requête et de nous concentrer sur l'utilisation de [Websockets](https://github.com/ASIJmEnnuie/PT_WebSockets.git).


Les objectifs de cette percée technique étaient de :

1. Réussir à faire fonctionner l'exemple *GraphQL* et Relay via npm
2. Comprendre et savoir utiliser* GraphQL*
3. Utiliser Java, *GraphQL*et *Relay* afin de permettre au côté client, réalisé en *ReactJS*, d'utiliser une simple requête pour accéder aux données souhaitées. 
4. Du côté client, pouvoir envoyer au serveur une simple requête et afficher une liste d'utilisateurs.


## Difficultés rencontrées
* Installation des dépendances nécessaires pour le fonctionnement de l'exemple d'application avec uniquement *GraphQL*
* Trouver les commandes nécessaires à l'exécution du projet (au lancement du serveur)
* Installation des dépendances necessaires pour faire fonctionner la partie *Relay*
* Documentation très pauvre, notamment pour l'utilisation de *GraphQL* en Java.
* Difficulté de l'utilisation de *GraphQL* : technologie très intéressante et pratique mais le peu de temps disponible pour réaliser le projet et le peu de documentation à disposition ne permettait pas d'obtenir une auto-formation suffisante pour la suite du projet.

## Liens utiles:
* [Dépot](https://github.com/ASIJmEnnuie/PT_GraphQL.git)
* [Langage de requête GraphQL](https://http://graphql.org/)
* [Framework Relay](http://graphql.org/)
