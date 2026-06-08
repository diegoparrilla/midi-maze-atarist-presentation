# Logbook

A running record of what we've done on this project. Newest entries at the
bottom. Each entry: date, time (CEST), and what was accomplished.

---

## 2026-06-08

### 16:03 — Initialized project guidance (`/init`)
- Analyzed the repo (only `README.md`, `LICENSE`, `CLAUDE.md` at the time).
- Added a **Project context** section to `CLAUDE.md`; deliberately did not invent
  build/test commands or architecture that didn't exist yet.

### 16:11 — Registered three NotebookLM references
- Added the three notebooks to the `/notebooklm` skill library using "smart add"
  (queried each notebook to derive accurate name/description/topics):
  - **MIDI Maze over IP — MIDI Connectivity & Protocol** (`cc5738ad…`)
  - **Atari ST/STE/TT/Falcon — Technical Reference** (`9842e9c6…`, already present)
  - **SidecarTridge / Booster Microfirmware Development** (`d0ed0a81…`)
- Added a **Reference notebooks: validate via `/notebooklm`** section to `CLAUDE.md`.

### 16:15 — Chose slide tooling and scaffolded the deck
- Decision: author slides in Markdown, build with **Slidev** (clean modern + retro
  accents; scaffold-only, author writes content).
- Created `package.json` (dev/build/export scripts), `slides.md` starter,
  `public/`, `.gitignore`; installed dependencies; `npm run build` verified green.
- Documented commands/layout/gotchas in `CLAUDE.md`.

### 16:24 — Built a custom Slidev theme (via `frontend-design`)
- Direction: clean light base, hot-orange hero accent, teal links, IBM Plex
  Mono/Sans + Silkscreen (pixel) for chrome only; dark mode supported.
- Added `styles/index.ts`, `styles/vars.css` (tokens), `styles/main.css`
  (typography, maze-cell bullets, accent rules, cover, CSS smiley), and
  `global-bottom.vue` (pixel footer with slide numbers).
- Restyled the cover in `slides.md`; verified by rendering slides to PNG.
- Documented the theme layer in `CLAUDE.md`.

### 16:29 — Created this logbook
- Added `logbook.md` and backfilled the session so far. Going forward, it is
  updated whenever a new task is requested.

### 16:31 — Connected to VS Code Insiders
- Verified the IDE MCP connection is live (read diagnostics for the open file).
  Enables live diagnostics, editor/selection context, and in-editor diffs.

