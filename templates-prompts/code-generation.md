# 🔧 Templates pour la Génération de Code

## 🟢 Template Débutant : Fonction Simple

```
Écris une fonction [LANGAGE] qui [DESCRIPTION_SIMPLE].

Exemple concret : Écris une fonction Python qui calcule la factorielle d'un nombre entier positif.

Contraintes :
- Utilise une approche récursive
- Gère les cas d'erreur (négatif, non-entier)
- Ajoute des commentaires explicatifs
- Format : fonction + tests unitaires simples
```

## 🟡 Template Intermédiaire : Module Complet

```
Développe un module [LANGAGE] pour [FONCTIONNALITÉ].

CONTEXTE :
- [DESCRIPTION_DÉTAILLÉE_DU_BESOIN]
- [CONTRAINTES_TECHNIQUES : compatibilité, performance, sécurité]

EXIGENCES FONCTIONNELLES :
- [FONCTION_1 : description précise]
- [FONCTION_2 : description précise]
- [GESTION_ERREURS : cas à traiter]

ARCHITECTURE SOUHAITÉE :
- [PATTERN_DE_CONCEPTION : MVC, Factory, Observer...]
- [STRUCTURE : classes/interfaces/modules]
- [DÉPENDANCES : bibliothèques externes]

SORTIE ATTENDUE :
- Code complet et fonctionnel
- Commentaires détaillés
- Tests unitaires
- Documentation d'utilisation
- Exemples d'usage concret
```

## 🔴 Template Avancé : Application Web

```
Conçois et développe une application web [TYPE : full-stack, SPA, API...] en [STACK_TECHNO].

PROBLÉMATIQUE BUSINESS :
[CONTEXTE_MÉTIER_DÉTAILLÉ]
[OBJECTIFS_UTILISATEUR]
[CONTRAINTES_FONCTIONNELLES]

ARCHITECTURE TECHNIQUE :
FRONTEND :
- Framework : [React/Vue/Angular]
- État : [Redux/Context/Zustand]
- UI : [Tailwind/Material-UI/Chakra]
- Routing : [React Router/Vue Router]

BACKEND :
- Runtime : [Node.js/Python/Go]
- Framework : [Express/FastAPI/Gin]
- Base de données : [PostgreSQL/MongoDB/Redis]
- Authentification : [JWT/OAuth/Sessions]

FONCTIONNALITÉS CLÉS :
1. [AUTHENTIFICATION : inscription, connexion, profils]
2. [CORE_FEATURE : fonctionnalité principale détaillée]
3. [GESTION_DONNÉES : CRUD, recherche, filtres]
4. [INTÉGRATIONS : APIs externes, paiement, notifications]

EXIGENCES NON-FONCTIONNELLES :
- Performance : [métriques cibles : temps réponse, débit]
- Sécurité : [OWASP top 10, chiffrement, validation]
- Accessibilité : [WCAG 2.1 AA, responsive design]
- Maintenabilité : [tests automatisés, documentation]

LIVRABLES :
- Code source complet et organisé
- Tests automatisés (unitaires + intégration)
- Documentation API (Swagger/OpenAPI)
- Guide de déploiement (Docker + CI/CD)
- Scripts de migration base de données
```

## 🚀 Template Expert : Système Distribué

