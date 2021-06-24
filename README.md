# heroku-nodejs-boilerplate

Ein Leitfaden zum Aufsetzen eines eigenen Nodejs-App Repository (!fork) für heroku. 

Das Original dieser Ableitung: [heroku/node-js-getting-started](https://github.com/heroku/node-js-getting-started)

Online-Anleitung von heroku: [Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs)


## Heroku`s boilerplate via Github-Importer kopieren

Über das erste Formularfeld des [Github-Importers](https://github.com/new/import) dieses Quell-Repository eingeben:

```sh
https://github.com/heroku/node-js-getting-started.git
```
danach die Ziel-Repository Details eingeben, fertig!


# Heroku login
Make sure you have [Node.js](http://nodejs.org/) and the [Heroku CLI](https://cli.heroku.com/) installed.

```sh
$ heroku login
```

## Running Locally

Jetzt können wir das eben kopierte Repository über unser eigenes Github-Konto klonen und direkt damit arbeiten.

```sh
$ git clone https://github.com/<your-username>/<repo-name>.git
$ cd repo-name
$ npm install
$ npm start  # oder $ heroku local
```

Your app should now be running on [localhost:5000](http://localhost:5000/).

## Create App-Container on Heroku
via ps:scale den plan skalieren
+ web=1: free
+ web=2: hobby (7$/month)
+ [Preise Heroku](https://www.heroku.com/pricing)

```sh
$ heroku create custom-app-name
$ git push heroku main
$ heroku ps:scale web=1
$ heroku open
```

## Work & Deploying to Heroku

```sh
$ npm install
# dev:local (commit/push via git cli)
$ git add .
$ git commit -m "Add cool API"
$ git push -u origin main
# prod:heroku (deploy)
$ git push heroku main
$ heroku open
```

## Heroku 
or

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Documentation

For more information about using Node.js on Heroku, see these Dev Center articles:

- [Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs)
- [Heroku Node.js Support](https://devcenter.heroku.com/articles/nodejs-support)
- [Node.js on Heroku](https://devcenter.heroku.com/categories/nodejs)
- [Best Practices for Node.js Development](https://devcenter.heroku.com/articles/node-best-practices)
- [Using WebSockets on Heroku with Node.js](https://devcenter.heroku.com/articles/node-websockets)
