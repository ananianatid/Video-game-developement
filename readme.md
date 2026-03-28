---
type: wiki
tags: [meta, documentation]
---

# Wiki — Game Development Vault

> Ce document explique la logique du vault, ses conventions, et comment l'utiliser efficacement.
> À lire en premier. À relire quand quelque chose semble ne pas avoir de place.

---

## Philosophie générale

Ce vault est un **outil de pensée**, pas une base de données. Son rôle est de capturer les décisions, de relier les idées entre elles, et de permettre à n'importe quel membre de l'équipe de comprendre l'état du projet à tout moment.

Trois règles fondamentales :

1. **Une note = une chose.** Un personnage, une mécanique, un lieu, une scène. Pas de notes fourre-tout.
2. **Tout ce qui compte doit être écrit.** Une décision non documentée n'existe pas pour l'équipe.
3. **Le vault reflète l'état réel du projet**, pas l'état idéal. Si quelque chose est `concept`, il est `concept`.

---

## Structure du vault

```
Video-game-developement/
├── Home.md              ← Tableau de bord global du projet
├── Wiki.md              ← Ce fichier
├── Categories/          ← Pages de synthèse par domaine (MOC)
├── Templates/           ← Modèles à copier pour créer de nouvelles notes
└── Bases/               ← Vues dynamiques Obsidian (ne pas éditer manuellement)
```

### Categories/

Les fichiers dans `Categories/` sont des **Maps of Content (MOC)** — des pages de synthèse qui agrègent et organisent les notes de leur domaine. Ils ne contiennent pas de contenu brut : ils pointent vers les notes atomiques et affichent des vues dynamiques via les `.base`.

| Fichier | Domaine |
|---|---|
| `Concept.md` | Identité fondatrice du projet |
| `World.md` | Univers, lieux, organisations, lore |
| `Characters.md` | Tous les personnages physiques nommés |
| `Narrative.md` | Structure narrative, scènes, dialogues, fins |
| `Game Design.md` | Mécaniques, systèmes, niveaux, quêtes, boss |
| `Balance.md` | Équilibrage numérique, playtests, problèmes ouverts |
| `Art Direction.md` | Style visuel, couleurs, assets, son |
| `Audio.md` | Bande-son, sound design, contraintes techniques |
| `UI-UX.md` | Interface, HUD, navigation, accessibilité |
| `Technical.md` | Stack, architecture, systèmes à implémenter |
| `Production.md` | Feuille de route, jalons, équipe |
| `Decisions.md` | Journal de toutes les décisions de conception |
| `Inspirations.md` | Références jeux, films, musique, visuels |

### Templates/

Les templates sont des **modèles prêts à l'emploi**. Pour créer une nouvelle note, dupliquer le template correspondant et le déplacer dans le bon dossier.

| Template | Usage | Catégorie cible |
|---|---|---|
| `Template Character.md` | Un personnage physique nommé | `Characters/` |
| `Template Organisation.md` | Une personne morale (corporation, faction, institution…) | `World/Organisations/` |
| `Template Scene.md` | Une scène narrative | `Narrative/Scenes/` |
| `Template Event.md` | Un événement avec choix du joueur | `Narrative/` |
| `Template Dialogue.md` | Un échange clé dont la formulation exacte compte | `Narrative/Dialogues/` |
| `Template Quest.md` | Une quête ou mission avec étapes et embranchements | `Game Design/Quests/` |
| `Template Mechanic.md` | Une mécanique atomique | `Game Design/Mechanics/` |
| `Template System.md` | Un système (ensemble de mécaniques) | `Game Design/Systems/` |
| `Template Level.md` | Un niveau ou une rencontre conçue | `Game Design/Levels/` |
| `Template Boss.md` | Un boss avec phases, attaques et mise en scène | `Game Design/Bosses/` |
| `Template Location.md` | Un lieu de l'univers | `World/Locations/` |
| `Template Milestone.md` | Un jalon de production | `Production/` |
| `Template Person.md` | Un membre de l'équipe | `Production/` |

### Bases/

Les fichiers `.base` sont gérés automatiquement par Obsidian. Ils alimentent les vues dynamiques affichées dans les catégories et dans `Home.md`. Ne pas les éditer manuellement.

---

## Conventions

### Propriété `type`

Chaque note doit avoir une propriété `type` dans son frontmatter YAML. C'est ce que les vues `.base` utilisent pour filtrer les notes. Les valeurs valides sont :

| Valeur | Utilisé pour |
|---|---|
| `home` | La page d'accueil |
| `wiki` | Ce fichier |
| `category` | Les MOC dans `Categories/` |
| `concept` | Notes de pitch, mood, inspirations fondatrices |
| `character` | Personnages physiques |
| `organisation` | Personnes morales (corporations, factions, institutions…) |
| `scene` | Scènes narratives |
| `event` | Événements avec choix |
| `dialogue` | Scripts de dialogue |
| `quest` | Quêtes et missions |
| `mechanic` | Mécaniques atomiques |
| `system` | Systèmes de gameplay |
| `level` | Niveaux |
| `boss` | Bosses |
| `location` | Lieux de l'univers |
| `lore` | Documents in-world, histoires, mythes |
| `balance-note` | Note d'équilibrage liée à un système spécifique |
| `playtest` | Compte-rendu de session de playtest |
| `milestone` | Jalons de production |
| `person` | Membres de l'équipe |
| `asset` | Assets à produire |
| `audio` | Références musicales |
| `color` | Entrées de palette de couleurs |

