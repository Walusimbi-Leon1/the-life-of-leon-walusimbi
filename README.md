# 📖 The Life of Leon Walusimbi

**An Autobiography by Walusimbi Leon (SGSS)**

---

## About

*The Life of Leon Walusimbi* is the true story of a creator from East Africa — the books he has written, the games he has built, the websites he has launched, the AI team he created, and the things he likes to do.

This book is special: **it writes itself, one chapter a day.** A GitHub Actions workflow runs every morning, calls the `big-pickle` model on opencode.ai, and adds ~2,000 words to the book — all under Leon's direction (see `book.config.json`). The book grows as his life does.

## 📚 Read Online

- 📖 **Read:** https://walusimbi-leon1.github.io/the-life-of-leon-walusimbi/book.html
- 🏠 **Home:** https://walusimbi-leon1.github.io/the-life-of-leon-walusimbi/

## 🛠️ How It's Written

1. Every day at **04:30 UTC (07:30 EAT)**, the `Daily Book Writing` workflow runs.
2. `scripts/write-book.js` reads the current book + instructions in `book.config.json`.
3. It asks `big-pickle` (opencode.ai) for the next ~2,000 words of memoir.
4. The chapter is appended to `book.md` and injected into `book.html`.
5. The commit is pushed as *SGSS Books Bot* → GitHub Pages rebuilds → the book grows.

You can also trigger a chapter manually: **Actions → Daily Book Writing → Run workflow**.

## 📂 Repository Structure

```
the-life-of-leon-walusimbi/
├── book.config.json      # 📋 The instructions — who Leon is, what each chapter covers
├── book.md               # The book source (markdown, grows daily)
├── book.html             # The styled reading page (grows daily)
├── index.html            # Landing page
├── cover.jpg             # Cover art
├── scripts/write-book.js # The daily writer
└── .github/workflows/    # The daily schedule
```

## 🔒 Secrets (set in repo settings)

| Secret | Purpose |
|---|---|
| `OPENCODE_API_KEY` → `_2` … `_5` | opencode.ai keys (rotated on failure) |
| `GH_PUSH_TOKEN` | Push token that bypasses branch protection |

## 📋 License

All works are [CC0 1.0 Universal](LICENSE) (Public Domain) — free to read, share, and distribute.

---

📚 Part of the SGSS Literary Collection · Founded by Walusimbi Leon · All works free for all
