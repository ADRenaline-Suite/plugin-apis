# Errors

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="errors.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 APIs](../../../README.md)

Clients branch on a different body every time, or the message leaks an internal detail.

## Steps

1. Each error that changes the client's path names the use-case extension it comes from.
2. Status is the RFC 9110 code: 400 or 422 for a rejected body, 401 when the caller is not authenticated, 403 when they are authenticated and not allowed, 404 when the resource is not there, 409 for a conflict, 429 when a limit was asked for.
3. With HTTP and JSON the body is `application/problem+json` (RFC 9457): `type`, `title`, `status`, `detail`, `instance`. `detail` says what the client can do next. It does not name a table, a stack frame, or a query.
4. Do not invent an error the use case does not have.

## Rules

1. `type` is a URI the person chose, or a gap. Do not mint a documentation site.

## Template

## Use case

## Extension

## Status

## Type

## Title

## Detail

## Assumed

## Done

- [ ] The use case or the source this piece requires is named, or the file was not written.
- [ ] Every heading above is filled or marked as a gap. `proposed` when a gap remains.
- [ ] Nothing was invented: no field, no error, no date, no role, no legal basis.
- [ ] The subject folder and `STATUS.md` follow the skill.

Close the reply with what was written, where, and what is still a gap.
