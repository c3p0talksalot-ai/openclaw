# Trello Setup

## API Credentials

See TOOLS.md in workspace for API key and token.

- Board ID: 69b4e1dfadb36edeff761149
- Board URL: https://trello.com/b/69b4e1dfadb36edeff761149/openclaw-tasks

## Lists

| List Name | List ID |
|-----------|---------|
| Backlog | 69b4e305ebec0ec84bb30e81 |
| Inventory Tracker | 69c62e04415ca8bd5088cbf8 |
| In Flight | 69c6a531a480ed5b7c84f1e6 |
| Done | 69b4e1e8ee541000fd661489 |

## GitHub Integration (Hooks)

### Commit Hook

When commits include ticket references (`refs #22` or `closes #22`), the hook automatically:
- Appends the Trello card URL to the commit
- Creates a link between the code and the ticket

### Setting Up the Hook

1. Go to Trello board → Power-Ups → Custom
2. Add GitHub integration (or use a third-party like Zapier)
3. Link the repository
4. Configure to listen for commit messages with ticket refs

### Commit Message Format

