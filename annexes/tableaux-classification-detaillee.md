# 📊 Annexe D : Tableaux de Classification Détaillée

## 1. Classification des Algorithmes ML

### **Par Type de Problème**

| **Problème** | **Algorithmes Recommandés** | **Complexité** | **Avantages** | **Limites** | **Cas d'Usage** |
|--------------|-----------------------------|----------------|---------------|-------------|-----------------|
| **Classification Binaire** | Régression logistique, SVM, Random Forest | Faible à Moyenne | Interprétable, rapide | Non adapté données complexes | Prédiction churn, détection spam |
| **Classification Multi-classes** | Random Forest, XGBoost, Neural Networks | Moyenne à Élevée | Flexible, performant | Complexité calcul | Reconnaissance image, NLP |
| **Classification Déséquilibrée** | SVM pondéré, Random Forest balancé, SMOTE | Moyenne | Gère imbalance, robuste | Paramétrage délicat | Détection fraude, diagnostic médical |
| **Classification Haute Dimension** | SVM avec noyau, PCA+SVM, Neural Networks | Élevée | Efficace grande dimension | Risque overfitting | Génomique, traitement signal |

### **Par Volume de Données**

| **Taille Dataset** | **Algorithmes Adaptés** | **Ressources Requises** | **Temps Entraînement** | **Exemples** |
|-------------------|-------------------------|------------------------|----------------------|-------------|
| **Petit (< 1k)** | KNN, Naive Bayes, Régression logistique | CPU basique | < 1 minute | Études pilotes, prototypes |
| **Moyen (1k - 100k)** | Random Forest, SVM, Gradient Boosting | CPU/GPU moyen | Minutes à heures | Applications business standards |
| **Grand (100k - 1M)** | XGBoost, LightGBM, Neural Networks | GPU recommandé | Heures | Big data, deep learning |
| **Très Grand (> 1M)** | Neural Networks distribués, Online Learning | Cluster GPU | Jours | Internet scale, temps réel |

### **Par Exigence d'Interprétabilité**

| **Niveau Interprétabilité** | **Algorithmes** | **Transparence** | **Explicabilité** | **Domaines** |
|-----------------------------|-----------------|------------------|-------------------|-------------|
| **Très Haute** | Régression linéaire/logistique, Decision Trees | Formules mathématiques | Coefficients directs | Réglementé, médical |
| **Haute** | Random Forest, GBM | Importance features | Partial dependence | Finance, assurance |
| **Moyenne** | SVM, Neural Networks simples | Frontière décision | LIME/SHAP | Marketing, retail |
| **Faible** | Deep Neural Networks, Transformers | Boîte noire | Approximations | Recherche, exploration |

---

## 2. Classification des Modèles de Séries Temporelles

### **Par Horizon de Prévision**

| **Horizon** | **Modèles Adaptés** | **Précision Attendue** | **Fréquence Mise à Jour** | **Exemples** |
|-------------|---------------------|----------------------|-------------------------|-------------|
| **Très court (heures)** | SES, ARIMA simple | MAPE < 5% | Continue | Trafic routier, énergie |
| **Court (jours)** | ARIMA, Holt-Winters | MAPE 5-15% | Quotidienne | Ventes retail, météo |
| **Moyen (semaines)** | SARIMA, Prophet | MAPE 10-25% | Hebdomadaire | Planification production |
| **Long (mois/années)** | Tendances + scénarios | MAPE 20-50% | Mensuelle | Stratégie business, démographie |

### **Par Type de Saisonnalité**

| **Pattern Saisonnier** | **Modèles Recommandés** | **Paramètres Clés** | **Exemples** |
|------------------------|-------------------------|-------------------|-------------|
| **Aucune** | ARIMA(p,d,q) | p,d,q optimaux | Prix actions, températures |
| **Régulière (mensuelle)** | SARIMA(p,d,q)(P,D,Q)[12] | P=1, Q=1 | Ventes retail, consommation |
| **Complexe (multiple)** | Prophet, Neural Networks | Composantes multiples | Énergie, transport aérien |
| **Changeante** | Online learning, Adaptative | Mise à jour continue | Mode, technologie |

### **Par Stabilité des Données**

