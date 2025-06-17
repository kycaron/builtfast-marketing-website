<template>
  <div
  class="flex flex-col p-[40px] w-[464px] h-[623px] rounded-[12px] gap-[32px] border"
  :style="{ backgroundColor: customBackgroundColor, borderColor: customBorderColor }"
  :class="[backgroundColor]"
>

      <!-- Title & Description -->
      <div class="space-y-2">
        <h2 :class="['text-xl font-semibold', titleColor]">{{ title }}</h2>
        <p :class="['text-sm', descriptionColor]">{{ description }}</p>
      </div>
  
      <!-- Price Block -->
      <div>
        <p :class="['text-sm', mutedTextColor]">STARTING AT</p>
        <p :class="['text-3xl font-bold flex items-baseline gap-1', priceColor]">
          {{ price }}
          <span :class="['text-base font-medium', periodColor]">{{ period }}</span>
        </p>
        <p :class="['text-xs mt-1', mutedTextColor]">*For 36 month term.</p>
      </div>
  
        <!-- CTA button -->
        <a
        :href="buttonLink"
        class="w-full text-sm font-semibold py-3 rounded text-center transition"
        :class="[buttonTextColor]"
        :style="{ backgroundColor: customButtonBg }"
        >
        {{ buttonText }}
        </a>
        
      <!-- Features List -->
       <ul class="space-y-3 text-sm" :class="featureTextColor">
        <li
          v-for="(feature, index) in features"
          :key="index"
          class="flex items-center"
        >
          <Icon :icon="featureIcon" :class="[featureIconColor, 'w-4 h-4 mr-2']" />
          {{ feature }}
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  defineProps({
    title: String,
    description: String,
    price: String,
    period: String,
    features: Array,
    buttonText: String,
    buttonLink: String,
  
    // Color props
    backgroundColor: {
      type: String,
      default: 'bg-white'
    },
    borderColor: {
      type: String,
      default: 'border-gray-200'
    },
    titleColor: {
      type: String,
      default: 'text-gray-900'
    },
    descriptionColor: {
      type: String,
      default: 'text-gray-600'
    },
    priceColor: {
      type: String,
      default: 'text-gray-900'
    },
    periodColor: {
      type: String,
      default: 'text-gray-500'
    },
    mutedTextColor: {
      type: String,
      default: 'text-gray-500'
    },
    featureTextColor: {
      type: String,
      default: 'text-gray-700'
    },
    buttonTextColor: {
      type: String,
      default: 'text-white'
    },
    buttonBgColor: {
      type: String,
      default: 'bg-gray-900'
    },
    buttonHoverBgColor: {
      type: String,
      default: 'hover:bg-gray-800'
    },
    featureIcon: {
      type: [Object, Function],
      required: true
    },
    featureIconColor: {
      type: String,
      default: 'text-emerald-500'
    },
    customBorderColor: {
    type: String,
    default: ''
  },
  customButtonBg: {
    type: String,
    default: ''
  },
  customBackgroundColor: {
    type: String,
    default: ''
  }
  })
  </script>
  