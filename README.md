# mvp-data-formatter

> Three-step data normalizer — auto-detects field mapping, applies transformations, and previews the cleaned output before export.

A Next.js app that demonstrates a lightweight ETL UI: load raw data from an external URL, auto-detect column types and suggest a field mapping, review and adjust the mapping, then preview the normalized rows and export.

## Features

- **Auto-detection** — `detectMapping()` infers field types and suggests canonical names from raw column headers
- **Step-by-step flow** — three dedicated pages guide load → map → preview without losing context
- **Live preview** — normalized rows update instantly as mapping is adjusted
- **Export** — download the cleaned dataset as JSON or CSV
- **External source** — pulls data from a configurable URL at render time via `getServerSideProps`

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js (Pages Router) |
| Normalization | Custom `lib/normalize.ts` |
| Styling | Inline styles (dark theme) |

## Getting Started

```bash
npm install
npm run dev   # http://localhost:3000
```

## Routes

| Path | Description |
|------|-------------|
| `/` | Step 1 — Load data from source URL |
| `/mapping` | Step 2 — Review and adjust field mapping |
| `/preview` | Step 3 — Preview normalized rows and export |

## License

MIT
