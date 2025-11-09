# 🔍 Templates pour le Débogage et l'Optimisation

## 🟢 Template Débutant : Erreur Simple

```
J'ai cette erreur [TYPE_ERREUR] dans mon code [LANGAGE] :

ERREUR :
[COLLER_LE_MESSAGE_D'ERREUR_COMPLET]

CODE PROBLÉMATIQUE :
[COLLER_LE_CODE_AVEC_LIGNE_ERREUR]

CONTEXTE :
- Ce que le code est censé faire : [DESCRIPTION]
- Quand l'erreur se produit : [CONDITIONS]
- Environnement : [VERSION_LANGAGE, OS, LIBRAIRIES]

AIDE DEMANDÉE :
1. Explique-moi la cause de cette erreur
2. Donne-moi la solution pour la corriger
3. Explique-moi comment éviter cette erreur à l'avenir
```

## 🟡 Template Intermédiaire : Performance Degradation

```
Analyse cette dégradation de performance dans [APPLICATION/SYSTÈME].

SYMPTÔMES OBSERVÉS :
- [MÉTRIQUE_AFFECTÉE : temps réponse, CPU, mémoire]
- Valeur actuelle : [VALEUR_PROBLÉMATIQUE]
- Valeur normale : [VALEUR_ATTENDUE]
- Quand se produit : [CONDITIONS_DÉCLENCHEMENT]

CONTEXTE TECHNIQUE :
- Architecture : [MONOLITH/MICROSERVICES/SERVERLESS]
- Technologies : [LANGAGE, FRAMEWORK, BASE_DONNÉES]
- Charge actuelle : [UTILISATEURS_CONCURRENTS, VOLUME_DONNÉES]
- Métriques système : [CPU, RAM, DISQUE, RÉSEAU]

CODE/LOGS SUSPECTS :
[EXTRAITS_DE_CODE_PROBLÉMATIQUES]
[LOGS_D'ERREUR_OU_PERFORMANCE]

ANALYSE DEMANDÉE :
1. Diagnostic des causes potentielles (top 3)
2. Solutions prioritaires avec impact estimé
3. Plan de monitoring pour prévention future
4. Recommandations d'architecture si nécessaire
```

## 🔴 Template Avancé : Système Complexe en Production

```
Diagnostic complet d'un problème système critique en production.

DESCRIPTION DU PROBLÈME :
[IMPACT_BUSINESS : perte de revenus, utilisateurs affectés]
[SYMPTÔMES : erreurs, lenteurs, indisponibilité]
[TIMING : quand commencé, évolution temporelle]

INFRASTRUCTURE AFFECTÉE :
- Composants : [SERVICES, BASES_DE_DONNÉES, CACHE, LOAD_BALANCERS]
- Architecture : [MICROSERVICES, SERVERLESS, MONOLITH]
- Déploiement : [KUBERNETES, DOCKER, VM, SERVERLESS]
- Monitoring : [OUTILS_UTILISÉS : Prometheus, DataDog, CloudWatch]

DONNÉES DE DIAGNOSTIC :
LOGS :
[EXTRAITS_LOGS_SIGNIFICATIFS]
[ERROR_PATTERNS_IDENTIFIÉS]

MÉTRIQUES :
[GRAPHIQUES_OU_VALEURS_CLÉS]
[ÉVOLUTION_AVANT/APRÈS_PROBLÈME]

TRACING :
[CHAÎNE_D'APPELS_PROBLÉMATIQUE]
[LATENCES_PAR_SERVICE]

ANALYSE REQUISE :
1. Root cause analysis (5 pourquoi)
2. Impact assessment (utilisateurs, business, technique)
3. Solutions immédiates (rollback, mitigation)
4. Solutions définitives (fix, architecture)
5. Plan de prévention (tests, monitoring, alerting)
6. Communication plan (stakeholders, utilisateurs)

LIVRABLES ATTENDUS :
- Rapport d'incident complet
- Actions correctives prioritaires
- Mesures préventives
- Indicateurs de suivi post-résolution
```

## 🚀 Template Expert : Optimisation Système à Grande Échelle

