# copilot-sticky-notes

## What it does

Personal local memory: capture notes, actions and context bundles as plain Markdown files on your own machine.

Part of the **department-copilots** suite: local-only copilots where the employee provides the input, Claude analyses it on the machine, and the employee decides what to do. No CRM, NMS, email or system integrations.

## Install

```bash
claude plugin marketplace add sara-hamza/department-copilots
```

```bash
claude plugin install sticky-notes@department-copilots
```

Personal local memory. Plain Markdown files under `~/.copilots/sticky-notes/` (override with `COPILOT_NOTES_DIR`). No sync, no integrations.

| Command | Use |
|---|---|
| `/sticky-notes:note <text>` | Save a note; to-dos become `- [ ]` checkboxes. Optional `topic:<t>` `tags:<a,b>` |
| `/sticky-notes:notes [words]` | List or search |
| `/sticky-notes:actions [topic:<t>]` | Open actions across notes |
| `/sticky-notes:done <id> <n>` | Tick an action |
| `/sticky-notes:bundle <topic>` | Everything on a topic plus open actions, as context before a task |

The script `skills/sticky-notes/scripts/notes.py` is stdlib-only and can be run by hand:

```bash
python3 ~/.claude/plugins/cache/department-copilots/sticky-notes/*/skills/sticky-notes/scripts/notes.py list
```
