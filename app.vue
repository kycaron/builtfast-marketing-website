<template>
  <AppLayout>
    <PageHeader title="Why BuiltFast?" highlight="BuiltFast?"
             subtitle="BuiltFast gives you fast, secure hosting that fits your business today and prepares you for your growth of tomorrow."/>


        <Pricing />
  
  </AppLayout>
</template>

<script setup>
import { Icon } from '@iconify/vue'
import AppLayout from '@/layout/AppLayout.vue'
import PageHeader from '@/components/PageHeader.vue'
import Pricing from '@/views/home/Pricing.vue'
</script>
