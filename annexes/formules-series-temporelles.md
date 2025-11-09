# 📈 Annexe B : Formules de Séries Temporelles

## Concepts Fondamentaux

### Processus Stationnaire

**Définition :** Un processus {Yₜ} est stationnaire si ses propriétés statistiques sont invariantes dans le temps.

**Condition faible :**
- E[Yₜ] = μ (moyenne constante)
- Var(Yₜ) = σ² (variance constante)
- Cov(Yₜ, Yₜ+k) = γ(k) (covariance qui dépend seulement du lag k)

### Racine Unitaire (Test de Dickey-Fuller)

**Test de Dickey-Fuller augmenté (ADF) :**
```
ΔYₜ = α + β Yₜ₋₁ + Σᵢ δᵢ ΔYₜ₋₁ + εₜ
```

**Hypothèses :**
- H₀ : β = 0 (présence de racine unitaire, non stationnaire)
- H₁ : β < 0 (stationnaire)

**Statistique de test :**
```
DF = β̂ / SE(β̂)
```

### Test de Phillips-Perron

**Alternative au test ADF :**
```
Plus robuste aux formes d'hétéroscédasticité
Utilise la covariance de Newey-West pour les écarts-types
```

---

## Modèles ARIMA

### Modèle AR(p) - Autorégressif

**Équation :**
```
Yₜ = μ + φ₁Yₜ₋₁ + φ₂Yₜ₋₂ + ... + φₚYₜ₋ₚ + εₜ
```

**Fonction d'autorégression :**
```
φ(B)Yₜ = μ + εₜ
Où φ(B) = 1 - φ₁B - φ₂B² - ... - φₚBᵖ
```

**Condition de stationnarité :**
- Racines de φ(B) = 0 doivent être à l'extérieur du cercle unité

### Modèle MA(q) - Moyenne Mobile

**Équation :**
```
Yₜ = μ + εₜ + θ₁εₜ₋₁ + θ₂εₜ₋₂ + ... + θₚεₜ₋ₚ
```

**Fonction de moyenne mobile :**
```
Yₜ = μ + θ(B)εₜ
Où θ(B) = 1 + θ₁B + θ₂B² + ... + θₚBᵖ
```

**Condition d'invertibilité :**
- Racines de θ(B) = 0 doivent être à l'extérieur du cercle unité

### Modèle ARMA(p,q)

**Équation générale :**
```
φ(B)Yₜ = μ + θ(B)εₜ
```

**Décomposition :**
```
Yₜ = μ + φ₁Yₜ₋₁ + ... + φₚYₜ₋ₚ + εₜ + θ₁εₜ₋₁ + ... + θₚεₜ₋ₚ
```

### Modèle ARIMA(p,d,q)

**Processus intégré d'ordre d :**
- ARIMA(p,0,q) = ARMA(p,q) (stationnaire)
- ARIMA(p,1,q) = différenciation première
- ARIMA(p,2,q) = différenciation seconde

**Transformation de différenciation :**
```
ΔYₜ = Yₜ - Yₜ₋₁
Δ²Yₜ = ΔYₜ - ΔYₜ₋₁ = Yₜ - 2Yₜ₋₁ + Yₜ₋₂
```

---

## Identification des Ordres p,d,q

### Fonction d'Autocorrélation (ACF)

**Coefficient d'autocorrélation d'ordre k :**
```
ρ(k) = Corr(Yₜ, Yₜ₋ₖ) = γ(k)/γ(0)
```

**Estimation :**
```
r̂(k) = Σ(Yₜ - μ̂)(Yₜ₋ₖ - μ̂) / Σ(Yₜ - μ̂)²
```

### Fonction d'Autocorrélation Partielle (PACF)

**PACF d'ordre k :** Coefficient de corrélation entre Yₜ et Yₜ₋ₖ après suppression de l'effet des lags intermédiaires.

**Pour AR(p) :**
- PACF significative jusqu'à l'ordre p
- PACF ≈ 0 pour k > p

**Pour MA(q) :**
- ACF significative jusqu'à l'ordre q
- ACF ≈ 0 pour k > q

### Critères d'Information

**AIC (Akaike) :**
```
AIC = -2 ln(L̂) + 2(p+q+k+1)
```

**BIC (Schwarz) :**
```
BIC = -2 ln(L̂) + (p+q+k+1) ln(n)
```

**HQIC (Hannan-Quinn) :**
```
HQIC = -2 ln(L̂) + 2(p+q+k+1) ln(ln(n))
```

---

## SARIMA (Modèles Saisonnier)

### Composantes d'une Série Temporelle

**Modèle additif :**
```
Yₜ = Tₜ + Sₜ + Cₜ + εₜ
```

**Modèle multiplicatif :**
```
Yₜ = Tₜ × Sₜ × Cₜ × εₜ
```

Où :
- Tₜ : Tendance (trend)
- Sₜ : Saisonnalité (seasonal)
- Cₜ : Cycle (cyclical)
- εₜ : Bruit blanc (noise)

### SARIMA(p,d,q)(P,D,Q)[s]

