<script setup lang="ts">
import Navbar from '~/components/Navbar.vue';
import HeroHeader from '~/components/HeroHeader.vue';
</script>

<template>
  <div class="min-h-screen min-w-full bg-black text-white font-inter">
    <Navbar />
    <div class="flex h-screen items-center">
      <div class="w-1/2 space-y-8 ml-[254px]">
        <HeroHeader
          title="Web Hosting Built for Speed & Service."
          highlight="Speed"
          highlightColor="cyan"
          subtitle="Lightning-fast hosting for modern websites. Unmatched performance, rock-solid reliability, and expert support that scales with your business."
        />
        <button class="bg-orange-500 hover:bg-orange-600 px-6 py-3 text-white font-medium text-sm rounded">
          START NOW
        </button>
      </div>

      <div class="w-1/2 h-full bg-[url(/assets/images/hero_one_gradient.png)]">
       </div>
    </div>
  </div>
</template>