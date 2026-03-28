---
type: category
tags: [moc, decisions]
---

# Design Decisions Log

> Ce fichier trace chaque décision de conception significative prise pendant le développement —
> avec son contexte, les alternatives considérées et les conséquences.
> Ne jamais supprimer une entrée. Ajouter une nouvelle entrée si une décision est révisée.

---

## Format d'une entrée

```
### [YYYY-MM-DD] — Titre de la décision
**Decision:** Ce qui a été décidé.
**Context:** Pourquoi cette question s'est posée.
**Alternatives considered:** Ce qui a été rejeté et pourquoi.
**Consequences:** Impact sur le reste du projet.
```

---

## Décisions

### [2025] — Système de match à durée fixe plutôt qu'à limite de score
**Decision:** Les matchs se jouent sur une durée fixe. Le joueur avec le plus de points à l'expiration du temps gagne.
**Context:** Un système "premier à X points" ne créait aucune tension progressive et rendait le power-up Time Dilation sans intérêt.
**Alternatives considered:** Premier à 11 points (Pong classique) — rejeté : trop court, pas de mécaniques de retournement. Premier à 7 — même problème.
**Consequences:** Time Dilation devient un power-up stratégique central. La durée de match variable par palier renforce les enjeux dramatiques de chaque round.

---

### [2025] — Choix du moteur : Godot 4
**Decision:** Godot 4 avec GDScript comme moteur de développement.
**Context:** Jeu narratif 2D, budget indépendant, petite équipe.
**Alternatives considered:** Unity — controverse sur les licences depuis 2023, surcharge C#. Unreal — largement surdimensionné pour de la 2D, complexité C++. Phaser.js — insuffisant pour des systèmes narratifs complexes.
**Consequences:** Export multiplateforme natif, pas de royalties, courbe d'apprentissage raisonnable, bons outils 2D.

---

### [2025] — Condition de victoire en cas d'égalité
**Decision:** *(à définir)* — mort subite ? prolongation ? tirage au sort ?
**Context:** Le power-up Time Dilation peut être bloqué quand le score est à égalité. Mais un match peut quand même se terminer par un match nul.
**Alternatives considered:** —
**Consequences:** —
