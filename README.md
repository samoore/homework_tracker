# 📚 Homework Hero

A friendly, mobile-first homework tracker designed for students aged 11–12 who are juggling multiple subjects and teachers for the first time.

No app store. No login. No server. Just save the file and open it in any browser.

---

## ✨ Features

- **Add homework tasks** — subject (with emoji icons), due date, and description
- **Urgency alert banner** — pops up automatically when tasks are due within 2 days; must be manually dismissed or snoozed
- **Colour-coded due dates** — overdue 🚨, today 🔥, tomorrow ⏰, upcoming 📅
- **Complete tasks** — tick the checkbox to archive work into the Completed tab
- **Persistent storage** — everything saves in the browser's `localStorage`; survives page reloads and browser restarts
- **Fully responsive** — table view on desktop, card view on mobile with a bottom nav bar
- **No install required** — single HTML file, works offline

---

## 🚀 Getting Started

### Option 1 — Just open it
Download `index.html` and open it in any modern browser (Chrome, Safari, Firefox, Edge).

### Option 2 — Serve it locally
```bash
# Python 3
python3 -m http.server 8080

# Node (npx)
npx serve .
```
Then visit `http://localhost:8080`.

### Option 3 — Deploy to the web
Drop `index.html` into any static host:
- [GitHub Pages](https://pages.github.com/) — free, just push to a `gh-pages` branch
- [Netlify Drop](https://app.netlify.com/drop) — drag and drop the file
- [Vercel](https://vercel.com/) — `vercel --prod`

---

## 📱 Mobile / Phone Use

This tool is designed to live on a phone. To get the best experience:

**iOS (Safari)**
1. Open the file or hosted URL in Safari
2. Tap the Share button → **Add to Home Screen**
3. It will appear as an app icon on your home screen

**Android (Chrome)**
1. Open in Chrome
2. Tap the three-dot menu → **Add to Home Screen**

> **Note:** Data is stored per browser. If you add it to your home screen and also open it in a browser tab, they share the same storage on the same device.

---

## 🗂️ Project Structure

```
homework-hero/
├── index.html          # The entire application (HTML + CSS + JS, single file)
├── README.md           # This file
├── CONTRIBUTING.md     # How to contribute
└── CHANGELOG.md        # Version history
```

---

## 🛠️ Tech Stack

| Layer      | Technology |
|------------|------------|
| Markup     | HTML5      |
| Styles     | CSS3 (custom properties, grid, flexbox, animations) |
| Logic      | Vanilla JavaScript (ES6+) |
| Storage    | `localStorage` + `sessionStorage` |
| Fonts      | Google Fonts — Fredoka One + Nunito |
| Build tool | None — zero dependencies |

---

## 🔔 Alert / Notification Behaviour

The urgency banner fires automatically on page load when any pending task is due within **2 days** (including overdue tasks).

| Action | Effect |
|--------|--------|
| **"Got it — I'm on it!"** | Dismisses for the rest of today. Returns tomorrow if tasks are still urgent. |
| **"Snooze"** | Dismisses for the current browser session only. Returns on next page load. |

---

## 🌱 Roadmap / Ideas

- [ ] PWA manifest + service worker for true offline install
- [ ] Push notifications (requires backend or service worker)
- [ ] Teacher/parent view mode (read-only share link)
- [ ] Custom subject colours
- [ ] Weekly summary / streak tracker
- [ ] Export to CSV or PDF

---

## 👥 Contributors

| Name | Role |
|------|------|
| Stuart Moore (https://github.com/samoore) | Creator & Project Owner |
| [Claude](https://claude.ai) (Anthropic) | Initial build, mobile UX, alert system |

---

## 📄 Licence

MIT — do whatever you like with it. A credit back is always appreciated but not required.
