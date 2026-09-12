<p align="center">
  <img src="assets/logo_name.svg" alt="Stride" width="200" height="56"/>
</p>

<p align="center">
  A lightweight project progress tracker for research groups and graduate students,<br>
  built as a single self-contained HTML file — no install, no server, no account.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Purdue%20University-CSaT-CEB888?style=flat-square" alt="Purdue University · CSaT">
  <img src="https://img.shields.io/badge/license-MIT-5C5FEB?style=flat-square" alt="MIT License">
  <img src="https://img.shields.io/badge/no%20install-open%20%26%20use-34D399?style=flat-square" alt="No install">
</p>

## Features

- **Two-row layout per project** — key info on top, details below
- **Priority badges** — High / Medium / Low, click to cycle
- **Stage tracking** — Planning → In Progress → Analyzing → Writing → Under Review → On Hold → Done
- **Deadline & next step** — what needs to happen and by when
- **Blocker categories** — flag what's blocking progress
- **Notes column** — free-form text per project
- **Filter by priority** and **sort** by priority, deadline, last updated, or name
- **Auto-saves to browser localStorage** — no account, no server
- **Export to Excel (.xlsx) or JSON** — for backups and sharing
- **Import from Excel or JSON** — restore or migrate data
- **Dark / light / system theme**
- **Export reminder banner** — appears when you have changes not yet backed up

## Usage

Open `index.html` in any modern browser. That's it — no install, no dependencies, no build step.

If you're using the hosted GitHub Pages version, just bookmark the URL. Your data lives in your browser's localStorage and is private to you.

### Keyboard shortcuts

| Action | Key |
|--------|-----|
| Finish editing a cell | `Enter` |
| New line in Notes | `Shift + Enter` |
| Cycle priority badge | `Space` or `Enter` while focused |

## Data & privacy

All project data is stored in **your browser only** (`localStorage` key `pt-v2`). Nothing is sent to any server. Data does not sync across browsers or devices — use **Export → Excel** or **Export → JSON** to back up and transfer your data.

## Self-hosting

Because Stride is a single HTML file, hosting it anywhere that serves static files works:

- **GitHub Pages** — enable Pages in repo Settings → Pages, source = main branch / root. Your URL will be `https://yourusername.github.io/stride`.
- **Any static host** — Netlify, Vercel, S3, etc. Drop `index.html` in and point a domain at it.
- **Local** — just open the file directly in a browser. Export/import still works.

Each user who opens the same hosted URL gets their own independent localStorage, so data never mixes between users.

## Export compatibility

Excel exports include all fields and are compatible with Excel, Numbers, and LibreOffice Calc. JSON exports follow this schema:

```json
{
  "exported": "ISO 8601 timestamp",
  "version": 2,
  "projects": [ { ... } ]
}
```

Both formats can be re-imported into Stride.

## Built with

- Vanilla HTML / CSS / JavaScript — no framework
- [SheetJS](https://sheetjs.com/) (XLSX) for Excel export/import
- [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) & [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) via Google Fonts
- [Claude by Anthropic](https://claude.ai)

## Author

**Xiaotao Yang** · Purdue University, CSaT

## License

MIT — free to use, modify, and distribute.
