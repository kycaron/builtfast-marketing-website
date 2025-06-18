<script setup lang="ts">
import { ref } from 'vue';
import { Icon } from '@iconify/vue';

const isHostingOpen = ref(false);
const isDomainsOpen = ref(false);
const isSupportOpen = ref(false);
const isMobileMenuOpen = ref(false);

const hostingItems = [
  { icon: 'material-symbols:cloud-outline', title: 'Web Hosting', desc: 'Fast and reliable web hosting solutions' },
  { icon: 'mdi:server', title: 'VPS Hosting', desc: 'Virtual private servers for more control' },
  { icon: 'fa-brands:wordpress', title: 'Managed WordPress Hosting', desc: 'Optimized hosting for WordPress sites' },
];

const domainItems = [
  { icon: 'mdi:domain-plus', title: 'Register a Domain', desc: 'Find and secure your domain name' },
  { icon: 'mdi:swap-horizontal', title: 'Transfer a Domain', desc: 'Move your domain to BuiltFast' },
];

const supportItems = [
  { icon: 'mdi:email-outline', title: 'Contact Us', desc: 'Reach out to our 24/7 support team' },
];
</script>

<template>
  <header class="w-full bg-transparent text-white font-inter">
    <div class="flex justify-between items-center px-5 py-4 md:px-10 max-w-screen-xl mx-auto">
      <img alt="builtfast_logo" src="../assets/images/logo.svg" class="h-8" />

      <!-- Mobile Menu Toggle -->
      <button @click="isMobileMenuOpen = !isMobileMenuOpen" class="md:hidden">
        <Icon icon="mdi:menu" class="text-2xl" />
      </button>

      <!-- Desktop Menu -->
      <nav class="hidden md:flex items-center space-x-8 relative">
        <!-- Hosting Dropdown -->
        <div class="relative" @mouseenter="isHostingOpen = true" @mouseleave="isHostingOpen = false">
          <a href="#" class="flex items-center space-x-2 hover:text-white text-gray-300">
            <span>Hosting</span>
            <Icon icon="iconamoon:arrow-down-2-bold" />
          </a>
          <div v-show="isHostingOpen" class="absolute top-10 left-0 bg-white text-black shadow-xl rounded-xl w-[340px] p-6 space-y-4 z-50">
            <div v-for="item in hostingItems" :key="item.title" class="flex items-start space-x-3 hover:bg-gray-100 px-3 py-2 rounded-md transition">
              <Icon :icon="item.icon" class="text-blue-600 text-xl mt-1" />
              <div>
                <p class="font-semibold text-sm">{{ item.title }}</p>
                <p class="text-gray-500 text-sm">{{ item.desc }}</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Domains Dropdown -->
        <div class="relative" @mouseenter="isDomainsOpen = true" @mouseleave="isDomainsOpen = false">
          <a href="#" class="flex items-center space-x-2 hover:text-white text-gray-300">
            <span>Domains</span>
            <Icon icon="iconamoon:arrow-down-2-bold" />
          </a>
          <div v-show="isDomainsOpen" class="absolute top-10 left-0 bg-white text-black shadow-xl rounded-xl w-[340px] p-6 space-y-4 z-50">
            <div v-for="item in domainItems" :key="item.title" class="flex items-start space-x-3 hover:bg-gray-100 px-3 py-2 rounded-md transition">
              <Icon :icon="item.icon" class="text-blue-600 text-xl mt-1" />
              <div>
                <p class="font-semibold text-sm">{{ item.title }}</p>
                <p class="text-gray-500 text-sm">{{ item.desc }}</p>
              </div>
            </div>
          </div>
        </div>

        <a href="#" class="hover:text-white text-gray-300">Websites</a>
        <a href="#" class="hover:text-white text-gray-300">Resources</a>

        <!-- Support Dropdown -->
        <div class="relative" @mouseenter="isSupportOpen = true" @mouseleave="isSupportOpen = false">
          <a href="#" class="flex items-center space-x-2 hover:text-white text-gray-300">
            <span>Support</span>
            <Icon icon="iconamoon:arrow-down-2-bold" />
          </a>
          <div v-show="isSupportOpen" class="absolute top-10 left-0 bg-white text-black shadow-xl rounded-xl w-[340px] p-6 space-y-4 z-50">
            <div v-for="item in supportItems" :key="item.title" class="flex items-start space-x-3 hover:bg-gray-100 px-3 py-2 rounded-md transition">
              <Icon :icon="item.icon" class="text-blue-600 text-xl mt-1" />
              <div>
                <p class="font-semibold text-sm">{{ item.title }}</p>
                <p class="text-gray-500 text-sm">{{ item.desc }}</p>
              </div>
            </div>
          </div>
        </div>

        <button class="bg-cyan-400 hover:bg-cyan-700 text-white font-bold h-9 w-[72px] rounded-lg transition">
          LOGIN
        </button>
      </nav>
    </div>

    <!-- Mobile Menu -->
<div v-if="isMobileMenuOpen" class="md:hidden bg-black px-5 pb-6 pt-4 space-y-4 text-white font-inter">
  <!-- Hosting with Submenu -->
  <div>
    <button @click="isHostingOpen = !isHostingOpen" class="w-full text-left flex justify-between items-center py-2">
      <span>Hosting</span>
      <Icon :icon="isHostingOpen ? 'mdi:chevron-up' : 'mdi:chevron-down'" class="text-lg" />
    </button>
    <div v-if="isHostingOpen" class="ml-4 mt-2 space-y-2 text-sm text-gray-300">
      <a href="#" class="block">Web Hosting</a>
      <a href="#" class="block">VPS Hosting</a>
      <a href="#" class="block">Managed WordPress Hosting</a>
    </div>
  </div>

  <!-- Domains with Submenu -->
  <div>
    <button @click="isDomainsOpen = !isDomainsOpen" class="w-full text-left flex justify-between items-center py-2">
      <span>Domains</span>
      <Icon :icon="isDomainsOpen ? 'mdi:chevron-up' : 'mdi:chevron-down'" class="text-lg" />
    </button>
    <div v-if="isDomainsOpen" class="ml-4 mt-2 space-y-2 text-sm text-gray-300">
      <a href="#" class="block">Register a Domain</a>
      <a href="#" class="block">Transfer a Domain</a>
    </div>
  </div>

  <!-- Websites (no submenu) -->
  <a href="#" class="block py-2">Websites</a>

  <!-- Resources (no submenu) -->
  <a href="#" class="block py-2">Resources</a>

  <!-- Support with Submenu -->
  <div>
    <button @click="isSupportOpen = !isSupportOpen" class="w-full text-left flex justify-between items-center py-2">
      <span>Support</span>
      <Icon :icon="isSupportOpen ? 'mdi:chevron-up' : 'mdi:chevron-down'" class="text-lg" />
    </button>
    <div v-if="isSupportOpen" class="ml-4 mt-2 space-y-2 text-sm text-gray-300">
      <a href="#" class="block">Contact Us</a>
    </div>
  </div>

  <!-- Login Button -->
  <button class="mt-4 bg-cyan-400 hover:bg-cyan-700 text-white font-bold h-10 w-full rounded-lg transition">
    LOGIN
  </button>
</div>

  </header>
</template>