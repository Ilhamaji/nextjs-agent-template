<div align="center">

# Next.js Agent Template

**A Next.js 16 starter designed for AI coding agents** — a clear entrypoint, scoped rules, and *progressive disclosure* so the model stays on track and spends fewer tokens.

[![Status](https://img.shields.io/badge/status-ready%20to%20use-brightgreen?style=flat-square)](#)
[![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Tailwind](https://img.shields.io/badge/Tailwind%20CSS-4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)

**English** · [Bahasa Indonesia](README.id.md)

</div>

---

## About

Most Next.js starters are written for humans. This one is written for **both** humans and AI agents (Claude Code, Cursor, Copilot, and so on).

The problem is that an agent has to read the whole repo to infer conventions — and often guesses wrong. This template moves the conventions into files the agent reads first, then splits the rest into skills that are loaded only when relevant (*progressive disclosure*).

## What's Inside

- `AGENTS.md` and `CLAUDE.md` at the root, plus rule files for other editors: `.cursor/rules/agents.mdc`, `.github/copilot-instructions.md`, `.windsurfrules`.
- **12 skills** in `.agents/skills/`, including `antislop` (6 variants: code, copywriting, human, layoutmobile, ui, and a general guardrail), `design-taste-frontend`, `security-audit`, `impeccable`, and `web-design-guidelines`.
- A design reference library inside `design-taste-frontend`: palettes, typography, heroes, sections, motion, and example sites.
- CI in `.github/workflows/ci.yml`.
- `.nvmrc` to pin the Node version.

## Tech Stack

| Layer | Technology |
| --- | --- |
| Framework | Next.js 16 (App Router) |
| UI | React 19 |
| Language | TypeScript |
| Styling | Tailwind CSS 4 |
| Bundler | Turbopack |

## Getting Started

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Project Layout

```
AGENTS.md                          # primary conventions for the agent
CLAUDE.md                          # derivative for Claude Code
.cursor/rules/agents.mdc           # Cursor rules
.github/copilot-instructions.md    # GitHub Copilot rules
.windsurfrules                     # Windsurf rules
.agents/skills/                    # 12 skills, loaded on demand
  ├── antislop/                    # general guardrail
  ├── antislop-code/               # code patterns to avoid
  ├── antislop-copywriting/        # copy that does not read like a robot
  ├── antislop-ui/                 # prevent generic UI
  ├── design-taste-frontend/       # design library + references
  ├── security-audit/
  └── ...
app/                               # Next.js App Router
.github/workflows/ci.yml
.nvmrc
```

## Good For

- Starting a new project with an AI agent without the "template look".
- Experimenting with an *agent-first* codebase layout.
- Learning a structure for agent rules that scales.

---

<div align="center">
Built by <a href="https://github.com/Ilhamaji">Ilham Aji</a>
</div>