```
Optimisation complète d'un système à haute charge et criticité.

CONTEXTE SYSTÈME :
- Échelle : [UTILISATEURS_CONCURRENTS, REQUÊTES/SECONDE]
- Architecture : [MICROSERVICES, EVENT-DRIVEN, SERVERLESS]
- Technologies : [STACK_COMPLET_AVEC_VERSIONS]
- Contraintes : [SLA_DISPONIBILITÉ, LATENCE_MAX, COÛT_BUDGET]

PROBLÈMES IDENTIFIÉS :
PERFORMANCE :
- [GOULOT_1 : description quantitative]
- [GOULOT_2 : métriques et impact]
- [PATTERN_DE_CHARGE : pics, croissance]

SCALABILITÉ :
- [LIMITE_ACTUELLE : nombre utilisateurs/requêtes]
- [FACTEUR_BLOQUANT : CPU, mémoire, I/O, réseau]
- [ARCHITECTURE_LIMITANTE : monolithic, single points of failure]

COÛT :
- [DÉPENSE_PAR_UTILISATEUR/REQUÊTE]
- [RESSOURCES_SURDIMENSIONNÉES]
- [OPTIMISATIONS_POSSIBLES : reserved instances, spot instances]

ANALYSE TECHNIQUE DÉTAILLÉE :
PROFILING :
[OUTILS_UTILISÉS : APM, profilers, flame graphs]
[RÉSULTATS : fonctions lentes, allocations mémoire, I/O bottlenecks]

ARCHITECTURE REVIEW :
[POINTS_FAIBLES_IDENTIFIÉS]
[ANTI-PATTERNS_DÉTECTÉS : N+1 queries, tight coupling]
[OPPORTUNITÉS_D'AMÉLIORATION]

DONNÉES ET ANALYTICS :
[QUERIES_LENTES : exemples avec EXPLAIN plans]
[CACHE_MISS_RATES : efficacité mise en cache]
[DATA_SKEW : répartition inégale des données]

STRATÉGIES D'OPTIMISATION :
COURT TERME (0-3 mois) :
1. [OPTIMISATION_1 : impact estimé, effort]
2. [OPTIMISATION_2 : métriques cibles]
3. [QUICK_WINS : gains immédiats]

MOYEN TERME (3-12 mois) :
1. [REFACTORING_1 : architecture cible]
2. [MIGRATION_TECHNO : nouvelle stack]
3. [INFRA_OPTIMIZATION : cloud optimization]

LONG TERME (1+ an) :
1. [REWRITING : reconstruction complète]
2. [ARCHITECTURE_EVOLUTION : event-sourcing, CQRS]
3. [INNOVATION : AI/ML integration, edge computing]

IMPLEMENTATION ROADMAP :
PHASE 1 : DIAGNOSTIC ET BASELINE
- Métriques actuelles détaillées
- Tests de charge représentatifs
- Profiling complet du système

PHASE 2 : OPTIMISATIONS RAPIDES
- Quick wins identifiés
- Monitoring temps réel
- Rollback planifié

PHASE 3 : AMÉLIORATIONS STRUCTURELLES
- Refactoring planifié
- Tests de non-régression
- Déploiement progressif

PHASE 4 : EVOLUTION ARCHITECTURALE
- Nouvelle architecture design
- Migration progressive
- Formation équipes

MÉTRIQUES DE SUCCÈS :
PERFORMANCE :
- Latence moyenne : cible < [X]ms
- Throughput : cible > [Y] req/s
- Disponibilité : cible > [Z]%

COÛT :
- Réduction coût/unité : cible [A]%
- ROI optimisation : payback < [B] mois

QUALITÉ :
- Erreurs système : cible < [C]%
- Satisfaction utilisateur : cible > [D]/5

OUTILS ET MÉTHODOLOGIE :
- APM : [DataDog, New Relic, Dynatrace]
- Profiling : [PyCharm, VisualVM, perf]
- Load testing : [JMeter, Locust, k6]
- Monitoring : [Prometheus, Grafana, Kibana]
- Methodologie : [DevOps, SRE, Lean]

LIVRABLES EXPERTS :
1. Rapport d'optimisation complet avec ROI
2. Plan d'implémentation détaillé par phase
3. Dashboard de monitoring prédéfini
4. Runbook opérationnel post-optimisation
5. Playbook de réponse aux incidents futurs
```

## 🎯 Templates Spécialisés

### Template Débogage Mémoire

```
Diagnostic d'un problème de mémoire dans [APPLICATION_LANGAGE].

SYMPTÔMES :
- [TYPE_PROBLÈME : leaks, OOM, fragmentation]
- Fréquence : [OCCURRENCE : systématique, aléatoire, charge]
- Impact : [EFFET : crash, lenteur, indisponibilité]

CONTEXTE :
- Architecture : [HEAP_SIZE, GC_STRATEGY, ALLOCATION_PATTERNS]
- Charge : [UTILISATEURS, DONNÉES_TRAITÉES]
- Environnement : [JVM_VERSION, CONTAINER_LIMITS]

OUTILS UTILISÉS :
[PROFILING_TOOLS : VisualVM, MAT, JProfiler]
[MONITORING : heap dumps, GC logs, thread dumps]

ANALYSE DEMANDÉE :
1. Root cause identification
2. Memory leak sources (top 5)
3. GC inefficiency patterns
4. Solutions prioritaires avec code examples
5. Monitoring recommendations
6. Prevention best practices
```

### Template Optimisation Base de Données

