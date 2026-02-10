# Série "Le Produit Agile : de l'Idéation à la Livraison"

**6 ateliers hands-on de 2h pour maîtriser DDD de bout en bout**

---

## **Atelier 1 : Aligner & Découvrir le domaine** (2h)
**Focus DDD : Understand + Discover**

### Understand - Comprendre le business (30min)
- **Impact Mapping** : Pourquoi ce produit ? Pour qui ? Quel impact business attendu ?
- Identification de l'objectif, des acteurs, des impacts et des livrables
- Alignement sur la vision produit

### Discover - Event Storming Big Picture (1h20)
- Exploration collaborative du domaine métier
- Brainstorming des événements métier sur une timeline
- Identification des hot spots, zones de complexité et opportunités
- Émergence des bounded contexts candidats

### Synthèse (10min)
- Sélection du périmètre prioritaire pour la suite

**Outils PO** : Impact Mapping, Event Storming  
**Livrables** : Impact Map + Timeline Event Storm avec hot spots identifiés

---

## **Atelier 2 : Modéliser les processus** (2h)
**Focus DDD : Discover (Process Level) avec Event Modelling**

### Event Modelling - Process Level (1h40)
- Approfondissement du périmètre sélectionné
- Ajout des **commandes** (intentions utilisateur)
- Identification des **Read Models** (vues/écrans nécessaires)
- Modélisation des **états** du système et leurs transitions
- Acteurs et leurs interactions avec le système
- Wireframes légers des interfaces clés

### Validation & Ajustements (20min)
- Passage en revue des scénarios critiques
- Identification des points à clarifier

**Outils PO** : Event Modelling  
**Livrable** : Modèle événementiel complet avec commandes, événements et read models

---

## **Atelier 3 : Décomposer & Prioriser** (2h)
**Focus DDD : Decompose + Strategize**

### Decompose - Découper en sous-domaines (1h)
- Identification des sous-domaines à partir de l'Event Modelling
- Application des heuristics de découpage (cohésion/couplage)
- Définition des frontières et responsabilités
- Langage ubiquitaire par sous-domaine

### Strategize - Core Domain Chart (50min)
- Classification des sous-domaines :
  - **Core** : différenciation business
  - **Supporting** : nécessaire mais pas différenciant
  - **Generic** : commodité
- Priorisation stratégique
- Décisions Build / Buy / Partner

### Synthèse (10min)
- Roadmap stratégique des sous-domaines

**Outils PO** : Design Heuristics, Core Domain Chart  
**Livrable** : Carte des sous-domaines + Core Domain Chart avec stratégie

---

## **Atelier 4 : Connecter & Cartographier** (2h)
**Focus DDD : Connect + Organise**

### Connect - Domain Message Flow (1h10)
- Modélisation des flux de messages entre sous-domaines/contextes
- Identification des interactions et dépendances
- Séquencement des événements inter-contextes
- Validation avec des scénarios end-to-end concrets

### Context Map - Relations entre contextes (30min)
- Cartographie des relations entre bounded contexts
- Patterns de collaboration : 
  - Partnership, Shared Kernel
  - Customer/Supplier, Conformist
  - Anti-Corruption Layer, Open Host Service
- Identification des équipes et responsabilités

### Synthèse (20min)
- Validation de l'architecture distribuée

**Outils PO** : Domain Message Flow, Context Map  
**Livrable** : Diagrammes de flux + Context Map avec patterns de collaboration

---

## **Atelier 5 : Organiser & Spécifier** (2h)
**Focus DDD : Organise + Define avec spécifications exécutables**

### User Story Mapping (1h)
- Organisation des fonctionnalités selon le parcours utilisateur
- Backbone (activités principales) et user stories
- Découpage en releases : MVP, puis incréments de valeur
- Priorisation par valeur/effort
- Visualisation des dépendances entre stories

### Define - Bounded Context Canvas (35min)
- Définition détaillée du ou des contextes prioritaires
- Responsabilités, inbound/outbound, décisions de conception
- Langage ubiquitaire explicite

### Spécifications exécutables - Gherkin/BDD (20min)
- Introduction au format Given/When/Then
- Transformation de 2-3 User Stories en scénarios .feature
- Focus sur le langage métier

### Préparation atelier 6 (5min)

**Outils PO** : User Story Mapping, Bounded Context Canvas, Gherkin  
**Livrable** : Story Map avec releases + Bounded Context Canvas + Premiers fichiers .feature

---

## **Atelier 6 : Spécifications tactiques & Code IA** (2h)
**Focus DDD : Define (tactique) + Code**

### Design tactique & Spécifications complètes (50min)
- Identification des **agrégats** et leurs invariants
- Définition des **Entities** vs **Value Objects**
- **Domain Events** détaillés
- Règles métier et politiques
- Complétion des fichiers **.feature** pour les stories MVP
  - Scénarios nominaux
  - Cas limites et erreurs
  - Règles métier en Given/When/Then

### Génération de code AI-assistée (1h)
- Génération des step definitions depuis les fichiers .feature
- Implémentation du domain model guidée par les tests BDD
- Génération de l'API (REST/GraphQL)
- Génération automatique des tests
- Optionnel : génération d'un frontend simple
- **Validation : les specs .feature passent au vert ✅**

