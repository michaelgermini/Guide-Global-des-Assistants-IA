# 🔮 Templates pour les Modèles de Prévision

## 🟢 Template Débutant : Prévision Simple

```
Crée un modèle de prévision basique pour [MÉTRIQUE_PRÉDIRE] sur [HORIZON_TEMPORREL].

DONNÉES HISTORIQUES :
- Période disponible : [ANNÉES_MOIS_DONNÉES]
- Fréquence : [QUOTIDIENNE_HEBDOMADAIRE_MENSUELLE]
- Variables externes : [FACTEURS_INFLUENÇANT_PRÉVISION]

MÉTHODE PRÉVISIONNELLE :
- Approche : [MOYENNE_MOBILE_RÉGRESSION_LINÉAIRE]
- Justification : [SIMPLICITÉ_DONNÉES_DISPONIBLES]
- Outils : [EXCEL_SPREADSHEET_OUTILS_GRATUITS]

VALIDATION MODÈLE :
- Métriques : [MAE_RMSE_PRÉCISION_POURCENTAGE]
- Test période : [DERNIERS_MOIS_VALIDATION]
- Comparaison : [VS_VALEURS_RÉELLES_SIMPLICITÉ]

SORTIE PRÉVISIONNELLE :
- Graphique tendance : [VISUALISATION_ÉVOLUTION]
- Valeurs prédites : [CHIFFRES_PRÉVISIONS]
- Intervalle confiance : [PLAGE_INCERTITUDE]
```

## 🟡 Template Intermédiaire : Prévision Série Temporelle

```
Développe un modèle de prévision série temporelle pour [INDICATEUR_BUSINESS] avec [DONNÉES_SAISONNIÈRES].

CONTEXTE BUSINESS :
- Impact prévision : [DÉCISIONS_PRISES_ENJEUX_FINANCIERS]
- Horizon prédiction : [COURT_TERME_1-3_MOIS_MOYEN_TERME_3-12_MOIS]
- Fréquence mise à jour : [HEBDOMADAIRE_MENSUELLE_TRIMESTRIELLE]

ANALYSE EXPLORATOIRE :
COMPOSANTES SÉRIE :
- Tendance : [IDENTIFICATION_CROISSANCE_STAGNATION_DÉCLIN]
- Saisonnalité : [PATTERNS_QUOTIDIENS_HEBDOMADAIRES_ANNUELS]
- Cycle : [PERIODES_LONGS_ÉCONOMIQUES_PANDÉMIES]
- Bruit : [VARIABILITÉ_RÉSIDUELLE_ALÉATOIRE]

STATIONNARITÉ :
- Test ADF : [AUGMENTED_DICKEY_FULLER_P_VALUE]
- Différenciation : [DEGRÉ_NÉCESSAIRE_STATIONNARITÉ]
- Transformation : [LOG_RACINE_DIFFÉRENCES_SAISONNIÈRES]

CORRÉLATION AUTORÉGRESSIVE :
- ACF/PACF : [FONCTIONS_AUTOCORRÉLATION_ANALYSE]
- Ordres p,d,q : [PARAMÈTRES_ARIMA_IDENTIFIÉS]
- Saisonalité : [PARAMÈTRES_SAISONNIERS_P_D_Q_M]

MODÈLES CANDIDATS :
ARIMA CLASSIQUE :
- Configuration : [ARIMA(P,D,Q)(P,D,Q)[S]]
- AIC/BIC : [CRITÈRES_SÉLECTION_MODÈLE]
- Résidus : [TEST_BLANC_BRUIT_GAUCHEN]

SARIMA AVANCÉ :
- Composantes saisonnières : [PRISES_EN_COMPTE_CYCLES]
- Paramètres optimaux : [GRID_SEARCH_OPTIMISATION]
- Validation : [CROSS_VALIDATION_TEMPORRELLE]

MODÈLES EXPONENTIELS :
- Simple : [LISSAGE_EXPONENTIEL_ALPHA_OPTIMAL]
- Double : [TENDANCE_SAISONNALITÉ_BETA_GAMMA]
- Validation : [ERREUR_PRÉVISIONNELLE_MINIMISÉE]

ÉVALUATION PERFORMANCE :
MÉTRIQUES QUANTITATIVES :
- MAE (Mean Absolute Error) : [ERREUR_ABSOLUE_MOYENNE]
- RMSE (Root Mean Square Error) : [ERREUR_QUADRATIQUE_MOYENNE]
- MAPE (Mean Absolute Percentage Error) : [ERREUR_POURCENTAGE_MOYENNE]

VALIDATION VISUELLE :
- Graphiques ajustement : [COMPARAISON_PRÉDICTIONS_RÉEL]
- Analyse résidus : [NORMALITÉ_AUTOCORRÉLATION_HÉTÉROSCÉDASTICITÉ]
- Prévisions vs réalité : [ACCURACY_HORIZON_COURT_MOYEN]

IMPLÉMENTATION OPÉRATIONNELLE :
AUTOMATISATION :
- Pipeline données : [COLLECTE_NETTOYAGE_TRANSFORMATION]
- Entraînement modèle : [RÉENTRAÎNEMENT_PROGRAMMÉ]
- Déploiement prédictions : [API_DASHBOARD_INTÉGRATION]

MONITORING :
- Drift détection : [CHANGEMENTS_DISTRIBUTION_DONNÉES]
- Performance tracking : [DÉGRADATION_MÉTRIQUES_ALERTES]
- Réentraînement : [SEUILS_RETRAINING_AUTOMATISÉ]
```

