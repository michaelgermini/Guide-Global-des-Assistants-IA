# 🔢 Annexe C : Exemples Mathématiques Concrets

## 1. Algèbre Linéaire Appliquée

### **Exemple : Système de Recommandation**

**Problème :** Prédire les notes d'utilisateurs pour des films non vus.

**Matrice utilisateurs-films :**
```
Utilisateurs ↓    Film A    Film B    Film C    Film D
Alice              5         4         ?         3
Bob                4         ?         5         2
Charlie            ?         4         4         5
Diana              3         3         ?         4
```

**Décomposition en valeurs singulières (SVD) :**
```
M = U × Σ × Vᵀ

Matrice U (utilisateurs × facteurs latents) :
Alice   : [0.45, 0.22, 0.78]
Bob     : [0.67, 0.31, 0.45]
Charlie : [0.52, 0.69, 0.38]
Diana   : [0.38, 0.55, 0.62]

Σ (valeurs singulières) : [12.3, 8.7, 5.2]

Matrice V (films × facteurs latents) :
Film A  : [0.41, 0.58, 0.29]
Film B  : [0.52, 0.34, 0.67]
Film C  : [0.48, 0.71, 0.35]
Film D  : [0.39, 0.46, 0.58]
```

**Prédiction note Alice pour Film C :**
```
Notê = U_Alice · Σ · V_FilmC
     = [0.45, 0.22, 0.78] · [12.3, 8.7, 5.2] · [0.48, 0.71, 0.35]
     = 4.2 (arrondi à 4)
```

---

## 2. Probabilités et Statistiques

### **Exemple : Test A/B E-commerce**

**Contexte :** Test de deux designs de page produit.

**Données collectées :**
```
Design A : 1245 visiteurs, 89 conversions (7.15%)
Design B : 1187 visiteurs, 112 conversions (9.43%)
```

**Test du χ² d'indépendance :**
```
Tableau de contingence :
                    Converti    Non converti    Total
Design A            89          1156            1245
Design B            112         1075            1187
Total               201         2231            2432

χ² = Σ (observé - attendu)² / attendu
   = (89-75.3)²/75.3 + (1156-1169.7)²/1169.7 + (112-125.7)²/125.7 + (1075-1061.3)²/1061.3
   = 2.48 + 0.16 + 1.48 + 0.09 = 4.21

ddl = (2-1)×(2-1) = 1
Seuil χ² 0.05 = 3.84

Conclusion : χ² = 4.21 > 3.84 → Différence significative !
```

---

## 3. Optimisation Mathématique

### **Exemple : Programmation Linéaire - Optimisation Stock**

**Problème :** Maximiser profit tout en respectant contraintes de stockage.

**Variables :**
```
x₁ = quantité produit A produite (unités)
x₂ = quantité produit B produite (unités)
```

**Fonction objectif :**
```
Maximiser : Profit = 50x₁ + 40x₂
```

**Contraintes :**
```
Matière première : 2x₁ + 3x₂ ≤ 120 kg
Main d'œuvre     : 4x₁ + 2x₂ ≤ 100 h
Stockage         : x₁ + 2x₂ ≤ 60 m³
Non-négativité   : x₁, x₂ ≥ 0
```

**Solution optimale (méthode simplex) :**
```
x₁ = 20, x₂ = 26.67
Profit maximum = 50×20 + 40×26.67 = 2133.33€
```

---

## 4. Théorie des Graphes

### **Exemple : Réseau Social d'Influence**

**Graphe :** 6 personnes connectées sur LinkedIn.

**Matrice d'adjacence :**
```
    Alice Bob Charlie Diana Eve Frank
Alice  0     1    1      0     0    1
Bob    1     0    1      1     0    0
Charlie1     1    0      1     1    0
Diana  0     1    1      0     1    1
Eve    0     0    1      1     0    1
Frank  1     0    0      1     1    0
```

**Centralité de degré :**
```
Alice : 3 connexions (plus influente)
Charlie : 3 connexions
Diana : 3 connexions
Bob : 2 connexions
Eve : 2 connexions
Frank : 3 connexions
```

