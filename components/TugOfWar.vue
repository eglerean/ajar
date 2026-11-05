<script setup lang="ts">
import { computed } from 'vue'

/**
 * Tug of war from slide 3 of the compact deck: integrity pulls towards open,
 * privacy pulls towards closed; AI stands behind integrity, cybersecurity behind privacy;
 * the marker in the middle is "your decision".
 *
 *   <TugOfWar />                                     full diagram (slide 3)
 *   <TugOfWar mini active="privacy" />               corner icon, one part highlighted
 *   <TugOfWar mini :active="['ai', 'integrity']" />
 *
 * Parts: integrity, privacy, ai, cyber, decision.
 * Use the mini version inside <div class="corner-icon"> (style.css).
 */
const props = defineProps({
  active: { type: [String, Array], default: () => [] },
  mini: { type: Boolean, default: false },
})

const activeSet = computed(() => new Set(Array.isArray(props.active) ? props.active : [props.active]))
function cls(part: string) {
  // Full diagram: everything in colour. Mini: only the active parts.
  return props.mini && !activeSet.value.has(part) ? 'tw-off' : `tw-${part}`
}
</script>

<template>
  <!-- Corner icon -->
  <svg v-if="mini" class="tw-mini" viewBox="0 0 164 64" role="img"
    :aria-label="`Tug of war between integrity and privacy, active: ${[...activeSet].join(', ')}`">
    <line x1="66" y1="32" x2="98" y2="32" class="tw-rope" />
    <rect x="1" y="12" width="24" height="40" rx="5" :class="cls('ai')" class="tw-back" />
    <rect x="28" y="4" width="38" height="56" rx="7" :class="cls('integrity')" />
    <rect x="98" y="4" width="38" height="56" rx="7" :class="cls('privacy')" />
    <rect x="139" y="12" width="24" height="40" rx="5" :class="cls('cyber')" class="tw-back" />
    <polygon points="82,20 74,34 90,34" :class="cls('decision')" />
    <text x="13" y="33" class="tw-l tw-ls">AI</text>
    <text x="47" y="33" class="tw-l">I</text>
    <text x="117" y="33" class="tw-l">P</text>
    <text x="151" y="33" class="tw-l tw-ls">C</text>
  </svg>

  <!-- Full diagram -->
  <svg v-else class="tw-full" viewBox="0 0 680 172" role="img"
    aria-label="Tug of war: integrity pulls towards open, privacy pulls towards closed. AI stands behind both integrity and privacy and adds risk on each side. The marker in the middle is your decision.">
    <!-- direction labels -->
    <text x="215" y="22" class="tw-dir" text-anchor="start">← towards open</text>
    <text x="465" y="22" class="tw-dir" text-anchor="end">towards closed →</text>
    <!-- rope -->
    <line x1="240" y1="105" x2="440" y2="105" class="tw-rope" />
    <!-- marker -->
    <polygon points="340,78 326,104 354,104" :class="cls('decision')" />
    <line x1="340" y1="104" x2="340" y2="132" class="tw-pole" />
    <text x="340" y="152" class="tw-mark">your decision</text>
    <!-- AI behind integrity -->
    <rect x="0" y="62" width="100" height="86" rx="12" :class="cls('ai')" class="tw-back" />
    <text x="50" y="100" class="tw-name">AI</text>
    <text x="50" y="122" class="tw-sub">adds risk</text>
    <!-- Integrity -->
    <rect x="110" y="48" width="130" height="114" rx="14" :class="cls('integrity')" />
    <text x="175" y="98" class="tw-name">Integrity</text>
    <text x="175" y="122" class="tw-sub">others must be</text>
    <text x="175" y="138" class="tw-sub">able to check</text>
    <!-- Privacy -->
    <rect x="440" y="48" width="130" height="114" rx="14" :class="cls('privacy')" />
    <text x="505" y="98" class="tw-name">Privacy</text>
    <text x="505" y="122" class="tw-sub">nobody harmed</text>
    <text x="505" y="138" class="tw-sub">by taking part</text>
    <!-- AI behind privacy (the mini icon still labels this part "C") -->
    <rect x="580" y="62" width="100" height="86" rx="12" :class="cls('cyber')" class="tw-back" />
    <text x="630" y="100" class="tw-name">AI</text>
    <text x="630" y="122" class="tw-sub">adds risk</text>
  </svg>
</template>

<style>
.tw-full { width: 100%; height: auto; }
.tw-rope { stroke: #8a6a3b; stroke-width: 7; stroke-linecap: round; }
.tw-mini .tw-rope { stroke-width: 5; }
.tw-pole { stroke: var(--asc-text); stroke-width: 2; }
.tw-ground { stroke: var(--asc-border); stroke-width: 2; stroke-dasharray: 6 6; }
.tw-integrity { fill: var(--aalto-blue, var(--asc-clay)); stroke: var(--asc-text); stroke-width: 2; }
.tw-privacy { fill: var(--aalto-red, var(--asc-clay)); stroke: var(--asc-text); stroke-width: 2; }
.tw-ai { fill: color-mix(in srgb, var(--aalto-blue, var(--asc-clay)) 35%, transparent); stroke: var(--asc-text); stroke-width: 1.5; stroke-dasharray: 5 4; }
.tw-cyber { fill: color-mix(in srgb, var(--aalto-red, var(--asc-clay)) 35%, transparent); stroke: var(--asc-text); stroke-width: 1.5; stroke-dasharray: 5 4; }
.tw-decision { fill: var(--aalto-yellow, var(--asc-sand)); stroke: var(--asc-text); stroke-width: 2; }
.tw-off { fill: none; stroke: var(--asc-muted); stroke-width: 1.5; opacity: 0.6; }
.tw-name { font-family: var(--asc-font-serif); font-weight: 700; font-size: 22px; text-anchor: middle; fill: #000; }
.tw-name-s { font-size: 17px; }
.tw-sub { font-size: 13px; text-anchor: middle; fill: #000; }
.tw-dir { font-size: 14px; font-weight: 600; fill: var(--asc-muted); }
.tw-mark { font-size: 15px; font-weight: 700; text-anchor: middle; fill: var(--asc-text); }
.tw-l { font-family: var(--asc-font-sans); font-size: 20px; font-weight: 700; text-anchor: middle; dominant-baseline: middle; fill: var(--asc-text); }
.tw-ls { font-size: 13px; }
/* The tug-of-war icon is wider than it is tall, so give it more room than the default 100px corner icon */
.slidev-layout .corner-icon:has(.tw-mini) { width: 130px; }
.slidev-layout:has(.tw-mini) h1 { padding-right: calc(130px + 0.5rem); }
</style>
