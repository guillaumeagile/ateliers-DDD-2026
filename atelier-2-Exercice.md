# Atelier DDD - part 2 – CRM Job

## Event Modelling - Domain Message Flow Modelling


pour repartir sur le vaste domaine que nous avons entrevu à la session précédente, 
nous allons élargir notre champ d'observation en développant une vision globale du domaine métier.

# 🧭 Cartographie des bounded contexts – périmètre élargi (FR)

## 1️⃣ Domaine Intention & Projet Professionnel

*Pourquoi je cherche, vers quoi, avec quelles priorités*

1. **Projet professionnel**
2. **Objectifs de carrière**
3. **Positionnement du candidat**
4. **Compétences & savoir‑faire**
5. **Évolution & reconversion professionnelle**

---

## 2️⃣ Domaine Marché & Opportunités

*Ce que le marché propose, indépendamment de l’action du candidat*

1. **Découverte d’opportunités**
2. **Veille du marché de l’emploi**
3. **Offres & opportunités informelles**
4. **Entreprises & organisations**
5. **Attractivité employeur**

---

## 3️⃣ Domaine Candidatures & Sélection

*Interaction formelle entre le candidat et une opportunité*

1. **Candidatures**
2. **Processus de recrutement**
3. **Étapes de sélection**
4. **Entretiens & évaluations**
5. **Décisions & issues de candidature**

---

## 4️⃣ Domaine Interaction & Exécution

*Ce que le candidat fait concrètement au quotidien*

1. **Communication avec les recruteurs**
2. **Relances & suivis**
3. **Organisation personnelle**
4. **Planification & gestion du temps**
5. **Gestion documentaire**

---

## 5️⃣ Domaine Décision & Arbitrage

*Comparer, choisir, renoncer*

1. **Évaluation des opportunités**
2. **Comparaison des offres**
3. **Critères de décision**
4. **Négociation & conditions**

---

## 6️⃣ Domaine Analyse & Amélioration Continue

*Comprendre ce qui fonctionne, ajuster sa stratégie*

1. **Suivi de la performance**
2. **Analyse des candidatures**
3. **Apprentissage et ajustement**
4. **Historique et traçabilité du parcours**

---

## 7️⃣ Domaine Humain & Expérience Personnelle

*Ce que vit réellement le chercheur d’emploi*

1. **Motivation & engagement**
2. **Stress & charge mentale**
3. **Bien‑être du candidat**
4. **Journal de recherche d’emploi**

---

## 8️⃣ Domaines transverses / intermédiaires

*Zones de chevauchement assumées, très utiles pour un produit large*

1. **Pipeline de recherche d’emploi**
2. **Parcours candidat (timeline)**
3. **Réseau professionnel**
4. **Relations recruteurs & contacts**
5. **Vision globale & pilotage**

---

# ✅ Pourquoi cette liste est un outil de travail pour l’équipe DDD

Cette cartographie des bounded contexts n’est pas seulement un support de cadrage ou de communication.  
Elle constitue avant tout **un outil de travail central pour un atelier DDD (Domain‑Driven Design)**.

## 🎯 Objectif dans un atelier DDD

- chaque **bounded context** sert de cadre explicite de réflexion
- les participants sont invités à **établir un glossaire métier propre à chaque contexte**

👉 L’objectif n’est **pas** d’unifier immédiatement le vocabulaire, mais de **faire émerger les différences**.

---

## 📘 Travail sur les glossaires métiers par bounded context

Pour chaque bounded context :

- lister les **termes métiers clés**
- décrire leur **signification précise**
- identifier :
    - règles métier
    - ambiguïtés
    - synonymes ou faux amis

Exemples de termes ambigus :
- *Opportunité*
- *Candidature*
- *Relation*
- *Feedback*
- *Pipeline*

---

## 🔄 Mise en commun des glossaires

- comparaison inter‑contextes
- identification :
    - des recouvrements réels
    - des faux amis
    - des divergences de concepts

👉 Le **modèle de domaine émerge à partir du langage**.

---

## 📖 Rappel : l’Ubiquitous Language (Eric Evans)

*L’Ubiquitous Language est un langage commun, partagé par les experts métier et les développeurs, utilisé de manière cohérente dans les conversations, les documents et le code, à l’intérieur d’un bounded context.*

- contextuel
- évolutif
- co‑construit




## 🎯 Enseignements

- même mot ≠ même concept
- relations sémantiques avant techniques
- décisions DDD guidées par le langage



---

## 🧾 Template de glossaire métier par bounded context

### Informations générales
- Nom du bounded context
- Objectif métier
- Participants
- Date / version

### Terme

- **Définition dans ce contexte**
- **Règles métier associées**
- **Synonymes**
- **Termes proches mais différents**
- **Ce que ce terme n’est pas**
- **Événements métier associés**
- **Notes / questions ouvertes**

### Points de vigilance inter‑contextes
- existe ailleurs ?
- même mot, sens différent ?
- relation pressentie :
    - Shared Kernel
    - Upstream / Downstream
    - Anti‑Corruption Layer

---

## 🗺️ Légende des relations entre bounded contexts (DDD)

Cette légende est un **outil pédagogique et opérationnel** pour analyser les relations **à partir du langage métier**.

---

## 🔼 Upstream

Contexte **producteur** du langage ou des règles métier.

- fait autorité
- influence les autres
- guidé par ses priorités métier

Questions :
- où est la vérité métier ?
- qui décide du vocabulaire ?

Risques :
- langage imposé
- concepts mal compris

---

## 🔽 Downstream

Contexte **consommateur**.

- dépend d’un autre contexte
- subit les changements
- nécessite parfois une protection

Risques :
- couplage fort
- fragilité du modèle local

---

## 🤝 Conformist

Alignement volontaire sur un upstream.

Pertinent si :
- domaine non stratégique
- vitesse > autonomie

À éviter si :
- règles métier spécifiques
- perte de clarté du langage

---

## 🔗 Shared Kernel

Petit noyau de concepts réellement communs.

- coordination forte
- évolution synchronisée

Anti‑pattern :
- kernel trop large
- mini‑monolithe partagé

---

## 🛡️ Anti‑Corruption Layer (ACL)

Barrière conceptuelle protégeant le langage local.

Indispensable si :
- mêmes mots, sens différents
- règles incompatibles
