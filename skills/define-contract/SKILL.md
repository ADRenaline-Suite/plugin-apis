---
name: define-contract
description: Writes the HTTP contract for one use case: operations, errors, and the version policy.
---

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="SKILL.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 APIs](../../README.md)

# Writes the HTTP contract for one use case: operations, errors, and the version policy

One contract for the use case this turn names. The document is OpenAPI. The paths are resources. The errors are problem details when the style is HTTP and JSON.

Source: OpenAPI Specification 3.2.1 (10 September 2026). RFC 9110. RFC 9457. Resource naming follows the practice Microsoft documents for web APIs and the Azure API Guidelines: plural nouns for collections, the same name for the same concept, shallow paths, links instead of a deep chain.

## Before writing

1. Read only the reference this command names: [operations](references/operations.md), [errors](references/errors.md), or [version](references/version.md).
2. The use case is an accepted file, or the case the person states in this turn. Without it, write nothing.
3. A version policy the person already chose wins. If none is chosen, record path versioning under Assumed and say `/api-version` replaces it.

References: [operations](references/operations.md), [errors](references/errors.md), [version](references/version.md).

## Delivery

Every file this skill writes goes in `adrenaline/apis/`, or in `outputDirs["plugin-apis"]` when `.cursor/adrenaline.json` gives a valid relative path. If `adrenaline/apis/` does not exist yet and `apis/` at the project root already has this plugin's `ORIGIN.json` or `STATUS.md`, keep writing there and say so.

When the person names one project, app, service, or domain, put that subject's file in `<subject>/`. A file about the whole product stays at the output root. `<NNN>` is the next free number in the whole output folder. The `archivo` cell is `<subject>/<file>` when there is a subject (`doc/arch/adr-008-asunto-subcarpeta.md`).

Write `ORIGIN.json` beside `STATUS.md` when the folder is created, and again only if it is missing or a field differs. Fields: `suite` `ADRenaline-Suite`, `plugin` `plugin-apis`, `repository` `https://github.com/ADRenaline-Suite/plugin-apis`, `convention` `adr-001`. It is not an `<NNN>` file and it has no row in `STATUS.md`.

Do not invent a fact the person did not give. A required heading with no fact stays a gap and the file stays `proposed`. "None." fills a heading.

## Done

- [ ] Only the reference for this command was applied.
- [ ] The output folder, the subject subfolder, `ORIGIN.json`, and `STATUS.md` match the delivery rules.
- [ ] A missing required fact is a gap. The file stays `proposed`.

## Example

A request that names the piece and its source writes one file. A request missing that source writes nothing and names the gap.
