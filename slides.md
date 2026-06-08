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
layout: fact
---

# Rung 1

That was the metal. Hold onto it — we'll come back.

<!-- WINSTON verbal punctuation / landmark. Anyone who drifted can rejoin here. ~15s. -->

---

## Number of inspections = the key metric

<div class="flex gap-8 items-center mt-2">

<div class="loop">
  <div class="loop__ring"></div>
  <div class="loop__hint"><span>You only <b>learn</b><br>once per lap</span></div>
  <div class="node" style="--a:0deg">Code</div>
  <div class="node" style="--a:60deg">Test</div>
  <div class="node" style="--a:120deg">Build &amp;<br>Reload</div>
  <div class="node is-key" style="--a:180deg">Inspect</div>
  <div class="node" style="--a:240deg">Commit</div>
  <div class="node" style="--a:300deg">LEARN!</div>
</div>

<div class="eras flex-1">
  <div class="era bad" v-click>
    <span class="era__year">1988</span>
    <div class="era__desc">Compile off a floppy, squint at the screen.</div>
    <div class="era__verdict">Slow &amp; expensive → don't fail</div>
  </div>
  <div class="era good" v-click>
    <span class="era__year">2023</span>
    <div class="era__desc">Hot reload, debuggers, git.</div>
    <div class="era__verdict">Fast &amp; cheap → fail fast</div>
  </div>
  <div class="era twist" v-click>
    <span class="era__year">2026 · AI</span>
    <div class="era__desc">AI runs the lap for you. Inspections ≈ free.</div>
    <div class="era__verdict">Bottleneck moves to judgment</div>
  </div>
</div>

</div>

<!--
THE EVOLUTION SLIDE — bridges 1988 (metal) and 2026 (stack). The loop is Code → Test →
Build & Reload → Inspect → Commit → LEARN. The metric is how many laps you can afford,
because you only LEARN once per lap. Reveal eras one click at a time.

Per-step time, the point to make verbally:
  Step            1988            2023           2026 (AI)
  Code            hours, by hand  minutes (IDE)  seconds*  (*high abstraction only)
  Build & Reload  minutes/floppy  seconds        instant
  Inspect         printf / LED    debugger/logs  AI reads output, proposes fix
  Commit          save & pray     git, instant   AI branches for you
  LEARN           few laps, slow  many, fail-fast lap ≈ free → judging, not doing

1988: laps so expensive you optimize to NOT fail (precision).
2023: laps free → fail fast, recover faster.
2026: AI laps for you → iteration stops being the bottleneck; JUDGMENT is. "Knowing when
it's wrong" — the same line as the closing slide.

KILLER TIE-IN (say it): in MIDI Maze I was in all three eras AT ONCE — 2026 in Python,
~2023 in C, still 1988 in 68000 asm. The era isn't the date; it's the abstraction level.
That sentence links this slide to the ladder and the takeaway. ~2 min.
-->

---
layout: section
---

<span class="act-num">ACT 2 · 2026</span>

# The stack

<div class="recap">Previously: 1986, close to the metal.</div>

<!-- Divider + recap (cycling the thesis). -->

---

## The architecture

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
  <text class="srv-t" x="450" y="114" text-anchor="middle">TCP/IP server</text>
  <text class="srv-s" x="450" y="131" text-anchor="middle" style="fill: var(--accent-ink)">· Python ·</text>
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

## Rung: C (the Pico)

- RP2040 firmware: MIDI in/out, Wi-Fi, the bridge logic
- Real-time-ish, but with a stdlib and a debugger
- Where most of the "make it actually work" lived

<div class="ph mt-6">
  <span class="ph__tag">photo</span>
  The Pico wired to the Atari ST / the bridge board
</div>

<!-- War story rung 2: comfortable middle ground. ~75s. -->

---

## Rung: Python (the glue)

- Test harnesses, packet inspection, the PC-side client
- Fast to write, fast to throw away
- The layer furthest from the metal — remember that

<!--
War story rung 3. Explicitly flag "furthest from the metal" — this is the setup for the
Act 3 payoff. ~60s.
-->

