# KJV Study

A local-first King James Version Bible study tool organized by book.

## Features

- **Library** — browse all 66 books (Old & New Testament)
- **Chapter reader** — read KJV text with previous/next navigation
- **Notes & highlights** — per-verse annotations stored in IndexedDB
- **Cross-references** — verse links from OpenBible.info / Treasury of Scripture Knowledge
- **Themes** — curated topical verse collections
- **Famous verses** — well-known passages with jump-to-context
- **My Study** — review your notes/highlights; export/import JSON backups

## Live site (GitHub Pages)

**https://k4vr.github.io/kjv-study/**

GitHub must build this app with **GitHub Actions**, not “Deploy from a branch”:

1. Open [Settings → Pages](https://github.com/K4VR/kjv-study/settings/pages)
2. Under **Build and deployment** → **Source**, choose **GitHub Actions**
3. After each push to `main`, wait for the **Deploy GitHub Pages** workflow to show a green check, then hard-refresh the site (Ctrl+Shift+R or Cmd+Shift+R)

A blank white page means the unbuilt source `index.html` is being served. A “Failed to load …” chapter error means the Bible JSON was not published at `/kjv-study/data/kjv/`. Both are fixed by using GitHub Actions as the Pages source and letting that workflow finish.

## Develop

```bash
npm install
npm run download-data   # optional: refresh public KJV + cross-ref JSON
npm run dev
```

## Build

```bash
npm run build
npm run preview
```

## Data attribution

- **Scripture text:** King James Version (public domain), sourced via community JSON editions.
- **Cross-references:** Derived from [OpenBible.info](https://www.openbible.info/labs/cross-references/) / Treasury of Scripture Knowledge (CC BY), via structured exports used by kjvstudy.org.

Personal notes, highlights, and custom themes never leave your browser unless you export a backup.
