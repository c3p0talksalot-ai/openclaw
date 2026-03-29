# Coding Repos & Workflows

## Before Starting Any Coding Task

1. **Read project-specific coding standards** — Check for , , or similar files in the repo
2. **Read architecture docs** — Look for , , or  folder
3. **Check existing patterns** — Review similar code in the codebase before writing new code

## Git Workflow

### Branch Strategy

-  — production-ready code
- Feature branches:  (e.g., )

### Starting a New Task



### Before PR



### Commit Messages

Include ticket references:


## Agent Rules

### When to Ask Before Proceeding

- Requirements are unclear or ambiguous
- Decision affects architecture significantly
- Running destructive commands (delete, drop, force push)
- Anything that leaves the machine (emails, tweets, external API calls)

### When to Start Work Directly

- Requirements are clear and straightforward
- Following established patterns in the codebase
- Documentation/dorg work that doesn't affect runtime

### Communication

- **Wait for go-ahead** before starting coding after ticket created
- **Post updates every 10 minutes** for long-running tasks
- **Ask clarifying questions** if requirements are vague

### Code Execution

- **Spawn sub-agent** for coding tasks rather than coding directly in main session
- **Never commit directly to main** — use feature branches
- **Delete branches** after merge

## Red Lines

- Don't exfiltrate private data. Ever.
- Don't run destructive commands without asking.
- `trash` > `rm` (recoverable beats gone forever)

## Project Standards

Always look for and follow:
- Coding standards documents (`CODING_STANDARDS.md`, `CONTRIBUTING.md`)
- Architecture documents (`architecture.md`, `docs/`)
- Linting rules (`.eslintrc`, `.prettierrc`)
- Testing patterns (`__tests__`, `test/`)
- Existing code patterns in the codebase