## 🔴 Template Avancé : Prévision Multi-Variée Avancée

```
Construit un système de prévision multivarié pour [SYSTÈME_COMPLEXE] intégrant [VARIABLES_EXOGÈNES].

PROBLÉMATIQUE COMPLEXE :
- Variables endogènes : [SORTIES_PRINCIPALES_PRÉDIRE]
- Variables exogènes : [ENTRÉES_INFLUENÇANT_SYSTÈME]
- Relations causales : [DÉPENDANCES_CONNUES_HYPOTHÉTIQUES]
- Contraintes opérationnelles : [LIMITES_RÉELLES_SYSTÈME]

ARCHITECTURE PRÉVISIONNELLE :
APPROCHE HYBRIDE :
- Modèles statistiques : [ARIMAX_VECTOR_AUTOREGRESSION]
- Machine learning : [RANDOM_FOREST_GRADIENT_BOOSTING]
- Deep learning : [LSTM_TRANSFORMERS_POUR_SÉQUENCES]

INGÉNIERIE FEATURES :
TEMPORAL FEATURES :
- Lags endogènes : [VALEURS_PASSÉES_INFLUENÇANT]
- Lags exogènes : [VARIABLES_EXTERNES_DÉCALÉES]
- Rolling statistics : [MOYENNES_MÉDIANES_ÉCARTS_ROULANTS]
- Seasonal decomposition : [EXTRACTION_COMPOSANTES_SAISONNIÈRES]

DOMAIN FEATURES :
- Business rules : [CONNAISSANCES_MÉTIER_INTÉGRÉES]
- External data : [INDICATEURS_ÉCONOMIQUES_MÉTÉO_TENDANCES]
- Interaction terms : [EFFETS_COMBINÉS_VARIABLES]
- Categorical encoding : [TRANSFORMATION_VARIABLES_QUALITATIVES]

SÉLECTION FEATURES :
- Importance features : [PERMUTATION_IMPORTANCE_SHAP_VALUES]
- Correlation analysis : [MULTICOLLINÉARITÉ_VIF_ANALYSE]
- Dimensionality reduction : [PCA_FEATURE_SELECTION_LASSO]
- Domain expertise : [VALIDATION_MÉTIER_CRITIQUE]

ENSEMBLE MODELING :
VOTING ENSEMBLES :
- Modèles individuels : [DIFFÉRENTS_ALGORITHMES_COMPLÉMENTAIRES]
- Poids optimisation : [OPTIMISATION_BAYÉSIENNE_PONDÉRATIONS]
- Meta-learner : [MODÈLE_SUPÉRIEUR_COMBINAISON_PRÉDICTIONS]

STACKING AVANCÉ :
- Base models : [HÉTÉROGÉNÉITÉ_ALGORITHMES_ASSURÉE]
- Meta features : [PRÉDICTIONS_OUT_OF_FOLD_UTILISÉES]
- Cross-validation : [VALIDATION_ROBUSTE_PRÉVENTION_OVERFIT]

TIME SERIES ENSEMBLES :
- Multiple horizons : [PRÉVISIONS_COURT_MOYEN_LONG_TERMES]
- Model averaging : [MOYENNES_PONDÉRÉES_PRÉDICTIONS]
- Uncertainty quantification : [INTERVALLES_CONFIANCE_QUANTILES]

VALIDATION ROBUSTE :
CROSS-VALIDATION TEMPORELLE :
- Time series split : [RESPECT_ORDRE_TEMPORAL_VALIDATION]
- Rolling forecast : [SIMULATION_PRÉVISIONS_RÉELLES]
- Expanding window : [AUGMENTATION_PROGRESSIVE_TRAINING_SET]

BACKTESTING ÉCONOMIQUE :
- Trading simulation : [SIMULATION_DÉCISIONS_FINANCIÈRES]
- Cost-benefit analysis : [ANALYSE_ROI_PRÉVISIONS]
- Risk-adjusted metrics : [SHARPE_RATIO_MAX_DRAWDOWN]

SCÉNARIOS SENSIBILITÉ :
- Stress testing : [CHOCS_EXTREMES_RÉSISTANCE_MODÈLE]
- What-if analysis : [SCÉNARIOS_HYPOTHÉTIQUES_IMPACT]
- Monte Carlo simulation : [INCERTITUDE_STOCHASTIQUE_PROPAGATION]

DÉPLOIEMENT PRODUCTION :
MICROSERVICES ARCHITECTURE :
- Model serving : [FASTAPI_DOCKER_KUBERNETES]
- Feature store : [FEAST_TEMPO_FEATURES_CENTRALISÉES]
- Online learning : [ADAPTATION_CONTINUE_NOUVELLES_DONNÉES]

MLOPS PIPELINE :
- Data pipeline : [APACHE_AIRFLOW_KUBEFLOW_AUTOMATISATION]
- Model registry : [MLFLOW_DVC_VERSIONING_MODÈLES]
- Monitoring : [EVIDENTLY_WHYSKER_DRIFT_DÉTECTION]
- CI/CD : [GITHUB_ACTIONS_AUTOMATISATION_DÉPLOIEMENT]

PERFORMANCE MONITORING :
BUSINESS METRICS :
- Forecast accuracy : [WAPE_MAPE_PINBALL_LOSS]
- Business impact : [REVENUE_IMPROVEMENT_COST_SAVINGS]
- User satisfaction : [ADOPTION_RATE_FEEDBACK_QUALITY]

TECHNICAL METRICS :
- Latency : [<100MS_PRÉDICTIONS_EN_LIGNE]
- Throughput : [1000+_REQUÊTES/SECONDE]
- Reliability : [99.9%_UPTIME_DISPONIBILITÉ]
```

