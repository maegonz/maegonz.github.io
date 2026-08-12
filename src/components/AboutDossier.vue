<script setup>
const qa = [
  { q: 'Currently based', a: 'IMT Nord Europe, final year of my Master\u2019s.' },
  { q: 'Core obsession', a: 'Where quantum computing meets machine learning \u2014 what quantum structure can (and can\u2019t) buy a learning system.' },
  { q: 'Also fluent in', a: 'Graph neural networks, explainable AI, and Computer Vision' },
  { q: 'How I work', a: 'Literature review \u2192 study design \u2192 analysis \u2192 writing \u2014 methodologically sound, and readable by someone outside the field.' },
]
</script>

<template>
  <section id="about" class="dossier stock-paper">
    <div class="page">
      <p class="volume-tag">Vol. 01 — Dossier</p>
      <h2 class="dossier-title slash-accent">About the agent</h2>
      <span class="marginalia">the short version →</span>

      <div class="qa-grid">
        <div v-for="item in qa" :key="item.q" class="qa-row">
          <dt>{{ item.q }}</dt>
          <dd>{{ item.a }}</dd>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.dossier {
  padding: 56px 0 64px;
}

.dossier-title {
  font-family: var(--font-display);
  text-transform: uppercase;
  font-size: clamp(1.9rem, 4vw, 2.6rem);
  margin: 0 0 6px;
}

.qa-grid {
  margin-top: 30px;
  display: grid;
  gap: 0;
  border-top: 1px solid var(--paper-line);
}

.qa-row {
  display: grid;
  grid-template-columns: 220px 1fr;
  gap: 20px;
  padding: 18px 0;
  border-bottom: 1px solid var(--paper-line);
}

.qa-row dt {
  font-family: var(--font-mono);
  font-size: 0.78rem;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  opacity: 0.65;
}

.qa-row dd {
  margin: 0;
  font-family: var(--font-serif);
  font-size: 1.15rem;
  line-height: 1.5;
}

@media (max-width: 640px) {
  .qa-row {
    grid-template-columns: 1fr;
    gap: 6px;
  }
}
</style>
