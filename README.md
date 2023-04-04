# data-learning

Ce repository est basé sur le
repository [data-science-project-2](https://github.com/Selimmmm/data-science-project-2/blob/master/consignes.ipynb)
de [Selimmmm](https://github.com/Selimmmm)

## Requirements

Pour pouvoir utiliser ce repository, le fichier requirements.txt contient toutes les dépendances nécessaires au bon
fonctionnement.
Utilisé la commande suivante pour installer les dépendances :

```bash
pip install -r requirements.txt
```

## Objectif

L'objectif de ce projet est de mettre en place un modèle de prédiction du prix des appartements en fonction de leurs
nombres de pièces, de leur surface.

### Partie 1 - Nettoyage des données

- [x] Nettoyer les données pour la colonnes `availability`
- [x] Nettoyer les données pour la colonnes `size`
- [x] Nettoyer les données pour la colonnes `total_sqft`
- [x] Vérification des données à l'aide de la méthode `info()`
- [x] Sauvegarde des données nettoyées dans une table sql nommée `data_cleaned`
- [x] Amélioration du nettoyage des données pour la colonne `total_sqft`

### Partie 2 - Statistiques descriptives

*Réutiliser les données de data_cleaned ou de data_cleaned_2*

- [x] Représenter un scatter plot, chaque variable en abscisse et le prix en ordonnée.
- [x] Représenter un graphique qui permet de déterminer le prix moyen en fonction du nombre de balcons.
- [x] Représenter un graphique qui permet de déterminer le prix moyen en fonction du nombre de salles de bains.
- [x] Créer une data frame qui contient les colonnes suivantes :
    - `availability` : les dates de disponibilité possibles (valeurs uniques)
    - `count` : le nombre de biens qui deviennent disponibles à cette date
    - `count_cum`: le nombre de biens cumulés disponibles à cette date
    - `price_mean`: le prix moyen des biens qui deviennent disponibles à cette date
- [x] Représenter la matrice des corrélations des variables quantitatives.

### Partie 3 - Prédiction

*Réutiliser les données de data_cleaned ou de data_cleaned_2*

- [x] Séparer les données en un jeu d'entraînement et un jeu de test (70 / 30)
- [x] Prédiction avec une variable numérique
    - [x] Calculer les prédictions avec une régression linéaire simple et les sauvegarder dans une table sql
      nommée `model_1_predictions`
    - [x] Calculer la même prédiction que précédemment, mais remplacer la variable `total_sqft` (X_train) par le nombre
      de jours avant la disponibilité (`days_before`).
- [x] Calculer les prédictions avec une régression linéaire multiple et les sauvegarder dans une table sql
  nommée `model_2_predictions`
- [x] Reproduire la table `model_2_predictions` en incluant une variable catégorielle (en
  utilisant `pandas.get_dummies`). la sauvegarder dans une table sql nommée `model_3_predictions`