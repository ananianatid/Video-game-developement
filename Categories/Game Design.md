---
type: category
tags: [moc, game-design]
---

# Game Design

> La boucle centrale, les mécaniques, les systèmes, les niveaux et l'équilibrage.

---

## Contenu de cette section

La catégorie **Game Design** est la section la plus technique du vault. Elle sépare le design en trois couches :

- **Mechanics** — actions atomiques du joueur et leurs retours. Une mécanique par note, en utilisant [[Template Mechanic]].
- **Systems** — ensembles de mécaniques qui interagissent pour produire un comportement émergent (économie, progression, combat). Un système par note, en utilisant [[Template System]].
- **Levels** — espaces ou rencontres conçus individuellement, en utilisant [[Template Level]].
- **Balance Notes** — notes libres suivant l'ajustement numérique, les résultats des playtest et l'historique des itérations.

---

## Boucle centrale

> Décrire la boucle fondamentale en un paragraphe. Tout le reste doit servir cette boucle.

---

## Mécaniques

### Par catégorie

```base
views:
  - type: table
    name: Table
    order:
      - file.name
```

### Par statut

```base
views:
  - type: table
    name: Table
    order:
      - file.name
```

### Mécaniques à prototyper
```base
filters:
  and:
    - 'type == "mechanic"'
views:
  - type: table
    name: Mechanics
    order:
      - file.name
```

---

## Systèmes

### Tous les systèmes

```base
filters:
  and:
    - 'type == "system"'
views:
  - type: table
    name: Systems
    order:
      - file.name
```

### Systèmes avec des dépendances non résolues
```base
filters:
  and:
    - 'type == "system"'
views:
  - type: table
    name: Systems
    order:
      - file.name
```

---

## Niveaux

### Tous les niveaux par acte
```base
filters:
  and:
    - 'type == "level"'
views:
  - type: table
    name: Levels
    order:
      - file.name
```

### Niveaux en cours
```base
filters:
  and:
    - 'type == "level"'
views:
  - type: table
    name: Levels
    order:
      - file.name
```

---

## Questions de conception à répondre

- Quelle est la **fantasy centrale** — le seul sentiment que le joueur poursuit ?
- Que fait le joueur toutes les 30 secondes ? Toutes les 5 minutes ? Toutes les heures ?
- Quelle mécanique est introduite en premier, et qu'enseigne-t-elle ?
- Quel est le système le plus complexe, et quand le joueur le rencontre-t-il ?
- Qu'est-ce qui peut être supprimé sans casser la boucle centrale ?
