# Music-Centric Social Network Database

## Description
Ce projet est une base de données relationnelle conçue pour gérer diverses entités et relations liées à un réseau social, TunePulse, centré sur la musique. Il permet à ses utilisateurs de découvrir de nouveaux sons, d'assister à des concerts, d'émettre des avis/notes, de partager des photos/vidéos, de gérer des relations de followers et d'amis, de créer des playlists et de faire des publications. 

Il inclut des scripts pour implémenter la base de données, générer des données fictives, les insérer dans la base de données et des requetes prédéfinies pour différentes manipulations des données.

---

## Contenu

### 1. **Fichier : `base.sql`**
Ce fichier contient :
- Les instructions pour créer toutes les tables nécessaires à la base de données.
- Les données initiales utilisées pour peupler ces tables.

### 2. **Fichier : `requetes.sql`**
- Ce fichier regroupe **20 requêtes SQL** pour interroger et manipuler les données de la base.
- Chaque requête est optimisée pour répondre à des besoins spécifiques du réseau social.

### 3. **Dossier : `Données`**
Le dossier `Données` comprend deux sous-dossiers :
- **`Données_créées`** :
  - Contient **36 fichiers** au format `table.sql`.
  - Chaque fichier correspond aux données d'une table spécifique.
- **`Données_script`** :
  - Contient **26 fichiers Python** au format `table.py`.
  - Ces scripts génèrent les données fictives pour peupler les tables.
  - Certains scripts créent les données de plusieurs tables en une seule exécution, comme le fichier `Tag_FK.py`, qui génère les données pour 5 tables de liaison associées aux tags.

---

## Génération des Données

Les données ont été générées à l'aide de scripts Python, utilisant la bibliothèque `Faker` pour produire des données réalistes et diversifiées. Tous les scripts ainsi que les données générées sont disponibles dans le dossier `Données`.

---

## Utilisation

### Étape 1 : Création de la Base de Données
1. Exécutez le fichier `base.sql` dans votre gestionnaire de base de données pour créer toutes les tables et insérer les données initiales.
   ```bash
   mysql -u [utilisateur] -p [nom_base] < base.sql

### Étape 2 : Generation des données 
2. Utilisez les scripts dans Données_script pour générer ou modifier les données fictives :
   ```bash
   python Données_script/Tag_FK.py

### Étape 3 : Requetes 
3. Chargez et exécutez les requêtes du fichier requetes.sql pour interagir avec la base : 
   ```bash
   mysql -u [utilisateur] -p [nom_base] < requetes.sql

--- 

## Bibliothèque Utilisée pour Générer les Données

**Faker** :
- Génération de données fictives réalistes (noms, adresses, dates, etc.).
- Les scripts Python dans le dossier Données_script s'appuient sur cette bibliothèque.
