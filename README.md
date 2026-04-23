# Turkish Transcribe — Frontend

> Web interface for the Turkish educational transcription service. Real-time progress, drag-and-drop, multi-format export.

[![Next.js](https://img.shields.io/badge/Next.js-15-000000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![shadcn/ui](https://img.shields.io/badge/shadcn/ui-000000?style=flat-square)](https://ui.shadcn.com/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)](Dockerfile)

---

## What this is

The browser-side companion to [turkish-transcribe-be](https://github.com/1lker/turkish-transcribe-be). Drag-and-drop a lecture audio file or paste a YouTube URL, watch live transcription progress over WebSocket, download as JSON / SRT / plain text.

---

## Features

- **Drag-and-drop** audio/video upload with progress tracking
- **YouTube URL ingest** — transcribe straight from a public URL
- **Real-time WebSocket progress** — chunk-level granularity
- **Result viewer** with timestamp navigation
- **Multi-format export** — JSON, SRT subtitles, plain text
- **Modern UI** — shadcn/ui + Tailwind + Geist font

---

## Quick start

### Local dev

```bash
git clone https://github.com/1lker/turkish-transcribe-fe.git
cd turkish-transcribe-fe
npm install
npm run dev
# → http://localhost:3000
```

### Production build

```bash
npm run build
npm start
```

### Docker

```bash
docker build -t turkish-transcribe-fe .
docker run -p 3000:3000 turkish-transcribe-fe
```

---

## Configuration

Set the backend URL via environment variable:

```bash
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_WS_URL=ws://localhost:8000
```

---

## Tech stack

| Layer | Choice |
|---|---|
| Framework | Next.js 15 (App Router) |
| Language | TypeScript (strict) |
| Styling | Tailwind CSS |
| Components | shadcn/ui (Radix primitives) |
| Font | Geist Sans + Geist Mono |
| Container | Docker |

---

## Project structure

```
src/
├── app/                # Next.js App Router pages
├── components/         # React components
├── lib/                # API client, WebSocket helpers
└── styles/             # Globals
```

---

## Author

**İlker Yörü** — CTO @ [Mindra](https://mindra.co)
[GitHub](https://github.com/1lker) · [LinkedIn](https://linkedin.com/in/ilker-yoru) · [ilkeryoru.com](https://ilkeryoru.com)

## License

MIT
