<!-- Auto-registered by Slidev: persistent footer chrome on every slide. -->
<template>
  <footer class="deck-foot">
    <span class="deck-foot__title">MIDI&nbsp;MAZE&nbsp;/&nbsp;IP</span>
    <span class="deck-foot__bar" />
    <span class="deck-foot__num">
      {{ pad($slidev.nav.currentPage) }} / {{ pad($slidev.nav.total) }}
    </span>
  </footer>
</template>

<script setup>
const pad = (n) => String(n).padStart(2, '0')
</script>

<style scoped>
.deck-foot {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 34px;
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 0 24px;
  font-family: var(--font-pixel);
  font-size: 0.58rem;
  letter-spacing: 0.12em;
  color: var(--ink-soft);
  z-index: 10;
  pointer-events: none;
}
.deck-foot__bar {
  flex: 1;
  height: 0;
  border-top: 1px dashed var(--line);
}
.deck-foot__num {
  color: var(--accent);
}
</style>
