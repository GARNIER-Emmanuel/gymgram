1. Objectif & Cible
Cible : 2 utilisateurs (toi et ton "gym partner").

Concept : Un carnet d'entraînement partagé où chacun voit automatiquement les séances de l'autre pour se motiver mutuellement.

2. Fonctionnalités Principales
A. Authentification & Profil
Login/Register : Simple (Email/Mdp).

Profil : Nom, Photo de profil, Stats perso (Poids, Max).

B. Le "Feed Global" (Cœur social simplifié)
Au lieu d'un algorithme complexe d'abonnements, c'est une simple Timeline Commune.

Affichage : Une seule page "Accueil" qui liste toutes les séances postées par les utilisateurs, triées de la plus récente à la plus ancienne.

Contenu d'un post :

Auteur de la séance.

Résumé (ex: "Pectoraux - 1h10").

Carrousel de photos (optionnel).

Détail des perfs clés (ex: "100kg x 5 au Couché").

Interactions :

Bouton Like (encouragement rapide).

Espace Commentaires (pour le debrief ou le chambrage entre vous deux).

C. Module "Séance" (Saisie)
Créer une séance : Date, Heure de début/fin.

Ajout Exercices :

Muscu (Machine/Poids libre) : Poids, Reps, Repos.

Cardio : Temps, Distance.

Validation : Une fois la séance "Terminée", elle est automatiquement publiée sur le Feed Global.

D. Module "Données Perso" (Privé ou Partagé)
Suivi Poids : Saisie du poids + Photo (la photo peut être privée ou postée sur le feed au choix).

Nutrition : Un champ unique "Total Kcal Jour".

E. Statistiques (Bouton "Stats")
Graphique d'évolution du poids.

Graphique de volume d'entraînement.

Graphique Nutrition (Kcal).

(Pas de classement/leaderboard, juste tes courbes face à toi-même).

3. Simplification Technique (Bonne nouvelle pour toi)
Puisqu'il n'y a que 2 personnes et un seul feed, la base de données (BDD) et le code sont beaucoup plus simples :

Plus besoin de table "Abonnements/Followers" : Tu n'as pas à gérer qui suit qui.

Requête SQL simplifiée :

Au lieu de : "Cherche les posts des gens que je suis".

Tu fais juste : SELECT * FROM posts ORDER BY created_at DESC. (Prends tout et trie par date).

Moins de logique backend : Pas de gestion de confidentialité complexe (Profil privé/public), tout est visible entre vous deux.