<script setup lang="ts">
import AppLayout from "@/layout/AppLayout.vue";

</script>

<template>
<AppLayout>
  <template #default>
    <div class="bg-[#050f19] text-white rounded-lg h-72 lg:h-96 flex flex-col justify-center items-center space-y-6">
    <slot name="title"/>
    <slot name="cta"/>
    </div>
  </template>
</AppLayout>
</template>

<style scoped>

</style>