<script setup>
import PageHeaders from "../components/PageHeader.vue";
import AppLayout from "~/layout/AppLayout.vue";
import HeroHeader from "~/components/HeroHeader.vue";
import FeatureGrid from "../FeatureGrid.vue";

const featuresList = [
  {
    icon: 'material-symbols:speed-rounded',
    title: 'People Not Just Profits',
    description: 'People-first hosting, built to serve business like yours.',
  },
  {
    icon: 'material-symbols:headset-mic-outline-sharp',
    title: 'Customer First Approach',
    description: 'Our first priority? You. Everything else follows from that.',
  },
  {
    icon: 'material-symbols:ads-click',
    title: 'Built by Hosting Veterans',
    description: "We've seen it all, and we built something better.",
  },

];
</script>

<template>
<div class="bg-[#F6F9FB]">
  <AppLayout>
    <template #default>
      <PageHeaders title="The BuiltFast Difference" highlight="Difference"
                   highlight-color="cyan"/>

      <FeatureGrid :features="featuresList" />
    </template>
  </AppLayout>
  <InfoCard>
    <template #title>
      <HeroHeader title="Let's Build Your Online Success Story" highlight="Success" highlight-color="blue" />
    </template>
    <template #cta>
     <button class="bg-orange-500">sdflj</button>
    </template>
  </InfoCard>
</div>

</template>


<style scoped>

</style>