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
    default: 'red',
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

const textBefore = computed(() => titleParts.value[0]);
const textAfter = computed(() => titleParts.value[1]);

const highlightColorClass = computed(() => {
  const colorMap = {
    red: 'bg-red-300',
    blue: 'bg-blue-300',
    orange: 'bg-orange-300',
    cyan: 'bg-[#1DC9D8]',
  };
  return colorMap[props.highlightColor] || colorMap.red;
});
</script>

<template>
  <div class="text-center mb-8">
    <h2 class="lg:text-[56px] text-4xl font-semibold">
      <span v-if="!highlight">{{ title }}</span>
      <template v-else>
        <span>{{ textBefore }}</span>
        <span class="relative inline-block">
          <span class="relative z-10">{{ highlight }}</span>
          <span
              class="absolute left-0 lg:bottom-2 bottom-1 px-1 w-full h-1.5 lg:h-2.5 z-0"
              :class="highlightColorClass"
          ></span>
        </span>
        <span>{{ textAfter }}</span>
      </template>
    </h2>
    <p v-if="subtitle" class="mt-10 text-[18px] font-light text-gray-600 mx-auto font-inter">
      {{ subtitle }}
    </p>
  </div>
</template>