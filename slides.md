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
No abras con el chiste del título: la promesa de verdad va en la siguiente diapositiva.
Saludo breve y directo: soy Diego, un Señor de Logroño que hace cosas con ordenadores, y esto va de una mala idea.
"30s"
-->

---
layout: statement
---

# By the end, you'll predict<br>where AI <span class="accent">actually</span> helps —<br>now and in the future

<!--
LA PROMESA. Es el contrato de la charla: todo lo demás lo paga. Dilo despacio y mirando al público.
Casi literal: 

"Al final de la charla vais a poder mirar cualquier capa del stack —de ensamblador del 68000 pasando por
script de Python, hasta el diseño de la arquitectura— y predecir cuánto os ayuda de verdad la IA ahí hoy. 
Y os llevaréis una idea de hacia dónde probablemente irá en el futuro."

45s
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
LA HISTORIA DE ORIGEN (cuéntala con calma, en tono cercano).
- Hago hardware para ordenadores de hace 40 años. Creé "The SidecarT", un cartucho para el Atari ST;
  funcionó sorprendentemente bien. De un cacharro salieron varios y monté una empresa pequeña,
  SidecarTridge. La placa y el logo del collage son míos; en la foto soy yo con dieciséis años.
- ¿Por qué volví al retro? El COVID: como mucha gente, pensamos que igual nos moríamos y miramos atrás,
  a cuando éramos felices. Para mí, mi primer ordenador. Nostalgia pura, quería volver a sentir aquello.
- Empecé a programar una intro, desempolvé un Atari ST… y casi sin darme cuenta estaba soldando la
  primera versión de The SidecarT.
- El chiste va al final, no al principio: todo este proyecto —y esta charla— es esa nostalgia con mala
  idea. Tono autocrítico, crédito por viejo. No te enrolles.


2 min
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
Marca la frontera: esto NO es lo que esperan —ni charla de nostalgia ni hype de IA—; va de cómo ha
cambiado programar de 1986 a 2026 y hacia dónde va.

Acción: haz la pregunta de verdad — "¿quién ha escrito alguna vez una línea de ensamblador?".
Espera 7 segundos. Mira las manos.
Señala la división de la sala: esa frontera entre los de ensamblador y el resto es justo el tema de
la charla.

45s
-->

---
layout: section
---

<span class="act-num">ACT 1 · 1986</span>

# Close to the metal

<!-- Separador de acto. 

El mundo donde nació MIDI Maze. Rápido, no te pares. 

10s -->

---

## MIDI Maze (1987): the FPS's grandfather

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
Presenta la pieza sobre la que gira toda la charla y dale PESO: MIDI Maze (1987) es anterior a
Wolfenstein 3D (1992) y a Doom (1993) — el abuelo del shooter en primera persona, y ya tenía
multijugador en red (lo que hizo famoso a Doom) cinco años antes.
- Las caras sonrientes son los otros jugadores: ese es tu símbolo. Señala la cara que explota en la portada.
- Recorre el linaje de izquierda a derecha: todos son FPS conocidísimos y todos vienen de este juego de
  Atari ST que casi nadie conoce.

90s
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
El alcance: no fue una rareza de Atari — como Faceball 2000 llegó a consolas y portátiles de Nintendo
y Sega en los 90. Pero el ORIGINAL, el del anillo MIDI, fue el Atari ST (resaltado).
Menciona los casi-fue: estuvo a punto de ser título de Virtual Boy (NikoChan Battle).

45s
-->

---

## MIDI Maze, in motion

<div class="flex gap-10 items-center justify-center mt-2">

  <div class="flex flex-col gap-2" style="flex:none; width:230px">
    <img src="/mmjs-06-playing.png" alt="MIDI Maze gameplay (rebuilt in JS)" style="width:100%; border:1px solid var(--line); border-radius:5px; box-shadow:0 4px 12px rgba(0,0,0,0.16)" />
    <img src="/mmjs-01-mode-menu.png" alt="Solo game / Network game menu" style="width:100%; border:1px solid var(--line); border-radius:5px; box-shadow:0 4px 12px rgba(0,0,0,0.16)" />
  </div>

  <div class="flex flex-col items-center text-center" style="flex:none; width:330px">
    <img src="/qr-midimaze.svg" alt="QR — play MIDI Maze" style="width:260px; background:#fff; padding:12px; border:1px solid var(--line); border-radius:12px; box-shadow:0 8px 22px rgba(0,0,0,0.16)" />
    <div class="mt-2 text-xl"><span class="accent">midimaze.sidecartridge.com</span></div>
    <div class="mt-2" style="font-size:0.85rem; line-height:1.4">
      Rebuilt with <strong>Claude Code (Opus 5.8)</strong> from the C sources. Play <strong>Solo mode</strong> now — if it works for everyone, we'll try <span class="accent">network mode</span> later.
    </div>
  </div>

</div>

<!--
Acción: pídeles que escaneen el QR (midimaze.sidecartridge.com) y abran el juego EN EL MÓVIL, en modo Solo.
Cuéntalo: lo hemos recompilado con Claude Code (Opus 5.8) desde el código fuente en C original.
Señala la captura del menú —"Solo game / Network game"— y que jueguen un par de minutos en Solo.