---

## The AI cast

- **Codex** — ...
- **Claude Code** — ...
- **Copilot** — ...
- **NotebookLM** — the reference librarian (Atari manuals, MIDI specs)

<!--
Introduce the AI tools as recurring CHARACTERS, not a feature list. One line each on the
role they played. We'll pay them off as "personalities" in Act 3. Keep placeholders here
until you decide who gets credit/blame for what. ~75s.
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

<div class="recap">Previously: 1986 metal → 2026 stack. Now the payoff.</div>

<!-- Divider into the heart of the talk. -->

---

## The surprise

AI is only as good as the abstraction is high.

<div class="ladder">
  <div class="rung good"><span class="rung__name">Python</span> high-level glue <span class="rung__ai">brilliant</span></div>
  <div class="rung meh"><span class="rung__name">C</span> firmware <span class="rung__ai">mediocre</span></div>
  <div class="rung bad"><span class="rung__name">68000 asm</span> the metal <span class="rung__ai">improvising</span></div>
</div>

<div class="mt-6 text-xl">The closer to the metal, the more it <span class="accent">improvises</span>.</div>

<!--
THE SALIENT IDEA + THE SURPRISE. This is the slide they photograph. Counter to the
"AI replaces engineers" narrative: it got WORSE the deeper we went. ~2 min — let it land.
-->

---

## Personality 1: the brilliant one

High abstraction (Python). Fluent, fast, mostly right.

<div class="ph mt-6">
  <span class="ph__tag">moment</span>
  A real example where AI nailed it
</div>

<!-- Tie to a concrete moment in the project. ~60s. -->

---

## Personality 2: the mediocre one

Middle of the stack (C). Plausible, but you have to check everything.

<div class="ph mt-6">
  <span class="ph__tag">moment</span>
  A real example where it was almost-but-not-quite
</div>

<!-- ~60s. -->

---

## Personality 3: improvising so it doesn't get fired

The metal (68000 asm). Confident. Wrong. Invents instructions.

<div class="ph mt-6">
  <span class="ph__tag">moment</span>
  A real example of confident nonsense
</div>

<!--
The funniest beat — confidently fabricated asm. Land the "improvising so it doesn't get
fired" line hard. This is your most quotable moment. ~75s.
-->

---

## Reverse engineering with AI<br>(without losing faith in humanity)

- Use AI where it's strong; verify relentlessly where it's weak
- NotebookLM on the primary sources beat asking a model from memory
- You stay the engineer; it's the buddy, not the boss

<!--
The practical takeaway — what actually worked. Honest, useful, sets up the close. ~90s.
-->

---
layout: statement
---

# Brilliant senior at the top.<br>Confident intern at the bottom.

<!-- THE SLOGAN. Say it, pause, move on. The handle they repeat to a colleague. ~20s. -->

---

## Did it work?

<div class="ph mt-4">
  <span class="ph__tag">video</span>
  Demo: MIDI Maze multiplayer over IP — ST + remote node
</div>

<!--
The payoff moment. PREFER a recorded clip over live (Winston: control your risk). If live,
have the video as backup. ~2-3 min including setup.
-->

---

## What to take home

<div class="ladder">
  <div class="rung"><span class="rung__name">1986</span> humans climb down to the metal; knowledge is scarce, memorized</div>
  <div class="rung"><span class="rung__name">2026</span> we live high on the ladder; AI is strongest where we've climbed highest</div>
  <div class="rung bad"><span class="rung__name">→ future</span> AI climbs down the ladder; the human skill becomes judgment &amp; verification</div>
</div>

<div class="mt-6 text-lg">The durable skill isn't typing code. It's <span class="accent">knowing when it's wrong</span>.</div>

<!--
THE FINAL CONTENT SLIDE (Winston: end on contributions/takeaways, NOT "thank you").
This is the 1986 → 2026 → future spine. The future row is YOUR prediction — rewrite it in
your own words. Deliver this slowly; it's the thing they carry out the door. ~2 min.
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
