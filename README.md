# Regression lineaire sur les prix des maisons

Ce projet utilise le jeu de donnees **House Prices** pour apprendre les bases du Machine Learning avec une regression lineaire.

## Objectif

Predire `SalePrice` a partir des caracteristiques des maisons.

Le notebook utilise toutes les variables disponibles sauf :

- `SalePrice`, qui est la valeur a predire ;
- `Id`, qui sert seulement a identifier la maison.

## Preparation des donnees

Le notebook :

1. charge `train.csv` et `test.csv` ;
2. separe les variables numeriques et categorielles ;
3. remplace les valeurs numeriques manquantes par la mediane ;
4. standardise les variables numeriques ;
5. remplace les valeurs texte manquantes ;
6. transforme les categories en colonnes numeriques avec le one-hot encoding ;
7. entraine une `LinearRegression` ;
8. compare l'apprentissage sur les prix reels et sur `log1p(SalePrice)` ;
9. cree `submission.csv`.

## Installation

L'environnement conserve dans le projet est `.venv`.

Dans PowerShell :

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

## Execution

Ouvrir `house_prices_regression.ipynb` dans VS Code, selectionner l'environnement `.venv`, puis executer les cellules dans l'ordre.

## Fichiers principaux

- `house_prices_regression.ipynb` : analyse, preparation, entrainement et prediction ;
- `train.csv` : donnees d'entrainement avec `SalePrice` ;
- `test.csv` : donnees a predire ;
- `submission.csv` : predictions generees ;
- `requirements.txt` : dependances Python ;
- `data_description.txt` : description des colonnes.