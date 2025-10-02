# Cahier de suivi de projet - KELODJOU DJOMO NAFISSATOU IVANA
**Matricule:** 22T2894 
**Cours:** INF4127 - OPTIMISATION II
**Année académique:** 2025-2026

---

## TPE 1 - [Date: 02/10/2025]

### Objectifs
- Découverte du calcul symbolique
- Prise en main de la bibliothèque SymPy
- Compréhension des différences entre calcul symbolique et numérique

### Travail réalisé

#### 1. Étude théorique
- **Définition du calcul symbolique:** Manipulation d'expressions mathématiques exactes avec des symboles et variables plutôt que des approximations numériques
- **Avantages identifiés:**
  - Résultats exacts sans erreurs d'arrondi
  - Meilleure compréhension de la structure mathématique
  - Dérivation automatique sans erreurs de calcul manuel

#### 2. Apprentissage de SymPy
**Concepts maîtrisés:**
- Création de symboles avec `sp.symbols()`
- Manipulation d'expressions algébriques (factorisation, expansion)
- Calcul différentiel (dérivées, gradients)
- Calcul intégral (intégrales définies et indéfinies)
- Résolution d'équations et systèmes d'équations

#### 3. Applications pratiques développées

**Exemple 1: Optimisation d'une fonction**
# Création d'expressions
expr = x**2 + 2*x + 1
print(expr)  # x**2 + 2*x + 1

# Factorisation
factorized = sp.factor(expr)
print(factorized)  # (x + 1)**2

# Développement
expanded = sp.expand((x + y)**3)
print(expanded)  # x**3 + 3*x**2*y + 3*x*y**2 + y**3

#### 4. Difficulté rencontré

- Confusion initiale entre manipulation symbolique et évaluation numérique (ex: pourquoi sp.sqrt(2) retourne √2 et non 1.414)


#### 5. Solutions
 
- Consultation de la documentation officielle et échanges avec les membres du groupe


---

## TPE 2 - [Date: 02/10/2025]

# Binary Cross-Entropy Loss Analysis

## Description du Projet

Ce projet implémente une analyse mathématique de la fonction de perte Binary Cross-Entropy (BCE), couramment utilisée en classification binaire. Il comprend trois tâches principales :

1. **Calcul du gradient** de la BCE par rapport aux prédictions
2. **Analyse de la convexité** via la dérivée seconde
3. **Visualisation et application pratique** sur des données réelles


### Task 1 : Calcul du Gradient
- Définition symbolique de la fonction BCE : `BCE = -[y·log(ŷ) + (1-y)·log(1-ŷ)]/n`
- Calcul de la dérivée première : ` = (y - ŷ)/(n·ŷ·(ŷ - 1))`
- Utilisation de SymPy pour le calcul symbolique

### Task 2 : Analyse de Convexité
- Calcul de la dérivée seconde pour prouver la convexité
- Évaluation numérique à différents points (ŷ = 0.1, 0.5, 0.9)
- Démonstration que `dérivée seconde > 0` pour ŷ ∈ (0,1)

### Task 3 : Application Pratique
- Chargement d'un dataset de classification (`classification_data.csv`)
- Entraînement d'un modèle de régression logistique
- Calcul du BCE moyen sur le dataset
- Visualisation de la courbe BCE avec ligne tangente

## Prérequis

pip install numpy sympy matplotlib pandas scikit-learn


## Structure des Fichiers

project/
│
├── BCE.ipynb               # Notebook principal
├── classification_data.csv     # Dataset d'entrée
└── README.md                   # Ce fichier


## Exécution

### Méthode 1 : Jupyter Notebook
jupyter notebook Untitled.ipynb

### Méthode 2 : JupyterLab

jupyter lab


Puis exécuter toutes les cellules dans l'ordre.

## Résultats Observés

### 1. Gradient de la BCE

gradient(BCE) = -y/ŷ + (1-y)/(1-ŷ)
         ───────────────────────
                  n

Forme simplifiée : `(y - ŷ)/(n·ŷ·(ŷ - 1))`

### 2. Convexité
La dérivée seconde est positive pour tout ŷ ∈ (0,1) :

| ŷ   | dérivée seconde (y=1, n=1) |
|-----|----------------------|
| 0.1 | 100.00               |
| 0.5 | 4.00                 |
| 0.9 | 1.23                 |

**Conclusion** : La fonction est convexe, garantissant un minimum global unique.

### 3. Visualisation

Le graphique montre :
- La courbe BCE décroissante quand ŷ augmente (pour y=1)
- La ligne tangente au point ŷ = 0.5
- Équation de la tangente : `y = -2.00x + 1.69`

### 4. Performance sur Dataset Réel
- **BCE moyen** : ~0.0001 (très faible, indiquant de bonnes prédictions)
- Le modèle de régression logistique performe bien sur les données

## Interprétations Mathématiques

### Propriétés de la BCE

1. **Pénalisation asymétrique** : 
   - Erreurs près de 0 ou 1 sont fortement pénalisées
   - Encourage des prédictions confiantes quand elles sont correctes

2. **Convexité** :
   - Garantit convergence vers le minimum global en optimisation
   - Pas de minima locaux

3. **Gradient** :
   - Plus grand quand la prédiction est éloignée de la vraie valeur
   - Facilite l'apprentissage rapide des erreurs importantes

## Extensions Possibles

- Comparer avec d'autres fonctions de perte (MSE)
- Analyser l'impact de différents points tangents
- Visualiser la surface de perte en 3D avec plusieurs échantillons
- Implémenter l'optimisation par descente de gradient