| **Stabilité** | **Modèles** | **Avantages** | **Précautions** | **Monitoring** |
|---------------|-------------|---------------|-----------------|---------------|
| **Très stable** | ARIMA classique | Précis, rapide | Drift détecté tard | Mensuel |
| **Modérément stable** | Holt-Winters | Gère tendance + saison | Changements brusques | Hebdomadaire |
| **Variable** | Prophet, LSTM | Flexible, robuste | Overfitting | Quotidien |
| **Très volatile** | Ensemble methods, Online learning | Adaptatif, robuste | Complexité calcul | Temps réel |

---

## 3. Classification des Techniques de Feature Engineering

### **Par Type de Données**

| **Type Données** | **Techniques Applicables** | **Outils Python** | **Complexité** | **Impact** |
|------------------|----------------------------|------------------|----------------|-----------|
| **Numériques continues** | Standardisation, transformation log, binning | StandardScaler, PowerTransformer | Faible | ++ |
| **Numériques discrètes** | Encodage ordinal, regroupement | OrdinalEncoder, KBinsDiscretizer | Moyenne | + |
| **Catégorielles nominales** | One-hot, target encoding, frequency encoding | OneHotEncoder, TargetEncoder | Moyenne | +++ |
| **Texte** | TF-IDF, embeddings, n-grams | TfidfVectorizer, Word2Vec | Élevée | +++ |
| **Dates** | Extraction features (jour, mois, saison), lags | DateTime features, Lag features | Faible | ++ |
| **Images** | CNN features, transfer learning | ResNet, VGG | Très élevée | ++++ |
| **Séquences** | RNN, attention mechanisms | LSTM, Transformer | Très élevée | ++++ |

### **Par Objectif de Transformation**

| **Objectif** | **Techniques** | **Quand utiliser** | **Métriques** |
|--------------|----------------|-------------------|---------------|
| **Réduction dimension** | PCA, ICA, t-SNE | Visualisation, compression | Variance expliquée |
| **Sélection features** | RFE, LASSO, importance features | Performance, interprétabilité | Accuracy, stabilité |
| **Création features** | Polynomiale, interactions, domain knowledge | Performance boost | Lift, AUC gain |
| **Nettoyage** | Imputation, outliers, scaling | Qualité données | Data quality score |
| **Encodage** | Label, one-hot, embedding | Algorithmes ML | Performance modèle |

### **Par Ressources Disponibles**

| **Ressources** | **Techniques Simples** | **Techniques Avancées** | **Recommandation** |
|----------------|----------------------|-----------------------|------------------|
| **Temps limité** | Imputation moyenne, standardisation | Feature selection automatique | Prioriser essentiel |
| **Expertise limitée** | AutoML, templates préconçus | Domain expertise manuelle | Commencer simple |
| **Données limitées** | Feature engineering basique | Deep learning (risque overfitting) | Méthodes traditionnelles |
| **Ressources abondantes** | Ensemble complet techniques | Optimisation hyperparamètres | Exploration complète |

---

## 4. Classification des Métriques d'Évaluation

### **Pour Classification**

| **Aspect Évalué** | **Métriques** | **Interprétation** | **Quand privilégier** |
|------------------|---------------|-------------------|----------------------|
| **Performance globale** | Accuracy, Balanced Accuracy | % bonnes prédictions | Classes équilibrées |
| **Précision prédiction** | Precision, Recall, F1-Score | Qualité prédictions positives | Coûts erreurs différents |
| **Calibration** | Brier Score, Calibration curves | Fiabilité probabilités | Décisions basées seuils |
| **Discrimination** | AUC-ROC, Precision@K | Séparation classes | Ranking important |
| **Robustesse** | Cross-validation scores, confidence intervals | Stabilité modèle | Production critical |

### **Pour Régression**

| **Aspect Évalué** | **Métriques** | **Interprétation** | **Quand privilégier** |
|------------------|---------------|-------------------|----------------------|
| **Erreur absolue** | MAE, MedAE | Erreur moyenne absolue | Outliers impact faible |
| **Erreur quadratique** | MSE, RMSE | Pénalise gros écarts | Outliers problématiques |
| **Erreur relative** | MAPE, sMAPE | % erreur relative | Comparaison échelles |
| **R² et ajusté** | R², Adjusted R² | Variance expliquée | Comparaison modèles |
| **Robustesse** | Quantiles erreurs, max error | Performance worst-case | Applications critiques |

