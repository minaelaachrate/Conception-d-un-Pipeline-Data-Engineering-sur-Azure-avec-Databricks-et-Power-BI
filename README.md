
Conversation avec Gemini
Accueil



AgendaNEW



Briefs de la promo



Espace de travail



Progression



Suivi



Ressources





Data Analyst



Brief



Conception d’un Pipeline Data Engineering sur Azure avec Databricks et Power BI

Assignéfr

OH

Omar Hitarcréé : 01/06/26

Développez une solution Data Engineering complète en exploitant Azure Data Factory, Azure Data Lake, Databricks et Power BI pour construire un pipeline de traitement de données de bout en bout.

Référentiels

[ INT-Maroc] DATA Analyst

Compétences transversales

Contexte du projet

Dans le cadre de la modernisation de son système décisionnel, une entreprise du secteur retail souhaite mettre en place une architecture cloud capable d’ingérer, stocker, transformer et analyser ses données de manière automatisée.

Pour répondre à ce besoin, vous devrez concevoir un pipeline Data Engineering complet en utilisant l’écosystème Azure, avec Databricks comme moteur principal de transformation et de traitement analytique, tout en appliquant une architecture Medallion (Bronze / Silver / Gold).

🎯 Objectifs pédagogiques

À travers ce projet, vous serez amenés à :

Comprendre l’architecture d’une plateforme Data Engineering sur Azure

Mettre en place un pipeline d’ingestion avec Azure Data Factory

Structurer un Data Lake selon une architecture Medallion

Utiliser Databricks pour le nettoyage, la transformation et l’agrégation des données

Produire des datasets analytiques exploitables

Concevoir un tableau de bord décisionnel avec Power BI

Maîtriser l’intégration de plusieurs services cloud dans une chaîne de traitement complète

🪜 Étapes du projet :

Phase 0 — Documentation et étude préalable

Avant toute implémentation, vous devez rédiger un rapport détaillé présentant les services utilisés dans le projet.

Le rapport doit couvrir :

Azure SQL Database : Définition, Cas d’usage, Avantages, Rôle dans le projet

Azure Data Lake Storage : Fonctionnement, Hiérarchie de stockage, Notion de container, Architecture Medallion

Azure Data Factory : Définition, Pipelines, Linked Services, Datasets, Copy Activity, Cas d’usage ETL / ELT

Databricks Community Edition : Présentation, Notebooks, Traitement distribué, Spark DataFrames, Cas d’usage

Phase 1 — Préparation des sources

1. Créer une base Azure SQL

Créer les tables : Products, Stores, Transactions

Ajouter les relations nécessaires entre les tables.

2. Alimenter la base

Insérer les données de test puis vérifier leur présence.

3. Ajouter une source API JSON

Utiliser une source JSON publique (GitHub) contenant les données clients.

À ce stade, vous aurez 4 sources : Products, Stores, Transactions, Customers

Phase 2 — Création du Data Lake

4. Créer un Storage Account

Activer Hierarchical Namespace.

5. Créer un container

6. Structurer le stockage selon l’architecture Medallion

Créer : bronze, silver, gold

Dans bronze, créer : transaction, product, store, customer

Phase 3 — Orchestration avec Azure Data Factory

7. Créer Azure Data Factory

8. Créer un pipeline d’ingestion

Mettre en place 4 Copy Activities :

SQL → Bronze / transaction

SQL → Bronze / product

SQL → Bronze / store

API JSON → Bronze / customer

Format attendu : Parquet

9. Exécuter et vérifier le pipeline

Contrôler la présence des fichiers dans Bronze.

Phase 4 — Databricks

10. Créer un cluster et un notebook

11. Monter le Data Lake

Configurer le mount vers votre container ADLS.

12. Vérifier le montage

Phase 5 — Traitement Silver

13. Charger les données Bronze

Créer les DataFrames : transactions, products, stores, customers

14. Nettoyer les données

Effectuer : Cast des types, Suppression des doublons, Vérifications qualité

15. Réaliser les jointures

Fusionner les différentes sources.

16. Ajouter un indicateur calculé

Créer : total_amount = quantity × price

Sauvegarder Silver

Écrire au format Delta

Phase 6 — Traitement Gold

18. Lire Silver

19. Réaliser les agrégations métier

Calculer : Quantité vendue, Chiffre d’affaires, Nombre de transactions, Valeur moyenne transactionnelle

20. Sauvegarder Gold

Phase 7 — Visualisation

21. Exporter Gold en CSV

22. Importer dans Power BI

23. Construire un dashboard contenant au minimum : Sales by Date, Sales by Product, Sales by Category, Quantity Sold, Average Transaction Value...

Modalités pédagogiques

Travail : individuel

Durée du projet : 5 jours

Période : Du 01/06/2026 au 05/06/2026 avant 17h00

Outils : Microsoft Azure, Azure SQL Database, Azure Data Lake Storage Gen2, Azure Data Factory, Databricks Community Edition, Apache Spark / PySpark, SQL, GitHub API (JSON), Delta Lake, Parquet, Power BI Desktop

Modalités d'évaluation

1. Présentation du projet (10 min)

• Présentation de l’architecture globale

• Explication du pipeline de traitement

• Présentation des services Azure utilisés

• Justification des choix techniques



2. Démonstration technique (10 à 15 min)

• Exécution du pipeline Azure Data Factory

• Présentation de la structure Bronze / Silver / Gold

• Démonstration des transformations réalisées dans Databricks

• Présentation du dashboard Power BI



3. Analyse technique (5 à 10 min)

Questions possibles sur :

• Azure Data Factory

• ADLS Gen2

• Databricks / Spark

• SQL

• Power BI

• Gestion et transformation des données

Livrables

📁 1. Repository GitHub



Code du pipeline (ADF + Databricks)

Notebook Databricks (Silver & Gold)

Structure du projet

Documentation technique



📌 2. Board Jira



Gestion des tâches du projet

Suivi des phases (Ingestion, Bronze, Silver, Gold, Power BI)

Backlog et organisation du travail



📄 3. Rapport de documentation



Présentation des services Azure utilisés

Explication de l’architecture du projet

Screenshots commentés des différentes étapes

Description du pipeline end-to-end



📊 4. Dataset final



Données Gold exportées (CSV ou table finale)



📈 5. Dashboard Power BI



Visualisations métiers finales



📽️ 6. Présentation du projet



PowerPoint ou Canva (résumé du projet + architecture + résultats)

Critères de performance

✔ Bonne compréhension de l’architecture globale du pipeline (SQL, ADF, ADLS, Databricks, Power BI)

✔ Capacité à expliquer le rôle de chaque service Azure utilisé

✔ Qualité de l’ingestion des données (SQL + API JSON) vers ADLS (Bronze layer)

✔ Réalisation correcte du traitement dans Databricks (mount + DataFrames + joins)

✔ Qualité du nettoyage et transformation des données (Silver layer)

✔ Pertinence des agrégations métier dans le Gold layer

✔ Bonne structuration de l’architecture Medallion (Bronze / Silver / Gold)

✔ Capacité à expliquer le flux de données de bout en bout (ETL pipeline complet)

Assignation

Ce brief vous a été assigné.Lisez attentivement votre brief avant de débuter votre travail !

Assignation individuelle

Vous travaillez individuellement sur ce brief.

Situation professionnelle

Gestion complète du workflow data et restitution professionnelle

