<script setup>
import { Icon } from '@iconify/vue'
import AppLayout from '@/layout/AppLayout.vue'
import PageHeader from '@/components/PageHeader.vue'
import Pricing from '@/views/home/Pricing.vue'
import Hero from '@/views/home/Hero.vue'
import AbouteBuiltFast from '@/views/AboutBuiltFast.vue'
import Benefits from '@/views/home/Benefits.vue'
import ControlCenter from './views/home/ControlCenter.vue'
import SiteSafety from './views/home/SiteSafety.vue'

</script>

<template>
  <Hero />

  <AbouteBuiltFast />

  <Pricing />

  <Benefits />

  <ControlCenter />

  <SiteSafety />
</template>