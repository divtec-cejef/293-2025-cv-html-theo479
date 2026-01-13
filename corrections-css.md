## A) Normalize.css : le mettre en local (consigne)

Actuellement, vous chargez Normalize via CDN :
```

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css"/>
```

À corriger :

* télécharger `normalize.css` et le placer en `./css/normalize.css`
* le lier en local :
```

<link rel="stylesheet" href="./css/normalize.css">
```

💡 *En local, votre site fonctionne sans dépendances externes.*

> *Un projet propre évite les ressources critiques “à distance”.*

---

## B) Corriger les `id` (éviter majuscules + accents)

Actuellement, vos ancres contiennent des majuscules et des accents :
```
id="Expérience"
id="Compétences"
id="Formation"
```

À corriger :

* utiliser uniquement minuscules, sans accents, sans espaces
  Exemple :
```

<h2 id="experience">Mon Expérience</h2>
<h2 id="competences">Mes Compétences</h2>
<h2 id="formation">Ma Formation</h2>
```

Et mettre à jour le menu :
```
<a href="#experience">Mon Expérience</a> <a href="#competences">Mes Compétences</a> <a href="#formation">Ma Formation</a>
```

---

## C) Retirer le CSS inline sur l’image (style="...")

Actuellement :
```
<img ... style="width:150px; border-radius:10px;">
```

À corriger :

* créer une classe et mettre le style dans `main.css`

Exemple HTML :
```
<img class="photo-profil" src="cv/OIP.webp" alt="Photo de profil">
```

Exemple CSS :
```
.photo-profil {
width: 150px;
border-radius: 10px;
height: auto;
}
```

💡 *Le style ne doit pas être dans le HTML.*

> *HTML = structure, CSS = mise en forme.*

---

## D) Ajouter `em` et `rem` (consigne)

Vous avez du `px` ✅
Il manque :

* une taille en `em`
* une taille en `rem`

Exemple :
```
h2 {
font-size: 1.5em; /* em */
}

p {
font-size: 1rem; /* rem */
}
```

💡 *L’exercice demande les 3 unités pour comprendre leurs différences.*

> *`px` = fixe, `em` = relatif au parent, `rem` = relatif à la racine.*

---

## E) Nettoyer le CSS : doublons et propriétés répétées

Vous avez plusieurs blocs `body { ... }` séparés, et dans `h1` vous avez `padding` deux fois.

Exemple :
```
body { max-width: 400px; margin: auto; }
body { background-image: ... }
body { font-family: ... }
```

À corriger :

* regrouper en un seul bloc `body` (plus lisible)
* garder un seul `padding` dans `h1`

💡 *Un CSS regroupé est plus simple à maintenir et évite les confusions.*

---

## G) Remplacer les `<br>` par des listes (HTML plus propre)

Actuellement vous simulez une liste avec des tirets + `<br>` :
```

<p>- ...<br>- ...</p>
```

À corriger :

* utiliser un vrai `<ul><li>...</li></ul>`

Exemple :
```

<ul>
  <li>J'ai sauvé la map...</li>
  <li>J'ai participé à...</li>
</ul>
```

💡 *Les listes HTML sont faites pour ça.*

> *Une structure sémantique aide aussi l’accessibilité.*
