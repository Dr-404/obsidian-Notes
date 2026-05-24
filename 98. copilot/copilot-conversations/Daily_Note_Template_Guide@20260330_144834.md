---
epoch: 1774856914859
modelKey: "gemini-flash-latest|google"
topic: "Daily Note Template Guide"



tags:
  - copilot-conversation
---

**user**: how to create daily note template in this
[Context: Notes: Journal/DailyNotes/29-03-2026.md]
[Timestamp: 2026/03/30 14:48:34]

**ai**: To create a daily note template in Obsidian, you need to set up a template file and then configure the **Daily notes** plugin to use it. Here is a step-by-step guide:

### 1. Create your Template Note
First, you need a note that will serve as the blueprint for your daily entries.

- Create a folder named `Templates` (if you don't have one already).
- Create a new note inside that folder, for example, named [[Daily Note Template]].
- Add the structure you want. You can use placeholders that Obsidian will automatically fill:
    - `{{date}}`: Inserts the current date.
    - `{{time}}`: Inserts the current time.
    - `{{title}}`: Inserts the title of the note (which is usually the date).

**Example Template Content:**
```markdown
# Journal for {{date}}

## 🎯 Goals for Today
- [ ] 

## ✅ Tasks
- [ ] 

## 📝 Notes & Thoughts


## 🙏 Gratitude
- 
```

### 2. Configure the Daily Notes Plugin
Now, tell Obsidian to use this template whenever you create a new daily note.

- Open **Settings** (gear icon).
- Go to **Core plugins** and ensure **Daily notes** is toggled on.
- Click the gear icon next to **Daily notes** to open its settings.
- **Template file location**: Search for and select your [[Daily Note Template]].
- **New file location**: Set this to the folder where you want your daily notes stored (based on your current file, this would be `Journal/DailyNotes`).
- **Date format**: Ensure it matches your preferred style (e.g., `DD-MM-YYYY`).

### 3. Using the Template
Once configured, you can generate your daily note in a few ways:
- Click the **Open today's daily note** icon (the calendar page icon) in the left ribbon.
- Use the Command Palette (`Ctrl/Cmd + P`) and type "Daily notes: Open today's daily note".

### Advanced Option: Templater Plugin
If you want more advanced features (like automatically calculating "Yesterday" or "Tomorrow" links), many users install the community plugin called [[Templater]]. It uses `<% tp.date.now() %>` syntax to provide much more flexibility than the standard core templates.

Since you are currently working in [[29-03-2026]], you can manually apply a template to it by opening the Command Palette and selecting **Templates: Insert template** if you have already created the template note.
[Timestamp: 2026/03/30 14:48:51]