---
name: notesctl
description: Manage Apple Notes via deterministic local scripts (create, append, list, search, export, and edit). Use when a user asks OpenClaw to add a note, list notes, search notes, or manage note folders.
metadata:
  {
    "openclaw": {
      "emoji": "📝",
      "os": ["darwin"],
      "requires": { "bins": ["memo", "python3", "osascript"] }
    }
  }
---

# notesctl (Apple Notes, low-token)

## Goal

Minimize token usage and avoid fragile quoting by routing Apple Notes operations through bundled scripts.

## Quick start

### Create a new note (deterministic title/body)

- JSON stdin (recommended):

```bash
echo '{"title":"标题","body":"第一行\n第二行","folder":"Notes"}' | {baseDir}/scripts/notes_post.sh
```

- Direct args:

```bash
{baseDir}/scripts/notes_new.sh "标题" $'正文第一行\n正文第二行' "Notes"
```

### List/search/export

```bash
{baseDir}/scripts/notes_list.sh "Notes"
{baseDir}/scripts/notes_search.sh "query" "Notes"
{baseDir}/scripts/notes_export.sh "query" "Notes" "/tmp"  # interactive select then export
```

## Output conventions

- Keep receipts short: `已写入 Notes：<标题>`.

## Notes on editing

Editing existing notes is inherently more fragile:
- Prefer append workflows or create a new note with a reference.
- If the user explicitly wants interactive editing, use `memo notes -e` (manual selection + editor).
