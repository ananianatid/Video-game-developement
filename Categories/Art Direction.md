---
type: category
tags: [moc, art-direction]
---

# Art Direction

> Style visuel, couleurs, UI/UX, design des personnages, environnements, musique et son.

---

## Contenu de cette section

La catégorie **Art Direction** traduit le registre émotionnel défini dans [[Concept]] et [[Mood & Aesthetic]] en décisions créatives concrètes. Elle se divise en :

- **Visual Style** — l'engagement esthétique global
- **Color Palette** — le système de couleurs défini, avec ses rôles et valeurs
- **UI/UX** — philosophie d'interface, design du HUD, menus
- **Character Design** — identité visuelle de chaque personnage
- **Environments** — traitement visuel par lieu ou biome
- **Music & Sound** — structure de la bande-son, direction du sound design, références

---

## Résumé du style visuel

> Un paragraphe. Définir une direction esthétique claire. À quoi ressemble ce monde au premier regard ?

---

## Palette de couleurs
```base
filters:
  and:
    - 'type == "color"'
views:
  - type: table
    name: Color palette
    order:
      - file.name
```

---

## Designs des personnages
```base
filters:
  and:
    - 'type == "character"'
views:
  - type: table
    name: Character designs
    order:
      - file.name
```

---

## Designs des environnements
```base
filters:
  and:
    - 'type == "location"'
views:
  - type: table
    name: Environments
    order:
      - file.name
```

---

## Musique & Son

> Lier à `Music & Sound.md` une fois créé.

- Structure de la bande-son (pistes par acte, par lieu, par boss)
- Direction du sound design (registre acoustique, références)
- Règles de musique adaptative (quand la musique change-t-elle ?)

---

## Principes de direction artistique

- Chaque décision visuelle doit servir la **fantasy centrale** définie dans [[Concept]].
- La couleur encode le sens — définir ce que chaque rôle de palette communique avant de l'assigner.
- L'UI doit être invisible — le joueur ne doit jamais penser à l'interface, seulement au jeu.
- Le son représente la moitié de l'expérience — définir la direction audio aussi tôt que la direction visuelle.

---

## Assets à produire
```base
filters:
  and:
    - 'type == "asset"'
views:
  - type: table
    name: Assets
    order:
      - file.name
```