```
Optimisation d'une base de données [TYPE : PostgreSQL, MongoDB, Redis] sous haute charge.

CONTEXTE CHARGE :
- Requêtes/seconde : [QPS_ACTUEL vs CIBLE]
- Latence moyenne : [LATENCE_ACTUELLE vs CIBLE]
- Taille données : [VOLUME_ACTUEL vs PRÉVISIONS]

QUERIES PROBLÉMATIQUES :
[SLOW_QUERIES_AVEC_EXPLAIN_PLAN]
[N+1_QUERIES_IDENTIFIÉES]
[LOCK_CONTENTION_ISSUES]

SCHÉMA ET INDEXES :
[TABLES_SANS_INDEXES_PRIMAIRES]
[INDEXES_INEFFICACES]
[RELATIONS_NON_OPTIMISÉES]

CONFIGURATION ACTUELLE :
[PARAMÈTRES_MÉMOIRE : shared_buffers, work_mem]
[PARAMÈTRES_CONNEXIONS : max_connections, pool_size]
[PARAMÈTRES_MAINTENANCE : autovacuum, analyze]

OPTIMISATIONS PROPOSÉES :
1. [INDEX_OPTIMIZATION : types, colonnes, impact]
2. [QUERY_REWRITING : refactorings SQL]
3. [CONFIGURATION_TUNING : paramètres cibles]
4. [ARCHITECTURE_CHANGES : partitioning, replication]

IMPLEMENTATION PLAN :
- Tests de performance avant/après
- Rollback strategy
- Monitoring post-déploiement
- Alerting thresholds
```

### Template Profiling Performance

```
Analyse complète des performances d'une application [TYPE : WEB, MOBILE, API].

MÉTRIQUES DE BASELINE :
- Temps réponse moyen : [VALEUR]ms
- Throughput : [VALEUR] req/s
- Utilisation CPU : [VALEUR]%
- Utilisation mémoire : [VALEUR]%
- Erreurs/minute : [VALEUR]

PROFILING MÉTHODOLOGIQUE :
OUTILS :
- CPU : [async-profiler, Java Flight Recorder]
- Mémoire : [heap dumps, memory profilers]
- I/O : [disk I/O, network monitoring]
- Database : [slow query logs, connection pooling]

POINTS D'ATTENTION :
1. [HOTSPOTS_IDENTIFIÉS : méthodes/functions lentes]
2. [MEMORY_PRESSURE : allocations excessives, leaks]
3. [I/O_BOTTLENECKS : disk, network, database calls]
4. [CONCURRENCY_ISSUES : locks, deadlocks, contention]

ANALYSE PAR COMPOSANT :
- Frontend : [rendering, JavaScript execution, network]
- Backend : [API calls, business logic, data processing]
- Database : [queries, connections, caching]
- Infrastructure : [load balancing, CDN, caching layers]

RECOMMANDATIONS PRIORITAIRES :
1. [HIGH_IMPACT_QUICK_WIN : effort faible, impact élevé]
2. [MEDIUM_TERM_OPTIMIZATION : effort moyen, impact significatif]
3. [ARCHITECTURAL_IMPROVEMENT : effort élevé, impact majeur]

IMPLEMENTATION ROADMAP :
- Phase 1 : Optimisations immédiates (1-2 semaines)
- Phase 2 : Améliorations structurelles (1-3 mois)
- Phase 3 : Évolution architecturale (3-6 mois)
```

## 📊 Framework d'Analyse Débogage

### Méthodologie Structurée

```
1. REPRODUCTION
   ├── Conditions précises pour reproduire
   ├── Environnement minimal
   └── Données de test représentatives

2. ISOLATION
   ├── Division en composants
   ├── Tests unitaires ciblés
   └── Élimination des variables confondantes

3. DIAGNOSTIC
   ├── Logs et métriques détaillés
   ├── Profiling systématique
   └── Analyse des causes racines (5 pourquoi)

4. RÉSOLUTION
   ├── Solutions hiérarchisées par impact
   ├── Tests de validation
   └── Mesures de prévention

5. VALIDATION
   ├── Tests de non-régression
   ├── Monitoring post-fix
   └── Documentation des leçons apprises
```

### Outils par Type de Problème

| Type de Problème | Outils Recommandés | Métriques Clés |
|------------------|-------------------|----------------|
| **Performance** | APM (New Relic, DataDog), Profilers (YourKit, JProfiler) | Latence, throughput, utilisation ressources |
| **Mémoire** | Memory analyzers (MAT, VisualVM), Heap dumps | GC frequency, memory leaks, fragmentation |
| **Base de données** | Query analyzers (PgBadger, slow log), EXPLAIN plans | Query time, index usage, lock waits |
| **Réseau** | Wireshark, network monitors, load balancers logs | Latence réseau, timeouts, retransmissions |
| **Concurrency** | Thread dumps, deadlock detectors, race condition tools | Lock contention, deadlocks, thread utilization |

### Indicateurs de Qualité des Solutions

- **Efficacité** : Problème résolu sans effets secondaires
- **Robustesse** : Solution fonctionne dans tous les scénarios
- **Maintenabilité** : Code reste lisible et évolutif
- **Observabilité** : Métriques permettent de détecter les récidives
- **Documentabilité** : Solution peut être expliquée et enseignée

Ces templates constituent votre arsenal complet pour diagnostiquer, déboguer et optimiser les systèmes informatiques complexes, transformant les problèmes techniques en opportunités d'amélioration continue.
