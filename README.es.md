<p align="right">Idioma:&emsp;<a href="README.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

# APIs (`plugin-apis`)

Escribe el contrato HTTP de un caso de uso: las operaciones, los errores en problem details y la política de versión.

Las instrucciones están en inglés. El archivo que guarda el plugin sigue el idioma del pedido. Los archivos van en `adrenaline/apis/`.

## /api-operations

Método, ruta, entrada, salida y si la llamada es idempotente. La ruta es un sustantivo en plural. Una relación más profunda es un enlace, no otro tramo de ruta.

## /api-errors

Estado y un cuerpo problem details para cada extensión del caso de uso que cambia el camino del cliente.

## /api-version

Dónde vive la versión, qué rompe a un cliente viejo y cómo conviven dos versiones. Si nadie eligió, el archivo anota versión en la ruta bajo Assumed.

## Ayuda

## /api-help

El catálogo de este plugin. No escribe un archivo.

## Para quién es

Quien necesita el contrato que un cliente va a llamar. El caso de uso queda en `plugin-project-manager`. La amenaza y el control verificable quedan en `plugin-security`. El agregado queda en `plugin-backend`. La página para el lector queda en `plugin-documentation`. Este plugin no copia sus skills.

## Qué incluye

Portable, para cualquier agente que siga [Agent Skills](https://agentskills.io/specification):

- `define-contract` escribe el contrato.

Cursor y Claude Code: los commands de arriba. En Cursor, `/api-operations`. En Claude Code, `/plugin-apis:api-operations`.

Solo Cursor: las rules `output-folder`, `contract-needs-use-case`. Claude Code no carga rules. Las mismas restricciones están en los skills.

## Instalar

En Cursor, instala el plugin desde este repositorio en Customize.

En Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-apis
claude plugin install plugin-apis@plugin-apis
```

Para probar una copia local, arranca Claude Code con `claude --plugin-dir <ruta de este repositorio>`.

## Ejemplo

Pide `/api-operations` y nombra el caso de uso. El archivo lista cada llamada que el cliente debe hacer. Un esquema de autenticación que falta queda en hueco hasta que `plugin-security` lo haya escrito.

## Configuración

Los archivos van en `adrenaline/apis/`. La clave `outputDirs["plugin-apis"]` de `.cursor/adrenaline.json` sustituye esa ruta cuando es relativa y no lleva `..`. Un servicio nombrado va en `<subject>/`.

## Licencia

MIT. Copyright (c) 2026 Ricardo Plascencia.

