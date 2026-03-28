---
type: category
tags: [moc, world]
---

# World

> Les règles, l'histoire et la géographie de l'univers du jeu.

---

## Contenu de cette section

La catégorie **World** contient tout ce qui existe indépendamment du joueur et de l'histoire. C'est le substrat sur lequel vivent la narration et les personnages. Les notes ici doivent être atomiques — un lieu, une faction, un événement de lore par note.

Sous-catégories à créer au fur et à mesure de l'avancement du projet :
- `World/Locations/` — zones, pièces, planètes, hubs
- `World/Factions/` — organisations, groupes, pouvoirs
- `World/Lore/` — histoire, mythes, événements, documents

---

## Principes de structure

- Chaque note de **lieu** utilise [[Template Location]].
- Les lieux se lient entre eux via la propriété `connected_to`.
- Les factions sont liées aux lieux qu'elles contrôlent et aux personnages qui leur appartiennent.
- Les notes de lore sont en format libre — elles représentent des documents in-world, des histoires ou des mythes que le joueur peut découvrir.

---

## Tous les lieux
```base
filters:
  and:
    - 'type == "location"'
views:
  - type: table
    name: Locations
    order:
      - file.name
```

---

## Notes de lore
```base
filters:
  and:
    - 'type == "lore"'
views:
  - type: table
    name: Lore notes
    order:
      - file.name
```
