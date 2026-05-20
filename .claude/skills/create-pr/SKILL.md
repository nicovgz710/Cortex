---
name: create-pr
description: >
  Create a pull request from staged changes. Handles the full workflow: create a
  conventionally-named branch, commit staged changes, push, and open a PR with a
  well-structured title and description. Use this skill whenever the user asks to
  "create a PR", "open a pull request", "submit changes for review", "push this
  as a PR", or any variation of requesting a pull request. Also use it when the
  user says "sube esto como PR", "crea un PR", "abre un pull request", or
  "manda esto a review". If changes are ready and the user wants them reviewed
  by teammates, this is the skill to use.
---

# Create Pull Request

Automate the full PR workflow: branch creation, commit, push, and PR opening
with consistent conventions.

## Core principle

Only staged changes go into the PR. Unstaged changes stay in the working tree
untouched. This gives the user full control over what gets submitted for review.

## Workflow

### 1. Assess the current state

Run these in parallel:

```bash
git status                          # overview of staged vs unstaged
git diff --cached --stat            # what will actually go into the PR
git diff --stat                     # what will NOT go into the PR
git log --oneline -5                # recent commits for context
git branch --show-current           # current branch
```

**Always show the user a clear summary** before proceeding. Present it like this:

```
Estos cambios VAN al PR (staged):
  modified:   src/auth.ts
  new file:   src/utils/token.ts

Estos cambios NO van al PR (unstaged):
  modified:   README.md
  modified:   package.json

Archivos sin trackear (no van al PR):
  .env.local
  tmp/
```

This gives the user a chance to say "wait, add X too" or "actually remove Y"
before anything gets committed.

**If nothing is staged**, stop and tell the user:
> "No hay cambios en staging. Agregá los archivos que quieras incluir en el PR
> con `git add <archivo>` y volvé a pedirme el PR."

**If already on a feature branch** (not `main`), ask the user whether to:
- Create a new branch from here, or
- Use the current branch as-is

### 2. Determine the change type

Look at the staged diff and classify the change. This classification drives the
branch name, commit message, and PR title.

| Type       | When to use                                              |
|------------|----------------------------------------------------------|
| `feat`     | New functionality, new files that add capabilities       |
| `fix`      | Bug fix, correction of existing behavior                 |
| `docs`     | Documentation only (markdown, comments, READMEs)         |
| `refactor` | Code restructuring without changing behavior             |
| `test`     | Adding or updating tests                                 |
| `chore`    | Config, dependencies, tooling, CI                        |
| `style`    | Formatting, linting, whitespace (no logic changes)       |

If the changes span multiple types, pick the dominant one. When in doubt between
`feat` and `docs`, ask yourself: "does this add a capability or just describe
one?"

### 3. Create the branch

**Convention**: `type/short-description`

- Use kebab-case for the description
- Keep it under 50 characters total
- Be specific enough that a teammate can guess the content

```
feat/user-authentication
fix/login-redirect-loop
docs/uruguay-market-research
refactor/extract-api-client
chore/update-dependencies
```

```bash
git checkout -b <branch-name>
```

### 4. Commit the staged changes

**Commit message convention**: Conventional Commits format.

```
type(scope): short imperative description

Optional body with more context. Explain the "why" when it's not obvious
from the diff. Keep lines under 72 characters.
```

- **type**: same as branch type
- **scope**: the area of the project affected (optional, use when helpful)
- **short description**: imperative mood ("add", "fix", "update"), lowercase, no period, under 50 chars
- **body**: only when the "what" isn't obvious from the diff

Examples:
```
docs(market): update research and competitors for Uruguay
feat(auth): add JWT token refresh on expiration
fix(api): handle null response from payment gateway
```

Use a HEREDOC to pass the message:
```bash
git commit -m "$(cat <<'EOF'
type(scope): description here

Optional body here.
EOF
)"
```

### 5. Push the branch

```bash
git push -u origin <branch-name>
```

### 6. Create the PR

**PR title**: Same as the commit's first line (the `type(scope): description` part).
Keep it under 70 characters.

**PR description template**:

```bash
gh pr create --base main --title "<title>" --body "$(cat <<'EOF'
## Summary

- First change or reason
- Second change
- Third change (keep to 2-4 bullets)

## Context

_Why_ these changes matter. One short paragraph linking to relevant docs,
issues, or decisions if applicable.

## Review notes

Anything the reviewer should pay attention to or test manually.
EOF
)"
```

The description should be in the same language the user is using in the
conversation (Spanish or English).

### 7. Report back

After the PR is created, show the user:
- The PR URL
- A one-line summary of what was included
- Reminder of any unstaged changes that were NOT included

## Edge cases

- **Merge conflicts with main**: warn the user before creating the PR. Don't
  try to resolve automatically.
- **Branch already exists on remote**: append a short suffix (`-v2`, `-update`)
  rather than failing.
- **Large diffs (>500 lines changed)**: mention it in the PR description so
  reviewers know to set aside time.
- **Sensitive files staged** (`.env`, credentials, keys): warn and ask for
  confirmation before committing.

## What NOT to do

- Never `git add` files on behalf of the user. The user controls what's staged.
- Never push to `main` directly.
- Never use `--force` push.
- Never amend existing commits.
- Never skip git hooks (`--no-verify`).
