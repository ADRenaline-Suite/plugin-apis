# Changelog

## [0.0.1] - 2026-11-01

### Added

- HTTP operations traced to a use case, with plural collection paths and idempotency from RFC 9110.
- Errors as RFC 9457 problem details, each tied to a use-case extension.
- A version policy. Path versioning is recorded under Assumed when nobody chose.
- Commands `/api-help`, `/api-operations`, `/api-errors`, and `/api-version`.
