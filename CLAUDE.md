# CLAUDE.md

This file provides guidance for AI assistants (Claude and others) working in this repository.

## Repository Overview

**Repository:** `gaminggusgus94/Test`
**Status:** Freshly initialized — no source code has been committed yet.

This repository is currently empty and awaiting initial project setup. The CLAUDE.md file serves as a living document: update it as the codebase evolves to keep guidance accurate for future AI-assisted development sessions.

---

## Repository Structure

```
/
└── CLAUDE.md          # This file — AI assistant guidance
```

As the project grows, update this section to reflect the actual directory layout, e.g.:

```
/
├── src/               # Application source code
├── tests/             # Test files
├── docs/              # Documentation
├── .github/workflows/ # CI/CD pipelines
├── CLAUDE.md
└── README.md
```

---

## Development Workflow

### Branching Strategy

- **Main branch:** `main` (or `master`) — stable, production-ready code only
- **Feature branches:** `claude/<short-description>-<session-id>` for AI-assisted work
- **Human branches:** Use descriptive names like `feature/<name>`, `fix/<name>`, `chore/<name>`

### Branch Rules for AI Assistants

- Always develop on the designated branch specified in the task context
- Branch names must start with `claude/` for AI-generated work
- **Never** push directly to `main`/`master` without explicit permission

### Git Workflow

```bash
# Check current branch before starting
git status

# Create and switch to a feature branch if needed
git checkout -b claude/<description>-<session-id>

# Stage specific files (avoid git add -A to prevent accidental secrets)
git add <file1> <file2>

# Commit with a descriptive message
git commit -m "feat: add initial project structure"

# Push to remote
git push -u origin <branch-name>
```

### Commit Message Conventions

Use the [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>(<optional-scope>): <short description>

[optional body]
```

**Types:**
| Type | When to Use |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation changes only |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `test` | Adding or updating tests |
| `chore` | Build process, tooling, or dependency updates |
| `ci` | CI/CD pipeline changes |

**Examples:**
```
feat: add user authentication module
fix(api): handle null response from payment gateway
docs: update CLAUDE.md with testing instructions
test: add unit tests for cart calculation logic
```

### Push Guidelines

- Always use `git push -u origin <branch-name>`
- If push fails due to network errors, retry up to 4 times with exponential backoff: 2s, 4s, 8s, 16s
- **Never** use `--force` on shared branches without explicit user approval

---

## Git Safety Rules

These rules apply to all development in this repository:

1. **Never** commit secrets, credentials, `.env` files, or API keys
2. **Never** use `--no-verify` to skip pre-commit hooks
3. **Never** run `git reset --hard`, `git push --force`, or `git clean -f` without explicit user instruction
4. **Always** prefer creating a new commit over amending an existing one
5. **Always** stage specific files by name rather than `git add -A` or `git add .`
6. **Never** use interactive git commands (`-i` flag) as they require terminal interaction

---

## Code Style & Conventions

_To be filled in once the project language and tooling are established._

General principles to follow until conventions are defined:

- Follow the style already present in the codebase ("when in Rome")
- Keep changes minimal and focused — avoid scope creep
- Avoid over-engineering: no premature abstractions, no hypothetical future requirements
- Do not add comments, docstrings, or type annotations to code you did not change
- Prefer editing existing files over creating new ones

---

## Testing

_To be filled in once testing framework is established._

General principles:
- Run tests before committing
- Do not mark a task complete if tests are failing
- Write tests for new behavior; do not break existing tests

---

## CI/CD

_To be filled in once CI/CD pipelines are configured._

---

## Environment Setup

_To be filled in once dependencies and tooling are defined._

---

## Key Files to Know

| File | Purpose |
|------|---------|
| `CLAUDE.md` | This file — AI assistant guidance |

_Update this table as important files are added to the project._

---

## Working with AI Assistants

### What Claude Should Do

- Read relevant files before modifying them
- Make minimal, focused changes scoped to the task
- Ask for clarification rather than guessing at ambiguous requirements
- Keep this CLAUDE.md up to date as the project evolves
- Commit and push completed work to the designated branch

### What Claude Should NOT Do

- Add unrequested features, refactors, or "improvements"
- Delete or overwrite files without understanding their purpose
- Bypass git hooks or safety checks
- Commit to `main`/`master` directly
- Push to a branch other than the one specified in the task context

---

## Updating This File

This document should be updated whenever:
- A new language, framework, or major dependency is added
- Testing or build tooling changes
- Branching or workflow conventions are established or changed
- Important architectural decisions are made

Keep entries concise and accurate. Outdated guidance is worse than no guidance.
