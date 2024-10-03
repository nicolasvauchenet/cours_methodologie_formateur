# Correction - TP SCRUM : MyTodo

## Objectif du TP

Dans ce TP, vous deviez appliquer la méthode **SCRUM** pour développer un produit minimum viable (MVP) d'une application
de gestion de tâches appelée **MyTodo**. Voici la correction détaillée de chaque étape.

---

## 01. Le MVP

### Travail à réaliser

- **Définir les rôles et les compétences nécessaires pour réaliser le MVP** :  
  Les rôles principaux à définir sont :
    - **Product Owner** : Responsable de la vision produit, il définit les besoins et priorise les fonctionnalités.
    - **Scrum Master** : Facilite les processus agiles, s'assure que SCRUM est bien appliqué, et aide l'équipe à
      supprimer les obstacles.
    - **Équipe de Développement** : Développeurs full-stack, UI/UX designers, et testeurs QA.

  Les compétences à mobiliser sont :
    - Développeurs full-stack
    - Web designers
    - Testeurs QA
    - DevOps

- **Élaborer le MVP à partir de l'expression des besoins** :  
  Le MVP doit inclure les fonctionnalités minimales suivantes :
    - Création de tâches.
    - Attribution de dates d'échéance.
    - Marquage des tâches comme terminées.
    - Suppression de tâches.
    - Affichage des tâches triées par date d'échéance.

  L'application doit être simple, intuitive, et fonctionner sur appareils mobiles et de bureau.

- **Estimer la durée pour chaque fonctionnalité du MVP** :
    - **Création de tâches** : 10 heures.
    - **Modification de tâches** : 5 heures.
    - **Suppression de tâches** : 5 heures.
    - **Affichage des tâches** : 10 heures.
    - **Système de tri des tâches** : 10 heures.

  **Total** : 40 heures de développement.

### Correction

Vous deviez identifier correctement les rôles et compétences nécessaires. Le MVP devait être simple avec uniquement les
fonctionnalités essentielles, et les estimations devaient être réalistes. La correction évalue si vous avez bien
priorisé les besoins et estimé les tâches avec précision.

---

## 02. Mise en place de SCRUM

### Travail à réaliser

- **Définir les acteurs SCRUM** :
    - **Scrum Master** : Facilite et guide l'équipe dans l'application de SCRUM.
    - **Product Owner** : Définit les priorités et interagit avec les parties prenantes.
    - **Équipe de Développement** : Inclut les développeurs et testeurs qui implémentent les fonctionnalités.

- **Rédiger les User Stories** :
    - **Trier la liste de tâches**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN DE pouvoir trier la liste de mes tâches par nom, statut ou date d'échéance  
          AFIN DE visualiser mes tâches de façon optimale.
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que je suis sur la liste des tâches  
              Quand je clique sur un bouton de tri et que j'ai choisi l'ordre du tri  
              Alors je vois la liste des tâches triées selon le critère choisi.

    - **Priorité des tâches**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN DE pouvoir attribuer une priorité à mes tâches  
          AFIN D'améliorer l'organisation de mon travail.
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que je suis sur la liste de mes tâches  
              Quand je crée ou je modifie une tâche  
              Alors j'ai la possibilité de sélectionner une priorité.

    - **Trier la liste de tâches par priorité**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN DE pouvoir trier la liste de mes tâches par priorité  
          AFIN DE visualiser mes tâches par importance.
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que je suis sur la liste des tâches  
              Quand je clique sur le bouton de tri par priorité et que j'ai choisi l'ordre du tri  
              Alors je vois la liste des tâches triées selon le critère choisi.

    - **Rappels automatiques**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN D'un système de rappels automatiques  
          AFIN DE ne pas oublier mes tâches arrivant à échéance.
        - **Tâches :**
            - Système de vérification des tâches arrivant à échéance
            - Système de messagerie adressable à un utilisateur donné
            - Mise en place du planificateur (CRON)
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que j'ai activé l'option "Rappel automatique"  
              Quand une de mes tâches arrive à échéance  
              Alors je reçois un rappel par e-mail.

    - **Partager une tâche**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN De pouvoir partager mes tâches  
          AFIN DE montrer ma liste de tâches à d'autres utilisateurs.
        - **Tâches :**
            - Ajouter une relation Many-To-Many entre Tâche et Utilisateur, avec un attribut "rôle" = "Partagé"
            - Modifier le formulaire de la tâche pour ajouter la sélection d'un utilisateur et du rôle "Partagé"
            - Modifier la liste des tâches pour ajouter la fonctionnalité de partage
            - Ajouter une page à l'interface présentant les tâches partagées, ajouter une colonne "Propriétaire"
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que je suis en train de créer ou de modifier une tâche  
              Quand je sélectionne un utilisateur et que je lui attribue le rôle "Partagé"  
              Alors cet utilisateur apparaît dans une colonne supplémentaire ("Partagé avec") de ma liste de tâches  
              Alors cet utilisateur voit la tâche dans sa liste de tâches "Partagées avec moi".

    - **Trier la liste de tâches partagées par propriétaire**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN DE pouvoir trier la liste des tâches qui sont partagées avec moi par propriétaire  
          AFIN DE visualiser les tâches de chaque utilisateur.
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que je suis sur la liste des tâches partagées avec moi  
              Quand je clique sur le bouton de tri par propriétaire et que j'ai choisi l'ordre du tri  
              Alors je vois la liste des tâches triées selon le critère choisi.

    - **Gérer les tâches à plusieurs**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN DE créer et maintenir une liste de tâches commune avec d'autres utilisateurs  
          AFIN DE collaborer avec d'autres utilisateurs sur une même liste de tâches.
        - **Tâches :**
            - Ajouter le rôle "Propriétaire" à la relation entre Tâche et Utilisateur
            - Ajouter le rôle "Propriétaire" au formulaire de la tâche
            - Modifier la liste des tâches pour ajouter la fonctionnalité "En commun"
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que je suis en train de créer ou de modifier une tâche  
              Quand je sélectionne un utilisateur et que je lui attribue le rôle "Propriétaire"  
              Alors tous les utilisateurs concernés apparaissent dans une colonne supplémentaire ("En commun avec") de
              leur liste de tâches.

    - **Date de démarrage d'une tâche**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN DE pouvoir indiquer la date de démarrage d'une tâche  
          AFIN DE prévoir et de prioriser mon travail.
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que je suis sur la liste de mes tâches  
              Quand je crée ou je modifie une tâche  
              Alors je peux indiquer sa date de démarrage.

    - **Trier la liste de tâches par date de démarrage**
        - **Définition :**  
          EN TANT QU'utilisateur  
          J'AI BESOIN DE pouvoir trier ma liste de tâches par date de démarrage  
          AFIN DE visualiser mes tâches à venir.
        - **Critères d'Acceptation :**
            - **Scénario 1 :**  
              Étant donné que je suis sur ma liste de tâches  
              Quand je clique sur le bouton de tri par date de démarrage et que j'ai choisi l'ordre du tri  
              Alors je vois la liste des tâches triées selon le critère choisi.

