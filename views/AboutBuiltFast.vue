<script setup>
import AppLayout from '@/layout/AppLayout.vue';
import PageHeader from '@/components/PageHeader.vue';
import FeatureGrid from '@/views/FeatureGrid.vue';

const featuresList = [
  {
    icon: 'material-symbols:speed-rounded',
    title: 'Speed',
    description: 'Built for blazing fast speeds and guaranteed performance.',
  },
  {
    icon: 'material-symbols:headset-mic-outline-sharp',
    title: 'Support 24/7',
    description: 'Real experts. Real answers. Always here \n day or night.',
  },
  {
    icon: 'material-symbols:ads-click',
    title: 'Simplicity',
    description: 'A clean and custom control panel that just works \n no clutter, no confusion.',
  },
];
</script>
<template>
    <AppLayout>
        <template #default>
            <PageHeader title="Why BuiltFast?" highlight="BuiltFast?"
              subtitle="BuiltFast gives you fast, secure hosting that fits your business today and prepares you for your growth of tomorrow."/>

      <FeatureGrid :features="featuresList" />
        </template>
    </AppLayout>
</template>