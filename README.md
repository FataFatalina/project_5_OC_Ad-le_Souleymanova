# project_5_OC_Adele_Souleymanova
## Projet 5 : Ségmentation des clients d'une base de données d'une plateforme E-commerce Olist

But du projet: segmentation des clients afin de comprendre les différents types d’utilisateurs
fournir à l’équipe marketing une description actionable et proposer contrat de maintenance du Modèle

Approche: utilisation de méthodes non supervisées pour regrouper ensemble des clients de profils similaires
évaluer la fréquence à laquelle la segmentation doit être mise à jour afin de proposer un devis de contrat de maintenance.

Notebook 1 du projet 5:
Dans ce notebook nous allons:

I) Analyser les datasets

    1) Importer les données
    2) Visualiser les premieres lignes des datasets
     
II) Joindre les differents datasets

    1) Renommer les colonnes concernant les zip codes dans les differents datasets
    2) Supprimer les duplicats
    3) Jointure des datasets "client"
    4) Jointure finale avec datasets "produits"
    
III) Feature engineering

    1) Manipulation des features temporels
    2) Création de catégories plus simples 
    3) Aggregation par clients et création de nouvelles colonnes
    4) Jointure des features crées en une seule dataframe ' data'
    
    
IV) Analyse exploratoire

    1) Visualisation des Etats qui achètent le plus
    2) Les produits les plus vendus
    3) L'évolution de la vente en fonction des mois de l'année
    4) Représentation géographique de la consommation par les clients

    
V) Data preprocessing 

    1) Visualisation de la corrélation linéaire entre les différents features
    2) Vérification de valeurs manquates et imputation par les valeurs modales
    3) Suppresion de features redondantes et Encodage des variables categorielle
    4) Sélection des features les plus intéressants selon la variance
    5) Positiver les valeurs
    6) Train/Test split
    

    
