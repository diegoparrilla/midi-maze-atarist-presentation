---
# Slidev deck config. See https://sli.dev/custom/#frontmatter-configures
theme: default
title: Too old for this sh*t — MIDI Maze over IP
info: |
  ## Too old for this sh*t
  MIDI Maze, Atari ST, Raspberry Pico, AI & other bad decisions.
  OpenSouthCode 2026 · Diego Parrilla. Built with Slidev.
transition: slide-left
mdc: true
fonts:
  sans: 'IBM Plex Sans'
  mono: 'IBM Plex Mono'
  weights: '400,500,600,700'
layout: cover
class: cover-slide
---

<div class="maze-smiley" aria-hidden="true"></div>

<div class="kicker">OpenSouthCode 2026 · Atari ST since 1987</div>

# Too old for this <span class="accent">sh*t</span>

MIDI Maze, Atari ST, Raspberry Pico, AI & other bad decisions.

<div class="byline">Diego Parrilla</div>

<!--
WINSTON: open on the PROMISE (next slide), then land the joke. Don't open cold on the joke.
Keep this slide up while people settle. ~30s.
-->

---
layout: statement
---

# By the end, you'll predict<br>where AI <span class="accent">actually</span> helps —<br>now and in the future

<!--
THE EMPOWERMENT PROMISE — say it almost verbatim:
"By the end of this talk you'll be able to look at any layer of the stack — from 68000
assembly to a Python script — and predict how much an AI can really help you there
today. And you'll have a working theory of where it helps next — where this is all
heading." This is the contract. Everything pays this off. ~45s.
-->

---
layout: two-cols
---

# I use AI to reopen<br>1980s traumas

Other people use it to be productive.

- A guy from Logroño, old enough to remember floppies the size of a truck's steering wheel
- Then COVID hit — and I went looking for when I was happiest
- Found it in an old **Atari ST**. Coded a little intro…
- …then a hardware which became **The SidecarT**, then a company: **SidecarTridge**

::right::

<!--
THE ORIGIN STORY (tell it warm, ~90s):
- I build hardware for 40-year-old computers. I created "The SidecarT" — a cartridge
  device for the Atari ST — it did surprisingly well. One device became several, and I
  ended up founding a small company, SidecarTridge. The board and logo in the collage
  are mine.
- How did I fall back into retro computing? COVID. Like a lot of people, we genuinely
  thought we might all die — so we looked back to when we were happy. For me that was my
  first computer. Pure nostalgia, and I wanted to feel it again.
- So I started coding a little demo/intro, dug out an old Atari ST to play with… and
  almost without noticing, I was soldering the first version of The SidecarT.
- Point: this whole project (and this talk) is that nostalgia, weaponised.
-->

<div class="collage">
  <div class="frame" style="--w:266px; top:12px; left:28px; --r:-2.5deg">
    <img src="/st-cartridge.jpeg" alt="Atari 520 ST with cartridge port" />
  </div>
  <div class="frame" style="--w:122px; top:40px; left:296px; --r:3.5deg">
    <img src="/sidecart-board.png" alt="SidecarTridge Pico W board" />
  </div>
  <div class="frame pixel" style="--w:124px; top:196px; left:34px; --r:-3deg">
    <img src="/diego16.png" alt="Diego at sixteen" />
  </div>
  <div class="frame" style="--w:214px; top:312px; left:178px; --r:2deg">
    <img src="/sidecart-logo.png" alt="SidecarTridge" />
  </div>
</div>

<!--
NOW the joke lands (Winston: joke second, not first). Quick self-intro, establish the
self-deprecating tone and credibility-by-age. Keep it FAST — 60s max. Don't linger.
-->

---

## This is not what you think

- <span class="accent">Not</span> a nostalgia talk
- <span class="accent">Not</span> an AI-hype talk
- It's about how **building software** changed from 1986 to 2026 — and where it goes next

<div class="mt-10 text-xl">

**Quick question:** who here has *ever* written a line of assembly?

</div>

<!--
WINSTON: build a FENCE (distinguish from the talks they expect) + ASK A QUESTION.
Actually ask. Wait ~7 seconds. Read the hands — that divide between asm-people and
not is literally the subject of the talk. Call it out.
-->

---
layout: section
---

<span class="act-num">ACT 1 · 1986</span>

# Close to the metal

<!-- Divider. The world where MIDI Maze was born. Fast. -->

---

## MIDI Maze (1987): the first FPS

The grandfather of the genre — networked deathmatch on the Atari ST, **no internet, no LAN**, years before "first-person shooter" was even a phrase. Every shooter below descends from it.

<div class="lineage">
  <div class="shot root" style="--r:-2deg">
    <img src="/midimaze-shot.jpg" alt="MIDI Maze" />
    <div class="shot__cap"><span class="shot__name">MIDI Maze</span><span class="shot__year">1987 · the ancestor</span></div>
  </div>
  <div class="shot" style="--r:1.5deg">
    <img src="/fps-wolf3d.jpg" alt="Wolfenstein 3D" />
    <div class="shot__cap"><span class="shot__name">Wolfenstein 3D</span><span class="shot__year">1992</span></div>
  </div>
  <div class="shot" style="--r:-1.5deg">
    <img src="/fps-doom.jpg" alt="Doom" />
    <div class="shot__cap"><span class="shot__name">Doom</span><span class="shot__year">1993</span></div>
  </div>
  <div class="shot" style="--r:2deg">
    <img src="/fps-quake.jpg" alt="Quake" />
    <div class="shot__cap"><span class="shot__name">Quake</span><span class="shot__year">1996</span></div>
  </div>
  <div class="shot" style="--r:-2deg">
    <img src="/fps-halflife.jpg" alt="Half-Life" />
    <div class="shot__cap"><span class="shot__name">Half-Life</span><span class="shot__year">1998</span></div>
  </div>
  <div class="shot" style="--r:1.5deg">
    <img src="/fps-halo.jpg" alt="Halo: Combat Evolved" />
    <div class="shot__cap"><span class="shot__name">Halo</span><span class="shot__year">2001</span></div>
  </div>
  <div class="shot" style="--r:-1.5deg">
    <img src="/fps-cod.jpg" alt="Call of Duty" />
    <div class="shot__cap"><span class="shot__name">Call of Duty</span><span class="shot__year">2003</span></div>
  </div>
</div>

<!--
Set up the artifact the whole talk hangs on, and give it WEIGHT: MIDI Maze (1987)
predates Wolfenstein 3D (1992) and Doom (1993) — it's the oldest ancestor of the
first-person shooter, and it already had networked multiplayer (the thing Doom became
famous for) FIVE years earlier.
- The smiley faces are the other players — that's your SYMBOL; point at the exploding
  smiley on the cover.
- Walk the lineage left → right: every name here is a household FPS, and they all trace
  back to this Atari ST game most people have never heard of.
- Covers are fair-use box art (Wikipedia) — fine for a talk; swap if you prefer.
~90s.
-->

---

## Born on the Atari ST — then everywhere

The original (1987) was **Atari ST**. It later jumped to consoles as **Faceball 2000**.

<div class="lineage">
  <div class="shot root" style="--r:-2deg">
    <img src="/hw-atarist.jpg" alt="Atari ST" />
    <div class="shot__cap"><span class="shot__name">Atari ST</span><span class="shot__year">1987 · original</span></div>
  </div>
  <div class="shot" style="--r:1.5deg">
    <img src="/hw-gameboy.png" alt="Game Boy" />
    <div class="shot__cap"><span class="shot__name">Game Boy</span><span class="shot__year">1991</span></div>
  </div>
  <div class="shot" style="--r:-1.5deg">
    <img src="/hw-snes.png" alt="Super NES" />
    <div class="shot__cap"><span class="shot__name">Super NES</span><span class="shot__year">1992</span></div>
  </div>
  <div class="shot" style="--r:2deg">
    <img src="/hw-pcengine.jpg" alt="PC Engine" />
    <div class="shot__cap"><span class="shot__name">PC Engine</span><span class="shot__year">1993</span></div>
  </div>
  <div class="shot" style="--r:-1.5deg">
    <img src="/hw-gamegear.png" alt="Game Gear" />
    <div class="shot__cap"><span class="shot__name">Game Gear</span><span class="shot__year">1993</span></div>
  </div>
</div>

<div class="ports-foot">
  Cancelled: Atari 8-bit · IBM PC · NES · Virtual Boy (<em>NikoChan Battle</em>). &nbsp;Clones: <em>MIDI-Maze II</em>, <em>iMaze</em>.
</div>

<!--
The reach point: this wasn't a niche Atari curiosity — as Faceball 2000 it shipped on
Nintendo and Sega handhelds/consoles into the 90s. But the ORIGINAL, the one with the
MIDI ring, was the Atari ST (highlighted). Note the near-misses too: it was nearly a
Virtual Boy launch-ish title (NikoChan Battle). ~45s.
-->

---

## MIDI Maze, in motion

<div class="video-embed">
  <iframe src="https://www.youtube.com/embed/8hSoy1S43dw?rel=0"
          title="MIDI Maze gameplay — Atari ST, 1987"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen></iframe>
</div>

<div class="video-cap">MIDI Maze 1 v1.0 — Xanth FX, 1987 · youtube.com/watch?v=8hSoy1S43dw</div>

<!--
Play ~30s. Point at the smiley enemies (your SYMBOL), the maze, the speed — and that this
is real 1987 footage. Then: "remember, every player you'd see here is a separate Atari ST
wired into the ring."

⚠️ Embedding YouTube needs internet at talk time. SAFER for the venue: download the clip
to public/ and swap the iframe for a local file, e.g.:
  <video controls src="/midimaze-gameplay.mp4" class="w-full"></video>
Keep a local copy as backup even if you stream.
-->

---
layout: two-cols
---

## Wait — what's an Atari ST?

For everyone who wasn't born yet:

- A 16-bit **home computer** — Atari, **1985**
- **Motorola 68000** CPU — same family as the first Macs & the Amiga
- **GEM**: a mouse-and-windows desktop, years before most homes had Windows
- **MIDI ports built in** — the musician's machine (and why this talk exists)
- A few hundred KB of RAM · floppy disks · no hard drive

<div class="mt-3 text-lg">If you're under 40, it's <span class="accent">older than you</span>.</div>

::right::

<div class="text-center mt-2">
  <img src="/hw-atarist.jpg" alt="Atari 1040 ST with monitor running GEM" style="width: 100%; background:#fff; padding:8px; border:1px solid var(--line); border-radius:6px; box-shadow:0 6px 16px rgba(0,0,0,0.16)" />
  <div class="manual-cap">Atari 1040 ST + monitor, running GEM (1985)</div>
</div>

<!--
A primer for an audience that may never have seen one. Keep it FAST and concrete: 1985
home computer, 68000 CPU (the chip in early Macs and the Amiga), a real mouse-driven GUI
(GEM) before most people had Windows, and — the detail that matters for us — MIDI IN/OUT
ports built right in, which made it the musician's machine and is the reason MIDI Maze
could network over MIDI at all. Land the "older than you" joke. ~45s.
-->

---
layout: two-cols
---

## The trick: a MIDI ring

Players chained machine-to-machine through the **MIDI ports** — each ST's OUT into the next ST's IN, all the way around.

<div class="manual-card mt-3">
  <img src="/midi-ring-photo.png" class="manual-shot" alt="The MIDI-Ring (original Atari ST manual)" />
  <div class="manual-cap">From the original Atari ST manual</div>
