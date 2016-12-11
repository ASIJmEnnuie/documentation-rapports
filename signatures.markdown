# Liste des Signatures des méthodes utilisées pour les version 1 et 2 d'Evasion

## Gestion d'évènements

Fonction Recherche d'évènements avec critère(s):
```
@MessageMapping("/evenements")
@SendTo("/topic/listeEvenements")
public List<Evenement> getEvents(String name, String date, 
               String category, String price, String place,
       				 String time, String activity, String proximity)
```

Fonction Recherche de tous les évènements :
```
@MessageMapping("/allEvenements")
@SendTo("/topic/listeAllEvenements")
public List<Evenement> getAllEvents()
```

Fonction Ajout d'un évènement : (possibilité d'ajouter le prix éventuellement)
```
@MessageMapping("/ajoutEvenements")
@SendTo("/topic/creationEvenements")
public Long AddEvents(String activity, String name, String place, 
									 		String date, String time, String nbPlaces, 
                      String description) {
```

## Gestion d'activités
addActivity
getActivities
getAllActivities

## Gestion utilisateurs
connexion
inscription
