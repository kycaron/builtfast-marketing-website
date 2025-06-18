<template>
  <div class="flex flex-col px-4 sm:px-0">
    <h1 class="text-4xl sm:text-5xl lg:text-6xl xl:text-[64px] leading-tight sm:leading-tight lg:leading-[1.2] font-bold text-white text-left font-sans">
      <span v-if="!highlight">{{ title }}</span>
      <template v-else>
        {{ titleParts[0] }}
        <span :class="highlightColorClass">{{ highlight }}</span>
        {{ titleParts[1] }}
      </template>
    </h1>
    <p
      v-if="subtitle"
      class="mt-4 sm:mt-6 text-base sm:text-lg text-gray-300 text-left max-w-full sm:max-w-lg font-light"
    >
      {{ subtitle }}
    </p>
  </div>
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  highlight: {
    type: String,
    default: '',
  },
  highlightColor: {
    type: String,
    default: 'blue',
  },
  subtitle: {
    type: String,
    default: '',
  },
});

const titleParts = computed(() => {
  if (!props.highlight || !props.title.includes(props.highlight)) {
    return [props.title, ''];
  }
  return props.title.split(props.highlight, 2);
});

const highlightColorClass = computed(() => {
  const colorMap = {
    red: 'text-red-400',
    blue: 'text-blue-400',
    orange: 'text-orange-400',
    cyan: 'text-cyan-400',
  };
  return colorMap[props.highlightColor] || colorMap.red;
});
</script>