</div>

::right::

<svg class="ring-svg" viewBox="0 0 470 360" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="ringhead" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--accent)" />
    </marker>
  </defs>

  <!-- ring flow: each ST's MIDI OUT -> next ST's MIDI IN, clockwise -->
  <path class="ring-arrow" marker-end="url(#ringhead)" d="M296.4,74.2 A140,140 0 0 1 335.7,102.7" />
  <path class="ring-arrow" marker-end="url(#ringhead)" d="M373.6,219.5 A140,140 0 0 1 358.6,265.7" />
  <path class="ring-arrow" marker-end="url(#ringhead)" d="M259.3,337.9 A140,140 0 0 1 210.7,337.9" />
  <path class="ring-arrow" marker-end="url(#ringhead)" d="M111.4,265.7 A140,140 0 0 1 96.4,219.5" />
  <path class="ring-arrow" marker-end="url(#ringhead)" d="M134.3,102.7 A140,140 0 0 1 173.6,74.2" />

  <!-- the circulating frame -->
  <g transform="rotate(28 316 88)">
    <rect class="ring-chip" x="286" y="79" width="60" height="18" rx="9" />
    <text class="ring-chip-text" x="316" y="91" text-anchor="middle">FRAME ▸</text>
  </g>

  <!-- what travels / how fast -->
  <text class="ring-center" x="235" y="188" text-anchor="middle">
    <tspan x="235" dy="0">every player's position</tspan>
    <tspan x="235" dy="13">one lap = one game tick</tspan>
    <tspan x="235" dy="13" style="fill: var(--accent-ink)">MIDI @ 31,250 baud</tspan>
  </text>

  <!-- MASTER (top) -->
  <text class="ring-anno" x="235" y="22" text-anchor="middle">MASTER · sets the tempo</text>
  <rect class="ring-node master" x="192" y="35" width="86" height="50" rx="8" />
  <text class="ring-label" x="235" y="56" text-anchor="middle">Atari ST</text>
  <text class="ring-port" x="235" y="73" text-anchor="middle">◂ IN    OUT ▸</text>

  <rect class="ring-node" x="325.2" y="131.7" width="86" height="50" rx="8" />
  <text class="ring-label" x="368.2" y="152.7" text-anchor="middle">Atari ST</text>
  <text class="ring-port" x="368.2" y="169.7" text-anchor="middle">◂ IN    OUT ▸</text>

  <rect class="ring-node" x="274.3" y="288.3" width="86" height="50" rx="8" />
  <text class="ring-label" x="317.3" y="309.3" text-anchor="middle">Atari ST</text>
  <text class="ring-port" x="317.3" y="326.3" text-anchor="middle">◂ IN    OUT ▸</text>

  <rect class="ring-node" x="109.7" y="288.3" width="86" height="50" rx="8" />
  <text class="ring-label" x="152.7" y="309.3" text-anchor="middle">Atari ST</text>
  <text class="ring-port" x="152.7" y="326.3" text-anchor="middle">◂ IN    OUT ▸</text>

  <rect class="ring-node" x="58.8" y="131.7" width="86" height="50" rx="8" />
  <text class="ring-label" x="101.8" y="152.7" text-anchor="middle">Atari ST</text>
  <text class="ring-port" x="101.8" y="169.7" text-anchor="middle">◂ IN    OUT ▸</text>
</svg>

<div class="ring-foot">
  Raw 8-bit bytes — <strong>not music</strong>. Control values are non-standard MIDI (e.g. <code>0x00</code> = MASTER).
</div>

<!--
THE thing we are going to break. Walk it: the MASTER injects a FRAME and sets the tempo;
each ST reads the frame on its MIDI IN, stamps in its own player position, and shoves it
out its MIDI OUT to the next machine — all the way around and back to the MASTER. One full
lap = one game tick. No server, no switch: a literal cable ring at 31,250 baud.
The "raw 8-bit, non-standard bytes" detail is the seed of Act 2's "why a PC can't join". ~2 min.
-->

---

## The ST's OS — in terms you know