**Centralité d'intermédiarité (pour chemins courts) :**
```
Charlie : 4 (contrôle le flux d'information)
Alice : 3
Diana : 3
```

---

## 5. Calcul Différentiel

### **Exemple : Optimisation Prix - Elasticité**

**Fonction de demande :**
```
Q = 1000 × P^(-1.5)  (loi puissance)
```

**Revenus :**
```
R = P × Q = 1000 × P^(-1.5) × P = 1000 × P^(-0.5)
```

**Dérivée première (marge) :**
```
dR/dP = 1000 × (-0.5) × P^(-1.5) = -500 × P^(-1.5)
```

**Dérivée seconde :**
```
d²R/dP² = -500 × (-1.5) × P^(-2.5) = 750 × P^(-2.5) > 0
```
Concavité confirmée → maximum existe.

**Prix optimal :**
```
dR/dP = 0 ⇒ P^(-1.5) = 0 (impossible)
Utilisons méthode Newton ou analyse limite.

Pour P→0 : R→∞ (illimité)
Pour P→∞ : R→0

Recherche maximum numérique :
P = 10 : R = 1000 × 10^(-0.5) = 316.23
P = 20 : R = 1000 × 20^(-0.5) = 223.61
P = 5  : R = 1000 × 5^(-0.5) = 447.21
P = 3  : R = 1000 × 3^(-0.5) = 577.35
P = 2  : R = 1000 × 2^(-0.5) = 707.11
P = 1  : R = 1000 × 1^(-0.5) = 1000.00

Maximum : P ≈ 2.5, R ≈ 632.46
```

---

## 6. Équations Différentielles

### **Exemple : Modèle de Croissance Clientèle**

**Équation différentielle :**
```
dC/dt = r × C × (K - C)/K  (modèle logistique)
```

Où :
- C(t) = nombre clients à l'instant t
- r = taux de croissance (0.15/mois)
- K = capacité maximale (10,000 clients)

**Solution analytique :**
```
C(t) = K / (1 + ((K-C₀)/C₀) × e^(-r t))
```

**Avec C₀ = 1,000 clients initiaux :**
```
C(t) = 10,000 / (1 + 9 × e^(-0.15 t))
```

**Prévisions :**
```
t=0  : C=1,000 (état initial)
t=12 : C=1,000 / (1 + 9×e^(-1.8)) ≈ 1,850 clients
t=24 : C=1,000 / (1 + 9×e^(-3.6)) ≈ 3,200 clients
t=36 : C=1,000 / (1 + 9×e^(-5.4)) ≈ 5,200 clients
t=60 : C=1,000 / (1 + 9×e^(-9.0)) ≈ 9,100 clients (proche saturation)
```

---

## 7. Transformées de Fourier

### **Exemple : Analyse Saisonnalité Ventes**

**Série temporelle :** Ventes mensuelles sur 3 ans.

**Transformée de Fourier discrète :**
```
X[k] = Σ_{n=0}^{N-1} x[n] × e^(-j 2π k n / N)
```

**Fréquences détectées :**
```
Fréquence annuelle (k=12) : Amplitude = 45,200€
Fréquence trimestrielle (k=3) : Amplitude = 12,800€
Fréquence mensuelle (k=1) : Amplitude = 8,900€
```

**Décomposition :**
```
Ventes(t) = 125,000 + 45,200×cos(2π t /12) + 12,800×cos(2π t /3) + ...
```

---

## 8. Théorie de l'Information

### **Exemple : Compression de Données**

**Texte original :** "Le guide IA est excellent pour apprendre"
**Longueur :** 42 caractères

**Calcul entropie :**
```
Probabilités :
Espace : 3/42 ≈ 0.071
e : 6/42 ≈ 0.143
L : 1/42 ≈ 0.024
x : 1/42 ≈ 0.024
...etc

Entropie H = -Σ pᵢ log₂(pᵢ) ≈ 4.2 bits/symbole
```

**Compression LZ77 :**
- Taille compressée : 28 octets
- Taux compression : 33% réduction
- Efficacité : 1.33 bits/symbole moyen

---

## 9. Géométrie Algorithmique

### **Exemple : Clustering K-means**

**Données :** 100 clients avec âge et revenu.

