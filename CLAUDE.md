# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## Project context

Repository for a talk: **MIDI Maze over IP for Atari ST** — the slide deck and
supporting materials for that talk. Licensed **CC BY-NC 4.0** (Attribution-NonCommercial;
see LICENSE). Third-party images (box art, screenshots, the public-domain Grace Hopper
portrait) are excluded.

The deck is authored in Markdown and built with **Slidev** (https://sli.dev).
The talk content itself is written by the author; validate technical claims
against the `/notebooklm` notebooks (see below) before asserting them on a slide.

### Commands

- `npm run dev` — live-reloading presentation server (opens browser).
- `npm run build` — build the static deck to `dist/` (must succeed before pushing).
- `npm run export` / `export:pdf` / `export:pptx` — export via Playwright Chromium.

### Layout

- `slides.md` — the deck. One `##` per content slide; `---` separates slides;
  frontmatter at the top configures theme/title/fonts. HTML comments are presenter notes.
- `public/` — static assets; reference an image as `/name.png` (absolute path).
- Custom look layers on top of the stock `default` theme (do not swap the theme):
  - `styles/index.ts` → imports `styles/vars.css` (design tokens) + `styles/main.css`
    (typography, accents, cover). Slidev auto-imports `styles/index.ts`.
  - `global-bottom.vue` — the persistent pixel footer (title + slide number);
    auto-registered by Slidev.
  - Design = clean light base, hot-orange (`--accent`) hero, teal links, IBM Plex
    Mono/Sans + Silkscreen (pixel) for chrome only. Dark mode via `html.dark` (`d` key).
    Reuse tokens in `vars.css`; helper classes: `.kicker`, `.accent`, `.byline`.

### Gotchas

- A broken asset reference (e.g. `![](/missing.png)`) fails `npm run build` even
  though `npm run dev` tolerates it — keep referenced files present in `public/`.

---

## Reference notebooks: validate via `/notebooklm`

Before making non-trivial claims in code, slides, or docs, validate against the
relevant NotebookLM notebook (all registered in the `/notebooklm` skill library).
Each question opens a fresh browser session and answers only from the sources, so
prefer it over memory for low-level Atari/MIDI/firmware details.

- **MIDI Maze over IP — MIDI Connectivity & Protocol** — the core domain
  notebook. MIDI Maze using the MIDI port as a raw 8-bit serial link
  (non-standard bytes, e.g. `0x00` = ring MASTER), Windows WINMM.dll filtering
  of raw MIDI, Atari BIOS/XBIOS MIDI access (trap #13/#14, serial device 3),
  why virtual MIDI ports fail, and the SysEx-based adapted protocol for PC-to-PC
  multiplayer.
- **Atari ST/STE/TT/Falcon — Technical Reference** — the Atari Compendium and
  related references: TOS/GEMDOS/BIOS/XBIOS, GEM (VDI/AES), hardware (68000, MFP
  68901, YM-2149, Blitter, WD 1772), MIDI/RS-232/DMA interfaces, memory map, and
  development toolchains.
- **SidecarTridge / Booster Microfirmware Development** — building firmware on
  the SidecarTridge (RP2040 ↔ Atari ST cartridge port): repo layout (`/rp`,
  `/target`), `build.sh` producing the `.uf2` + Booster Manager app `.json`, the
  TPROTOCOL command channel (read-only cartridge port via ROM3 reads), and
  RP2040 bus emulation with PIO/DMA.

Workflow: ask focused questions, follow up on gaps (each answer ends with "Is
that ALL you need to know?" — read it and decide), then record the non-obvious
conclusions in a comment or doc so the next reader doesn't have to re-validate.

---

## Working style

These behavioral guidelines bias toward caution over speed. For trivial tasks, use judgment.

### 1. Think before coding

Before implementing:
- State your assumptions explicitly. If uncertain, ask.
- If multiple interpretations exist, present them — don't pick silently.
- If a simpler approach exists, say so. Push back when warranted.
- If something is unclear, stop. Name what's confusing. Ask.

### 2. Simplicity first

Minimum code that solves the problem. Nothing speculative.
- No features beyond what was asked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that wasn't requested.
- No error handling for impossible scenarios.
- If you write 200 lines and it could be 50, rewrite it.

Ask: "Would a senior engineer say this is overcomplicated?" If yes, simplify.

### 3. Surgical changes

Touch only what you must. Clean up only your own mess.
- Don't "improve" adjacent code, comments, or formatting.
- Don't refactor things that aren't broken.
- Match existing style, even if you'd do it differently.
- If you notice unrelated dead code, mention it — don't delete it.
- When your changes orphan an import/variable/function, remove it. Don't remove pre-existing dead code unless asked.

The test: every changed line should trace directly to the user's request.

### 4. Goal-driven execution

Define success criteria. Loop until verified.
- "Add validation" → "Write tests for invalid inputs, then make them pass"
- "Fix the bug" → "Write a test that reproduces it, then make it pass"
- "Refactor X" → "Ensure tests pass before and after"

For multi-step tasks, state a brief plan with a verification check per step.

### 5. No AI attribution

Never add AI-tool attribution to commits, PR descriptions, code comments,
docs, or any other artifact. This means **no**:
- "Generated with Claude Code", "Co-authored by Claude", "Made with ChatGPT",
  or any similar phrasing.
- `Co-Authored-By: Claude …`, `Co-Authored-By: ChatGPT …`, or any other
  AI co-author trailer.
- "AI-assisted", "written with the help of an LLM", etc., as comments or
  changelog entries.

Write the message as the human author. Do not mention AI tools used to
produce the work.
