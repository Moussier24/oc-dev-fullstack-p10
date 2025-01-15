# Documentation Technique BobApp

## 1. Pipeline CI/CD

### 1.1 Backend Pipeline

#### Tests et Couverture
- Exécution des tests unitaires avec JUnit
- Génération des rapports de couverture avec JaCoCo
- Stockage des résultats des tests comme artefacts

#### Analyse de Code
- Scan SonarCloud pour la qualité du code
- Vérification des standards de code
- Détection des vulnérabilités

#### Déploiement
- Build de l'image Docker
- Push vers Docker Hub (uniquement sur main)

### 1.2 Frontend Pipeline

#### Tests et Couverture
- Tests unitaires avec Karma/Jasmine
- Génération des rapports de couverture
- Stockage des résultats comme artefacts

#### Analyse de Code
- Scan SonarCloud pour la qualité du code
- Vérification des standards TypeScript/Angular
- Détection des vulnérabilités

#### Déploiement
- Build de l'image Docker
- Push vers Docker Hub (uniquement sur main)

## 2. KPIs et Seuils Proposés

### 2.1 Couverture de Code
- Backend : minimum 80%
- Frontend : minimum 80%
Justification : Une bonne couverture de tests est essentielle pour détecter les régressions et maintenir la qualité du code.

### 2.2 Dette Technique
- Maximum 5 jours
Justification : Limiter l'accumulation de problèmes techniques qui pourraient ralentir les développements futurs.

### 2.3 Autres Métriques Importantes
- Bugs bloquants : 0
- Vulnérabilités critiques : 0
- Code smells : < 100 par projet

## 3. Analyse des Métriques Actuelles

### 3.1 Backend
[Voir le rapport complet](https://sonarcloud.io/project/overview?id=moussier24_ocp10-back)
- Couverture de tests : 45%
- Dette technique : 8 jours
- Bugs : 12
- Vulnérabilités : 3
- Code smells : 156

### 3.2 Frontend
[Voir le rapport complet](https://sonarcloud.io/project/overview?id=moussier24_ocp10-front)
- Couverture de tests : 38%
- Dette technique : 6 jours
- Bugs : 8
- Vulnérabilités : 2
- Code smells : 124

Les métriques sont mises à jour automatiquement à chaque exécution du pipeline CI/CD et sont disponibles dans les résumés des actions GitHub. Pour une analyse détaillée et des tendances historiques, consultez les rapports SonarCloud liés ci-dessus.

## 4. Analyse des Retours Utilisateurs

### 4.1 Points Critiques
1. "L'application plante régulièrement lors de l'affichage des blagues"
   - Impact : Élevé
   - Priorité : Urgent
   - Solution proposée : Améliorer la gestion des erreurs et le logging

2. "Les temps de chargement sont trop longs"
   - Impact : Moyen
   - Priorité : Haute
   - Solution proposée : Optimiser les requêtes et mettre en place du caching

3. "Pas de nouvelles fonctionnalités depuis longtemps"
   - Impact : Faible
   - Priorité : Basse
   - Solution proposée : Planifier une roadmap de fonctionnalités

## 5. Actions Prioritaires

### 5.1 Court Terme (1-2 mois)
1. Augmenter la couverture de tests (Objectif : 80%)
2. Corriger les bugs bloquants
3. Mettre en place un monitoring des erreurs

### 5.2 Moyen Terme (3-6 mois)
1. Réduire la dette technique
2. Optimiser les performances
3. Améliorer la documentation

## 6. Conclusion

L'analyse révèle plusieurs points d'amélioration urgents, notamment la couverture de tests insuffisante et la présence de bugs critiques. La mise en place de la CI/CD permettra d'améliorer la qualité du code et la rapidité des déploiements, mais des efforts importants sont nécessaires pour atteindre les KPIs proposés. 