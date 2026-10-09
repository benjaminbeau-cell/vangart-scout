# Méthode Scout v2

## Score (sur 100)

score = 10 × (0,35 × Brodabilité + 0,30 × Bankabilité + 0,20 × Impact + 0,15 × Test rapide) − malus

| Critère | Poids | Ce qui est regardé |
|---|---|---|
| Brodabilité | 35 % | Formes lisibles, contours nets, peu de couleurs de fil, peu de dégradés fins ou d'effets photo, matière traduisible en points |
| Bankabilité | 30 % | Engagement du post comparé à la médiane du compte, actualité (galerie, musée, foire), série phare, éditions déjà faites |
| Impact visuel | 20 % | Force de l'image au format édition (50 à 80 cm) et en vignette |
| Test rapide | 15 % | Un seul panneau, format raisonnable, points et changements de fil estimés |

Notes de 0 à 10 (demi-points permis). Malus : non-œuvre ou logo (~8), droits partagés (~5), image floue (~3).

Exclus d'office : œuvres d'autres artistes, sculptures, installations, vues d'expo illisibles, produits dérivés.

Points et couleurs de fil : ordres de grandeur pour un format d'environ 60 cm.

## Procédure

1. Ouvrir le profil Instagram (connecté, pour voir 30 à 60 posts).
2. Relever pour chaque œuvre : titre, technique, format, année, lieu, date, likes, lien du post.
3. Calculer la médiane des likes ; engagement = likes du post / médiane.
4. Noter, garder les 10 meilleures, recadrer les images sur l'œuvre.
5. Publier le rapport. Benjamin choisit l'œuvre ; aucun mail n'est envoyé sans sa validation.

## Structure d'un rapport (`data/<pseudo>.json`)

`artist`, `url`, `createdAt`, `postsScanned`, `summary`, `excluded`, `works[]` avec `title`, `sub`, `date`, `likes`, `engagement`, `postUrl`, `scores{brod,bank,impact,test}`, `malus`, `colors`, `points`, `flags[]`, `note`, `image`.
