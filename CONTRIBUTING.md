# 🤝 Contributing to Homework Hero

Thanks for wanting to make Homework Hero better! This is a simple project — here's how to get involved.

---

## 🐛 Reporting Bugs

1. Check the existing issues first to avoid duplicates
2. Open a new issue with:
   - What you expected to happen
   - What actually happened
   - Your browser and device (e.g. "iPhone 14, Safari 17")
   - Steps to reproduce

---

## 💡 Suggesting Features

Open an issue labelled `enhancement`. Describe:
- Who benefits from the feature
- How it would work from the user's perspective
- Any edge cases to consider

---

## 🔧 Making Changes

Because this is a single-file project, the workflow is simple:

```bash
# 1. Fork the repo on GitHub, then clone your fork
git clone https://github.com/YOUR-USERNAME/homework-hero.git
cd homework-hero

# 2. Create a feature branch
git checkout -b feature/your-feature-name

# 3. Edit index.html
#    - CSS lives in the <style> block
#    - HTML structure follows the <style> block
#    - JavaScript lives in the <script> block at the bottom

# 4. Test in multiple browsers and at mobile widths (≤640px)

# 5. Commit your changes
git add index.html
git commit -m "feat: describe what you added"

# 6. Push and open a Pull Request
git push origin feature/your-feature-name
```

---

## ✅ Contribution Checklist

Before opening a PR, please confirm:

- [ ] Tested on desktop (Chrome or Firefox)
- [ ] Tested on mobile width (use browser DevTools or a real device)
- [ ] No external dependencies added (keep it zero-dependency)
- [ ] `localStorage` keys are not changed without a migration note
- [ ] CHANGELOG.md updated with a brief description of the change

---

## 🎨 Code Style

- **Indentation:** 2 spaces
- **CSS:** Use existing custom properties (`--teal`, `--navy`, etc.) for colours
- **JavaScript:** ES6+, `const`/`let` only, no `var`
- **Comments:** Add a comment above any non-obvious logic block
- **Commits:** Use [Conventional Commits](https://www.conventionalcommits.org/) style:
  - `feat:` new feature
  - `fix:` bug fix
  - `style:` CSS/visual changes only
  - `docs:` README or comment changes
  - `refactor:` code restructure, no behaviour change

---

## 👥 Contributors

Add your name to the Contributors table in `README.md` as part of your first PR — you've earned it!

---

## 💬 Questions?

Open a Discussion or an Issue — there are no silly questions here.
