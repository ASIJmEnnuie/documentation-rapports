# Liste des Signatures des méthodes utilisées pour les version 1 et 2 d'Evasion

## Gestion d'évènements
Noms attributs :

	private Long id_evt;
    private String nom_evt;
    private String lieu_evt;
    private String orga_evt;
    private String date_evt;
    private String heure_evt;
    private String desc_evt;
    private int nb_insc_evt;
    private int nb_places_evt;
    private String image_evt;
    private String price;
    private String activite;
    
Fonction Recherche d'évènements avec critère(s):
```
@MessageMapping("/evenementsAvecCritere")
@SendTo("/topic/listeEvenementsCritere")
public List<Evenement> getEvents(String name, String date, 
               String category, String price, String place,
       				 String time, String activity, String proximity)
```

Fonction Recherche de tous les évènements :
```
@MessageMapping("/evenements")
@SendTo("/topic/listeEvenements")
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