**Équation générale :**
```
φ(B) Φ(Bˢ) (1-B)^d (1-Bˢ)^D Yₜ = μ + θ(B) Θ(Bˢ) εₜ
```

**Paramètres :**
- p,q : Ordres non saisonniers AR, MA
- d : Degré de différenciation non saisonnière
- P,Q : Ordres saisonniers AR, MA
- D : Degré de différenciation saisonnière
- s : Période saisonnière (12 pour données mensuelles)

---

## Modèles Exponentiels

### Lissage Exponentiel Simple (SES)

**Équation :**
```
Lₜ = α Yₜ + (1-α) Lₜ₋₁
```

Où :
- Lₜ : Niveau estimé à l'instant t
- α ∈ [0,1] : Paramètre de lissage

**Prévision :**
```
Ŷₜ₊₁ = Lₜ
```

### Lissage Exponentiel Double (Holt)

**Niveau :**
```
Lₜ = α Yₜ + (1-α)(Lₜ₋₁ + Tₜ₋₁)
```

**Tendance :**
```
Tₜ = β (Lₜ - Lₜ₋₁) + (1-β) Tₜ₋₁
```

**Prévision h-pas :**
```
Ŷₜ₊ₕ = Lₜ + h Tₜ
```

### Lissage Exponentiel Triple (Holt-Winters)

**Modèle additif :**
```
Lₜ = α (Yₜ - Sₜ₋s) + (1-α)(Lₜ₋₁ + Tₜ₋₁)
Tₜ = β (Lₜ - Lₜ₋₁) + (1-β) Tₜ₋₁
Sₜ = γ (Yₜ - Lₜ₋₁ - Tₜ₋₁) + (1-γ) Sₜ₋s
```

**Prévision :**
```
Ŷₜ₊ₕ = Lₜ + h Tₜ + Sₜ₊ₕ₋s
```

---

## Prophet (Meta/Facebook)

### Modèle Général

**Équation :**
```
y(t) = g(t) + s(t) + h(t) + εₜ
```

