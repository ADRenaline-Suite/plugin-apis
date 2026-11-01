# Política de versión

<p align="right">Idioma:&emsp;<a href="version.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 APIs](../../../README.md)

Un cambio que rompe sale sin un lugar donde el cliente viejo pueda seguir llamando.

## Pasos

1. Ninguna norma obliga a poner la versión en la ruta, en una cabecera o en el tipo de medio. Escribe la política que la persona eligió y la razón.
2. Si no eligió, anota versión en la ruta (`/v1`) bajo Assumed. Di que `/api-version` la sustituye. Es la forma que más APIs HTTP públicas publican, incluida la guía de Azure de versionar desde la primera entrega. No es un requisito de OpenAPI.
3. Un cambio que rompe es uno que un cliente existente no puede ignorar: un campo quitado o renombrado, una operación quitada, un significado cambiado. Un campo opcional añadido no rompe si los clientes ignoran campos desconocidos. Di cuál de los dos es este cambio.
4. Nombra cuánto tiempo permanece la versión anterior solo si la persona lo dijo. Si no, ese título es `None.`

## Reglas

1. No retires una versión que la persona no retiró.

## Plantilla

## Política

## Por qué

## Cambio que rompe

## Versión anterior

## Assumed

## Done

- [ ] El caso de uso o la fuente que esta pieza pide está nombrada, o el archivo no se escribió.
- [ ] Cada título de arriba está lleno o marcado como hueco. `proposed` si queda un hueco.
- [ ] No se inventó nada: ni un campo, ni un error, ni una fecha, ni un rol, ni una base legal.
- [ ] La subcarpeta del asunto y `STATUS.md` siguen el skill.

Cierra la respuesta con qué se escribió, dónde, y qué sigue siendo un hueco.