**Algorithme K-means (K=3) :**
```
Itération 1 :
Centroïde 1 : âge=25, revenu=35k
Centroïde 2 : âge=45, revenu=65k
Centroïde 3 : âge=65, revenu=95k

Distance euclidienne pour point (30, 45k) :
d₁ = √((30-25)² + (45-35)²) = √(25 + 100) = √125 ≈ 11.2
d₂ = √((30-45)² + (45-65)²) = √(225 + 400) = √625 = 25
d₃ = √((30-65)² + (45-95)²) = √(1225 + 2500) = √3725 ≈ 61

Assignation : Cluster 1 (distance minimale)
```

**Convergence après 5 itérations :**
```
Inertie intra-cluster : 45,200
Silhouette score moyen : 0.72 (bon clustering)
```

---

## 10. Théorie des Jeux

### **Exemple : Stratégie Tarifaire Concurrentielle**

**Jeu à deux joueurs :** Deux entreprises fixent leurs prix.

**Matrice payoffs (profits en milliers €) :**
```
                    Prix Concurrent Bas    Prix Concurrent Élevé
Prix Entreprise Bas    (800, 800)            (1200, 600)
Prix Entreprise Élevé  (600, 1200)           (1000, 1000)
```

**Équilibre de Nash :** (Bas, Bas) → Profit 800k chacun
- Si entreprise A choisit Bas, entreprise B choisit Bas (800k > 600k)
- Si entreprise A choisit Élevé, entreprise B choisit Bas (1200k > 1000k)
- Donc équilibre : les deux choisissent Bas

**Stratégie dominante :** Prix Bas (meilleur choix indépendamment de l'adversaire)

---

## ⚠️ ATTENTION : Interprétation Contextuelle

### **Les mathématiques ne remplacent pas le jugement métier**

**Exemple problématique :**
```
Modèle parfait : R² = 0.97, p-value < 0.001
Mais : données d'entraînement = données de test !
Résultat : Overfitting non détecté, modèle inutilisable en production
```

**Leçon :** Les formules mathématiques sont des outils, pas des solutions magiques.

---

## 💡 CONSEIL : Approche Hybride

### **Mathématiques + Expertise Métier**

**Workflow recommandé :**
1. **Formulation mathématique** du problème
2. **Exploration algorithmique** des solutions
3. **Validation métier** des résultats
4. **Itération** basée sur feedback terrain

**Exemple concret :**
```
Problème : Optimiser prix produit
1. Math : Modèle économétrique demande-prix
2. Algo : Simulation Monte Carlo scénarios
3. Métier : Validation acceptabilité marché
4. Résultat : Prix optimal + stratégie go-to-market
```

---

## ✓ BONNES PRATIQUES : Mathématiques Appliquées

### **1. Validation Systématique**
```
□ Cohérence logique des équations
□ Sens physique des paramètres
□ Robustesse aux conditions limites
□ Validation croisée méthodes
```

### **2. Communication Accessible**
```
□ Traduction concepts mathématiques en langage métier
□ Visualisations pour expliquer résultats complexes
□ Scénarios "what-if" pour explorer sensibilité
□ Documentation complète raisonnements
```

### **3. Éthique et Transparence**
```
□ Explicabilité des modèles (XAI)
□ Tests de biais et discrimination
□ Communication incertitudes
□ Gouvernance utilisation résultats
```

### **4. Itération Continue**
```
□ Monitoring performance post-déploiement
□ Récalibration périodique modèles
□ Incorporation nouvelles données
□ Amélioration continue approche
```

---

## 🎯 CONCLUSION : Puissance des Mathématiques Appliquées

Ces exemples concrets démontrent comment les **concepts mathématiques abstraits** se transforment en **solutions business tangibles** :

- **Algèbre linéaire** → Systèmes de recommandation personnalisés
- **Probabilités** → Tests statistiques fiables pour décisions
- **Optimisation** → Allocation optimale des ressources
- **Théorie des graphes** → Analyse de réseaux d'influence
- **Calcul différentiel** → Optimisation de prix et coûts

**La clé du succès :** Maîtrise technique + créativité appliquée + rigueur méthodologique.