# Squad Decisions

Organization-wide decisions inherited by every project that adds this repository as a Squad upstream. Projects may add their own decisions or override these in their local `.squad/decisions.md`.

## Active Decisions

### 1. Pull requests are small and single-purpose

Keep each pull request focused on one change. Split refactors from behavior changes.

### 2. Tests accompany behavior changes

Any change to runtime behavior includes or updates automated tests. See the `testing-standards` skill.

### 3. Conventional commit messages

Use Conventional Commits (`feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`). See the `pull-request-conventions` skill.

### 4. Humans approve merges

Agents may open pull requests, but a human reviews and merges them.

### 5. No secrets in the repository

Never commit credentials, tokens, or connection strings. Read them from environment variables or a secret store.

## Governance

- Changes to these shared decisions are made through pull requests to this repository.
- Consuming projects pick up changes by running `squad upstream sync`.
