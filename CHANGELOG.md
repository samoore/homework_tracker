# 📋 Changelog

All notable changes to Homework Hero are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.1.0] — 2026-03-06

### Added
- **Urgency alert banner** — modal overlay appears on page load when any pending task is due within 2 days (including overdue tasks)
  - Lists all urgent tasks grouped by severity (overdue / today / tomorrow / 2 days)
  - "Got it — I'm on it!" dismisses the banner for the rest of the current calendar day
  - "Snooze" dismisses for the current browser session only
  - Re-appears the next day if urgent tasks remain undone
- Alert correctly distinguishes overdue, today, tomorrow, and 2-day urgency levels with distinct colours and emoji

### Changed
- Task urgency borders on mobile cards now also reflect "2 days away" (yellow) separately from "ok" (teal)

---

## [1.0.0] — 2026-03-05

### Added
- Initial release of Homework Hero
- Add homework tasks with subject, due date, and description
- 11 subject options with emoji icons and colour-coded badges
- Tasks sorted automatically by due date (soonest first)
- Colour-coded due date labels: overdue 🚨, today 🔥, tomorrow ⏰, soon 📅
- Tick checkbox to mark task complete — moves to Completed tab
- Uncheck in Completed tab to move a task back to To Do
- Delete individual tasks from either tab
- Persistent storage via `localStorage` — survives page reload
- Header stats showing pending and completed counts
- Toast notifications for all actions (add, complete, undo, delete)
- **Desktop view:** table layout with subject, details, due date columns
- **Mobile view (≤640px):**
  - Card-based layout instead of table (thumb-friendly)
  - Coloured left border per urgency level
  - Full-width Add button
  - Bottom navigation bar replacing tab buttons
  - 16px minimum font size on inputs (prevents iOS auto-zoom)
  - Toast notification repositioned to top of screen

## [1.2.0] — 2026-03-06

### Added
- **Backup bar** — sits between the add form and the task tabs; always visible
- **Export backup** (⬇️ Save Backup) — downloads all tasks as a dated `.json` file (e.g. `homework-hero-backup-2026-03-06.json`); shows time of last save in the bar
- **Import backup** (⬆️ Load Backup) — file picker accepts `.json` backup files; validates content before doing anything
- **Import confirmation modal** — shows task counts and export date from the file before committing, with two safe options:
  - **Merge** — adds backup tasks alongside existing ones, silently skipping duplicates (matched by task ID)
  - **Replace All** — wipes current tasks and loads the backup fresh
  - **Cancel** — aborts with no changes made
- Backup file format includes app name, version, export timestamp, and task count for easy identification

## [1.3.0] — 2026-03-06

### Added
- **Automatic background backup to OPFS** — every time a task is added, completed, deleted, or imported, the full task list is silently written to the browser's Origin Private File System (a private sandbox separate from localStorage, not cleared when the browser wipes site data)
- Writes are debounced (800ms) so rapid changes (e.g. bulk imports) produce only one write
- **"🟢 Auto-saved at HH:MM:SS"** status shown in the backup bar after each successful write
- **"🔁 Restore Auto-Save" button** — appears in the backup bar when a prior OPFS backup is detected; opens the existing import modal (with Merge / Replace All / Cancel options) pre-populated with the auto-save contents and timestamp
- On startup with no localStorage tasks but an existing OPFS backup, the bar surfaces a hint so the user knows recovery is available
- Manual "Save to File" button still works exactly as before for portable `.json` downloads

### Changed
- Renamed backup bar buttons to "Save to File" / "Load from File" for clarity
- Export payload version bumped to 1.3.0
