 Pipeline ETL Automatisé : CSV & API vers MySQL

##  Description
Pipeline ETL complet automatisé qui :
- **Extrait** des données depuis fichiers CSV et API REST Countries
- **Transforme** et nettoie les données (jointures, calculs, typage)
- **Charge** les données dans MySQL avec gestion des schémas
- **Automatise** le processus pour minimiser l'intervention manuelle

##  Structure du Projet

### 1. Configuration (`config/`)
- `.env` : Stocke les variables sensibles (identifiants MySQL)
- `requirements.txt` : Liste des dépendances Python

### 2. Données (`data/`)
- `orders.csv` : Commandes clients (ID, date, client, lieu)
- `details.csv` : Détails commandes (montant, profit, catégorie)
- *(Exemples fournis dans le dossier `/sample_data`)*

### 3. Notebook Principal (`ETL_Pipeline.ipynb`)
- **Extraction** :
  - Lecture des CSV avec pandas
  - Appel à l'API REST Countries
- **Transformation** :
  - Fusion des données
  - Calcul de métriques (marge de profit)
  - Nettoyage (dates, valeurs manquantes)
- **Chargement** :
  - Création automatique des tables
  - Insertion incrémentielle
- **Validation** :
  - Requêtes de vérification
  - Détection d'anomalies

### 4. Fonctions Clés
- `setup_database()` : Initialise la base MySQL
- `load_data_to_mysql()` : Charge avec typage automatique
- `run_validation_queries()` : Vérifie l'intégrité des données

##   Technologies
- **Langage** : Python 3
- **Bibliothèques** : Pandas, SQLAlchemy, Requests
- **Base de données** : MySQL (XAMPP)
- **Outils** : Jupyter Notebook

##  Installation
1. Cloner le dépôt
2. Installer les dépendances :
   ```bash
   pip install -r requirements.txt
   ```
3. Configurer `.env` avec vos identifiants MySQL
4. Démarrer XAMPP et activer MySQL

##  Fonctionnalités Clés
-  Création automatique des tables
-  Synchronisation incrémentielle
-  Vérification des doublons
-  Logs détaillés à chaque étape
-  Compatible SQLAlchemy 2.x


  ```markdown
  ## 🔧 Configuration Requise
  - XAMPP avec MySQL
  - Python 3.8+
  - Compte API REST Countries (gratuit)
  ```
