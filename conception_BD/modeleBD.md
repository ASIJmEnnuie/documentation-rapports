# Schéma relationnel base de donnée #
### Ce modèle doit pouvoir couvrir le projet jusqu'à la version 3.
### (La clé primaire de chaque table est représentée en gras)


Activite (__id__, nom, adresse, description, site, id_admin_derniere_modif, date_derniere_modif)

Evenement (__id_evt__, id_act, date_evt, heure, description, nb_inscrits, nb_places, nom, id_orga, prix)

Compte (__id__, nom, prenom, date_naissance, genre, email, mot_de_passe, flag_suppression)

Admin (__id__, id_compte, date_debut, date_fin)

Categorie (__id__, nom, id_img)

Image (__id__, chemin)

Image_Activite (__id_act, id_img__, est_principale)

Image_Evenement (__id_evt, id_img__, est_principale)

Image_Compte (__id_compte, id_img__, est_principale)

Collaborateur_Evenement (__id_evt, id_compte__)

Participant_Evenement (__id_evt, id_compte__)

Catégorie_Activite (__id_act, id_cat__)

Categorie_favorite_Compte (__id_cat, id_compte__)

Ami (__id_compte1, id_compte2__)
