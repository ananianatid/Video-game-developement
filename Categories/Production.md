---
type: category
tags: [moc, production]
---

# Production

> Feuille de route, jalons, stack technique et équipe.

---

## Contenu de cette section

La catégorie **Production** est la couche opérationnelle du vault. Elle trace ce qui doit être construit, par qui et pour quand. Les notes ici utilisent [[Template Milestone]] et pointent vers les notes de design, de narration et d'art dont elles dépendent.

---

## Infos projet

| | |
|---|---|
| **Engine** | — |
| **Language** | — |
| **Renderer** | — |
| **Platform** | — |
| **Repo** | — |
| **Team size** | — |

---

## Feuille de route

| Phase | Description | Statut |
|-------|-------------|--------|
| Pre-production | GDD, prototypes, vertical slice | — |
| Alpha | Toutes les fonctionnalités intégrées, assets provisoires | — |
| Beta | Contenu complet, correction de bugs | — |
| Gold | Prêt à être livré | — |

---

## Jalons

### Tous les jalons
```base
filters:
  and:
    - 'type == "milestone"'
views:
  - type: table
    name: All milestones
    order:
      - deadline
      - file.name
```

### À venir
```base
filters:
  and:
    - 'type == "milestone"'
    - 'status == "upcoming"'
views:
  - type: table
    name: Upcoming
    order:
      - deadline
      - file.name
```

### En cours
```base
filters:
  and:
    - 'type == "milestone"'
    - 'status == "in-progress"'
views:
  - type: table
    name: In progress
    order:
      - deadline
      - file.name
```

### En retard
```base
filters:
  and:
    - 'type == "milestone"'
    - 'status == "delayed"'
views:
  - type: table
    name: Delayed
    order:
      - deadline
      - file.name
```

---

## Stack technique

> Lister les technologies principales une fois décidées. Mettre à jour au fil de l'évolution de la stack.

- **Engine** —
- **Physics** —
- **Audio** —
- **UI framework** —
- **Version control** —
- **CI/CD** —
- **Project management** —

---

## Équipe

```base
filters:
  and:
    - 'type == "person"'
views:
  - type: table
    name: Team
    order:
      - file.name
```

---

## Principes de production

- Un jalon n'est `done` que lorsque tous ses livrables sont testables par quelqu'un qui ne les a pas construits.
- Les dépendances entre jalons doivent être explicites — ne jamais supposer qu'une tâche en amont est terminée.
- Réduire le périmètre avant de réduire la qualité. La boucle centrale doit toujours être jouable.
- Chaque sprint doit se terminer avec quelque chose qu'un joueur peut toucher.
