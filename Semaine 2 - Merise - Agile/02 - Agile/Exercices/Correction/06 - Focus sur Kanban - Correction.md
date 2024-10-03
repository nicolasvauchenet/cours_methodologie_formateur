# Focus sur Kanban - Correction : Mise en place d’un tableau Kanban

## Création d’un tableau Kanban

Tableau Kanban initial :

- À faire (To Do) : Conception de la base de données, Développement de l’interface utilisateur, Test de
  l’authentification, Correction des bugs de la version précédente.
- En cours (In Progress) : Aucune tâche au début.
- En revue (In Review) : Aucune tâche au début.
- Terminé (Done) : Aucune tâche au début.
  Ce tableau Kanban permet de visualiser toutes les tâches à accomplir et de suivre leur progression. Les tâches
  commencent dans "À faire" et passeront dans les colonnes suivantes au fur et à mesure de leur avancement.

## Définition des règles WIP

- Limite WIP proposée : Une limite de 2 tâches en cours dans la colonne "En cours" est recommandée.
- Justification : Votre équipe compte 4 développeurs, mais certains d’entre eux devront être disponibles pour les revues
  de code, la gestion des bugs, ou d’autres tâches imprévues. Limiter à 2 tâches dans "En cours" permet d’éviter la
  surcharge et de garantir que chaque tâche soit traitée correctement avant d’en commencer de nouvelles.

## Optimisation du flux de travail

- Problème identifié : Les tâches s'accumulent dans la colonne "En revue" en raison du manque de ressources pour
  effectuer les revues de code.
- Solution proposée :
    - Augmenter la priorité des revues de code et allouer un développeur dédié chaque jour pour effectuer les revues.
    - Mettre en place une limite WIP spécifique pour la colonne "En revue" afin de limiter le nombre de tâches en
      attente de revue.
    - Encourager les revues croisées : un développeur travaillant sur une tâche différente peut effectuer la revue d’un
      autre développeur pour accélérer le processus.