- **Regrouper les User Stories en Epics :**

  Vous deviez regrouper ces User Stories dans des **Epics** logiques. Voici quelques exemples d'Epics possibles :

    - **Epic 1 : Gestion des tâches**
        - Inclut les User Stories liées à la création, modification, suppression et tri des tâches.

    - **Epic 2 : Collaboration**
        - Inclut les User Stories liées à la gestion des tâches partagées et la collaboration entre plusieurs
          utilisateurs.

    - **Epic 3 : Notifications**
        - Inclut les User Stories liées aux rappels automatiques des tâches.

    - **Planifier et estimer le Product Backlog** :
      Le **Product Backlog** doit contenir les User Stories triées par priorité, avec des estimations de durée
      associées (en
      points ou heures).

- **Mettre en place le tableau Kanban** :
  Le tableau Kanban doit comporter les colonnes suivantes :
    - **À faire**
    - **En cours**
    - **Terminé**

### Correction

Vous deviez bien définir les rôles SCRUM et organiser les User Stories. Les User Stories devaient être regroupées par *
*Epics** logiques, et le **Product Backlog** devait être bien structuré avec des priorités claires. Le tableau Kanban
devait être mis en place correctement avec les colonnes essentielles.

---

## 03. Planification de Sprint

### Travail à réaliser

- **Sprint Planning** :
    - Le **Product Owner** présente les User Stories et sélectionne celles qui feront partie du sprint.
    - L'équipe utilise le **Planning Poker** pour estimer chaque tâche. Ces estimations se font en "points d'effort".

- **Estimation de la vélocité** :
    - La vélocité est estimée en fonction des points réalisés lors des sprints précédents. Si c'est le premier sprint,
      la vélocité sera une estimation basée sur la complexité des tâches et la capacité de l'équipe.

### Correction

Vous deviez participer activement au **Sprint Planning**, poser des questions pertinentes pour bien comprendre chaque
User Story, et estimer correctement les tâches en utilisant le **Planning Poker**. La vélocité du sprint devait être
réaliste, en tenant compte des capacités de l'équipe.

---

## 04. Lancement du Sprint

### Travail à réaliser

- **Prise en main du Sprint Backlog et du tableau Kanban** :
    - L'équipe de développement doit choisir les tâches du **Sprint Backlog** et les déplacer dans la colonne "En cours"
      du tableau Kanban.

- **Daily Scrum Meeting** :
    - Chaque jour, les membres de l'équipe doivent répondre aux trois questions clés :
        1. Qu'ai-je fait hier ?
        2. Que vais-je faire aujourd'hui ?
        3. Est-ce que je rencontre des obstacles ?

- **Suivi des indicateurs** :
    - Le **Burndown Chart** permet de visualiser la progression du travail restant.
    - Le **Burnup Chart** montre la progression vers l'objectif final.
    - Le **Cumulative Flow Diagram** aide à voir l'accumulation des tâches et les goulets d'étranglement.
    - [Exemple de graphiques](https://docs.google.com/spreadsheets/d/1cc-053TWUaBzwQrgNxTKSw-alPcjmOB87SXYD2dsP0c/edit?usp=sharing)

### Correction

Vous deviez bien gérer le tableau Kanban et respecter les limites **WIP**. Les **Daily Scrum Meetings** devaient être
efficaces et centrés sur les progrès et obstacles. Le suivi des indicateurs devait être mis en place pour surveiller la
progression du sprint.

---

## 05. Fin du Sprint

### Travail à réaliser

- **Sprint Review** :
    - L'équipe présente les fonctionnalités réalisées au **Product Owner**.
    - Le Product Owner évalue si les tâches respectent les critères d'acceptation.

- **Sprint Retrospective** :
    - L'équipe discute des aspects positifs et des améliorations à apporter.
    - La rétrospective se concentre sur la collaboration, les processus et les outils utilisés.

### Correction

Vous deviez participer activement à la **Sprint Review** et présenter les tâches réalisées au **Product Owner**. Lors de
la **Sprint Retrospective**, vous deviez identifier clairement ce qui a fonctionné et ce qui doit être amélioré pour les
futurs sprints.

---

### Conclusion

La correction porte sur l'application des principes SCRUM tout au long du cycle. L'évaluation finale se fait sur votre
capacité à structurer correctement un projet agile, à prioriser les tâches et à collaborer efficacement dans un
environnement SCRUM.
