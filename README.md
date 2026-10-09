# VANGART Scout

Outil de prospection artistes : à partir du compte Instagram d'un artiste, un top 10 des œuvres les plus adaptées à VANGART (brodables et vendables), avec un score détaillé sur 100.

## Contenu

- `index.html` : l'application (une seule page, sans dépendance à installer).
- `data/` : un fichier JSON par artiste analysé + `index.json` (liste des artistes).
- `img/` : images des œuvres (nom = identifiant référencé dans les JSON).
- `METHODE.md` : grille de score et procédure d'analyse.

## Lancer

- En local : `python3 -m http.server` dans ce dossier, puis http://localhost:8000
- En ligne : activer GitHub Pages (Settings > Pages > branche `main`, dossier racine).

Ouvrir `index.html` directement en double-clic ne marche pas : le navigateur bloque la lecture des JSON hors serveur.

## Deux versions

- **Version claude.ai (référence)** : https://claude.ai/artifact/D6HMSqPaweBoioy93kj6yW
  Recherche par lien Instagram, file d'attente, choix de l'œuvre enregistré. Données dans la base de l'artifact.
- **Cette version GitHub** : lecture seule. Elle affiche les rapports présents dans `data/`. La recherche donne le message à envoyer à Claude.

## Ajouter un artiste

1. Déposer `data/<pseudo>.json` (même structure que les fichiers existants) et ses images dans `img/`.
2. Ajouter le pseudo dans `data/index.json`.

Le score total n'est pas stocké : la page le calcule depuis les quatre notes (voir `METHODE.md`).

## Évolution prévue

Brancher la recherche sur Supabase (projet d'Aurélien) : table `requests` (file) et table `reports` (résultats), mêmes champs que les JSON.
