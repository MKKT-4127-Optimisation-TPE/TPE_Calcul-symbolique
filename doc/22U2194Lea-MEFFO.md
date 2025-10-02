--------------------------------------------------------------------------------------------------------------------------------------
# SUIVI PERSONNEL DE L'ETUDIANT
---------------------------------------------------------------------------------------------------------------------------------------

## CALCUL SYMBOLIQUE ET PRESENTATION DE LA BIBLIOTHEQUE SYMPY


##  Informations
- **NomS & pRENOMS :** MEFFO TAHAFO LEA JECY
- **Matricule:** 22U2194
- **Spécialité :** MASTER 1 SPÉCIALITÉ DATASCIENCES 
- **Projet :** Calcul symbolique avec Python (Sympy)  


-----------------------------------------------------------------------------------------------------------------------------------------
##  Objectifs personnels
- Comprendre les bases du calcul symbolique  
- Apprendre à utiliser Sympy pour manipuler des expressions mathématiques  
- Réaliser des implémentations pratiques dans le notebook fourni  


### Définition

Le calcul symbolique  consiste à manipuler des expressions mathématiques sous forme symbolique plutôt que numérique (c’est à dire,le calcul  numérique, manipule des nombres concrets alors que le calcul symbolique,manipule des symboles, variables et expressions sans forcément les évaluer en nombres... )     Contrairement au calcul numérique qui travaille avec des valeurs approchées, le calcul symbolique conserve les variables et constantes sous leur forme exacte.


### Caractéristiques principales

- Manipulation d'expressions avec des variables non évaluées
- Calculs exacts sans approximation numérique
- Capacité à effectuer des dérivations, intégrations, simplifications algébriques
- Résolution d'équations de manière exacte


### Qu'est-ce que SymPy ?

SymPy est une bibliothèque Python open-source dédiée au calcul symbolique. Elle offre des fonctionnalités complètes pour :

- L'algèbre symbolique
- Le calcul différentiel et intégral
- La résolution d'équations
- L'algèbre linéaire symbolique...


### Modules principaux :

- core : Expressions de base
- solvers : Résolution d'équations
- calculus : Dérivées, intégrales
- matrices : Algèbre linéaire
- stats : Statistiques symboliques


### Exemples d'Utilisation de SymPy
import sympy as sp

#### Déclaration de variables symboliques
x, y, z = sp.symbols('x y z')
a, b = sp.symbols('a b')

#### Déclaration de fonction symbolique
f = sp.Function('f')(x)


----------------------------------------------------------------------------------------------------------------------

##  Journal de travail

### jour 1:Jeudi 26 Septembre 2025
- Installation de sympy
- Qu'est ce que c'est le calcul symbolique?

### Jour 2:Mercredi 02 Octobre 2025
- Manipulation simple de symboles (ex : factorisation, dérivation,gradient)  
- Découverte des principales fonctions Sympy  

### Jour 3:Jeudi 03 Octobre 2025
- Configuration de l'organisation Github
- Création de branches  

------------------------------------------------------------------------------------------------------------------------

##  Compétences acquises
- Utilisation de Python pour le calcul symbolique  
- Utilisation des fonctions principales de Sympy : `simplify`, `diff`, `integrate`, `solve`  
- Capacité à appliquer le calcul symbolique dans un contexte concret (ex : minimiser une fonction de coût )  

-------------------------------------------------------------------------------------------------------------------------
##  Améliorations possibles
- Approfondir l’utilisation de Sympy dans le cadre du cours d'optimisation
- Explorer d’autres bibliothèques de calcul formel (ex : SageMath)  
- Relier Sympy avec NumPy pour comparer calcul symbolique et numérique  

---------------------------------------------------------------------------------------------------------------------------