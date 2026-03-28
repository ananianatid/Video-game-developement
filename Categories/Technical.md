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
| Engine | — | — |
| Language | — | — |
| Renderer | — | — |
| Platforms | — | — |
| Version control | — | — |

---

## Architecture du projet

```
res://  (ou équivalent selon le moteur)
  scenes/
    game/       # Boucle de gameplay principale
    ui/         # HUD, menus, écrans
    narrative/  # Cinématiques, événements
  scripts/
    core/       # Machine à états, game manager
    mechanics/  # Systèmes de gameplay
    narrative/  # Dialogue, déclencheurs d'événements
  assets/
    sprites/
    audio/
    fonts/
    data/       # Fichiers de configuration (JSON, Resources…)
```

---

## Systèmes à implémenter

- [ ] Machine à états globale (menus → gameplay → résultat → narratif)
- [ ] Boucle de gameplay principale
- [ ] Système de sauvegarde / chargement
- [ ] Système de dialogue / événements narratifs
- [ ] Système de progression (à définir selon le genre)
- [ ] Effets visuels et retours (feedback) joueur

---

## Objectifs de performance

- **Résolution cible** —
- **FPS cible** —
- **Taille de build estimée** —

---

## Risques techniques

| Risque | Probabilité | Mitigation |
|---|---|---|
| — | — | — |

---

## Outils / plugins tiers

-

---

## Principes techniques

- Chaque système doit être testable de manière isolée — créer des scènes permettant de tester une seule mécanique à la fois.
- Ne jamais coder en dur les paramètres de gameplay — stocker dans des fichiers de ressources pour que l'équilibrage ne nécessite pas de changements de code.
- La boucle de gameplay centrale doit être jouable avant que tout système narratif ne soit construit.
