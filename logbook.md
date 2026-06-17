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

### 20:46 — Optimized public/hw-gameboy.png
- Downscaled the Game Boy photo from 2820×3420 (6.4 MB) to 659×800 (480 KB) with `sips`
  — ~93% smaller, no visible loss at the polaroid size. Verified by render.

### 18:13 — Renamed the architecture slide
- Slide 18 heading "The architecture" → "The Candidate Architecture", setting up a
  candidate → (revisions) → "Final Architecture" arc to be added later. Uncommitted.

### 18:25 — Added real SidecarT photo to slide 20
- Placed a real photo (SidecarT RP2040 board beside the Atari ST) on the "Rung: C (the
  Pico)" slide, replacing the placeholder; made it two-col (bullets left, framed photo
  right). Compressed the source from 40 MB PNG to 268 KB JPEG (1400px). Uncommitted.

### 18:46 — Reordered Act 2: introduce SidecarT + the goal before the architecture
- The architecture was dropping SidecarT/RP2040 on the audience with no intro. Fixed:
  renamed the Act 2 divider "The stack" → "Faking the MIDI ring"; added two slides before
  "The Candidate Architecture": (1) "Meet the SidecarT" (device intro: cartridge port,
  RP2040 + Wi-Fi, microfirmware, TPROTOCOL; board photo) and (2) "The plan: one virtual
  ring" (new SVG: ST+SidecarT nodes around a central "Ring Orchestrator" — dashed virtual
  ring + solid TCP/IP spokes). Renamed the architecture's server box to "Orchestrator" and
  updated the Act 3 recap. Added `.goal-svg/.spoke/.vring` CSS. Deck = 35 slides. Uncommitted.

### 18:57 — Moved the inspection-loop slide to the conclusion; added an Atari ST primer
- Moved "Number of inspections = the key metric" out of Act 1's setup to right before
  "What to take home" (it's the same 1988→2026 evolution thesis as the takeaway; now the
  conclusion zoom-out after the demo). Rung 1 → Act 2 now joins cleanly.
- Added a new slide before the MIDI ring: "Wait — what's an Atari ST?" (1985 home computer,
  68000, GEM, built-in MIDI ports; 1040 ST photo + "older than you" line) for audience
  members who never saw one. Deck = 36 slides. Uncommitted.

### 19:07 — Enriched "Meet the SidecarT" (slide 18)
- Reframed the headline ("not a ROM emulator — a bizarre coprocessor") and condensed to
  four bullets adding: 2,200+ built (+ ~200–400 clones) and open-source licensing (firmware
  GPL, hardware CC non-commercial). Avoided an 8-bullet wall by merging the tech lines.

