<script setup>
const year = new Date().getFullYear()
</script>

<template>
  <footer id="contact" class="signoff stock-ink">
    <div class="page">
      <p class="volume-tag">Vol. 06 — Sign-off</p>
      <h2 class="signoff-title slash-accent">End of transmission,<br />for now.</h2>

      <p class="signoff-lede">
        Open to research collaboration, internships, and conversations about
        quantum machine learning. Reach out below.
      </p>

      <div class="signoff-emails">
        <a href="mailto:amanuel.jn@gmail.com">amanuel.jn@gmail.com</a>
        <a href="mailto:antony.manuel@etu.imt-nord-europe.fr">antony.manuel@etu.imt-nord-europe.fr</a>
      </div>

      <div class="signoff-actions">
        <a class="button button-primary" href="mailto:amanuel.jn@gmail.com">Email me</a>
        <a class="button button-secondary" href="#top">Back to Vol. 00</a>
      </div>

      <p class="signoff-fine">© {{ year }} Antony Manuel. Field log closed, more volumes to come.</p>
    </div>
  </footer>
</template>

<style scoped>
.signoff {
  padding: 64px 0 48px;
}

.signoff-title {
  font-family: var(--font-display);
  text-transform: uppercase;
  font-size: clamp(2rem, 5vw, 3.2rem);
  line-height: 1.02;
  margin: 0 0 20px;
}

.signoff-lede {
  max-width: 52ch;
  line-height: 1.7;
  color: rgba(242, 230, 204, 0.86);
  margin-bottom: 24px;
}

.signoff-emails {
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-family: var(--font-mono);
  font-size: 0.95rem;
  margin-bottom: 28px;
}

.signoff-emails a {
  text-decoration: underline;
  text-underline-offset: 4px;
  color: var(--ember-soft);
}

.signoff-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-bottom: 40px;
}

.signoff-actions .button {
  border-color: var(--paper);
  color: var(--paper);
}

.signoff-actions .button-primary {
  border-color: var(--blood);
}

.signoff-fine {
  font-family: var(--font-mono);
  font-size: 0.74rem;
  opacity: 0.5;
}
</style>
