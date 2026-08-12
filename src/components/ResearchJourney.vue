<script setup>
const stops = [
  {
    date: '03/2026',
    title: 'M2 — Quantum GANs',
    body: 'Hybrid quantum-classical architectures and convergence analysis for generative models. Current research focus.',
  },
  {
    date: '10/2025',
    title: 'INRIA - Transformer Explainability',
    body: 'Master\u2019s in Computer Science & Applied Mathematics. Coursework and projects spanning GNNs, NLP, and computer vision.',
  },
  {
    date: '05/2025',
    title: 'Numalis - Adversarial Detection Methods',
    body: 'Investigating machine learning model behaviour against adversarial examples — attribution methods, Sobol indices, and concept-based explainability.',
  },
  {
    date: '04/2025',
    title: 'CRIStAL - SMLP',
    body: 'Master\u2019s in Computer Science & Applied Mathematics. Coursework and projects spanning GNNs, NLP, and computer vision.',
  },
  {
    date: '09/2023',
    title: 'IMT Nord Europe',
    body: 'Master\u2019s in Computer Science & Applied Mathematics. Coursework and projects spanning GNNs, NLP, and computer vision.',
  },
]
</script>

<template>
  <section id="research" class="journey stock-paper">
    <div class="page">
      <p class="volume-tag">Vol. 03 — Research journey</p>
      <h2 class="journey-title slash-accent">The trail so far</h2>

      <ol class="timeline">
        <li v-for="stop in stops" :key="stop.title" class="timeline-item">
          <span class="timeline-date">{{ stop.date }}</span>
          <div class="timeline-body">
            <h3>{{ stop.title }}</h3>
            <!-- <p>{{ stop.body }}</p> -->
          </div>
        </li>
      </ol>
    </div>
  </section>
</template>

<style scoped>
.journey {
  padding: 60px 0 68px;
}

.journey-title {
  font-family: var(--font-display);
  text-transform: uppercase;
  font-size: clamp(1.9rem, 4vw, 2.6rem);
  margin: 0 0 34px;
}

.timeline {
  list-style: none;
  margin: 0;
  padding: 0;
  border-left: 2px solid var(--blood);
}

.timeline-item {
  position: relative;
  padding: 4px 0 28px 30px;
}

.timeline-item::before {
  content: "";
  position: absolute;
  left: -7px;
  top: 6px;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: var(--blood);
  border: 2px solid var(--paper);
  box-shadow: 0 0 0 2px var(--blood);
}

.timeline-date {
  font-family: var(--font-mono);
  font-size: 0.78rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--blood-deep);
}

.timeline-body h3 {
  font-family: var(--font-serif);
  font-size: 1.3rem;
  margin: 6px 0 6px;
}

.timeline-body p {
  margin: 0;
  line-height: 1.6;
  max-width: 62ch;
  opacity: 0.85;
}
</style>
