# IRTS Parmentier — Ateliers « Automatiser avec l'IA »

Site statique regroupant les supports d'atelier IRTS Parmentier. Aucune dépendance, aucun build : ce sont des fichiers HTML autonomes.

## Pages

| Fichier | Description |
|---|---|
| `index.html` | **Fiche atelier individuelle** — cartographie des cas d'usage IA. Identité (prénom / service / date), liste de tâches chronophages avec ajout/suppression illimité, matrice impact × faisabilité, analyse du cas d'usage prioritaire, restitution. Sauvegarde automatique dans le navigateur. Export PDF via le bouton (impression). |
| `cartographie.html` | **Cartographie des process** — éditeur visuel : ajout de cartes (logiciel, action, donnée, décision, acteur), déplacement à la souris, création de flèches reliant les cartes (avec libellés), légende par catégorie. Sauvegarde automatique, export PDF. |
| `logo-irts.png` | Logo IRTS Parmentier utilisé par les deux pages. |

Les données saisies sont stockées **localement** (`localStorage`) dans le navigateur de l'utilisateur — rien n'est envoyé sur un serveur.

## Hébergement sur Render

Le dépôt contient un blueprint `render.yaml` (site statique). Deux façons de déployer :

**A. Via le blueprint (recommandé)**
1. Sur [dashboard.render.com](https://dashboard.render.com) → **New +** → **Blueprint**.
2. Sélectionner ce dépôt GitHub. Render lit `render.yaml` et crée un **Static Site** servant la racine du dépôt.
3. La page d'accueil est `index.html` (servie automatiquement).

**B. Manuellement**
1. **New +** → **Static Site** → connecter ce dépôt.
2. *Build Command* : (vide) — *Publish Directory* : `.`
3. Déployer.

> Important : la page d'accueil doit s'appeler **`index.html`**. C'est pourquoi la fiche a été renommée depuis l'ancien fichier `Fiche Atelier IRTS (autonome).html` (que Render ne pouvait pas servir par défaut).

## Développement local

Ouvrir simplement les fichiers `.html` dans un navigateur, ou lancer un petit serveur :

```bash
python3 -m http.server 8000
# puis http://localhost:8000
```
