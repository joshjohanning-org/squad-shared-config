# Shared Work Routing

Organization-wide routing guidance. Map these roles to whichever team members exist in the consuming project's `.squad/team.md`.

## Routing Table

| Work Type | Route To (role) | Examples |
|-----------|-----------------|----------|
| Architecture, scope, triage | Lead | Design proposals, issue triage, breaking changes |
| UI and client code | Frontend | Components, styling, accessibility |
| APIs, data, services | Backend | Endpoints, persistence, integrations |
| Tests and quality | Tester | Unit/integration tests, regression checks |
| Docs and changelogs | Scribe | README updates, decision logging |

## Rules

1. Security-sensitive changes (auth, secrets, permissions) always include the Lead for review.
2. Any change touching public APIs routes to the Tester in parallel with implementation.
3. If no member matches a role, route to the Lead.