## 🚀 Template Expert : Prévision Incertaine et Probabiliste

```
Développe un système de prévision probabiliste pour [DÉCISION_CRITIQUE] sous incertitude élevée.

CONTEXTE INCERTITUDE :
- Sources variabilité : [ÉCONOMIQUES_GÉOPOLITIQUES_CLIMATIQUES_TENDANCES]
- Impact décisions : [COÛTS_OPPORTUNITÉS_RISQUES_ASSOCIÉS]
- Horizon temporel : [STRATÉGIQUE_3-5_ANS_TACTIQUE_6-18_MOIS]
- Niveau confiance requis : [95%_99%_INTERVALLES_PRÉDICTIONS]

MÉTHODOLOGIE PROBABILISTE :
ENSEMBLES BAYÉSIENS :
- Prior distributions : [CONNAISSANCES_APRIORI_EXPERTS]
- Likelihood functions : [MODÉLISATION_VEROSSIMILITUDE_DONNÉES]
- Posterior sampling : [MCMC_HAMILTONIAN_MONTE_CARLO]
- Predictive distributions : [INCERTITUDE_PROPAGATION_QUANTIFIÉE]

QUANTILES ET SCÉNARIOS :
- Value at Risk : [VaR_95%_PERTES_MAXIMALES_ATTENDUES]
- Expected Shortfall : [ES_95%_PERTES_CONDITIONNELLES_MOYENNES]
- Scenario analysis : [BEST_WORST_BASE_CASES_DÉFINIS]
- Stress testing : [CHOCS_HISTORIQUES_SIMULÉS_IMPACT]

PROPAGATION INCERTITUDE :
MONTE CARLO SIMULATIONS :
- Input distributions : [PARAMÈTRES_STOCHASTIQUES_MODÉLISÉS]
- Dependency modeling : [COPULES_CORRÉLATIONS_COMPLEXES]
- Output distributions : [RÉPARTITIONS_PRÉDICTIONS_FINALES]
- Sensitivity analysis : [ANALYSE_INFLUENCE_PARAMÈTRES]

BAYESIAN NETWORKS :
- Causal relationships : [GRAPHE_CAUSAL_EXPERTS_DOMAINES]
- Conditional probabilities : [TABLES_CPT_APPRISES_DONNÉES]
- Evidence propagation : [MISE_À_JOUR_CROYANCES_NOUVELLES_DONNÉES]
- Decision optimization : [MAXIMISATION_UTILITÉ_ATTENDUE]

GESTION RISQUE AVANCÉ :
RISK BUDGETING :
- Risk allocation : [BUDGET_RISQUE_PAR_SOURCE_INCERTITUDE]
- Diversification : [RÉDUCTION_CORRÉLATIONS_RISQUES]
- Hedging strategies : [Couverture_OPTIMISÉE_INSTRUMENTS_FINANCIERS]
- Rebalancing : [AJUSTEMENTS_DYNAMIQUES_ALLOCATION]

ROBUST OPTIMIZATION :
- Min-max strategies : [OPTIMISATION_PIRE_SCÉNARIO_GARANTI]
- Ambiguity sets : [ENSEMBLES_INCERTITUDES_CONSIDÉRÉS]
- Adjustable policies : [DÉCISIONS_ADAPTATIVES_NOUVELLES_INFORMATIONS]
- Regret minimization : [MINIMISATION_REGRETS_COMPARÉS_OPTIMAL_THÉORIQUE]

COMMUNICATION INCERTITUDE :
VISUALISATION PROBABILISTÉ :
- Fan charts : [PRÉVISIONS_INTERVALLES_CONFIANCE_ÉVOLUTION]
- Probability density plots : [DISTRIBUTIONS_PROBABILITÉS_COMPLETES]
- Scenario fans : [MULTIPLES_TRAJECTOIRES_POSSIBLES]
- Tornado diagrams : [ANALYSE_SENSIBILITÉ_PARAMÈTRES_INFLUENTS]

INTERPRÉTATION DÉCISIONNELLE :
- Expected value : [VALEUR_ATTENDUE_SCÉNARIOS_PONDÉRÉS]
- Risk-adjusted returns : [RENDEMENTS_AJUSTÉS_VOLATILITÉ]
- Decision trees : [ARBRES_DÉCISIONS_PROBABILISTES_OPTIMISÉS]
- Real options valuation : [VALORISATION_FLEXIBILITÉ_DÉCISIONS_FUTURES]

OUTILS ET INFRASTRUCTURE :
PLATEFORMES PROBABILISTES :
- Stan/PyMC3 : [INFÉRENCE_BAYÉSIENNE_AVANCÉE]
- RiskMetrics : [ANALYSE_RISQUE_FINANCIER_PROFESSIONNEL]
- Crystal Ball : [SIMULATIONS_MONTE_CARLO_SPREADSHEET]
- @RISK : [GESTION_RISQUE_QUANTITATIVE_INTEGRÉE]

ARCHITECTURE SYSTÈME :
- Event sourcing : [TRACE_COMPLÈTE_DÉCISIONS_HISTORIQUE]
- CQRS pattern : [SÉPARATION_LECTURE_ÉCRITURE_OPTIMISATION]
- Saga orchestration : [COORDINATION_TRANSACTIONS_DISTRIBUÉES]
- Domain-driven design : [MODÉLISATION_MÉTIER_ROBUSTE]

VALIDATION ET AUDIT :
STRESS TESTING :
- Historical scenarios : [CRISES_PASSÉES_SIMULÉES_IMPACT]
- Hypothetical shocks : [SCÉNARIOS_EXTRÊMES_ÉVALUÉS_RÉSISTANCE]
- Reverse stress testing : [CONDITIONS_BREAKING_POINT_SYSTÈME]

MODEL RISK MANAGEMENT :
- Model validation : [VALIDATION_INDÉPENDANTE_EXPERTS_QUANT]
- Backtesting : [VALIDATION_RÉTROSPECTIVE_PERFORMANCE]
- Benchmarking : [COMPARAISON_MODÈLES_ALTERNATIFS]
- Governance : [COMITÉ_MODÈLE_APPROBATION_CHANGEMENTS]

INTÉGRATION DÉCISIONNELLE :
DÉCISION UNDER UNCERTAINTY :
- Utility theory : [THÉORIE_UTILITÉ_PRÉFÉRENCES_DÉCISIONNEL]
- Prospect theory : [COMPORTEMENT_DÉCISIONNEL_RÉEL_INTÉGRÉ]
- Multi-attribute utility : [DÉCISIONS_MULTICRITÈRES_COMPLEXES]
- Real-time adaptation : [MISE_À_JOUR_DÉCISIONS_NOUVELLES_INFORMATIONS]
```

