<script setup lang="ts">
import { Icon } from '@iconify/vue';

interface Feature {
  icon: string;
  title: string;
  description: string;
}

defineProps<{
  features: Feature[];
}>();
</script>

<template>
  <div class="grid grid-cols-1 gap-x-8 md:grid-cols-2 lg:grid-cols-3">
    <div v-for="feature in features" class="flex flex-col space-y-4" :key="feature.title">
      <div class="flex size-[75px] items-center justify-center rounded-2xl bg-cyan-400">
        <Icon :icon="feature.icon" class="size-[60px] text-white" />
      </div>

      <div class="font-medium text-[32px]">
        {{ feature.title }}
      </div>
      <div class="text-slate-600 w-10/12 font-inter font-light text-[18px] leading-relaxed">
        {{ feature.description }}
      </div>
    </div>
  </div>
</template>