### **Pour Séries Temporelles**

| **Aspect Évalué** | **Métriques** | **Interprétation** | **Horizon** |
|------------------|---------------|-------------------|-------------|
| **Précision globale** | MAE, RMSE, MAPE | Erreur moyenne | Tous horizons |
| **Précision direction** | % bonnes directions | Prédit hausse/baisse | Court terme |
| **Stabilité** | Variance erreurs | Fiabilité prévisions | Tous horizons |
| **Robustesse** | Erreurs extrêmes, outliers | Performance stress | Long terme |

---

## 5. Classification des Outils et Frameworks

### **Par Niveau d'Expertise**

| **Niveau** | **Outils Recommandés** | **Courbe Apprentissage** | **Productivité** | **Cas d'Usage** |
|------------|----------------------|-------------------------|------------------|---------------|
| **Débutant** | AutoML (DataRobot, H2O), Streamlit | Faible | Élevée | Prototypes rapides |
| **Intermédiaire** | scikit-learn, caret, mlr | Moyenne | Bonne | Applications standards |
| **Avancé** | TensorFlow, PyTorch, Keras | Élevée | Excellente | Recherche, production |
| **Expert** | JAX, MXNet, frameworks spécialisés | Très élevée | Maximale | Innovation cutting-edge |

### **Par Taille de Projet**

| **Échelle** | **Stack Technologique** | **Infrastructure** | **Outils DevOps** | **Coût** |
|-------------|----------------------|-------------------|-------------------|---------|
| **Petit projet** | Python + scikit-learn | Local/machine personnelle | Git + scripts | Faible |
| **Moyen projet** | Python + frameworks ML | Serveur dédié/cloud | Docker + CI/CD | Moyen |
| **Grand projet** | Distributed ML (Spark, Dask) | Cluster cloud | Kubernetes + MLOps | Élevé |
| **Enterprise** | Plateformes intégrées (SageMaker, Vertex AI) | Multi-cloud hybrid | Full MLOps stack | Très élevé |

### **Par Type d'Application**

| **Application** | **Frameworks Spécialisés** | **Bibliothèques Clés** | **Considérations** |
|----------------|---------------------------|----------------------|-------------------|
| **Computer Vision** | PyTorch Vision, TensorFlow Hub | OpenCV, Pillow | GPU essentiel |
| **NLP** | Transformers, spaCy | Hugging Face, NLTK | Modèles pré-entraînés |
| **Time Series** | Prophet, tsfresh | statsmodels, sktime | Saisonnalité, outliers |
| **Recommandation** | Surprise, LightFM | implicit, annoy | Scalabilité, cold start |
| **Anomaly Detection** | PyOD, Alibi Detect | scikit-learn, tensorflow | False positives |
| **Reinforcement Learning** | Stable Baselines, Ray RLlib | OpenAI Gym, PettingZoo | Environnements complexes |

---

## 6. Classification des Problèmes Business

### **Par Secteur d'Activité**

| **Secteur** | **Problèmes ML Courants** | **Données Typiques** | **Métriques Clés** | **Challenges** |
|-------------|--------------------------|---------------------|-------------------|---------------|
| **Finance** | Scoring crédit, détection fraude, trading | Transactions, historiques | AUC, precision@recall | Régulation, confidentialité |
| **Santé** | Diagnostic, prédiction, personnalisation | Médical, génomique | Sensitivity, specificity | Éthique, biais |
| **Retail** | Recommandation, pricing, inventaire | Transactions, comportement | Revenue lift, conversion | Saisonnalité, concurrence |
| **Industrie** | Maintenance prédictive, qualité, optimisation | IoT, capteurs | Downtime réduit, yield | Données bruitées, edge computing |
| **Tech/Media** | Recommandation contenu, détection spam, NLP | Logs utilisateur, texte | Engagement, accuracy | Scale, temps réel |

### **Par Fonction Métier**

