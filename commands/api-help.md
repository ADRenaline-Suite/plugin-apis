---
name: api-help
description: "ADRenaline. Help: catalog of plugin-apis (skills, rules, commands)."
---

# Help — ADRenaline APIs

Print this catalog as the reply. Do not run any skill or command. Do not invent entries that are not listed. If a component was added to the plugin and is missing here, add one line from its frontmatter `description` and say the catalog was refreshed.

When this help command is the first command in the message, every command, skill, or rule named after it is the subject of the help. Do not run those names. Do not print the full catalog. For each name, in the order given, print its catalog line (the linked id and the sentence). When the README has a heading for that command, also print the paragraphs under that heading, up to the next heading. A skill name uses the skill's catalog line and the README group that names that skill, up to its first command heading. A name that is not in this catalog is one line: it is not in this plugin. Do not invent what it does, and do not write a file.

Write the sentences in the language of the request. Keep command names, file ids, and every URL unchanged. Every id is a markdown link to the GitHub URL on its line. Do not print a repository `name` as the visible label of a plugin.

Keep the section headings, in this order: Plugin, Commands, Skills, Rules, then Agents, Hooks, and MCP when the plugin has them, then Output, then Not in this plugin. The title and the Plugin line show `ADRenaline` plus the `displayName`, then one sentence on what the plugin does. Under Commands, group the lines by the skill named in the line. Each group opens with that skill name linked to its SKILL.md. One line per item: the linked id, then the sentence. Output links this plugin's GitHub repository under that same label. A plugin under Not in this plugin uses `ADRenaline` plus its short name, and links to `https://github.com/<owner>/<other-plugin>` only when that repository exists.

## Plugin

- [**ADRenaline APIs**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/README.md) — Writes the HTTP contract: each operation, its errors, and how versions coexist.

## Commands

- [**/api-help**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/README.md) — This help (one-line catalog of the plugin).
- [**define-contract**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/skills/define-contract/SKILL.md) — Writes the HTTP contract for one use case: operations, errors, and the version policy.
- [**/api-operations**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/skills/define-contract/references/operations.md) — Operations: method, path, input, output, and idempotency, each traced to a use case.
- [**/api-errors**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/skills/define-contract/references/errors.md) — Errors: status and problem-details body, each tied to a use-case extension.
- [**/api-version**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/skills/define-contract/references/version.md) — Version policy: where the version lives, what breaks, and how two versions coexist.

## Skills

- [**define-contract**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/skills/define-contract/SKILL.md) — Writes the HTTP contract for one use case: operations, errors, and the version policy.

## Rules

- [**output-folder**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/rules/output-folder.mdc) — Every file goes in `adrenaline/apis/` (or in `outputDirs["plugin-apis"]` of `.cursor/adrenaline.json`). The artifact follows the language of the request.
- [**contract-needs-use-case**](https://github.com/ADRenaline-Suite/plugin-apis/blob/main/rules/contract-needs-use-case.mdc) — An operation needs a use case. The threat model, the aggregate, and the reader document stay in their plugins.

## Output

- Repository: [**ADRenaline APIs**](https://github.com/ADRenaline-Suite/plugin-apis).
- Folder: `adrenaline/apis/`. One named subject goes in `<subject>/`. `<NNN>` is monotonic across the whole folder.

## Not in this plugin

- Use case → ADRenaline plugin-project-manager.
- Security requirement → ADRenaline plugin-security.
- Domain model → ADRenaline plugin-backend.
- API reference for readers → ADRenaline plugin-documentation.
