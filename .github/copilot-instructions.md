
# Instruccions de Desenvolupament per a DevTasks

## 1. Arquitectura de Mòduls i Desacoblament

- Tota la lògica de negoci (càlculs, validacions, filtratges) ha d'anar únicament a `js/taskManager.js` utilitzant ES6 Modules (`export`).
- Les funcions de `taskManager.js` han de ser pures, sense referències a `document`, `window` o `localStorage`.
- La manipulació del DOM, els esdeveniments d'interfície i la persistència corresponen exclusivament a `js/app.js`.

## 2. Tests Unitaris Amb Vitest

- Per a qualsevol nova funció o modificació a `taskManager.js`, crea obligatòriament les proves unitàries a `tests/app.test.js` utilitzant Vitest (`describe`, `it`, `expect`).

## 3. Estil i Qualitat de Codi

- Utilitza JavaScript modern (ES6+).
- Escriu funcions clares i utilitza noms de variables descriptius.
- Evita l'ús de variables globals no desitjades.
