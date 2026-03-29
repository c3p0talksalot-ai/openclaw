# Ticket Management Workflows

## Ticket Lifecycle

1. **Ticket created** in Trello (Inventory Tracker or Backlog)
2. **Create Discord channel** in project category
3. **Post summary** in new channel with:
   - Ticket title + description
   - Trello link
   - Key context from requirements/docs
4. **Move card** to "In Flight" list
5. **Create memory file** at `memory/ticket-{card-id}.md`
6. **Reply in triage channel** with jump link to new channel
7. **Wait for go-ahead** before starting work
8. **Code**: Spawn sub-agent (don't code directly)
9. **Post updates every 10 minutes** if work is taking longer

## Trello-GitHub Integration

See [trello-setup.md](trello-setup.md#github-integration-hooks) for hook setup.

When commits include ticket references (`refs #22` or `closes #22`):
- Hook automatically appends Trello card URL to commit
- Creates traceable link between code and ticket