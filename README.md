# Travaux Pratiques de Machine Learning 2 - Clustering

## Introduction

Ce projet porte sur une analyse non supervisée de données à l’aide d’algorithmes de **clustering**, avec un accent particulier sur **K-Means**. L’objectif principal est d’identifier des groupes naturels (clusters) au sein des données, d’optimiser les paramètres du modèle, de visualiser les résultats et d'interpréter les profils caractéristiques (personnas) issus des groupes détectés.

## Objectifs

1. **Optimisation de K-Means** : Tester plusieurs combinaisons d’hyperparamètres, notamment :
   - le nombre de clusters (`k`),
   - l’algorithme d’initialisation (`init`),
   - le nombre d’itérations.
2. **Évaluation de l’effet de la réduction de dimension** :
   - Comparaison des performances avec ou sans **PCA** (analyse en composantes principales).
3. **Standardisation des données** :
   - Étude de l’effet de différents scalers : `StandardScaler`, `MinMaxScaler`, `RobustScaler`, ou sans standardisation.
4. **Sélection du meilleur modèle** :
   - Basée sur des métriques comme le **Silhouette Score**, l’**inertie**, ou d’autres critères de cohérence des clusters.
5. **Visualisation des clusters** :
   - Utilisation de **t-SNE** pour réduire les données à 2 dimensions et afficher la répartition des clusters.
6. **Analyse des profils moyens (personnas)** :
   - Calcul de l’image moyenne ou du profil moyen associé à chaque cluster.

## Méthodologie

### 1. Préparation des données

Les données ont été prétraitées via différentes méthodes de **standardisation** selon les paramètres testés. Ensuite, la réduction de dimension avec **PCA** a été appliquée (ou non), en fonction de la configuration.

### 2. Modélisation avec K-Means

Une grille de recherche manuelle a été effectuée en faisant varier :
- `k` : nombre de clusters (de 2 à 15),
- `init` : `k-means++` ou `random`,
- application ou non de PCA.

Chaque combinaison a été évaluée sur ses performances de clustering.

### 3. Visualisation avec t-SNE

Une visualisation en 2D a été générée à partir de t-SNE, permettant d’observer la distribution des clusters obtenus pour le meilleur modèle.

### 4. Analyse des Personnas

Pour chaque cluster, un **profil moyen** a été calculé :
- Moyenne des observations appartenant au cluster.
- Visualisation de l’image moyenne associée (si données imagées).
- Interprétation des caractéristiques dominantes du groupe.

## Résultats

- Le meilleur modèle a été sélectionné en fonction du **meilleur compromis** entre cohérence interne (silhouette), dispersion (inertie) et lisibilité des clusters.
- L’application de **PCA (80%)** et de **StandardScaler** a souvent permis d'améliorer la séparation des clusters.
- Les clusters trouvés présentaient des profils distincts, visualisables avec t-SNE.
- Les **images moyennes par cluster** ont été extraites et interprétées comme des personnas typiques.

## Visualisation

- **t-SNE** : Réduction à 2D pour visualiser les clusters.
- **Images moyennes par cluster** : Représentations visuelles synthétiques.
- **Métriques** : Courbes du silhouette score, courbe d’inertie (`elbow`).

## Conclusion

Ce projet montre l’importance :
- De tester différentes configurations pour le clustering non supervisé.
- D’appliquer des méthodes de prétraitement adaptées (scaling, réduction de dimension).
- De visualiser et interpréter les résultats pour une compréhension concrète des groupes détectés.

## Fichiers

- `Clustering.ipynb` : Notebook principal contenant les tests de K-Means, les visualisations t-SNE, les calculs de silhouette, et l’analyse des clusters.

---

*YATABARE Cheikna Amala*  
*Travaux Pratiques de Machine Learning 2*