### 19:18 — Populated slide 22 (Rung: C) from the md-MIDI2IP repo
- Explored ../md-MIDI2IP (the real project) and cherry-picked concrete RP2040-firmware
  facts: ~4,800 lines C+PIO, 225 MHz overclock, read-only cartridge → ROM emulation +
  ROM3 PIO/DMA snoop, 16 KB in/out queues, lwIP TCP @ 1 ms poll. Added the throughput
  war story as a banner: v1 per-byte handshake ~970 B/s (3× slower than 1987's 3125 B/s)
  → v2 fire-and-forget streaming beat the original ring (EPIC-09). Repo also has 12 epics
  + a Python orchestrator (~830 LOC) available for other slides.

### 19:33 — Narrative principle: candidate = first assumptions only
- Agreed the deck arc: everything up to/including The Candidate Architecture + the rungs
  presents only FIRST ASSUMPTIONS; the "how we had to change it" is a later reveal
  ("Reality bites → The Final Architecture") placed at the END of Act 2, before Act 3.
- De-spoilered slide 22 (Rung: C): removed the v2 fire-and-forget banner + the ~970 B/s
  verdict; reframed as the lock-step, byte-by-byte handshake assumption (mirror the cable).
  Audited the other rungs + Candidate Architecture — clean (no solution leaks).
- TODO next: build the "Reality bites → The Final Architecture" turn at the end of Act 2.

### 19:41 — Enriched the C and Python rungs (first-version only)
- Slide 22 (Rung: C): added the TPROTOCOL bullet — the SidecarT's command channel, built
  for synchronous multi-KB buffers/commands, so per-byte MIDI drags lots of plumbing
  (sets up the later throughput reveal without spoiling it).
- Slide 23 (Rung: Python): replaced the generic bullets with first-version specifics from
  the repo — the asyncio ring orchestrator (smart: master election, flow-control, match
  coordination), the Hatari gateway software peer, self-test harnesses. Notes flag not to
  reveal the later dumb-relay simplification.

### 19:50 — Slide 23: removed Hatari (held for v2)
- Dropped the Hatari gateway bullet from the Python rung; it'll be introduced later to
  justify version 2. Replaced with self-test harnesses & packet inspection. Notes flag the
  deferral.

### 20:00 — Populated slide 24 (The AI cast)
- Filled the AI cast with the real tools/roles: OpenAI Codex/ChatGPT 5.4 & 5.5 (Codex →
  firmware/TPROTOCOL C+68000 optimisation; ChatGPT → research + architecture), Anthropic
  Claude Code 5.7 & 5.8 (solution coding + this deck), GitHub Copilot (code reviews),
  Google NotebookLM (Atari books + the MIDI-Maze TFG by Jesús Ángel González Gorrado).

### 20:05 — Committed + pushed the Act 2 restructure batch
- Commit 5b06934 "Restructure Act 2 and flesh out the build slides" pushed to origin/main.

### 20:12 — Built the "Reality bites → The Final Architecture" reveal (end of Act 2)
- Added two slides between the Python rung and the AI cast: "…then reality bit" (throughput
  collision: 1987 cable 3,125 B/s vs v1 ~970 B/s, 3× slower; Hatari introduced to iterate)
  and "The Final Architecture" (candidate→final·v2 diff: per-byte→fire-and-forget DMA
  stream, smart→dumb-relay orchestrator, +Hatari peer; banner: beats the 31,250-baud ring).
  Drafted from md-MIDI2IP facts (marked DRAFT in notes). Deck = 38 slides. Uncommitted.

### 20:22 — Made the abstraction ladder an evolving motif
- Added a "Research — architecting the solution" rung above Python on the "surprise" ladder
  (now Research brilliant · Python great · C mediocre · 68000 asm improvising — clean
  gradient; nudged Python brilliant→great to keep the top→bottom order).
- Added an earlier, UNGRADED copy ("The abstraction ladder", the map) before Rung 1 — same
  four rungs, no verdicts, with a "later we'll ask how AI did" teaser. So the ladder appears
  twice: map first, graded report card at the Act 3 surprise. Deck = 39 slides. Uncommitted.

### 20:45 — Added "Architecting with ChatGPT 5.4/5.5 Research mode" (slide 17)
- New slide after the abstraction ladder: ChatGPT research-mode failures when asked to
  architect MIDI Maze over IP (physical-layer box, wiring the SidecarT to the MIDI ports,
  over-engineering). Generated a QR (qrencode → public/qr-chatgpt-research.svg) linking to
  the shared research session; captioned "Read the research →". Deck = 40 slides. Uncommitted.
- OPEN TENSION: this slide shows ChatGPT struggling at Research/architecture, but the ladder
  rates "Research = brilliant" — user to decide whether to downgrade that rung.

### 20:52 — Slide 17: added the orange "lesson" banner
- Added a .bigidea banner (like slide 12): the architecture problem was too complex for a
  good/simple out-of-the-box solution → "We must guide the research."

### 21:03 — Added "The Candidate Architecture V1++" (slide 27)
- Copied the Candidate Architecture between "…then reality bit" and "The Final Architecture";
  renamed to V1++ (marker IDs →3 to avoid SVG id clashes). Added a Hatari emulator + the
  hatari-gateway (Python tool from md-MIDI2IP) hanging off the orchestrator — Hatari ⇄ file
  FIFOs ⇄ gateway ⇄ TCP/IP ⇄ orchestrator — revealed on click 5 as the "++"; a software peer
  so you can test/play without a second real ST. Extended viewBox + capped width to fit.
  Deck = 41 slides. Uncommitted.

### 21:20 — Reordered Act 2 reality sequence + de-animated V1++
- New slide 26 "MIDI-ring booh-booh": a single ST won't ring (doesn't become MASTER, game
  never starts, returns the "MIDI-ring booh-booh" error) → orange THE FIX banner: add a
  computer we know works. Moved "…then reality bit" to AFTER V1++ (now 28). Sequence:
  26 booh-booh → 27 V1++ (Hatari peer) → 28 reality bit → 29 Final Architecture.
