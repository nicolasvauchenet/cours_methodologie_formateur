# Rapport de présentation - Projet d'évaluation UML

## Introduction

Le projet consiste à modéliser un système de gestion pour le festival de musique **Rock'N Waves** en utilisant les
principes de modélisation UML. Ce système doit couvrir plusieurs domaines fonctionnels essentiels pour assurer le bon
déroulement du festival. Chaque domaine sera illustré à travers une série de diagrammes UML pour mettre en lumière les
fonctionnalités métier et logicielles associées. Le rapport présente également une description détaillée des
fonctionnalités modélisées.

---

## 1. Programmation et horaires des artistes

### 1.1 Fonctionnalités métier

- Gestion des créneaux horaires des artistes.
- Attributions des artistes aux scènes (grande et petite scène).
- Coordination des horaires pour éviter les conflits.
- Notification des artistes et équipes techniques.
- Suivi des performances.

### 1.2 Fonctionnalités logicielles

- Gestion des entités Artiste et Performance.
- Authentification et autorisation pour accéder aux fonctionnalités de gestion des créneaux.
- Gestion des horaires via une base de données relationnelle.
- Validation des conflits d’horaires.

### 1.3 Diagrammes UML

#### Diagramme de cas d'utilisation

![1.3.1 - Diagramme de Cas d'Utilisation-1_3_1___Diagramme_de_Cas_d_Utilisation___Programmation_des_artistes.png](1.3.1%20-%20Diagramme%20de%20Cas%20d%27Utilisation-1_3_1___Diagramme_de_Cas_d_Utilisation___Programmation_des_artistes.png)

#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


---

## 2. Accueil et services aux artistes

### 2.1 Fonctionnalités métier

- Gestion de l'hébergement des artistes.
- Coordination des transports pour les déplacements des artistes.
- Gestion des services de catering.
- Suivi des demandes spécifiques des artistes.

### 2.2 Fonctionnalités logicielles

- Gestion des entités Artiste, Hébergement, Transport.
- Authentification et autorisation pour l’accès à la gestion des services.
- Gestion des réservations d’hébergement et de transport via une base de données.
- Suivi et validation des demandes.

### 2.3 Diagrammes UML

#### Diagramme de cas d'utilisation


#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


---

## 3. Logistique du festival

### 3.1 Fonctionnalités métier

- Gestion du matériel nécessaire pour les performances (instruments, éclairage, sonorisation).
- Coordination des équipes techniques (son, lumière).
- Gestion des équipes de sécurité.
- Organisation et gestion des bénévoles.

### 3.2 Fonctionnalités logicielles

- Gestion des entités Matériel, Équipe technique, Bénévoles.
- Gestion des plannings des équipes via une base de données.
- Authentification et autorisation pour la gestion des ressources.
- Validation des affectations de matériel et des équipes sur les scènes.

### 3.3 Diagrammes UML

#### Diagramme de cas d'utilisation


#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


---

## 4. Communication et publicité

### 4.1 Fonctionnalités métier

- Gestion des campagnes publicitaires.
- Promotion des artistes et des événements.
- Communication avec les festivaliers (newsletters, réseaux sociaux).
- Suivi de l'impact des campagnes publicitaires.

### 4.2 Fonctionnalités logicielles

- Gestion des entités Campagne publicitaire, Newsletter, Artistes.
- Authentification pour accéder aux outils de gestion de campagne.
- Automatisation de l'envoi de newsletters et publications sur les réseaux sociaux.
- Stockage des données relatives aux interactions des festivaliers avec les campagnes.

### 4.3 Diagrammes UML

#### Diagramme de cas d'utilisation


#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


---

## 5. Gestion de la billetterie et services sur site

### 5.1 Fonctionnalités métier

- Vente de billets en ligne et sur place.
- Gestion des points d'accès et de validation des billets.
- Suivi des ventes de billets en temps réel.
- Gestion des services proposés aux visiteurs (restauration, stands de produits dérivés).

### 5.2 Fonctionnalités logicielles

- Gestion des entités Billet, Point d'accès, Service sur site.
- Intégration d'un module de paiement sécurisé.
- Authentification pour l’administration de la billetterie.
- Suivi des statistiques de vente via un tableau de bord.

### 5.3 Diagrammes UML

#### Diagramme de cas d'utilisation


#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


---

## 6. Gestion des budgets et des ressources

### 6.1 Fonctionnalités métier

- Suivi des dépenses (cachets des artistes, location de matériel).
- Suivi des recettes (vente de billets, merchandising).
- Gestion des ressources humaines (bénévoles, techniciens, personnel administratif).
- Optimisation de l'utilisation des ressources.

### 6.2 Fonctionnalités logicielles

- Gestion des entités Dépense, Recette, Ressources humaines.
- Authentification pour accéder aux fonctionnalités de gestion des budgets.
- Validation des transactions financières.
- Suivi des budgets via une base de données relationnelle.

### 6.3 Diagrammes UML

#### Diagramme de cas d'utilisation


#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


---

## 7. Sécurité et gestion des urgences

### 7.1 Fonctionnalités métier

- Déploiement des agents de sécurité sur le site.
- Gestion des accès et surveillance des zones critiques.
- Planification des mesures d'urgence (évacuations, incidents techniques).
- Coordination des équipes de premiers secours.

### 7.2 Fonctionnalités logicielles

- Gestion des entités Sécurité, Zone d'accès, Incident.
- Authentification pour l’accès aux fonctionnalités de gestion des urgences.
- Suivi et validation des incidents signalés.
- Intégration des communications avec les équipes d'urgence.

### 7.3 Diagrammes UML

#### Diagramme de cas d'utilisation


#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


---

## 8. Gestion des partenariats et sponsors

### 8.1 Fonctionnalités métier

- Coordination avec les sponsors.
- Suivi des engagements contractuels avec les sponsors.
- Gestion de la visibilité accordée aux partenaires (affiches, stands, présence en ligne).
- Suivi des contreparties offertes aux sponsors.

### 8.2 Fonctionnalités logicielles

- Gestion des entités Sponsor, Contrat, Contrepartie.
- Authentification pour accéder aux fonctionnalités de gestion des contrats de partenariat.
- Suivi et validation des contreparties offertes via un tableau de bord.
- Intégration avec les outils de communication pour la visibilité des sponsors.

### 8.3 Diagrammes UML

#### Diagramme de cas d'utilisation


#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


---

## 9. Analyse des performances et retours d'expérience

### 9.1 Fonctionnalités métier

- Collecte des retours d'expérience des festivaliers.
- Analyse des performances des artistes et de l'organisation.
- Suivi des indicateurs de satisfaction.
- Génération de rapports post-événement.

### 9.2 Fonctionnalités logicielles

- Gestion des entités Retour d'expérience, Indicateur de satisfaction, Rapport.
- Authentification pour accéder aux outils d’analyse des performances.
- Stockage et traitement des données relatives aux retours des festivaliers.
- Génération automatique des rapports via des tableaux de bord.

### 9.3 Diagrammes UML

#### Diagramme de cas d'utilisation


#### Diagramme d'activité


#### Diagramme de séquence


#### Diagramme de classes


#### Modèle entité-relation


## 10. Diagrammes UML globaux

#### Diagramme de classes global


#### Modèle entité-relation global


---

## Conclusion

Le système modélisé couvre les principaux besoins fonctionnels du festival **Rock'N Waves**. Chaque domaine, de la
programmation des artistes à la gestion des sponsors, est soutenu par des diagrammes UML qui illustrent clairement la
structure, les processus et les interactions clés. Le système proposé est flexible, évolutif et conçu pour répondre aux
besoins immédiats du festival tout en étant capable de s'adapter aux futures éditions.

Pour une application de cette envergure, qui doit gérer plusieurs domaines fonctionnels tels que la billetterie, la
logistique, la sécurité, les partenariats, et l'analyse des performances, une architecture modulaire, scalable et
maintenable est essentielle. Voici quelques suggestions d'architectures qui conviendraient, avec leurs avantages et
inconvénients.

### Architecture Hexagonale (Ports and Adapters)

L’architecture hexagonale, aussi appelée architecture Ports and Adapters, est une approche bien adaptée à cette
application car elle sépare les préoccupations métiers du système des couches techniques (infrastructure, interfaces
utilisateur).

#### Caractéristiques :

- **Domain-Centric :** Le cœur du système est constitué par la logique métier (gestion des artistes, billetterie,
  logistique, etc.). Les autres couches (interfaces, bases de données, services externes) se connectent à ce noyau via
  des adaptateurs (ports).
- **Flexibilité :** Les interfaces utilisateurs, les bases de données ou les systèmes externes peuvent être changés sans
  impacter la logique métier.
- **Tests :** Cette architecture facilite le testing unitaire des domaines métiers, car les dépendances externes sont
  isolées.

#### Structure :

- **Domaine :** Toute la logique métier, y compris les entités et services (ex. : gestion des artistes, gestion des
  budgets).
- **Ports :** Interfaces définissant ce que le domaine attend des services externes (ex. : interface pour envoyer des
  notifications ou gérer des paiements).
- **Adaptateurs :** Implémentations concrètes des ports, par exemple un service de paiement tiers, une API de gestion
  des performances, ou une base de données.
- **Application :** Les orchestrateurs qui coordonnent les opérations métiers (par exemple, la gestion des transactions
  de billetterie ou l'attribution des créneaux aux artistes).

#### Avantages :

- **Séparation des préoccupations :** Les différentes couches sont bien séparées, facilitant l'évolution et la
  maintenance du code.
- **Flexibilité technologique :** Les technologies peuvent être facilement changées ou mises à jour (ex. : changer de
  service de paiement ou d'API sans impacter le reste du système).
- **Testabilité :** Les tests unitaires et d'intégration sont simplifiés grâce à l'isolation des dépendances externes.

#### Inconvénients :

- **Complexité initiale :** La mise en place de cette architecture peut nécessiter un investissement initial plus élevé
  en raison de la séparation des couches et de la configuration des adaptateurs.

### Architecture Microservices

Une architecture microservices peut également être envisagée si l'application nécessite une grande scalabilité et des
équipes indépendantes travaillant sur différents modules.

#### Caractéristiques :

- **Modularité extrême :** Chaque fonctionnalité majeure (billetterie, logistique, analyse des performances, sécurité)
  est encapsulée dans un service indépendant avec sa propre base de données.
- **Indépendance des services :** Les services peuvent être développés, déployés et scalés indépendamment.
- **Communication via API :** Les services communiquent via des API (REST, gRPC) ou des événements asynchrones (pub/sub,
  message brokers).

#### Structure :

- **Services indépendants :** Chaque domaine (billetterie, sécurité, logistique, partenariats, etc.) devient un
  microservice.
- **API Gateway :** Un point d'entrée centralisé pour gérer la communication entre les clients (interface utilisateur)
  et les services.
- **Base de données dédiée :** Chaque microservice possède sa propre base de données, ce qui améliore l'autonomie des
  services.

#### Avantages :

- **Scalabilité :** Les services critiques (comme la billetterie) peuvent être mis à l'échelle indépendamment des
  autres.
- **Résilience :** Un service défaillant n'affecte pas les autres services.
- **Indépendance technologique :** Chaque service peut être développé avec des technologies différentes (par exemple, la
  billetterie en Node.js et la logistique en Symfony).

#### Inconvénients :

- **Complexité de l'orchestration :** La gestion des microservices (communication, déploiement, monitoring) peut devenir
  complexe, nécessitant des outils comme Kubernetes ou des services de gestion de conteneurs.
- **Latence et fiabilité :** Les microservices introduisent de la latence dans les appels API, et la gestion des erreurs
  devient plus complexe.
