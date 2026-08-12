<script setup>
const qa = [
  { q: 'Currently based', a: 'IMT Nord Europe, final year of my Master\u2019s.' },
  { q: 'Core obsession', a: 'Where quantum computing meets machine learning \u2014 what quantum structure can (and can\u2019t) buy a learning system.' },
  { q: 'Also fluent in', a: 'Graph neural networks, explainable AI, and Computer Vision.' },
  { q: 'How I work', a: 'Literature review \u2192 study design \u2192 analysis \u2192 writing \u2014 methodologically sound, and readable by someone outside the field.' },
]

const stops = [
  {
    date: '11/2025',
    title: 'CrossTechXperience Hackathon',
    body: 'Hybrid quantum-classical architectures and convergence analysis for generative models. Current research focus.',
  },
  {
    date: '10/2025',
    title: 'Transformer Explainability project with Mikaela Keller from INRIA',
    body: 'Master\u2019s in Computer Science & Applied Mathematics. Coursework and projects spanning GNNs, NLP, and computer vision.',
  },
  {
    date: '05/2025',
    title: 'Internship at Numalis on Adversarial Detection Methods',
    body: 'Investigating machine learning model behaviour against adversarial examples — attribution methods, Sobol indices, and concept-based explainability.',
  },
  {
    date: '04/2025',
    title: 'Project at CRIStAL on SMLP human interaction dataset',
    body: 'Master\u2019s in Computer Science & Applied Mathematics. Coursework and projects spanning GNNs, NLP, and computer vision.',
  },
]
</script>

<template>
  <section id="about" class="dossier-journey stock-paper">
    <div class="page">
      <div class="dj-grid">
        <div class="dj-col dj-dossier">
          <p class="volume-tag">Vol. 01 — Dossier</p>
          <h2 class="dj-title slash-accent">About the agent</h2>
          <span class="marginalia">the short version →</span>

          <div class="qa-grid">
            <div v-for="item in qa" :key="item.q" class="qa-row">
              <dt>{{ item.q }}</dt>
              <dd>{{ item.a }}</dd>
            </div>
          </div>
        </div>

        <div class="dj-col dj-journey">
          <p class="volume-tag">Vol. 03 — Research journey</p>
          <h2 class="dj-title slash-accent">The trail so far</h2>
          <span class="marginalia">how I got here →</span>

          <ol class="timeline">
            <li v-for="stop in stops" :key="stop.title" class="timeline-item">
              <span class="timeline-date">{{ stop.date }}</span>
              <div class="timeline-body">
                <h3>{{ stop.title }}</h3>
              </div>
            </li>
          </ol>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.dossier-journey {
  padding: 56px 0 64px;
}

.dj-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0 56px;
  align-items: start;
}

.dj-col {
  position: relative;
}

.dj-journey {
  padding-left: 56px;
  border-left: 1px solid var(--paper-line);
}

.dj-title {
  font-family: var(--font-display);
  text-transform: uppercase;
  font-size: clamp(1.7rem, 3.2vw, 2.4rem);
  margin: 0 0 6px;
}

.marginalia {
  display: inline-block;
  margin-bottom: 22px;
}

/* --- Dossier QA --- */
.qa-grid {
  margin-top: 8px;
  display: grid;
  gap: 0;
  border-top: 1px solid var(--paper-line);
}

.qa-row {
  display: grid;
  grid-template-columns: 1fr;
  gap: 4px;
  padding: 16px 0;
  border-bottom: 1px solid var(--paper-line);
}

.qa-row dt {
  font-family: var(--font-mono);
  font-size: 0.76rem;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  opacity: 0.65;
}

.qa-row dd {
  margin: 0;
  font-family: var(--font-serif);
  font-size: 1.05rem;
  line-height: 1.5;
}

/* --- Journey timeline --- */
.timeline {
  list-style: none;
  margin: 8px 0 0;
  padding: 0;
  border-left: 2px solid var(--blood);
}

.timeline-item {
  position: relative;
  padding: 4px 0 22px 26px;
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
  font-size: 0.74rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--blood-deep);
}

.timeline-body h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  margin: 6px 0 0;
}

@media (max-width: 860px) {
  .dj-grid {
    grid-template-columns: 1fr;
    gap: 48px 0;
  }

  .dj-journey {
    padding-left: 0;
    border-left: none;
    padding-top: 40px;
    border-top: 1px solid var(--paper-line);
  }
}
</style>