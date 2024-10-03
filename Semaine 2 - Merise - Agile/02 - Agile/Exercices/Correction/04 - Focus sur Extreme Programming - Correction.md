# Focus sur Extreme Programming - Correction : Les pratiques clés de Extreme Programming

## Pair Programming

- Avantages observés : Le pair programming favorise une meilleure qualité de code dès le départ, réduit les erreurs, et
  améliore la collaboration au sein de l’équipe. Il permet aussi d'avoir une revue de code immédiate et d'apprendre des
  compétences des autres.
- Inconvénients observés : Cela peut être chronophage si les deux développeurs ne sont pas bien synchronisés. Cela peut
  aussi causer des frustrations si l’un des membres du binôme domine trop la session.
- Solutions proposées : Encourager une meilleure rotation des rôles entre "driver" (celui qui code) et "observer" (celui
  qui relit). Organiser des sessions de feedback régulier pour améliorer cette pratique au fil des sprints.

## Test-Driven Development (TDD)

### Test unitaire :

```php
public function testCalculerTVA()
{
    $this->assertEquals(120, calculerTVA(100, 20));
}
```

### Code minimal pour passer le test :

```php
function calculerTVA($montant, $taux)
{
    return $montant * (1 + $taux / 100);
}
```

## Refactoring :

Après s'être assuré que le test passe, le code pourrait être refactorisé pour améliorer sa lisibilité sans impacter son
comportement fonctionnel :

```php
function calculerTVA($montant, $taux)
{
    $tva = ($montant * $taux) / 100;
    return $montant + $tva;
}
```

## Refactoring

- Exemple de refactorisation : Imaginons que la méthode ajouterProduit d'une classe Panier contient beaucoup de code
  dupliqué pour calculer les réductions. L'idée serait d'extraire cette logique dans une méthode privée
  calculerReduction, ce qui simplifierait le code et améliorerait sa réutilisabilité.
- Justification : Réduire la duplication de code permet de minimiser le risque d'erreurs futures, facilite la
  maintenance, et améliore la lisibilité.
- Vérification : Les tests unitaires doivent être exécutés après le refactoring pour vérifier que la fonctionnalité
  reste intacte. Aucun test ne doit échouer après les modifications apportées.
