# 🧪 Templates pour les Tests Automatisés

## 🟢 Template Débutant : Tests Unitaires Simples

```
Crée une suite de tests unitaires pour [FONCTION/MODULE] en [LANGAGE].

FONCTION À TESTER :
[COLLER_LE_CODE_DE_LA_FONCTION]

CAS DE TEST À COUVRIR :
1. [CAS_NOMINAL : description, entrée, sortie attendue]
2. [CAS_ERREUR : description, entrée, exception attendue]
3. [CAS_LIMITE : description, entrée edge case, comportement attendu]

FRAMEWORK DE TEST :
- [LANGAGE] : [JUnit, pytest, Jest, etc.]
- Assertions : [bibliothèque utilisée]
- Mocking : [si nécessaire pour dépendances externes]

STRUCTURE DES TESTS :
- Arrange : préparation données et objets
- Act : exécution fonction testée
- Assert : vérification résultats

GÉNÉRATION DEMANDÉE :
- Code complet des tests
- Exécution et résultats attendus
- Explication de chaque test case
```

## 🟡 Template Intermédiaire : Tests d'Intégration

```
Développe des tests d'intégration pour [MODULE/SERVICE] avec [DÉPENDANCES_EXTERNES].

CONTEXTE TECHNIQUE :
- Composant testé : [DESCRIPTION_MODULE]
- Dépendances : [API, BASE_DONNÉES, SERVICES_EXTERNES]
- Environnement : [DEV, STAGING, PRODUCTION-LIKE]

STRATÉGIE DE TEST :
APPROCHE :
- [BIG_BANG, TOP_DOWN, BOTTOM_UP, SANDWICH]
- Isolation : [CONTAINERS, MOCKS, STUBS]
- Données de test : [FIXTURES, FACTORIES, RANDOM]

SCÉNARIOS D'INTÉGRATION :
1. [SCENARIO_1 : description complète]
   - Préconditions : [état initial requis]
   - Actions : [séquence d'appels/interactions]
   - Assertions : [résultats attendus]

2. [SCENARIO_2 : description complète]
   - Préconditions : [état initial requis]
   - Actions : [séquence d'appels/interactions]
   - Assertions : [résultats attendus]

INFRASTRUCTURE DE TEST :
- Testcontainers : [DOCKER_IMAGES_UTILISÉES]
- Base de données : [IN_MEMORY_DB, REAL_DB_ISOLATED]
- Services externes : [WIREFMOCK, CONTRACT_TESTING]
- CI/CD : [PIPELINE_INTEGRATION]

CODES DE TEST :
- Setup/teardown automatisé
- Gestion des données de test
- Assertions multi-niveaux
- Reporting détaillé
```

## 🔴 Template Avancé : Tests End-to-End Complets

```
Conçois une stratégie complète de tests end-to-end pour [APPLICATION_WEB/MOBILE/API].

APPLICATION À TESTER :
- Type : [WEB_APP, MOBILE_APP, API_REST, MICROSERVICES]
- Utilisateurs : [PROFILS_UTILISATEUR_TYPES]
- Parcours critiques : [USER_JOURNEYS_PRINCIPAUX]

ARCHITECTURE DE TEST :
OUTILS TECHNIQUES :
- Framework E2E : [Cypress, Selenium, Playwright, Appium]
- Langage : [JavaScript, Python, Java, C#]
- CI/CD : [GitHub Actions, Jenkins, GitLab CI]
- Reporting : [Allure, ReportPortal, TestRail]

STRATÉGIE DE COUVERTURE :
USER JOURNEYS CRITIQUES :
1. [PARCOURS_1 : description complète]
   - Étapes : [CLIC, SAISIE, NAVIGATION]
   - Assertions : [ÉLÉMENTS_VISIBLES, DONNÉES_CORRECTES]
   - Données de test : [SCÉNARIOS_VARIATIONS]

2. [PARCOURS_2 : description complète]
   - Étapes : [CLIC, SAISIE, NAVIGATION]
   - Assertions : [ÉLÉMENTS_VISIBLES, DONNÉES_CORRECTES]
   - Données de test : [SCÉNARIOS_VARIATIONS]

GESTION DES DONNÉES :
- Isolation : [TEST_DATA_SEPARATION, CLEANUP_AUTOMATIQUE]
- Variabilité : [RANDOM_DATA_GENERATION, EDGE_CASES]
- Persistance : [DATABASE_RESET, API_MOCKING]

ENVIRONNEMENTS DE TEST :
- Local : [DOCKER_COMPOSE, LOCALSTACK]
- CI : [PARALLEL_EXECUTION, MATRIX_TESTING]
- Staging : [PRODUCTION_LIKE_ENVIRONMENT]
- Production : [CANARY_TESTING, FEATURE_FLAGS]

PERFORMANCE E2E :
- Métriques : [RESPONSE_TIME, MEMORY_USAGE, ERROR_RATE]
- Thresholds : [ACCEPTABLE_LIMITS_PAR_MÉTRIQUE]
- Monitoring : [REAL_TIME_ALERTS, HISTORICAL_TRENDS]

RÉSILIENCE ET CHAOS :
- Network failures simulation
- Service degradation testing
- Database connection loss
- High load scenarios

MAINTENANCE DES TESTS :
- Flakiness detection : [RETRY_MECHANISMS, STABILITY_METRICS]
- Refactoring : [PAGE_OBJECTS, CUSTOM_COMMANDS]
- Documentation : [TEST_CASE_DOCUMENTATION, VIDEO_RECORDING]
```

