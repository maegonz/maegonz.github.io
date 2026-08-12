<script setup>
const ticker = [
  'quantum circuits before hot chocolate',
  'reads papers with a pen, always',
  'currently reading Chainsaw Man at 1am',
  'believes Gojo is not optional',
  'IMT Nord Europe, final year',
  'will talk about Takeru Hokazono everytime',
]

const notes = [
  { title: 'Desk right now', body: 'DiGress and Cometh papers, one half-finished notebook, and, of course, the last season of Silo.' },
  { title: 'Current issue', body: 'Still trying to figure out how to make Sobol indices work on graphs' },
  { title: 'Go-to tool', body: 'PyTorch Geometric for anything graph-shaped.' },
  { title: 'Currently reading', body: 'Fire and Blood, alongside The Road to Dune.' },
  { title: 'Pet peeve', body: 'Black-box models with no attempt at explanation.' },
  { title: 'Currently learning', body: "How to make attribution methods (Sobol indices, EVA) hold up outside the paper's own benchmark, turns out 'explainable' is easy to claim and hard to earn." },
]
</script>

<template>
  <section id="dispatches" class="dispatches stock-ink">
    <div class="ticker" aria-hidden="true">
      <div class="ticker-track">
        <span v-for="(t, i) in [...ticker, ...ticker]" :key="i" class="ticker-item">{{ t }} •</span>
      </div>
    </div>

    <div class="page">
      <p class="volume-tag">Vol. 02 — Dispatches</p>
      <h2 class="dispatches-title slash-accent">Field notes</h2>

      <div class="sticky-grid">
        <article v-for="n in notes" :key="n.title" class="sticky-note">
          <h3>{{ n.title }}</h3>
          <p>{{ n.body }}</p>
        </article>
      </div>
    </div>
  </section>
</template>

<style scoped>
.dispatches {
  padding-bottom: 60px;
}

.ticker {
  overflow: hidden;
  border-top: 1px solid rgba(242, 230, 204, 0.18);
  border-bottom: 1px solid rgba(242, 230, 204, 0.18);
  background: var(--blood);
  padding: 10px 0;
}

.ticker-track {
  display: flex;
  gap: 28px;
  width: max-content;
  animation: scroll-ticker 26s linear infinite;
}

.ticker-item {
  font-family: var(--font-mono);
  font-size: 0.82rem;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: var(--paper);
  white-space: nowrap;
}

@keyframes scroll-ticker {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

.dispatches-title {
  font-family: var(--font-display);
  text-transform: uppercase;
  font-size: clamp(1.9rem, 4vw, 2.6rem);
  margin: 44px 0 26px;
}

.sticky-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 18px;
}

.sticky-note {
  background: var(--ember-soft);
  color: var(--ink);
  padding: 18px;
  border-radius: 2px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.35);
  transform: rotate(-2deg);
}

.sticky-note:nth-child(1) { transform: rotate(-2.5deg); background: #decda6; }
.sticky-note:nth-child(2) { transform: rotate(1.5deg); background: #e4c4c1; grid-row: span 2; }
.sticky-note:nth-child(3) { transform: rotate(-1.2deg); background: #cce3be; }
.sticky-note:nth-child(4) { transform: rotate(2.2deg); background: #decda6; }
.sticky-note:nth-child(5) { transform: rotate(-1.8deg); background: #cce3be; }
.sticky-note:nth-child(6) { transform: rotate(1.1deg); background: #e4c4c1; }

.sticky-note h3 {
  font-family: var(--font-hand);
  font-size: 1.35rem;
  margin: 0 0 6px;
  color: var(--blood);
}

.sticky-note p {
  margin: 0;
  font-size: 0.92rem;
  line-height: 1.5;
}
.sticky-note:hover {
  transform: rotate(0deg) translateY(-3px);
  transition: transform 180ms ease;
}

@media (max-width: 860px) {
  .sticky-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}
</style>
