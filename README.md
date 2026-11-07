<div align="center">

# Next.js Agent Template

**Starter Next.js 16 yang dirancang untuk AI coding agent** — entrypoint jelas, aturan berscope, dan *progressive disclosure* supaya model tetap fokus dan hemat token.

[![Status](https://img.shields.io/badge/status-ready%20to%20use-brightgreen?style=flat-square)](#)
[![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Tailwind](https://img.shields.io/badge/Tailwind%20CSS-4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)

</div>

---

## Tentang

Kebanyakan starter Next.js dibuat untuk manusia. Template ini dibuat untuk **dua-duanya**: manusia dan AI agent (Claude Code, Cursor, Copilot, dll).

Masalahnya, agent harus membaca seluruh repo untuk memahami konvensi — dan sering salah menebak. Template ini memindahkan konvensi ke berkas yang dibaca agent lebih dulu, lalu memecah sisanya jadi skill yang dimuat hanya saat relevan (*progressive disclosure*).

## Yang Ada di Dalam

- `AGENTS.md` dan `CLAUDE.md` di root, plus berkas aturan untuk editor lain: `.cursor/rules/agents.mdc`, `.github/copilot-instructions.md`, `.windsurfrules`.
- **12 skill** di `.agents/skills/`, antara lain `antislop` (6 varian: code, copywriting, human, layoutmobile, ui, dan guardrail umum), `design-taste-frontend`, `security-audit`, `impeccable`, dan `web-design-guidelines`.
- Library referensi desain di skill `design-taste-frontend`: palet, tipografi, hero, section, motion, dan contoh situs.
- CI di `.github/workflows/ci.yml`.
- `.nvmrc` untuk mengunci versi Node.

## Tech Stack

| Bagian | Teknologi |
| --- | --- |
| Framework | Next.js 16 (App Router) |
| UI | React 19 |
| Bahasa | TypeScript |
| Styling | Tailwind CSS 4 |
| Bundler | Turbopack |

## Mulai

```bash
npm install
npm run dev
```

Buka [http://localhost:3000](http://localhost:3000).

## Struktur

```
AGENTS.md                          # konvensi utama untuk agent
CLAUDE.md                          # turunan untuk Claude Code
.cursor/rules/agents.mdc           # aturan Cursor
.github/copilot-instructions.md    # aturan GitHub Copilot
.windsurfrules                     # aturan Windsurf
.agents/skills/                    # 12 skill, dimuat sesuai kebutuhan
  ├── antislop/                    # guardrail umum
  ├── antislop-code/               # pola kode yang harus dihindari
  ├── antislop-copywriting/        # copy yang tidak robotik
  ├── antislop-ui/                 # cegah UI generik
  ├── design-taste-frontend/       # library desain + referensi
  ├── security-audit/
  └── ...
app/                               # Next.js App Router
.github/workflows/ci.yml
.nvmrc
```

## Cocok Untuk

- Memulai project baru dengan AI agent tanpa hasil "template-y".
- Bereksperimen dengan pola *agent-first* codebase.
- Belajar struktur aturan agent yang scalable.

---

<div align="center">
Dibuat oleh <a href="https://github.com/Ilhamaji">Ilham Aji</a>
</div>