## 🚀 Template Expert : Pyramide de Tests Complète

```
Architecte une pyramide de tests complète pour [APPLICATION_ENTERPRISE] avec automatisation maximale.

CONTEXTE APPLICATION :
- Échelle : [TAILLE_CODEBASE, ÉQUIPES, UTILISATEURS]
- Complexité : [MICROSERVICES, LÉGACY_SYSTEMS, DISTRIBUTED_ARCHITECTURE]
- Criticité : [BUSINESS_CRITICAL, REGULATED_INDUSTRY]

PYRAMIDE DE TESTS CIBLE :
UNITAIRES (70-80%) :
- Couverture : > 80% lignes de code
- Rapidité : < 10 minutes exécution complète
- Isolation : tests indépendants, mocks/stubs
- Frameworks : [JUnit, pytest, Jest, xUnit]

INTEGRATION (15-20%) :
- Couverture : APIs, bases de données, services externes
- Rapidité : < 30 minutes
- Environnements : containers, test databases
- Patterns : [CONSUMER_DRIVEN_CONTRACTS, CDC]

END-TO-END (5-10%) :
- Couverture : user journeys critiques uniquement
- Rapidité : < 60 minutes
- Environnements : staging/production-like
- Focus : business value vs technical coverage

STRATÉGIE D'AUTOMATISATION :
INFRASTRUCTURE CI/CD :
- Build automation : [GRADLE, MAVEN, NPM_SCRIPTS]
- Test execution : [PARALLEL_RUNS, DYNAMIC_SCALING]
- Artifact management : [NEXUS, ARTIFACTORY, DOCKER_REGISTRY]
- Deployment : [KUBERNETES, DOCKER_COMPOSE, CLOUD_RUN]

OUTILS ET FRAMEWORKS :
TESTING FRAMEWORKS :
- Unit : [FRAMEWORK_PAR_LANGAGE]
- Integration : [REST_ASSURED, TESTCONTAINERS]
- E2E : [SELENIUM_GRID, CYPRESS, PLAYWRIGHT]
- Performance : [JMETER, GATLING, K6]
- Security : [OWASP_ZAP, BURP_SUITE]

QUALITY GATES :
- Code quality : [SONARQUBE, CODECLIMATE]
- Security scanning : [SNYK, BLACKDUCK, CHECKMARX]
- Performance baselines : [RESPONSE_TIME_THRESHOLDS]
- Coverage minimums : [BRANCH_COVERAGE_TARGETS]

GESTION DES DONNÉES DE TEST :
- Test data management : [DATA_FACTORIES, FIXTURES]
- Data isolation : [DATABASE_SANDBOXES, API_MOCKING]
- Data generation : [RANDOM_DATA, EDGE_CASES]
- Data cleanup : [AUTOMATED_TEARDOWN, STATE_RESET]

MONITORING ET ANALYTICS :
METRICS DE QUALITÉ :
- Test coverage trends
- Flaky test detection
- Test execution times
- Failure patterns analysis

DASHBOARDS ET REPORTING :
- Real-time dashboards : [GRAFANA, KIBANA]
- Test reports : [ALLURE, EXTENT_REPORTS]
- Trend analysis : [HISTORICAL_PERFORMANCE]
- Stakeholder communication : [EXECUTIVE_SUMMARIES]

CONTINUOUS IMPROVEMENT :
TEST EVOLUTION :
- New test case identification
- Test maintenance automation
- Performance optimization
- False positive reduction

TEAM DYNAMICS :
- Test ownership distribution
- Knowledge sharing sessions
- Pair testing practices
- Community of practice

INNOVATION TESTING :
- Exploratory testing sessions
- AI-assisted test generation
- Visual regression testing
- Accessibility testing automation

SCALING ET MAINTENANCE :
ARCHITECTURE ÉVOLUTIVE :
- Test microservices
- Shared test libraries
- Service virtualization
- Cross-team test coordination

COST OPTIMIZATION :
- Cloud cost management
- Test execution optimization
- Maintenance effort reduction
- ROI measurement and tracking

GOVERNANCE ET COMPLIANCE :
- Test standards enforcement
- Regulatory compliance testing
- Audit trails maintenance
- Quality assurance processes
```