Same layered idea as any PC — you call *down* the stack via a `TRAP` (the ST's `syscall`). MIDI lives in **BIOS** & **XBIOS**.

<div class="archcmp">
  <div class="archcmp__head">Atari ST · 1985</div>
  <div></div>
  <div class="archcmp__head">A PC you know</div>

  <div class="acell"><span class="acell__name">Your game</span></div>
  <div class="approx">≈</div>
  <div class="acell"><span class="acell__name">Your app</span></div>

  <div class="acell"><span class="acell__name">GEM</span><div class="acell__sub">AES + VDI · windows & graphics</div></div>
  <div class="approx">≈</div>
  <div class="acell"><span class="acell__name">GUI toolkit</span><div class="acell__sub">Win32 / Qt / GTK</div></div>

  <div class="acell"><span class="acell__name">GEMDOS</span><span class="tlabel">TRAP #1</span><div class="acell__sub">files · processes · memory</div></div>
  <div class="approx">≈</div>
  <div class="acell"><span class="acell__name">OS + syscalls</span><div class="acell__sub">kernel API · libc</div></div>

  <div class="acell hot"><span class="acell__name">BIOS</span><span class="tlabel">TRAP #13</span><div class="acell__sub">device I/O — console, serial, MIDI…</div></div>
  <div class="approx">≈</div>
  <div class="acell hot"><span class="acell__name">Std device I/O</span><div class="acell__sub">kernel drivers</div></div>

  <div class="acell hot"><span class="acell__name">XBIOS</span><span class="tlabel">TRAP #14</span><div class="acell__sub">Atari-specific hardware</div></div>
  <div class="approx">≈</div>
  <div class="acell hot"><span class="acell__name">Hardware drivers</span><div class="acell__sub">vendor / HAL</div></div>
</div>

<!--
Simplified, audience-friendly mental model: the ST is layered exactly like a machine they
already know. GEM ≈ the GUI; GEMDOS (trap #1) ≈ the OS/syscalls; BIOS (trap #13) ≈ low-level
device I/O; XBIOS (trap #14) ≈ hardware drivers. The one thing to remember: a program asks
the OS for things by firing a 68000 TRAP — the ST's "syscall". MIDI lives down in BIOS &
XBIOS (highlighted) — and the exact calls are on the next slide. ~60s.
-->

---

## Send one MIDI byte — ST vs PC

<div class="grid grid-cols-2 gap-6 mt-2">
<div>

**Atari ST** · 68000 — *raw bytes*

```asm
* Bconout: send one byte (BIOS, dev 3)
  move.w  d1,-(sp)   ; the byte (even 0x00)
  move.w  #3,-(sp)   ; dev 3 = MIDI
  move.w  #3,-(sp)   ; fn 3 = Bconout
  trap    #13
* read: Bconin (#2) · buffer: Midiws (#14)
```

On the ST, MIDI is pure **serial** — a `MIDI IN` and a `MIDI OUT` socket at **31,250 baud**. Any byte goes.

</div>
<div>

**Modern PC** · C / WINMM — *MIDI messages*

```c
HMIDIOUT h;
midiOutOpen(&h, 0, 0, 0, 0);
// you send packed MESSAGES, not bytes:
midiOutShortMsg(h, 0x007F3C90); // note-on
// a bare 0x00 byte? no call for it —
// WINMM drops anything that isn't valid MIDI
```

</div>
</div>

<div class="mt-2 text-center" style="font-size: 0.82rem; color: var(--ink-soft)">
Same wire, different abstraction: the ST hands you raw bytes; the PC only speaks valid MIDI messages.
</div>

<div class="bigidea">
  <span class="spark">💡 THE GOOD IDEA</span>
  <strong>Hijack the MIDI IN/OUT at the BIOS &amp; XBIOS level</strong> and redirect it to a <strong>network stack</strong> — through the <strong>SidecarT</strong> hardware + firmware.
</div>

<!--
The crux, as a side-by-side. LEFT (ST): MIDI is BIOS device 3, a dumb serial line — Bconout
(trap #13) pushes any byte, including 0x00 (the MASTER marker). RIGHT (PC): the OS exposes
MIDI as a message API — Win32 WINMM. midiOutShortMsg takes a packed DWORD message (status +
2 data bytes), not raw bytes; there's literally no call for "emit one raw 0x00" (midiOutLongMsg
only takes a valid SysEx F0..F7), and WINMM filters non-standard data. So the identical-looking task is trivial on the ST and impossible through the PC's MIDI
stack — which is exactly why we needed the SidecarT to speak raw. ~75s.
-->

---
layout: statement
---

# In 2026, people still<br>play it competitively

<!--
Surprise beat. Championships at retro meetups, 40 years on. This is WHY it's worth
reviving over the network — there's a living community. Short, ~30s.
-->

---
layout: statement
---

# Let's break the ring<br>and rebuild it over <span class="accent">TCP/IP</span>

<!--
THE BAD IDEA. Say it sounded great in your head. Beat. This is the project thesis and
the comedic engine ("what could go wrong"). ~30s.
-->

---

## The ingredient list of doom

- 40-year-old hardware
- 68000 assembly
- A modern microcontroller (Raspberry Pico / RP2040)
- C, and Python on top
- Codex, Claude Code, Copilot, NotebookLM
- One señor from Logroño

<div class="mt-8 text-2xl">Spoiler: <span class="accent">everything</span> went wrong.</div>

<!--
The cast of the disaster. Land "Spoiler: everything went wrong" as a button. This list
also previews the abstraction ladder we'll climb. ~60s.
-->

---

## The AI cast

- **OpenAI · Codex / ChatGPT 5.4 & 5.5** — Codex optimised the microfirmware & **TPROTOCOL** (C + 68000); ChatGPT researched & designed the solution and architecture
- **Anthropic · Claude Code 5.7 & 5.8** — solution coding… and this presentation ;-)
- **GitHub Copilot** — code reviews
- **Google NotebookLM** — the librarian: Atari reference books + the MIDI-Maze-to-PC reverse-engineering TFG by **Jesús Ángel González Gorrado**

<!--
Introduce the AI tools as recurring CHARACTERS — we pay them off as the three "personalities"
in Act 3. Roles: Codex for low-level optimisation (firmware/TPROTOCOL, C & 68000); ChatGPT
for research + architecture design; Claude Code for the solution code (and this deck);
Copilot for reviews; NotebookLM as the source-grounded librarian over the Atari books and
the UNIZAR TFG (reverse-engineering MIDI Maze for PC) by Jesús Ángel González Gorrado. ~75s.
-->

---

## The abstraction ladder

One project, four levels — from the big picture down to the metal. We'll climb all of them.

<div class="ladder">
  <div class="rung"><span class="rung__name">Research</span> architecting the solution</div>
  <div class="rung"><span class="rung__name">Python</span> high-level glue</div>
  <div class="rung"><span class="rung__name">C</span> firmware</div>
  <div class="rung"><span class="rung__name">68000 asm</span> the metal</div>
</div>

<div class="mt-6 text-lg">Keep an eye on each rung — later we'll ask how the <span class="accent">AI</span> did at each one.</div>

<!--
EVOLVING LADDER — appearance #1 (the map). Just the four levels we work at, top (Research /
architecture) down to the metal (68000 asm). NO verdicts yet — how AI performed at each
rung is the Act 3 "surprise" payoff (slide reuses this exact ladder, now graded). This also
sets up the "Rung" language used across Act 2. ~30s.
-->

---

## Architecting the solution — ChatGPT 5.4/5.5 "Research mode"

<div class="flex gap-8 items-start mt-2">
<div class="flex-1">

- Asked it to **draft an architecture** for MIDI Maze over TCP/IP on the Atari ST
- Stubbornly proposed a **physical-layer** box — translating MIDI ⇄ TCP/IP by **wiring into the MIDI ports**
- Told it to use **The SidecarT** → it *still* wired the SidecarT to the **MIDI ports**! **WTF?!?!**
- Told it: SidecarT **+ a custom firmware to trap MIDI** → still doesn't get it, and **over-engineers**

</div>
<div class="text-center" style="flex:none">
  <img src="/qr-chatgpt-research.svg" alt="QR — the ChatGPT research" style="width:170px; background:#fff; padding:10px; border:1px solid var(--line); border-radius:8px" />
  <div class="manual-cap">Read the research →</div>
</div>
</div>

<div class="diag">
  <span class="diag__tag">WHY — IT'S CALLED "ANCHORING"</span>
  It locks onto its first draft and only <strong>edits</strong> it (local search) — it never re-derives from scratch. So your hints get <strong>grafted on</strong>, not absorbed, and the bloat survives. It optimises for coverage &amp; robustness, not simplicity → <strong>correct, but operationally absurd</strong>.
</div>

<div class="bigidea" style="margin-top:0.6rem">
  <span class="spark">💡 THE LESSON</span>
  Too complex for a good solution out of the box — <strong>we must guide the research.</strong>
</div>

<!--
The "Research mode" reality check. ChatGPT 5.4/5.5 in research mode kept missing the point
when asked to architect MIDI Maze over IP: it insisted on a physical-layer device wired into
the MIDI DIN ports; even when told to use the SidecarT it wired the SidecarT to the MIDI
ports; and when told to trap MIDI in firmware it over-engineered. QR links to the full shared
research session.
WHY (the diagnosis box): the behaviour is closest to ANCHORING — the model treats its first
architecture as established fact (it's now part of the context) and does LOCAL search: edit
the existing design rather than re-derive it from the requirements + new insights. Related
framings: belief/solution persistence ("you're right, the bus is unnecessary… we'll keep the
bus but simplify it"); context inertia / trajectory dependence (20 pages of discussion exert
a pull); hysteresis (output depends on conversation history, not just final requirements). It
happens because consistency with prior text is heavily rewarded in training while discarding
work is not — and because it optimises for completeness/coverage/robustness rather than the
expert's criteria (simplicity, operational cost, coupling, failure modes, maintainability).
Net: technically correct, operationally absurd (Kafka+CQRS+Event-Sourcing+Saga… for 500 users).
NOTE: this is a great laugh and a real datapoint — but it sits in tension with the ladder's
"Research = brilliant" verdict; decide whether to downgrade that rung. ~90s.
-->

---

## Technically correct. Operationally absurd.

<div class="oe-need">Asked for the <strong>simplest</strong> v1 to run MIDI Maze over LAN, ChatGPT's real proposal was…</div>

<div class="oechips">
  <span class="oechip">16× custom MIDI daughterboards</span><span class="oearr">→</span>
  <span class="oechip">6N138 opto-isolators</span><span class="oearr">→</span>
  <span class="oechip">5 V level-shifters</span><span class="oearr">→</span>
  <span class="oechip">dedicated 2.4 GHz router</span><span class="oearr">→</span>
  <span class="oechip">central Linux ring server</span><span class="oearr">→</span>
  <span class="oechip">framed TCP + CRC32</span><span class="oearr">→</span>
  <span class="oechip">heartbeats + telemetry</span><span class="oearr">→</span>
  <span class="oechip">Atari TSR + command catalog</span><span class="oearr">→</span>
  <span class="oechip">3-month Gantt + 16× BOM</span>
</div>

<div class="oe-need">…to forward bytes the SidecarT <strong>already carries over its cartridge port</strong> — in pure firmware, zero new hardware.</div>

<div class="oe-punch"><span class="ok">Nothing is wrong.</span> &nbsp; <span class="bad">Everything is unnecessary.</span></div>

<div class="bigidea" style="margin-top:0.7rem">
  <span class="spark">THE ILLUSION</span>
  It <strong>looks</strong> like senior-architect brilliance — but that competence is an <strong>illusion</strong>. Only a human expert spots the over-engineering. Research-grade AI still needs <strong>expert verification</strong>.
</div>

<!--
THE PAYOFF to the anchoring slide — and the slide that resolves the ladder tension. This is the
REAL "deep research" output ChatGPT gave when asked for the SIMPLEST v1 to run original MIDI Maze
over a LAN: keep the physical MIDI ports and BUILD HARDWARE — 16 custom opto-isolated MIDI
daughterboards (6N138, 5 V level-shifters, 220R loops) soldered to the SidecarT debug UART — plus
a dedicated 2.4 GHz AP, a central Linux "ring server", a framed-TCP protocol with CRC16/CRC32
headers + sequence numbers, heartbeats/telemetry, an Atari TSR with a full command catalog, jitter
buffers, a validation matrix and a 3-month Gantt chart with a 16× bill of materials. Every piece is
individually defensible; the whole is absurd — because the SidecarT ALREADY carries the bytes over
its cartridge port in firmware, so the shipped solution needed zero new hardware. "Nothing is wrong.
Everything is unnecessary." THE BIG POINT: at the Research/architecture rung the AI LOOKS the most
competent — and that's the trap. The competence is an illusion that holds up only until an expert
reviews it; the higher the abstraction, the MORE human verification matters. Pays off in "knowing
when it's wrong / what not to build". ~75s.
-->

---
layout: statement
---

<div class="kicker">A quick confession 🙋</div>

# I'm too old to solder<br><span class="accent">16 daughterboards</span><br>because a chatbot told me to.

<div class="mt-8 text-2xl">
  Show of hands — who here has already survived a<br><strong>"technically correct, operationally absurd"</strong> masterpiece?
</div>

<!--
THE AUDIENCE MOMENT — callback to the motto ("Too old for this sh*t") and to the 16-daughterboard
proposal we just saw. Deliver the confession line dry, let it breathe, THEN ask the show-of-hands
question and actually wait for hands. This is the room-bonding beat: every experienced engineer has
inherited a cathedral that should've been a shed. Land the shared pain, maybe grab one quick war
story from the audience, then pivot: the thing that saved us from theirs (and from ChatGPT's) is
the same — experience, taste, knowing what NOT to build. That's the human edge the rest of the talk
is about. Keep it loose; this is breathing room before we climb back down the rungs. ~60-90s.
-->

---
layout: fact
---

# Our turn.

We guide it ourselves — one rung at a time. <span style="opacity:0.6">(the metal's still down there; we'll be back.)</span>

<!--
WINSTON landmark + pivot. Bridges the lesson from the over-engineering beat ("we must guide the
research; the AI won't simplify on its own") straight into ACT 2's hands-on build. "Our turn" =
we stop asking the chatbot for a cathedral and start building the shed ourselves, climbing the
ladder rung by rung. The parenthetical teases the rung climb (68000 / C / Python) coming up.
Anyone who drifted during the AI detour can rejoin here. ~15s.
-->

---
layout: section
---

<span class="act-num">ACT 2 · 2026</span>

# Faking the MIDI ring

<div class="recap">Make every ST believe the cable ring is still there.</div>

<!-- Divider + recap. Act 2 = the plan + the build: introduce the SidecarT and the
"ring orchestrator" goal BEFORE the architecture, then climb the rungs. -->

---
layout: two-cols
---

## Meet the SidecarT

Not a "ROM emulator" — a tool to **enhance** the ST. A bizarre **coprocessor** (here: our network bridge).

- **Cartridge port** · **RP2040** (Pi Pico-class) + **Wi-Fi**
- Custom **microfirmware**; ST ↔ board over **TPROTOCOL**
- **2,200+** built · ~200–400 clones in the wild
- Open source: **firmware GPL** · **hardware CC** (non-commercial)

::right::

<div class="text-center mt-2">
  <img src="/sidecart-board.png" alt="SidecarT board" style="width: 230px; background:#fff; padding:8px; border:1px solid var(--line); border-radius:6px; box-shadow:0 6px 16px rgba(0,0,0,0.16)" />
  <div class="manual-cap">SidecarT · RP2040 + Wi-Fi</div>
</div>

<!--
Introduce the device BEFORE the architecture. THE FRAME: people call it a "ROM emulator",
but it's really a developer tool that bolts a modern brain onto the ST — a bizarre
coprocessor. It's a cartridge with an RP2040 + Wi-Fi; the ST can't write to the cartridge
(read-only bus), so the two talk over TPROTOCOL via ROM reads. Credibility: 2,200+ units
built and ~200–400 clones — a real, shipping product, not a breadboard. And it's open: GPL
firmware, CC (non-commercial) hardware — worth saying out loud to an open-source crowd.
Today we repurpose it as the MIDI-to-network bridge. ~60s.
-->

---

## The plan: one virtual ring

Each **ST + SidecarT** is a node; a **TCP/IP "ring orchestrator"** passes the frame around — a *virtual* ring.

<svg class="goal-svg" viewBox="0 0 740 350" xmlns="http://www.w3.org/2000/svg">
  <!-- real TCP/IP connections (spokes to the orchestrator) -->
  <line class="spoke" x1="370" y1="175" x2="370" y2="50" />
  <line class="spoke" x1="370" y1="175" x2="620" y2="175" />
  <line class="spoke" x1="370" y1="175" x2="370" y2="300" />
  <line class="spoke" x1="370" y1="175" x2="120" y2="175" />

  <!-- the virtual MIDI ring (logical) -->
  <ellipse class="vring" cx="370" cy="175" rx="250" ry="125" />

  <!-- nodes -->
  <rect class="dev" x="295" y="25" width="150" height="50" rx="8" />
  <text class="dev-title" x="370" y="47" text-anchor="middle">Atari ST</text>
  <text class="note-t" x="370" y="63" text-anchor="middle" style="fill: var(--accent-ink)">+ SidecarT</text>

  <rect class="dev" x="545" y="150" width="150" height="50" rx="8" />
  <text class="dev-title" x="620" y="172" text-anchor="middle">Atari ST</text>
  <text class="note-t" x="620" y="188" text-anchor="middle" style="fill: var(--accent-ink)">+ SidecarT</text>

  <rect class="dev" x="295" y="275" width="150" height="50" rx="8" />
  <text class="dev-title" x="370" y="297" text-anchor="middle">Atari ST</text>
  <text class="note-t" x="370" y="313" text-anchor="middle" style="fill: var(--accent-ink)">+ SidecarT</text>

  <rect class="dev" x="45" y="150" width="150" height="50" rx="8" />
  <text class="dev-title" x="120" y="172" text-anchor="middle">Atari ST</text>
  <text class="note-t" x="120" y="188" text-anchor="middle" style="fill: var(--accent-ink)">+ SidecarT</text>

  <!-- ring orchestrator -->
  <rect class="srv" x="290" y="143" width="160" height="64" rx="8" />
  <text class="srv-t" x="370" y="170" text-anchor="middle">Ring Orchestrator</text>
  <text class="srv-s" x="370" y="187" text-anchor="middle">TCP/IP · Python</text>
</svg>

<div class="text-center" style="font-size: 0.82rem; color: var(--ink-soft)">
  <span style="color: var(--accent)">┄ virtual ring (logical)</span> &nbsp;·&nbsp; — real TCP/IP, every node to the orchestrator
</div>

<div class="text-center mt-1" style="font-size: 0.95rem">
  To each ST it must look <strong>exactly</strong> like 1987 — same bytes, same order. We just move the wire to the Internet.
</div>

<!--
The GOAL, stated before the detailed design. Physically it's a STAR (every SidecarT
connects to one TCP/IP server, the "ring orchestrator"); logically it's the same RING as
1987 — the orchestrator passes each frame node-to-node in ring order. The hard constraint:
MIDI Maze and the ST stay 100% unmodified; to them it must be byte-for-byte the old cable
ring. Next slide: how the pieces actually fit together. ~75s.
-->

---

## The Candidate Architecture

<svg class="arch2-svg" viewBox="0 -56 910 291" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="ahDark2" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--ink)" />
    </marker>
    <marker id="ahAcc2" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--accent)" />
    </marker>
    <marker id="ahTeal2" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--link)" />
    </marker>
  </defs>

  <!-- the virtual ring: the two ends are joined in software -->
  <path class="ring-arc" v-click="4" marker-start="url(#ahAcc2)" marker-end="url(#ahAcc2)" d="M95,60 Q450,-104 805,60" />
  <text class="ring-arc-lbl" v-click="4" x="450" y="2" text-anchor="middle">one virtual MIDI ring — the ends are joined in software</text>

  <!-- inter-device links (bidirectional) -->
  <line class="flow2"     marker-start="url(#ahDark2)" marker-end="url(#ahDark2)" x1="170" y1="140" x2="215" y2="140" />
  <line class="flow2 net" marker-start="url(#ahAcc2)"  marker-end="url(#ahAcc2)"  x1="355" y1="140" x2="395" y2="140" />
  <line class="flow2 net" marker-start="url(#ahAcc2)"  marker-end="url(#ahAcc2)"  x1="505" y1="140" x2="545" y2="140" />
  <line class="flow2"     marker-start="url(#ahDark2)" marker-end="url(#ahDark2)" x1="685" y1="140" x2="730" y2="140" />
  <text class="flow2-lbl" x="192" y="131" text-anchor="middle">cartridge</text>
  <text class="flow2-lbl" x="375" y="131" text-anchor="middle">TCP/IP</text>
  <text class="flow2-lbl" x="525" y="131" text-anchor="middle">TCP/IP</text>
  <text class="flow2-lbl" x="707" y="131" text-anchor="middle">cartridge</text>

  <!-- Atari ST (left) -->
  <rect class="dev"    x="20" y="62" width="150" height="157" rx="8" />
  <rect class="dev-hd" x="20" y="62" width="150" height="24" rx="8" />
  <text class="dev-title" x="95" y="79" text-anchor="middle">Atari ST · 68000</text>
  <rect class="layer" x="44" y="92"  width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="109" text-anchor="middle">MIDI Maze</text>
  <rect class="layer" x="44" y="122" width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="139" text-anchor="middle">GEM</text>
  <rect class="layer" x="44" y="152" width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="169" text-anchor="middle">BIOS / XBIOS</text>
  <rect class="layer hook" x="44" y="182" width="102" height="26" rx="4" />
  <text class="layer-t accent" x="95" y="199" text-anchor="middle">XBRA hook</text>
  <line class="flow-in" v-click="3" marker-end="url(#ahTeal2)" x1="32"  y1="212" x2="32"  y2="90" />
  <line class="flow-out" v-click="1" marker-end="url(#ahAcc2)"  x1="158" y1="90"  x2="158" y2="212" />

  <!-- SidecarT (left) -->
  <rect class="dev"    x="215" y="62" width="140" height="157" rx="8" />
  <rect class="dev-hd" x="215" y="62" width="140" height="24" rx="8" />
  <text class="dev-title" x="285" y="79" text-anchor="middle">SidecarT · RP2040</text>
  <rect class="layer" x="238" y="92"  width="94" height="26" rx="4" />
  <text class="layer-t" x="285" y="109" text-anchor="middle">microfirmware</text>
  <rect class="layer bridge" x="238" y="122" width="94" height="26" rx="4" />
  <text class="layer-t accent" x="285" y="139" text-anchor="middle">TPROTO ⇄ TCP/IP</text>
  <rect class="layer" x="238" y="152" width="94" height="26" rx="4" />
  <text class="layer-t" x="285" y="169" text-anchor="middle">Wi-Fi / TCP/IP</text>
  <text class="note-t" x="285" y="200" text-anchor="middle">MIDI kept intact</text>
  <line class="flow-in" v-click="3" marker-end="url(#ahTeal2)" x1="226" y1="212" x2="226" y2="90" />
  <line class="flow-out" v-click="1" marker-end="url(#ahAcc2)"  x1="344" y1="90"  x2="344" y2="212" />

  <!-- routing server (Python) -->
  <rect class="srv" x="395" y="92" width="110" height="117" rx="8" />
  <text class="srv-t" x="450" y="114" text-anchor="middle">Orchestrator</text>
  <text class="srv-s" x="450" y="131" text-anchor="middle" style="fill: var(--accent-ink)">TCP/IP · Python</text>
  <text class="srv-s" v-click="2" x="450" y="159" text-anchor="middle">routes the ring</text>
  <text class="srv-s" v-click="2" x="450" y="172" text-anchor="middle">node → node</text>

  <!-- SidecarT (right): identical stack -->
  <rect class="dev"    x="545" y="62" width="140" height="157" rx="8" />
  <rect class="dev-hd" x="545" y="62" width="140" height="24" rx="8" />
  <text class="dev-title" x="615" y="79" text-anchor="middle">SidecarT · RP2040</text>
  <rect class="layer" x="568" y="92"  width="94" height="26" rx="4" />
  <text class="layer-t" x="615" y="109" text-anchor="middle">microfirmware</text>
  <rect class="layer bridge" x="568" y="122" width="94" height="26" rx="4" />
  <text class="layer-t accent" x="615" y="139" text-anchor="middle">TPROTO ⇄ TCP/IP</text>
  <rect class="layer" x="568" y="152" width="94" height="26" rx="4" />
  <text class="layer-t" x="615" y="169" text-anchor="middle">Wi-Fi / TCP/IP</text>
  <text class="note-t" x="615" y="200" text-anchor="middle">MIDI kept intact</text>
  <line class="flow-in" v-click="3" marker-end="url(#ahTeal2)" x1="556" y1="90" x2="556" y2="212" />
  <line class="flow-out" v-click="1" marker-end="url(#ahAcc2)"  x1="674" y1="212"  x2="674" y2="90" />

  <!-- Atari ST (right): identical stack -->
  <rect class="dev"    x="730" y="62" width="150" height="157" rx="8" />
  <rect class="dev-hd" x="730" y="62" width="150" height="24" rx="8" />
  <text class="dev-title" x="805" y="79" text-anchor="middle">Atari ST · 68000</text>
  <rect class="layer" x="754" y="92"  width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="109" text-anchor="middle">MIDI Maze</text>
  <rect class="layer" x="754" y="122" width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="139" text-anchor="middle">GEM</text>
  <rect class="layer" x="754" y="152" width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="169" text-anchor="middle">BIOS / XBIOS</text>
  <rect class="layer hook" x="754" y="182" width="102" height="26" rx="4" />
  <text class="layer-t accent" x="805" y="199" text-anchor="middle">XBRA hook</text>
  <line class="flow-in" v-click="3" marker-end="url(#ahTeal2)" x1="742" y1="90" x2="742" y2="212" />
  <line class="flow-out" v-click="1" marker-end="url(#ahAcc2)"  x1="868" y1="212"  x2="868" y2="90" />
