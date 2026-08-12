<script setup>
defineProps({
  direction: { type: String, default: 'to-paper' } // 'to-paper' | 'to-ink'
})
</script>

<template>
  <div
    class="torn-divider"
    :class="direction === 'to-paper' ? 'torn-divider--to-paper' : 'torn-divider--to-ink'"
  >
    <div class="halftone-fade"></div>
    <svg viewBox="0 0 1200 46" preserveAspectRatio="none">
      <path
        v-if="direction === 'to-paper'"
        d="M0,46 L0,18 L40,24 L82,10 L121,22 L163,6 L206,20 L248,9 L289,23 L332,12 L373,26
           L415,8 L458,21 L500,11 L542,25 L584,9 L626,22 L668,7 L710,20 L752,10 L794,24
           L836,9 L878,23 L920,11 L962,25 L1004,8 L1046,21 L1088,10 L1130,24 L1172,12 L1200,20
           L1200,46 Z"
        fill="var(--paper)"
      />
      <path
        v-else
        d="M0,46 L0,18 L40,24 L82,10 L121,22 L163,6 L206,20 L248,9 L289,23 L332,12 L373,26
           L415,8 L458,21 L500,11 L542,25 L584,9 L626,22 L668,7 L710,20 L752,10 L794,24
           L836,9 L878,23 L920,11 L962,25 L1004,8 L1046,21 L1088,10 L1130,24 L1172,12 L1200,20
           L1200,46 Z"
        fill="var(--ink)"
      />
    </svg>
  </div>
</template>
