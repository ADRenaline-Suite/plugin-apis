# Operaciones

<p align="right">Idioma:&emsp;<a href="operations.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 APIs](../../../README.md)

Un cliente no puede ver qué llamada corresponde al caso de uso, o la ruta es un verbo.

## Pasos

1. Nombra el caso de uso. Una operación es un paso que el cliente debe llamar, no cada línea del escenario.
2. El método sale de RFC 9110. GET y HEAD son seguros. PUT y DELETE son idempotentes. POST no lo es, salvo que el contrato añada una clave de idempotencia y la persona la haya pedido.
3. La ruta es un sustantivo en plural para una colección (`/orders`) y el mismo sustantivo más un id para un ítem (`/orders/{orderId}`). Un segundo nivel es la relación que el caso de uso necesita (`/customers/{customerId}/orders`). Ahí se detiene. Las relaciones siguientes son enlaces en el cuerpo, no `/a/{id}/b/{id}/c/{id}`.
4. Usa la palabra del producto. El mismo concepto conserva el mismo nombre. No dejes salir un nombre de tabla o de clase.
5. La entrada y la salida nombran los campos que el caso de uso ya usa. No añadas un campo para que el esquema se vea completo.
6. Declara `openapi: 3.2.1`.

## Reglas

1. El esquema de autenticación se copia de un requisito de `plugin-security`. Si falta, el título es un hueco.
2. Una clave de idempotencia está presente solo si la persona la pidió. El nombre que ella usó es el nombre del contrato.

## Plantilla

## Caso de uso

## Operación

## Método

## Ruta

## Idempotente

## Entrada

## Salida

## Esquema de autenticación

## Assumed

## Done

- [ ] El caso de uso o la fuente que esta pieza pide está nombrada, o el archivo no se escribió.
- [ ] Cada título de arriba está lleno o marcado como hueco. `proposed` si queda un hueco.
- [ ] No se inventó nada: ni un campo, ni un error, ni una fecha, ni un rol, ni una base legal.
- [ ] La subcarpeta del asunto y `STATUS.md` siguen el skill.

Cierra la respuesta con qué se escribió, dónde, y qué sigue siendo un hueco.
