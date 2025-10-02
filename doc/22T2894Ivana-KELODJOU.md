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