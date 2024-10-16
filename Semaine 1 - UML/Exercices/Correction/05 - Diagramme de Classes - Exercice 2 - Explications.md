# Explication des étapes de conception d'un diagramme de classes UML

## Première étape : Modélisation des entités

![05 - Diagramme de Classes - Exercice 2 - Étape 1 - Modélisation.png](05%20-%20Diagramme%20de%20Classes%20-%20Exercice%202%20-%20%C3%89tape%201%20-%20Mod%C3%A9lisation.png)

Dans cette première étape, l'accent est mis sur la modélisation des entités principales du système, avec leurs attributs
et méthodes. Chaque entité est directement responsable de ses actions, ce qui signifie que les comportements et la
logique sont inclus dans les entités elles-mêmes. Voici les points clés de cette première étape :

- **Responsabilités regroupées :** Les entités telles que `Lecteur`, `Bibliothécaire`, `Livre`, `Emprunt`, et `Rappel`
  contiennent non seulement leurs propriétés mais aussi les méthodes liées à leur gestion. Par exemple, `Lecteur` gère
  directement l'emprunt et le retour de livres, et `Bibliothécaire` gère l'enregistrement des emprunts et l'envoi de
  rappels.

- **Relations simples :** Les entités sont liées par des relations directes. Par exemple, `Lecteur` est lié à `Emprunt`,
  et `Bibliothèque` possède des `Livres`.

### Changements à apporter :

Ce modèle ne sépare pas clairement la logique métier de la gestion des entités. Les entités prennent en charge des
responsabilités qui devraient être gérées par des services spécifiques, rendant le système moins flexible et moins
évolutif. Par exemple, `Bibliothécaire` gère directement l'envoi de rappels, ce qui n'est pas idéal si on souhaite
changer la manière d'envoyer ces rappels plus tard.

## Deuxième étape : Séparation des responsabilités avec des services

![05 - Diagramme de Classes - Exercice 2 - Étape 2 - Séparation.png](05%20-%20Diagramme%20de%20Classes%20-%20Exercice%202%20-%20%C3%89tape%202%20-%20S%C3%A9paration.png)

Dans cette deuxième étape, les services sont introduits pour séparer la gestion des entités et leurs fonctionnalités.
Cela permet de clarifier les responsabilités et d'améliorer la modularité du système.

- **Séparation des responsabilités :** Des classes de service sont créées pour gérer les fonctionnalités spécifiques
  comme l'emprunt et le retour de livres (`ServiceEmprunt`), l'envoi de rappels (`ServiceRappel`), et la gestion des
  livres dans la bibliothèque (`ServiceBibliothèque`). Les entités, telles que `Lecteur`, `Livre`, ou `Bibliothèque`, ne
  sont plus responsables de ces opérations complexes.

- **Logique externalisée :** Les méthodes qui étaient initialement dans les entités sont maintenant transférées dans les
  services. Par exemple, `Bibliothécaire` n'enregistre plus directement les emprunts, mais délègue cette tâche à
  `ServiceEmprunt`, ce qui permet d'avoir une logique plus centralisée.

- **Classes sans abstraction :** Même si les services existent, tout est encore lié de manière explicite à des classes
  concrètes. Par exemple, `ServiceEmprunt` gère spécifiquement l'emprunt de `Livre`, et `ServiceRappel` gère
  spécifiquement des `Rappels`. Cela rend le système un peu plus modulaire, mais les dépendances directes entre les
  classes limitent encore son évolutivité.

### Changements à apporter :

Bien que les services aient amélioré la séparation des responsabilités, il n’y a pas encore de véritable abstraction
dans le système. Si une nouvelle ressource ou un nouveau type de rappel devait être ajouté, cela nécessiterait des
modifications dans plusieurs classes, car elles sont encore couplées à des implémentations concrètes (par exemple,
`Livre` et `Rappel`).

## Troisième étape : Introduction des abstractions

![05 - Diagramme de Classes - Exercice 2 - Étape 3 - Abstraction.png](05%20-%20Diagramme%20de%20Classes%20-%20Exercice%202%20-%20%C3%89tape%203%20-%20Abstraction.png)

Dans cette troisième étape, le système est rendu plus flexible et évolutif grâce à l'introduction d’interfaces.
L'objectif est de généraliser les comportements en se concentrant sur les fonctionnalités fondamentales, tout en
préparant le système à accepter de nouvelles implémentations sans modifier le code existant.

- **Abstraction avec des interfaces :** Des interfaces telles que `Empruntable`, `Stockable`, `Gérable`, `Rappelable`,
  `RessourceEmpruntable`, et `IRappel` sont introduites. Ces interfaces définissent des contrats pour les comportements
  fondamentaux sans se soucier des détails d'implémentation. Cela permet au système d’être plus flexible en autorisant
  plusieurs implémentations des interfaces (par exemple, d'autres types de ressources empruntables comme des DVD ou des
  eBooks).

- **Couches d'abstraction :** Les classes de service implémentent ces interfaces pour offrir des comportements
  standardisés. Par exemple, `ServiceEmprunt` implémente `Gérable`, ce qui lui permet de gérer n'importe quelle
  ressource empruntable, qu'il s'agisse de Livre ou d'autres types de ressources qui pourraient être ajoutés
  ultérieurement.

- **Évolutivité :** Grâce aux interfaces, le système est ouvert aux évolutions. Si, par exemple, tu voulais ajouter un
  `RappelSMS` ou `RappelEmail`, tu pourrais simplement créer une nouvelle classe implémentant l'interface `IRappel` sans
  changer les classes existantes. De même, tu peux ajouter d'autres types de ressources empruntables en implémentant
  `RessourceEmpruntable`.

- **Dépendance sur les abstractions :** Les classes interagissent désormais avec les interfaces plutôt qu’avec des
  classes concrètes. Cela réduit le couplage et permet d’ajouter ou de modifier des implémentations sans changer les
  classes existantes.

## Conclusion des trois étapes :

- **Première étape :** Le système a commencé avec une approche monolithique où les entités étaient responsables à la
  fois de leur propre gestion et de la logique métier, ce qui n'était pas très modulaire.

- **Deuxième étape :** La séparation des responsabilités par l’introduction des services a permis de clarifier la
  gestion des entités, mais le système était encore trop dépendant de classes concrètes.

- **Troisième étape :** L'introduction des interfaces a apporté la modularité et la flexibilité nécessaires pour
  permettre l'évolution du système sans introduire de couplage fort entre les composants.

En résumé, chaque étape a amélioré la séparation des préoccupations et la modularité, avec la troisième étape qui
introduit des abstractions pour rendre le système évolutif et maintenable. 