Où :
- g(t) : Tendance (linéaire ou logistique)
- s(t) : Saisonnalité (annuelle, mensuelle, etc.)
- h(t) : Effets de vacances/chocs externes
- εₜ : Bruit (distribution normale ou Student's t)

### Tendance

**Linéaire :**
```
g(t) = (k + a(t)ᵀ δ) t + (m + a(t)ᵀ γ)
```

**Logistique :**
```
g(t) = C / (1 + exp(-k(t - m)))
```

### Saisonnalité

**Fourier series :**
```
s(t) = Σ_{n=1}^N [a_n cos(2π n t / P) + b_n sin(2π n t / P)]
```

Où P = période saisonnière

### Changements de Tendance

**Détection automatique :**
- Utilise historique pour estimer changements probables
- Paramètre `changepoint_prior_scale` contrôle sensibilité

---

## Évaluation des Prévisions

### Métriques d'Erreurs

**Erreur absolue moyenne (MAE) :**
```
MAE = (1/n) Σ |yᵢ - ŷᵢ|
```

**Erreur quadratique moyenne (MSE) :**
```
MSE = (1/n) Σ (yᵢ - ŷᵢ)²
```

**RMSE (Root Mean Square Error) :**
```
RMSE = √[(1/n) Σ (yᵢ - ŷᵢ)²]
```

**Erreur absolue moyenne en pourcentage (MAPE) :**
```
MAPE = (100/n) Σ |yᵢ - ŷᵢ| / |yᵢ|
```

### Tests de Prédiction

**Test de Diebold-Mariano :**
```
DM = [Σ dᵢ² / Σ (yᵢ - ŷᵢ)²]^(1/2)
Où dᵢ = erreur_modèle1 - erreur_modèle2
```

### Validation Temporaire

**Rolling forecast origin :**
- Estimation sur données passées
- Prévision sur horizon fixe
- Déplacement de la fenêtre temporelle
- Calcul d'erreurs cumulées

---

## ⚠️ ATTENTION : Pièges Courants

### **Stationnarité Nécessaire**
```
❌ ARIMA sur série non stationnaire → Prévisions aberrantes
✅ Test ADF systématique avant modélisation
```

### **Saisonnalité Non Détectée**
```
❌ Oubli composante saisonnière → Erreurs systématiques
✅ Analyse ACF/PACF sur périodes saisonnières
```

### **Overfitting**
```
❌ Ordres p,q trop élevés → Modèle complexe, peu généralisable
✅ Critères AIC/BIC pour sélection optimale
```

### **Extrapolation Hors Échantillon**
```
❌ Prévisions trop lointaines → Incertitude exponentielle
✅ Horizons réalistes selon stabilité historique
```

---

## 💡 CONSEIL : Choix du Modèle

### **Guide Pratique**

| Situation | Modèle Recommandé | Justification |
|-----------|-------------------|----------------|
| **Données stables** | ARIMA | Modèle statistique robuste |
| **Tendance marquée** | Holt-Winters | Gestion tendance + saisonnalité |
| **Données irrégulières** | Prophet | Flexible, gère anomalies |
| **Prévisions court terme** | SES | Simple, réactif |
| **Grand volume données** | ARIMA automatique | Évolutif, scalable |
| **Business forecasting** | Prophet | Interprétable, production-ready |

### **Workflow Recommandé**

1. **Analyse exploratoire :**
   - Graphiques série temporelle
   - Décomposition (trend/seasonal/residual)
   - Tests de stationnarité

2. **Préparation données :**
   - Gestion valeurs manquantes
   - Transformation si nécessaire
   - Création variables externes

3. **Sélection modèle :**
   - Comparaison AIC/BIC
   - Validation croisée temporelle
   - Tests prédictifs

4. **Validation :**
   - Métriques sur données test
   - Analyse résidus
   - Robustesse scénarios

---

## ✓ BONNES PRATIQUES : Prévisions Séries Temporelles

### **1. Préparation Rigoureuse**
```
□ Analyse graphique complète (trend, saisonnalité, outliers)
□ Tests de stationnarité (ADF, KPSS)
□ Transformation si nécessaire (différenciation, log)
□ Gestion valeurs manquantes (interpolation, modèle)
```

### **2. Sélection Modèle Méthodique**
```
□ Comparaison modèles concurrents
□ Validation croisée temporelle
□ Métriques prédictives appropriées
□ Tests statistiques significativité
```

### **3. Évaluation Critique**
```
□ Analyse résidus (indépendance, normalité)
□ Tests prédictifs hors échantillon
□ Stabilité paramètres temporelle
□ Robustesse scénarios économiques
```

### **4. Communication Transparente**
```
□ Intervalles de confiance réalistes
□ Sensibilité aux hypothèses
□ Limites du modèle explicites
□ Mises à jour régulières prévues
```

### **5. Gouvernance Production**
```
□ Monitoring performance continu
□ Retraining automatique programmé
□ Alertes anomalies détectées
□ Documentation complète maintenue
```

---

## 📊 EXEMPLES CONCRETS

### **Exemple 1 : Prévision Ventes Mensuelles**

**Données :** 60 mois de ventes d'un produit
```
Modèle identifié : ARIMA(1,1,1)(0,1,1)[12]
Paramètres :
- φ₁ = 0.45 (autorégression mensuelle)
- θ₁ = -0.32 (moyenne mobile)
- Θ₁ = -0.67 (saisonnalité annuelle)

Précision : MAPE = 8.2% sur données test
```

### **Exemple 2 : Prévision Trafic Web**

**Données :** Visites quotidiennes site e-commerce
```
Modèle Prophet avec :
- Tendance linéaire : k = 12.5 visites/jour
- Saisonnalité hebdomadaire : week-end +45%
- Vacances : Noël +120%, soldes +85%

Précision : RMSE = 245 visites sur moyenne 1200
```

### **Exemple 3 : Prévision Demande Énergie**

**Données :** Consommation électrique horaire
```
SARIMA(2,1,1)(1,0,1)[24] avec :
- Composante AR(2) : dépendance 2 dernières heures
- Différenciation première : tendance éliminée
- Saisonnalité horaire : pic 19h, creux 4h

MAPE = 4.8% sur prévisions 24h
```

---

## 🔬 AVANCÉ : Modèles Multivariés

### **VAR (Vector Autoregression)**

**Système d'équations :**
```
Y₁,t = α₁ + Σ φ₁ᵢ Y₁,t₋ᵢ + Σ ψ₁ⱼ Y₂,t₋ⱼ + ε₁,t
Y₂,t = α₂ + Σ φ₂ᵢ Y₂,t₋ᵢ + Σ ψ₂ⱼ Y₁,t₋ⱼ + ε₂,t
```

### **VECM (Vector Error Correction Model)**

**Pour séries cointegrées :**
```
ΔY₁,t = α₁ (Y₁,t₋₁ - β Y₂,t₋₁) + Σ autres termes + ε₁,t
ΔY₂,t = α₂ (Y₁,t₋₁ - β Y₂,t₋₁) + Σ autres termes + ε₂,t
```

### **GARCH (Generalized Autoregressive Conditional Heteroskedasticity)**

**Pour volatilité variable :**
```
σₜ² = ω + Σ αᵢ εₜ₋ᵢ² + Σ βⱼ σₜ₋ⱼ²
```

**Application :** Modélisation de la volatilité financière, risques de marché.

---

## 🎯 CONCLUSION : Maîtrise des Séries Temporelles

La modélisation de séries temporelles combine **rigueur statistique** et **intuition métier** pour produire des prévisions fiables et actionnables.

**Points clés réussites :**
- ✅ Compréhension profonde des données historiques
- ✅ Sélection méthodique du modèle approprié
- ✅ Validation rigoureuse des prévisions
- ✅ Communication transparente des incertitudes

**Évolution technologique :** L'intégration d'IA (LSTM, Transformer) ouvre de nouvelles frontières pour capturer des patterns complexes dans les données temporelles.