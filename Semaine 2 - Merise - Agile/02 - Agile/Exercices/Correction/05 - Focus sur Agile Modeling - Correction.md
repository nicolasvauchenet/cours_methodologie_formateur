# Focus sur Agile Modeling - Correction : Modélisation agile avec "just enough" et "good enough"

## Modélisation des utilisateurs et des rôles (UML)

- Diagramme attendu : Utilisez un diagramme de classes UML pour représenter les utilisateurs et les rôles. Les
  utilisateurs seront représentés par une classe abstraite Utilisateur, avec trois sous-classes : Administrateur,
  Utilisateur Régulier, et Invité.

- La classe Utilisateur est abstraite, et contient les attributs de base (par exemple, nom, email).

- Chaque sous-classe hérite de Utilisateur et peut contenir des attributs ou des méthodes spécifiques.

### Modèle UML :

![05a - Diagramme de classes.png](05a%20-%20Diagramme%20de%20Classes.png)

- Justification : Ce modèle est "just enough" car il capture les relations essentielles entre les utilisateurs et leurs
  rôles, sans entrer dans les détails spécifiques de chaque rôle. Si de nouveaux rôles sont ajoutés, il suffira
  d'ajouter de nouvelles sous-classes ou de modifier les relations entre elles.

- Évolution possible : Si de nouveaux rôles comme "Modérateur" sont ajoutés, ils peuvent être facilement incorporés en
  tant que nouvelles sous-classes dans le diagramme.

## Modélisation des interactions utilisateur (UML)

- Diagramme attendu : Utilisez un diagramme de cas d'utilisation UML pour modéliser les interactions utilisateur. Ce
  diagramme montre les actions principales que l'utilisateur peut accomplir : créer, modifier et supprimer des articles.

### Modèle UML :

![05b - Diagramme de Cas d'Utilisation.png](05b%20-%20Diagramme%20de%20Cas%20d%27Utilisation.png)

- Justification : Ce modèle est "good enough" car il montre les actions principales de l'utilisateur sans entrer dans
  les détails des implémentations techniques. Il est simple mais suffisant pour comprendre les interactions utilisateur.

- Évolution possible : À mesure que le projet évolue, d'autres actions comme "Publier article" ou "Archiver article"
  peuvent être ajoutées à ce modèle de manière progressive.

## Modélisation des flux de données (Merise ou UML)

- Diagramme attendu : Utilisez un diagramme de séquence UML pour montrer le flux de données entre l’interface
  utilisateur, la base de données et l’API externe. Le but est de capturer les interactions principales, sans entrer
  dans les détails de chaque interaction.

### Modèle UML :

![05c - Diagramme de Séquence.png](05c%20-%20Diagramme%20de%20S%C3%A9quence.png)

- Justification : Ce modèle est "just enough" car il montre les principaux flux de données sans entrer dans les détails
  du contenu exact des requêtes ou des réponses. C’est un point de départ pour visualiser comment les données circulent
  dans le système, ce qui est suffisant pour guider l'équipe au début du projet.

- Évolution possible : Si de nouvelles sources de données ou de nouveaux services API sont intégrés dans l'application,
  le modèle peut être enrichi pour inclure ces nouvelles interactions.
