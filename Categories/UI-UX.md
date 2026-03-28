---
type: category
tags: [moc, ui-ux]
---

# UI / UX

> Philosophie d'interface, carte des écrans, design du HUD, flux de navigation et accessibilité.

---

## Contenu de cette section

La catégorie **UI/UX** définit tout ce que le joueur voit qui ne fait pas partie du monde du jeu lui-même. Les décisions d'interface doivent servir l'esthétique centrale — rétro-futuriste, inspirée de l'arcade — sans gêner le déroulement du match.

---

## Philosophie d'interface

> L'UI doit-elle être diégétique (faire partie du monde) ou explicite ? Quel est le ton visuel ?

L'UI doit servir le **registre émotionnel** défini dans [[Art Direction]] — chaque élément d'interface doit renforcer l'univers du jeu, pas le parasiter.

---

## Carte des écrans

| Écran | Description | Statut |
|---|---|---|
| Menu principal | Titre, démarrer, options, crédits | `concept` |
| Gameplay principal | Boucle de jeu centrale | `concept` |
| Pause | Reprendre, quitter, paramètres | `concept` |
| Résultat / fin de séquence | Récapitulatif, récompenses | `concept` |
| Progression | Arbre de compétences, inventaire, boutique | `concept` |
| Événement narratif | Boîte de dialogue, invite de choix | `concept` |
| Crédits | — | `concept` |

---

## HUD de gameplay

- **Indicateur principal** — (santé, score, ressource clé…) — position et taille à définir
- **Indicateur secondaire** — (minuterie, mini-carte, stamina…)
- **Éléments contextuels** — (power-ups actifs, objectifs en cours…)
- **Règle générale** — le HUD ne doit jamais distraire de l'action principale

---

## Flux de navigation

```
Menu Principal
  Nouvelle partie → [intro / tutoriel] → Gameplay
  Continuer → Gameplay
  Options → Audio / Vidéo / Contrôles
  Crédits

Gameplay
  Pause → Reprendre / Options / Quitter
  Fin de séquence → Résultat → [événement narratif] → suite

Événement narratif
  Choix A → conséquence
  Choix B → conséquence
  Pas d'action → conséquence passive
```

---

## Accessibilité

- [ ] Mode daltonien (palettes alternatives)
- [ ] Taille du texte ajustable
- [ ] Contrôles remappables
- [ ] Sous-titres pour tous les dialogues
- [ ] Option réduction des animations (désactiver les effets de secousse d'écran, les effets de particules)

---

## Style visuel

- **Police(s)** —
- **Couleurs primaires** —
- **Animations UI** —
- **Références visuelles** —

---

## Principes UI

- Le HUD pendant un match ne doit jamais nécessiter plus d'un coup d'œil — les yeux du joueur doivent rester sur la balle.
- Les menus doivent faire partie de l'univers du jeu, pas d'une couche séparée.
- Chaque transition doit avoir un objectif — pas de coupes sans intention.