```
Architecte et implémente un système distribué [TYPE : microservices, serverless, edge computing] pour [CAS_D'USAGE_CRITIQUE].

VISION SYSTÈME :
[PROBLÉMATIQUE_COMPLEXE_À_RÉSOUDRE]
[IMPACT_BUSINESS_ATTENDU]
[CONTRAINTES_SCALABILITÉ : utilisateurs concurrents, volume données]

ARCHITECTURE DISTRIBUÉE :
INFRASTRUCTURE :
- Cloud provider : [AWS/GCP/Azure multi-cloud]
- Orchestration : [Kubernetes/Docker Swarm]
- Service mesh : [Istio/Linkerd]
- Base de données : [architecture distribuée, sharding, replication]

MICROSERVICES :
1. [SERVICE_API_GATEWAY : routage, authentification, rate limiting]
2. [SERVICE_CORE : logique métier principale]
3. [SERVICE_DATA : gestion données, cache, analytics]
4. [SERVICE_COMMUNICATION : messaging, notifications, realtime]
5. [SERVICE_INFRA : monitoring, logging, sécurité]

PATTERNS ARCHITECTURAUX :
- [SAGA : coordination transactions distribuées]
- [CIRCUIT_BREAKER : résilience pannes]
- [EVENT_SOURCING : historique complet des changements]
- [CQRS : séparation lecture/écriture]
- [API_COMPOSITION : agrégation services]

EXIGENCES TECHNIQUES AVANCÉES :
PERFORMANCE :
- Latence < [X]ms pour 95% des requêtes
- Débit > [Y] req/s
- Disponibilité > 99.99% (SLA)

SÉCURITÉ :
- Zero-trust architecture
- End-to-end encryption
- Automated security scanning
- Compliance [RGPD/HIPAA/SOX]

OBSERVABILITÉ :
- Distributed tracing (Jaeger/OpenTelemetry)
- Centralized logging (ELK stack)
- Metrics collection (Prometheus)
- Real-time monitoring (Grafana)

DÉPLOIEMENT :
- GitOps workflow (ArgoCD/Flux)
- Progressive delivery (feature flags, canary)
- Automated testing (chaos engineering)
- Disaster recovery automation

LIVRABLES EXPERTS :
- Architecture détaillée (diagrammes C4)
- Code source production-ready
- Infrastructure as Code (Terraform/CloudFormation)
- Pipelines CI/CD complets
- Runbooks opérationnels
- Plans de sécurité et conformité
- Métriques et tableaux de bord
- Tests de charge et performance
```

## 🎯 Templates Spécialisés

### Template API REST Optimisée

```
Crée une API REST robuste en [LANGAGE] pour [DOMAINE_MÉTIER].

ENDPOINTS PRINCIPAUX :
- GET /api/v1/[ressources] - Liste paginée avec filtres
- POST /api/v1/[ressources] - Création avec validation
- GET /api/v1/[ressources]/{id} - Détail avec relations
- PUT /api/v1/[ressources]/{id} - Mise à jour partielle
- DELETE /api/v1/[ressources]/{id} - Suppression logique

FONCTIONNALITÉS AVANCÉES :
- Pagination intelligente (cursor-based pour performance)
- Filtrage complexe (opérateurs : eq, ne, gt, lt, like, in)
- Tri multi-niveaux avec nulls handling
- Recherche full-text avec scoring
- Rate limiting par endpoint et utilisateur
- Caching multi-niveaux (Redis + HTTP)
- Versioning sémantique d'API
- HATEOAS pour navigation

SÉCURITÉ INTÉGRÉE :
- Authentification JWT avec refresh tokens
- Autorisation RBAC (Role-Based Access Control)
- Validation des entrées (sanitization + schema)
- Protection contre les attaques courantes (OWASP Top 10)
- Audit logging complet
- CORS configuration sécurisée

PERFORMANCE :
- Réponse < 200ms pour 95% des requêtes
- Gestion des timeouts et circuit breakers
- Compression automatique des réponses
- Database optimization (indexes, query planning)
- Connection pooling et prepared statements

TESTING COMPREHENSIF :
- Tests unitaires (> 80% couverture)
- Tests d'intégration API
- Tests de performance (load testing)
- Tests de sécurité automatisés
- Tests de régression avec données synthétiques

DOCUMENTATION :
- OpenAPI 3.0 specification complète
- Exemples d'usage pour chaque endpoint
- SDKs générés automatiquement (Python, JavaScript, Go)
- Guides d'intégration pour développeurs
```

### Template Optimisation Algorithme