Engánchalos: "si va bien para todos, al final probamos el modo en red juntos".
Ten una captura/vídeo local de respaldo por si falla el wifi.

60s
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
Mini-explicación para quien no lo haya visto nunca. Rápido y concreto: ordenador doméstico de 1985,
CPU 68000 (la de los primeros Mac y el Amiga), GUI de ratón (GEM) años antes de que la gente tuviera
Windows y —lo que nos importa— puertos MIDI IN/OUT de serie: por eso era la máquina de los músicos y
por eso MIDI Maze podía hacer red por MIDI.

Remata el chiste: "si tienes menos de 40, es más viejo que tú".

45s
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
ESTO es lo que vamos a romper. Recórrelo: el MASTER mete un FRAME y marca el tempo; cada ST lo lee por
su MIDI IN, escribe su propia posición y lo empuja por su MIDI OUT al siguiente — toda la vuelta y de
vuelta al MASTER. Una vuelta entera = un tick de juego. Sin servidor, sin switch: un anillo de cable
literal a 31.250 baudios.

Suelta la semilla: son bytes crudos de 8 bits, no estándar".

2 min
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
Modelo mental fácil: el ST está en capas, igual que una máquina que ya conocen. GEM ≈ la GUI;
GEMDOS (trap #1) ≈ el SO / syscalls; BIOS (trap #13) ≈ E/S de dispositivos de bajo nivel; XBIOS
(trap #14) ≈ drivers de hardware. Lo único que hay que recordar: un programa le pide cosas al SO
disparando un TRAP del 68000 — el "syscall" del ST. El MIDI vive abajo, en BIOS y XBIOS (resaltado);
las llamadas exactas van en la siguiente.

60s
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
El quid, en paralelo. IZQUIERDA (ST): el MIDI es el dispositivo 3 del BIOS, una línea serie tonta —
Bconout (trap #13) suelta cualquier byte, incluido el 0x00 (la marca de MASTER). DERECHA (PC): el SO
expone el MIDI como API de mensajes — WINMM de Win32. midiOutShortMsg recibe un mensaje empaquetado
(status + 2 bytes de datos), no bytes crudos; no existe llamada para "emitir un 0x00 suelto"
(midiOutLongMsg solo acepta SysEx válido F0..F7) y WINMM filtra lo no estándar.

Remate: la misma tarea es trivial en el ST e imposible por el stack MIDI del PC — por eso
necesitábamos que el SidecarT hablara en crudo.

75s
-->

---
layout: statement
---

# In 2026, people still<br>play it competitively

<!--
Golpe sorpresa: campeonatos en quedadas retro, 40 años después. Por eso merece la pena revivirlo en
red — hay comunidad viva. Corto.

30s
-->

---
layout: statement
---

# Let's break the ring<br>and rebuild it over <span class="accent">TCP/IP</span>

<!--
LA MALA IDEA. Di que en tu cabeza sonaba genial. Pausa. Es la tesis del proyecto y el motor cómico
("¿qué podría salir mal?").

30s
-->

---

## Who's this lady?

<div class="flex justify-center mt-3">
  <img src="/grace-hopper.jpg" alt="Who's this lady?" style="height: 400px; background:#fff; padding:8px; border:1px solid var(--line); border-radius:8px; box-shadow:0 8px 22px rgba(0,0,0,0.18)" />
</div>

<div class="text-center manual-cap mt-3">No Googling. Shout it out.</div>

<!--
GANCHO con el público antes de hablar de herramientas. Es GRACE HOPPER — casi nadie la reconoce, y ese
es el truco. Revélalo tras una pausa y aterriza POR QUÉ está aquí: construyó el PRIMER COMPILADOR — el
primer salto HACIA ARRIBA en la escalera de abstracción; decidió que los humanos no deberían escribir en
código máquina.

LA HISTORIA (es la columna vertebral de toda la charla — cuéntala):
- Cuando propuso programación independiente de la máquina y traducción automática, muchos programadores
  y jefes lo vieron impracticable, hasta absurdo. No literalmente "los programadores de verdad usan
  ensamblador" (eso es moderno), pero el MISMO sentimiento: los ordenadores eran carísimos, la memoria
  mínima, los ciclos de CPU preciosos, se daba por hecho que el código máquina a mano era más eficiente,
  y "un compilador nunca generará código tan bueno como un buen programador".
- Le decían: "los ordenadores solo saben hacer aritmética; no pueden escribir programas".
- Su frase: "Tenía un compilador funcionando y nadie quería tocarlo. Me explicaban con paciencia que los
  ordenadores solo sabían hacer aritmética."

EL REMATE — el mismísimo argumento se repite desde hace 70 años:
  código máquina → ensamblador → FORTRAN → C → C++ → Java → Python → código generado por IA.
En cada peldaño, algunos expertos juraban que "los buenos usan la capa de abajo" — y cada vez el software
subió igualmente, porque la productividad pesaba más que el control de bajo nivel.

LA IRONÍA (pega fuerte con público retro/embebido): hoy hasta los de ensamblador confían en compiladores
de C optimizadores, y el código generado suele ganar al hecho a mano salvo en lo más crítico. La batalla
que dio Hopper en los 50 ES la misma que se libra hoy con la programación asistida por IA. De eso va esta
charla. Enlaza: "hoy hay una capa nueva encima — vamos a conocer al reparto" → ingredientes / reparto IA / escalera.

60-75s
-->

---

## The ingredient list of doom

- Atari ST: 40-year-old hardware
- MIDI Maze: 68000 assembly
- SidecarTridge Multi-device (The SidecarT) — RPi Pico W / RP2040
- 68000 assembly, C and Python on top
- Codex, Claude Code, Copilot, NotebookLM
- One señor from Logroño

<div class="mt-8 text-2xl">Spoiler: <span class="accent">everything</span> went wrong.</div>

<!--
El reparto del desastre. Remata "Spoiler: todo salió mal" como golpe final. La lista también adelanta
la escalera de abstracción que vamos a subir.

60s
-->

---

## The AI cast

- **OpenAI · Codex / ChatGPT 5.4 & 5.5** — Codex optimised the microfirmware & **TPROTOCOL** (C + 68000); ChatGPT — research & architecture drafts
- **Anthropic · Claude Code 5.7 & 5.8** — solution coding… and this presentation ;-)
- **GitHub Copilot** — code reviews
- **Google NotebookLM** — the librarian: Atari reference books + the MIDI-Maze-to-PC reverse-engineering TFG by **Jesús Ángel González Gorrado**

<!--
Presenta las herramientas de IA — el reparto del proyecto. OJO: en el Acto 3 calificamos a la IA por
NIVEL de abstracción (cuatro personalidades — becario / contratista / sénior / arquitecto, por peldaño),
NO herramienta por herramienta; así que no prometas que estos nombres concretos vuelven como las personalidades.
Papeles: Codex para optimización de bajo nivel (firmware/TPROTOCOL, C y 68000); ChatGPT para investigación
y diseño de arquitectura; Claude Code para el código de la solución (y esta presentación); Copilot para
revisiones; NotebookLM como bibliotecario con fuentes: los libros de Atari y el TFG de la UNIZAR
(ingeniería inversa de MIDI Maze para PC) de Jesús Ángel González Gorrado.

75s
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
LA ESCALERA — primera aparición (el mapa). Solo los cuatro niveles en los que trabajamos, de arriba
(Research / arquitectura) hasta el metal (ensamblador 68000). AÚN sin notas: cómo le fue a la IA en cada
peldaño es el "sorpresón" del Acto 3 (la misma escalera, ya calificada). También fija el lenguaje de
"peldaño" que usamos en el Acto 2.

30s
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
El baño de realidad del "Research mode". ChatGPT 5.4/5.5 en modo investigación no pillaba el punto al
pedirle la arquitectura de MIDI Maze sobre IP: insistía en un aparato de capa física cableado a los
puertos DIN MIDI; aunque le decías que usara el SidecarT, lo cableaba a los puertos MIDI; y cuando le
decías que atrapara el MIDI en firmware, sobre-ingenierizaba. El QR lleva a la sesión de research completa.
POR QUÉ (la caja de diagnóstico): se parece al ANCHORING (anclaje) — el modelo trata su primera
arquitectura como un hecho (ya forma parte del contexto) y hace búsqueda LOCAL: edita el diseño existente
en vez de re-derivarlo desde los requisitos + las pistas nuevas. Variantes: persistencia de creencia
("tienes razón, el bus sobra… pero dejamos el bus y lo simplificamos"); inercia del contexto / dependencia
de la trayectoria (20 páginas de conversación tiran); histéresis (la salida depende del historial, no solo
de los requisitos finales). Pasa porque en el entrenamiento se premia ser consistente con el texto previo
y NO descartar trabajo — y porque optimiza completitud/cobertura/robustez en vez de los criterios del
experto (simplicidad, coste operativo, acoplamiento, modos de fallo, mantenibilidad).
Resultado: técnicamente correcto, operativamente absurdo (la propuesta real — 16 placas hijas MIDI
optoacopladas + un servidor de anillo en Linux + un Gantt de 3 meses — para mover bytes que el SidecarT
ya transporta; ver la siguiente). Por eso en el Acto 3 la escalera califica Research como ILUSIÓN
("looks brilliant ⚠"), no como brillante.

90s
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
EL PAGO de la slide de anclaje — y la que resuelve la tensión de la escalera. Esto es la salida REAL de
"deep research" que dio ChatGPT al pedirle la v1 MÁS SIMPLE para correr MIDI Maze original por una LAN:
mantener los puertos MIDI físicos y FABRICAR HARDWARE — 16 placas hijas MIDI optoacopladas (6N138,
level-shifters de 5 V, bucles de 220R) soldadas a la UART de debug del SidecarT — más un AP de 2,4 GHz
dedicado, un "servidor de anillo" central en Linux, un protocolo TCP con cabeceras y CRC16/CRC32 + números
de secuencia, heartbeats/telemetría, un TSR de Atari con catálogo de comandos, jitter buffers, una matriz
de validación y un Gantt de 3 meses con una BOM ×16. Cada pieza se defiende sola; el conjunto es absurdo —
porque el SidecarT YA mueve los bytes por su puerto de cartucho en firmware, así que la solución final no
necesitaba hardware nuevo. "Nothing is wrong. Everything is unnecessary."
LA IDEA FUERTE: en el peldaño de Research/arquitectura la IA PARECE la más competente — y esa es la trampa.
Esa competencia es una ilusión que aguanta solo hasta que la revisa un experto; cuanto más alta la
abstracción, MÁS importa la verificación humana. Se paga en "saber cuándo se equivoca / qué no construir".

75s
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
MOMENTO DE PÚBLICO — guiño al lema ("Too old for this sh*t") y a la propuesta de las 16 placas hija que
acabamos de ver. Suelta la confesión en seco, deja que respire, y LUEGO haz la pregunta de manos —
espera de verdad a que levanten la mano. Es el momento de conectar con la sala: todo ingeniero con
experiencia ha heredado una catedral que debía ser una caseta. Aterriza el dolor compartido, pilla quizá
una batallita rápida del público, y gira: lo que nos salvó de la suya (y de la de ChatGPT) es lo mismo —
experiencia, criterio, saber qué NO construir. Esa es la ventaja humana de la que va el resto de la charla.
Suelto y relajado; es un respiro antes de volver a bajar peldaños.

60-90s
-->

---
layout: fact
---

# Our turn.

We guide it ourselves — one rung at a time. <span style="opacity:0.6">(the metal's still down there; we'll be back.)</span>

<!--
Hito + pivote. Conecta la lección del exceso de ingeniería ("hay que guiar la research; la IA no
simplifica sola") con el montaje práctico del ACTO 2. "Our turn" = dejamos de pedirle catedrales al
chatbot y construimos la caseta nosotros, peldaño a peldaño. El paréntesis adelanta la subida (68000 /
C / Python). Quien se haya despistado en el desvío de IA puede reengancharse aquí.

15s
-->

---
layout: section
---

<span class="act-num">ACT 2 · 2026</span>

# Faking the MIDI ring

<div class="recap">Make every ST believe the cable ring is still there.</div>

<!-- Separador + recap. Acto 2 = el plan + el montaje: presenta el SidecarT y el objetivo del
"orquestador de anillo" ANTES de la arquitectura, y luego sube los peldaños. 

10s -->

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

<div class="h-full flex flex-col items-center justify-center text-center">
  <img src="/sidecart-board.png" alt="SidecarT board" style="width: 268px; background:#fff; padding:8px; border:1px solid var(--line); border-radius:6px; box-shadow:0 6px 16px rgba(0,0,0,0.16)" />
  <div class="manual-cap mt-2">SidecarT · RP2040 + Wi-Fi</div>
</div>

<!--
Presenta el cacharro ANTES de la arquitectura. EL ENCUADRE: lo llaman "emulador de ROM", pero en realidad
es una herramienta de desarrollo que le pone un cerebro moderno al ST — un coprocesador raro. Es un
cartucho con RP2040 + Wi-Fi; el ST no puede escribir en el cartucho (bus de solo lectura), así que se
hablan por TPROTOCOL mediante lecturas de ROM. Credibilidad: 2.200+ unidades fabricadas y ~200–400 clones
— producto real que se vende, no una protoboard. Y es abierto: firmware GPL, hardware CC (no comercial) —
dilo en voz alta ante un público open source. Hoy lo reutilizamos como puente MIDI-a-red.

60s
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
  <text class="srv-t" x="370" y="170" text-anchor="middle">Orchestrator</text>
  <text class="srv-s" x="370" y="187" text-anchor="middle">TCP/IP · Python</text>
</svg>

<div class="text-center" style="font-size: 0.82rem; color: var(--ink-soft)">
  <span style="color: var(--accent)">┄ virtual ring (logical)</span> &nbsp;·&nbsp; — real TCP/IP, every node to the orchestrator
</div>

<div class="text-center mt-1" style="font-size: 0.95rem">
  To each ST it must look <strong>exactly</strong> like 1987 — same bytes, same order. We just move the wire to the Internet.
</div>

<!--
EL OBJETIVO, antes del diseño detallado. Físicamente es una ESTRELLA (cada SidecarT se conecta a un
servidor TCP/IP, el "orquestador de anillo"); lógicamente es el mismo ANILLO que en 1987 — el orquestador
pasa cada frame de nodo a nodo en orden de anillo. La restricción dura: MIDI Maze y el ST quedan 100% sin
tocar; para ellos tiene que ser byte a byte el viejo anillo de cable. Siguiente: cómo encajan las piezas.

75s
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
EL diagrama que hace clic en todo el proyecto. Recórrelo de izquierda a derecha UNA vez:
1. MIDI Maze llama a BIOS/XBIOS para sacar bytes MIDI; un hook XBRA atrapa esas llamadas y las
   redirige — en vez de al puerto MIDI, salen por el puerto de cartucho.
2. Por el cartucho viajan dentro de TPROTOCOL. El microfirmware del SidecarT (RP2040) desenvuelve
   TPROTOCOL, deja los bytes MIDI intactos y los reenvuelve en TCP/IP.
3. El servidor TCP/IP es el casamentero: cada SidecarT se conecta a él y enruta cada paquete al
   SidecarT destino correcto.
4. En el otro extremo, lo inverso — TCP/IP → TPROTOCOL → cartucho → hook XBRA → MIDI Maze. Ningún ST
   se entera de que el anillo se volvió Internet.
FRASE CLAVE: el contenido MIDI nunca cambia; solo cambia el sobre que lo envuelve.
Cada Atari ST y cada SidecarT corren el MISMO stack (es un diagrama de arquitectura, no de secuencia).
El arco discontinuo de arriba es el quid: todos los nodos juntos forman UN anillo MIDI virtual — el bucle
de cable de 1987, cerrado por software. El casamentero/enrutador del centro es un servidor TCP/IP en Python.

2.5 min
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
El mecanismo que hace posible todo el proyecto. XBRA ("eXternal BRanch Array") es la forma estándar de la
comunidad para encadenar de forma cooperativa un vector de sistema del 68000 en el ST: justo antes de tu
handler colocas 3 longwords — la marca 'XBRA', un cookie de 4 caracteres que te identifica y 'oldp' = el
handler que desplazaste. Se instala con Setexc (XBIOS): guardas el vector antiguo en oldp y apuntas el
vector a tu handler; el cookie + oldp permiten recorrer y quitar la cadena luego.
CLAVE: MIDI Maze llega al puerto MIDI por las DOS capas, así que enganchamos los DOS vectores — trap #13
(BIOS: Bconin/Bconout/Bconstat en el dispositivo 3) Y trap #14 (XBIOS: Midiws, y la lectura de MIDI-IN que
usa para detectar el MASTER). Cada handler mira si la llamada es MIDI; si lo es, mandamos los bytes por el
cartucho al SidecarT (TPROTOCOL); si no, jmp a oldp y el resto del SO queda intacto. Efecto neto: MIDI
Maze, sin tocar nada, cree que sigue hablando con su puerto MIDI. (Los offsets de pila son ilustrativos —
los reales tienen en cuenta el trap frame.)

2 min
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
SOLO LA PRIMERA SUPOSICIÓN — sin spoilers aquí. MIDI Maze es de verdad lock-step (restricción C-01): cada
byte de MIDI OUT se responde con una lectura IN síncrona, y ese lock-step ES el reloj de frame. Así que la
suposición fiel fue: retransmitir cada byte por el puente, en orden, con handshake de confirmación —
reproducir el cable exacto. Mecanismo (la build candidata): cartucho de solo lectura, así que el Pico
emula ROM y espía las lecturas de ROM3 con un anillo PIO+DMA; el intercambio va por TPROTOCOL — el canal
de comandos del SidecarT, hecho para transferencias síncronas de buffers de varios KB y comandos, así que
cada byte arrastra mucha fontanería; TCP con lwIP hasta el orquestador; ~4.800 líneas de C + PIO.
NO reveles aquí que ese handshake por byte salió 3× demasiado lento — esa colisión y el arreglo por
streaming son el giro "la realidad muerde → La Arquitectura Final" del final del Acto 2.

75s
-->

---

## Rung: Python (the glue)

- The **ring orchestrator** — a Python **asyncio** TCP server wiring every node into a ring
- First version is **smart**: master election, flow-control, match coordination
- Plus **self-test harnesses** & packet inspection — write fast, throw away fast
- The layer **furthest from the metal**

<!--
Peldaño 3 — solo la primera versión en Python (de md-MIDI2IP). El orquestador (orchestrator.py, servidor
TCP asyncio) acepta cada nodo y los conecta en anillo; en esta primera versión es el "listo" — elección de
MASTER, control de flujo, coordinación de partida. Más arneses de self-test e inspección de paquetes. Lo
más lejos del metal — la preparación del pago del Acto 3.
OJO: no menciones Hatari / la hatari-gateway aquí — se introduce DESPUÉS para justificar la v2. Y no
reveles que luego al orquestador lo dejamos en un simple relay — eso es la sorpresa.

60s
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
EL BUG que motiva la V1++. Con un solo ST real, la candidata no forma anillo: el nodo no gana MASTER de
forma fiable, la partida no arranca y MIDI Maze a veces suelta su propio error — literalmente "MIDI-ring
booh-booh". Un anillo necesita más de un nodo creíble. Así que añadimos un compañero que SABEMOS correcto
— siguiente: Hatari por la gateway.

45s
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
V1++ = la Arquitectura Candidata con un añadido: un compañero por software. El emulador de Atari ST,
Hatari, no habla TCP directamente, así que la hatari-gateway (una herramienta Python de md-MIDI2IP que
puentea el MIDI de Hatari por FIFOs de fichero hacia TCP/IP) lo conecta al orquestador — y pasa a ser un
nodo más del anillo. Por qué importa: puedes desarrollar e incluso jugar sin tener dos Atari ST físicos.
Esto prepara la v2 (iteración rápida, pasada de pruebas en hardware).

75s
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
EL GIRO — ahora que el anillo funciona de verdad (V1++ con el peer Hatari), lo medimos y salen DOS
problemas distintos. (1) VELOCIDAD: el handshake por byte de TPROTOCOL va a ~970 B/s en el camino
SidecarT + ST REAL — 3× MÁS LENTO que el cable de 1987 (3125) porque cada byte cruza el cartucho en
lock-step. Y ojo: esto NO pasa en el peer Hatari + hatari-gateway — ese va a toda la velocidad de la
emulación MIDI de Hatari — así que el cuello de botella es el puente hardware, no la idea. (2) CORRECCIÓN:
el orquestador "listo" (elección de MASTER, etc.) se construyó sobre una LECTURA EQUIVOCADA del protocolo
MIDI sacada del TFG (la lógica de 0x00=MASTER); no necesitamos nada de esa listura — solo un relay rápido
que MIRA los bytes (peek), nunca los parsea. Ambos arreglos aterrizan en La Arquitectura Final.

70s
-->

---

## The Final Architecture V2 — the fixes

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
LA RECOMPENSA. Tres iteraciones de md-MIDI2IP (Iteración 2) convirtieron la Candidata en algo que funciona:
(1) EPIC-09 — fuera el handshake por byte de TPROTOCOL; en su lugar, un stream fire-and-forget sobre el
anillo ROM3 de commemul (bit-8 OUT, bit-9 IN + confirm-ack); esto mata el techo de ~970 B/s que la hacía
3× más lenta que el cable de 1987. (2) EPIC-11 — el RingState del orquestador "listo" era una heurística de
elección de MASTER basada en una MALA LECTURA del protocolo MIDI (provocaba un cambio de MASTER en
hardware); fuera → un relay tonto que nunca parsea, más telemetría del anillo en vivo. (3) EPIC-10 —
validar una partida real de 2 jugadores en STs de verdad, con un self-test automático de por medio.
Encuadre honesto: la v2 quita el techo artificial del handshake y deja el maze jugable por IP en hardware
real — el objetivo era paridad/jugabilidad, no correr más que el cable. El peer Hatari + hatari-gateway
(visto en V1++) es lo que nos dejó iterar tan rápido.

90s
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
EL MISMO diagrama que V1++, evolucionado a v2 (resaltado en color + brillo). Qué cambió: (1) las dos cajas
puente del SidecarT pasan del camino de comandos síncrono "TPROTO ⇄ TCP/IP" a un stream fire-and-forget
"stream ⇄ TCP/IP" sobre el anillo commemul (los saltos entre nodos ahora se animan como un stream; bit-8 =
byte OUT, bit-9 = avance IN + confirm-ack). (2) el orquestador baja de "router de anillo listo" a "relay
tonto" que solo mira (peek), nunca parsea, más telemetría en vivo. El hook XBRA, el camino MIDI del ST
intacto y el peer Hatari por software siguen IGUAL que en V1++ — solo se movieron las piezas que brillan.
Son las tres victorias de la slide anterior, vistas en el cableado.

60s
-->

---
layout: fact
---

# One project,<br>four decades of tools

<!-- Hito. Repite la tesis: el proyecto es una máquina del tiempo que recorre la escalera. 

20s -->

---
layout: section
---

<span class="act-num">ACT 3</span>

# AI vs the ladder

<div class="recap">Previously: 1986 metal → 2026 rebuild. Now the payoff.</div>

<!-- Separador hacia el corazón de la charla. "10s" -->

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
LA IDEA CENTRAL + EL SORPRESÓN. Esta es la que fotografían. DOS modos de fallo, no uno: cerca del metal
(C, ensamblador 68000) falla VISIBLEMENTE — improvisa y lo pillas al instante. Arriba (Research/arquitectura)
falla INVISIBLEMENTE — fluido, completo, sobre-ingenierizado, y PARECE brillante, así que los errores cuelan
salvo que lo verifique un experto (guiño a la slide de la "ilusión"). De ahí el peldaño Research en verde
discontinuo: parece sólido, no lo es. El punto que lo une va contra el relato de "la IA sustituye a los
ingenieros": el peligro no está solo donde es débil, sino donde es *convincente*. El criterio/la verificación
humana es la habilidad duradera. Deja que cale.
"2 min"
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
"Improvising so it doesn't get fired" — el momento más gracioso y citable. TRES fallos reales del trabajo
en 68000 de este proyecto (target/atarist/src/userfw.s): (1) usa instrucciones de 680x0 que el 68000 pelado
del ST no tiene; (2) escribe en espacio de ROM una y otra vez aunque le dijiste en las guías que la ROM es
de solo lectura; (3) sobre-complica — p. ej. salta a una etiqueta compartida solo para ejecutar un rte,
cuando el handler limpio es literalmente "move.l MIDI_IN_STATUS,d0 / rte" en línea (antes→después real del
commit 3d0e422 → actual). CLAVE: estos fallan ALTO — no ensamblan o petan en hardware, así que los pillas
rápido (poco peligro; contrasta con el arquitecto). COROLARIO: no te libras prompteando — hay que iterar el
código generado, revisión tras revisión, hasta que esté bien.
"90s"
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
EL REENFOQUE del peldaño C. Contraintuitivo pero cierto: con el andamiaje adecuado, la IA escribe C
*precioso*. (1) Buen C a la primera; un par de iteraciones y queda optimizado. (2) El peligro real en un
micro es el testeo/validación, no escribir. (3) Por eso pre-construí el arnés — un framework de microfirmware
+ una skill de Claude que programa dentro de su sandbox (hecho meses antes, a propósito). (4) Resultado:
precisión de francotirador, válido, sin cuelgues, muy productivo. EL GIRO: nada de eso salvó la cosa, porque
el fallo no era el código — era el SPEC. El diseño de comandos síncronos de TPROTOCOL (el cuello de botella
de la v1) estaba mal, y la IA construyó fielmente, impecablemente, lo equivocado. Código impecable / spec
fatal. Este es el puente: el fallo subió de código (asm) a spec — y los specs vienen de arriba (→ el
arquitecto). Spec basura entra, basura impecable sale. CONTRASTE CLAVE con la Personalidad 1: allí el bucle
es sobre el CÓDIGO; AQUÍ el código ya está bien — el bucle que hay que correr es sobre el SPEC. Lo que iteras
sube por la escalera con el fallo.
"90s"
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
EL PICO DE LA DELEGACIÓN. Arriba de la escalera, en un lenguaje moderno de alto nivel, la IA está en su
mejor momento: (1) no hace falta prescribir framework/librería — del spec elige un buen diseño; (2) el
código es impecable; (3) es trivialmente testeable (un arnés de tests es fácil — al revés que C en el micro
o asm en el ST); (4) así el bucle se vuelve TOTALMENTE AGÉNTICO — escribe, testea, arregla y reintenta hasta
verde, comprobaciones de validez automatizadas, sin manos. (5) Y de nuevo el límite era el SPEC, no el
código — pero aquí el conjunto de tests destapa los fallos del spec rápido. EL APRENDIZAJE: con specs buenos
y estructurados puedes delegar la mayor parte del trabajo a la IA agéntica; lo irreductiblemente tuyo es el
spec + el criterio. LA PREPARACIÓN de P4: "el spec / la arquitectura" es justo lo que NO puedes delegar —
porque ahí la competencia es una ilusión. Aquí se gana tu confianza, y eso es lo que el arquitecto explota
después.
"75s"
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
EL PAGO de toda la escalera (guiño a las slides de la ilusión + la subida P1→P3). El fallo ha ido subiendo:
código (becario) → spec (contratista) → y el spec/la arquitectura se escriben AQUÍ. Así que el spec
equivocado de "comandos síncronos" que hundió a C y a Python nació en ESTE peldaño. El fallo es INVISIBLE:
nada peta, ni un opcode inventado — solo un diseño fluido, citado y sobre-ingenierizado que implementas
impecablemente y envías. Y como se lee igual que el sénior en quien acabas de confiar (y al que acabas de
delegar todo, P3), bajas la guardia — justo cuando es más peligroso. EL PUNTO: P3 decía "delega todo menos
el spec + el criterio". Esto es POR QUÉ — el único peldaño que no puedes ceder es la arquitectura, porque
ahí la competencia es una ilusión que solo pilla un experto. Este es EL hallazgo de la charla. Déjalo caer
en seco.
"90s"
-->

---
layout: statement
---

# The intern improvises.<br>The architect over-engineers.<br>Both sound <span class="accent">certain</span>.

<div class="mt-6 text-2xl">The dangerous one is the architect — because it's the one you <strong>believe</strong>.</div>

<!--
EL LEMA (sustituye a "sénior brillante / becario confiado"). Todo el acto en una frase: no es tonto-abajo /
listo-arriba — es poco fiable en AMBOS extremos, y más peligroso justo donde más convence. Dilo, pausa, y
luego la frase remate. El asa que repetirán a un colega.
"30s"
-->

---

## Working with AI<br>(without losing faith in humanity)

- **Build the sandbox first** — your highest-leverage work is the *harness*: a framework + tests that let the AI code safely and prove itself
- **Delegate the loop, own the spec** — with good, structured specs, hand the whole code loop to agentic AI; keep the spec, the architecture, the judgment
- **Iterate the right layer** — down low you iterate the *code*; up high you iterate the *spec*. Match the fix to the failure
- **Distrust the most polished answer** — verify hardest where it's most convincing; ground it in sources (NotebookLM on primary docs beats a model's memory)

<div class="mt-6 text-2xl">You stay the engineer. It's the <span class="accent">buddy</span>, not the boss.</div>

<!--
EL MANUAL PRÁCTICO — destilado del Acto 3, por orden de palanca:
(1) CONSTRUYE EL SANDBOX — el movimiento humano que lo desbloqueó todo: un framework de microfirmware + una
    skill de Claude para que la IA programe en una caja segura y testeable (P2/P3). Aquí es donde TÚ aportas más.
(2) DELEGA EL BUCLE, QUÉDATE EL SPEC — con specs buenos y estructurados, la IA agéntica corre
    escribe→testea→arregla sola (P3); lo que conservas es el spec, la arquitectura, el criterio — lo que la IA finge (P4).
(3) ITERA LA CAPA CORRECTA — lo que iteras sube con el fallo: código en el metal (P1), spec más arriba (P2).
    No vuelvas a promptear código cuando lo roto es el spec.
(4) DESCONFÍA DE LA RESPUESTA MÁS PULIDA — la ilusión del arquitecto (P4): verifica más fuerte donde más
    convence; haz que cite fuentes primarias (NotebookLM) en vez de fiarte de su memoria.
La frase final es la nota humana que justifica el título — colega, no jefe. Prepara el demo + el cierre.
"90s"
-->

---
layout: statement
---

# Demo time! 🕹️

<div class="mt-4 text-2xl">MIDI Maze, multiplayer, <span class="accent">over IP</span> — live on real hardware.</div>

<div class="flex flex-col items-center mt-6">
  <img src="/qr-midimaze.svg" alt="QR — join the game" style="width:220px; background:#fff; padding:12px; border:1px solid var(--line); border-radius:12px; box-shadow:0 8px 22px rgba(0,0,0,0.16)" />
  <div class="mt-3 text-xl"><span class="accent">midimaze.sidecartridge.com</span> · join in <strong>Network mode</strong></div>
</div>

<!--
DEMO EN VIVO — cambia al montaje: Atari ST real(es) + puente(s) SidecarT + el orquestador, MIDI Maze
jugando en multijugador sobre TCP/IP. Acción: di al público que escaneen el QR (midimaze.sidecartridge.com)
y entren en modo Red (Network) para jugar contra nosotros. Ten un vídeo grabado a mano como respaldo por si
el montaje o el wifi fallan (Winston: controla el riesgo). Incluye el tiempo de montaje.
"2-3 min"
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
    <span class="era__year">1986</span>
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
ZOOM-OUT, justo antes del cierre. El proyecto funcionó (slide anterior) — pero la historia de verdad es
cómo cambió *construir* en sí. El bucle es Código → Build & Reload → Test → Inspeccionar → Commit; cada
vuelta te da exactamente UNA inspección — una oportunidad de aprender — así que la métrica es cuántas vueltas
te puedes permitir. LA MÉTRICA FUNDAMENTAL: vueltas (iteraciones) para sacar una feature, y no para de
encogerse — X(1986) > Y(2023) >> Z(2026): hacían falta ~40 vueltas en 1986, ~12 en 2023 (mejores
herramientas/frameworks/conocimiento hacen más por vuelta), ~3 en 2026 — porque el agente PLIEGA muchas
iteraciones humanas en su propio bucle interno. Dos dimensiones por era: vueltas/feature Y tiempo/vuelta
(los tiempos por paso son representativos — compilar/enlazar en floppy ≈ minutos; HMR moderno ~instantáneo,
se nota >15s; codificación agéntica ≈ 8–48 min/tarea multi-iteración, NO la latencia de ~8s de una sola
llamada; ajusta a tus números). Revela de uno en uno (un clic):
  1986: ~40 vueltas × ~24 min/vuelta ≈ 2 días/feature — domina compilar/enlazar en floppy; vueltas tan caras que optimizas para NO fallar.
  2023: ~12 vueltas × ~20 min/vuelta ≈ 4 h/feature — pasos mecánicos ~0, así que tu propio código es la vuelta; menos vueltas, falla rápido.
  2026: ~3 vueltas ≈ 1 h de TU tiempo — el bucle no se hizo más rápido, se MOVIÓ: el agente machaca muchos
  intentos por dentro (10–40 min), plegando lo que eran varias iteraciones humanas en una. Dejas de teclear;
  todo tu coste pasa a ser REVISAR → el criterio es el cuello de botella. No vendas velocidad; lo honesto es:
  menos vueltas, pero más pesadas para el humano.
Enlaza directo con "Qué te llevas a casa": la habilidad duradera es saber cuándo se equivoca.
GANCHO: en este proyecto estuve en las tres eras a la vez — 2026 en Python, ~2023 en C, aún 1986 en
ensamblador 68000. La era no es la fecha; es el nivel de abstracción.
"2 min"
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
LA ÚLTIMA SLIDE DE CONTENIDO (Winston: termina en aportaciones/conclusiones, NO en "gracias").
Es la espina 1986 → 2023 → 2026 → futuro. La fila del futuro es TU predicción — reescríbela con tus palabras.
RESALTA el banner "deletions, not additions" — es el pago de la slide V2 (ganamos arrancando el handshake por
byte Y el orquestador listo, no añadiendo virguería). Átalo al criterio: la IA abarata escribir código, así
que la palanca pasa a saber qué quitar / qué no construir. Dilo despacio; es lo que se llevan a casa.
"2 min"
-->

---
layout: center
class: cover-slide
---

<div class="maze-smiley" aria-hidden="true"></div>

# Still too old for this <span class="accent">sh*t</span>

<div class="byline">
  Diego Parrilla · sidecartridge.com · @sidecartridge · @soyparrilla<br>
  github.com/sidecartridge/md-MIDI2IP
</div>

<!--
PALABRAS FINALES = chiste / guiño (Winston: que se rían al salir, nunca terminar en "gracias"). Enlaces
pequeños. Luego, preguntas.
"20s"
-->
