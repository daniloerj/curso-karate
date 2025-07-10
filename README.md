# curso-karate

Automatización de pruebas de APIs REST usando [Karate DSL](https://github.com/karatelabs/karate) y Maven.

## Descripción

Este proyecto contiene pruebas automatizadas para la API pública [jsonplaceholder](https://jsonplaceholder.typicode.com/), cubriendo escenarios de usuarios, posts, comentarios y más.

## Estructura

- `src/test/java/examples/jsonplaceholder/`: Features de Karate para cada endpoint.
- `Jenkinsfile`: Pipeline para integración continua en Jenkins.
- `.github/workflows/karate.yml`: Workflow para CI en GitHub Actions.

## Ejecución local

```sh
mvn clean test
```

## Integración continua

- **Jenkins:** Usa el Jenkinsfile para ejecutar las pruebas automáticamente.
- **GitHub Actions:** El workflow ejecuta las pruebas en cada push o pull request.

## Requisitos

- Java 11+
- Maven 3.6+

## Autor

Danilo Efrain