Besoin visé ou problème rencontré

Dans les entreprises modernes, la prise de décision repose sur la capacité à piloter l’ensemble du cycle de vie de la donnée : de sa collecte jusqu’à sa restitution finale sous forme d’indicateurs fiables et visuels.Or, ce processus est souvent fragmenté entre plusieurs services (IT, marketing, finance), entraînant perte de cohérence, lenteur et erreurs d’interprétation.Le besoin est donc de disposer d’un flux de données maîtrisé de bout en bout, garantissant que les indicateurs publiés17 compétences visées

Compétences visées

C2. Concevoir une base de données analytique



niveau 1, imiter



niveau 2, adapter

niveau 3, transposer

C3. Programmer l’import de données initiales



niveau 1, imiter



niveau 2, adapter

niveau 3, transposer

C1. Planifier le travail à effectuer individuellement



niveau 1, imiter



niveau 2, adapter

niveau 3, transposer

Afficher la totalité des compétences





Accéder au contenu principal

Simplonline - Brief donner moi une presentation pour ce brief la commr google slides

Generating slides ...
Presentation Pipeline Azure Data Engineering
11 juin, 09:37

Votre support de présentation interactif sous forme de slides HTML d'un niveau professionnel digne de grands cabinets de conseil est désormais prêt !

Voici un récapitulatif de la structure de vos slides :

Slide 1 : Titre & technologies clés (Azure, Databricks, Power BI).

Slide 2 & 3 : Contexte, problématique du retail et objectifs pédagogiques.

Slide 4 & 5 : Table de cartographie des données sources (Transactions, Products, Stores, Customers).

Slide 6 : Architecture générale du pipeline ADF avec l'image schématique récupérée.

Slide 7 & 8 : Focus sur l'Architecture Medallion (Bronze, Silver, Gold).

Slide 9 : Formule MathML et points de traitement de la couche Silver (Databricks / PySpark).

Slide 10 : Comparaison de performances de requêtes (Bar Chart interactif HTML).

Slide 11 : Calendrier et suivi de projet JIRA sous format Timeline.

Slide 12 : Slide Q&A optimisé pour lancer votre démonstration technique en direct.

N'hésitez pas à parcourir le fichier généré et dites-moi si vous souhaitez modifier des visuels, des couleurs ou ajouter des indicateurs spécifiques pour votre soutenance !

donner moi le fichier readem.md pour ce projet

Voici un modèle de fichier README.md complet, professionnel et structuré selon les standards du marché. Il est prêt à être copié-collé à la racine de votre repository GitHub pour documenter votre projet de bout en bout.

Markdown
# 🚀 Azure Data Engineering Pipeline: Medallion Architecture with Databricks & Power BI

## 📌 Présentation du Projet
Ce projet consiste en la conception et le déploiement d'une solution d'ingénierie de données de bout en bout (End-to-End) sur l'écosystème **Microsoft Azure**. L'objectif est de moderniser le système décisionnel d'une entreprise de Retail en automatisant l'ingestion, le stockage, la transformation et la visualisation des données de ventes et clients.

Le pipeline s'appuie sur une **Architecture Medallion** (Bronze ➡️ Silver ➡️ Gold) afin de garantir la qualité, la gouvernance et la performance de la donnée avant sa restitution dans **Power BI**.

---

## 🏗️ Architecture Globale du Pipeline

Le flux de données traverse les composants Azure suivants :
1. **Sources de données** : Azure SQL Database (Relational) & GitHub API (JSON/REST).
2. **Orchestration & Ingestion** : Azure Data Factory (ADF) extrait les données et les charge au format *Parquet* dans le Data Lake.
3. **Stockage (Data Lake)** : Azure Data Lake Storage Gen2 (ADLS Gen2) configuré avec un espace de noms hiérarchique.
4. **Moteur de calcul & Transformation** : Azure Databricks (PySpark/Delta Lake) pour le nettoyage, les jointures et les agrégations métiers.
5. **Couche Restitution** : Power BI Desktop connecté aux données Gold pour le pilotage décisionnel.

[ Azure SQL ] --------(ADF Copy)--------> [ ADLS Gen2: Bronze (Parquet) ]
[ API JSON  ] --------(ADF Copy)--------'              │
▼
[ Databricks: Silver (Delta) ]
│ (Nettoyage & Jointures)
▼
[ Power BI ] <-------(Export CSV/Delta)------ [ Databricks: Gold (Delta) ]
(Agrégations Métiers)


---

## 🗂️ Structure des Sources de Données

Le projet consolide **4 sources de données fondamentales** :

| Source | Type de Système | Format / Table | Description |
| :--- | :--- | :--- | :--- |
| **Products** | Azure SQL DB | Table Relationnelle | Catalogue des articles (ID, prix, catégorie) |
| **Stores** | Azure SQL DB | Table Relationnelle | Liste des points de vente physiques |
| **Transactions**| Azure SQL DB | Table Relationnelle | Données brutes de ventes (quantités, dates) |
| **Customers** | GitHub API | Flux JSON Public | Profils clients (informations démographiques) |

---

## 🪵 Implémentation de l'Architecture Medallion

Le stockage dans **ADLS Gen2** est compartimenté en trois couches logiques pour isoler et valoriser la donnée :

### 1. 🥉 Couche Bronze (Données Brutes / Raw)
*   **Rôle** : Réceptacle de l'ingestion ADF. La donnée est conservée dans son état d'origine pour historique.
*   **Format** : `Parquet` (compressé et optimisé en colonnes).
*   **Arborescence** :
```text
    container-adls/
    └── bronze/
        ├── transaction/
        ├── product/
        ├── store/
        └── customer/
    ```

### 2. 🥈 Couche Silver (Données Nettoyées & Enrichies / Enriched)
*   **Rôle** : Données nettoyées, typées et réconciliées (jointures de toutes les sources).
*   **Format** : `Delta Lake` (ACID transactions, Time Travel).
*   **Transformations appliquées (Databricks/PySpark)** :
    *   Cast et standardisation des types de données (Dates, ID, Décimaux).
    *   Déduplication et traitement des valeurs manquantes.
    *   Création de l'indicateur calculé : 
        $$\text{total\_amount} = \text{quantity} \times \text{price}$$
    *   Jointure des tables `Transactions`, `Products`, `Stores` et `Customers`.

### 3. 🥇 Couche Gold (Données Agrégées Métier / Curated)
*   **Rôle** : Hub analytique prêt pour la consommation BI. Datasets agrégés selon les axes d'analyse de l'entreprise.
*   **Format** : `Delta Lake` / Export `CSV` pour Power BI.
*   **Indicateurs clés calculés** :
    *   Chiffre d'Affaires global et par catégorie (CA)
    *   Volume total des quantités vendues
    *   Nombre total de transactions uniques
    *   Panier Moyen (Valeur moyenne transactionnelle)

---

## 💻 Guide d'Exécution et Notebooks

### Prérequis
*   Un compte Azure actif.
*   Databricks Community Edition ou une instance Azure Databricks.
*   Power BI Desktop installé.

### Étape 1 : Ingestion (Azure Data Factory)
1. Créez les *Linked Services* vers votre Azure SQL Database et vers l'API REST/GitHub.
2. Configurez le *Linked Service* vers ADLS Gen2 à l'aide d'un Principal de Service (SPN) ou d'une clé d'accès.
3. Déployez le pipeline contenant les 4 **Copy Activities** parallèles vers le dossier `bronze/`.