- Slide 27 (V1++): removed all v-click — the full diagram (incl. Hatari + hatari-gateway)
  now draws in a single shot.
- Slide 28: added the orchestrator realization — two wrong calls surface: transport (3× too
  slow) AND the "smart" orchestrator was overkill → need a fast relay that inspects/peeks,
  never parses. Deck = 42 slides. Uncommitted.

### 21:28 — Slide 28: split the two failures by kind (speed vs correctness)
- Transport problem reframed as SPEED and scoped to the hardware path: the per-byte TPROTOCOL
  handshake crawls only on SidecarT + real Atari ST (cartridge lock-step); the Hatari +
  hatari-gateway peer is fine — runs at the full speed of Hatari's MIDI emulation → bottleneck
  is the hardware bridge, not the idea. Relabeled the "bad" era card to "v1 · SidecarT + real ST".
- Orchestrator problem reframed as CORRECTNESS: the "smart" master-election logic came from a
  wrong reading of the MIDI protocol in the TFG; we just need a fast relay that peeks, never
  parses. Build OK. Deck = 42 slides. Uncommitted.

### 21:34 — Moved "The AI cast" earlier (was 30 → now after "The ingredient list of doom")
- The AI cast now sits between "The ingredient list of doom" (15) and "The abstraction ladder"
  (16) — the cast of AI tools is introduced before we map them onto the ladder / research slide,
  instead of late in Act 2. Pure relocation, no content change. Build OK. Deck = 42 slides. Uncommitted.

### 21:50 — Reworked "The Final Architecture" → visual "The Final Architecture V2" (slide 30)
- Replaced the plain Candidate-vs-Final table with a visual layout: three EPIC "fix cards"
  (struck-through old assumption → accent fix → green ★ win badge) + a throughput-leap bar chart.
- Content validated against md-MIDI2IP Iteration-2 epics (Explore agent):
  - EPIC-09 (Transport): drop per-byte TPROTOCOL handshake → fire-and-forget stream on the
    commemul ROM3 ring (bit-8 OUT, bit-9 IN + confirm-ack); kills the ~970 B/s ceiling.
  - EPIC-11 (Orchestrator): the "smart" RingState was a master-election heuristic built on a
    MISREAD of the MIDI protocol (master-flip bug) → rip out, dumb byte relay + live telemetry.
  - EPIC-10 (Proof): real 2-player match on hardware behind an automated self-test gate.
- Accuracy fix: dropped the old "beats the original 31,250-baud ring" overclaim — the repo only
  claims the handshake ceiling is gone and the maze is playable on real hardware (parity, not
  out-running the cable). New CSS: .v2grid/.v2card/.speed in styles/main.css. Build OK. Deck = 42 slides.

### 21:58 — Slide 30 (V2) tweaks: drop EPIC tags, rename Proof card
- Removed the "EPIC-09/10/11 ·" prefixes from the three fix-card badges (now just Transport /
  Orchestrator / Proof). Renamed the Proof card role "Prove it on metal" → "Prove metal + Hatari"
  and folded the Hatari software peer (via the gateway) into its body. Build OK. Deck = 42 slides.

### 22:10 — Added the "deletions, not additions" outcome (slide 30 + conclusions)
- Slide 30 (V2): added a dashed-divided "THE PATTERN" line under the throughput bars — both
  engineering wins (EPIC-09 handshake, EPIC-11 RingState) were deletions, not additions.
- "What to take home" (slide 41): added an orange "REMEMBER THIS" bigidea banner highlighting
  the same lesson — "the new craft is knowing what not to build" — tied to the judgment spine.
- New CSS: .subtract in styles/main.css. Build OK. Deck = 42 slides. Uncommitted.

### 22:25 — Slide 18: added the "why" diagnosis (anchoring) for ChatGPT's suboptimal architecture
- Added a compact .diag box between the symptom bullets and the lesson banner: the behaviour is
  ANCHORING — locks onto its first draft and only edits it (local search), never re-derives;
  hints get grafted on, bloat survives; optimises for coverage/robustness not simplicity →
  "correct, but operationally absurd". Shortened the lesson banner to make room.