</svg>

<div class="text-center" style="font-size: 0.8rem; margin-top: 0.2rem">
  <span style="color: var(--accent); font-weight: 700">■ your moves out</span>
  &nbsp;·&nbsp;
  <span style="color: var(--link); font-weight: 700">■ others' moves in</span>
  &nbsp;—&nbsp; each packet goes <strong>down to wrap</strong> (toward the wire), then <strong>up to unwrap</strong> (into the game)
</div>

<div class="text-center mt-1" style="font-size: 0.9rem">
  The <strong>MIDI bytes are never touched</strong> — only the envelope changes:
  <code>TPROTOCOL⟨MIDI⟩</code> across the cartridge port, <code>TCP/IP⟨MIDI⟩</code> across the network.
</div>

<!--
THE diagram that makes the project click. Walk it left → right ONCE:
1. MIDI Maze calls BIOS/XBIOS to push MIDI bytes; an XBRA hook traps those calls and
   redirects them — instead of the MIDI port, they go out the cartridge port.
2. Over the cartridge they ride inside TPROTOCOL. The SidecarT (RP2040) microfirmware
   unwraps TPROTOCOL, leaves the MIDI bytes untouched, and re-wraps them in TCP/IP.
3. The TCP/IP server is the matchmaker: every SidecarT connects to it; it routes each
   packet to the right destination SidecarT.
4. At the far end the inverse happens — TCP/IP → TPROTOCOL → cartridge → XBRA hook →
   MIDI Maze. Neither ST ever knows the ring became the Internet.
KEY LINE: the MIDI payload never changes; only the envelope around it does.
Every Atari ST and every SidecarT runs the SAME stack (it's an architecture diagram, not
a sequence diagram). The dashed arc up top is the point: all the nodes together form ONE
virtual MIDI ring — the cable loop of 1987, closed in software. The matchmaker/router in
the middle is a Python TCP/IP server. ~2.5 min.
-->

---
layout: two-cols
---

## Rung: 68000 assembly (the ST)

The ST side is the **XBRA hook** — `XBRA` is the standard Atari protocol to chain a system vector without stepping on anyone else.

- MIDI Maze reaches MIDI two ways, so we trap **both**: **BIOS `#13`** (`Bconin/out/stat`) *and* **XBIOS `#14`** (`Midiws`, MIDI-IN).
- Each hook is XBRA-chained: `'XBRA'` magic · our cookie · pointer to the previous handler.
- **MIDI? → SidecarT.** Anything else → straight to the original ROM handler.
- MIDI Maze never notices — it still just calls BIOS / XBIOS.

::right::

```asm
* install on BOTH MIDI vectors (XBRA-chained)
  Setexc 13,hook_bios   ; trap #13  BIOS
  Setexc 14,hook_xbios  ; trap #14  XBIOS

hook_bios:  cmp.w #3,8(sp)     ; device 3 = MIDI?
            beq   to_sidecart  ;  yes -> cartridge
            jmp   (oldp_b)     ;  no  -> real BIOS

hook_xbios: cmp.w #12,8(sp)    ; Midiws (MIDI out)?
            beq   to_sidecart
            jmp   (oldp_x)     ;  else -> real XBIOS
```

