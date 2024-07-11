# LTI - Sistema de Seguimiento de Talento (ATS)

## Descripción
LTI es un sistema de seguimiento de talento desarrollado con TypeScript. El frontend utiliza React y el backend está construido con Node, Express y PostgreSQL. Seguimos los principios de Diseño Dirigido por el Dominio (DDD) y Desarrollo Dirigido por Pruebas (TDD).

## Tecnologías
- TypeScript
- React
- Node.js
- Express
- PostgreSQL

## Principios
- Diseño Dirigido por el Dominio (DDD)
- Desarrollo Dirigido por Pruebas (TDD)

## Estructura de Directorios

La estructura de directorios del proyecto es la siguiente:

```
backend/
└── src/
    ├── application/
    │   ├── dto/
    │   └── use-cases/
    ├── domain/
    │   ├── entities/
    │   ├── repositories/
    │   ├── services/
    │   └── value-objects/
    ├── infrastructure/
    │   ├── persistence/
    │   └── services/
    └── interfaces/
        ├── cli/
        └── http/
```

### Descripción de Directorios

- **application/**: Contiene la lógica de aplicación y casos de uso.
  - **dto/**: Objetos de transferencia de datos.
  - **use-cases/**: Casos de uso de la aplicación.

- **domain/**: Contiene el modelo de dominio.
  - **entities/**: Entidades del dominio con identidad única.
  - **repositories/**: Interfaces para acceder y manipular agregados.
  - **services/**: Servicios de dominio que encapsulan lógica de negocio.
  - **value-objects/**: Objetos de valor definidos por sus atributos.

- **infrastructure/**: Detalles técnicos como persistencia de datos y servicios externos.
  - **persistence/**: Implementaciones de repositorios y acceso a datos.
  - **services/**: Implementaciones de servicios de infraestructura.

- **interfaces/**: Define cómo los usuarios y otros sistemas interactúan con la aplicación.
  - **cli/**: Interfaces de línea de comandos.
  - **http/**: APIs HTTP.

## Archivos en `.gitignore`

El archivo `.gitignore` contiene las siguientes entradas para excluir archivos y directorios no deseados del control de versiones:

```
node_modules/
dist/
.env
*.log
coverage/
```

- **node_modules/**: Directorio donde npm instala las dependencias.
- **dist/**: Directorio de salida para archivos compilados.
- **.env**: Archivos de configuración de entorno.
- ***.log**: Archivos de registro.
- **coverage/**: Directorio de informes de cobertura de pruebas.

## Pruebas

Las pruebas se encuentran en el directorio `src/` y utilizan Jest como framework de pruebas. Los comandos relevantes en `package.json` son:

```json
"scripts": {
  "test": "jest",
  "test:watch": "jest --watch"
}
```

Para ejecutar las pruebas, usa el siguiente comando:

```sh
npm test
```

## Módulos

El proyecto utiliza varios módulos y dependencias, que se especifican en `package.json`. Algunas de las dependencias clave son:

- **express**: Framework web para Node.js.
- **jest**: Framework de pruebas.
- **supertest**: Librería para pruebas de integración de APIs.
- **typescript**: Lenguaje de programación que extiende JavaScript.

## Configuración de TypeScript

El archivo `tsconfig.json` contiene la configuración de TypeScript:

```json
{
  "compilerOptions": {
    "module": "commonjs",
    "target": "es6",
    "outDir": "./dist",
    "rootDir": "./src",
    "strict": true,
    "esModuleInterop": true
  },
  "include": ["src/**/*.ts"],
  "exclude": ["node_modules"]
}
```

## Ejecución del Proyecto

Para iniciar el proyecto en modo desarrollo, usa el siguiente comando:

```sh
npm run dev
```

Para iniciar el proyecto en modo producción, usa el siguiente comando:

```sh
npm start
```

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir cualquier cambio que desees realizar.