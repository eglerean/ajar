<script setup lang="ts">
import { computed } from 'vue'

/**
 * The four-domain grid from slide 4: rows Integrity, Privacy, Cybersecurity;
 * columns Privacy, Cybersecurity, AI. Only the upper triangle has cells (6 intersections).
 *
 *   <DomainGrid full />                         slide 4: labelled cells that link to their slides
 *   <DomainGrid mini active="priv-ai" />        corner icon, one cell highlighted
 *   <DomainGrid mini :active="['int-cyb', 'priv-cyb']" />
 *
 * Cell keys: int-priv, int-cyb, int-ai, priv-cyb, priv-ai, cyb-ai.
 * Use the mini version inside <div class="corner-icon"> (style.css).
 */
const props = defineProps({
  active: { type: [String, Array], default: () => [] },
  mini: { type: Boolean, default: false },
  full: { type: Boolean, default: false },
})

const rows = [
  { key: 'int', label: 'Integrity', short: 'I' },
  { key: 'priv', label: 'Privacy', short: 'P' },
  { key: 'cyb', label: 'Cybersecurity', short: 'C' },
]
const cols = [
  { key: 'priv', label: 'Privacy', short: 'P' },
  { key: 'cyb', label: 'Cybersecurity', short: 'C' },
  { key: 'ai', label: 'AI', short: 'AI' },
]

// Examples and slide numbers from the slide plan (slide 4 table)
const cells: Record<string, { text: string, slides: number[] }> = {
  'int-priv': { text: 'Confidentiality promises shape the answers', slides: [8] },
  'int-cyb': { text: 'Tampering and provenance', slides: [5, 12] },
  'int-ai': { text: 'Disclosure vs documentation', slides: [14] },
  'priv-cyb': { text: '"Closed" data that leaks', slides: [12] },
  'priv-ai': { text: 'Cheaper re-identification, leaky models', slides: [15, 16] },
  'cyb-ai': { text: 'Agents and poisoned inputs', slides: [17] },
}

const activeSet = computed(() => new Set(Array.isArray(props.active) ? props.active : [props.active]))

function key(r: number, c: number) {
  return `${rows[r].key}-${cols[c].key}`
}

// Mini SVG geometry
const S = 22 // cell size
const G = 3 // gap
const O = 20 // offset for the axis letters
function x(c: number) { return O + c * (S + G) }
function y(r: number) { return O + r * (S + G) }
</script>

<template>
  <!-- Corner icon -->
  <svg v-if="mini" class="dg-mini" :viewBox="`0 0 ${O + 3 * (S + G)} ${O + 3 * (S + G)}`" role="img"
    :aria-label="`Four-domain grid, active: ${[...activeSet].join(', ')}`">
    <text v-for="(c, j) in cols" :key="'c' + j" :x="x(j) + S / 2" :y="O - 6" class="dg-axis">{{ c.short }}</text>
    <text v-for="(r, i) in rows" :key="'r' + i" :x="O - 6" :y="y(i) + S / 2" class="dg-axis dg-axis-row">{{ r.short }}</text>
    <template v-for="(r, i) in rows" :key="'row' + i">
      <template v-for="(c, j) in cols" :key="'cell' + i + j">
        <rect v-if="j >= i" :x="x(j)" :y="y(i)" :width="S" :height="S" rx="4"
          :class="activeSet.has(key(i, j)) ? 'dg-on' : 'dg-off'" />
      </template>
    </template>
  </svg>

  <!-- Full grid for slide 4 -->
  <div v-else class="dg-full">
    <div class="dg-corner" />
    <div v-for="c in cols" :key="'h' + c.key" class="dg-head">{{ c.label }}</div>
    <template v-for="(r, i) in rows" :key="'fr' + i">
      <div class="dg-rowhead">{{ r.label }}</div>
      <template v-for="(c, j) in cols" :key="'fc' + i + j">
        <div v-if="j < i" class="dg-empty" />
        <div v-else class="dg-cell" :class="{ 'dg-cell-on': activeSet.has(key(i, j)) }">
          <div class="dg-text">{{ cells[key(i, j)].text }}</div>
          <div class="dg-links">
            <a v-for="n in cells[key(i, j)].slides" :key="n" href="#" @click.prevent="$slidev.nav.go(n)">slide {{ n }}</a>
          </div>
        </div>
      </template>
    </template>
  </div>
</template>

<style>
/* Mini icon */
.dg-mini .dg-axis { font-family: var(--asc-font-sans); font-size: 11px; font-weight: 700; fill: var(--asc-muted); text-anchor: middle; dominant-baseline: middle; }
.dg-mini .dg-off { fill: none; stroke: var(--asc-muted); stroke-width: 1.5; opacity: 0.6; }
.dg-mini .dg-on { fill: var(--aalto-blue, var(--asc-clay)); stroke: var(--asc-text); stroke-width: 1.5; }

/* Full grid */
.dg-full { display: grid; grid-template-columns: 9rem repeat(3, minmax(0, 1fr)); gap: 0.4rem; }
.dg-full .dg-head, .dg-full .dg-rowhead { font-family: var(--asc-font-serif); font-weight: 600; font-size: 1rem; align-self: end; }
.dg-full .dg-head { text-align: center; padding-bottom: 0.1rem; }
.dg-full .dg-rowhead { align-self: center; }
.dg-full .dg-cell { display: flex; flex-direction: column; justify-content: space-between; min-height: 3.6rem; padding: 0.35rem 0.7rem; border: 2px solid var(--asc-border); border-radius: var(--asc-radius-md); background: var(--asc-surface); }
.dg-full .dg-cell-on { background: var(--aalto-blue, var(--asc-clay)); border-color: var(--aalto-blue, var(--asc-clay)); color: #000; }
.dg-full .dg-text { font-size: 0.85rem; line-height: 1.2; }
.dg-full .dg-links { margin-top: 0.15rem; font-size: 0.7rem; display: flex; gap: 0.5rem; }
.dg-full .dg-empty { border: 1px dashed var(--asc-border); border-radius: var(--asc-radius-md); opacity: 0.4; }
</style>