## 🎯 Templates Spécialisés par Domaine

### Template Prévision Demande Commerciale

```
Développe un modèle de prévision demande pour [PRODUIT_SERVICE] avec [DONNÉES_VENTES_HISTORIQUES].

DONNÉES DISPONIBLES :
- Historique ventes : [ANNÉES_DISPONIBLES_GRANULARITÉ]
- Variables explicatives : [PRIX_CONCURRENTIEL_MÉTÉO_ÉVÉNEMENTS]
- Données externes : [PIB_TENDANCES_GOOGLE_TRENDS]

MÉTHODOLOGIE PRÉVISIONNELLE :
ANALYSE PATTERNS :
- Saisonnalité : [PIC_NOUEL_FÊTES_ÉTÉ_RENTREE]
- Tendance : [CROISSANCE_STAGNATION_DÉCLIN_MARCHÉ]
- Cycles économiques : [CORRÉLATION_PIB_CONJONCTURE]
- Effets promotionnels : [IMPACT_PUBLICITÉ_PRIX_PROMOTIONNELS]

MODÈLE CAUSAL :
- Variables indépendantes : [PRIX_PUBLICITÉ_CONCURRENCE_SAISONNALITÉ]
- Spécification : [LOG_LINÉAIRE_POLYNOMIALE_SEUILS]
- Tests causalité : [GRANGER_CAUSALITY_ANALYSE]
- Robustesse : [TESTS_HÉTÉROSCÉDASTICITÉ_MULTICOLLINÉARITÉ]

MODÈLE MACHINE LEARNING :
ALGORITHMES CANDIDATS :
- Random Forest : [GESTION_NON-LINÉARITÉ_INTERACTIONS_COMPLEXES]
- Gradient Boosting : [PERFORMANCE_OPTIMALE_DONNÉES_HÉTÉROGÈNES]
- Neural Networks : [CAPTURE_PATTERNS_COMPLEXES_AUTOMATIQUEMENT]

FEATURE ENGINEERING :
- Time-based : [JOUR_SEMAINE_MOIS_SAISON_ENCOURS]
- Lag features : [VENTES_PRÉCÉDENTES_1_2_3_4_SEMAINES]
- Rolling statistics : [MOYENNES_ÉCARTS_DERNIERS_4_SEMAINES]
- External factors : [TEMPÉRATURE_PRÉCIPITATIONS_ÉVÉNEMENTS_LOCAUX]

VALIDATION BUSINESS :
MÉTRIQUES COMMERCIALES :
- Forecast accuracy : [WAPE_PONDÉRÉ_VOLUMES_VENTES]
- Service level : [TAUX_SATISFACTION_LIVRAISON_DISPONIBILITÉ]
- Inventory turnover : [OPTIMISATION_STOCKS_ROTATION]
- Lost sales : [VENTES_PERDUES_ROUPTURE_STOCK_ESTIMÉES]

IMPACTS OPÉRATIONNELS :
- Production planning : [AJUSTEMENT_CHAÎNES_APPROVISIONNEMENT]
- Inventory optimization : [RÉDUCTION_STOCKS_EXCÉDENTAIRES]
- Cash flow improvement : [PRÉVISIONS_TRÉSORERIE_OPTIMISÉES]
- Supplier relations : [COMMANDES_FOURNISSEURS_ANTICIPÉES]

IMPLÉMENTATION OPÉRATIONNELLE :
OUTILS INTÉGRATION :
- ERP connection : [SAP_ORACLE_INTEGRATION_AUTOMATISÉE]
- BI dashboards : [TABLEAU_LOOKER_METRICS_RÉEL_TIME]
- Alert system : [NOTIFICATIONS_DÉPASSEMENTS_SEUILS]
- User training : [FORMATION_MANAGERS_UTILISATION_PRÉVISIONS]

MAINTENANCE MODÈLE :
- Monthly updates : [RÉENTRAÎNEMENT_DONNÉES_FRAÎCHES]
- Performance monitoring : [DÉGRADATION_ACCURACY_ALERTES]
- Model comparison : [BENCHMARKING_NOUVELLES_APPROCHES]
- User feedback : [AMÉLIORATION_CONTINUE_RETROUURS_UTILISATEURS]
```

