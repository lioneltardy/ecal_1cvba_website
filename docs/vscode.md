# Installation et mise en route

Ce guide explique comment installer les outils et démarrer le projet. Suivre les étapes dans l'ordre — chaque étape suppose que la précédente est faite.

**Ce dont on a besoin :**
- Un ordinateur sous macOS ou Windows
- Une connexion internet
- Une adresse e-mail ECAL (`prenom.nom@ecal.ch`)
- Un compte Figma (celui utilisé pour la maquette)

---

## Étape 1 — Installer VS Code

VS Code est l'éditeur de code utilisé pour tout le projet.

1. Aller sur [code.visualstudio.com](https://code.visualstudio.com)
2. Cliquer sur **Download** — le site détecte automatiquement le système
3. Ouvrir le fichier téléchargé et installer l'application
4. Lancer VS Code

> **macOS :** faire glisser l'icône VS Code dans le dossier Applications. Si macOS bloque l'ouverture, aller dans Réglages système → Confidentialité et sécurité → cliquer sur "Ouvrir quand même".

> **Windows :** lors de l'installation, cocher l'option **"Add to PATH"** — c'est important pour la suite.

---

## Étape 2 — Installer Node.js

Node.js est nécessaire pour faire tourner Vite, l'outil qui recharge le navigateur automatiquement à chaque modification du code.

1. Aller sur [nodejs.org](https://nodejs.org)
2. Télécharger la version **LTS** (Long Term Support) — bouton de gauche
3. Installer avec tous les paramètres par défaut

**Vérifier que ça marche :**

Ouvrir le Terminal (macOS) ou l'Invite de commandes (Windows) et taper :

```
node --version
```

Un numéro de version doit s'afficher, par exemple `v20.11.0`. Si un message d'erreur apparaît, réinstaller Node.js.

> **Trouver le Terminal :**
> macOS : `Cmd + Espace`, taper "Terminal", appuyer sur Entrée.
> Windows : `Win + R`, taper `cmd`, appuyer sur Entrée.

---

## Étape 3 — Créer un compte GitHub et activer GitHub Education

GitHub est la plateforme où est hébergé le projet. GitHub Education donne accès à Copilot gratuitement avec une adresse e-mail scolaire.

### 3a. Créer le compte

1. Aller sur [github.com](https://github.com)
2. Cliquer sur **Sign up**
3. Utiliser l'adresse ECAL (`prenom.nom@ecal.ch`)
4. Choisir un nom d'utilisateur — quelque chose de professionnel, ce compte sera conservé après l'école
5. Valider l'adresse e-mail via le lien reçu par mail

### 3b. Activer GitHub Education

1. Aller sur [education.github.com/students](https://education.github.com/students)
2. Cliquer sur **Get Student Benefits**
3. Se connecter avec le compte GitHub
4. Sélectionner l'adresse ECAL et indiquer "École cantonale d'art de Lausanne"
5. Soumettre la demande — la validation prend quelques minutes à quelques jours

> **Si la validation prend du temps :** continuer avec les étapes suivantes. Il est possible d'activer un essai gratuit de 30 jours de Copilot directement sur github.com → Settings → Copilot en attendant.

---

## Étape 4 — Télécharger le projet

Télécharger le projet depuis GitHub sous forme d'archive ZIP.

1. Aller sur [github.com/harkle/ecal_1cvba_website](https://github.com/harkle/ecal_1cvba_website)
2. Cliquer sur le bouton vert **Code**
3. Cliquer sur **Download ZIP**
4. Décompresser l'archive dans un dossier de travail (par exemple, dans Documents)
5. Ouvrir VS Code
6. Faire **File → Open Folder** et sélectionner le dossier décompressé

> Le dossier du projet est maintenant ouvert dans VS Code. Dans le panneau de gauche, les fichiers `index.html`, `src/`, `assets/` doivent être visibles.

---

## Étape 5 — Lancer Vite

<br>

<img src="./img/vscode-run.gif" alt="Vite run" width="100%">

<br>

Vite recharge automatiquement le navigateur à chaque sauvegarde de fichier.

1. Dans VS Code, ouvrir le terminal intégré : **View → Terminal** (ou `` Ctrl+` `` / `` Cmd+` ``)
2. Installer les dépendances du projet (à faire une seule fois) :
   ```
   npm install
   ```
   Des lignes défilent pendant quelques secondes — c'est normal.

3. Lancer le serveur de développement :
   ```
   npm run dev
   ```

4. Vite affiche une adresse locale :
   ```
   Local:   http://localhost:5173/
   ```

5. Ouvrir cette adresse dans le navigateur — la page du projet doit s'afficher.

**À partir de maintenant :** chaque sauvegarde (`Cmd+S` / `Ctrl+S`) met à jour le navigateur automatiquement.

> **Arrêter Vite :** taper `Ctrl+C` dans le terminal.
> **Relancer Vite :** retaper `npm run dev`.

---

## Étape 6 — Installer les extensions VS Code

Ouvrir l'onglet Extensions (`Cmd+Shift+X` / `Ctrl+Shift+X`) et installer :

### GitHub Copilot

1. Rechercher "GitHub Copilot"
2. Installer l'extension officielle de GitHub
3. VS Code demande de se connecter au compte GitHub — cliquer sur "Sign in"
4. Si GitHub Education est validé, Copilot s'active automatiquement

### GitHub Copilot Chat

1. Rechercher "GitHub Copilot Chat"
2. Installer l'extension (souvent installée automatiquement avec Copilot)

> Ces deux extensions sont liées — Copilot pour les suggestions inline, Copilot Chat pour le dialogue en langage naturel.

---

## Étape 7 — Connecter Figma à Copilot (MCP Figma)

Le MCP Figma permet à Copilot de lire directement la maquette et de générer du code qui correspond au design.

### Activer le serveur MCP dans Figma Desktop

1. Ouvrir Figma Desktop et passer en **Dev Mode** (bouton en haut à droite)
2. Dans le panneau droit, cliquer sur **Enable desktop MCP server**
3. Confirmer dans la boîte de dialogue — Figma configure automatiquement VS Code

C'est tout. Pas de fichier à modifier, pas de configuration manuelle.

### Utiliser le MCP dans Copilot Chat

1. Dans Figma, sélectionner le frame ou la section à coder
2. Clic droit → **Copy link to selection**
3. Dans Copilot Chat, coller le lien avec une instruction :

> *"Voici le lien vers ma section Synopsis : [lien Figma]. Générer le HTML et le CSS correspondant en utilisant uniquement les classes du framework. Vanilla CSS, zéro JavaScript."*

> **Note :** cette fonctionnalité est en beta et peut se comporter différemment selon la version de VS Code. Si ça ne fonctionne pas, décrire simplement ce qu'on veut reproduire avec des mots — Copilot s'en sort très bien aussi.

---

## Étape 8 — Comprendre la structure du projet

Avant de commencer à coder, prendre 5 minutes pour explorer les fichiers :

```
/
├── index.html              ← Page unique du site (ne pas créer d'autres .html)
├── src/
    ├── css/
    │   ├── style.css       ← Point d'entrée CSS (importe tout le framework)
    │   ├── reset.css       ← Reset navigateur
    │   ├── colors.css      ← Variables de couleurs et classes utilitaires
    │   ├── typography.css  ← Styles typographiques et classes utilitaires
    │   ├── spacings.css    ← Classes utilitaires pour les espacements (margins/paddings)
    │   └── layout.css      ← Style des éléments de layout (containers, flex, grid, sections) et CSS personnalisé de l'étudiant·e
    └── images/             ← SVG et autres images locales intégrées au HTML/CSS
```

**Règle simple :** travailler uniquement dans le fichier `index.html` pour le structure et le contenu et dans les fichier `src/css/*` pour les styles.

---

## Utiliser Copilot

### Comment Copilot connaît le projet

Le fichier `llms.txt` à la racine du projet contient toutes les instructions pour Copilot : les classes CSS disponibles, les règles à respecter, la structure attendue. Copilot le lit automatiquement. Il est recommandé, à chaque début de session de travail avec l’IA, de lui rappeler de consulter le contenu de ce fichier pour s'assurer qu'elle suit les bonnes règles.

### Workflow avec la maquette Figma

1. Dans Figma, sélectionner la frame ou la section à coder
2. Copier le lien du frame : clic droit → **Copy link to selection**
3. Dans Copilot Chat (`Cmd+Shift+I` / `Ctrl+Shift+I`), décrire ce qu'on veut :

> *"Voici le lien vers ma section Synopsis dans Figma : [lien]. Générer le HTML et le CSS correspondant en utilisant uniquement les classes du framework et en vanilla CSS, sans JavaScript."*

> *"Voici le lien vers ma section Distribution : [lien]. Créer la grille de portraits avec les classes du framework. CSS uniquement."*

En début de session, il est conseillé de rappeler à Copilot de lire le fichier `llms.txt` pour s'assurer qu'elle suit les bonnes règles.

> *"Merci de lire le fichier llms.txt pour connaître les classes CSS disponibles et les règles à respecter."*

### Ce que Copilot fait bien dans ce projet
- Reproduire un layout depuis un frame Figma
- Trouver la bonne combinaison de classes pour un espacement ou une grille
- Écrire des transitions et animations CSS
- Corriger une erreur dans le HTML ou le CSS

### Ce qu'il faut garder en tête
Copilot peut se tromper ou s'écarter du framework. Toujours vérifier que le code généré utilise les classes du projet et pas des valeurs inventées. Si le résultat ne correspond pas à la maquette, reformuler le prompt avec plus de précision.

---

## En cas de problème

**Le terminal affiche une erreur en rouge :** lire le message — il indique souvent exactement ce qui ne va pas. Copier-coller le message dans Copilot Chat.

**Vite ne se lance pas :** vérifier que le terminal est bien ouvert dans le dossier du projet. Le chemin doit se terminer par `/ecal_1cvba_website`.

**Le navigateur n'affiche pas les modifications :** vérifier que Vite tourne toujours dans le terminal. Si ce n'est pas le cas, relancer avec `npm run dev`.

**Copilot ne répond pas :** vérifier que la connexion au compte GitHub est active — icône de profil en bas à gauche de VS Code.

**Le MCP Figma ne se connecte pas :** redémarrer VS Code et Figma, puis relancer le serveur depuis le panneau MCP.

**Une classe CSS ne fonctionne pas :** vérifier l'orthographe exacte — une faute de frappe suffit à casser un style. Consulter la liste complète des classes dans `llms.txt`.
