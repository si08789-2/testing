# Configuració de l'Entorn de Desenvolupament per JavaScript i Jest

## Pas 1: Instal·lació de Node.js

Abans de començar assegurat de tenir Node.js instal·lat al teu sistema. Jest s'execturaà en un entorn Node.js.

### Windows y Linux

1. Descarrega Node.js des de [Node.js official website](https://nodejs.org/).
2. Segueix les instruccions d'instal·lació.

Per verificar la instal·lació executa:

```bash
node --version
npm --version
```

Aquests comandaments han de mostrar les versions de Node.js i npm (el gestor de paquets de Node.js), respectivament.

## Pas 2: Configuració del Projecte

Crea una nova carpeta per al teu projecte i navega-hi des del terminal.


```bash
mkdir mi-proyecto-jest
cd mi-proyecto-jest
```
Inicialitza un nou projecte de Node.js:

```bash
npm init -y
```

Això crearà un fitxer package.json al teu projecte.

## Pas 3: Instal·lació de Jest

Instal·la Jest utilitzant npm:

```bash
npm install --save-dev jest
```

## Pas 4: Configuració de Jest

Edita el fitxer package.json per afegir un script de proves que utilitzi Jest. Ha de quedar així:

```json
{
  "scripts": {
    "test": "jest"
  }
}
```

## Pas 5: Creació d'Arxius de Proves

Crea fitxers per al teu codi i les proves. Per exemple, per a l'exercici 1:

suma.js

```javascript

function suma(a, b) {
    return a + b;
}
module.exports = suma;
```
suma.test.js

```javascript

const suma = require('./suma');

test('suma 1 + 2 es igual a 3', () => {
    expect(suma(1, 2)).toBe(3);
});
```

Repeteix aquest procés per als altres exercicis.

## Pas 6: Executar les proves

Per executar les teves proves, utilitza el següent comandament al terminal:

```bash
npm test
```


Jest buscarà automàticament arxius amb extensions __.test.js__ o __.spec.js__ y executarà les proves.
