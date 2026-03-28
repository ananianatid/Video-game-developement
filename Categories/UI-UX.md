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

L'UI doit ressembler au **tableau de scores d'une diffusion intergalactique** — épurée, lumineuse, légèrement holographique. Chaque élément doit renforcer le sentiment que le joueur est en compétition devant l'univers entier.

---

## Carte des écrans

| Écran | Description | Statut |
|---|---|---|
| Menu principal | Titre, démarrer, options, crédits | `concept` |
| Carte du tournoi | Progression visuelle à travers les paliers | `concept` |
| Pré-match | Présentation de l'adversaire, dialogue | `concept` |
| HUD du match | Minuterie, score, power-ups, arène | `concept` |
| Pause | Reprendre, quitter, paramètres | `concept` |
| Résultat du match | Victoire/défaite, récap du score, XP gagnée | `concept` |
| Progression | Arbre de compétences, boutique, capacités débloquées | `concept` |
| Événement narratif | Boîte de dialogue, invite de choix | `concept` |
| Crédits | — | `concept` |

---

## HUD du match

- **Minuterie** — centre haut, prominent, change de couleur sous 30s
- **Score** — joueur à gauche / adversaire à droite, grand
- **Power-up actif** — centre bas, avec indicateur de recharge
- **Indicateurs d'arène** — niveau de gravité, zones actives (subtil, pas distrayant)

---

## Flux de navigation

```
Menu Principal
  Nouvelle partie → Cinématique d'intro → Carte du tournoi
  Continuer → Carte du tournoi
  Options → Audio / Vidéo / Contrôles
  Crédits

Carte du tournoi
  Sélectionner un match → Dialogue pré-match → HUD du match
  Victoire → Résultat du match → Événement narratif (si applicable) → Carte du tournoi
  Défaite → Résultat du match → Carte du tournoi

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
- Les menus doivent faire partie de la diffusion du tournoi, pas d'une couche séparée.
- Chaque transition doit avoir un objectif — pas de coupes sans intention.