<!--
The mechanism that makes the whole project possible. XBRA ("eXternal BRanch Array") is the
community-standard way to cooperatively hook a 68000 system vector on the ST: just before
your handler you place 3 longwords — the magic 'XBRA', a 4-char cookie identifying you, and
'oldp' = the handler you displaced. Install with Setexc (XBIOS): save the old vector as oldp,
point the vector at your handler; the cookie + oldp let the chain be walked and removed later.
KEY: MIDI Maze reaches the MIDI port through BOTH layers, so we hook BOTH vectors —
trap #13 (BIOS: Bconin/Bconout/Bconstat on device 3) AND trap #14 (XBIOS: Midiws, and the
MIDI-IN read used for MASTER detection). Each handler checks if the call is MIDI; if so we
ship the bytes out the cartridge to the SidecarT (TPROTOCOL); if not, jmp to oldp so the
rest of the OS is untouched. Net effect: MIDI Maze, completely unmodified, thinks it's still
talking to its MIDI port. (Stack offsets are illustrative — the real ones account for the
trap frame.) ~2 min.
-->

---
layout: two-cols
---

## Rung: C (the Pico)

- MIDI Maze is **lock-step**: every byte **out** is answered by a byte **in** — that's the game's clock
- So, first assumption: relay it **byte-by-byte, in order, with a handshake** — *exactly* like the cable
- Read-only cartridge → emulate ROM, snoop **ROM3** reads via **PIO + DMA**
- Carried over **TPROTOCOL** — the SidecarT's command channel, built for **synchronous** multi-KB buffers & commands → lots of **plumbing**
- **lwIP** TCP up to the orchestrator · RP2040 @ **225 MHz**

::right::

<div class="mt-4" style="background:#fff; padding:8px; border:1px solid var(--line); border-radius:6px; box-shadow:0 6px 16px rgba(0,0,0,0.16)">
  <img src="/sidecart-st-photo.jpg" alt="SidecarT board beside the Atari ST" style="display:block; width:100%; border-radius:3px" />
</div>
<div class="manual-cap">The SidecarT (RP2040) and the Atari ST</div>

<!--
FIRST ASSUMPTION ONLY — no spoilers here. MIDI Maze is genuinely lock-step (constraint
C-01): every MIDI OUT byte is answered by a synchronous IN readback, and that lock-step IS
the frame clock. So the faithful first assumption was: relay each byte across the bridge,
in order, with a confirm/ack handshake — reproduce the cable exactly. Mechanism (the
candidate build): read-only cartridge, so the Pico emulates ROM and snoops ROM3 reads via
a PIO+DMA ring; the exchange rides TPROTOCOL — the SidecarT's command channel, designed for
synchronous multi-KB buffer transfers and commands, so each byte drags a lot of plumbing;
lwIP TCP to the orchestrator; ~4,800 lines of C + PIO.
DO NOT reveal here that this per-byte handshake turned out 3× too slow — that collision and
the streaming fix are the "Reality bites → The Final Architecture" turn at the end of Act 2. ~75s.
-->

---

## Rung: Python (the glue)

- The **ring orchestrator** — a Python **asyncio** TCP server wiring every node into a ring
- First version is **smart**: master election, flow-control, match coordination
- Plus **self-test harnesses** & packet inspection — write fast, throw away fast
- The layer **furthest from the metal**

<!--
Rung 3 — first-version Python only (from md-MIDI2IP). The orchestrator (orchestrator.py,
asyncio TCP server) accepts every node and wires them into a ring; in this first version
it's the "smart" one — master election, flow-control, match coordination. Plus selftest
harnesses & packet inspection. Furthest from the metal — the setup for the Act 3 payoff.
NOTE: don't mention Hatari / the Hatari gateway here — it's introduced LATER to justify v2.
And don't reveal that the orchestrator is later gutted to a dumb relay — that's the reveal. ~60s.
-->

---

## "MIDI-ring booh-booh"

First real test — a single Atari ST + SidecarT. The candidate just… won't ring.

- The ST doesn't reliably become **MASTER**
- The game **never starts**
- …and sometimes it greets us with this:

<div style="text-align:center; margin-top:0.6rem">
  <span style="font-family:var(--slidev-font-mono); font-weight:700; color:#d23f57; border:2px solid #d23f57; background:color-mix(in srgb,#d23f57 8%,#fff); border-radius:6px; padding:0.55rem 1.3rem; font-size:1.4rem; display:inline-block">⚠ MIDI-ring booh-booh</span>
</div>

<div class="bigidea" style="margin-top:0.9rem">
  <span class="spark">💡 THE FIX</span>
  Add another computer to the ring — one we <strong>know works</strong>.
</div>

<!--
THE BUG that motivates V1++. With a single real ST, the candidate can't form a ring: the
node doesn't reliably win MASTER, the game never starts, and MIDI Maze sometimes prints its
own error — literally "MIDI-ring booh-booh". A ring needs more than one believable node. So
we add a peer we KNOW is correct — next slide: Hatari via the gateway. ~45s.
-->

---

## The Candidate Architecture V1++

<svg class="arch2-svg" style="max-width:860px" viewBox="0 -56 910 404" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="ahDark3" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--ink)" />
    </marker>
    <marker id="ahAcc3" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--accent)" />
    </marker>
    <marker id="ahTeal3" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--link)" />
    </marker>
  </defs>

  <path class="ring-arc" marker-start="url(#ahAcc3)" marker-end="url(#ahAcc3)" d="M95,60 Q450,-104 805,60" />
  <text class="ring-arc-lbl" x="450" y="2" text-anchor="middle">one virtual MIDI ring — the ends are joined in software</text>

  <line class="flow2"     marker-start="url(#ahDark3)" marker-end="url(#ahDark3)" x1="170" y1="140" x2="215" y2="140" />
  <line class="flow2 net" marker-start="url(#ahAcc3)"  marker-end="url(#ahAcc3)"  x1="355" y1="140" x2="395" y2="140" />
  <line class="flow2 net" marker-start="url(#ahAcc3)"  marker-end="url(#ahAcc3)"  x1="505" y1="140" x2="545" y2="140" />
  <line class="flow2"     marker-start="url(#ahDark3)" marker-end="url(#ahDark3)" x1="685" y1="140" x2="730" y2="140" />
  <text class="flow2-lbl" x="192" y="131" text-anchor="middle">cartridge</text>
  <text class="flow2-lbl" x="375" y="131" text-anchor="middle">TCP/IP</text>
  <text class="flow2-lbl" x="525" y="131" text-anchor="middle">TCP/IP</text>
  <text class="flow2-lbl" x="707" y="131" text-anchor="middle">cartridge</text>

  <!-- Atari ST (left) -->
  <rect class="dev"    x="20" y="62" width="150" height="157" rx="8" />
  <rect class="dev-hd" x="20" y="62" width="150" height="24" rx="8" />
  <text class="dev-title" x="95" y="79" text-anchor="middle">Atari ST · 68000</text>
  <rect class="layer" x="44" y="92"  width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="109" text-anchor="middle">MIDI Maze</text>
  <rect class="layer" x="44" y="122" width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="139" text-anchor="middle">GEM</text>
  <rect class="layer" x="44" y="152" width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="169" text-anchor="middle">BIOS / XBIOS</text>
  <rect class="layer hook" x="44" y="182" width="102" height="26" rx="4" />
  <text class="layer-t accent" x="95" y="199" text-anchor="middle">XBRA hook</text>
  <line class="flow-in" marker-end="url(#ahTeal3)" x1="32"  y1="212" x2="32"  y2="90" />
  <line class="flow-out" marker-end="url(#ahAcc3)"  x1="158" y1="90"  x2="158" y2="212" />

  <!-- SidecarT (left) -->
  <rect class="dev"    x="215" y="62" width="140" height="157" rx="8" />
  <rect class="dev-hd" x="215" y="62" width="140" height="24" rx="8" />
  <text class="dev-title" x="285" y="79" text-anchor="middle">SidecarT · RP2040</text>
  <rect class="layer" x="238" y="92"  width="94" height="26" rx="4" />
  <text class="layer-t" x="285" y="109" text-anchor="middle">microfirmware</text>
  <rect class="layer bridge" x="238" y="122" width="94" height="26" rx="4" />
  <text class="layer-t accent" x="285" y="139" text-anchor="middle">TPROTO ⇄ TCP/IP</text>
  <rect class="layer" x="238" y="152" width="94" height="26" rx="4" />
  <text class="layer-t" x="285" y="169" text-anchor="middle">Wi-Fi / TCP/IP</text>
  <text class="note-t" x="285" y="200" text-anchor="middle">MIDI kept intact</text>
  <line class="flow-in" marker-end="url(#ahTeal3)" x1="226" y1="212" x2="226" y2="90" />
  <line class="flow-out" marker-end="url(#ahAcc3)"  x1="344" y1="90"  x2="344" y2="212" />

  <!-- orchestrator -->
  <rect class="srv" x="395" y="92" width="110" height="117" rx="8" />
  <text class="srv-t" x="450" y="114" text-anchor="middle">Orchestrator</text>
  <text class="srv-s" x="450" y="131" text-anchor="middle" style="fill: var(--accent-ink)">TCP/IP · Python</text>
  <text class="srv-s" x="450" y="159" text-anchor="middle">routes the ring</text>
  <text class="srv-s" x="450" y="172" text-anchor="middle">node → node</text>

  <!-- SidecarT (right) -->
  <rect class="dev"    x="545" y="62" width="140" height="157" rx="8" />
  <rect class="dev-hd" x="545" y="62" width="140" height="24" rx="8" />
  <text class="dev-title" x="615" y="79" text-anchor="middle">SidecarT · RP2040</text>
  <rect class="layer" x="568" y="92"  width="94" height="26" rx="4" />
  <text class="layer-t" x="615" y="109" text-anchor="middle">microfirmware</text>
  <rect class="layer bridge" x="568" y="122" width="94" height="26" rx="4" />
  <text class="layer-t accent" x="615" y="139" text-anchor="middle">TPROTO ⇄ TCP/IP</text>
  <rect class="layer" x="568" y="152" width="94" height="26" rx="4" />
  <text class="layer-t" x="615" y="169" text-anchor="middle">Wi-Fi / TCP/IP</text>
  <text class="note-t" x="615" y="200" text-anchor="middle">MIDI kept intact</text>
  <line class="flow-in" marker-end="url(#ahTeal3)" x1="556" y1="90" x2="556" y2="212" />
  <line class="flow-out" marker-end="url(#ahAcc3)"  x1="674" y1="212"  x2="674" y2="90" />

  <!-- Atari ST (right) -->
  <rect class="dev"    x="730" y="62" width="150" height="157" rx="8" />
  <rect class="dev-hd" x="730" y="62" width="150" height="24" rx="8" />
  <text class="dev-title" x="805" y="79" text-anchor="middle">Atari ST · 68000</text>
  <rect class="layer" x="754" y="92"  width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="109" text-anchor="middle">MIDI Maze</text>
  <rect class="layer" x="754" y="122" width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="139" text-anchor="middle">GEM</text>
  <rect class="layer" x="754" y="152" width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="169" text-anchor="middle">BIOS / XBIOS</text>
  <rect class="layer hook" x="754" y="182" width="102" height="26" rx="4" />
  <text class="layer-t accent" x="805" y="199" text-anchor="middle">XBRA hook</text>
  <line class="flow-in" marker-end="url(#ahTeal3)" x1="742" y1="90" x2="742" y2="212" />
  <line class="flow-out" marker-end="url(#ahAcc3)"  x1="868" y1="212"  x2="868" y2="90" />

  <!-- V1++ : a software peer joins the ring -->
  <g>
    <line class="flow2 net" marker-start="url(#ahAcc3)" marker-end="url(#ahAcc3)" x1="450" y1="209" x2="450" y2="236" />
    <text class="flow2-lbl" x="476" y="226" text-anchor="start">TCP/IP</text>
    <rect class="srv" x="378" y="236" width="144" height="30" rx="6" />
    <text class="srv-t" x="450" y="255" text-anchor="middle">hatari-gateway</text>
    <line class="flow2 net" marker-start="url(#ahAcc3)" marker-end="url(#ahAcc3)" x1="450" y1="266" x2="450" y2="290" />
    <text class="flow2-lbl" x="476" y="281" text-anchor="start">file FIFOs</text>
    <rect class="dev" x="372" y="290" width="156" height="48" rx="8" style="stroke: var(--accent); stroke-width:2.5" />
    <text class="dev-title" x="450" y="311" text-anchor="middle">Hatari</text>
    <text class="note-t" x="450" y="327" text-anchor="middle">ST emulator · software peer</text>
  </g>
