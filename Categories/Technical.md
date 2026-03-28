---
type: category
tags: [moc, technical]
---

# Technical

> Moteur, architecture, systèmes, objectifs de performance et risques techniques.

---

## Contenu de cette section

La catégorie **Technical** est le pendant ingénierie de [[Game Design]]. Elle documente les décisions sur la stack, l'architecture du projet et les systèmes à construire. Elle doit être mise à jour à chaque décision technique — voir aussi [[Decisions]] pour la justification de chaque choix.

---

## Stack

| Élément | Choix | Justification |
|---|---|---|
| Engine | Godot 4 | Open source, 2D natif, licence MIT, export multiplateforme |
| Language | GDScript | Syntaxe proche de Python, intégration étroite avec Godot |
| Renderer | 2D (CanvasItem) | Pas de 3D nécessaire — jeu purement 2D |
| Platforms | PC, Web, Mobile | Cibles d'export natives de Godot |
| Version control | Git | — |

---

## Architecture du projet

```
res://
  scenes/
    game/       # Match, arène, balle, raquette
    ui/         # HUD, menus, boîtes de dialogue
    narrative/  # Cinématiques, écrans d'événements
  scripts/
    core/       # Machine à états, game manager
    mechanics/  # Power-ups, dilatation du temps, dilatation de l'espace
    narrative/  # Système de dialogue, déclencheurs d'événements
  assets/
    sprites/
    audio/
    fonts/
    data/       # JSON / Resources pour la config des matchs, personnages
```

---

## Systèmes à implémenter

- [ ] Machine à états du jeu (menu → match → résultat → narratif)
- [ ] Système de minuterie de match (durée variable par palier)
- [ ] Physique de la balle avec modificateurs d'effets (spin, courbe, distorsion)
- [ ] Système de power-ups (spawn, ramassage, activation, durée)
- [ ] Power-up Time Dilation (modifier le temps de match restant)
- [ ] Power-up Space Dilation (agrandir le demi-terrain du joueur)
- [ ] Modificateurs d'arène (gravité, zones, obstacles mobiles)
- [ ] Système de dialogue / événements narratifs
- [ ] Système de progression (arbre de compétences + boutique + déblocages de boss)
- [ ] Système de sauvegarde / chargement
- [ ] Effets visuels (shaders, particules, lignes de balayage CRT)

---

## Objectifs de performance

- **Résolution cible** —
- **FPS cible** — 60
- **Taille de build estimée** —

---

## Risques techniques

| Risque | Probabilité | Mitigation |
|---|---|---|
| Time Dilation causant des cas limites (temps négatif, état d'égalité) | Moyenne | Définir des règles strictes : min 10s restantes après dilatation, égalité = mort subite |
| Space Dilation créant une confusion visuelle | Moyenne | Retour visuel clair sur les limites du terrain |
| Complexité du système de dialogue qui s'emballe | Faible | Utiliser un plugin Godot existant (ex. Dialogic) |

---

## Outils / plugins tiers

-

---

## Principes techniques

- Chaque système doit être testable de manière isolée — créer des scènes permettant de tester une seule mécanique à la fois.
- Ne jamais coder en dur la durée d'un match ou les règles de score — stocker dans des fichiers de ressources pour que l'équilibrage ne nécessite pas de changements de code.
- La boucle de match centrale doit être jouable avant que tout système narratif ne soit construit.
