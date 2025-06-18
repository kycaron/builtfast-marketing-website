<script setup lang="ts">
import { Icon } from '@iconify/vue';
</script>

<template>
  <div class="container font-inter pt-10 flex justify-between items-center lg:w-10/12 px-5 bg-black text-white mx-auto ml-[258px]">
    <img alt="builtfast_logo" src="../assets/images/logo.svg" />
    <div class="hidden md:flex items-center space-x-8">
      <a href="#" class="text-gray-300 hover:text-white transition-colors flex items-center space-x-2"><span>Hosting</span> <Icon icon="iconamoon:arrow-down-2-bold" class="text-white"/></a>
      <a href="#" class="text-gray-300 hover:text-white transition-colors flex items-center space-x-2"><span>Domains</span> <Icon icon="iconamoon:arrow-down-2-bold" class="text-white"/></a>
      <a href="#" class="text-gray-300 hover:text-white transition-colors">Websites</a>
      <a href="#" class="text-gray-300 hover:text-white transition-colors">Resources</a>
      <a href="#" class="text-gray-300 hover:text-white transition-colors">Support</a>
    <button class="bg-cyan-400 !font-source-sans hover:bg-cyan-700 text-white font-bold h-9 w-[72px] rounded-lg transition-colors">
      LOGIN
    </button>
    </div>
  </div>
</template>

<style scoped>
</style>