### Template Prévision Économique Macro

```
Construit un modèle de prévision économique pour [INDICATEUR_MACRO] intégrant [VARIABLES_ÉCONOMIQUES].

CONTEXTE ÉCONOMIQUE :
- Indicateur cible : [PIB_INFLATION_CHÔMAGE_TAUX_INTÉRÊT]
- Horizon prévisionnel : [TRIMESTRIEL_SEMESTRIEL_ANNUEL]
- Utilisation : [POLITIQUE_MONÉTAIRE_PLANIFICATION_STRATÉGIQUE]
- Niveau précision requis : [BANQUE_CENTRALE_INSTITUTION_FINANCIÈRE]

DONNÉES ÉCONOMIQUES :
SOURCES OFFICIELLES :
- Indicateurs macro : [INSEE_STATISTIQUES_BCE_FMI]
- Enquêtes entreprises : [CLIMAT_AFFAIRES_SENTIMENT_CONSO]
- Marchés financiers : [TAUX_CHANGE_ACTIONS_OBLIGATIONS]
- Données internationales : [FMI_OCDE_BANQUE_MONDIALE]

FRÉQUENCE ET HISTORIQUE :
- Données mensuelles : [3-5_ANNÉES_HISTORIQUE_DISPONIBLE]
- Données trimestrielles : [10-20_ANNÉES_SÉRIES_LONGUES]
- Données annuelles : [30+_ANNÉES_TENDANCES_LONG_TERME]
- Indicateurs avancés : [LEADING_INDICATORS_DISPONIBLES]

MÉTHODOLOGIE ÉCONOMÉTRIQUE :
MODÈLES VECTORIELS :
- VAR models : [VECTOR_AUTOREGRESSION_RELATIONS_MUTUELLES]
- SVAR : [IDENTIFICATION_CHOCS_STRUCTURELS]
- BVAR : [INCORPORATION_PRIORS_BAYÉSIENS]
- FAVAR : [FACTORS_AUGMENTED_GRANDES_DIMENSIONS]

MODÈLES DSGE :
- Calibration modèle : [PARAMÈTRES_ÉCONOMIQUES_ESTIMÉS]
- Simulation scenarios : [POLITIQUES_FISCALES_MONÉTAIRES]
- Stress testing : [RÉSISTANCE_CHOCS_ÉCONOMIQUES]
- Forecasting : [PRÉVISIONS_CONDITIONNELLES_SCÉNARIOS]

MACHINE LEARNING ÉCONOMIQUE :
ENSEMBLE METHODS :
- Gradient boosting : [NON-LINÉARITÉ_CAPTURE_PATTERNS_COMPLEXES]
- Neural networks : [LSTM_POUR_SÉQUENCES_ÉCONOMIQUES]
- Random forests : [GESTION_HÉTÉROGÉNÉITÉ_DONNÉES]

FEATURE SELECTION :
- Economic theory : [VARIABLES_THÉORIQUES_PRIORISÉES]
- Data-driven : [IMPORTANCE_FEATURES_AUTOMATISÉE]
- Regularization : [LASSO_POUR_SÉLECTION_SPARSE]
- Domain expertise : [VALIDATION_ÉCONOMISTES_INTÉGRÉE]

VALIDATION ROBUSTE :
OUT-OF-SAMPLE TESTING :
- Rolling forecast : [PRÉVISIONS_RÉCURSIVES_ÉVOLUTION]
- Fixed window : [STABILITÉ_PERFORMANCE_TEMPORISÉE]
- Real-time evaluation : [COMPARAISON_CONSENSUS_MARCHÉ]

DIEBOLD-MARIANO TEST :
- Comparaison forecasts : [TESTS_STATISTIQUES_SUPÉRIORITÉ]
- Multiple horizons : [ÉVALUATION_DIFFÉRENTS_ÉCHÉANCIERS]
- Economic value : [UTILITÉ_PRATIQUE_PRÉVISIONS]

COMMUNICATION INSTITUTIONNELLE :
PRÉSENTATION BANQUE CENTRALE :
- Probabilité distributions : [INCERTITUDE_COMMUNICATION_TRANSPARENTE]
- Scenario analysis : [ALTERNATIVES_POSSIBLES_EXPLIQUÉES]
- Risk assessment : [VULNÉRABILITÉS_SYSTÈME_HIGHLIGHTED]
- Policy implications : [RECOMMANDATIONS_DÉCISIONNELLES_CLAIRES]

RAPPORTS TECHNIQUES :
- Méthodologie détaillée : [SPÉCIFICATIONS_MODÈLES_TRANSPARENTS]
- Data sources : [ORIGINES_DONNÉES_DOCUMENTÉES]
- Model properties : [PROPRIÉTÉS_STATISTIQUES_COMMUNIQUÉES]
- Forecast evaluation : [VALIDATION_RIGOUREUSE_PUBLIÉE]

IMPACT POLITIQUE :
DÉCISIONS INSTITUTIONNELLES :
- Taux directeurs : [IMPACT_PRÉVISIONS_INFLATION_DÉCISIONS]
- Quantitative easing : [ÉVALUATION_BESOINS_LIQUIDITÉ_MARCHÉS]
- Regulatory changes : [ANTICIPATION_IMPACT_RÉGLEMENTATIONS]
- Crisis management : [OUTILS_PRÉVENTION_GESTION_CRISIS]

TRANSPARENCE DÉMOCRATIQUE :
- Public communication : [EXPLICATION_CHOIX_POLITIQUES_CITOYENS]
- Accountability : [TRACE_DÉCISIONS_IMPACT_MESURÉ]
- Stakeholder engagement : [CONSULTATION_ACTEURS_ÉCONOMIQUES]
- Education économique : [PÉDAGOGIE_COMPLEXITÉ_CHOIX]
```