| **Fonction** | **Use Cases ML** | **Données Disponibles** | **Impact Business** | **Rapidité Implémentation** |
|--------------|------------------|------------------------|-------------------|---------------------------|
| **Marketing** | Segmentation, churn prediction, campagnes | CRM, comportement web | CAC réduit, LTV augmenté | Moyenne |
| **Ventes** | Lead scoring, pricing dynamique, forecast | Historique ventes, marché | Revenue +20%, forecast accuracy | Rapide |
| **RH** | Recrutement, turnover prediction, formation | Données employé, performance | Coûts recrutements -30% | Moyenne |
| **Supply Chain** | Demand forecasting, optimisation stocks | Transactions, inventaire | Stockouts -50%, coûts -25% | Moyenne-lente |
| **Customer Service** | Chatbots, routing tickets, satisfaction | Tickets, feedbacks | Résolution +40%, satisfaction +25% | Rapide |

### **Par Maturité Digitale**

| **Maturité** | **Niveau ML Approprié** | **Infrastructure Requise** | **ROI Attendu** | **Timeline** |
|--------------|------------------------|---------------------------|----------------|-------------|
| **Débutant** | Automatisation règles métier, reporting | Cloud basic, BI tools | 50-100% | 3-6 mois |
| **Intermédiaire** | ML supervisé standard, analytics prédictive | Data warehouse, ML platform | 100-200% | 6-12 mois |
| **Avancé** | Deep learning, optimisation complexe | MLOps, AI platform | 200-500% | 12-24 mois |
| **Leader** | AI stratégique, innovation produit | AI research lab, partnerships | 500%+ | Continue |

---

## 7. Classification des Architectures ML

### **Par Pattern de Déploiement**

| **Pattern** | **Description** | **Avantages** | **Inconvénients** | **Cas d'Usage** |
|-------------|-----------------|---------------|------------------|---------------|
| **Batch** | Traitement périodique données | Simple, robuste | Latence élevée | Reporting, analytics |
| **Near Real-time** | Mise à jour fréquente (minutes) | Bon compromis | Complexité moyenne | Recommandation, scoring |
| **Real-time** | Prédiction instantanée | Ultra-réactif | Haute complexité | Fraude, trading |
| **Edge** | Exécution device local | Privacy, latence | Ressources limitées | IoT, mobile |
| **Federated** | Apprentissage distribué | Confidentialité | Coordination complexe | Santé, finance |

### **Par Modèle d'Exploitation**

| **Modèle** | **Caractéristiques** | **Coûts** | **Maintenance** | **Exemples** |
|------------|---------------------|-----------|-----------------|-------------|
| **SaaS ML** | Plateforme tierce, API | Abonnement | Minima | Startups, POC |
| **On-premise** | Infrastructure propre | Capex élevé | Expertise interne | Réglementé, sécurité |
| **Hybrid** | Core local, cloud extensions | Mixte | Moyenne | Enterprise transition |
| **Serverless** | Auto-scaling cloud | Usage-based | Faible | Variable workloads |
| **Open Source** | Libre, customisable | Coûts développement | Élevée | Innovation, contrôle |

### **Par Stratégie de Mise à Jour**

| **Stratégie** | **Fréquence** | **Déclencheurs** | **Avantages** | **Risques** |
|---------------|---------------|------------------|---------------|-------------|
| **Statique** | Jamais | - | Simple, stable | Obsolescence |
| **Périodique** | Quotidienne/mensuelle | Calendrier | Prévisible | Pas réactif |
| **Conditionnelle** | Métriques seuils | Performance drop | Adaptatif | Complexité |
| **Continue** | Temps réel | Nouvelles données | Optimal | Ressources élevées |
| **Hybride** | Mixte approches | Context-dependent | Flexible | Gestion complexe |

---

## 8. Classification des Risques et Challenges

### **Par Phase du Projet ML**

| **Phase** | **Risques Principaux** | **Prévention** | **Détection** | **Atténuation** |
|-----------|----------------------|----------------|---------------|----------------|
| **Problématisation** | Mauvaise définition problème | Workshops métier | Validation stakeholders | Redéfinition itérative |
| **Collecte données** | Données insuffisantes/biaisées | Audit qualité, diversité | Tests statistiques | Collecte complémentaire |
| **Préparation** | Feature engineering pauvre | Expertise domaine | Validation métier | Itération features |
| **Modélisation** | Overfitting, sélection modèle | Cross-validation, régularisation | Métriques validation | Ensemble methods |
| **Déploiement** | Drift conceptuel, scalabilité | Monitoring, tests A/B | Alertes automatiques | Rollback plans |
| **Maintenance** | Dégradation performance | Retraining automatique | KPIs monitoring | Mise à jour continue |