### 16:35 — Captured the talk abstract
- Fetched the OpenSouthCode 2026 proposal (#1085) and recorded the talk's title,
  logistics (26 Jun 2026, 45 min), themes, and tone. Saved as project memory for
  future deck work. Confirmed: deck + conversation in English, talk in Spanish;
  NotebookLM is reference-only.

### 16:40 — Agreed the talk structure
- Adopted a 3-act arc (1986 metal → 2026 stack → AI vs the ladder) structured with
  Patrick Winston's "How to Speak" heuristics (promise, cycling, verbal punctuation,
  fence, the 5 S's, end-on-takeaway). Added the 1986→2026→future evolution spine and
  the salient idea: AI usefulness tracks the abstraction ladder. Title kept cheeky.

### 16:51 — Drafted the full slide-by-slide deck
- Wrote all 29 slides into `slides.md` (Winston discipline: sparse slides, talking
  points in presenter notes). Added CSS for section dividers, placeholder boxes, and
  the abstraction-ladder visual. Updated the cover to the real title. Build green;
  verified key slides (promise, ladder/surprise, takeaway) by rendering to PNG.
  Open items to refine: real diagrams/screenshots/video, the AI-cast specifics, the
  three "personality" moments, and the future prediction (author's own words).

### 16:58 — Reworded the promise slide
- Extended the empowerment promise to cover the future: "By the end, you'll predict
  where AI actually helps — now and in the future." Updated presenter notes to match.

### 17:17 — Added the "inspection loop" evolution slide
- Recreated the dev-loop diagram in-theme (Code → Test → Build & Reload → Inspect →
  Commit → LEARN; Inspect highlighted as the key metric) and added the 2026/AI era
  alongside 1988 and 2023, revealed click-by-click (slow&expensive → fast&cheap →
  judgment). Slotted as the Act 1 → Act 2 bridge (slide 12/30). Per-step timing table
  and the "all three eras at once = the abstraction ladder" tie-in live in the notes.
  Added CSS for the circular loop + era cards; build verified by render.

### 17:32 — Added the teenage Diego portrait to slide 3
- Converted the embedded `diego_sprite.h` C array (139×141 indexed sprite, the
  digitised NEOchrome self-portrait) from ../md-framebuffer-template into a real
  transparent PNG (`public/diego16.png`), rendered with the demo's cojo_palette
  (grey skin ramp, steel-blue shirt, index 15 → transparent). Placed it on slide 3
  (the "1980s traumas" intro), upscaled pixel-crisp with a pixel-font caption.
  Build verified by render.

### 17:39 — Turned slide 3 into a collage
- Downloaded three SidecarTridge images into `public/` (Pico W board, wordmark logo,
  520 ST + cartridge photo) and combined them with the teenage-Diego portrait into a
  scrapbook collage (white frames, slight rotations, soft shadows) on slide 3.
  Added `.collage` CSS; tightened the layout into an overlapping cluster; verified by render.

### 17:43 — Added the SidecarT / SidecarTridge origin story to slide 3
- Rewrote slide 3's bullets into the real arc: Logroño guy → COVID nostalgia → old
  Atari ST → created **The SidecarT** → founded **SidecarTridge**. Put the full warm
  COVID backstory ("we thought we might all die, so we looked back to when we were
  happy → dug out an Atari ST → soldering the first SidecarT") in the presenter notes.

### 17:51 — Reworked slide 6 into the FPS lineage
- Reframed slide 6 as "MIDI Maze (1987): the first FPS — the oldest ancestor of the
  genre." Downloaded fair-use cover art via the Wikipedia API into `public/` and built
  a single-row polaroid lineage: MIDI Maze (highlighted root) → Wolfenstein 3D '92 →
  Doom '93 → Quake '96 → Half-Life '98 → Halo '01 → Call of Duty '03. Added `.lineage`
  CSS; verified by render.

### 17:56 — Built the MIDI ring diagram (slide 7)
- Replaced the placeholder on "The trick: a MIDI ring" with a real SVG: five Atari STs
  in a ring, MASTER (P1) highlighted, clockwise arrows showing MIDI OUT → next MIDI IN,
  "up to 16 players · one loop" in the center. Two-column layout (explanation left,
  diagram right). Added `.ring-*` SVG CSS; verified by render.

### 18:01 — Elaborated the MIDI ring diagram
- Enriched slide 7's ring: MIDI IN/OUT ports on every node, a "MASTER · sets the tempo"
  annotation, a circulating FRAME token on the cable, center facts (every player's
  position · one lap = one game tick · MIDI @ 31,250 baud), and a footnote on raw 8-bit
  non-standard bytes (0x00 = MASTER) — seeding Act 2's "why a PC can't join."

### 18:15 — Added a gameplay-video slide + vintage MIDI-ring scan
- Inserted a new slide between the FPS lineage and the MIDI ring: an embedded YouTube
  gameplay clip (MIDI Maze 1 v1.0, Xanth FX 1987, id 8hSoy1S43dw) in a responsive 16:9
  frame. Notes flag the network dependency and how to swap for a local MP4 backup.
- Kept the ring SVG; added the original Atari ST manual's "The MIDI-Ring" illustration
  (user-provided, ataribits.weebly.com → `public/midi-ring-photo.png`) beside it,
  CSS-cropped to the drawing and framed as a vintage card. Deck is now 31 slides.

### 18:25 — Added the "ports" slide (MIDI Maze → Faceball 2000)
- Researched the ports via Wikipedia and added a new slide after the FPS lineage:
  "Born on the Atari ST — then everywhere." Atari ST (1987) highlighted as the original;
  cards for the Faceball 2000 ports — Game Boy '91, Super NES '92, PC Engine Super
  CD-ROM² '93, Game Gear '93 — plus a footnote (cancelled: Atari 8-bit/PC/NES/Virtual
  Boy "NikoChan Battle"; clones: MIDI-Maze II, iMaze). Added `.ports` CSS. Deck = 32 slides.

### 18:29 — Built the architecture diagram (Act 2, slide 16)
- Replaced the placeholder on "The architecture" with an SVG flow: Atari ST (unmodified)
  ↔MIDI↔ SidecarT (fakes the rest of the ring) ↔Wi-Fi↔ TCP/IP cloud (the ring, online)
  ↔Wi-Fi↔ SidecarT ↔MIDI↔ Atari ST. Bridges accent-highlighted; MIDI = solid double
  arrows, Wi-Fi = dashed accent. Payoff caption: each ST still thinks it's in a local
  MIDI ring. Added `.arch-*` CSS; verified by render.

### 18:42 — Rebuilt the architecture as a full protocol-stack diagram
- Replaced the simple topology with a stacked diagram per device: Atari ST (MIDI Maze →
  GEM → BIOS/XBIOS → XBRA hook that traps MIDI I/O) → cartridge/TPROTOCOL → SidecarT
  RP2040 (microfirmware → TPROTOCOL⇄TCP/IP → Wi-Fi stack, MIDI payload untouched) →
  TCP/IP routing server (listens + routes to the right SidecarT) → ghosted mirror
  (inverse unwrap) → remote Atari ST. Caption: only the envelope changes
  (TPROTOCOL⟨MIDI⟩ on cartridge, TCP/IP⟨MIDI⟩ on the wire). Added `.arch2-*`/`.dev`/
  `.layer`/`.srv` CSS; verified by render.

### 18:47 — Architecture: show the return path in full
- Un-ghosted the right half — now five full device stacks mirrored about the server.
  Right-side SidecarT and Atari ST use reversed layer order (Wi-Fi→TCP/IP⇄TPROTO→
  microfirmware; XBRA hook→BIOS/XBIOS→GEM→MIDI Maze) so the inverse unwrap reads
  top-to-bottom. Verified by render.

### 18:55 — Architecture refinements (identical stacks, virtual ring, Python)
- Made every device's stack identical on both sides (architecture, not sequence — same
  layers regardless of direction). Added a dashed arc over the whole pipeline joining
  the two end Atari STs, labeled "one virtual MIDI ring — the ends are joined in
  software." Marked the router as a Python TCP/IP server ("routes the ring node → node").
  Added `.ring-arc` CSS; verified by render.

### 18:58 — Architecture: fixed left network link label
- Changed the left SidecarT↔server link label from "Wi-Fi" to "TCP/IP" so both network
  hops read consistently.

### 19:05 — Architecture: packet-flow arrows through the stacks
- Narrowed the layer chips to open side-gutters and added vertical flow arrows crossing
  every layer in each device: orange ↓ "packet out" (right gutter) and teal ↑ "packet in"
  (left gutter), with a legend. Added `.flow-out`/`.flow-in` CSS and an `ahTeal2` marker.

### 19:15 — Animated the architecture slide (click-by-click)
- Staged the SVG with Slidev `v-click`: (1) packet-out arrows, (2) the Python server's
  routing text, (3) packet-in arrows, (4) the virtual-ring arc closes. Added a continuous
  dash-flow animation (`@keyframes pktflow`) so the in/out arrows stream toward their
  arrowheads once revealed. Verified all click frames by `--with-clicks` export.

### 19:21 — Architecture: corrected right-side flow direction
- Flipped the right-half flow arrows so each packet reads as one continuous journey:
  down to wrap on the sender, up to unwrap (bubbling up) on the receiver. Right-side
  orange now points up, right-side teal points down. Updated the legend (down = wrap to
  the wire, up = unwrap into the game).

### 19:23 — Removed the "Why a PC can't just join" slide
- Deleted the old slide 17 at the user's request. Deck = 31 slides.

### 19:36 — Added a BIOS / traps detail slide (after the MIDI ring)
- New two-col slide "Inside the ST: the BIOS" (slide 10): the BIOS as the ST's lowest OS
  layer invoked by 68000 TRAPs (TRAP #1 GEMDOS, #13 BIOS, #14 XBIOS); MIDI = BIOS device
  #3 driven byte-by-byte (Bconstat/Bconin/Bconout); takeaway that raw bytes like 0x00 =
  MASTER aren't valid MIDI (fine on ST, filtered by a modern OS). Sourced from the
  'Reverse Engineering the MIDI Maze Protocol' NotebookLM (trap #13/#14, device 3, raw
  0x00=MASTER confirmed; function names canonical). Deck = 32 slides.

### 19:48 — Retrieved section 2.4.2 from the TFG PDF
- NotebookLM kept returning the same canned summary (stale session), so pulled the source
  directly: downloaded the UNIZAR TFG PDF, installed poppler, extracted section "2.4.2
  Estudio del código ensamblador de MIDI Maze." Confirmed the device I/O model (dev 3 =
  MIDI), ops 1/2/3 = Bconstat/Bconin/Bconout (check −1/0, read, write), trap #13 BIOS /
  trap #14 XBIOS, result in D0, and the 0x00→MASTER trace (jsr $341b2 → BIOS; $188f0 →
  $341a2 → XBIOS reads MIDI IN into D0; tst #$0 → MASTER/SLAVE). Saved the PDF as a
  reference memory ([[midimaze-tfg-source]]). Slide not changed yet (offered to fold in).

### 20:00 — Folded TFG detail in; slide 7 polaroids; reordered asm slide
- Slide 10 (BIOS): added op numbers (1/2/3 = Bconstat/Bconin/Bconout), "result in D0", and
  the 0x00→XBIOS-readback→MASTER note; notes now cite TFG §2.4.2.
- Asm rung slide: replaced the toy snippet with the real Anexo B startup MASTER-claim trace
  ($341b2 BIOS, $341a2/$188f0 XBIOS, tst d0 → MASTER/SLAVE).
- Slide 7: swapped the text platform cards for hardware-photo polaroids (Atari ST original
  highlighted + Game Boy/SNES/PC Engine/Game Gear), like slide 6; downloaded 5 freely-
  licensed Wikimedia console photos to public/ (hw-*.{jpg,png}).
- Moved the "Rung: 68000 assembly" slide to immediately after the BIOS slide (now slide 11)
  so the low-level ST detail is grouped. Deck = 32 slides.

### 20:08 — Repurposed the asm slide into the XBRA hook slide, then relocated it
- Replaced the "Rung: 68000 assembly" slide's content with "Stealing MIDI: the XBRA hook":
  two-col explanation of the XBRA vector-chaining protocol (magic 'XBRA' + cookie + oldp;
  hook the BIOS trap #13; if device 3 = MIDI → SidecarT, else chain to the ROM handler) plus
  an asm snippet of the header + dispatch. (The 68000 MASTER-claim trace was removed in the
  process — can be re-added elsewhere if wanted.)
- Then moved that XBRA slide to sit right after the architecture slide and before "Rung: C"
  (now slide 18). Deck = 32 slides.

### 20:12 — Retitled the XBRA slide as the 68000 rung
- Renamed slide 18 to "Rung: 68000 assembly (the ST)" (XBRA hook = the ST-side asm work),
  restoring the rung trio: 68000 asm (XBRA hook) → C (Pico) → Python (glue).

### 20:16 — XBRA hook: trap BOTH BIOS and XBIOS
- Updated the XBRA-hook rung to trap both MIDI vectors: BIOS trap #13 (Bconin/out/stat,
  dev 3) and XBIOS trap #14 (Midiws, MIDI-IN). Code now installs both via Setexc with a
  hook_bios (device-3 check) and hook_xbios (Midiws check); notes updated.

### 20:19 — Added a "Standard MIDI calls" examples slide (after the BIOS slide)
- New slide 11: two code columns — BIOS (trap #13: Bconout fn3 sequence + Bconstat fn1 /
  Bconin fn2) and XBIOS (trap #14: Midiws fn12 buffer write + Iorec fn14 input record),
  with the "push args → trap → result in D0" takeaway. Sets up the XBRA hook payoff.
  Deck = 33 slides.

### 20:25 — Simplified slide 10 into an ST-vs-PC architecture comparison
- Replaced the BIOS bullets/MIDI-calls two-col with a side-by-side layer map: Atari ST
  (Your game / GEM / GEMDOS trap #1 / BIOS trap #13 / XBIOS trap #14) ≈ a PC (app / GUI
  toolkit / OS+syscalls / std device I/O / hardware drivers), BIOS & XBIOS rows highlighted.
  TRAP = the ST's syscall. MIDI-call detail stays on slide 11. Added `.archcmp` CSS.

### 20:29 — Slide 11 reframed as ST-vs-PC code comparison
- Replaced the BIOS/XBIOS two-col with "Send one MIDI byte — ST vs PC": left = ST 68000
  (Bconout trap #13, raw bytes incl. 0x00); right = PC Python (mido sends MIDI *messages*,
  no API for a bare 0x00, WINMM filters non-standard). Punchline: "different abstraction —
  that gap is the whole project." Mirrors slide 10's ST≈PC framing.

### 20:32 — Slide 11: PC side in C; trimmed caption
- Switched the PC column from Python (mido) to C / WINMM (midiOutOpen + midiOutShortMsg
  packed-message; no call for a raw 0x00). Removed the "That gap is the whole project"
  sentence from the caption.

### 20:34 — Slide 11: noted MIDI is just serial (31,250 baud)
- Added to the ST side: "MIDI is pure serial — a MIDI IN and a MIDI OUT socket at 31,250
  baud. Any byte goes."

### 20:37 — Slide 11: highlighted "the good idea" banner
- Added a bold accent banner: hijack the MIDI IN/OUT at the BIOS & XBIOS level and redirect
  it to a network stack via the SidecarT hardware + firmware. Demoted the abstraction-gap
  caption to a quiet sub-note so the banner dominates. Added `.bigidea` CSS.

### 20:39 — First commit (end of session)
- Added `.claude/settings.local.json` to `.gitignore` (local-only), then committed the
  whole deck to `main`. Verified node_modules/dist stay ignored. Session wrap-up.
