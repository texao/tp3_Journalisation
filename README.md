# Application de journalisation et d'observabilité

## Description
Ce projet est une application backend développée en Java, intégrant des fonctionnalités de journalisation avec de la bibliothèque **Log4j2**. L'objectif principal est de capturer et d'analyser les actions des utilisateurs pour générer des profils détaillés.

## Prérequis
- **Java** : Version 11 ou supérieure.
- **Bibliothèques nécessaires** :
  - Log4j2
  - Jackson (pour la manipulation des fichiers JSON)
  - Eclipse JDT (utilisation du *Visitor* pour l'analyse du code source)


## Structure du projet 
- **Classes principales** : 
  - `ProductRepository` : Gestion des produits.
  - `UserProfiler` : Création et mise à jour des profils utilisateurs.
  - `MethodVisitor` : Utilisé pour parcourir et injecter des logs dans le code source.
  - `MethodVisitor` : Implémentation du *Visitor* pour analyser et enrichir dynamiquement le code source avec des instructions de log.
- **Répertoires importants** :
  - **Source** : Contient le backend (classes `Product`, `User`, etc.).
  - **UserProfile** : Fichier JSON générés contenant les actions des utilisateurs.
  - **Racine** : Contient les fichiers de code après application du `MethodVisitor`.



## Utilisation 
- Exécutez le fichier `MethodVisitor`. Cela analysera le backend, ajoutera des instructions de log dans les méthodes, et générera les nouveaux fichiers enrichis à la racine du projet.
- Lancez le fichier `Main`. Cela exécutera les scénarios utilisateurs, génèrera un fichier JSON contenant les profils utilisateurs, et affichera les statistiques d'utilisation dans la console.


## Fonctionnalités
- **Journalisation avec Log4j2** :
  - Captures d'événements utilisateurs.
  - Génération de fichiers de logs.
- **Analyse des profils utilisateurs** :
  - Classification des utilisateurs en fonction de leurs actions principales (lecture, écriture, recherche du produit le plus cher).
  - Export des profils sous forme de fichier JSON.
