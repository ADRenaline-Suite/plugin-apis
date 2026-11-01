# Operations

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="operations.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 APIs](../../../README.md)

A client cannot tell which call matches the use case, or the path is a verb.

## Steps

1. Name the use case. One operation is one step the client must call, not every line of the scenario.
2. Method comes from RFC 9110. GET and HEAD are safe. PUT and DELETE are idempotent. POST is not, unless the contract adds an idempotency key and the person asked for that key.
3. Path is a plural noun for a collection (`/orders`) and the same noun plus an id for one item (`/orders/{orderId}`). A second level is the relation the use case needs (`/customers/{customerId}/orders`). Stop there. Further relations are links in the body, not `/a/{id}/b/{id}/c/{id}`.
4. Use the product's word. The same concept keeps the same name. Do not leak a table name or a class name.
5. Input and output name the fields the use case already uses. Do not add a field to make the schema look complete.
6. Declare `openapi: 3.2.1`.

## Rules

1. Auth scheme is copied from a `plugin-security` requirement. If it is missing, the heading is a gap.
2. An idempotency key is present only when the person asked for it. The field name they used is the name in the contract.

## Template

## Use case

## Operation

## Method

## Path

## Idempotent

## Input

## Output

## Auth scheme

## Assumed

## Done

- [ ] The use case or the source this piece requires is named, or the file was not written.
- [ ] Every heading above is filled or marked as a gap. `proposed` when a gap remains.
- [ ] Nothing was invented: no field, no error, no date, no role, no legal basis.
- [ ] The subject folder and `STATUS.md` follow the skill.

Close the reply with what was written, where, and what is still a gap.
