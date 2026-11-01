# Version policy

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="version.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 APIs](../../../README.md)

A breaking change ships with no place for the old client to keep calling.

## Steps

1. No standard forces the version into the path, a header, or the media type. Write the policy the person chose and the reason.
2. If they did not choose, record path versioning (`/v1`) under Assumed. Say that `/api-version` replaces it. This is the shape most public HTTP APIs ship, including the Azure guidance to version from the first release. It is not a requirement of OpenAPI.
3. A breaking change is one an existing client cannot ignore: a removed or renamed field, a removed operation, a changed meaning. An added optional field is not breaking when clients ignore unknown fields. Say which of the two this change is.
4. Name how long the previous version stays, only if the person said so. Otherwise that heading is `None.`

## Rules

1. Do not retire a version the person did not retire.

## Template

## Policy

## Why

## Breaking change

## Previous version

## Assumed

## Done

- [ ] The use case or the source this piece requires is named, or the file was not written.
- [ ] Every heading above is filled or marked as a gap. `proposed` when a gap remains.
- [ ] Nothing was invented: no field, no error, no date, no role, no legal basis.
- [ ] The subject folder and `STATUS.md` follow the skill.

Close the reply with what was written, where, and what is still a gap.