```
Optimise cet algorithme [PROBLÈME_INITIAL] pour améliorer sa complexité de [O_INITIAL] vers [O_CIBLE].

CONTEXTE :
[DESCRIPTION_DU_PROBLÈME]
[CONTRAINTES : temps, espace, données d'entrée]

ANALYSE INITIALE :
Complexité actuelle : [O(n²), O(n log n), etc.]
Goulots d'étranglement identifiés :
- [POINT_1 : cause et impact]
- [POINT_2 : cause et impact]

STRATÉGIES D'OPTIMISATION :
1. [APPROCHE_1 : algorithme de substitution]
   - Complexité : [O_CIBLE_1]
   - Trade-offs : [avantages/inconvénients]

2. [APPROCHE_2 : optimisation structure de données]
   - Structure : [HashMap, Trie, Segment Tree, etc.]
   - Amélioration : [facteur d'optimisation]

3. [APPROCHE_3 : parallélisation/vectorisation]
   - Framework : [OpenMP, CUDA, SIMD]
   - Scalabilité : [speedup théorique]

IMPLÉMENTATION OPTIMISÉE :
- Code complet avec commentaires détaillés
- Comparaison performances avant/après
- Tests de robustesse (edge cases)
- Mesures de complexité temporelle/espace

VALIDATION :
- Jeux de tests représentatifs
- Métriques de performance (temps, mémoire)
- Analyse de stabilité statistique
- Comparaison avec baselines existantes

EXTENSIONS POSSIBLES :
- [APPROCHE_AVANCÉE_1 : machine learning]
- [APPROCHE_AVANCÉE_2 : quantum computing]
- [SCALABILITÉ : adaptation à big data]
```

### Template Refactoring Legacy

```
Refactorise ce code legacy [LANGAGE] pour améliorer [ASPECTS_CIBLÉS : maintenabilité, performance, sécurité].

CODE ORIGINAL :
[COLLER_LE_CODE_LEGACY_ICI]

ANALYSE DES PROBLÈMES :
1. [CODE_SMELL_1] : Impact et fréquence
2. [CODE_SMELL_2] : Complexité introduite
3. [TECHNICAL_DEBT] : Coûts de maintenance

OBJECTIFS DE REFACTORING :
- [MAINTENABILITÉ] : Réduire la complexité cyclomatique
- [PERFORMANCE] : Optimiser les goulots d'étranglement
- [SÉCURITÉ] : Éliminer les vulnérabilités identifiées
- [TESTABILITÉ] : Améliorer la couverture de tests

PATTERNS APPLIQUÉS :
1. [PATTERN_1 : Extract Method, Move Method]
   - Avant : [code problématique]
   - Après : [structure refactorisée]
   - Bénéfices : [améliorations mesurées]

2. [PATTERN_2 : Replace Conditional with Polymorphism]
   - Architecture : [classes/interfaces créées]
   - Extensibilité : [ajout facile de nouveaux cas]

3. [PATTERN_3 : Introduce Parameter Object]
   - Groupement : [paramètres liés rassemblés]
   - Lisibilité : [signature méthode simplifiée]

VALIDATION POST-REFACTORING :
- Tests de non-régression complets
- Métriques de qualité (maintainability index)
- Performance benchmarking
- Code review et documentation

MIGRATION PROGRESSIVE :
- Feature flags pour déploiement gradué
- Compatibilité descendante maintenue
- Rollback planifié
- Monitoring post-déploiement
```

## 📊 Métriques de Qualité des Prompts

| Critère | Excellent | Bon | À Améliorer |
|---------|-----------|-----|-------------|
| **Clarté** | Objectif précis, contexte complet | Objectif identifiable | Ambigu, manque de contexte |
| **Structure** | Format bien défini, sections logiques | Structure basique | Désorganisé, flux confus |
| **Contraintes** | Spécifications détaillées et réalistes | Quelques contraintes définies | Contraintes vagues ou manquantes |
| **Actionnabilité** | Résultats directement utilisables | Résultats utilisables avec adaptations | Nécessite beaucoup de retravail |
| **Innovation** | Encourage créativité et solutions nouvelles | Suit les bonnes pratiques | Reproduit seulement les patterns connus |

## 🔄 Optimisation Itérative des Prompts

### Phase 1 : Test Initial
```
Prompt de base → Résultat obtenu → Analyse des écarts
```

### Phase 2 : Raffinement
```
Ajout de contraintes spécifiques → Clarification du contexte → Précision du format attendu
```

### Phase 3 : Spécialisation
```
Personnalisation pour le domaine → Intégration d'exemples → Optimisation des variables
```

### Phase 4 : Standardisation
```
Création de template réutilisable → Documentation des meilleures pratiques → Partage équipe
```

Ces templates constituent votre arsenal complet pour générer du code de qualité professionnelle avec les assistants IA, maximisant l'efficacité tout en maintenant les standards de développement élevés.
