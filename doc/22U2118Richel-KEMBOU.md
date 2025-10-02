# Suivi personnel – [KEMBOU FOSSO RICHEL]

##  Informations
- **Nom :** KEMBOU FOSSO RICHEL  
- **Classe :** MASTER 1 - INFORMATIQUE FONDA - DEPARTEMENT D'INFORMATIQUE - UNIVERSITE DE YAOUNDE I  
- **Projet :** Calcul symbolique avec Python (Sympy)  

---

##  Objectifs personnels
- Comprendre les bases du calcul symbolique  
- Apprendre à utiliser Sympy pour manipuler des expressions mathématiques  
- Réaliser des implémentations pratiques dans le notebook fourni  

---

## Travail réalisé

### Jour 1 [Date:26/09/2025]
- Lecture de la présentation théorique sur le calcul symbolique  
- Installation de Sympy dans python 
- Découverte des principales fonctions Sympy et  Manipulation simple de symboles (ex : factorisation, dérivation, evaluation en des points, affichage mathématiques)
- Implementation dans le notebook **

### Jour 3 [Date:1/10/2025]
- Création de la présentation en pdf.

### Jour 2
- Création du Repository dans l'organisation **MKKT-4127-Optimisation-TPE**
- Création de la branche "22U2118_KEMBOU".
- 


---

##  Compétences acquises
- Utilisation de Python pour le calcul symbolique  
- Maîtrise des fonctions principales de Sympy : `simplify`, `diff`, `integrate`, `solve`

---

## 📌 C'EST QUOI L'ENTROPIE CROISEE CATEGORIELLE

L'**entropie croisée catégorielle** est une **FONCTION DE LOSS**  pour la classification multi-classes.

```python
def entropie_croisee(y_true, y_pred):
    return -np.sum(y_true * np.log(y_pred))

```
en langage Symbolique on le représente par le bout de code  suivante 
```python
i, N = sp.symbols('i N', integer=True, positive=True)
y = sp.Function('y')(i)
y_hat = sp.Function('y_hat')(i)

ECC = - sp.summation(y * sp.log(y_hat), (i, 1, N))
sp.pretty_print(ECC)
```

### Convexité
ce qui la justifie c'est l'expression de sa dérivée seconde qui est toujours positive en tout point prédit marqué **y_hat** Dans notre cas. Pour avoir ce résultat, et le vérifier il faut suivre le code suivant

```python
grad_2_ecc = sp.diff(ECC, y_hat, 2) #Ici on met 2 pour marquer dérivée seconde.
sp.pretty_print(grad_2_ecc) 
```
**Cela affecte directement la Hessienne d'une telle fonction de cout et dont toutes les valeurs propres seront toujours positives.**
  

---

