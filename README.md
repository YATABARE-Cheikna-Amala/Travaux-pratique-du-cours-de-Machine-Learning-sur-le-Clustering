# Travaux Pratiques de Machine Learning 2 - Classification

## Introduction
Ce projet présente une analyse complète de la classification à l'aide de plusieurs modèles d'apprentissage automatique, notamment **Random Forest**, **XGBoost**, **Dummy Classifier**, et **K-Nearest Neighbors (KNN)**. L'objectif est de comparer les performances des différents modèles et de sélectionner le meilleur pour résoudre le problème de classification.

## Objectifs
1. **Préparation des données** : Traitement des données pour l'entraînement des modèles, y compris la gestion des variables catégorielles et continues.
2. **Modélisation** : Mise en œuvre des modèles **Random Forest** et **XGBoost**, ainsi que des comparaisons avec les modèles de référence **Dummy Classifier** et **KNN**.
3. **Sélection du meilleur modèle** : Evaluation de la performance de chaque modèle sur un ensemble de données de test afin de déterminer le meilleur modèle de classification.
4. **Interprétation des résultats** : Identification des meilleures caractéristiques (features) qui influencent le modèle de manière significative.
5. **Enregistrement du meilleur modèle** : Sauvegarde du modèle **XGBoost** (le meilleur modèle) en format `.dill` pour une utilisation ultérieure.

## Méthodologie

### Préparation des données
Les données ont été soigneusement nettoyées et préparées pour l'entraînement des modèles. Cela inclut la gestion des valeurs manquantes, le codage des variables catégorielles, et la normalisation des caractéristiques lorsque nécessaire.

### Modélisation
1. **Dummy Classifier** : Utilisé comme base de référence pour évaluer la performance des autres modèles.
2. **K-Nearest Neighbors (KNN)** : Un modèle de classification simple basé sur la proximité des données.
3. **Random Forest** : Un modèle d'ensemble qui utilise plusieurs arbres de décision pour améliorer la performance et la robustesse.
4. **XGBoost** : Un algorithme d'apprentissage en gradient boosting qui a montré des résultats supérieurs dans les tests.

### Choix du meilleur modèle
Après avoir testé tous les modèles, **XGBoost** a été sélectionné comme le meilleur modèle en raison de sa performance supérieure en termes de **accuracy**, **precision**, **recall**, et **F1-score**. 

### Sélection des meilleures caractéristiques
Les caractéristiques les plus influentes pour la prédiction ont été extraites et analysées. Ces caractéristiques ont été utilisées pour affiner le modèle et améliorer ses performances.

### Sauvegarde du modèle
Le modèle **XGBoost** a été sauvegardé en format `.dill` pour un usage futur, facilitant ainsi sa réutilisation sans nécessiter de nouvel entraînement.

## Résultats
Les performances des différents modèles ont été comparées, et voici les résultats principaux :
- Le modèle **XGBoost** a obtenu les meilleures performances, surpassant le **Random Forest** et les autres modèles.
- Le modèle **KNN** et le **Dummy Classifier** ont montré des résultats plus faibles, ce qui a renforcé l'importance de l'utilisation des modèles plus complexes comme **XGBoost**.

## Enregistrement du Modèle
Le meilleur modèle, **XGBoost**, a été enregistré dans le fichier `models/xgboost_model.dill`. Ce fichier contient le modèle entraîné, prêt à être utilisé pour de futures prédictions.

## Conclusion
Ce projet montre l'importance de tester différents modèles d'apprentissage automatique et de sélectionner celui qui offre les meilleures performances en fonction des critères de classification. Le modèle **XGBoost** a été choisi comme étant le plus performant pour ce problème spécifique, et il est désormais enregistré pour un usage ultérieur.

---

### Fichiers
- `tp-classification-revenue.ipynb` : Notebook contenant le code pour la mise en œuvre des modèles et l'analyse des résultats.
- `models/xgboost_model1.dill` : Le modèle XGBoost enregistré pour les prédictions futures.
- `README.md` : Ce fichier contenant une description du TP.

---


---

*YATABARE Cheikna Amala*  
*Travaux Pratiques de Machine Learning 2*
