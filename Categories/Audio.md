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
| Match standard | | | `concept` |
| Match de boss | | | `concept` |
| Victoire | | | `concept` |
| Défaite | | | `concept` |
| Scènes narratives | | | `concept` |
| Paliers du tournoi | | | `concept` |

---

## Direction du sound design

- **SFX clés** —
- **Couches ambiantes** —
- **Voix / dialogues** — oui / non

---

## Contraintes techniques

- **Format cible** —
- **Budget mémoire** —
- **Moteur audio** — (ex. Godot AudioStreamPlayer, FMOD, Wwise)

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

- Le son doit renforcer l'esthétique **rétro-futuriste** — la synthwave et le chiptune comme base, pas comme costume.
- Chaque palier du tournoi doit être soniquement distinct — le joueur doit *entendre* que les enjeux ont augmenté.
- Le bip original de Pong est sacré. Les SFX de la balle et de la raquette doivent en être l'écho.
- La musique adaptative doit évoluer selon l'écart de score, pas seulement selon le temps restant.
