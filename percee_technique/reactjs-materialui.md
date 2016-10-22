# Percée Technique sur *ReactJS* couplé à *Matérial-UI*

## Responsables
* [Thibault THEOLOGIEN](https://github.com/MacBootglass)
* [Enora GICQUEL](https://github.com/Kahmeset)

## Résumé
Dans le but de tester la faisabilité du projet en utilisant *ReactJS* comme framework côté client, une percée technique a été réalisée. Nous avons dû reproduire une portion de la maquette de la page d'accueil en tant qu'utilisateur connecté.
Nous avons choisi de coupler *React* au framework *Material-UI* permettant de récupérer un grand nombre d'éléments *ReactJS* (barre de navigation, bouton, ect ...) déjà stylisés et entièrement personnalisables.

Les éléments et fonctionnalités suivants devaient être présents:
1. barre de navigation (~= Appbar) en haut de la page web
2. bouton de forme circulaire, prenant l'apparance d'une image de profil, dans le coin droit de la barre de navigation
3. click sur le bouton (**fonctionnalité 2**) ouvrant un bandeau de navigation latéral droit, et passant au dessus de la page web.
4. bouton dans dans le coin gauche de la barre de navigation
5. click sur le bouton (**fonctionnalité 4**) ouvrant un bandeau de navigation latéral gauche, décalant le reste du contenu de la page
6. bandeau de navigation latéral gauche ouvert par défaut
7. un seul bandeau de navigation  latéral ne peut être ouvert à la fois
8. carousel d'éléments web formatés
9. responsive-design

## Difficultés rencontrées
* Installation des dépendances necessaires au bon fonctionnement du projet (notamment *docker* et *nodejs*)
* Passage de paramètres entre les différents éléments *ReactJS* créés
* Récupération de paramètres des élèments "owned" (~= fils) d'éléments *ReactJS*
* La **fonctionnalité 5** a été assez longue à mettre en place à l'aide des éléments fournis par *Material-UI* (Drawer). *ReactJS* ne nous laisse pas le choix d'utiliser une autre unité que le pixel pour décaler le contenu de la page. Il était donc difficile d'obtenir un résultat responsive-design. De plus les animations étaient difficilement paramétrables, et par défaut décalées entre le coulissement de la barre de navigation, et le reste du contenu de la page web. Un élément *ReactJS* exploitant du *CSS* a donc été créé.

## Liens utiles:
* [Dépot](https://github.com/ASIJmEnnuie/PT_React.git)
* [Framework ReactJS](https://facebook.github.io/react/index.html)
* [Framework Material-UI](http://www.material-ui.com#/)
