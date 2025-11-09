# 📐 Annexe A : Formules de Régression et Classification

## Régression Linéaire Simple

### Formule Fondamentale
```
ŷ = β₀ + β₁x
```
Où :
- ŷ = Valeur prédite (variable dépendante)
- β₀ = Ordonnée à l'origine (intercept)
- β₁ = Coefficient de pente (slope)
- x = Variable indépendante

### Calcul des Coefficients par Moindres Carrés

**Coefficient de pente β₁ :**
```
β₁ = Σ[(xᵢ - μₓ)(yᵢ - μᵧ)] / Σ(xᵢ - μₓ)²
```

**Ordonnée à l'origine β₀ :**
```
β₀ = μᵧ - β₁μₓ
```

### Métriques d'Évaluation

**Coefficient de détermination R² :**
```
R² = 1 - (SS_res / SS_tot)
   = Σ(ŷᵢ - μᵧ)² / Σ(yᵢ - μᵧ)²
```
- R² ∈ [0,1] : Plus proche de 1 = meilleur modèle
- R² = 0 : Modèle n'explique aucune variance
- R² = 1 : Modèle explique parfaitement les données

**Erreur quadratique moyenne (MSE) :**
```
MSE = (1/n) Σ(yᵢ - ŷᵢ)²
```

**Racine carrée de l'erreur quadratique moyenne (RMSE) :**
```
RMSE = √[(1/n) Σ(yᵢ - ŷᵢ)²]
```

---

## Régression Linéaire Multiple

### Formule Générale
```
ŷ = β₀ + β₁x₁ + β₂x₂ + ... + βₖxₖ + ε
```

### Méthode des Moindres Carrés Ordinaires (OLS)

**Solution matricielle :**
```
β̂ = (XᵀX)⁻¹XᵀY
```

Où :
- X = Matrice des variables indépendantes (n × p)
- Y = Vecteur des valeurs observées (n × 1)
- β̂ = Vecteur des coefficients estimés (p × 1)

### Tests Statistiques

**Test F pour significativité globale :**
```
F = [SSR/k] / [SSE/(n-k-1)]
```
- SSR = Somme des carrés de régression
- SSE = Somme des carrés des résidus
- k = Nombre de variables indépendantes
- n = Nombre d'observations

**Test t pour chaque coefficient :**
```
t = β̂ⱼ / SE(β̂ⱼ)
```
- SE(β̂ⱼ) = Erreur standard du coefficient j
- Comparé à distribution t de Student

### Problèmes Courants et Solutions

**Multicolinéarité :**
```
VIFⱼ = 1/(1-Rⱼ²)
```
- VIF > 10 : Forte multicolinéarité
- Solution : Supprimer variables corrélées

**Hétéroscédasticité :**
- Test de Breusch-Pagan ou White
- Solution : Transformation logarithmique ou WLS

---

## Régression Polynomiale

### Formule d'Ordre 2
```
ŷ = β₀ + β₁x + β₂x²
```

### Formule d'Ordre k
```
ŷ = β₀ + β₁x + β₂x² + ... + βₖxᵏ
```

### Choix de l'Ordre Optimal

**Critère d'information d'Akaike (AIC) :**
```
AIC = 2k + n ln(SSE/n)
```

**Critère d'information bayésien (BIC) :**
```
BIC = k ln(n) + n ln(SSE/n)
```

### Validation Croisée

**Validation croisée k-fold :**
```
Erreur CV = (1/k) Σ [Erreur foldᵢ]
```

---

## Régression Logistique Binaire

### Fonction Logit
```
logit(p) = ln(p/(1-p)) = β₀ + β₁x₁ + ... + βₖxₖ
```

### Fonction Sigmoïde (Probabilité)
```
p(y=1|x) = 1 / (1 + e^(-(β₀ + β₁x₁ + ... + βₖxₖ)))
```

### Estimation des Paramètres

**Méthode du maximum de vraisemblance :**
- Pas de solution analytique fermée
- Utilisation d'algorithmes itératifs (Newton-Raphson)

### Métriques d'Évaluation

**Log-vraisemblance :**
```
LL = Σ[yᵢ ln(p̂ᵢ) + (1-yᵢ) ln(1-p̂ᵢ)]
```

**Déviance :**
```
Dév = -2 LL
```

**Pseudo R² de McFadden :**
```
R²_McFadden = 1 - (LL_modele / LL_null)
```

---

## Arbres de Décision

### Mesure d'Impureté (Classification)

**Indice de Gini :**
```
Gini(S) = 1 - Σ pᵢ²
```

**Entropie :**
```
Entropie(S) = - Σ pᵢ log₂(pᵢ)
```

### Gain d'Information
```
Gain(S,A) = Entropie(S) - Σ (|Sᵥ|/|S|) × Entropie(Sᵥ)
```

