# Errores

<p align="right">Idioma:&emsp;<a href="errors.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 APIs](../../../README.md)

Los clientes ramifican con un cuerpo distinto cada vez, o el mensaje deja salir un detalle interno.

## Pasos

1. Cada error que cambia el camino del cliente nombra la extensión del caso de uso de la que sale.
2. El estado es el código de RFC 9110: 400 o 422 para un cuerpo rechazado, 401 si quien llama no está autenticado, 403 si está autenticado y no tiene permiso, 404 si el recurso no está, 409 para un conflicto, 429 si se pidió un límite.
3. Con HTTP y JSON el cuerpo es `application/problem+json` (RFC 9457): `type`, `title`, `status`, `detail`, `instance`. `detail` dice qué puede hacer el cliente después. No nombra una tabla, un marco de pila ni una consulta.
4. No inventes un error que el caso de uso no tiene.

## Reglas

1. `type` es un URI que la persona eligió, o un hueco. No inventes un sitio de documentación.

## Plantilla

## Caso de uso

## Extensión

## Estado

## Type

## Title

## Detail

## Assumed

## Done

- [ ] El caso de uso o la fuente que esta pieza pide está nombrada, o el archivo no se escribió.
- [ ] Cada título de arriba está lleno o marcado como hueco. `proposed` si queda un hueco.
- [ ] No se inventó nada: ni un campo, ni un error, ni una fecha, ni un rol, ni una base legal.
- [ ] La subcarpeta del asunto y `STATUS.md` siguen el skill.

Cierra la respuesta con qué se escribió, dónde, y qué sigue siendo un hueco.
