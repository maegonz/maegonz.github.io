<script setup>
const base = import.meta.env.BASE_URL

const projects = [
  {
    title: 'Spatial-Temporal Convolutional Networks for Human-Motion Analysis',
    image: 'figures/animation.gif',
    tags: ['Computer Vision', 'GNN'],
    link: 'https://github.com/maegonz/spatial-temporal-analysis',
  },
  {
    title: 'Graph Convolutional Networks for Enzyme Classification & Sign Language Recognition',
    image: 'figures/placidplace-sign-language-7167_512.gif',
    tags: ['GNN', 'NLP'],
    link: 'https://github.com/maegonz/graph-convolutional-networks',
  },
  {
    title: 'NFL Game Predictions with Transformers',
    image: 'figures/nfl_preview.gif',
    tags: ['Transformers'],
    link: 'https://github.com/maegonz/nfl-transformers',
  },
  {
    title: 'Hybrid Quantum-Classical Classifiers',
    image: 'figures/decision_boundary_training.gif',
    tags: ['Quantum Computing'],
    link: 'https://github.com/maegonz/quantum-classifiers',
  },
  {
    title: 'RSNA Intracranial Aneurysm Detection',
    image: 'figures/rsna_preview.gif',
    tags: ['Computer Vision', 'Medical'],
    link: 'https://github.com/maegonz/aneurysm-detection',
  },
  {
    title: 'Cycle Gans for Image-to-Image Translation',
    image: 'figures/fake_satellite.gif',
    tags: ['GANs'],
    link: 'https://github.com/maegonz/Generative-Adversarial-Networks',
  },
  {
    title: 'M1 Thesis on Adversarial Detection Methods',
    image: 'figures/m1_internship_first_page.png',
    tags: ['Explainability', 'Adversarial Examples', 'Computer Vision'],
    link: 'https://github.com/maegonz/Generative-Adversarial-Networks',
  },
]
</script>

<template>
  <section id="projects" class="mosaic stock-ink">
    <div class="page">
      <p class="volume-tag">Vol. 04 — Projects</p>
      <h2 class="mosaic-title slash-accent">Selected case files</h2>
      <span class="marginalia">click a case to open the file ↓</span>

      <div class="mosaic-grid">
        <details v-for="p in projects" :key="p.title" class="case-card">
          <summary>
            <img :src="base + p.image" :alt="p.title" loading="lazy" />
            <div class="case-meta">
              <h3>{{ p.title }}</h3>
              <div class="case-tags">
                <span v-for="tag in p.tags" :key="tag">{{ tag }}</span>
              </div>
            </div>
          </summary>
          <div class="case-body">
            <a :href="p.link" target="_blank" rel="noreferrer" class="button button-secondary">View on GitHub</a>
          </div>
        </details>
      </div>
    </div>
  </section>
</template>

<style scoped>
.mosaic {
  padding: 60px 0 68px;
}

.mosaic-title {
  font-family: var(--font-display);
  text-transform: uppercase;
  font-size: clamp(1.9rem, 4vw, 2.6rem);
  margin: 0 0 8px;
}

.marginalia {
  display: inline-block;
  margin-bottom: 26px;
}

.mosaic-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}

.case-card {
  border: 1px solid rgba(242, 230, 204, 0.18);
  border-radius: 4px;
  overflow: hidden;
  background: rgba(242, 230, 204, 0.04);
}

.case-card summary {
  cursor: pointer;
  list-style: none;
}

.case-card summary::-webkit-details-marker {
  display: none;
}

.case-card img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  filter: grayscale(0.15) contrast(1.05);
}

.case-meta {
  padding: 14px;
}

.case-meta h3 {
  font-family: var(--font-serif);
  font-size: 1.02rem;
  line-height: 1.3;
  margin: 0 0 8px;
}

.case-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.case-tags span {
  font-family: var(--font-mono);
  font-size: 0.68rem;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  padding: 3px 8px;
  border: 1px solid var(--ember);
  color: var(--ember);
  border-radius: 999px;
}

.case-body {
  padding: 0 14px 16px;
}

@media (max-width: 960px) {
  .mosaic-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 620px) {
  .mosaic-grid {
    grid-template-columns: 1fr;
  }
}
</style>
