<script setup></script>

<template>
  <header class="hero stock-ink">
    <div class="page hero-grid">
      <div class="hero-copy">
        <p class="volume-tag">Vol. 00 — Cover</p>
        <h1 class="hero-title">
          <span class="slash-accent">Antony</span><br />
          <span class="accent">Manuel</span>
        </h1>
        <p class="hero-role">Field notes from a research career in progress</p>
        <p class="hero-lede">
          Final-year Master's student in Computer Science &amp; Applied
          Mathematics at IMT Nord Europe. Working at the intersection of
          <strong>quantum computing</strong> and <strong>machine learning</strong>,
          with hands-on chops in graph neural networks, explainable AI,
          and computer vision.
        </p>
        <div class="hero-actions">
          <a class="button button-primary" href="#contact">Get in touch</a>
          <a class="button button-secondary" href="https://github.com/maegonz" target="_blank" rel="noreferrer">GitHub</a>
          <a class="button button-secondary" href="https://linkedin.com/in/antonymanuel" target="_blank" rel="noreferrer">LinkedIn</a>
          <a class="button button-secondary" href="/doc/resume_Antony_MANUEL.pdf" target="_blank" rel="noreferrer">Resume</a>
        </div>
      </div>

      <div class="hero-polaroid">
        <div class="polaroid">
          <img src="/figures/IMG_2328.JPG" alt="Portrait of Antony Manuel" />
          <span class="tape tape-left"></span>
          <span class="tape tape-right"></span>
          <p class="polaroid-caption">field agent — vol. 00</p>
        </div>
        <span class="stamp">FIELD LOG</span>
      </div>
    </div>
  </header>
</template>

<style scoped>
.hero {
  padding: 64px 0 56px;
  overflow: hidden;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.15fr 0.85fr;
  gap: 40px;
  align-items: center;
}

.hero-title {
  font-family: var(--font-display);
  font-weight: 400;
  text-transform: uppercase;
  font-size: clamp(3rem, 7vw, 5.4rem);
  line-height: 0.96;
  letter-spacing: 0.01em;
  margin: 0 0 18px;
}

.hero-role {
  font-family: var(--font-serif);
  font-style: italic;
  font-size: 1.15rem;
  color: var(--ember-soft);
  margin: 0 0 16px;
}

.hero-lede {
  font-size: 1.02rem;
  line-height: 1.7;
  color: rgba(242, 230, 204, 0.86);
  max-width: 52ch;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 26px;
}

.hero-actions .button {
  border-color: var(--paper);
  color: var(--paper);
}

.hero-actions .button-primary {
  border-color: var(--blood);
  color: var(--paper);
}

.hero-polaroid {
  position: relative;
  display: flex;
  justify-content: center;
}

.polaroid {
  position: relative;
  width: min(100%, 300px);
  background: var(--paper);
  padding: 14px 14px 44px;
  border-radius: 2px;
  box-shadow: 0 22px 44px rgba(0, 0, 0, 0.45);
  transform: rotate(-3deg);
}

.polaroid img {
  width: 100%;
  aspect-ratio: 4 / 5;
  object-fit: cover;
  filter: sepia(0.12) contrast(1.05);
}

.polaroid-caption {
  position: absolute;
  bottom: 12px;
  left: 14px;
  right: 14px;
  margin: 0;
  font-family: var(--font-hand);
  font-size: 1.15rem;
  color: var(--ink-soft);
  text-align: center;
}

.tape {
  position: absolute;
  width: 74px;
  height: 26px;
  background: rgba(238, 166, 44, 0.55);
  border: 1px solid rgba(21, 16, 13, 0.15);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.25);
}

.tape-left {
  top: -12px;
  left: -18px;
  transform: rotate(-32deg);
}

.tape-right {
  top: -10px;
  right: -20px;
  transform: rotate(24deg);
}

.stamp {
  position: absolute;
  top: -6px;
  right: -6px;
  font-family: var(--font-mono);
  font-size: 0.72rem;
  letter-spacing: 0.14em;
  color: var(--blood);
  border: 2px solid var(--blood);
  border-radius: 999px;
  padding: 8px 12px;
  transform: rotate(14deg);
  background: rgba(21, 16, 13, 0.7);
}

@media (max-width: 860px) {
  .hero-grid {
    grid-template-columns: 1fr;
  }

  .hero-polaroid {
    order: -1;
  }
}
</style>