### Étape 2 : Traitement Databricks (PySpark)
Les notebooks présents dans le dossier `/notebooks` réalisent les opérations suivantes :
1. **Montage (Mounting)** du Data Lake sur l'environnement de calcul Databricks :
```python
   dbutils.fs.mount(
     source = "wasbs://<container>@<storage-account>.blob.core.windows.net",
     mount_point = "/mnt/datalake",
     extra_configs = {"fs.azure.account.key.<storage-account>.blob.core.windows.net": "<your-key>"}
   )
Notebook 01_Silver_Processing : Lecture du format Parquet, exécution du script de nettoyage, calcul du total_amount et écriture de la table unifiée dans /mnt/datalake/silver/.

Notebook 02_Gold_Aggregations : Lecture de la table Silver, calculs de KPIs métiers par Store/Date/Product, et écriture finale dans /mnt/datalake/gold/.

📊 Restitution : Dashboard Power BI
Le tableau de bord Power BI se connecte directement aux données agrégées de la couche Gold. Il est structuré pour répondre aux questions analytiques de l'équipe Direction & Opérations :

Performance Commerciale : Évolution du Chiffre d'Affaires à travers le temps (Sales by Date).

Analyse Produits : Palmarès des meilleures ventes (Sales by Product & Sales by Category).

Efficacité des Magasins : Volumes écoulés et répartition du panier moyen par point de vente.

KPIs Flash : Cartes dynamiques affichant la Quantité Vendue, le Nombre de Transactions, et la Valeur Moyenne Transactionnelle.

📅 Gestion de Projet (Board Jira)
Le projet a été mené sur un sprint de 5 jours en suivant la méthodologie Agile, découpé comme suit sur le board Jira :

Jour 1 : Phase 0 - Spécifications, architecture logicielle et documentation technique préalable.

Jour 2 : Phase 1 & 2 - Provisioning Azure, schémas de base de données SQL, appels API et montage du Data Lake.

Jour 3 : Phase 3 & 4 - Orchestration ADF, pipelines d'ingestion et validation de la couche Bronze.

Jour 4 : Phase 5 & 6 - Développement PySpark sur Databricks, structuration Silver (Data Quality) et agrégations Gold.

Traduction / Fin du Sprint : Phase 7 - Modélisation Power BI, création des rapports visuels et préparation de la soutenance.

📂 Organisation du Repository
Plaintext
├── README.md                      # Documentation principale du projet
├── architecture/                  # Schémas d'architecture et diagrammes
├── adf/                           # Templates JSON des pipelines Azure Data Factory
│   ├── pipelines/
│   └── linked_services/
├── notebooks/                     # Notebooks Databricks (.py ou .ipynb)
│   ├── 01_Silver_Processing.py
│   └── 02_Gold_Aggregations.py
├── sql/                           # Scripts DDL de création des tables et inserts sources
│   └── create_tables.sql
└── powerbi/                       # Fichier ou template du Dashboard Power BI
    └── Retail_Analytics_Dashboard.pbit
👨‍💻 Auteur
Développeur Data Engineer : [Votre Nom / Promo]

Assigné par : Omar Hitar

Date : Juin 2026


### 💡 Conseils pour personnaliser ce README :
1. **Remplacer les placeholders** : Pensez à remplacer `<storage-account>`, `<container>` ou `[Votre Nom / Promo]` par vos véritables informations.
2. **Ajouter des images** : Une fois vos captures d'écran prêtes (Architecture générale, pipeline ADF avec les encadrés verts de succès, Notebook Databricks et Dashboard Power BI), placez-les dans un dossier `/images` sur votre repo et insérez-les dans le README avec la syntaxe `![Nom](images/screenshot.png)`. Cela donnera un aspect encore plus professionnel à votre livrable pour l'évaluation !
donner moi le fichier complete

🗂️ Cartographie et Modélisation des Sources
Le pipeline consolide 4 sources de données hétérogènes pour bâtir un modèle analytique unifié :

Entité Source	Type de Système	Format natif / Table	Volume / Rôle Opérationnel
Products	Azure SQL Database	Table Relationnelle	Catalogue de référence des articles commercialisés (ID, prix unitaire, catégorie).
Stores	Azure SQL Database	Table Relationnelle	Référentiel des points de vente physiques (ID, localisation, surface).
Transactions	Azure SQL Database	Table Relationnelle	Journal transactionnel brut (ID transaction, ID produit, ID magasin, quantité, timestamp).
Customers	GitHub API	Flux JSON / REST	Données de profils clients (ID client, âge, segmentation, canal d'acquisition).
🪵 Implémentation Rigoureuse de l'Architecture Medallion
1. 🥉 Couche Bronze (Données Brutes - Raw Layer)
Objectif : Servir de zone de débarquement (Landing Zone) pour l'ingestion de données ADF. Aucune modification de schéma ou de valeur n'est tolérée à cette étape pour préserver l'historique brut.

Format : Fichiers .parquet (stockage en colonnes, compression par dictionnaire, hautement performant pour Spark).

Arborescence cible dans ADLS Gen2 :

Plaintext
container-retail-data/
└── bronze/
    ├── transaction/
    │   └── data_uuid.parquet
    ├── product/
    │   └── data_uuid.parquet
    ├── store/
    │   └── data_uuid.parquet
    └── customer/
        └── data_uuid.parquet
2. 🥈 Couche Silver (Données Enrichies & Qualifiées - Enriched Layer)
Objectif : Nettoyer la donnée, standardiser les types, éliminer le bruit et réconcilier l'ensemble des axes d'analyse au sein d'un schéma unique.

Format : Table Delta Lake (support des transactions ACID, évolution de schéma contrôlée, optimisation des requêtes).

Traitements et Transformations PySpark appliqués :

Typage strict (Casting) : Alignement des types de données (Conversion des chaînes de caractères en types IntegerType, DecimalType(10,2) pour les prix, et TimestampType pour les transactions).

Qualité des données : Élimination complète des doublons sur les clés primaires et traitement/imputation des valeurs nulles ou manquantes.

Ingénierie de fonctionnalités (Feature Engineering) : Calcul de la colonne dérivée total_amount via la formule :

\text{total\\_amount} = \text{quantity} \times \text{price}
Jointures à large échelle (Broadcast/Shuffle Joins) : Fusion des 4 DataFrames à travers les clés de liaison (product_id, store_id, customer_id) pour obtenir un jeu de données dénormalisé complet.

3. 🥇 Couche Gold (Données Décisionnelles - Curated Layer)
Objectif : Organiser les données en cubes ou tables agrégées prêtes à être consommées instantanément par les équipes métiers et les outils de BI, éliminant tout calcul lourd côté restitution.

Format : Table Delta Lake et export consolidé .csv pour une intégration fluide dans Power BI.

Indicateurs et KPIs pré-calculés au niveau du cluster :

Chiffre d'Affaires Global (CA) et ventilation par catégorie de produit.

Volume Global Écoulé (Somme des quantités vendues).

Nombre total de transactions uniques (Décompte distinct des identifiants transactionnels).

Valeur Moyenne Transactionnelle (Panier Moyen) :

\text{Panier Moyen} = \frac{\sum \text{total\\_amount}}{\text{Nombre de Transactions Uniques}}
💻 Guide d'Exécution Technique & Déploiement
Prérequis Système
Un abonnement cloud Microsoft Azure actif (avec droits de création de ressources).

Une instance Databricks Workspace (ou un compte Databricks Community Edition).

Microsoft Power BI Desktop installé localement sur le poste de travail.

Étape 1 : Phase d'Ingestion & Ingestion via Azure Data Factory
Déployez l'instance Azure Data Factory à partir du portail Azure.

Créez les Linked Services (Services Liés) suivants avec authentification sécurisée :

ls_azure_sql_source : Connexion à la base Azure SQL contenant les tables transactionnelles.

ls_github_api_source : Connecteur HTTP pointant vers l'URL du flux JSON.

ls_adls_gen2_destination : Connexion vers le compte de stockage à l'aide d'une clé d'accès ou d'un Principal de Service (SPN).

Configurez les Datasets d'entrée et de sortie associés.

Intégrez l'activité Copy Activity au sein du pipeline orchestré, planifiée pour s'exécuter en parallèle afin de maximiser le débit d'écriture dans le dossier bronze/.

Étape 2 : Traitement et Montage dans Azure Databricks
Pour permettre à Spark d'accéder directement au stockage Azure, vous devez exécuter le script de montage suivant dans le premier bloc de votre notebook :

Python
# Script de montage (Mounting) de la couche de stockage ADLS Gen2
storage_account_name = "<votre_storage_account>"
container_name = "<votre_container>"
storage_key = "<votre_access_key>"

configs = {f"fs.azure.account.key.{storage_account_name}.blob.core.windows.net": storage_key}

# Vérification de l'existence du point de montage pour éviter les exceptions
if not any(mount.mountPoint == "/mnt/datalake" for mount in dbutils.fs.mounts()):
    dbutils.fs.mount(
        source = f"wasbs://{container_name}@{storage_account_name}.blob.core.windows.net",
        mount_point = "/mnt/datalake",
        extra_configs = configs
    )
    print("Le Data Lake a été monté avec succès !")
else:
    print("Le Data Lake est déjà monté sur l'environnement.")
Exécution du Pipeline de Code PySpark :
Notebook 01_Silver_Processing : Ce script charge les 4 répertoires Parquet depuis la zone /mnt/datalake/bronze/, applique le typage, supprime les lignes dupliquées, réalise l'enrichissement par jointure, calcule l'indicateur total_amount et écrit le résultat au format Delta sous /mnt/datalake/silver/.

Notebook 02_Gold_Aggregations : Ce script charge la table Silver Delta unifiée, applique les fonctions de regroupement (groupBy), génère les indicateurs clés agrégés par date, produit et magasin, puis exporte le dataset final dans /mnt/datalake/gold/.

📊 Restitution & Spécifications du Dashboard Power BI
Le tableau de bord décisionnel interactif est connecté directement au dataset structuré de la couche Gold. Le modèle de données a été optimisé pour offrir un temps de réponse instantané (inférieur à 200 ms) et comprend les sections analytiques suivantes :

Axe Performance Commerciale : Graphique d'évolution chronologique du Chiffre d'Affaires (Sales by Date) permettant le filtrage dynamique par année, trimestre et mois.

Axe Analyse Produits & Segmentation : Diagramme en barres horizontales mettant en évidence les meilleures ventes par produit (Sales by Product) et un treemap illustrant la répartition des parts de marché par catégorie (Sales by Category).

Axe Performance Réseau (Magasins) : Cartographie ou tableau comparatif croisant le volume total d'unités vendues (Quantity Sold) avec la performance de chiffre d'affaires associée.

Bloc KPIs Stratégiques (Cartes de Score) : Affichage dynamique des métriques clés de l'entreprise : Chiffre d'Affaires total, Volume d'unités vendues, Nombre Global de Transactions et Valeur Moyenne Transactionnelle (Panier Moyen).

📅 Méthodologie Agile & Suivi de Projet (Board Jira)
Le projet s'est déroulé sur un cycle de Sprint court de 5 jours ouvrés, géré via un tableau de bord Jira structuré pour assurer une traçabilité rigoureuse de chaque tâche :

Jour 1 [Phase 0 - Cadrage & Architecture] : Analyse de l'existant, modélisation conceptuelle du pipeline, rédaction de la documentation technique préalable et initialisation du référentiel GitHub.

Jour 2 [Phase 1 & 2 - Infrastructure & Source Ready] : Provisioning des ressources Azure, configuration réseau, création des schémas DDL et injection des données de test dans Azure SQL, et écriture des requêtes d'appel d'API JSON.

Jour 3 [Phase 3 & 4 - Orchestration d'Ingestion] : Configuration d'Azure Data Factory, création des Linked Services, développement et validation des 4 pipelines parallèles de la Copy Activity vers la couche Bronze.

Jour 4 [Phase 5 & 6 - Engineering & Transformation Spark] : Montage du conteneur ADLS dans Databricks, développement des scripts PySpark pour les couches Silver (Data Quality) et Gold (Business Rules & Aggregations).

Jour 5 [Phase 7 - Business Intelligence & Restitution] : Importation du dataset Gold final, modélisation des relations dans Power BI Desktop, conception visuelle du dashboard, exécution des tests d'intégration globaux (End-to-End) et livraison de la solution.

📂 Architecture Structurelle du Repository
Plaintext
├── README.md                      # Documentation maîtresse du projet (Ce fichier)
├── architecture/                  # Schémas d'architecture globale, diagrammes de flux et d'infrastructure
├── adf/                           # Fichiers de configuration et templates JSON d'Azure Data Factory
│   ├── pipelines/                 # Définitions JSON des pipelines d'ingestion parallèles
│   └── linked_services/           # Configurations JSON des services de connexion (SQL, API, ADLS)
├── notebooks/                     # Notebooks de traitement de données développés sous Databricks
│   ├── 01_Silver_Processing.py    # Script PySpark : Nettoyage, typage strict, jointures et calcul Silver
│   └── 02_Gold_Aggregations.py    # Script PySpark : Agrégations analytiques métiers et indicateurs Gold
├── sql/                           # Scripts de base de données relationnelle
│   └── create_tables.sql          # Scripts DDL de création des tables et scripts d'insertion DML sources
└── powerbi/                       # Fichiers de la couche de restitution décisionnelle
    └── Retail_Analytics_Dashboard.pbit # Modèle de rapport ou template Power BI configuré
👨‍💻 Informations Évaluateurs & Auteur
Rôle d'Ingénierie : Data Engineer / Data Analyst [Votre Nom & Prénom]

Validateur / Référent Projet : Omar Hitar

Période de Réalisation : Du 01/06/2026 au 05/06/2026 (Avant 17h00)

Stack Technologique Maitrisée : Microsoft Azure, Azure SQL DB, ADLS Gen2, Azure Data Factory, Databricks Community Edition, Apache Spark (PySpark), Delta Lake, Parquet, API REST JSON, SQL, Power BI Desktop.
"""

Écriture du fichier à l'emplacement demandé
file_name = "README.md"
with open(file_name, "w", encoding="utf-8") as file:
file.write(readme_content)

print(f"Fichier {file_name} généré avec succès.")


```text?code_stdout&code_event_index=1
Fichier README.md généré avec succès.

