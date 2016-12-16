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
@SendTo("/topic/eventlistWithCriteria")
public List<Evenement> getEvents(String name, String date, 
               String category, String price, String place,
       				 String time, String activity, String proximity)
```

Fonction Recherche de tous les évènements :
```
@MessageMapping("/events")
@SendTo("/topic/eventlist")
public List<Evenement> eventList()
```

Fonction Ajout d'un évènement : (possibilité d'ajouter le prix éventuellement)
```
@MessageMapping("/ajoutEvenements")
@SendTo("/topic/eventCreation")
public Long AddEvents(String activity, String name, String place, 
									 		String date, String time, int nbPlaces, 
                      String description) {
```

## Gestion d'activités
Noms attributs :

    private Long id_act;
    private String nomAct;
    private String adresse;
    private String description;
    private String site;
    private String id_admin_modif;
    private String date_modif;
    
Fonction Ajout d'une activité :
```
@MessageMapping("/ajoutActivites")
@SendTo("/topic/creationActivites")
public Long AddActivities(String nom, String adresse, 
													String description, String site, 
                          String adminmodif, String datemodif)
```

Fonction d'ajout d'activité avec critère(s) :
```
@MessageMapping("/activitesAvecCritere")
@SendTo("/topic/listeActivitesCritere")
public List<Activite> getActivities(String name, String adress,
																		String description, String website,
                                    String adminmodif, String datemodif) 
```

Fonction Recherche de toutes les activités :
```
@MessageMapping("/activites")
@SendTo("/topic/listeActivites")
public List<Activite> getAllActivities()
```

## Gestion utilisateurs
Noms attributs :

    private Long id;
    private String nom;
    private String prenom;
    private String dateNaissance;
    private String genre;
    private String email;
    private String motDePasse;
    private boolean flagSuppression;
    
Connexion :
```
@MessageMapping("/connexionUser")
@SendTo("/topic/connexion")
public Long connexion(String email, String mdp)
```
Inscription :
```
@MessageMapping("/ajoutCompte")
@SendTo("/topic/userCreation")
public Long AddUser(String nom, String prenom, String dateNaissance,
										String genre, String email, String mdp, 
                                        boolean flagSuppression) 

```


--TODO--
## Utilisation du site
Inscription ou Désinscription à un évenement :
```
@MessageMapping("/attendEvenement")
@SendTo("/topic/attendEvenement")
public Long attendEvenement(String idUser, String idEvt)
```