</svg>

<div class="text-center mt-1" style="font-size: 0.9rem">
  <strong>+ Hatari</strong> joins the same ring through the <strong>hatari-gateway</strong> (file FIFOs ⇄ TCP/IP) — a software peer, so you can test &amp; play without a second real ST.
</div>

<!--
V1++ = the Candidate Architecture with one addition (revealed on the last click): a software
peer. The Hatari ST emulator can't speak TCP directly, so the hatari-gateway (a Python tool
in md-MIDI2IP, bridging Hatari's MIDI via file FIFOs to TCP/IP) connects it to the
orchestrator — it becomes just another node on the ring. Why it matters: you can develop and
even play without owning two physical Atari STs. This sets up v2 (fast iteration, hardware
test pass). ~75s.
-->

---

## …then reality bit

Now the ring runs — and two wrong calls surface. One is a *speed* problem, the other a *correctness* problem.

<div class="flex gap-6 justify-center my-6">
  <div class="era good" style="min-width:240px; text-align:center">
    <span class="era__year">1987 · cable ring</span>
    <div style="font-family:var(--slidev-font-mono); font-weight:700; font-size:1.6rem; color:#2e9e5b">3,125 B/s</div>
    <div class="era__desc">the bar to beat</div>
  </div>
  <div class="era bad" style="min-width:240px; text-align:center">
    <span class="era__year">v1 · SidecarT + real ST</span>
    <div style="font-family:var(--slidev-font-mono); font-weight:700; font-size:1.6rem; color:#d23f57">~970 B/s</div>
    <div class="era__desc">3× slower — the maze freezes</div>
  </div>
</div>

- **Transport — speed:** the per-byte TPROTOCOL handshake only crawls on the **SidecarT + real Atari ST** path (every byte over the cartridge blocks the next). The **Hatari + hatari-gateway** peer is fine — it runs at the **full speed of Hatari's MIDI emulation**. So the bottleneck is the *hardware bridge*, not the idea → the fix is in how we **move bytes**.
- **Orchestrator — correctness:** the **"smart"** one (master election, flow-control) came from a **wrong reading of the MIDI protocol** in the TFG. We don't need any of that smartness — just a **fast relay** that *inspects* the bytes (peeks), never *parses* them.

<!--
THE TURN — now that the ring actually runs (V1++ with the Hatari peer), we measure it and TWO
distinct problems surface. (1) SPEED: the per-byte TPROTOCOL handshake runs ~970 B/s on the
SidecarT + REAL ST path — 3× SLOWER than the 1987 cable (3125) because every byte crosses the
cartridge in lock-step. Crucially this does NOT happen on the Hatari + hatari-gateway peer —
that runs at the full speed of Hatari's MIDI emulation — so the bottleneck is the hardware
bridge, not the concept. (2) CORRECTNESS: the "smart" orchestrator (master election etc.)
was built on a MISREADING of the MIDI protocol from the TFG (the 0x00=MASTER election logic);
we don't need that smartness at all — just a fast relay that PEEKS at bytes, never parses.
Both fixes land in The Final Architecture. ~70s.
-->

---

## The Final Architecture V2

<div class="v2grid">
  <div class="v2card">
    <div class="v2card__epic">Transport</div>
    <div class="v2card__role">Stop handshaking</div>
    <div class="v2card__old">per-byte TPROTOCOL handshake — spin-wait on a token for every single byte</div>
    <div class="v2card__new">fire-and-forget <strong>stream</strong> on the commemul ring: bit-8 = OUT byte, bit-9 = IN advance + confirm-ack</div>
    <div class="v2card__win">★ the ~970 B/s ceiling is gone</div>
  </div>
  <div class="v2card">
    <div class="v2card__epic">Orchestrator</div>
    <div class="v2card__role">Stop parsing</div>
    <div class="v2card__old">"smart" RingState — a master-election heuristic built on a <em>misread</em> of the MIDI protocol</div>
    <div class="v2card__new">dumb <strong>byte relay</strong> — never parses; just relays, plus a live ring-telemetry view</div>
    <div class="v2card__win">★ firmware owns the ring end-to-end</div>
  </div>
  <div class="v2card">
    <div class="v2card__epic">Proof</div>
    <div class="v2card__role">Prove metal + Hatari</div>
    <div class="v2card__old">v1 only proved the path — never a full 2-player match, and needed two physical STs</div>
    <div class="v2card__new">2-player match on <strong>real STs</strong> — or a <strong>Hatari</strong> software peer via the gateway, behind an automated self-test</div>
    <div class="v2card__win">★ it actually plays</div>
  </div>
</div>

<div class="speed">
  <div class="speed__row"><span class="speed__lbl">v1 · candidate</span><span class="speed__track"><i class="speed__bar bad" style="width:31%"></i></span><span class="speed__val">~970 B/s — crawls</span></div>
  <div class="speed__row"><span class="speed__lbl">1987 · cable</span><span class="speed__track"><i class="speed__bar bar" style="width:100%"></i></span><span class="speed__val">3,125 B/s — the bar</span></div>
  <div class="speed__row"><span class="speed__lbl">v2 · streaming</span><span class="speed__track"><i class="speed__bar hot" style="width:100%"></i></span><span class="speed__val">handshake gone → plays on real hardware</span></div>
</div>

<div class="subtract"><span class="subtract__tag">THE PATTERN</span> Both wins were <strong>deletions, not additions</strong> — the fix was tearing out plumbing, not writing more.</div>

<!--
THE PAYOFF. Three iterations from md-MIDI2IP (Iteration 2) turned the Candidate into something
that works: (1) EPIC-09 — drop the per-byte TPROTOCOL handshake for a fire-and-forget byte
stream on the commemul ROM3 ring (bit-8 OUT, bit-9 IN + confirm-ack); this kills the ~970 B/s
ceiling that made it 3× slower than the 1987 cable. (2) EPIC-11 — the "smart" orchestrator's
RingState was a master-election heuristic built on a MISREAD of the MIDI protocol (caused a
master-flip on hardware); rip it out → a dumb byte relay that never parses, plus live ring
telemetry. (3) EPIC-10 — validate a real 2-player match on actual STs behind an automated
self-test gate. Honest framing: v2 removes the artificial handshake ceiling and makes the maze
playable over IP on real hardware — the goal was parity/playability, not out-running the cable.
The Hatari + hatari-gateway peer (shown on V1++) is what let us iterate this fast. ~90s.
-->

---

## The Final Architecture V2 — the wiring

<svg class="arch2-svg" style="max-width:760px" viewBox="0 -56 910 404" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="ahDark4" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--ink)" />
    </marker>
    <marker id="ahAcc4" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--accent)" />
    </marker>
    <marker id="ahTeal4" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto-start-reverse">
      <path d="M0,0 L7,3 L0,6 Z" style="fill: var(--link)" />
    </marker>
  </defs>

  <path class="ring-arc" marker-start="url(#ahAcc4)" marker-end="url(#ahAcc4)" d="M95,60 Q450,-104 805,60" />
  <text class="ring-arc-lbl" x="450" y="2" text-anchor="middle">one virtual MIDI ring — the ends are joined in software</text>

  <line class="flow2"            marker-start="url(#ahDark4)" marker-end="url(#ahDark4)" x1="170" y1="140" x2="215" y2="140" />
  <line class="flow2 net stream" marker-start="url(#ahAcc4)"  marker-end="url(#ahAcc4)"  x1="355" y1="140" x2="395" y2="140" />
  <line class="flow2 net stream" marker-start="url(#ahAcc4)"  marker-end="url(#ahAcc4)"  x1="505" y1="140" x2="545" y2="140" />
  <line class="flow2"            marker-start="url(#ahDark4)" marker-end="url(#ahDark4)" x1="685" y1="140" x2="730" y2="140" />
  <text class="flow2-lbl" x="192" y="131" text-anchor="middle">cartridge</text>
  <text class="flow2-lbl" x="375" y="131" text-anchor="middle">stream</text>
  <text class="flow2-lbl" x="525" y="131" text-anchor="middle">stream</text>
  <text class="flow2-lbl" x="707" y="131" text-anchor="middle">cartridge</text>

  <!-- Atari ST (left) -->
  <rect class="dev"    x="20" y="62" width="150" height="157" rx="8" />
  <rect class="dev-hd" x="20" y="62" width="150" height="24" rx="8" />
  <text class="dev-title" x="95" y="79" text-anchor="middle">Atari ST · 68000</text>
  <rect class="layer" x="44" y="92"  width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="109" text-anchor="middle">MIDI Maze</text>
  <rect class="layer" x="44" y="122" width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="139" text-anchor="middle">GEM</text>
  <rect class="layer" x="44" y="152" width="102" height="26" rx="4" />
  <text class="layer-t" x="95" y="169" text-anchor="middle">BIOS / XBIOS</text>
  <rect class="layer hook" x="44" y="182" width="102" height="26" rx="4" />
  <text class="layer-t accent" x="95" y="199" text-anchor="middle">XBRA hook</text>
  <line class="flow-in" marker-end="url(#ahTeal4)" x1="32"  y1="212" x2="32"  y2="90" />
  <line class="flow-out" marker-end="url(#ahAcc4)"  x1="158" y1="90"  x2="158" y2="212" />

  <!-- SidecarT (left) -->
  <rect class="dev"    x="215" y="62" width="140" height="157" rx="8" />
  <rect class="dev-hd" x="215" y="62" width="140" height="24" rx="8" />
  <text class="dev-title" x="285" y="79" text-anchor="middle">SidecarT · RP2040</text>
  <rect class="layer" x="238" y="92"  width="94" height="26" rx="4" />
  <text class="layer-t" x="285" y="109" text-anchor="middle">microfirmware</text>
  <rect class="layer bridge upd" x="238" y="122" width="94" height="26" rx="4" />
  <text class="layer-t accent" x="285" y="139" text-anchor="middle">stream ⇄ TCP/IP</text>
  <rect class="layer" x="238" y="152" width="94" height="26" rx="4" />
  <text class="layer-t" x="285" y="169" text-anchor="middle">Wi-Fi / TCP/IP</text>
  <text class="note-t" x="285" y="200" text-anchor="middle">fire-and-forget</text>
  <line class="flow-in" marker-end="url(#ahTeal4)" x1="226" y1="212" x2="226" y2="90" />
  <line class="flow-out" marker-end="url(#ahAcc4)"  x1="344" y1="90"  x2="344" y2="212" />

  <!-- orchestrator -->
  <rect class="srv upd" x="395" y="92" width="110" height="117" rx="8" />
  <text class="srv-t" x="450" y="114" text-anchor="middle">Orchestrator</text>
  <text class="srv-s" x="450" y="131" text-anchor="middle" style="fill: var(--accent-ink)">TCP/IP · Python</text>
  <text class="srv-s" x="450" y="159" text-anchor="middle">dumb relay</text>
  <text class="srv-s" x="450" y="172" text-anchor="middle">peeks · never parses</text>

  <!-- SidecarT (right) -->
  <rect class="dev"    x="545" y="62" width="140" height="157" rx="8" />
  <rect class="dev-hd" x="545" y="62" width="140" height="24" rx="8" />
  <text class="dev-title" x="615" y="79" text-anchor="middle">SidecarT · RP2040</text>
  <rect class="layer" x="568" y="92"  width="94" height="26" rx="4" />
  <text class="layer-t" x="615" y="109" text-anchor="middle">microfirmware</text>
  <rect class="layer bridge upd" x="568" y="122" width="94" height="26" rx="4" />
  <text class="layer-t accent" x="615" y="139" text-anchor="middle">stream ⇄ TCP/IP</text>
  <rect class="layer" x="568" y="152" width="94" height="26" rx="4" />
  <text class="layer-t" x="615" y="169" text-anchor="middle">Wi-Fi / TCP/IP</text>
  <text class="note-t" x="615" y="200" text-anchor="middle">fire-and-forget</text>
  <line class="flow-in" marker-end="url(#ahTeal4)" x1="556" y1="90" x2="556" y2="212" />
  <line class="flow-out" marker-end="url(#ahAcc4)"  x1="674" y1="212"  x2="674" y2="90" />

  <!-- Atari ST (right) -->
  <rect class="dev"    x="730" y="62" width="150" height="157" rx="8" />
  <rect class="dev-hd" x="730" y="62" width="150" height="24" rx="8" />
  <text class="dev-title" x="805" y="79" text-anchor="middle">Atari ST · 68000</text>
  <rect class="layer" x="754" y="92"  width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="109" text-anchor="middle">MIDI Maze</text>
  <rect class="layer" x="754" y="122" width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="139" text-anchor="middle">GEM</text>
  <rect class="layer" x="754" y="152" width="102" height="26" rx="4" />
  <text class="layer-t" x="805" y="169" text-anchor="middle">BIOS / XBIOS</text>
  <rect class="layer hook" x="754" y="182" width="102" height="26" rx="4" />
  <text class="layer-t accent" x="805" y="199" text-anchor="middle">XBRA hook</text>
  <line class="flow-in" marker-end="url(#ahTeal4)" x1="742" y1="90" x2="742" y2="212" />
  <line class="flow-out" marker-end="url(#ahAcc4)"  x1="868" y1="212"  x2="868" y2="90" />

  <!-- software peer stays on the ring -->
  <g>
    <line class="flow2 net stream" marker-start="url(#ahAcc4)" marker-end="url(#ahAcc4)" x1="450" y1="209" x2="450" y2="236" />
    <text class="flow2-lbl" x="476" y="226" text-anchor="start">TCP/IP</text>
    <rect class="srv" x="378" y="236" width="144" height="30" rx="6" />
    <text class="srv-t" x="450" y="255" text-anchor="middle">hatari-gateway</text>
    <line class="flow2 net stream" marker-start="url(#ahAcc4)" marker-end="url(#ahAcc4)" x1="450" y1="266" x2="450" y2="290" />
    <text class="flow2-lbl" x="476" y="281" text-anchor="start">file FIFOs</text>
    <rect class="dev" x="372" y="290" width="156" height="48" rx="8" style="stroke: var(--accent); stroke-width:2.5" />
    <text class="dev-title" x="450" y="311" text-anchor="middle">Hatari</text>
    <text class="note-t" x="450" y="327" text-anchor="middle">ST emulator · software peer</text>
  </g>