### Mesure d'Homogénéité (Régression)

**Erreur quadratique moyenne :**
```
MSE = (1/n) Σ(yᵢ - μ_S)²
```

**Réduction d'impureté :**
```
Δ = MSE_parent - Σ (nᵥ/n) × MSE_enfant
```

### Élagage (Pruning)

**Coût-complexité :**
```
C(T) = SSE(T) + α × |T|
```
Où |T| = nombre de nœuds terminaux

---

## Forêts Aléatoires (Random Forest)

### Agrégation de Bootstrap (Bagging)

**Échantillonnage bootstrap :**
- Taille échantillon = n (même taille que l'original)
- Probabilité de sélection = 1/n pour chaque observation
- Remplacement : observations peuvent être sélectionnées plusieurs fois

### Construction d'Arbre Individuel

**Sous-ensemble de variables :**
- m = √p pour classification
- m = p/3 pour régression
- Où p = nombre total de variables

### Prédiction Finale

**Classification :**
```
Classe majoritaire = argmax Σ I(ŷᵢ = classe)
```

**Régression :**
```
Prédiction moyenne = (1/B) Σ ŷᵢ
```

### Importance des Variables

**Decrease in Gini/Accuracy :**
```
Importanceᵥ = (1/B) Σ Δᵢᵥ
```
Où Δᵢᵥ = diminution d'impureté due à la variable v dans l'arbre i

---

## SVM (Support Vector Machines)

### Formulation Primal (Cas linéaire)
```
Minimize: (1/2)||w||² + C Σ ξᵢ
Subject to: yᵢ(w·xᵢ + b) ≥ 1 - ξᵢ, ξᵢ ≥ 0
```

### Formulation Dual
```
Maximize: Σ αᵢ - (1/2) Σ Σ αᵢ αⱼ yᵢ yⱼ xᵢ·xⱼ
Subject to: Σ αᵢ yᵢ = 0, 0 ≤ αᵢ ≤ C
```

### Noyau RBF (Radial Basis Function)
```
K(xᵢ,xⱼ) = exp(-γ||xᵢ - xⱼ||²)
```

### Noyau Polynomial
```
K(xᵢ,xⱼ) = (γ xᵢ·xⱼ + r)^d
```

### Paramètres Critiques

**Paramètre de régularisation C :**
- C élevé → Moins de violations de marge, risque de surapprentissage
- C faible → Plus de violations, modèle plus généralisable

**Paramètre γ (pour RBF) :**
- γ élevé → Fonction de décision très irrégulière
- γ faible → Fonction de décision très lisse

---

## Réseaux de Neurones

### Neurone Artificiel
```
z = Σ wᵢ xᵢ + b
a = σ(z)
```

### Fonctions d'Activation

**Sigmoïde :**
```
σ(z) = 1/(1 + e^(-z))
```

**ReLU (Rectified Linear Unit) :**
```
ReLU(z) = max(0, z)
```

**Tanh :**
```
tanh(z) = (e^z - e^(-z))/(e^z + e^(-z))
```

### Rétropropagation (Backpropagation)

**Erreur quadratique :**
```
E = (1/2) Σ (y - ŷ)²
```

**Gradient descent :**
```
w := w - η ∂E/∂w
```

### Optimisation

**Adam optimizer :**
```
m_t = β₁ m_(t-1) + (1-β₁) g_t
v_t = β₂ v_(t-1) + (1-β₂) g_t²
w_t = w_(t-1) - η m̂_t / (√v̂_t + ε)
```

### Régularisation

**Dropout :**
- Probabilité p de garder un neurone actif
- Prévention du surapprentissage

**Batch Normalization :**
```
x̂ = (x - μ_batch)/√(σ_batch² + ε)
x̃ = γ x̂ + β
```

---

## Évaluation des Modèles

### Métriques de Classification

**Matrice de Confusion :**
```
               Prédit Positif    Prédit Négatif
Réel Positif         TP                FN
Réel Négatif         FP                TN
```

**Précision (Precision) :**
```
Precision = TP / (TP + FP)
```

**Rappel (Recall) :**
```
Recall = TP / (TP + FN)
```

**F1-Score :**
```
F1 = 2 × (Precision × Recall) / (Precision + Recall)
```

**Spécificité :**
```
Specificity = TN / (TN + FP)
```

### Courbe ROC et AUC

**Taux de vrais positifs :**
```
TPR = TP / (TP + FN)
```

**Taux de faux positifs :**
```
FPR = FP / (FP + TN)
```

**AUC (Area Under Curve) :**
```
AUC = ∫ TPR d(FPR) de 0 à 1
```

### Métriques de Régression

**Erreur absolue moyenne (MAE) :**
```
MAE = (1/n) Σ |yᵢ - ŷᵢ|
```

**Erreur quadratique moyenne (MSE) :**
```
MSE = (1/n) Σ (yᵢ - ŷᵢ)²
```

**Erreur absolue médiane (MedAE) :**
```
MedAE = médiane(|yᵢ - ŷᵢ|)
```

**Coefficient de détermination ajusté :**
```
R²_ajusté = 1 - [(1-R²)(n-1)] / (n-k-1)
```

---

## Validation Croisée

### K-Fold Cross-Validation

**Erreur de validation :**
```
CV_error = (1/K) Σ MSE_foldᵢ
```

### Leave-One-Out Cross-Validation (LOOCV)

**Erreur LOOCV :**
```
LOOCV_error = (1/n) Σ MSE_(-i)
```

### Stratified K-Fold

**Pour classification déséquilibrée :**
- Préservation des proportions de classes dans chaque fold
- Réduction de la variance de l'estimation d'erreur

---

## Sélection de Modèles

### Critères d'Information

**AIC (Akaike Information Criterion) :**
```
AIC = 2k - 2 ln(L̂)
```

**BIC (Bayesian Information Criterion) :**
```
BIC = k ln(n) - 2 ln(L̂)
```

### Méthodes de Régularisation

**Ridge Regression (L2) :**
```
Minimize: Σ(yᵢ - ŷᵢ)² + λ Σ βⱼ²
```

**Lasso Regression (L1) :**
```
Minimize: Σ(yᵢ - ŷᵢ)² + λ Σ |βⱼ|
```

**Elastic Net :**
```
Minimize: Σ(yᵢ - ŷᵢ)² + λ₁ Σ |βⱼ| + λ₂ Σ βⱼ²
```

---

## ⚠️ ATTENTION : Interprétation des Métriques

### **Problèmes Courants**

**Overfitting :**
- Métriques excellentes sur données d'entraînement
- Performance dégradée sur nouvelles données
- Solution : Validation croisée, régularisation

**Data Leakage :**
- Information du futur dans données passées
- Métriques artificiellement gonflées
- Solution : Séparation temporelle stricte

**Classes Déséquilibrées :**
- Métriques biaisées vers classe majoritaire
- Precision/Recall plus informatifs que accuracy
- Solution : Métriques équilibrées, rééchantillonnage

### **Bonnes Pratiques**

**Validation croisée systématique :**
- Au minimum 5-fold CV
- Stratification pour classification
- Répétitions multiples pour robustesse

**Comparaison de modèles :**
- Tests statistiques sur différences de performance
- Considération complexité vs performance
- Validation sur données indépendantes

**Métriques métier pertinentes :**
- Alignement avec objectifs business
- Coûts différentiels des erreurs
- Seuils de décision optimisés

---

## 💡 CONSEIL : Choix du Modèle

### **Guide de Sélection**

| Type de Problème | Données | Modèle Recommandé | Justification |
|------------------|---------|-------------------|----------------|
| **Linéaire simple** | n<1000, p<10 | Régression linéaire | Interprétable, rapide |
| **Relations complexes** | n>1000 | Random Forest | Robuste, non-paramétrique |
| **Précision maximale** | Données propres | Gradient Boosting | Performance supérieure |
| **Interprétabilité** | Réglementé | Régression logistique | Transparente, probabiliste |
| **Données haute dim.** | p>>n | SVM avec noyau | Efficace en grande dimension |
| **Séquences/temps** | Données temporelles | ARIMA, LSTM | Spécialisé séries temporelles |

### **Considérations Pratiques**

**Temps de calcul :**
- Modèles linéaires : Formation instantanée
- Random Forest : Quelques minutes
- Neural Networks : Heures/jours

**Maintenabilité :**
- Modèles simples : Faciles à maintenir
- Modèles complexes : Expertise spécialisée requise

**Scalabilité :**
- Modèles linéaires : Excellente scalabilité
- SVM : Limitée à n~10,000
- Neural Networks : Scalable avec ressources

---

## ✓ BONNES PRATIQUES : Workflow ML Complet

### **1. Préparation des Données**
- Analyse exploratoire (EDA)
- Nettoyage et imputation
- Feature engineering
- Sélection de variables

### **2. Sélection et Entraînement**
- Baseline simple (régression linéaire)
- Comparaison de modèles
- Optimisation d'hyperparamètres
- Validation croisée

### **3. Évaluation et Interprétation**
- Métriques appropriées au problème
- Analyse d'erreurs
- Interprétabilité du modèle
- Tests de robustesse

### **4. Déploiement et Monitoring**
- Mise en production
- Monitoring performance
- Retraining automatique
- Gestion du drift de données

### **5. Documentation et Gouvernance**
- Code versionné
- Métadonnées complètes
- Tests automatisés
- Conformité réglementaire