### **Par Type d'Impact Business**

| **Impact** | **Risques Associés** | **Niveau Critique** | **Monitoring Requis** | **Plans Continuité** |
|------------|---------------------|-------------------|----------------------|---------------------|
| **Financier direct** | Erreurs prédiction coûteuses | Très élevé | Temps réel, alertes | Backup models, seuils |
| **Opérationnel** | Interruptions service | Élevé | Health checks | Redondance, failover |
| **Réputationnel** | Prises décision erronées | Moyen | Feedback utilisateurs | Communication crise |
| **Légal/éthique** | Biais discriminatoires | Très élevé | Audits réguliers | Conformité, gouvernance |
| **Stratégique** | Mauvaises orientations | Élevé | Revue stratégique | Flexibilité, pivots |

### **Par Environnement Technique**

| **Environnement** | **Risques Spécifiques** | **Mesures Préventives** | **Outils Monitoring** | **Récupération** |
|------------------|------------------------|----------------------|----------------------|----------------|
| **Cloud public** | Coûts imprévus, sécurité | Budget alerts, encryption | CloudWatch, monitoring | Multi-region failover |
| **On-premise** | Ressources limitées, maintenance | Capacity planning | Nagios, Zabbix | Hardware redundancy |
| **Edge computing** | Connectivité, puissance | Offline capabilities | Local logging | Sync différée |
| **Hybride** | Cohérence données, latence | Data pipelines robustes | Distributed tracing | Consistency protocols |
| **Multi-cloud** | Vendor lock-in, complexité | Abstraction layers | Federation tools | Migration plans |

---

## ⚠️ ATTENTION : Classifications Non Exhaustives

### **Évolution Constante du Domaine**
Les classifications présentées sont **instantanés temporels** qui évoluent rapidement avec :
- Nouveaux algorithmes de recherche
- Avancées architecturales (neuromorphique, quantum)
- Changements réglementaires
- Évolution des besoins business

### **Adaptation Contextuelle Requise**
Aucune classification n'est universelle :
- **Secteur spécifique** peut nécessiter adaptations
- **Contraintes organisationnelles** influencent choix
- **Maturité technique** limite options
- **Objectifs business** guident priorités

---

## 💡 CONSEIL : Approche Pragmatique

### **Framework de Décision Multicritères**

1. **Définition contraintes** : Budget, délais, ressources, expertise
2. **Évaluation options** : Performance, complexité, maintenabilité
3. **Tests pilotes** : Proof of concept avant déploiement large
4. **Itération continue** : Apprentissage et amélioration permanents

### **Balance Risques/Bénéfices**
```
Choix optimal = max [Bénéfices - (Risques × Facteur_risque)]
```

Où facteur_risque dépend de :
- Tolérance organisation au risque
- Criticité de l'application
- Capacités de récupération

---

## ✓ BONNES PRATIQUES : Utilisation Classifications

### **1. Validation Continue**
```
□ Revue classifications selon évolutions technologiques
□ Benchmark contre meilleures pratiques sectorielles
□ Ajustement basé retours utilisateurs
□ Documentation évolutions et justifications
```

### **2. Personnalisation Contextuelle**
```
□ Adaptation classifications contraintes spécifiques
□ Considération maturité organisationnelle
□ Intégration exigences métier particulières
□ Équilibre complexité vs valeur ajoutée
```

### **3. Gouvernance et Traçabilité**
```
□ Documentation décisions prises
□ Justification choix selon classifications
□ Suivi performance post-déploiement
□ Revue périodique et ajustements
```

### **4. Formation et Partage**
```
□ Formation équipes aux classifications
□ Partage bonnes pratiques organisation
□ Création référentiels internes
□ Contribution communauté externe
```

---

## 🎯 CONCLUSION : Classifications comme Guides, non Dogmes

Ces tableaux de classification constituent des **frameworks de décision structurés** pour naviguer l'écosystème complexe de l'IA, mais doivent toujours être adaptés au **contexte spécifique** de chaque organisation et projet.

**La clé du succès :** Utiliser les classifications comme **points de départ éclairés**, pas comme règles absolues, en les combinant avec expertise métier et validation empirique.