## 🎯 Templates Spécialisés

### Template Tests API RESTful

```
Crée une suite complète de tests API pour [API_REST] avec [FRAMEWORK_TEST].

SPÉCIFICATION API :
- Endpoints : [LISTE_URLS_AVEC_MÉTHODES]
- Authentification : [BEARER_TOKEN, API_KEY, OAUTH]
- Format données : [JSON, XML, FORM_DATA]

CATÉGORIES DE TESTS :
FONCTIONNELS :
- CRUD operations : POST, GET, PUT, DELETE
- Status codes validation (200, 201, 400, 401, 404, 500)
- Response schema validation
- Business rules enforcement

SÉCURITÉ :
- Authentication bypass attempts
- Authorization level validation
- Input validation (SQL injection, XSS)
- Rate limiting testing
- CORS configuration

PERFORMANCE :
- Response time under normal load
- Concurrent user simulation
- Memory leak detection
- Timeout handling

INTEGRATION :
- Database state changes
- External service dependencies
- Message queue interactions
- Cache invalidation

INFRASTRUCTURE DE TEST :
- Base URL configuration
- Test data setup/teardown
- Authentication token management
- Response assertion helpers

RAPPORTS ET MONITORING :
- Test execution results
- Coverage reports
- Performance metrics
- Failure analysis
```

### Template Tests Performance et Charge

```
Développe une stratégie de tests de performance pour [APPLICATION] supportant [CHARGE_CIBLE].

OBJECTIFS DE PERFORMANCE :
- Utilisateurs simultanés : [NOMBRE_CIBLE]
- Temps de réponse : < [LATENCE_MAX]ms
- Throughput : [REQUÊTES/SECONDE_CIBLE]
- Disponibilité : [UPTIME_CIBLE]%

SCÉNARIOS DE TEST :
CHARGE NORMALE :
- Utilisateurs : [X] concurrents
- Durée : [Y] minutes
- Assertions : [MÉTRIQUES_CIBLES]

PIC DE CHARGE :
- Utilisateurs : [X*3] concurrents
- Durée : [Z] minutes
- Assertions : [COMPORTEMENT_ATTENDU]

STRESS TESTING :
- Utilisateurs : [PROGRESSIF_JUSQU'À_LIMITE]
- Monitoring : [RESSOURCES_SYSTÈME]
- Breakpoint identification

ENDURANCE TESTING :
- Charge constante : [X] utilisateurs
- Durée : [24H+] heures
- Monitoring : [MEMORY_LEAKS, PERFORMANCE_DEGRADATION]

OUTILS ET INFRASTRUCTURE :
- Load generators : [JMETER, GATLING, K6]
- Monitoring : [PROMETHEUS, DATADOG, NEW_RELIC]
- Infrastructure : [AWS, GCP, AZURE_LOAD_TESTING]
- Reporting : [HTML_REPORTS, METRICS_DASHBOARDS]

ANALYSE DES RÉSULTATS :
- Performance bottlenecks identification
- Scaling recommendations
- Infrastructure optimization
- Code profiling insights

RECOMMANDATIONS D'OPTIMISATION :
- Database query optimization
- Caching strategy implementation
- CDN integration
- Horizontal scaling configuration
```

