# Claude Cowork — How to Use

> Claude Cowork is a desktop AI tool for automating file and task management. It runs on top of the Claude Agent SDK and gives Claude access to your local files, a sandboxed Linux shell, and connected tools (MCPs).

---

## What It Can Do

- Read, write, and edit files in your workspace folders
- Run shell commands (Python, Bash, Node) in an isolated Linux sandbox
- Connect to external tools via MCP (Slack, Notion, Jira, GitHub, etc.)
- Create documents — `.md`, `.docx`, `.pptx`, `.xlsx`, `.pdf`
- Browse the web and fetch pages
- Remember context across sessions via `CLAUDE.md` and `memory/`

---

## Core Concepts

### Workspace Folder
The folder you connect when you open Cowork. Claude can read and write here. Final outputs go here.

### Skills (`/skill-name`)
Pre-built workflows you can invoke with a slash command or natural language.

| Skill | What it does |
|-------|-------------|
| `/productivity:start` | Opens dashboard, bootstraps memory |
| `/productivity:task-management` | Manage TASKS.md |
| `/productivity:update` | Sync tasks, refresh memory |
| `/docx` | Create or edit Word documents |
| `/pptx` | Create or edit PowerPoint presentations |
| `/xlsx` | Create or edit Excel spreadsheets |
| `/pdf` | Create, extract, or manipulate PDFs |

### Memory System
Claude stores working memory in:
- `CLAUDE.md` — short-term context (people, terms, active projects)
- `memory/glossary.md` — decoder ring for shorthand and acronyms
- `memory/projects/` — per-project detail files
- `memory/context/` — company, vault structure, tools

### TASKS.md
A simple markdown task list. Claude reads and updates it during sessions.

---

## Useful Phrases

| Say this | What happens |
|----------|-------------|
| `good morning` | Recap of recent work + what to focus on |
| `new project` | Claude interviews you and sets up a project folder |
| `end of day` / `wrap up` | Claude logs the session so next session picks up |
| `help` | Claude lists what it can do |

---

## Dashboard (`dashboard.html`)

The productivity dashboard lives in your workspace folder (`001.Claude/dashboard.html`). It shows your tasks (board/list view) and memory files.

### How to open it
Open `dashboard.html` in **Brave, Chrome, or Edge**. Do not open it in Safari — Safari blocks the file picker APIs the dashboard uses.

On Mac: right-click the file → Open With → Brave (or Chrome/Edge).

### Tasks tab
1. Click **Select TASKS.md** (or the "Select File" button in the header)
2. A file picker opens — navigate to your `001.Claude/TASKS.md` and select it
3. Tasks load in board view (columns: In Progress / Up Next / Done)
4. To save changes: click **Save** in the header
   - If opened via `file://` in Brave: Save will **download** the updated file — replace your original `TASKS.md` with the downloaded one

### Memory tab
1. Switch to the **Memory** tab in the header
2. Click **Open Folder** → select your `001.Claude/` workspace folder
3. Claude's memory files load: CLAUDE.md overview + all `memory/` subdirectory files
4. Memory is read-only in the dashboard (edit via Claude or directly in files)

### Known limitations
- Opened via `file://` in Brave: Save downloads instead of writing directly — this is a browser security restriction
- The dashboard does not auto-sync; reload the page to see changes Claude made during a session

---

## Tips

- **Prefix rule:** Claude creates files prefixed with `[C]` — e.g. `[C] Report.md` — so you know what Claude made vs. what you made.
- **Don't ask, don't edit:** Claude will not edit your non-`[C]` files without permission.
- **Plugins:** Cowork supports plugins (bundles of MCPs + skills). Install from the plugin marketplace to add connectors for Slack, Jira, Notion, etc.
- **Shell access:** Claude can run Python, Bash, and Node in a sandboxed Linux VM. Good for data processing, file conversion, and automation.

---

## MCP Connectors
MCPs extend Claude's reach to external services. Connected via the plugin system.

Examples:
- **Slack** — read channels, send messages
- **Notion** — read/write pages and databases
- **GitHub** — read PRs, issues, repos
- **Google Calendar** — read events, schedule

---

*Note created by Claude Cowork — 2026-04-25*