</svg>

<div class="dchanges">
  <div class="dchange"><span class="ico">⚡</span><strong>Transport</strong> — <s>handshake</s> → <b>fire-and-forget stream</b></div>
  <div class="dchange"><span class="ico">🧹</span><strong>Orchestrator</strong> — <s>smart router</s> → <b>dumb relay</b> + telemetry</div>
</div>

<!--
SAME diagram as V1++, evolved to v2 (highlighted in accent + glow). What changed: (1) the two
SidecarT bridge boxes go from the synchronous "TPROTO ⇄ TCP/IP" command path to a "stream ⇄
TCP/IP" fire-and-forget byte stream on the commemul ring (the inter-node hops now animate to read
as a stream; bit-8 = OUT byte, bit-9 = IN advance + confirm-ack). (2) the orchestrator drops from
a "smart" ring router to a "dumb relay" that only peeks, never parses, plus live telemetry. The
XBRA hook, the kept-intact ST MIDI path, and the Hatari software peer are UNCHANGED from V1++ —
only the glowing pieces moved. This is slide 32's three wins, shown in the wiring. ~60s.
-->

---
layout: fact
---

# One project,<br>four decades of tools

<!-- Landmark. Cycle the thesis: the project is a time machine across the ladder. ~20s. -->

---
layout: section
---

<span class="act-num">ACT 3</span>

# AI vs the ladder

<div class="recap">Previously: 1986 metal → 2026 rebuild. Now the payoff.</div>

<!-- Divider into the heart of the talk. -->

---

## The surprise

AI is confidently wrong at <span class="accent">both ends</span>.

<div class="ladder">
  <div class="rung illusion"><span class="rung__name">Research</span> architecting the solution <span class="rung__ai">looks brilliant ⚠</span></div>
  <div class="rung good"><span class="rung__name">Python</span> high-level glue <span class="rung__ai">great</span></div>
  <div class="rung good"><span class="rung__name">C</span> firmware <span class="rung__ai">strong · sandboxed</span></div>
  <div class="rung bad"><span class="rung__name">68000 asm</span> the metal <span class="rung__ai">improvising</span></div>
</div>

<div class="mt-6 text-xl">Loud at the metal. Seductive at the top — it <span class="accent">looks best</span> exactly where you can least trust it.</div>

<!--
THE SALIENT IDEA + THE SURPRISE. This is the slide they photograph. TWO failure modes, not one:
near the metal (C, 68000 asm) it's VISIBLY bad — it improvises and you catch it immediately. At
the top (Research/architecture) it's INVISIBLY bad — fluent, complete, over-engineered, and it
LOOKS brilliant, so the errors slip past unless an expert verifies (callback to the "illusion"
slide). Hence the dashed green Research rung: looks solid, isn't. The unifying point counters the
"AI replaces engineers" narrative: the danger isn't only where it's weak, it's where it's
*convincing*. Human judgment/verification is the durable skill. ~2 min — let it land.
-->

---

## Personality 1 · the intern

**The metal — 68000 assembly.** Confident, fluent… and almost always wrong.

<div class="fmode seen">FAILS LOUD · you catch it instantly</div>

<div class="flex gap-6 items-start mt-3">
<div class="flex-1">

- **Wrong CPU** — emits **680x0** instructions (68020 / 68030) the ST's bare **68000** never had
- **Writes to ROM** — keeps storing into cartridge **ROM** space… which is *read-only*. Told it. Did it again.
- **Baroque control flow** — branches to a shared label *just to reach an* `rte`

</div>
<div style="flex:none; width:430px">

```asm
.mbt_stat:
    move.l  MIDI_IN_COUNT,d0
    beq.s   .mbt_rte
    moveq   #-1,d0
    bra.s   .mbt_rte    ; a detour…
.mbt_rte:
    rte                 ; …for what ONE
                        ; inline rte does
```

</div>
</div>

<div class="bigidea" style="margin-top:0.5rem">
  <span class="spark">NON-NEGOTIABLE</span>
  You don't prompt this away — you <strong>iterate the generated code</strong> until the AI nails it.
</div>

<!--
"Improvising so it doesn't get fired" — the funniest, most quotable beat. THREE real failures from
this project's 68000 work (target/atarist/src/userfw.s): (1) it reaches for 680x0 instructions the
ST's plain 68000 doesn't have; (2) it repeatedly emits stores into ROM space even after being told
in the guidelines that ROM is read-only; (3) it over-complicates — e.g. branching to a shared
.mbt_rte label just to execute an rte, when the clean handler is literally "move.l
MIDI_IN_STATUS,d0 / rte" inline (real before→after from commit 3d0e422 → current). KEY: these fail
LOUD — won't assemble, or crash on hardware, so you catch them fast (low danger; contrast the
architect). COROLLARY: you cannot prompt your way out of it — you must iterate the generated code,
review pass after review pass, until it's right. ~90s.
-->

---

## Personality 2 · the contractor

**The middle — C firmware.** Hand it a blueprint and it builds — flawlessly.

<div style="display:flex; gap:0.5rem">
  <span class="fmode seen">CODE · FLAWLESS</span>
  <span class="fmode slip">SPEC · FATAL</span>
</div>

- Writes **excellent C** — works first pass; iterate once or twice and it's *optimized*
- The hard part on an MCU isn't the code — it's **testing &amp; validation**
- So months earlier I built it a home: a **microfirmware framework + a Claude skill** for **sandboxed** development
- Result: **sniper-precise**, valid, crash-free, no "uh… what's going on?" — *wildly* more productive

<div class="bigidea" style="margin-top:0.7rem">
  <span class="spark">THE CATCH</span>
  The code was flawless; the <strong>spec</strong> was fatal — synchronous commands killed us.<br>
  With the intern you iterate the <strong>code</strong>. With the contractor you iterate the <strong>spec</strong>.
</div>

<!--
THE REFRAME of the C rung. Counter-intuitive but true: with the right scaffolding, AI writes C
*beautifully*. (1) Great first-pass C; a couple of iterations and it's optimized. (2) The real
hazard on a microcontroller is testing/validation, not authoring. (3) So I pre-built the harness —
a microfirmware framework + a Claude skill that codes inside its sandbox (built months earlier,
deliberately). (4) Result: sniper-precise, valid, no crashes, hugely productive. THE TWIST: none of
it saved us, because the failure wasn't the code — it was the SPEC. The synchronous TPROTOCOL
command design (the v1 bottleneck) was wrong, and the AI faithfully, flawlessly built the wrong
thing. CODE flawless / SPEC fatal. This is the bridge: the failure has climbed from code (asm) to
spec — and specs come from up the ladder (→ the architect). Garbage spec in, flawless garbage out.
KEY CONTRAST with Personality 1: there the iteration loop is over the CODE (review the asm until it's
right); HERE the code is already right — the loop you must run is over the SPEC. The thing you iterate
moves up the ladder with the failure. ~90s.
-->

---

## Personality 3 · the senior

**High up — Python.** Give it good specs and it just… delivers.

<div style="display:flex; gap:0.5rem">
  <span class="fmode seen">EARNS YOUR TRUST</span>
  <span class="fmode seen">FULLY AGENTIC</span>
</div>

- **No hand-holding** — no need to name a framework or library; from the spec it picks a good solution
- **Flawless code** — and trivially **testable** (vs C-on-MCU or asm-on-the-ST)
- **Self-driving loops** — write → test → fix → green, on its own; code compliance &amp; validity checked automatically
- **Specs still rule** — same as C, the bug was the *spec* — but the **test suite surfaces spec flaws fast**

