---
name: pull-request-conventions
description: Organization conventions for branches, commit messages, and pull requests. Use when committing, opening, or reviewing a pull request.
---

# Pull request conventions

## Branches

- Name branches `<type>/<short-description>`, for example `feat/login-form` or `fix/null-user-crash`.

## Commits

- Use Conventional Commits: `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`.
- Keep the subject line under 72 characters and in the imperative mood.

## Pull requests

- One logical change per pull request.
- The description includes: what changed, why, how it was tested, and any follow-up work.
- Link the related issue with `Fixes #123` or `Refs #123`.
- A human reviews and merges; agents never merge their own pull requests.
