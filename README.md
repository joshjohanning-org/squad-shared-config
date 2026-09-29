# squad-shared-config

A sample **shared [Squad](https://github.com/bradygaster/squad) configuration** that any repository can inherit using `squad upstream`, so teams don't have to copy or zip `.squad/` folders around.

> [!NOTE]
> This is a proof of concept. Squad is alpha software and its commands may change.

## What's shared

| File | Purpose |
|------|---------|
| [`.squad/decisions.md`](.squad/decisions.md) | Organization-wide decisions every team member follows |
| [`.squad/routing.md`](.squad/routing.md) | Role-based routing rules |
| [`.squad/identity/wisdom.md`](.squad/identity/wisdom.md) | Reusable patterns and anti-patterns |
| [`.squad/casting/policy.json`](.squad/casting/policy.json) | Allowed casting universes |
| [`.squad/skills/*/SKILL.md`](.squad/skills) | Shared skills (`pull-request-conventions`, `testing-standards`) |

These are the files Squad's upstream resolver reads. Project-specific state (team roster, agent history, logs) stays in each consuming repository.

## Use it in a repository

### Option 1: Copilot CLI plugin (recommended)

Install the `squad-setup` plugin from [joshjohanning-org/squad-copilot-plugins](https://github.com/joshjohanning-org/squad-copilot-plugins):

```bash
copilot plugin marketplace add joshjohanning-org/squad-copilot-plugins
copilot plugin install squad-setup@squad-copilot-plugins
```

Then, in your repository, start Copilot CLI and run `/init-shared-squad` (or ask "set up the shared squad").

### Option 2: Squad CLI directly

```bash
squad init   # if the repository doesn't have .squad/ yet
squad upstream add https://github.com/joshjohanning-org/squad-shared-config.git --name shared --ref main
squad upstream sync
```

Commit `.squad/upstream.json`. The cached clone in `.squad/_upstream_repos/` is gitignored automatically; teammates run `squad upstream sync` after cloning.

## Update the shared config

1. Open a pull request to this repository.
2. After it merges, consumers run `squad upstream sync` and start a new session.

## Same repository, different branches

If you'd rather not create a separate repository, put these same files on an orphan branch (for example `squad-config`) of your application repository, then from any feature branch run:

```bash
squad upstream add "$(git remote get-url origin)" --name shared --ref squad-config
squad upstream sync
```

Everyone shares the config branch without rebasing their feature branches.
