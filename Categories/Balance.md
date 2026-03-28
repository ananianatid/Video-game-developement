---
type: category
tags: [moc, balance]
---

# Balance

> Équilibrage numérique, courbes de progression, résultats de playtest et historique d'itération.

---

## Contenu de cette section

La catégorie **Balance** est le journal de bord des chiffres du jeu. Elle documente les valeurs testées, les problèmes d'équilibrage identifiés et les ajustements effectués. Elle existe séparément de [[Game Design]] pour une raison précise : le design décrit *ce que les systèmes font*, la balance documente *comment ils se comportent en pratique*.

Sous-catégories à créer au fil du développement :
- `Balance/Stats/` — valeurs brutes des personnages, ennemis, objets
- `Balance/Economy/` — courbes de progression, distribution des récompenses
- `Balance/Playtests/` — comptes-rendus de sessions de test

---

## Paramètres globaux

> Les valeurs fondamentales qui gouvernent l'ensemble du jeu. Toute modification ici a des répercussions globales.

| Paramètre | Valeur actuelle | Valeur précédente | Notes |
|---|---|---|---|
| — | — | — | — |

---

## Courbes de progression

> Comment le joueur progresse-t-il dans le temps ? Puissance, récompenses, difficulté.

### Courbe de puissance du joueur

> Description ou graphe de la montée en puissance attendue.

### Courbe de difficulté

> Comment la difficulté évolue-t-elle au fil du jeu ? Pics intentionnels, paliers de repos.

---

## Suivi par système

```base
filters:
  and:
    - 'type == "balance-note"'
views:
  - type: table
    name: Notes d'équilibrage
    order:
      - file.name
```

---

## Historique des playtests

```base
filters:
  and:
    - 'type == "playtest"'
views:
  - type: table
    name: Playtests
    order:
      - file.name
```

---

## Problèmes ouverts

> Déséquilibres identifiés qui n'ont pas encore été traités. Chaque entrée doit finir par migrer vers [[Decisions]] une fois résolue.

| Problème | Système concerné | Priorité | Statut |
|---|---|---|---|
| — | — | — | `ouvert` |

---

## Principes d'équilibrage

- Ne jamais modifier plusieurs paramètres à la fois — isoler chaque variable pour comprendre son effet.
- Documenter chaque modification avec la valeur avant, la valeur après, et l'observation qui a motivé le changement.
- L'équilibrage commence après que la mécanique fonctionne — ne pas équilibrer ce qui n'est pas encore implémenté.
- La perception du joueur prime sur les chiffres : un jeu qui *semble* équilibré l'est, même si les maths ne sont pas parfaites.
