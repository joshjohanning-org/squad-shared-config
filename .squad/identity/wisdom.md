# Team Wisdom

Reusable, organization-wide patterns and heuristics. Each entry is a distilled, actionable insight.

## Patterns

- **Read before writing.** Search for an existing helper, convention, or pattern before introducing a new one.
- **Smallest safe change.** Prefer surgical edits over broad rewrites; leave unrelated code alone.
- **Verify, then claim.** Run the relevant tests or build before reporting work as done.
- **Record the why.** When a non-obvious trade-off is made, capture it in `decisions.md`.

## Anti-patterns

- Committing generated files or local runtime state.
- Disabling tests or linters to make a build pass.
