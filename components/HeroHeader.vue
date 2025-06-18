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

<template>
  <div>
    <h1 class="text-[64px] leading-[1.2] font-bold text-white text-left">
      <span v-if="!highlight">{{ title }}</span>
      <template v-else>
        {{ titleParts[0] }}
        <span :class="highlightColorClass">{{ highlight }}</span>
        {{ titleParts[1] }}
      </template>
    </h1>
    <p v-if="subtitle" class="mt-6 text-[16px] text-gray-300 text-left max-w-lg">
      {{ subtitle }}
    </p>
  </div>
</template>