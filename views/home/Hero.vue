<script setup lang="ts">
import Navbar from '~/components/Navbar.vue';
import HeroHeader from '~/components/HeroHeader.vue';
</script>

<template>
  <div class="min-h-screen w-full bg-black text-white font-inter relative overflow-hidden">
    <Navbar />
    <div class="relative flex h-screen items-center">

      <div
          class="absolute space-y-8"
          style="width: 765px; height: 176px; top:250px; left: 254px;"
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



      <div
      class="absolute bg-[url('/assets/images/hero_one_gradient.png')]"
      style="width: 1400px; height: 933px; top: 0px; left: 541px;"
    >
  </div>

      <!-- <div class="w-full h-full bg-[url(/assets/images/hero_one_gradient.png)]">
       </div> -->
    </div>
  </div>
</template>