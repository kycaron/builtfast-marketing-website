<script setup lang="ts">
import Navbar from '~/components/Navbar.vue';
import HeroHeader from '~/components/HeroHeader.vue';
</script>

<template>
  <div class="lg:min-h-screen w-full bg-black text-white font-inter relative overflow-hidden">
    <Navbar />

    <div class="relative min-h-[600px] lg:h-screen flex items-center justify-center px-4 sm:px-8">
      <!-- Text & CTA -->
      <div
        class="absolute space-y-14 lg:space-y-8 w-[90%] sm:w-[765px] top-[200px] sm:top-[250px] left-1/2 transform -translate-x-1/2 sm:left-[254px] sm:translate-x-0 z-10 text-left"
      >
        <HeroHeader
          class="space-y-6"
          title="Web Hosting Built for Speed & Service."
          highlight="Speed"
          highlightColor="cyan"
          subtitle="Lightning-fast hosting for modern websites. Unmatched performance, rock-solid reliability, and expert support that scales with your business."
        />
        <button class="bg-orange-500 hover:bg-orange-600 px-6 py-3 text-white font-medium text-sm rounded">
          START NOW
        </button>
      </div>

      <!-- Background Image -->
      <div
        class="absolute bg-[url('/assets/images/hero_one_gradient.png')] bg-no-repeat bg-contain sm:bg-auto w-full h-full sm:w-[1400px] sm:h-[933px] sm:top-0 sm:left-[541px]"
      >
      </div>
    </div>
  </div>
</template>