<div class="bigidea" style="margin-top:0.7rem">
  <span class="spark">DELEGATE IT</span>
  With good, structured specs you can hand <strong>most of the work</strong> to agentic AI. What's left for you: the <strong>spec</strong> — and the judgment.
</div>

<!--
THE PEAK OF DELEGATION. At the top of the ladder, in a modern high-level language, AI is at its best:
(1) no need to prescribe a framework/library — from the spec it chooses a good design; (2) the code is
flawless; (3) it's trivially testable (a test harness is easy — unlike C on the MCU or asm on the ST);
(4) so the loop goes FULLY AGENTIC — it writes, tests, fixes and re-runs until green, code-validity
checks automated, hands-off. (5) And again the limiter was the SPEC, not the code — but here the test
suite makes spec flaws easy to spot. THE TAKEAWAY: with good, structured specs you can delegate most
of the work to agentic AI; what's irreducibly yours is the spec + the judgment. THE SETUP for P4: "the
spec / architecture" is exactly the thing you can't hand off — because that's where the competence is
an illusion. It earns your trust here, which is what the architect weaponises next. ~75s.
-->

---

## Personality 4 · the architect

**The very top — research &amp; architecture.** A beautiful deck, a full bibliography… and a <span class="accent">16-daughterboard cathedral</span> to move three bytes.

<div style="display:flex; gap:0.5rem">
  <span class="fmode warn">LOOKS BRILLIANT ⚠</span>
  <span class="fmode slip">FAILS SILENT · you ship it</span>
</div>

- The **spec** that doomed the contractor and the senior? It was **written right here.**
- No crash, no fake opcode — a fluent, cited, *over-engineered* design you build perfectly… and ship
- It looks like the **senior** you just learned to trust — so you stop checking. <span class="accent">That's the trap.</span>

<div class="bigidea" style="margin-top:0.7rem">
  <span class="spark">THE ONE THING YOU CAN'T DELEGATE</span>
  Everything below this rung, hand to the AI. The <strong>spec &amp; the architecture</strong>, you can't — this is where its competence is an <strong>illusion</strong>. This rung stays human.
</div>

<!--
THE PAYOFF of the whole ladder (callback to slides 18-20 + the climb P1→P3). The failure has been
climbing: code (intern) → spec (contractor) → and the spec/architecture itself is authored HERE. So
the wrong "synchronous commands" spec that doomed C and Python was born on THIS rung. The failure is
INVISIBLE: nothing crashes, no fabricated opcode — just a fluent, cited, over-engineered design you
implement flawlessly and ship. And because it reads exactly like the senior you just learned to
trust (and just delegated everything to, P3), you lower your guard — which is precisely when it's
most dangerous. THE PINPOINT: P3 said "delegate everything but the spec + judgment." THIS is why —
the one rung you cannot hand off is the architecture, because here competence is an illusion only an
expert catches. This is THE finding of the talk. Let it land cold. ~90s.
-->

---
layout: statement
---

# The intern improvises.<br>The architect over-engineers.<br>Both sound <span class="accent">certain</span>.

<div class="mt-6 text-2xl">The dangerous one is the architect — because it's the one you <strong>believe</strong>.</div>

<!--
THE SLOGAN (replaces "brilliant senior / confident intern"). The whole act in one breath: it's not
dumb-low / smart-high — it's unreliable at BOTH ends, and most dangerous exactly where it's most
convincing. Say it, pause, then the kicker line. The handle they repeat to a colleague. ~30s.
-->

---

## Working with AI<br>(without losing faith in humanity)

- **Build the sandbox first** — your highest-leverage work is the *harness*: a framework + tests that let the AI code safely and prove itself
- **Delegate the loop, own the spec** — with good, structured specs, hand the whole code loop to agentic AI; keep the spec, the architecture, the judgment
- **Iterate the right layer** — down low you iterate the *code*; up high you iterate the *spec*. Match the fix to the failure
- **Distrust the most polished answer** — verify hardest where it's most convincing; ground it in sources (NotebookLM on primary docs beats a model's memory)

<div class="mt-6 text-2xl">You stay the engineer. It's the <span class="accent">buddy</span>, not the boss.</div>

<!--
THE PRACTICAL PLAYBOOK — distilled from ACT 3, in order of leverage:
(1) BUILD THE SANDBOX — the human move that unlocked everything: a microfirmware framework + a Claude
    skill so the AI codes inside a safe, testable box (P2/P3). This is where YOU add the most value.
(2) DELEGATE THE LOOP, OWN THE SPEC — with good structured specs, agentic AI runs write→test→fix on
    its own (P3); what you keep is the spec, the architecture, the judgment — the things it fakes (P4).
(3) ITERATE THE RIGHT LAYER — the thing you iterate climbs with the failure: code at the metal (P1),
    spec higher up (P2). Don't re-prompt code when the spec is what's broken.
(4) DISTRUST THE POLISHED ANSWER — the architect's illusion (P4): verify hardest where it's most
    convincing; make it cite primary sources (NotebookLM) instead of trusting its memory.
Closing line is the human note that earns the slide's title — buddy, not boss. Sets up the demo +
close. ~90s.
-->

---
layout: statement
---

# Demo time! 🕹️

<div class="mt-6 text-2xl">MIDI Maze, multiplayer, <span class="accent">over IP</span> — live on real hardware.</div>

<!--
LIVE DEMO — switch to the setup: real Atari ST(s) + SidecarT bridge(s) + the orchestrator, MIDI Maze
running multiplayer over TCP/IP. Keep a recorded clip on hand as a fallback in case the live setup
misbehaves (Winston: control your risk). ~2-3 min including setup.
-->

---

## Number of inspections = the key metric

<div class="text-lg mt-1">Same loop every era — but the laps <span class="accent">and the hours</span> to ship a feature keep collapsing.</div>

<div class="flex gap-8 items-center mt-2">

<div class="loop">
  <div class="loop__ring"></div>
  <div class="loop__hint"><span>You only <b>learn</b><br>once per lap</span></div>
  <div class="node" style="--a:0deg">Code</div>
  <div class="node" style="--a:72deg">Build &amp;<br>Reload</div>
  <div class="node" style="--a:144deg">Test</div>
  <div class="node is-key" style="--a:216deg">Inspect</div>
  <div class="node" style="--a:288deg">Commit</div>
</div>

<div class="eras flex-1">
  <div class="era bad" v-click>
    <span class="era__year">1988</span>
    <div class="era__desc">Compile off a floppy, squint at the screen.</div>
    <div class="era__steps">Code 14m · Build 5m · Test 2m · <b>Inspect 2m</b> · Commit 1m</div>
    <div class="era__verdict"><b>~40 laps</b> → ≈ 2 days / feature · slow &amp; expensive: don't fail</div>
  </div>
  <div class="era good" v-click>
    <span class="era__year">2023</span>
    <div class="era__desc">Hot reload, debuggers, git.</div>
    <div class="era__steps">Code 18m · Build &lt;1s · Test 10s · <b>Inspect 1m</b> · Commit 10s</div>
    <div class="era__verdict"><b>~12 laps</b> → ≈ 4 hrs / feature · fast &amp; cheap: fail fast</div>
  </div>
  <div class="era twist" v-click>
    <span class="era__year">2026 · AI</span>
    <div class="era__desc">The agent grinds the loop — ~10–40 min, many tries.</div>
    <div class="era__steps">Code AI · Build auto · Test auto · <b>Inspect = you</b> · Commit auto</div>
    <div class="era__verdict"><b>~3 laps</b> → ≈ 1 hr of your time · agent folds the rest; review is the bottleneck</div>
  </div>
</div>

</div>

<!--
ZOOM-OUT, right before the takeaway. The project worked (previous slide) — but the real
story is how *building itself* changed. The loop is Code → Build & Reload → Test → Inspect →
Commit; each lap gives you exactly ONE inspection — one chance to learn — so the metric is how
many laps (inspections) you can afford. THE FUNDAMENTAL METRIC: laps (iterations) to ship a feature,
and it keeps collapsing — X(1988) > Y(2023) >> Z(2026): you needed ~40 laps in 1988, ~12 in 2023 (better
tools/frameworks/knowledge do more per lap), ~3 in 2026 — because the agent FOLDS the many human
iterations into its own internal loop. Two dimensions per era: laps/feature AND time/lap (per-step times
are representative — floppy compile/link ≈ minutes; modern HMR ~instant, devs notice >15s; agentic coding
≈ 8–48 min/task multi-iteration, NOT the ~8s single-call latency; adjust to your own numbers). Reveal one
click at a time:
  1988: ~40 laps × ~24 min/lap ≈ 2 days/feature — floppy compile/link dominates; laps so dear you optimize to NOT fail.
  2023: ~12 laps × ~20 min/lap ≈ 4 hrs/feature — mechanical steps ~0, so your own coding is the lap; fewer laps, fail fast.
  2026: ~3 laps ≈ 1 hr of YOUR time — the loop didn't get faster, it MOVED: the agent grinds many tries internally (10–40 min),
  folding what was several human iterations into one. You stop typing; your whole cost becomes REVIEW →
  judgment is the bottleneck. Don't oversell speed; the honest point is fewer-but-heavier human laps.
This hands straight into "What to take home": the durable skill is knowing when it's wrong.
TIE-IN: in this project I was in all three eras at once — 2026 in Python, ~2023 in C, still
1988 in 68000 asm. The era isn't the date; it's the abstraction level. ~2 min.
-->

---

## What to take home

<div class="ladder">
  <div class="rung"><span class="rung__name">1986</span> humans climb down to the metal; knowledge is scarce, memorized</div>
  <div class="rung"><span class="rung__name">2023</span> <span>peak human coding: the best tools, frameworks &amp; knowledge — and <strong>the last era we wrote every line</strong></span></div>
  <div class="rung"><span class="rung__name">2026</span> <span>we live at the top — <strong>AI writes the code, you judge it</strong>; and it dazzles exactly where it's <em>least</em> reliable</span></div>
  <div class="rung bad"><span class="rung__name">→ future</span> AI climbs down the ladder; humans climb up — to judgment &amp; taste</div>
</div>

<div class="mt-6 text-lg">The durable skill isn't typing code. It's <span class="accent">knowing when it's wrong</span>.</div>

<div class="bigidea" style="margin-top:0.9rem">
  <span class="spark">REMEMBER THIS</span>
  The biggest wins were <strong>deletions, not additions</strong> — the new craft is knowing what <strong>not</strong> to build.
</div>

<!--
THE FINAL CONTENT SLIDE (Winston: end on contributions/takeaways, NOT "thank you").
This is the 1986 → 2026 → future spine. The future row is YOUR prediction — rewrite it in
your own words. HIGHLIGHT the "deletions, not additions" banner — it's the payoff of the V2
slide (we beat the problem by ripping out the per-byte handshake AND the smart orchestrator,
not by adding cleverness). Tie it to judgment: AI makes writing code cheap, so the leverage
moves to knowing what to remove / not build. Deliver this slowly; it's the thing they carry
out the door. ~2 min.
-->

---
layout: center
class: cover-slide
---

<div class="maze-smiley" aria-hidden="true"></div>

# Still too old for this <span class="accent">sh*t</span>

<div class="byline">
  Diego Parrilla · github.com/&lt;repo&gt; · @&lt;handle&gt;
</div>

<!--
Final WORDS = a joke / callback (Winston: leave them laughing, never end on "thank you").
Links small. Then take questions. Replace repo/handle with the real ones.
-->
