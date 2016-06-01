# sequelize-formly

Un modulo que hace una REST options del schema de la base de datos en formato formly.
NOTA: actualmente la funcionalidad es solo con POSTGRES

## Prerequisites

Lo siguiente es necesario para utilizar el modulo.

    express
    sequelize

## Install

$ npm install sequelize-formly

## Usage

La definicion de ruta es la siguiente:

```
var sequelizeFormly = require('sequelize-formly');
app.options('/hammers', sequelizeFormly.options(Model));
```

o
```
import sequelizeFormly from "sequelize-formly";
app.options('/hammers', sequelizeFormly.options(Model));
```

## API

La ejecucion correcta del modulo retorna 201.
```
app.options('/hammers', sequelizeFormly.options(Model));
```

Ejemplo request
```
OPTIONS /hammers
Content-Type: application/json
{
    "key": "hammers",
    "type": "input",
    "templateOptions": {
      "type": "number",
      "label": "hammers",
      "required": true
    }
}
```