### Template Prévision Météorologique Opérationnelle

```
Développe un système de prévision météorologique opérationnelle pour [APPLICATION_CRITIQUE] avec [EXIGENCE_PRÉCISION].

APPLICATION UTILISATRICE :
- Secteur impacté : [AGRICULTURE_TRANSPORT_ENERGIE_TOURISME]
- Décisions dépendantes : [PLANIFICATION_JOURNALIÈRE_OPÉRATIONNELLE]
- Coûts erreurs : [IMPACT_FINANCIER_MÉTÉO_ERRONÉE_CHIFFRÉ]
- Horizon prédiction : [MAINTENANT_+24H_+72H_+7_JOURS]

DONNÉES MÉTÉOROLOGIQUES :
SOURCES DONNÉES :
- Observations sol : [STATIONS_MÉTÉO_DENSITÉ_RÉGIONALE]
- Radars précipitations : [COUVERTURE_SPATIALE_RÉSOLUTION]
- Satellites : [IMAGERIE_VISIBLE_INFRAOUGE_CANAUX_SPÉCIAUX]
- Modèles numériques : [GFS_ECMWF_ARPEGE_RÉSOLUTIONS]

ASSIMILATION DONNÉES :
- Data fusion : [COMBINAISON_SOURCES_HÉTÉROGÈNES]
- Quality control : [DÉTECTION_ERREURS_AUTOMATISÉE]
- Bias correction : [AJUSTEMENT_SYSTÉMATIQUE_ERREURS]
- Spatial interpolation : [ESTIMATION_POINTS_NON_MESURÉS]

MODÈLES PRÉVISIONNELS :
ENSEMBLE FORECASTING :
- Multi-model approach : [COMBINAISON_DIFFÉRENTS_MODÈLES]
- Perturbed physics : [INTRODUCTION_VARIABILITÉ_PHYSIQUE]
- Stochastic parameterizations : [INCERTITUDE_PARAMÈTRES_SUB-GRID]
- Post-processing : [CALIBRATION_AMÉLIORATION_PRÉVISIONS]

MACHINE LEARNING AUGMENTATION :
- Neural networks : [CNN_POUR_PATTERNS_SPATIAUX_U-NET]
- Gradient boosting : [XGBOOST_POUR_RELATIONS_COMPLEXES]
- Deep learning : [TRANSFORMERS_POUR_SÉQUENCES_TEMPORIELLES]
- Hybrid approaches : [FUSION_MODÈLES_PHYSIQUES_STATISTIQUES]

VALIDATION OPÉRATIONNELLE :
MÉTRIQUES PRÉVISIONNELLES :
- RMSE température : [ERREUR_QUADRATIQUE_MOYENNE_CELSIUS]
- POD précipitations : [PROBABILITÉ_DÉTECTION_PLUIE]
- FAR fausses alarmes : [FRÉQUENCE_FAUSSES_ALERTES]
- BSS skill score : [AMÉLIORATION_VS_PRÉVISION_PERSISTANCE]

ÉVALUATION IMPACT :
- Utility scores : [VALEUR_ÉCONOMIQUE_PRÉVISIONS_SECTEUR]
- Cost-loss ratios : [OPTIMISATION_DÉCISIONS_MÉTÉO_DÉPENDANTES]
- User satisfaction : [ADOPTION_PRÉVISIONS_UTILISATEURS_FINAUX]
- Warning effectiveness : [RÉDUCTION_PERTES_MÉTÉO_EXTREME]

IMPLÉMENTATION OPÉRATIONNELLE :
ARCHITECTURE SYSTÈME :
- High-performance computing : [CLUSTERS_GPU_SUPERCOMPUTERS]
- Data pipelines : [INGESTION_TRAITEMENT_DISTRIBUTION_AUTOMATISÉE]
- API services : [REST_APIS_GRPC_HAUTE_DISPONIBILITÉ]
- Monitoring alerting : [SUPERVISION_TEMPS_RÉEL_ANOMALIES]

PRODUCTION WORKFLOW :
- Model runs : [CYCLES_QUOTIDIENS_MULTIHORIZONS]
- Quality assurance : [VALIDATION_AUTOMATISÉE_SEUILS_QUALITÉ]
- Product generation : [CRÉATION_PRODUITS_UTILISATEURS_FINALISÉS]
- Dissemination : [DISTRIBUTION_CANAUX_UTILISATEURS_DIVERS]

COMMUNICATION UTILISATEUR :
VISUALISATIONS SPÉCIALISÉES :
- Weather maps : [CARTES_SYNOPTIQUES_INTERACTIVES]
- Probability forecasts : [PRÉVISIONS_PROBABILISTES_INCERTITUDE]
- Impact-based warnings : [ALERTES_IMPACT_SECTEUR_SPÉCIFIQUE]
- Trend analysis : [ANALYSES_TENDANCES_CHANGEMENT_CLIMATIQUE]

FORMATION UTILISATEURS :
- Technical training : [INTERPRÉTATION_PRODUITS_MÉTÉOROLOGIQUES]
- Decision support : [INTÉGRATION_DÉCISIONS_OPÉRATIONNELLES]
- Risk communication : [COMMUNICATION_INCERTITUDE_EFFICACE]
- Feedback integration : [AMÉLIORATION_CONTINUE_UTILISATEUR]

MAINTENANCE ÉVOLUTION :
RECHERCHE DÉVELOPPEMENT :
- Model improvements : [NOUVELLES_PHYSIQUES_AMÉLIORATIONS_NUMÉRIQUES]
- Data assimilation advances : [MEILLEURES_INTÉGRATIONS_OBSERVATIONS]
- Post-processing innovations : [AMÉLIORATIONS_PRÉVISIONS_UTILISATEURS]
- Verification methods : [NOUVELLES_MÉTRIQUES_ÉVALUATION]

SYSTÈME ÉVOLUTION :
- Technology upgrades : [NOUVELLES_ARCHITECTURES_COMPUTATIONNELLES]
- Data volume growth : [GESTION_BIG_DATA_MÉTÉOROLOGIQUES]
- User requirements changes : [ADAPTATION_BESOINS_UTILISATEURS_ÉVOLUTIFS]
- Climate change adaptation : [MODÉLISATION_CHANGEMENTS_CLIMATIQUES]
```