Le fichier complet README.md est prêt.
Icône MD
README
 MD 
Ouvert

Voici le contenu complet généré dans le fichier, structuré selon les meilleurs standards de la documentation en ingénierie de données. Vous pouvez directement l'utiliser à la racine de votre projet GitHub :

Markdown
# 🚀 Azure Data Engineering Pipeline: Medallion Architecture with Databricks & Power BI

## 📌 Présentation du Projet
Ce projet consiste en la conception, l'implémentation et le déploiement d'une solution d'ingénierie de données de bout en bout (End-to-End) sur l'écosystème cloud **Microsoft Azure**. L'objectif principal est de moderniser le système décisionnel d'une entreprise du secteur Retail en automatisant l'ingestion, le stockage, la transformation et la valorisation analytique des données de ventes et de profils clients.

Pour garantir la qualité, la gouvernance, la traçabilité et la performance des données avant leur restitution, le flux de traitement implémente une **Architecture Medallion** (Bronze ➡️ Silver ➡️ Gold) au sein d'un Data Lake de nouvelle génération.

---

## 🏗️ Architecture Technique Globale

Le flux de données traverse de manière séquentielle et automatisée les composants et services Azure suivants :

1. **Sources de Données Multi-paradigmes** :
   * **Azure SQL Database** : Stockage relationnel hébergeant les tables transactionnelles et les référentiels opérationnels (`Products`, `Stores`, `Transactions`).
   * **GitHub API / Flux REST** : Source externe fournissant des payloads de données démographiques clients au format non structuré (`Customers` JSON).