### Propriété `status`

Le `status` indique l'état d'avancement d'une note. Il varie selon le type :

| Type | Valeurs possibles |
|---|---|
| Mécaniques | `concept` · `prototype` · `implemented` · `cut` |
| Systèmes | `concept` · `prototype` · `implemented` |
| Quêtes | `concept` · `scripted` · `implemented` · `cut` |
| Boss | `concept` · `designed` · `implemented` |
| Scènes | `draft` · `written` · `final` |
| Dialogues | `draft` · `written` · `final` |
| Événements | `concept` · `written` · `implemented` |
| Niveaux | `concept` · `blocked` · `in-progress` · `done` |
| Jalons | `upcoming` · `in-progress` · `done` · `delayed` |

### Liens internes

Utiliser les liens Obsidian `[[Nom de la note]]` pour relier les notes entre elles. Quelques règles :

- Un **boss** doit pointer vers son [[Template Character]] associé et le [[Template Location]] de son arène.
- Une **quête** doit pointer vers les personnages impliqués, les lieux traversés et les scènes déclenchées.
- Un **dialogue** doit pointer vers la scène dont il fait partie.
- Une **organisation** doit pointer vers les lieux qu'elle contrôle et les personnages qui lui appartiennent.
- Une **mécanique** doit pointer vers les systèmes qui l'utilisent et les boss/niveaux qui la testent.

Ces liens constituent le graphe du projet — plus il est dense, plus le vault est utile.

---

## Ordre de remplissage recommandé

Le vault est conçu pour être rempli dans cet ordre. Chaque couche repose sur la précédente.

```
1. Concept          → Pitch, Mood & Aesthetic, Inspirations
2. World            → Lieux principaux, organisations majeures
3. Characters       → Protagoniste(s), antagoniste(s), organisations liées
4. Narrative        → Structure des actes, scènes clés, dialogues importants
5. Game Design      → Mécaniques core, systèmes, quêtes, boss
6. Balance          → Paramètres globaux, courbes de progression (après proto)
7. Art Direction    → Style visuel, palette, références
8. Audio            → Philosophie sonore, bande-son
9. UI-UX            → HUD, carte des écrans
10. Technical       → Stack, architecture, systèmes à implémenter
11. Production      → Jalons, feuille de route, équipe
```

`Decisions.md` et `Inspirations.md` sont alimentés en continu, dès le premier jour.
`Balance.md` ne devient vraiment utile qu'une fois que la mécanique core est prototypée.

---

## Le journal des décisions

`Decisions.md` est le fichier le plus important du vault après `Concept.md`.

**Règles :**
- Toute décision significative doit y être documentée au moment où elle est prise.
- Ne jamais supprimer une entrée. Si une décision est révisée, ajouter une nouvelle entrée qui la remplace et indique pourquoi.
- Le format est fixe : `Decision` / `Context` / `Alternatives considered` / `Consequences`.

Ce journal permet de comprendre *pourquoi* le projet est dans l'état où il est, pas seulement *dans quel état il est*.

---

## Balance vs Game Design

Ces deux catégories traitent toutes les deux des systèmes de jeu — voici comment les distinguer :

- **Game Design** documente *ce que les systèmes font* : leur intention, leur structure, leurs règles.
- **Balance** documente *comment ils se comportent en pratique* : les valeurs testées, les problèmes observés, les ajustements effectués.

Une mécanique est décrite dans Game Design. Les chiffres qui la gouvernent et leur historique d'itération vivent dans Balance.

---

## Personnages physiques vs organisations

- `Template Character` est réservé aux **personnes physiques** — individus nommés avec un arc narratif, des motivations propres, une voix.
- `Template Organisation` est réservé aux **personnes morales** — entités collectives (corporations, factions, institutions, guildes…) qui agissent comme un acteur dans l'univers mais ne sont pas une personne.

Un personnage *appartient* à une organisation. Une organisation *ne remplace pas* un personnage.

---

## Home.md — Le tableau de bord

`Home.md` est la page d'entrée du vault. Elle affiche :
- Les infos projet en un coup d'œil
- Les jalons bloqués et en cours
- Les scènes non finalisées
- Les mécaniques et systèmes en cours
- Les problèmes d'équilibrage ouverts
- Les personnages sans arc défini
- Les organisations et lieux de l'univers
- Les notes récentes

Elle est alimentée automatiquement par les vues `.base`. Pour qu'elle soit utile, les propriétés `status` des notes doivent être maintenues à jour.

---

## Ajouter une sous-catégorie

Quand un domaine grandit, créer des sous-dossiers :

```
Narrative/
  Acts/
  Scenes/
  Dialogues/
  Endings/

Game Design/
  Mechanics/
  Systems/
  Levels/
  Quests/
  Bosses/

World/
  Locations/
  Organisations/
  Lore/

Balance/
  Stats/
  Economy/
  Playtests/
```

Mettre à jour les filtres `.base` correspondants pour inclure le nouveau dossier si nécessaire.

---

## Ce que le vault n'est pas

- **Pas un outil de gestion de tâches.** Les tâches granulaires (bugs, tickets) vont dans un outil dédié. Le vault gère la conception et la documentation, pas le sprint board.
- **Pas un outil de communication.** Les décisions prises en réunion doivent être *retranscrites* ici — le vault n'est pas un compte-rendu, c'est la mémoire vivante du projet.
- **Pas figé.** La structure peut et doit évoluer avec le projet. Si une catégorie manque, la créer. Si un template ne convient pas, l'adapter.
