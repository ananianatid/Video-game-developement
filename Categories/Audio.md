---
type: category
tags: [moc, audio]
---

# Audio

> Musique, sound design, audio adaptatif et direction vocale.

---

## Contenu de cette section

La catégorie **Audio** définit l'identité sonore du jeu. Elle couvre la structure de la bande-son, la direction du sound design et les contraintes techniques. Les décisions audio doivent être prises aussi tôt que les décisions visuelles — le son représente la moitié de l'expérience.

- **Music** — bande-son, thèmes par contexte, règles adaptatives
- **Sound Design** — SFX, couches ambiantes, sons d'impact
- **Voice** — ton de la livraison des dialogues, direction du casting
- **Technical** — formats, budget mémoire, moteur audio

---

## Philosophie sonore

> Un paragraphe. Quelle émotion la musique doit-elle provoquer ? Que doit ressentir le joueur par le son seul ?

---

## Aperçu de la bande-son

| Contexte | Style / Ambiance | Références | Statut |
|---|---|---|---|
| Menu principal | | | `concept` |
| Exploration | | | `concept` |
| Combat | | | `concept` |
| Boss | | | `concept` |
| Victoire | | | `concept` |
| Défaite | | | `concept` |
| Scènes narratives | | | `concept` |

---

## Direction du sound design

- **SFX clés** —
- **Couches ambiantes** —
- **Voix / dialogues** — oui / non

---

## Contraintes techniques

- **Format cible** —
- **Budget mémoire** —
- **Moteur audio** — (ex. FMOD, Wwise, moteur natif du moteur de jeu)

---

## Références musicales

```base
filters:
  and:
    - 'type == "audio"'
views:
  - type: table
    name: Audio references
    order:
      - file.name
```

---

## Principes audio

- Le son doit renforcer l'esthétique définie dans [[Art Direction]] — cohérence visuelle et sonore dès le début.
- Chaque contexte de jeu majeur (combat, exploration, repos, tension) doit être soniquement distinct.
- Les SFX de gameplay central doivent être immédiatement reconnaissables et satisfaisants à répétition.
- La musique adaptative doit réagir à l'état du jeu, pas seulement au temps ou à la progression linéaire.
