# REST API

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-   les verbes HTTP ✔️ -> Les 4 principaux : `POST GET PUT DELETE`
-   les statuts HTTP ✔️ ->

1. Informationnels : `100-199`
1. Succes : `200-299`
1. Redirection : `300-399`
1. Erreur client : `400-499`
1. Erreur Serveur : `500-599`
   [source](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

-   les endpoints ✔️ -> C'est le terme pour les différentes URLs pour accéder aux différentes ressource
-   CORS ✔️ -> Cross Origin Resource Sharing : Un header HTTP qui permet au serveur de lister ou de décrire les origines (URLs) des requêtes qui ont la permission d'accéder à ses ressources depuis un navigateur web
-   la nomenclature recommandée pour les routes ✔️ -> Il faut utiliser des noms qui soient le plus représentatifs possible des entités que l' endpoint va récupérer.

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
// import d'un framework. Ici node/express
const express = require('express')
const bodyParser = require('body-parser')

const app = express()

app.use(bodyParser.json())

// Declaration de la route qui permet de récupérer tous les articles : GET '/articles'
app.get('/articles', (req, res) => {
	const articles = []
	// code pour récupérer tous les articles de la db
	res.status(200).send(articles)
})

// Declaration de la route qui permet d'ajouter un nouvel article : POST '/articles'
app.post('/articles', (req, res) => {
	// code pour ajouter un nouvel article...
	const newArticle = () => {
		return result
	}
	res.status(201).send(newArticle)
})
```

### Utilisation dans un projet ❌ / ✔️

[interne-atalante](https://github.com/Holmes-EH/interne-atalante/tree/main/api)

Description :
Ceci est un début de création d'un site intranet full stack. Le lien ci-dessus pointe vers le dossier contenant l'api rest. Codé en PHP orienté objet. Database : MySQL en localhost connecté avec PDO_MySQL.  
Le frontend est en React

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### La doc MDN

-   https://developer.mozilla.org/en-US/docs/Web/HTTP

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

-   action 1 ❌ / ✔️
-   action 2 ❌ / ✔️
-   ...

Résolution :

## 📽️ J'en fais la démonstration

-   J'ai ecrit un [tutoriel](...) ❌ / ✔️
-   J'ai fait une [présentation](...) ❌ / ✔️