- Presenter notes expanded with the full diagnosis (belief/solution persistence, context inertia /
  trajectory dependence, hysteresis; why = consistency rewarded in training vs discarding work;
  the Kafka+CQRS+Saga-for-500-users over-engineering example). New CSS: .diag. Build OK. Deck = 42 slides.

### 22:45 — New slide 19 "Technically correct. Operationally absurd." (over-engineering illusion)
- Added after the ChatGPT-research slide: a wrapped "buzzword tower" (REST→Kafka→CQRS→Event
  Sourcing→Redis→ElasticSearch→Saga→Metrics) "…to relay a handful of MIDI bytes between 2-4 STs",
  punchline "Nothing is wrong. Everything is unnecessary." (green/red), and an orange THE ILLUSION
  banner: research-grade AI LOOKS most competent at the top of the ladder, but it's an illusion that
  needs expert verification. New CSS: .oe-need/.oechips/.oechip/.oearr/.oe-punch. Build OK. Deck = 43 slides.

### 22:55 — "The surprise" ladder re-graded to resolve the Research-rung tension
- Changed thesis "AI is only as good as the abstraction is high." → "AI is confidently wrong at
  both ends." Research rung re-graded from green "brilliant" to a dashed-green "illusion" rung
  reading "looks brilliant ⚠" (new .rung.illusion CSS: looks solid, isn't). Closing line →
  "Loud at the metal. Seductive at the top — it looks best exactly where you can least trust it."
- Now consistent with the new slide 19 (illusion) + slide 18 (anchoring). User chose this option.
  Build OK. Deck = 43 slides.

### 23:10 — Slide 19: replaced the generic buzzword chain with ChatGPT's REAL over-engineered proposal
- The REST→Kafka→…→Metrics example was a placeholder. Swapped in the actual "deep research" v1
  ChatGPT proposed for MIDI Maze over LAN: 16× custom opto-isolated MIDI daughterboards (6N138 /
  5 V level-shifters) → dedicated 2.4 GHz router → central Linux ring server → framed TCP + CRC32 →
  heartbeats + telemetry → Atari TSR + command catalog → 3-month Gantt + 16× BOM.
- New contrast line: "…to forward bytes the SidecarT already carries over its cartridge port — in
  pure firmware, zero new hardware." Kept the "Nothing is wrong / Everything is unnecessary" punch
  and THE ILLUSION banner. Presenter note updated with the full absurd proposal. Build OK. Deck = 43 slides.

### 23:20 — New slide 20: audience "show of hands" beat (motto callback)
- Added a statement-layout slide after the over-engineering reveal: kicker "A quick confession 🙋",
  joke "I'm too old to solder 16 daughterboards because a chatbot told me to." (callbacks slide 19 +
  the "Too old for this sh*t" motto), then an audience show-of-hands question: who's survived a
  "technically correct, operationally absurd" masterpiece? Presenter note guides the interaction.
  "Rung 1" shifts to slide 21. Build OK. Deck = 44 slides.

### 23:35 — Repurposed the stranded "Rung 1" landmark into a pivot (slide 21)
- After the reordering, "Rung 1 — That was the metal. Hold onto it." had lost its referent (the
  slides before it are the AI cast / ladder / research rung, not the metal) and sat back-to-back
  with the ACT 2 divider. Reworded to "Our turn. / We guide it ourselves — one rung at a time.
  (the metal's still down there; we'll be back.)" — bridges the "must guide the research" lesson
  into ACT 2's build and teases the rung climb. Build OK. Deck = 44 slides.

### 23:55 — New slide 33 "The Final Architecture V2 — the wiring" (V1++ diagram, evolved to v2)
- Cloned the V1++ stack diagram (new marker ids *4 to avoid SVG id clashes) and evolved it to v2,
  highlighting slide 32's wins visually: SidecarT bridge boxes "TPROTO ⇄ TCP/IP" → "stream ⇄ TCP/IP"
  with accent glow + "fire-and-forget" note; inter-node hops labelled "stream" and animated;
  orchestrator "routes the ring/node→node" → "dumb relay / peeks · never parses" with accent glow.
  Unchanged pieces (XBRA hook, kept-intact MIDI, Hatari peer) left neutral. Bottom: two change chips
  (Transport / Orchestrator before→after). Shrank SVG to 760px so the chips fit on one row.
- New CSS: .layer.bridge.upd, .srv.upd, .flow2.stream, .dchanges/.dchange. Build OK. Deck = 45 slides.

### 00:25 — ACT 3 full reframe around the Research/illusion finding
- The old act was monotonic ("better the higher you go"); its slogan "Brilliant senior at the top /
  confident intern at the bottom" directly contradicted the new Research finding. Rewrote the spine:
- Personalities now climb bottom→top with a twist: P1 the intern (asm, FAILS LOUD/green), P2 the
  junior (C, FAILS QUIETLY/amber), P3 the senior (Python, EARNS YOUR TRUST/green — the setup),
  P4 the consultant (Research, FAILS SILENT/accent — "looks like the senior, so you stop checking;
  that's the trap" + 16-daughterboard callback). New visible-vs-invisible-failure framing via .fmode badges.
- New slogan slide: "The intern improvises. The architect over-engineers. Both sound certain. / The
  dangerous one is the architect — because it's the one you believe." (replaces the false slogan).
- Retitled "Reverse engineering with AI" → "Working with AI (without losing faith in humanity)";
  bullets reframed: verify hardest where it's most convincing; make it show sources; keep the judgment.
- "What to take home": fixed the middle line — AI *looks* strongest where we've climbed highest, so
  verify hardest there. Kept demo / inspections-loop / deletions banner / close. New CSS: .fmode.
  Fixed an accidental duplicate "Did it work?" heading. Build OK. Deck = 46 slides.

### 00:45 — Slide 37 (Personality 1 · the intern): real 68000 failures + actual code + corollary
- Replaced the placeholder with three real failures from the project's 68000 work: (1) emits 680x0
  instructions (68020/030) the bare 68000 lacks; (2) repeatedly stores into ROM space despite
  guidelines that ROM is read-only; (3) over-complicated control flow — branches to a shared
  .mbt_rte label just to execute an rte.
- Added the real before-pattern asm (from md-MIDI2IP commit 3d0e422 userfw.s: bra.s .mbt_rte → shared
  rte) as a code block; the clean version is just "move.l MIDI_IN_STATUS,d0 / rte" inline.
- Added a "THE COROLLARY" banner: you don't prompt it away — you iterate the generated code until the
  AI nails it. Two-column flex (failures | code). Build OK. Deck = 46 slides.

### 00:52 — Slide 37: renamed banner label "THE COROLLARY" → "THE RULE"
- "Corollary" read too academic for a punchy talk banner and undersold the "mandatory" tone; "THE
  RULE" is crisper and fits the deck's spark-label set (THE LESSON / THE PATTERN / THE ILLUSION).

### 00:55 — Slide 37: banner label → "NON-NEGOTIABLE"
- Changed the spark label from "THE RULE" to "NON-NEGOTIABLE" (user's choice) — leans hardest into
  the mandatory-iteration tone.

### 01:10 — Slide 38 (Personality 2): reframed C rung as "the contractor" (flawless code, fatal spec)
- Rewrote per real experience: AI writes excellent C (iterate → optimized); the MCU hazard is
  testing/validation, solved by a pre-built microfirmware framework + Claude skill for sandboxed dev →
  sniper-precise, crash-free, hugely productive. THE CATCH: it still failed because the SPEC was wrong
  (synchronous commands), not the code. Badges: CODE·FLAWLESS (green) / SPEC·FATAL (accent).
- Sharpens the act: failure climbs code (asm) → spec (C) → architecture (consultant). Renamed
  "the junior" → "the contractor" (pairs with P4 the consultant/architect). Build OK. Deck = 46 slides.
- OPEN: slide 36 "The surprise" ladder still rates C as "mediocre" — now contradicts P2's "flawless".

### 01:20 — Slide 38: made the code-vs-spec iteration contrast explicit
- Per user: P1 = iterate over the CODE; P2 = iterate over the SPEC. Updated THE CATCH banner to:
  "The code was flawless; the spec was fatal — synchronous commands killed us. With the intern you
  iterate the code. With the contractor you iterate the spec." Note updated with the key contrast.

### 01:28 — Slide 36 "The surprise": C rung re-graded mediocre → "strong · sandboxed"
- Reconciled with Personality 2's "CODE · FLAWLESS": C is genuinely strong given a harness; the failure
  was the spec (Research rung), not the code. Ladder now: Research=looks brilliant⚠, Python=great,
  C=strong·sandboxed, asm=improvising. Both-ends thesis intact (problem rungs are the two ends).

### 01:40 — Slide 39 (Personality 3 · the senior): Python = the delegation peak
- Reworked per real experience: no framework hand-holding (picks a good design from the spec);
  flawless + trivially testable; FULLY AGENTIC self-driving loops (write→test→fix→green, validity
  checks automated); spec is still the limiter but the test suite surfaces spec flaws fast.
- Badges: EARNS YOUR TRUST + FULLY AGENTIC (both green). Banner "DELEGATE IT": with good structured
  specs you can hand most of the work to agentic AI; what's left is the spec + judgment (sets up P4).
- Completes the through-line: iterate code (P1) → iterate spec (P2) → delegate the whole loop (P3) →
  but the spec/architecture is the illusion (P4). Build OK. Deck = 46 slides.

### 01:55 — Slide 40 (Personality 4): reworked into the act's payoff; renamed consultant → architect
- Given the refined P1→P3 through-line, rewrote P4 to pay it off: callback that the fatal spec (sync
  commands) was authored HERE; invisible failure (no crash, over-engineered, you ship it); the trust
  trap (looks like the senior you just delegated everything to). Dual badges LOOKS BRILLIANT⚠ (amber) /
  FAILS SILENT (accent). Pinpoint banner "THE ONE THING YOU CAN'T DELEGATE": delegate everything below;
  the spec & architecture stay human because competence here is an illusion.
- Renamed character "the consultant" → "the architect" (matches the approved slogan "the architect
  over-engineers" + pairs with P2 "the contractor": architect designs, contractor builds). Updated all
  consultant refs in notes. Build OK. Deck = 46 slides.

### 02:10 — Slide 42 "Working with AI": rewrote takeaways to distill ACT 3
- Replaced the 3 pre-reframe bullets with 4 leverage-ordered playbook items grounded in the act:
  (1) Build the sandbox first (harness = highest-value human work, P2/P3); (2) Delegate the loop, own
  the spec (agentic code loop, keep spec/architecture/judgment, P3/P4); (3) Iterate the right layer
  (code low, spec high, P1/P2); (4) Distrust the most polished answer (architect illusion + cite
  sources/NotebookLM, P4). Kept the human closing line "You stay the engineer — buddy, not the boss."
  Build OK. Deck = 46 slides.

### 02:25 — Slide 45 "What to take home": de-echoed vs slide 42; lands as the philosophical finish
- 2026 rung: dropped tactical "so verify hardest there" (echoed 42#4) → states the illusion as a
  principle: "AI looks most brilliant exactly where it's least reliable". Future rung: "judgment &
  verification" → "humans climb up — to judgment & taste" (drops 'verify', 42 owns it; adds role-
  inversion). Now 42 = tactical playbook, 45 = the arc + principle + deletions kicker. No verbatim echoes.
- Fixed a flex-layout bug: inline <em> split the 2026 rung into separate flex items (pushed "least
  reliable" right); wrapped the description in a <span> so it wraps as one unit. Build OK. Deck = 46 slides.

### 02:35 — Slide 43 "Did it work?" → "Demo time!" (live demo holder)
- Per user (will run the demo live): converted to a statement-layout holder — big "Demo time! 🕹️"
  + subtitle "MIDI Maze, multiplayer, over IP — live on real hardware." Removed the video placeholder;
  note updated for the live setup with a recorded clip as fallback. Build OK. Deck = 46 slides.

### 02:50 — Slide 44 "Number of inspections": tightened the loop (review fix)
- Single spine now: reordered to a correct clockwise cycle Code → Build & Reload → Test → Inspect →
  Commit (build-before-test, inspect-before-commit); dropped the redundant LEARN! node; Inspect is the
  sole hero (is-key). Title (inspections) + hero (Inspect) + center ("you only learn once per lap") now
  agree — inspection = the learning moment. 5 nodes at 72° spacing. Note updated. Build OK. Deck = 46 slides.

### 03:05 — Slide 44: added per-step time-per-era breakdown to each era card
- New .era__steps line in each card showing time per loop step, Inspect highlighted (accent): 1988
  Code20m/Build8m/Test5m/Inspect12m/Commit1m; 2023 5m/5s/10s/Inspect2m/5s; 2026 ~0/~0/~0/Inspect←all
  yours/~0. Shows mechanical steps collapsing to 0 while Inspect becomes the whole cost (ties title +
  "bottleneck moves to judgment"). Fixed contradictory 2026 desc "Inspections ≈ free" → "AI runs the
  mechanical lap — iterating is ≈ free". Times are illustrative/adjustable. Build OK. Deck = 46 slides.

### 03:30 — Slide 44: replaced made-up times with research-anchored ones + per-era cycle summary
- Investigated (web): floppy compile/link ≈ minutes ("five minutes…", multi-min on floppy systems);
  modern HMR ~instant (<1s), devs notice >15s; AI code synthesis ≈ 8.4s avg, agent runs build/test
  itself. Applied: 1988 Code3m/Build5m/Test2m/Inspect3m/Commit2m → ≈15 min/lap; 2023 1m/<1s/5s/
  Inspect30s/5s → ≈2 min/lap; 2026 Code~8s/Build auto/Test auto/Inspect=you/Commit auto → loop ≈ free.
- "Summarize each cycle": folded a per-era cycle total (≈15 min/lap, ≈2 min/lap, loop ≈ free) into the
  verdict line. Times labelled representative/adjustable in the note. Build OK. Deck = 46 slides.

### 03:45 — Slide 44: corrected the unrealistic 2026 "~8s" timing (user pushback)
- The ~8s was a misapplied benchmark (single LLM call latency), NOT real agentic dev time. Same source
  gives agentic coding ≈ 8–48 min/task, multi-iteration. Fixed 2026 card: "agent drives the whole loop —
  you supervise & review"; steps Code AI/Build auto/Test auto/Inspect=you/Commit auto; verdict
  "agent: ~10–40 min & many tries · you: review → bottleneck is judgment". Dropped "loop ≈ free".
- Reframed honestly: the 2026 loop didn't get faster, it MOVED — agent runs it (minutes, unattended),
  human cost collapses onto review/judgment. Note updated to warn against overselling speed. Deck = 46.

### 04:00 — Slide 44: reframed around iterations-to-ship-a-feature (X > Y >> Z) per user
- Added the fundamental metric the slide was missing: laps (iterations) to build a feature collapse across
  eras — ~40 (1988) > ~12 (2023) >> ~3 (2026). Why: 1988→2023 better tools/frameworks/knowledge do more
  per lap; 2023→2026 the agent FOLDS many human iterations into its own internal loop.
- Kicker under title: "Same loop every era — but the laps to ship a feature keep collapsing." Each era
  verdict now leads with bold laps/feature (× time/lap). 2026: "~3 laps — folds many iterations into one →
  review is the bottleneck"; desc "agent grinds the loop ~10–40 min, many tries". Note updated. Build OK. Deck = 46.

### 04:20 — Slide 44: fixed the bogus minutes-per-feature (user: "shamefully wrong")
- Root cause: "Code" (human work/lap) was set absurdly low (1m in 2023) → laps×per-lap implied 24 min to
  build a feature. Raised Code to realistic values so per-lap totals are sane and laps × time/lap = feature
  total: 1988 ~24min/lap ×40 ≈ 2 days; 2023 ~20min/lap ×12 ≈ 4 hrs; 2026 ~20min review ×3 ≈ 1 hr of your time.
- Verdicts now show realistic feature totals (≈2 days → ≈4 hrs → ≈1 hr of your time). Kicker: "laps AND the
  hours to ship a feature keep collapsing." Note updated. Math is self-consistent. Build OK. Deck = 46 slides.

### 04:35 — Slide 45 "What to take home": 2026 rung updated to carry slide-44's work-shift
- 2026 rung now: "we live at the top — AI writes the code, you judge it; and it dazzles exactly where
  it's least reliable" (was just the illusion line). Integrates slide-44's finding (work shifts from
  writing → judging/review) with the illusion; sharpens 1986↔2026 parallel (humans went down to do the
  low work in '86; AI does it and humans judge in '26). Future rung + durable-skill line + deletions
  banner unchanged. Build OK. Deck = 46 slides.

### 04:45 — Slide 45: added the 2023 rung (end of the human-coding era) per user
- Ladder was 1986→2026→future; added 2023: "peak human coding: best tools, frameworks & knowledge — and
  the last era we wrote every line". Makes the hand-off explicit (2023 = last human-written-code era,
  2026 = AI writes / you judge). Now 4 rungs + durable-skill line + deletions banner; fits. Build OK. Deck=46.

### 05:30 — Consistency pass (reviewed full deck; fixed 6 inconsistencies, each user-approved)
1. Era year: unified "old era" to 1986 everywhere (inspections slide 1988 → 1986; was clashing with
   Act 1 / Act 3 recap / take-home).
2. AI-cast → personalities: fixed stale speaker note (Act 3 grades by abstraction level, four
   personalities — not the named tools; was "three personalities"). Slide unchanged (no on-screen clash).
3. AI cast: ChatGPT line → neutral "research & architecture drafts" (was "designed the solution and
   architecture", which pre-contradicted the Act 3 illusion finding).
4. Orchestrator naming: box labels all "Orchestrator" (was "Ring Orchestrator" on The plan).
5. V2 slide titles distinguished: 32 = "…V2 — the fixes", 33 = "…V2 — the wiring".
6. Stale speaker notes: slide 18 (dropped resolved "downgrade the rung" line; Kafka example →
   real 16-daughterboard example) and slide 45 (spine now 1986 → 2023 → 2026 → future).
Build OK. Deck = 46 slides. Uncommitted (on top of 34b5ae7).

### 05:45 — Improvements pass (user-approved each)
A. Slide 6 title "the first FPS" → "the FPS's grandfather" (defensible vs Maze War; matches body copy).
B. AI version numbers (ChatGPT 5.4/5.5, Claude Code 5.7/5.8) — kept as-is per user (real versions).
C. Closing byline: replaced <repo>/<handle> placeholders with real links — Diego Parrilla ·
   sidecartridge.com · @sidecartridge · @soyparrilla · github.com/sidecartridge/md-MIDI2IP.
Reminders (no edits): keep local MP4 fallback for the gameplay embed + live demo; verify QR scans on the projector.
Build OK. Deck = 46 slides. Uncommitted (on top of 34b5ae7).

### 06:05 — New slide 15 "Who's this lady?" (Grace Hopper)
- Added an audience-hook slide before "The ingredient list of doom": Grace Hopper's official US Navy
  portrait (public domain, downloaded to public/grace-hopper.jpg, 960x1200) + the question "Who's this
  lady?" and prompt "No Googling. Shout it out." Speaker note: she built the first compiler — the first
  rung up the abstraction ladder the talk rides on — leading into the AI cast / ladder. Build OK. Deck = 47 slides.

### 06:15 — Slide 15 (Grace Hopper): added the compiler-history speaker notes
- Expanded the speaker note with the history that makes her the talk's spine: the resistance to the
  first compiler ("computers can only do arithmetic; they cannot write programs"; "I had a running
  compiler and nobody would touch it"); the 70-year repeat of the same argument (machine code →
  assembly → FORTRAN → C → C++ → Java → Python → AI-generated code, "real programmers use the layer
  below" each time); and the irony that asm programmers now trust optimizing C compilers — same battle
  as today's AI-assisted programming. Speaker-note only; no on-screen change. Build OK. Deck = 47 slides.

### 06:20 — Slide 16 "ingredient list of doom": named the hardware
- Bullet "A modern microcontroller (Raspberry Pico / RP2040)" → "SidecarTridge Multi-device (The
  SidecarT) — RPi Pico W / RP2040". Build OK. Deck = 47 slides.

### 06:24 — Slide 16: labelled the first two ingredients
- "40-year-old hardware" → "Atari ST: 40-year-old hardware"; "68000 assembly" → "MIDI Maze: 68000
  assembly" (kept deck-consistent "MIDI Maze", no hyphen). Build OK. Deck = 47 slides.

### 06:28 — Slide 16: language-stack bullet → "68000 assembly, C and Python on top"
- "C, and Python on top" → "68000 assembly, C and Python on top". Build OK. Deck = 47 slides.
