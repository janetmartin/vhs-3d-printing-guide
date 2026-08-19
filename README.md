# VHS 3D Printing Training Guide

**Document:** VHS-3DP-PRUSAMK3 · **Version:** 1.0 (April 2026)

An interactive, mobile-friendly training guide for the Original Prusa i3 MK3S at Vancouver Hackspace. Members use it on a phone or laptop at the printer to learn the machine, complete their first print, and self-check before sign-off.

## What it is

A single self-contained page (`index.html`) — no server, no database, no build step. Runs entirely in the browser via React from a CDN, so an internet connection is required. Progress is **not saved between sessions**.

Covers: how the printer works, a filament decision guide, 5 step-by-step tasks (with checklists, "why" explanations, and per-task quizzes), a good-vs-bad first layer guide, an "Am I Ready?" self-assessment, and "What's Next" after your first print.

## Editing

All content is plain JS objects near the top of `index.html`, inside the `<script type="text/babel">` block. Edit the relevant constant and refresh — no build step.

| Constant | Controls |
|---|---|
| `HOW_IT_WORKS` | Printer parts & mental model |
| `FILAMENT_GUIDE` | Filament decision framework & material table |
| `TASKS` | The 5 tasks — each also holds its own `quiz` array |
| `NEXT_STEPS` | Post-first-print guidance |
| `READINESS` | "Am I Ready?" checklist |
| `DIAGRAM_LABELS` | Printer diagram labels |

Images are embedded as base64 — replacing one means re-encoding and swapping the string.

## Hosting on GitHub Pages

1. Push `index.html` to the root of a public repo.
2. **Settings → Pages → Source → Deploy from a branch → `main` → `/ (root)`**.
3. Live at `https://yourusername.github.io/repository-name`.

## Known limitations

- No persistence between sessions.
- Image edits require hand-swapping base64 strings (no `/images` folder).
- Single ~800-line file — search rather than scroll.

## Printer

Original Prusa i3 MK3S — Vancouver Hackspace

## License

CC0 — public domain. Use, adapt, and share freely.

## AI Disclosure

Created with the assistance of Claude Code.