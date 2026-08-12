<script setup>
const papers = [
  {
    year: '2026',
    title: 'Spatio-temporal Transformer for Human Motion generation and action description',
    description: 'A look at how vision models fail under adversarial perturbation, and whether attribution methods can actually explain the failure rather than just describe it.',
    tags: ['Transformer', 'Spatio-temporal Attention', 'NLP', 'Diffusion process'],
    image: '/figures/human_motion_report_first_page.png',
    report: '/doc/human_motion_report.pdf',
    code: 'https://github.com/maegonz/Spatio-Temporal-Transformer-for-Human-Motion-tasks'
  },
  {
    year: '2026',
    title: 'Quantum GANs: Hybrid Architectures and Convergence Analysis',
    description: 'Pairing classical discriminators with parameterized quantum circuits, and asking whether the resulting generators actually converge faster than their fully classical counterparts.',
    tags: ['Quantum Computing', 'Generative Models', 'Hybrid Architectures'],
    image: '/figures/qgan_report_first_page.png',
    report: '/doc/qgan_report.pdf',
    code: 'https://github.com/maegonz/Quantum-GAN',
  },
]
</script>

<template>
  <section id="paper" class="latest stock-paper">
    <div class="page">
      <p class="volume-tag">Vol. 05 — Latest work</p>
      <h2 class="latest-title slash-accent">Reports from the field</h2>

      <article v-for="p in papers" :key="p.title" class="paper-row">
        <img :src="p.image" :alt="p.title" loading="lazy" class="paper-thumb" />
        <div class="paper-info">
          <span class="paper-year">{{ p.year }}</span>
          <h3>{{ p.title }}</h3>
          <p class="paper-desc">{{ p.description }}</p>
          <div class="paper-tags">
            <span v-for="t in p.tags" :key="t">{{ t }}</span>
          </div>
        </div>
        <div class="paper-actions">
          <a v-if="p.report" class="button button-primary" :href="p.report" target="_blank" rel="noreferrer">Report</a>
          <a v-if="p.code" class="button button-secondary" :href="p.code" target="_blank" rel="noreferrer">Code</a>
        </div>
      </article>
    </div>
  </section>
</template>

<style scoped>
.latest {
  padding: 60px 0 68px;
}

.latest-title {
  font-family: var(--font-display);
  text-transform: uppercase;
  font-size: clamp(1.9rem, 4vw, 2.6rem);
  margin: 0 0 30px;
}

.paper-row {
  display: grid;
  grid-template-columns: 168px 1fr auto;
  align-items: center;
  gap: 24px;
  padding: 20px 0;
  border-top: 1px solid var(--paper-line);
}

.paper-row:last-child {
  border-bottom: 1px solid var(--paper-line);
}

.paper-thumb {
  width: 150px;
  height: 220px;
  object-fit: cover;
  /* border: 2px solid var(--ink); */
  border-radius: 10px;
}

.paper-year {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  letter-spacing: 0.08em;
  color: var(--blood-deep);
}

.paper-info h3 {
  font-family: var(--font-serif);
  font-size: 1.2rem;
  margin: 4px 0 6px;
  line-height: 1.35;
}

.paper-desc {
  margin: 0 0 10px;
  font-size: 0.9rem;
  line-height: 1.55;
  color: var(--ink-soft);
  max-width: 58ch;
}

.paper-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.paper-tags span {
  font-family: var(--font-mono);
  font-size: 0.68rem;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  padding: 3px 8px;
  border: 1px solid var(--ink);
  border-radius: 999px;
  opacity: 0.7;
}

.paper-actions {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

@media (max-width: 720px) {
  .paper-row {
    grid-template-columns: 120px 1fr;
  }

  .paper-thumb {
    width: 120px;
    height: 88px;
  }

  .paper-actions {
    grid-column: 1 / -1;
    flex-direction: row;
  }
}
</style>