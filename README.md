# Too old for this sh\*t — MIDI Maze over IP

Slide deck for the talk **“Too old for this sh\*t: MIDI Maze, Atari ST, Raspberry Pico, AI & other bad decisions”** — OpenSouthCode 2026, by **Diego Parrilla**.

The talk takes a 1987 Atari ST game — *MIDI Maze*, the grandfather of the networked first-person shooter — and rebuilds its machine‑to‑machine **MIDI cable ring as a virtual ring over TCP/IP**, using a [SidecarTridge Multi‑device](https://sidecartridge.com) (RP2040) cartridge plus a small Python “ring orchestrator”.

Along the way it uses that project as a lens on a bigger question: **where does AI actually help across the abstraction ladder — from 68000 assembly up to Python — and where is its competence just a confident illusion?**

> The deck text is in **English**; the talk is delivered in **Spanish** (the speaker notes in `slides.md` are written in Spanish).

## Play it

🎮 **Play MIDI Maze in your browser:** <https://midimaze.sidecartridge.com> — rebuilt from the original C sources. Try **Solo mode**, or **Network mode** to play against others.

## Related projects

- **md-MIDI2IP** — the SidecarT firmware + Python orchestrator that bridge MIDI over IP: <https://github.com/sidecartridge/md-MIDI2IP>
- **midi-maze-js** — the in‑browser rebuild of the game: <https://github.com/diegoparrilla/midi-maze-js>
- **SidecarTridge** — the hardware: <https://sidecartridge.com>

## Build the deck

Built with [Slidev](https://sli.dev). Requires **Node.js 18+**.

```bash
npm install
npm run dev        # live-reloading preview at http://localhost:3030 (opens the browser)
npm run build      # static build to dist/
npm run export     # export via Playwright Chromium (also: export:pdf / export:pptx)
```

- Presenter view (slides + Spanish notes): <http://localhost:3030/presenter/>
- Slide overview: press **`o`** in the player.

> A broken asset reference (e.g. `![](/missing.png)`) fails `npm run build` even though `npm run dev` tolerates it — keep referenced files present in `public/`.

## Structure

- `slides.md` — the whole deck. One `##` per content slide; `---` separates slides; frontmatter at the top configures theme/title/fonts; HTML comments are the (Spanish) presenter notes.
- `public/` — images and assets, referenced with an absolute path (e.g. `/sidecart-board.png`).
- `styles/` — custom look layered on Slidev’s stock `default` theme: `index.ts` imports `vars.css` (design tokens) + `main.css` (typography, accents, components).
- `global-bottom.vue` — the persistent pixel footer (title + slide number).

## License

**CC BY‑NC 4.0** (Creative Commons Attribution‑NonCommercial) — see [LICENSE](LICENSE).
Share and adapt for non‑commercial use, with attribution to **Diego Parrilla (sidecartridge.com)**.

Some images are third‑party (game/console box art and screenshots, used for commentary; the
Grace Hopper portrait is U.S. Navy / public domain) and are **not** covered by this license.
