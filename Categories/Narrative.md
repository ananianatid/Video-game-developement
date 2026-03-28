---
type: category
tags: [moc, narrative]
---

# Narrative

> Structure de l'histoire, scènes, dialogues et fins.

---

## Contenu de cette section

La catégorie **Narrative** décompose l'histoire en unités atomiques. Une scène n'est pas un acte — l'une est un beat, l'autre est un conteneur. Structurer le dossier au fur et à mesure de l'avancement du projet :

- `Narrative/Acts/` — conteneurs narratifs de haut niveau
- `Narrative/Scenes/` — moments narratifs individuels, en utilisant [[Template Scene]]
- `Narrative/Dialogues/` — dialogues au niveau du script pour les échanges clés
- `Narrative/Endings/` — conclusions ramifiées et leurs conditions

---

## Structure de l'histoire

> Renseigner les actes au fur et à mesure du développement. Chaque acte est lié à ses scènes.

| Acte | Titre | Statut |
|-----|-------|--------|
| — | — | `draft` |

---

## Toutes les scènes par acte
```base
filters:
  and:
    - 'type == "scene"'
views:
  - type: table
    name: Scenes
    order:
      - file.name
```

---

## Scènes par statut
```base
filters:
  and:
    - 'type == "scene"'
views:
  - type: table
    name: Scenes
    order:
      - file.name
```

---

## Scènes avec choix du joueur
```base
filters:
  and:
    - 'type == "scene"'
views:
  - type: table
    name: Scenes
    order:
      - file.name
```

---

## Fins
```base
filters:
  and:
    - 'inFolder(file.file, "Narrative/Endings")'
views:
  - type: table
    name: Endings
    order:
      - file.name
```

---

## Principes de game design narratif

- Chaque scène doit avoir un **objectif dramatique** — qu'est-ce qui change entre le début et la fin de cette scène ?
- Les choix doivent refléter les valeurs du personnage, pas des solutions à des énigmes.
- Chaque fin doit être une réponse cohérente à la question centrale du jeu.
- Les notes de dialogue sont optionnelles — n'écrire des scripts complets que pour les scènes où la formulation exacte importe.