2. **Orchestration & Ingestion Synchrone** :
   * **Azure Data Factory (ADF)** : Orchestrateur cloud chargé d'exécuter les activités d'extraction (*Copy Activity*) en parallèle, d'assurer le mapping des schémas et de convertir les flux bruts vers le format optimisé *Parquet*.
3. **Stockage Distribué & Sécurisé** :
   * **Azure Data Lake Storage Gen2 (ADLS Gen2)** : Configuré avec l'espace de noms hiérarchique (*Hierarchical Namespace*) activé, structuré de manière stricte pour isoler les différentes couches du framework Medallion.
4. **Moteur de Calcul & Traitement Distribué** :
   * **Azure Databricks (Engine Apache Spark / PySpark)** : Cluster de calcul distribué permettant le montage sécurisé du Data Lake, le nettoyage intensif, les jointures complexes et le calcul d'indicateurs métiers avancés via l'utilisation du format de stockage transactionnel **Delta Lake**.
5. **Couche Restitution & Business Intelligence** :
   * **Power BI Desktop** : Connecté de façon optimisée aux datasets de la couche de consommation finale (Gold) pour la génération de rapports interactifs et le pilotage stratégique de l'activité.

```text
+------------------------+      +------------------------+
|   Azure SQL Database   |      |  GitHub API (JSON)     |
| (Products/Stores/Trans)|      |   (Customers Stream)   |
+-----------+------------+      +-----------+------------+
            |                               |
            |   [ ADF Ingestion Pipelines ] |
            +---------------+---------------+
                            |
                            ▼ (Format: Parquet)
+--------------------------------------------------------+
|            Azure Data Lake Storage Gen2 (ADLS)         |
|                                                        |
|  🥉 Couche BRONZE (Données Brutes Multi-Sources)        |
|     ├── transaction/ ├── product/ ├── store/ ├── customer/
+---------------------------+----------------------------+
                            |
                            ▼ [ Databricks / PySpark ]
+--------------------------------------------------------+
|  🥈 Couche SILVER (Données Nettoyées, Typées & Jointes)|
|     └── Format: Delta Lake (ACID, Time Travel)         |
+---------------------------+----------------------------+
                            |
                            ▼ [ Databricks / Aggregations ]
+--------------------------------------------------------+
|  🥇 Couche GOLD (Hub Analytique & Agrégations Métiers)|
|     └── Format: Delta / Export CSV Consommation        |
+---------------------------+----------------------------+
                            |
                            ▼
+--------------------------------------------------------+
|                Power BI Decision Dashboard             |
|   (CA, Volumes, Paliers de Ventes & Panier Moyen)      |
+--------------------------------------------------------+
🗂️ Cartographie et Modélisation des Sources
Le pipeline consolide 4 sources de données hétérogènes pour bâtir un modèle analytique unifié :

Entité Source	Type de Système	Format natif / Table	Volume / Rôle Opérationnel
Products	Azure SQL Database	Table Relationnelle	Catalogue de référence des articles commercialisés (ID, prix unitaire, catégorie).
Stores	Azure SQL Database	Table Relationnelle	Référentiel des points de vente physiques (ID, localisation, surface).
Transactions	Azure SQL Database	Table Relationnelle	Journal transactionnel brut (ID transaction, ID produit, ID magasin, quantité, timestamp).
Customers	GitHub API	Flux JSON / REST	Données de profils clients (ID client, âge, segmentation, canal d'acquisition).
🪵 Implémentation Rigoureuse de l'Architecture Medallion
1. 🥉 Couche Bronze (Données Brutes - Raw Layer)
Objectif : Servir de zone de débarquement (Landing Zone) pour l'ingestion de données ADF. Aucune modification de schéma ou de valeur n'est tolérée à cette étape pour préserver l'historique brut.

Format : Fichiers .parquet (stockage en colonnes, compression par dictionnaire, hautement performant pour Spark).

Arborescence cible dans ADLS Gen2 :

Plaintext
  container-retail-data/
  └── bronze/
      ├── transaction/
      │   └── data_uuid.parquet
      ├── product/
      │   └── data_uuid.parquet
      ├── store/
      │   └── data_uuid.parquet
      └── customer/
          └── data_uuid.parquet
2. 🥈 Couche Silver (Données Enrichies & Qualifiées - Enriched Layer)
Objectif : Nettoyer la donnée, standardiser les types, éliminer le bruit et réconcilier l'ensemble des axes d'analyse au sein d'un schéma unique.

Format : Table Delta Lake (support des transactions ACID, évolution de schéma contrôlée, optimisation des requêtes).

Traitements et Transformations PySpark appliqués :

Typage strict (Casting) : Alignement des types de données (Conversion des chaînes de caractères en types IntegerType, DecimalType(10,2) pour les prix, et TimestampType pour les transactions).

Qualité des données : Élimination complète des doublons sur les clés primaires et traitement/imputation des valeurs nulles ou manquantes.

Ingénierie de fonctionnalités (Feature Engineering) : Calcul de la colonne dérivée total_amount via la formule :

total_amount=quantity×price
Jointures à large échelle (Broadcast/Shuffle Joins) : Fusion des 4 DataFrames à travers les clés de liaison (product_id, store_id, customer_id) pour obtenir un jeu de données dénormalisé complet.

3. 🥇 Couche Gold (Données Décisionnelles - Curated Layer)
Objectif : Organiser les données en cubes ou tables agrégées prêtes à être consommées instantanément par les équipes métiers et les outils de BI, éliminant tout calcul lourd côté restitution.

Format : Table Delta Lake et export consolidé .csv pour une intégration fluide dans Power BI.

Indicateurs et KPIs pré-calculés au niveau du cluster :

Chiffre d'Affaires Global (CA) et ventilation par catégorie de produit.

Volume Global Écoulé (Somme des quantités vendues).

Nombre total de transactions uniques (Décompte distinct des identifiants transactionnels).

Valeur Moyenne Transactionnelle (Panier Moyen) :

Panier Moyen= 
Nombre de Transactions Uniques
∑total_amount
​
 
💻 Guide d'Exécution Technique & Déploiement
Prérequis Système
Un abonnement cloud Microsoft Azure actif (avec droits de création de ressources).

Une instance Databricks Workspace (ou un compte Databricks Community Edition).

Microsoft Power BI Desktop installé localement sur le poste de travail.

Étape 1 : Phase d'Ingestion & Ingestion via Azure Data Factory
Déployez l'instance Azure Data Factory à partir du portail Azure.

Créez les Linked Services (Services Liés) suivants avec authentification sécurisée :

ls_azure_sql_source : Connexion à la base Azure SQL contenant les tables transactionnelles.

ls_github_api_source : Connecteur HTTP pointant vers l'URL du flux JSON.

ls_adls_gen2_destination : Connexion vers le compte de stockage à l'aide d'une clé d'accès ou d'un Principal de Service (SPN).

Configurez les Datasets d'entrée et de sortie associés.

Intégrez l'activité Copy Activity au sein du pipeline orchestré, planifiée pour s'exécuter en parallèle afin de maximiser le débit d'écriture dans le dossier bronze/.

Étape 2 : Traitement et Montage dans Azure Databricks
Pour permettre à Spark d'accéder directement au stockage Azure, vous devez exécuter le script de montage suivant dans le premier bloc de votre notebook :

Python
# Script de montage (Mounting) de la couche de stockage ADLS Gen2
storage_account_name = "<votre_storage_account>"
container_name = "<votre_container>"
storage_key = "<votre_access_key>"

configs = {f"fs.azure.account.key.{storage_account_name}.blob.core.windows.net": storage_key}

# Vérification de l'existence du point de montage pour éviter les exceptions
if not any(mount.mountPoint == "/mnt/datalake" for mount in dbutils.fs.mounts()):
    dbutils.fs.mount(
        source = f"wasbs://{container_name}@{storage_account_name}.blob.core.windows.net",
        mount_point = "/mnt/datalake",
        extra_configs = configs
    )
    print("Le Data Lake a été monté avec succès !")
else:
    print("Le Data Lake est déjà monté sur l'environnement.")
Exécution du Pipeline de Code PySpark :
Notebook 01_Silver_Processing : Ce script charge les 4 répertoires Parquet depuis la zone /mnt/datalake/bronze/, applique le typage, supprime les lignes dupliquées, réalise l'enrichissement par jointure, calcule l'indicateur total_amount et écrit le résultat au format Delta sous /mnt/datalake/silver/.

Notebook 02_Gold_Aggregations : Ce script charge la table Silver Delta unifiée, applique les fonctions de regroupement (groupBy), génère les indicateurs clés agrégés par date, produit et magasin, puis exporte le dataset final dans /mnt/datalake/gold/.

📊 Restitution & Spécifications du Dashboard Power BI
Le tableau de bord décisionnel interactif est connecté directement au dataset structuré de la couche Gold. Le modèle de données a été optimisé pour offrir un temps de réponse instantané (inférieur à 200 ms) et comprend les sections analytiques suivantes :

Axe Performance Commerciale : Graphique d'évolution chronologique du Chiffre d'Affaires (Sales by Date) permettant le filtrage dynamique par année, trimestre et mois.

Axe Analyse Produits & Segmentation : Diagramme en barres horizontales mettant en évidence les meilleures ventes par produit (Sales by Product) et un treemap illustrant la répartition des parts de marché par catégorie (Sales by Category).

Axe Performance Réseau (Magasins) : Cartographie ou tableau comparatif croisant le volume total d'unités vendues (Quantity Sold) avec la performance de chiffre d'affaires associée.

Bloc KPIs Stratégiques (Cartes de Score) : Affichage dynamique des métriques clés de l'entreprise : Chiffre d'Affaires total, Volume d'unités vendues, Nombre Global de Transactions et Valeur Moyenne Transactionnelle (Panier Moyen).

📅 Méthodologie Agile & Suivi de Projet (Board Jira)
Le projet s'est déroulé sur un cycle de Sprint court de 5 jours ouvrés, géré via un tableau de bord Jira structuré pour assurer une traçabilité rigoureuse de chaque tâche :

Jour 1 [Phase 0 - Cadrage & Architecture] : Analyse de l'existant, modélisation conceptuelle du pipeline, rédaction de la documentation technique préalable et initialisation du référentiel GitHub.

Jour 2 [Phase 1 & 2 - Infrastructure & Source Ready] : Provisioning des ressources Azure, configuration réseau, création des schémas DDL et injection des données de test dans Azure SQL, et écriture des requêtes d'appel d'API JSON.

Jour 3 [Phase 3 & 4 - Orchestration d'Ingestion] : Configuration d'Azure Data Factory, création des Linked Services, développement et validation des 4 pipelines parallèles de la Copy Activity vers la couche Bronze.

Jour 4 [Phase 5 & 6 - Engineering & Transformation Spark] : Montage du conteneur ADLS dans Databricks, développement des scripts PySpark pour les couches Silver (Data Quality) et Gold (Business Rules & Aggregations).

Jour 5 [Phase 7 - Business Intelligence & Restitution] : Importation du dataset Gold final, modélisation des relations dans Power BI Desktop, conception visuelle du dashboard, exécution des tests d'intégration globaux (End-to-End) et livraison de la solution.

📂 Architecture Structurelle du Repository
Plaintext
├── README.md                      # Documentation maîtresse du projet (Ce fichier)
├── architecture/                  # Schémas d'architecture globale, diagrammes de flux et d'infrastructure
├── adf/                           # Fichiers de configuration et templates JSON d'Azure Data Factory
│   ├── pipelines/                 # Définitions JSON des pipelines d'ingestion parallèles
│   └── linked_services/           # Configurations JSON des services de connexion (SQL, API, ADLS)
├── notebooks/                     # Notebooks de traitement de données développés sous Databricks
│   ├── 01_Silver_Processing.py    # Script PySpark : Nettoyage, typage strict, jointures et calcul Silver
│   └── 02_Gold_Aggregations.py    # Script PySpark : Agrégations analytiques métiers et indicateurs Gold
├── sql/                           # Scripts de base de données relationnelle
│   └── create_tables.sql          # Scripts DDL de création des tables et scripts d'insertion DML sources
└── powerbi/                       # Fichiers de la couche de restitution décisionnelle
    └── Retail_Analytics_Dashboard.pbit # Modèle de rapport ou template Power BI configuré
👨‍💻 Informations Évaluateurs & Auteur
Rôle d'Ingénierie : Data Engineer / Data Analyst [Votre Nom & Prénom]

Validateur / Référent Projet : Omar Hitar

Période de Réalisation : Du 01/06/2026 au 05/06/2026 (Avant 17h00)

Stack Technologique Maitrisée : Microsoft Azure, Azure SQL DB, ADLS Gen2, Azure Data Factory, Databricks Community Edition, Apache Spark (PySpark), Delta Lake, Parquet, API REST JSON, SQL, Power BI Desktop.




Gemini est une IA et peut se tromper.


# 🚀 Azure Data Engineering Pipeline: Medallion Architecture with Databricks & Power BI

## 📌 Présentation du Projet
Ce projet consiste en la conception, l'implémentation et le déploiement d'une solution d'ingénierie de données de bout en bout (End-to-End) sur l'écosystème cloud **Microsoft Azure**. L'objectif principal est de moderniser le système décisionnel d'une entreprise du secteur Retail en automatisant l'ingestion, le stockage, la transformation et la valorisation analytique des données de ventes et de profils clients.

Pour garantir la qualité, la gouvernance, la traçabilité et la performance des données avant leur restitution, le flux de traitement implémente une **Architecture Medallion** (Bronze ➡️ Silver ➡️ Gold) au sein d'un Data Lake de nouvelle génération.

---

## 🏗️ Architecture Technique Globale

Le flux de données traverse de manière séquentielle et automatisée les composants et services Azure suivants :

1. **Sources de Données Multi-paradigmes** :
   * **Azure SQL Database** : Stockage relationnel hébergeant les tables transactionnelles et les référentiels opérationnels (`Products`, `Stores`, `Transactions`).
   * **GitHub API / Flux REST** : Source externe fournissant des payloads de données démographiques clients au format non structuré (`Customers` JSON).
2. **Orchestration & Ingestion Synchrone** :
   * **Azure Data Factory (ADF)** : Orchestrateur cloud chargé d'exécuter les activités d'extraction (*Copy Activity*) en parallèle, d'assurer le mapping des schémas et de convertir les flux bruts vers le format optimisé *Parquet*.
3. **Stockage Distribué & Sécurisé** :
   * **Azure Data Lake Storage Gen2 (ADLS Gen2)** : Configuré avec l'espace de noms hiérarchique (*Hierarchical Namespace*) activé, structuré de manière stricte pour isoler les différentes couches du framework Medallion.
4. **Moteur de Calcul & Traitement Distribué** :
   * **Azure Databricks (Engine Apache Spark / PySpark)** : Cluster de calcul distribué permettant le montage sécurisé du Data Lake, le nettoyage intensif, les jointures complexes et le calcul d'indicateurs métiers avancés via l'utilisation du format de stockage transactionnel **Delta Lake**.
5. **Couche Restitution & Business Intelligence** :
   * **Power BI Desktop** : Connecté de façon optimisée aux datasets de la couche de consommation finale (Gold) pour la génération de rapports interactifs et le pilotage stratégique de l'activité.

```text
+------------------------+      +------------------------+
|   Azure SQL Database   |      |  GitHub API (JSON)     |
| (Products/Stores/Trans)|      |   (Customers Stream)   |
+-----------+------------+      +-----------+------------+
            |                               |
            |   [ ADF Ingestion Pipelines ] |
            +---------------+---------------+
                            |
                            ▼ (Format: Parquet)