## 📊 Métriques de Performance Prévisionnelle

### Évaluation Quantitative

| Métrique | Excellent | Bon | À Améliorer |
|----------|-----------|-----|-------------|
| **MAE** | < 5% erreur moyenne | 5-10% | > 10% |
| **RMSE** | < 7% erreur quadratique | 7-15% | > 15% |
| **Accuracy** | > 90% bonnes prédictions | 80-90% | < 80% |
| **Coverage** | Intervalle confiance approprié | Légèrement large/étroit | Très inexact |
| **Timing** | Prédictions temps réel | < 1h retard | Délais importants |

### Évaluation Qualitative

| Critère | Indicateurs Excellence |
|---------|----------------------|
| **Robustesse** | Résiste aux données manquantes, outliers |
| **Interprétabilité** | Explication facteurs prédiction claire |
| **Scalabilité** | Performance maintenue volume croissant |
| **Maintenance** | Facilité mise à jour, évolution |
| **Business Value** | Impact mesuré décisions, ROI positif |

### Framework d'Amélioration Continue

**Phase 1 : Diagnostic**
- Audit modèles existants
- Analyse erreurs prédiction
- Benchmark concurrents

**Phase 2 : Développement**
- Nouveaux algorithmes testés
- Features additionnelles
- Validation croisée rigoureuse

**Phase 3 : Déploiement**
- A/B testing production
- Monitoring performance
- Feedback utilisateurs

**Phase 4 : Optimisation**
- Fine-tuning paramètres
- Ensemble modeling
- Automatisation processus

Ces templates constituent votre arsenal complet pour développer des systèmes de prévision robustes, précis et opérationnels, capables de traiter l'incertitude et de supporter des décisions critiques dans tous domaines d'application.
