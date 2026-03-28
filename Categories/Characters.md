---
type: category
tags: [moc, characters]
---

# Characters

> Chaque personnage nommé du jeu — jouable, narratif ou mécanique.

---

## Contenu de cette section

La catégorie **Characters** contient une note par personnage. Chaque note couvre l'identité, l'arc narratif, le rôle dans le gameplay et les relations. Les personnages sont liés aux scènes où ils apparaissent, aux lieux qu'ils habitent et aux mécaniques qu'ils enseignent ou incarnent.

Utiliser [[Template Character]] pour chaque nouvelle entrée.

---

## Vue d'ensemble du casting

### Protagonistes

```base
filters:
  and:
    - 'type == "character"'
views:
  - type: table
    name: Protagonists
    order:
      - file.name
```

### Antagonistes

```base
filters:
  and:
    - 'type == "character"'
views:
  - type: table
    name: Antagonists
    order:
      - file.name
```

### Boss

```base
filters:
  and:
    - 'type == "character"'
views:
  - type: table
    name: Bosses
    order:
      - file.name
```

### Alliés & Rivaux

```base
views:
  - type: table
    name: Table
    order:
      - file.name
```

### PNJs

```base
filters:
  and:
    - 'type == "character"'
views:
  - type: table
    name: NPCs
    order:
      - file.name
```

---

## Personnages sans arc défini

```base
filters:
  and:
    - 'type == "character"'
views:
  - type: table
    name: Characters
    order:
      - file.name
```

---

## Questions de conception par personnage

Avant qu'une fiche de personnage soit considérée comme complète, elle doit répondre aux questions suivantes :
- Que veut ce personnage ?
- De quoi a-t-il peur ?
- Comment évolue-t-il au fil de l'histoire ?
- Qu'apprend-il au joueur — sur le plan mécanique ou émotionnel ?
- Quelle est sa relation avec le protagoniste au début et à la fin ?