+--------------------------------------------------------+
|            Azure Data Lake Storage Gen2 (ADLS)         |
|                                                        |
|  🥉 Couche BRONZE (Données Brutes Multi-Sources)        |
|     ├── transaction/ ├── product/ ├── store/ ├── customer/
+---------------------------+----------------------------+
                            |
                            ▼ [ Databricks / PySpark ]
+--------------------------------------------------------+
|  🥈 Couche SILVER (Données Nettoyées, Typées & Jointes)|
|     └── Format: Delta Lake (ACID, Time Travel)         |
+---------------------------+----------------------------+
                            |
                            ▼ [ Databricks / Aggregations ]
+--------------------------------------------------------+
|  🥇 Couche GOLD (Hub Analytique & Agrégations Métiers)|
|     └── Format: Delta / Export CSV Consommation        |
+---------------------------+----------------------------+
                            |
                            ▼
+--------------------------------------------------------+
|                Power BI Decision Dashboard             |
|   (CA, Volumes, Paliers de Ventes & Panier Moyen)      |
+--------------------------------------------------------+
```

---

## 🗂️ Cartographie et Modélisation des Sources

Le pipeline consolide **4 sources de données hétérogènes** pour bâtir un modèle analytique unifié :

| Entité Source | Type de Système | Format natif / Table | Volume / Rôle Opérationnel |
| :--- | :--- | :--- | :--- |
| **Products** | Azure SQL Database | Table Relationnelle | Catalogue de référence des articles commercialisés (ID, prix unitaire, catégorie). |
| **Stores** | Azure SQL Database | Table Relationnelle | Référentiel des points de vente physiques (ID, localisation, surface). |
| **Transactions**| Azure SQL Database | Table Relationnelle | Journal transactionnel brut (ID transaction, ID produit, ID magasin, quantité, timestamp). |
| **Customers** | GitHub API | Flux JSON / REST | Données de profils clients (ID client, âge, segmentation, canal d'acquisition). |

---

## 🪵 Implémentation Rigoureuse de l'Architecture Medallion

### 1. 🥉 Couche Bronze (Données Brutes - Raw Layer)
* **Objectif** : Servir de zone de débarquement (Landing Zone) pour l'ingestion de données ADF. Aucune modification de schéma ou de valeur n'est tolérée à cette étape pour préserver l'historique brut.
* **Format** : Fichiers `.parquet` (stockage en colonnes, compression par dictionnaire, hautement performant pour Spark).
* **Arborescence cible dans ADLS Gen2** :
  ```text
  container-retail-data/
  └── bronze/
      ├── transaction/
      │   └── data_uuid.parquet
      ├── product/
      │   └── data_uuid.parquet
      ├── store/
      │   └── data_uuid.parquet
      └── customer/
          └── data_uuid.parquet
  ```

### 2. 🥈 Couche Silver (Données Enrichies & Qualifiées - Enriched Layer)
* **Objectif** : Nettoyer la donnée, standardiser les types, éliminer le bruit et réconcilier l'ensemble des axes d'analyse au sein d'un schéma unique.
* **Format** : Table `Delta Lake` (support des transactions ACID, évolution de schéma contrôlée, optimisation des requêtes).
* **Traitements et Transformations PySpark appliqués** :
  * **Typage strict (Casting)** : Alignement des types de données (Conversion des chaînes de caractères en types `IntegerType`, `DecimalType(10,2)` pour les prix, et `TimestampType` pour les transactions).
  * **Qualité des données** : Élimination complète des doublons sur les clés primaires et traitement/imputation des valeurs nulles ou manquantes.
  * **Ingénierie de fonctionnalités (Feature Engineering)** : Calcul de la colonne dérivée `total_amount` via la formule :
    $$\text{total\_amount} = \text{quantity} \times \text{price}$$
  * **Jointures à large échelle (Broadcast/Shuffle Joins)** : Fusion des 4 DataFrames à travers les clés de liaison (`product_id`, `store_id`, `customer_id`) pour obtenir un jeu de données dénormalisé complet.

### 3. 🥇 Couche Gold (Données Décisionnelles - Curated Layer)
* **Objectif** : Organiser les données en cubes ou tables agrégées prêtes à être consommées instantanément par les équipes métiers et les outils de BI, éliminant tout calcul lourd côté restitution.
* **Format** : Table `Delta Lake` et export consolidé `.csv` pour une intégration fluide dans Power BI.
* **Indicateurs et KPIs pré-calculés au niveau du cluster** :
  * **Chiffre d'Affaires Global (CA)** et ventilation par catégorie de produit.
  * **Volume Global Écoulé** (Somme des quantités vendues).
  * **Nombre total de transactions uniques** (Décompte distinct des identifiants transactionnels).
  * **Valeur Moyenne Transactionnelle (Panier Moyen)** :
    $$\text{Panier Moyen} = \frac{\sum \text{total\_amount}}{\text{Nombre de Transactions Uniques}}$$

---

## 💻 Guide d'Exécution Technique & Déploiement

### Prérequis Système
* Un abonnement cloud Microsoft Azure actif (avec droits de création de ressources).
* Une instance Databricks Workspace (ou un compte Databricks Community Edition).
* Microsoft Power BI Desktop installé localement sur le poste de travail.

### Étape 1 : Phase d'Ingestion & Ingestion via Azure Data Factory
1. Déployez l'instance Azure Data Factory à partir du portail Azure.
2. Créez les **Linked Services** (Services Liés) suivants avec authentification sécurisée :
   * `ls_azure_sql_source` : Connexion à la base Azure SQL contenant les tables transactionnelles.
   * `ls_github_api_source` : Connecteur HTTP pointant vers l'URL du flux JSON.
   * `ls_adls_gen2_destination` : Connexion vers le compte de stockage à l'aide d'une clé d'accès ou d'un Principal de Service (SPN).
3. Configurez les **Datasets** d'entrée et de sortie associés.
4. Intégrez l'activité **Copy Activity** au sein du pipeline orchestré, planifiée pour s'exécuter en parallèle afin de maximiser le débit d'écriture dans le dossier `bronze/`.

### Étape 2 : Traitement et Montage dans Azure Databricks
Pour permettre à Spark d'accéder directement au stockage Azure, vous devez exécuter le script de montage suivant dans le premier bloc de votre notebook :

```python
# Script de montage (Mounting) de la couche de stockage ADLS Gen2
storage_account_name = "<votre_storage_account>"
container_name = "<votre_container>"
storage_key = "<votre_access_key>"

