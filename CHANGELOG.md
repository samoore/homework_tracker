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
