<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="README.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

# APIs (`plugin-apis`)

Writes the HTTP contract for one use case: the operations, the problem-details errors, and the version policy.

The instructions are in English. The file the plugin saves follows the language of the request. Files go in `adrenaline/apis/`.

## /api-operations

Method, path, input, output, and whether the call is idempotent. The path is a plural noun. A deeper relation is a link, not another path segment.

## /api-errors

Status and a problem-details body for each use-case extension that changes the client's path.

## /api-version

Where the version lives, what breaks an old client, and how two versions coexist. If nobody chose, the file records path versioning under Assumed.

## Help

## /api-help

The catalog of this plugin. It does not write a file.

## Who it is for

Someone who needs the contract a client will call. The use case stays with `plugin-project-manager`. The threat and the verifiable control stay with `plugin-security`. The aggregate stays with `plugin-backend`. The reader-facing page stays with `plugin-documentation`. This plugin does not copy their skills.

## What it includes

Portable, for any agent that follows [Agent Skills](https://agentskills.io/specification):

- `define-contract` writes the contract.

Cursor and Claude Code: the commands above. In Cursor, `/api-operations`. In Claude Code, `/plugin-apis:api-operations`.

Cursor only: rules `output-folder`, `contract-needs-use-case`. Claude Code does not load rules. The same restrictions are in the skills.

## Install

In Cursor, install the plugin from this repository in Customize.

In Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-apis
claude plugin install plugin-apis@plugin-apis
```

To try a local copy, start Claude Code with `claude --plugin-dir <path to this repository>`.

## Example

Ask `/api-operations` and name the use case. The file lists each call the client must make. A missing authentication scheme stays a gap until `plugin-security` has written it.

## Configuration

Files go in `adrenaline/apis/`. A `.cursor/adrenaline.json` key `outputDirs["plugin-apis"]` replaces that path when it is a relative path without `..`. One named service goes in `<subject>/`.

## License

MIT. Copyright (c) 2026 Ricardo Plascencia.

