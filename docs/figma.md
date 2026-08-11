# Figma — Installation et prise en main

Figma est l'outil utilisé pour concevoir la maquette graphique du projet. Toute la phase de design se fait ici, avant de passer au code.

---

## Étape 1 — Créer un compte Figma

1. Aller sur [figma.com](https://www.figma.com)
2. Cliquer sur **Se lancer gratiutement**
3. S'inscrire avec l'adresse ECAL (`prenom.nom@ecal.ch`)
4. Valider l'adresse e-mail via le lien reçu par mail

---

## Étape 2 — Activer le plan Éducation

Le plan Éducation de Figma est gratuit et débloque toutes les fonctionnalités professionnelles (projets illimités, partage, historique de versions).

1. Aller sur [figma.com/education](https://www.figma.com/education/)
2. Cliquer sur **Inscrivez-vous**
3. Se connecter avec votre compte Figma
4. Remplir le formulaire en indiquant `École cantonale d'art de Lausanne (ECAL)`
5. Soumettre la demande — la validation est généralement immédiate

---

## Étape 3 — Installer Figma Desktop

L'application Desktop est obligatoire pour ce cours — elle est nécessaire pour activer la connexion MCP avec VS Code.

1. Aller sur [figma.com/downloads](https://www.figma.com/downloads/)
2. Télécharger **Figma Desktop** pour macOS ou Windows
3. Installer l'application
4. Se connecter avec le compte Figma créé à l'étape 1

---

## Prise en main de Figma

### Interface principale

Figma s'organise autour de quelques zones clés :

- **La barre latérale gauche** — calques, composants, assets
- **Le canevas** — zone de travail principale
- **La barre latérale droite** — propriétés de l'élément sélectionné (dimensions, couleurs, typographie, effets)
- **La barre d'outils en haut** — outils de sélection, formes, texte, images

### Raccourcis essentiels

| Action | macOS | Windows |
|--------|-------|---------|
| Sélectionner | `V` | `V` |
| Cadre (Frame) | `F` | `F` |
| Rectangle | `R` | `R` |
| Texte | `T` | `T` |
| Zoom sur la sélection | `Cmd+Shift+H` | `Ctrl+Shift+H` |
| Zoom 100% | `Cmd+0` | `Ctrl+0` |
| Dupliquer | `Cmd+D` | `Ctrl+D` |
| Grouper | `Cmd+G` | `Ctrl+G` |
| Annuler | `Cmd+Z` | `Ctrl+Z` |

### Frames et Auto Layout

Dans Figma, une **Frame** est le conteneur de base — l'équivalent d'un écran ou d'une section. Toujours travailler dans des Frames, pas directement sur le canevas.

**L'Auto Layout** est la fonctionnalité clé pour créer des mises en page qui se comportent comme du CSS Flexbox. Pour l'activer sur un élément sélectionné : `Shift+A`.

---

## Ressources pour apprendre Figma

- [Figma Learn — Getting started](https://help.figma.com/hc/en-us/categories/360002051613-Get-started)
- [Cours Figma sur OpenClassrooms](https://openclassrooms.com/fr/courses/7342806-creez-une-maquette-web-avec-figma)
- [Figma pour les débutants (YouTube)](https://www.youtube.com/results?search_query=figma+tutorial+débutant+français)

---

## Figma et le code — Dev Mode

Le **Dev Mode** est le mode d'inspection qui permet de voir les valeurs CSS de chaque élément : dimensions, couleurs, espacement, typographie. C'est le pont entre la maquette et le code.

Pour basculer en Dev Mode : cliquer sur le bouton **Dev Mode** en haut à droite de l'interface (ou `Shift+D`).

En Dev Mode, sélectionner n'importe quel élément pour voir ses propriétés CSS dans le panneau droit. Ces valeurs sont la référence pour coder la section correspondante.

> Le Dev Mode active également la connexion MCP avec VS Code — voir [Installation et mise en route](./setup.md#étape-7--connecter-figma-à-copilot-mcp-figma) pour les détails.
