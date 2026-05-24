# Claude Cowork Dashboard — How to Use

> The dashboard is a local HTML file (`dashboard.html`) that lives in your Claude workspace folder (`001.Claude/`). It gives you a visual view of your tasks and memory files without opening Cowork.

---

## Opening the Dashboard

**File location:** `001.Claude/dashboard.html`

**Required browser:** Open in **Brave, Chrome, or Edge** only.
- Right-click → Open With → Brave (or Chrome/Edge)
- Do NOT open in Safari — file pickers will not work

> Safari and Firefox block the file access APIs this dashboard uses. Brave/Chrome work when launched directly from the file browser.

---

## Tasks Tab

The Tasks tab shows your `TASKS.md` as a visual board or list.

### Steps to load tasks
1. Click **"Select TASKS.md"** (large button in the center, or **"Select File"** in the header)
2. A file picker opens — navigate to `001.Claude/TASKS.md` and select it
3. Tasks load into a Kanban board with columns: **In Progress / Up Next / Done**

### Switching views
Use the **Board / List** toggle in the header to switch between Kanban and list view.

### Adding and editing tasks
- Click **+ Add task** inside any column to create a new task
- Click a task card to edit it
- Drag cards between columns to change status

### Saving changes
Click **Save** in the header after making edits.

> **Note for Brave opened via `file://`:** Due to browser security restrictions, Save will **download** the updated file instead of writing directly. Replace your original `TASKS.md` with the downloaded copy.

---

## Memory Tab

The Memory tab shows Claude's working memory — `CLAUDE.md` and all files in the `memory/` directory.

### Steps to load memory
1. Click the **Memory** tab in the header
2. Click **"Open Folder"** (or **"Select Folder"** in the center)
3. Select your `001.Claude/` workspace folder — not a subfolder
4. Memory loads with sub-tabs for each file

### What you'll see
| Tab | Source file |
|-----|------------|
| Overview | `CLAUDE.md` — your working memory (people, terms, projects) |
| glossary | `memory/glossary.md` — shorthand decoder ring |
| company | `memory/context/company.md` — org and role context |
| vault-structure | `memory/context/vault-structure.md` — Obsidian folder map |
| SIF-security-testing | `memory/projects/SIF-security-testing.md` — active project |

> Memory is **read-only** in the dashboard. To update, ask Claude in Cowork or edit the files directly.

---

## Known Limitations

| Issue | Cause | Workaround |
|-------|-------|-----------|
| File picker doesn't open | Opened in Safari or Firefox | Use Brave/Chrome/Edge |
| Save downloads instead of writing | Brave `file://` security restriction | Replace original file with the download |
| Memory shows stale data | Dashboard doesn't auto-sync | Reload the page after Claude makes changes |
| "Open Folder" shows no files | Wrong folder selected | Select `001.Claude/` (the root workspace folder) |

---

## Quick Reference

| Action | How |
|--------|-----|
| Load tasks | Tasks tab → Select TASKS.md |
| Add a task | Click + in any board column |
| Save tasks | Header → Save button |
| View memory | Memory tab → Open Folder → select `001.Claude/` |
| Refresh after Claude edits | Reload the page (Cmd+R) |

---

*Note created by Claude Cowork — 2026-04-25*