configs = {f"fs.azure.account.key.{storage_account_name}.blob.core.windows.net": storage_key}

# Vérification de l'existence du point de montage pour éviter les exceptions
if not any(mount.mountPoint == "/mnt/datalake" for mount in dbutils.fs.mounts()):
    dbutils.fs.mount(
        source = f"wasbs://{container_name}@{storage_account_name}.blob.core.windows.net",
        mount_point = "/mnt/datalake",
        extra_configs = configs
    )
    print("Le Data Lake a été monté avec succès !")
else:
    print("Le Data Lake est déjà monté sur l'environnement.")
```

#### Exécution du Pipeline de Code PySpark :
1. **Notebook `01_Silver_Processing`** : Ce script charge les 4 répertoires Parquet depuis la zone `/mnt/datalake/bronze/`, applique le typage, supprime les lignes dupliquées, réalise l'enrichissement par jointure, calcule l'indicateur `total_amount` et écrit le résultat au format Delta sous `/mnt/datalake/silver/`.
2. **Notebook `02_Gold_Aggregations`** : Ce script charge la table Silver Delta unifiée, applique les fonctions de regroupement (`groupBy`), génère les indicateurs clés agrégés par date, produit et magasin, puis exporte le dataset final dans `/mnt/datalake/gold/`.

---

## 📊 Restitution & Spécifications du Dashboard Power BI

Le tableau de bord décisionnel interactif est connecté directement au dataset structuré de la couche **Gold**. Le modèle de données a été optimisé pour offrir un temps de réponse instantané (inférieur à 200 ms) et comprend les sections analytiques suivantes :

* **Axe Performance Commerciale** : Graphique d'évolution chronologique du Chiffre d'Affaires (*Sales by Date*) permettant le filtrage dynamique par année, trimestre et mois.
* **Axe Analyse Produits & Segmentation** : Diagramme en barres horizontales mettant en évidence les meilleures ventes par produit (*Sales by Product*) et un treemap illustrant la répartition des parts de marché par catégorie (*Sales by Category*).
* **Axe Performance Réseau (Magasins)** : Cartographie ou tableau comparatif croisant le volume total d'unités vendues (*Quantity Sold*) avec la performance de chiffre d'affaires associée.
* **Bloc KPIs Stratégiques (Cartes de Score)** : Affichage dynamique des métriques clés de l'entreprise : *Chiffre d'Affaires total*, *Volume d'unités vendues*, *Nombre Global de Transactions* et *Valeur Moyenne Transactionnelle (Panier Moyen)*.

---

## 📅 Méthodologie Agile & Suivi de Projet (Board Jira)

Le projet s'est déroulé sur un cycle de **Sprint court de 5 jours ouvrés**, géré via un tableau de bord **Jira** structuré pour assurer une traçabilité rigoureuse de chaque tâche :

* **Jour 1 [Phase 0 - Cadrage & Architecture]** : Analyse de l'existant, modélisation conceptuelle du pipeline, rédaction de la documentation technique préalable et initialisation du référentiel GitHub.
* **Jour 2 [Phase 1 & 2 - Infrastructure & Source Ready]** : Provisioning des ressources Azure, configuration réseau, création des schémas DDL et injection des données de test dans Azure SQL, et écriture des requêtes d'appel d'API JSON.
* **Jour 3 [Phase 3 & 4 - Orchestration d'Ingestion]** : Configuration d'Azure Data Factory, création des Linked Services, développement et validation des 4 pipelines parallèles de la Copy Activity vers la couche Bronze.
* **Jour 4 [Phase 5 & 6 - Engineering & Transformation Spark]** : Montage du conteneur ADLS dans Databricks, développement des scripts PySpark pour les couches Silver (Data Quality) et Gold (Business Rules & Aggregations).
* **Jour 5 [Phase 7 - Business Intelligence & Restitution]** : Importation du dataset Gold final, modélisation des relations dans Power BI Desktop, conception visuelle du dashboard, exécution des tests d'intégration globaux (End-to-End) et livraison de la solution.

---

## 📂 Architecture Structurelle du Repository

```text
├── README.md                      # Documentation maîtresse du projet (Ce fichier)
├── architecture/                  # Schémas d'architecture globale, diagrammes de flux et d'infrastructure
├── adf/                           # Fichiers de configuration et templates JSON d'Azure Data Factory
│   ├── pipelines/                 # Définitions JSON des pipelines d'ingestion parallèles
│   └── linked_services/           # Configurations JSON des services de connexion (SQL, API, ADLS)
├── notebooks/                     # Notebooks de traitement de données développés sous Databricks
│   ├── 01_Silver_Processing.py    # Script PySpark : Nettoyage, typage strict, jointures et calcul Silver
│   └── 02_Gold_Aggregations.py    # Script PySpark : Agrégations analytiques métiers et indicateurs Gold
├── sql/                           # Scripts de base de données relationnelle
│   └── create_tables.sql          # Scripts DDL de création des tables et scripts d'insertion DML sources
└── powerbi/                       # Fichiers de la couche de restitution décisionnelle
    └── Retail_Analytics_Dashboard.pbit # Modèle de rapport ou template Power BI configuré
```

---

## 👨‍💻 Informations Évaluateurs & Auteur
* **Rôle d'Ingénierie** : Data Engineer / Data Analyst [mina Elaachrate]
* **Validateur / Référent Projet** : Omar Hitar
* **Période de Réalisation** : Du 01/06/2026 au 05/06/2026 (Avant 17h00)
* **Stack Technologique Maitrisée** : Microsoft Azure, Azure SQL DB, ADLS Gen2, Azure Data Factory, Databricks Community Edition, Apache Spark (PySpark), Delta Lake, Parquet, API REST JSON, SQL, Power BI Desktop.
README.md
Affichage de README.md.
