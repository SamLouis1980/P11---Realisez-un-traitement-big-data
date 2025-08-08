#  Traitement d’images dans un environnement Big Data – Fruits!

## Contexte

La start-up **Fruits!** développe des solutions innovantes pour la récolte de fruits, avec un fort accent sur la préservation de la biodiversité.  
Dans le cadre du développement d’une application mobile permettant d’identifier un fruit à partir d’une photo, une première **architecture Big Data** a été mise en place pour préparer le traitement à grande échelle des images.

Ce projet consiste à compléter et industrialiser la **chaîne de traitement PySpark** sur un environnement Cloud (AWS EMR ou Databricks), en y intégrant notamment :
- La diffusion des poids du modèle TensorFlow sur les clusters
- Une étape de réduction de dimension par PCA

## Objectif

- Adapter et compléter le script PySpark fourni par un alternant
- Mettre en place la **diffusion des poids** d’un modèle TensorFlow (`MobileNetV2`) sur un cluster Spark
- Implémenter une **réduction de dimension PCA** en PySpark pour compresser les features extraites
- Démontrer le fonctionnement sur un cluster Big Data Cloud (AWS EMR ou Databricks)
- Exporter les résultats dans un format exploitable (CSV) sur un espace de stockage Cloud
- Respecter les contraintes RGPD (serveurs localisés en Europe)

## Technologies utilisées

- `PySpark` (`SparkSession`, `pandas_udf`, `PCA` de `pyspark.ml.feature`)
- `TensorFlow`, `Keras` (`MobileNetV2`, `preprocess_input`)
- `Pandas`, `NumPy`, `Pillow`
- `AWS EMR`, `S3` ou `Databricks` (selon configuration)
- `Python` standard (`os`, `time`, `io`)

## Structure du projet

- notebook.ipynb - Script PySpark complet avec preprocessing et PCA
- matrice_reduction_dimension.csv - Sortie de la réduction de dimension (stockée sur le Cloud)
- presentation.pptx - Présentation de l’architecture et de la démarche
