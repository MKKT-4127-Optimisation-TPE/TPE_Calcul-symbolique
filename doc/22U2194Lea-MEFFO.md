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
- etude de la convexite sur la fonction MSE 
- application de la mse sur la regression lineaire

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
# ############################################################################################################################"
-------------------------------------------------------------------------------------------------------------------------------

-------------------------------------------------------
##              TPE1 ETUDE DES FONCTIONS D ERREURS 
-------------------------------------------------------

Le devoirse concentre également sur l'analyse théorique de la fonction de coût utilisée, l'Erreur Quadratique Moyenne (EQM), en démontrant sa convexité à l'aide du calcul symbolique.

## Étude de la Fonction de Perte (EQM)

L'EQM (ou MSE) est la fonction de coût utilisée par la méthode des moindres carrés pour trouver les coefficients optimaux β.

### Formule et Rôle

La fonction est définie par :
EQM=N1​i=1∑N​(y^​i​−yi​)2

Le rôle de l'EQM est de quantifier l'erreur du modèle en pénalisant fortement les grandes différences entre les prédictions (y^​) et les valeurs réelles (y). L'entraînement des modèles cherche à minimiser cette valeur.


### Analyse de la Convexité (SymPy)

La convexité est une propriété cruciale car elle garantit que la fonction de coût a un minimum global unique, ce qui signifie que tout algorithme d'optimisation (comme la Descente de Gradient) trouvera la meilleure solution possible sans rester bloqué dans des minima locaux.

L'analyse symbolique de l'EQM par rapport à la prédiction (y^​) est réalisée en calculant la dérivée seconde (la Hessienne) :
Dérivée	Formule	Analyse
Première Dérivée (Gradient)	∂y^​∂EQM​=N2(y^​−y)​	Nécessaire pour la Descente de Gradient.
Seconde Dérivée (Hessienne)	∂y^​2∂2EQM​=N2​	Puisque N>0, la Hessienne est toujours positive.

### Conclusion de Convexité :

Puisque la dérivée seconde est toujours positive (≥0), la fonction de perte EQM est convexe. La surface de coût est un "bol" parfait, garantissant que l'entraînement du modèle trouvera le β optimal.

## Modélisation et Résultats

### Préparation des Données

Le script effectue un chargement robuste pour gérer les séparateurs (virgule ou espace) et renomme la colonne cible en y.

   -  Variables Explicatives (X) : X1​, X2​

   -  Variable Cible (y) : y (renommée depuis Y_Cible)

### Modèle Linéaire Multiple

Le modèle linéaire simple permet d'établir une ligne de base des performances.

Équation	y=β1​X1​+β2​X2​+β0
MSE (EQM)	mse_linear	Niveau de l'erreur minimale atteinte.
## Visualisations Générées

Le script produit plusieurs figures dans Matplotlib :

    Analyse Exploratoire (VAD) : Affichage des relations X1​ vs y, X2​ vs y, et la distribution 3D de l'ensemble des données.

    Surface de Coût EQM : Représentation 3D de la fonction EQM en fonction des coefficients β1​ et β2​. Le point rouge au fond de ce "bol" convexe montre exactement la solution (β1,opt​,β2,opt​) trouvée par l'algorithme.


##  Compétences acquises
- Utilisation de Python pour le calcul symbolique  
- renforcement des competences sur le calcul des derivées à la main
- Utilisation des fonctions principales de Sympy : `simplify`, `diff`, `integrate`, `solve`  
- Capacité à appliquer le calcul symbolique dans un contexte concret (ex : Regression linéaire )  

-------------------------------------------------------------------------------------------------------------------------
##  Améliorations futures
- Approfondir l’utilisation de Sympy dans l" etude d'autres fonctions de coût
- Developpement des reflexes de calculs à la main avant de modéliser sur machine grace à la ibliothèque dans le but de mieux comprendre les opérations faites par ces dernieres en arriere plan
