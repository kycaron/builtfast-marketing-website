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
  <div class="grid grid-cols-1 gap-x-8 gap-y-10 lg:gap-y-28 place-items-center md:grid-cols-2 lg:grid-cols-3">
    <div v-for="feature in features" class="flex flex-col h-full items-center lg:items-start space-y-8" :key="feature.title">
      <div class="flex size-16 lg:size-[75px] items-center justify-center rounded-2xl bg-cyan-400">
        <Icon :icon="feature.icon" class="size-9 size-[60px] text-white" />
      </div>

      <div class="font-medium text-center text-2xl min-h-8 lg:text-start lg:text-xl">
        {{ feature.title }}
      </div>
      <div class="text-slate-600 font-inter text-center lg:mr-12 lg:text-start font-light text-base lg:text-[18px] leading-relaxed">
        {{ feature.description }}
      </div>
    </div>
  </div>
</template>