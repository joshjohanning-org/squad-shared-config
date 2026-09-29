---
name: testing-standards
description: Organization testing standards. Use when writing, changing, or reviewing tests or any behavior change.
---

# Testing standards

- Every behavior change includes a test that fails without the change and passes with it.
- Prefer fast, deterministic unit tests; add integration tests for boundaries (network, database, file system).
- Do not use real credentials or production services in tests.
- Name tests after the behavior they verify, for example `returns 404 when user is missing`.
- Never delete or skip a failing test to make a build pass; fix the cause or raise it with a human.