### DevOps & Déploiement (10min)
- Configuration rapide du pipeline CI/CD
- Déploiement en pré-production
- Démonstration live

**Outils** : Aggregate Design Canvas, Gherkin, Claude/ChatGPT/Copilot, GitHub Actions  
**Livrable** : Application fonctionnelle en pré-production + tests BDD passants

---

## 🎯 Correspondance avec le DDD Starter Modelling Process

| Atelier | Étapes du processus DDD |
|---------|------------------------|
| 1 | **Understand** + **Discover** (Big Picture) |
| 2 | **Discover** (Process Level) |
| 3 | **Decompose** + **Strategize** |
| 4 | **Connect** + **Organise** |
| 5 | **Organise** (User Stories) + **Define** (Bounded Context) |
| 6 | **Define** (Tactical) + **Code** |

---

## 🛠️ Boîte à outils pour Product Owners

**Stratégie & Vision**
- Impact Mapping (Atelier 1)
- Core Domain Chart (Atelier 3)

**Découverte & Modélisation**
- Event Storming Big Picture (Atelier 1)
- Event Modelling (Atelier 2)
- Domain Message Flow (Atelier 4)

**Organisation & Planification**
- User Story Mapping (Atelier 5)
- Context Map (Atelier 4)
- Bounded Context Canvas (Atelier 5)

**Spécifications & Tests**
- Gherkin/BDD - Spécifications exécutables (Ateliers 5 & 6)
- Scenarios Given/When/Then en langage métier

---

## 🔗 Le fil rouge : des spécifications exécutables

Les **fichiers .feature en Gherkin** créent le pont entre :

✅ **Le langage métier** des Product Owners (compréhensible, collaboratif)  
✅ **Les tests automatisés** pour les développeurs (exécutables, validation continue)  
✅ **La documentation vivante** toujours à jour avec le code  

**Bénéfice clé** : Les POs peuvent continuer à enrichir les `.feature` après les ateliers, et les développeurs les utilisent comme contrat d'implémentation. C'est la "Definition of Done" partagée.

---

## 📋 Informations pratiques

**Durée** : 6 ateliers de 2h (12h au total)  
**Format** : Hands-on, collaboratif, avec des outils visuels  
**Participants** : 8-15 personnes (mix PO, développeurs, domain experts)  
**Matériel** : 
- Ateliers 1-5 : Post-its, tableaux ou Miro/Mural
- Atelier 6 : Laptops, accès IA (Claude/GPT), GitHub, cloud platform

**Rythme recommandé** : 1 atelier par semaine ou tous les 15 jours pour laisser le temps d'assimilation

**Pré-requis** : Aucun ! Ouvert aux débutants en DDD

---

## 🎓 Ce que vous saurez faire à l'issue de la série

✅ Aligner une équipe sur la vision business avec Impact Mapping  
✅ Explorer et modéliser un domaine métier complexe  
✅ Identifier les sous-domaines et prioriser stratégiquement  
✅ Concevoir une architecture distribuée avec Context Mapping  
✅ Planifier un produit avec User Story Mapping  
✅ Écrire des spécifications exécutables en Gherkin  
✅ Générer du code production-ready avec l'aide de l'IA  
✅ Déployer une application en pré-production  

**Le tout avec une approche pragmatique et des outils réutilisables immédiatement !**

---

## 🚀 Pour aller plus loin

Après ces ateliers, vous serez autonomes pour :
- Répéter le processus sur vos propres projets
- Adapter les outils à votre contexte
- Approfondir les patterns DDD tactiques et stratégiques
- Pratiquer le Test-Driven Development avec BDD

**Bienvenue dans l'aventure DDD ! 🎉**

---

## 📚 Ressources

### Références DDD Starter Modelling Process
- [DDD Starter Modelling Process](https://github.com/ddd-crew/ddd-starter-modelling-process)
- [DDD Crew - Ressources collaboratives](https://github.com/ddd-crew)

### Outils et Canvas
- [Bounded Context Canvas](https://github.com/ddd-crew/bounded-context-canvas)
- [Context Mapping](https://github.com/ddd-crew/context-mapping)
- [Core Domain Charts](https://github.com/ddd-crew/core-domain-charts)
- [Domain Message Flow Modelling](https://github.com/ddd-crew/domain-message-flow-modelling)
- [Aggregate Design Canvas](https://github.com/ddd-crew/aggregate-design-canvas)

### Livres essentiels
- "Domain-Driven Design" - Eric Evans
- "Implementing Domain-Driven Design" - Vaughn Vernon
- "Domain-Driven Design Distilled" - Vaughn Vernon
- "Learning Domain-Driven Design" - Vlad Khononov

### Event Storming & Event Modelling
- [EventStorming.com](https://www.eventstorming.com/)
- [EventModeling.org](https://eventmodeling.org/)

### BDD & Gherkin
- [Cucumber](https://cucumber.io/)
- [SpecFlow](https://specflow.org/) (pour .NET)
- [Behave](https://behave.readthedocs.io/) (pour Python)

---

## 👥 Contact

**Organisateur** : Agile Toulouse  
**Site web** : [agiletoulouse.fr](https://agiletoulouse.fr)

---

*Document créé pour Agile Toulouse - Licence Creative Commons BY-SA*