### Template Tests Sécurité Automatisés

```
Implémente des tests de sécurité automatisés pour [APPLICATION] selon [STANDARD_SÉCURITÉ].

STANDARDS APPLIQUÉS :
- OWASP Top 10 2021
- CIS Controls
- NIST Cybersecurity Framework
- Industry-specific regulations

CATÉGORIES DE TESTS :
AUTHENTIFICATION :
- Password policy enforcement
- Multi-factor authentication
- Session management security
- Brute force protection

AUTORISATION :
- Role-based access control (RBAC)
- Least privilege principle
- API endpoint authorization
- Data-level security

VALIDATION DES DONNÉES :
- Input sanitization
- SQL injection prevention
- Cross-site scripting (XSS) protection
- Command injection blocking

GESTION DES SESSIONS :
- Session fixation prevention
- Secure cookie configuration
- Session timeout enforcement
- Concurrent session control

CRYPTAGE :
- Data at rest encryption
- Data in transit (TLS 1.3)
- Key management security
- Hashing algorithm validation

INFRASTRUCTURE SÉCURITÉ :
- Firewall configuration
- Intrusion detection
- Log security monitoring
- Backup security validation

OUTILS D'AUTOMATISATION :
- DAST : [OWASP_ZAP, BURP_SUITE, NESSUS]
- SAST : [SONARQUBE, CHECKMARX, VERACODE]
- Container security : [TRIVY, CLAIR, FALCO]
- Infrastructure : [TERRAFORM_SECURITY, CLOUDFORMATION_GUARD]

INTÉGRATION CI/CD :
- Security gates : [FAIL_BUILD_ON_VULNERABILITIES]
- Automated scanning : [EVERY_COMMIT, DAILY, WEEKLY]
- Compliance reporting : [AUDIT_TRAILS, COMPLIANCE_DASHBOARDS]
- Remediation tracking : [VULNERABILITY_MANAGEMENT_SYSTEM]

RECOMMANDATIONS DE REMÉDIATION :
- Prioritized vulnerability fixes
- Security hardening procedures
- Training and awareness programs
- Incident response improvements
```

## 📊 Métriques de Qualité des Tests

### Couverture et Efficacité

| Métrique | Excellent | Bon | À Améliorer |
|----------|-----------|-----|-------------|
| **Coverage Unit** | > 85% | 70-85% | < 70% |
| **Coverage Integration** | > 60% | 40-60% | < 40% |
| **Coverage E2E** | > 30% | 15-30% | < 15% |
| **Test Execution Time** | < 15 min | 15-45 min | > 45 min |
| **Flaky Tests Rate** | < 1% | 1-5% | > 5% |
| **Defect Leakage** | < 5% | 5-15% | > 15% |

### Maintenance et Évolutivité

| Aspect | Bonnes Pratiques | Indicateurs Succès |
|--------|------------------|-------------------|
| **Test Code Quality** | DRY principle, readable names | Code review approvals > 95% |
| **Data Management** | Isolated test data, automated cleanup | No test data conflicts |
| **CI/CD Integration** | Automated pipelines, fast feedback | Deployment frequency > daily |
| **Team Collaboration** | Shared libraries, documentation | Knowledge sharing sessions |
| **Evolution** | Refactoring, new test addition | Test debt < 10% codebase |

### ROI des Tests Automatisés

**Calcul du Retour sur Investissement** :
```
ROI = (Économies_tests_manuels + Prévention_défauts + Accélération_livraison) / Coût_automatisation
```

**Économies Typiques** :
- Tests de régression : 80% temps économisé
- Débogage production : 60% réduction incidents
- Time-to-market : 40% accélération
- Qualité perçue : +25% satisfaction client

Ces templates constituent votre arsenal complet pour implémenter des stratégies de test robustes, automatisées et maintenables, garantissant la qualité et la fiabilité de vos applications à toutes les échelles.
