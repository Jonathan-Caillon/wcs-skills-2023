# Integration continue

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-   les enjeux de l'integration continue ✔️

L'integration continue permet, de vérifier la qualité du code et de déployer automatiquement le code sur un serveur de production.

-   la mise en place d'une github action ✔️

Avec github, il est possible de créer des actions qui vont s'exécuter en fonction de différents événements sur le repo, comme des pull requests ou alors des push. Ces actions peuvent être des tests, des linters, des déploiements, etc. Il est possible de filtrer les actions en fonction de la branche ou du fichier modifié, ainsi que de réutiliser des actions déjà existantes.

## 💻 J'utilise

### Un exemple personnel commenté ✔️

Cette action qui se lance a chaque push sur chaque branche du repo va lancer les tests. Selon les reglages de github, les tests doivent passer pour que le push soit accepté.

```yml
name: integration-tests-and-deploy

on: push

jobs:
    run-tests:
        runs-on: ubuntu-latest
        steps:
            - name: Check out code
              uses: actions/checkout@v2
            - name: create env file
              run: |
                  touch .env.test
                  echo "NODE_ENV=test
                  PORT=5555
                  JWT_SECRET_KEY=05165447ad9dc0ee73ebd61faeaf0830
                  " >> .env.test
            - name: Run tests
              run: npm i && npm run test
```

### Utilisation dans un projet ✔️

[lien github](https://github.com/WildCodeSchool/2209-wns-rivest-groupe3-back/compare/main...staging)
\
Description : Le repos du backend sur le projet Wild Code School -> Tabas.blog

### Utilisation en production si applicable ❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

[La Doc github..](https://docs.github.com/en/actions)

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
