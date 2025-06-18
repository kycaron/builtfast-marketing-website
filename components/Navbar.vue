<script setup lang="ts">
import { ref } from 'vue';
import { Icon } from '@iconify/vue';

const isHostingOpen = ref(false);
const isAboutOpen = ref(false);
const isDomainsOpen = ref(false);
const isSupportOpen = ref(false);

const hostingItems = [
  {
    icon: 'material-symbols:cloud-outline',
    title: 'Web Hosting',
    desc: 'Fast and reliable web hosting solutions',
  },
  {
    icon: 'mdi:server',
    title: 'VPS Hosting',
    desc: 'Virtual private servers for more control',
  },
  {
    icon: 'fa-brands:wordpress',
    title: 'Managed WordPress Hosting',
    desc: 'Optimized hosting for WordPress sites',
  },
];

const aboutItems = [
  {
    icon: 'mdi:account-group-outline',
    title: 'BuiltFast',
    desc: 'Meet the people behind BuiltFast',
  },
  {
    icon: 'mdi:handshake-outline',
    title: 'Partners',
    desc: 'Our trusted business partners',
  },
];

const domainItems = [
  {
    icon: 'mdi:domain-plus',
    title: 'Register a Domain',
    desc: 'Find and secure your domain name',
  },
  {
    icon: 'mdi:swap-horizontal',
    title: 'Transfer a Domain',
    desc: 'Move your domain to BuiltFast',
  },
];

const supportItems = [
  {
    icon: 'mdi:email-outline',
    title: 'Contact Us',
    desc: 'Reach out to our 24/7 support team',
  },
];
</script>

<template>
  <div class="container font-inter pt-10 flex justify-between items-center lg:w-10/12 px-5 bg-black text-white mx-auto ml-[258px] relative">
    <img alt="builtfast_logo" src="../assets/images/logo.svg" />

    <div class="hidden md:flex items-center space-x-8 relative">

      <div class="relative" @mouseenter="isHostingOpen = true" @mouseleave="isHostingOpen = false">
        <a href="#" class="text-gray-300 hover:text-white transition-colors flex items-center space-x-2">
          <span>Hosting</span>
          <Icon icon="iconamoon:arrow-down-2-bold" class="text-white" />
        </a>
        <div v-show="isHostingOpen" class="absolute top-10 left-0 bg-white text-black shadow-xl rounded-xl w-[340px] p-6 space-y-4 z-50">
          <div v-for="item in hostingItems" :key="item.title" class="flex items-start space-x-3 hover:bg-gray-100 px-3 py-2 rounded-md transition-colors cursor-pointer">
            <Icon :icon="item.icon" class="text-blue-600 text-xl mt-1" />
            <div>
              <p class="font-semibold text-sm">{{ item.title }}</p>
              <p class="text-gray-500 text-sm">{{ item.desc }}</p>
            </div>
          </div>
        </div>
      </div>

      <div class="relative" @mouseenter="isDomainsOpen = true" @mouseleave="isDomainsOpen = false">
        <a href="#" class="text-gray-300 hover:text-white transition-colors flex items-center space-x-2">
          <span>Domains</span>
          <Icon icon="iconamoon:arrow-down-2-bold" class="text-white" />
        </a>
        <div v-show="isDomainsOpen" class="absolute top-10 left-0 bg-white text-black shadow-xl rounded-xl w-[340px] p-6 space-y-4 z-50">
          <div v-for="item in domainItems" :key="item.title" class="flex items-start space-x-3 hover:bg-gray-100 px-3 py-2 rounded-md transition-colors cursor-pointer">
            <Icon :icon="item.icon" class="text-blue-600 text-xl mt-1" />
            <div>
              <p class="font-semibold text-sm">{{ item.title }}</p>
              <p class="text-gray-500 text-sm">{{ item.desc }}</p>
            </div>
          </div>
        </div>
      </div>

      <a href="#" class="text-gray-300 hover:text-white transition-colors">Websites</a>
      <a href="#" class="text-gray-300 hover:text-white transition-colors">Resources</a>

      <div class="relative" @mouseenter="isSupportOpen = true" @mouseleave="isSupportOpen = false">
        <a href="#" class="text-gray-300 hover:text-white transition-colors flex items-center space-x-2">
          <span>Support</span>
          <Icon icon="iconamoon:arrow-down-2-bold" class="text-white" />
        </a>
        <div v-show="isSupportOpen" class="absolute top-10 left-0 bg-white text-black shadow-xl rounded-xl w-[340px] p-6 space-y-4 z-50">
          <div v-for="item in supportItems" :key="item.title" class="flex items-start space-x-3 hover:bg-gray-100 px-3 py-2 rounded-md transition-colors cursor-pointer">
            <Icon :icon="item.icon" class="text-blue-600 text-xl mt-1" />
            <div>
              <p class="font-semibold text-sm">{{ item.title }}</p>
              <p class="text-gray-500 text-sm">{{ item.desc }}</p>
            </div>
          </div>
        </div>
      </div>

      <div class="relative" @mouseenter="isAboutOpen = true" @mouseleave="isAboutOpen = false">
        <a href="#" class="text-gray-300 hover:text-white transition-colors flex items-center space-x-2">
          <span>About Us</span>
          <Icon icon="iconamoon:arrow-down-2-bold" class="text-white" />
        </a>
        <div v-show="isAboutOpen" class="absolute top-10 left-0 bg-white text-black shadow-xl rounded-xl w-[340px] p-6 space-y-4 z-50">
          <div v-for="item in aboutItems" :key="item.title" class="flex items-start space-x-3 hover:bg-gray-100 px-3 py-2 rounded-md transition-colors cursor-pointer">
            <Icon :icon="item.icon" class="text-blue-600 text-xl mt-1" />
            <div>
              <p class="font-semibold text-sm">{{ item.title }}</p>
              <p class="text-gray-500 text-sm">{{ item.desc }}</p>
            </div>
          </div>
        </div>
      </div>

      <button class="bg-cyan-400 !font-source-sans hover:bg-cyan-700 text-white font-bold h-9 w-[72px] rounded-lg transition-colors">
        LOGIN
      </button>
    </div>
  </div>
</template>