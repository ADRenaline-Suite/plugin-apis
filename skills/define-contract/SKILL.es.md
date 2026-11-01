---
name: define-contract
description: Escribe el contrato HTTP de un caso de uso: operaciones, errores y la política de versión.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 APIs](../../README.md)

# Escribe el contrato HTTP de un caso de uso: operaciones, errores y la política de versión

Un contrato para el caso de uso que este turno nombra. El documento es OpenAPI. Las rutas son recursos. Los errores son problem details cuando el estilo es HTTP y JSON.

Source: OpenAPI Specification 3.2.1 (10 de septiembre de 2026). RFC 9110. RFC 9457. El nombre de los recursos sigue la práctica que Microsoft documenta para APIs web y las Azure API Guidelines: sustantivos en plural para colecciones, el mismo nombre para el mismo concepto, rutas poco profundas, enlaces en lugar de una cadena profunda.

## Antes de escribir

1. Lee solo la referencia que nombra este command: [operations](references/operations.md), [errors](references/errors.md) o [version](references/version.md).
2. El caso de uso es un archivo aceptado, o el caso que la persona dice en este turno. Sin eso, no escribas nada.
3. Gana la política de versión que la persona ya eligió. Si no hay ninguna, anota versión en la ruta bajo Assumed y di que `/api-version` la sustituye.

References: [operations](references/operations.md), [errors](references/errors.md), [version](references/version.md).

## Entrega

Cada archivo de este skill va en `adrenaline/apis/`, o en `outputDirs["plugin-apis"]` si `.cursor/adrenaline.json` da una ruta relativa válida. Si `adrenaline/apis/` aún no existe y `apis/` en la raíz del proyecto ya tiene el `ORIGIN.json` o el `STATUS.md` de este plugin, sigue escribiendo ahí y dilo.

Si la persona nombra un proyecto, una app, un servicio o un dominio, el archivo de ese asunto va en `<subject>/`. Un archivo de todo el producto se queda en la raíz de la salida. `<NNN>` es el siguiente número libre en toda la carpeta. La celda `archivo` es `<subject>/<file>` cuando hay asunto (`doc/arch/adr-008-asunto-subcarpeta.md`).

Escribe `ORIGIN.json` junto a `STATUS.md` al crear la carpeta, y otra vez solo si falta o un campo difiere. Campos: `suite` `ADRenaline-Suite`, `plugin` `plugin-apis`, `repository` `https://github.com/ADRenaline-Suite/plugin-apis`, `convention` `adr-001`. No es un archivo `<NNN>` y no tiene fila en `STATUS.md`.

No inventes un dato que la persona no dio. Un título obligatorio sin dato queda como hueco y el archivo sigue `proposed`. "None." llena un título.

## Done

- [ ] Solo se aplicó la referencia de este command.
- [ ] La carpeta de salida, la subcarpeta del asunto, `ORIGIN.json` y `STATUS.md` coinciden con las reglas de entrega.
- [ ] Un dato obligatorio que falta es un hueco. El archivo sigue `proposed`.

## Example

Un pedido que nombra la pieza y su fuente escribe un archivo. Un pedido sin esa fuente no escribe nada y nombra el hueco.
