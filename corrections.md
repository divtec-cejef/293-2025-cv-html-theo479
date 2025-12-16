## A) Normalize.css doit être en local
- Vous utilisez Normalize via un CDN
- Veuillez le télécharger et le placer en local dans `./css/normalize.css`
- Puis corriger le `<head>` :
```
<link rel="stylesheet" href="./css/normalize.css">
<link rel="stylesheet" href="./css/main.css">
```

## B) Déplacer la photo dans le dossier `img/`
- Votre image est dans `cv/`, mais l’exercice impose `img/`
- Veuillez déplacer `OIP.webp` dans `./img/` et corriger les chemins

## C) Photo cliquable : ajouter la sécurité `rel`
- Votre lien utilise `target="_blank"`
- Veuillez ajouter `rel="noopener noreferrer"`
- Exemple :
```
<a href="./img/OIP.webp" target="_blank" rel="noopener noreferrer">
  <img src="./img/OIP.webp" alt="Photo de profil">
</a>
```

## D) Favicons : à la racine et avec `./`
- Vos favicons sont référencés via `cv/favicon-...`
- Veuillez mettre les favicons à la racine et les référencer avec `./...`
- Exemple :
```
<link rel="icon" type="image/png" sizes="32x32" href="./favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="./favicon-16x16.png">
```

## E) Retirer les styles inline (mettre dans `main.css`)
- Vous avez du style directement dans le HTML sur l’image (`style="..."`)
- Veuillez déplacer ces styles dans `./css/main.css`

## F) Corriger les `id` (bonne pratique)
- Évitez les majuscules et accents dans les `id`
- Exemple recommandé :
  - `experience`
  - `competences`
  - `formation`
- Et mettez à jour le menu (`href="#..."`) en conséquence

## G) Utiliser des listes HTML au lieu de tirets dans un paragraphe
- Au lieu de mettre `- ...<br>`, veuillez utiliser une liste :
```
<ul>
  <li>...</li>
  <li>...</li>
</ul>
```

## Autres
- Attention à l'indentation et à la lisibilité du code
- balise `meta` dans le `head` pour la description à remplir
- essayez d'utiliser des `<strong>` dans certains texte pour mettre en valeur du contenu (par exemple, autour de `le point zéro`
- 
