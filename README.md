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

L'aplicació està publicada amb **GitHub Pages**
