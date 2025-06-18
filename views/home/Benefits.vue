<script setup>
import AppLayout from '@/layout/AppLayout.vue';
import PageHeader from '@/components/PageHeader.vue';
import FeatureGrid from '@/views/FeatureGrid.vue';

const featuresList = [
  {
    icon: 'mdi:refresh',
    title: 'Free Website Migration',
    description: 'We’ll move your site for free and work closely with you so your business doesn’t miss a beat.',
  },
  {
    icon: 'mdi:web',
    title: 'Free Domain Name',
    description: 'Free first year domain registration with select plans.',
  },
  {
    icon: 'mdi:lock-outline',
    title: 'Free SSL Certificates',
    description: 'Security shouldn’t be optional—every BuiltFast site includes a free SSL certificate.',
  },
  {
    icon: 'ic:outline-backup',
    title: 'Daily Backups',
    description: 'Your site, backed up daily, so you can rest easy knowing we’ve got it.',
  },
  {
    icon: 'material-symbols:stacked-line-chart',
    title: 'Scales with Your Business',
    description: 'Built to grow with you and scale effortlessly, regardless of which plan you start with.',
  },
  {
    icon: 'mdi:clock-outline',
    title: '99.99% Uptime',
    description: 'Your business never sleeps, and neither does your website. Expect uninterrupted performance, 24/7.',
  },
];


</script>
<template>
    <AppLayout>
        <template #default>
            <PageHeader title="Built-In Benefits That Just Make Sense" highlight="Benefits"/>

            <FeatureGrid :features="featuresList" />
        </template>
    </AppLayout>
</template>