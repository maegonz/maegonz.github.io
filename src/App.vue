<script setup>
import TornDivider from './components/TornDivider.vue'
import SiteHeader from './components/SiteHeader.vue'
import DossierJourney from './components/DossierJourney.vue'
import Dispatches from './components/Dispatches.vue'
import ProjectsMosaic from './components/ProjectsMosaic.vue'
import LatestWork from './components/LatestWork.vue'
import SiteFooter from './components/SiteFooter.vue'
</script>

<template>
  <div class="site">
    <SiteHeader />
    <TornDivider direction="to-paper" />

    <DossierJourney />
    <TornDivider direction="to-paper" />

    <LatestWork />
    <TornDivider direction="to-ink" />

    <Dispatches />
    <TornDivider direction="to-ink" />

    <ProjectsMosaic />
    <TornDivider direction="to-ink" />

    <SiteFooter />
  </div>
</template>