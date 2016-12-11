# Scéma relationnel base de donnée #
### Ce modèle doit pouvoir couvrir le projet jusqu'à la version 3.
### (La clé primaire de chaque table est représentée en gras)


Activite (__id__, nom, adresse, description, site, idAdminDerniereModif, dateDerniereModif)

Evenement (__id__, idAct, nom, lieu, idOrga, date, heure, description, nbInscrits, nbPlaces, prix)

Compte (__id__, nom, prenom, dateNaissance, genre, email, motDePasse, flagSuppression)

Admin (__id__, idCompte, dateDebut, dateFin)

Categorie (__id__, nom, idImg)

Image (__id__, chemin)

ImgAct (__idAct, idImg__, estPrincipale)

ImgEvt (__idEvt, idImg__, estPrincipale)

ImgCompte (__idCompte, idImg__, estPrincipale)

CollaborateurEvt (__idEvt, idCompte__)

ParticipantEvt (__idEvt, idCompte__)

CatégorieAct (__idAct, idCat__)

CategorieFavoriteCompte (__idCompte, idCat__)

Ami (__idCompte1, idCompte2__)
