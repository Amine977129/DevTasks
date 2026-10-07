# DevTasks

## Descripció

**DevTasks** és una aplicació web de gestió de tasques desenvolupada amb HTML, CSS i JavaScript.

L'objectiu del projecte és practicar conceptes de desenvolupament web i DevOps, especialment Git, GitHub, Pull Requests, GitHub Actions, proves automatitzades, protecció de la branca principal, Dependabot i desplegament amb GitHub Pages.

L'aplicació permet crear i gestionar tasques i filtrar-les segons el seu estat.

---

## Instal·lació

Per instal·lar el projecte localment, cal tenir **Node.js** instal·lat.

Clona el repositori:

```bash
git clone https://github.com/Amine977129/DevTasks.git
```

Entra al directori del projecte:

```bash
cd DevTasks
```

Instal·la les dependències:

```bash
npm install
```

---

## Tests

El projecte utilitza **Vitest** per executar les proves automatitzades.

Per executar els tests:

```bash
npm test
```

També es pot utilitzar el mode de desenvolupament dels tests:

```bash
npm run test:watch
```

Els tests comproven principalment les funcionalitats relacionades amb la gestió i validació de tasques.

---

## GitHub Actions

El projecte utilitza **GitHub Actions** per automatitzar diferents processos.

### CI

El workflow `ci.yml` s'executa quan es crea o actualitza un Pull Request cap a `main`.

Realitza els passos següents:

1. Descarrega el repositori.
2. Configura Node.js.
3. Instal·la les dependències.
4. Executa els tests amb `npm test`.

D'aquesta manera, es comprova automàticament que els canvis no trenquen el projecte.

### Deploy

El workflow `deploy.yml` s'executa quan hi ha un canvi a la branca `main`.

S'encarrega de publicar automàticament l'aplicació mitjançant **GitHub Pages**.

---

## Pull Requests

El projecte utilitza un flux de treball basat en branques i Pull Requests.

Els canvis es desenvolupen en branques separades de `main`.

Abans d'integrar els canvis:

1. Es crea una branca de funcionalitat.
2. Es fan els canvis i els commits.
3. Es crea un Pull Request cap a `main`.
4. GitHub Actions executa els tests.
5. Si els tests són correctes, el Pull Request es pot integrar.
6. Els canvis arriben finalment a `main`.

La branca `main` està protegida per evitar canvis directes i garantir un procés d'integració controlat.

---

## Deploy

L'aplicació està publicada amb **GitHub Pages**.

**Web publicada:**

https://amine977129.github.io/DevTasks/

Cada canvi integrat a `main` pot activar automàticament el workflow de desplegament.

---

## Dependències

Les dependències del projecte es gestionen amb **npm**.

El projecte utilitza **Dependabot** per comprovar periòdicament les actualitzacions de:

* Dependències npm del projecte.
* Dependències utilitzades pels GitHub Actions.

La configuració es troba al fitxer:

```text
.github/dependabot.yml
```

Dependabot pot crear Pull Requests automàticament quan detecta actualitzacions disponibles.

---

## Arquitectura

El projecte separa la lògica de l'aplicació de la interfície i de les proves.

### `app.js`

`app.js` gestiona principalment la interfície de l'aplicació i la interacció amb el DOM.

S'encarrega de:

* Gestionar els esdeveniments de la interfície.
* Llegir les dades introduïdes per l'usuari.
* Actualitzar la interfície.
* Mostrar i filtrar les tasques.

### `taskManager.js`

`taskManager.js` conté la lògica relacionada amb la gestió de les tasques.

Inclou funcions per:

* Crear tasques.
* Validar tasques.
* Filtrar tasques.
* Calcular estadístiques.

Aquesta separació permet mantenir la lògica de negoci independent de la interfície.

### `tests/`

La carpeta `tests/` conté les proves automatitzades del projecte.

Les proves comproven que les funcions principals de `taskManager.js` funcionen correctament.

Aquesta separació facilita el manteniment del projecte i permet detectar errors abans d'integrar els canvis a `main`.

---

## Estructura principal

```text
DevTasks/
│
├── .github/
│   └── workflows/
│       ├── ci.yml
│       └── deploy.yml
│
├── js/
│   ├── app.js
│   └── taskManager.js
│
├── tests/
│   └── app.test.js
│
├── .github/
│   └── dependabot.yml
│
├── index.html
├── style.css
├── package.json
├── package-lock.json
└── README.md
```

## Tecnologies

* HTML
* CSS
* JavaScript
* Node.js
* npm
* Vitest
* Git
* GitHub
* GitHub Actions
* GitHub Pages
* Dependabot
