P8: Déployez un modèle dans le cloud

Ce projet, réalisé dans le cadre du parcours Data Scientist d'OpenClassrooms, met en place une architecture Big Data pour l'application mobile de la start-up Fruits! (AgriTech). L'objectif est de traiter des images de fruits pour une classification future, en posant les bases d'un pipeline scalable sur AWS avec PySpark.


Structure du projet :

Fichiers principaux :

- Diallo_Alpha_1_122024.ipynb : Notebook PySpark exécuté sur AWS EMR, incluant :
      - Prétraitement des images (chargement, normalisation, extraction de features).
      - Réduction dimensionnelle via PCA.
      - Diffusion des poids d'un modèle TensorFlow Keras sur les clusters (broadcast des "weights").
      - Sauvegarde de la matrice réduite en CSV sur AWS S3.

- Diallo_Alpha_3_presentation_122024.pdf : Présentation (PDF, max. 30 slides) décrivant :
      - Les briques d'architecture (AWS EMR, S3, IAM).
      - Leur rôle dans l'architecture Big Data.
      - La mise en œuvre de l'environnement EMR.
      - Les étapes du pipeline PySpark.

Données :

Le jeu de données comprend des images de fruits et leurs labels, accessibles via un lien de téléchargement. Les résultats de la réduction dimensionnelle sont stockés en CSV sur AWS S3.

Objectifs du projet :

Mettre en place un pipeline Big Data pour traiter des images de fruits, en anticipation d'une augmentation du volume de données.

Étapes :

  - Prétraitement des images pour l'extraction de features.
  - Réduction dimensionnelle avec PCA pour optimiser le stockage et les calculs.
  - Diffusion des poids d'un modèle TensorFlow pour une inférence distribuée.
  - Stockage des résultats sur AWS S3.

Contraintes :

- Conformité RGPD : Serveurs en Europe (région eu-west-1).
- Optimisation des coûts : Instance EMR active uniquement pour tests/démos (< 10€).

Résultats principaux :

- Instance EMR opérationnelle avec PySpark pour un traitement distribué.
- Pipeline complet : prétraitement, PCA, broadcast des poids, et stockage des résultats sur S3.
- Conformité RGPD respectée avec une infrastructure européenne.
