<script setup lang="ts">
import AppLayout from '~/layout/AppLayout.vue';
import PageHeader from '~/components/PageHeader.vue';

</script>

<template>

<div class="bg-[#F6F9FB]">
  <AppLayout>
    <template #default>
        <div class="min-h-screen px-6 sm:px-10 md:px-20 lg:px-32 lg:py-12 flex flex-col lg:flex-row items-center justify-between gap-12">
          
          <!-- Text Section -->
          <div class="w-full lg:w-1/2 max-w-xl">
            <PageHeader
              title="Control with Simplicity"
              highlight="Simplicity"
              highlightColor="cyan"
            />
            <p class="mt-6 text-[16px] md:text-[18px] font-light text-gray-600 font-inter">
              Skip the cluttered dashboards and cookie-cutter panels. Builtfast gives you a
              custom-built control center, designed from the ground up for speed, clarity, and ease. Everything in one place and easy to navigate.
            </p>
            <p class="mt-6 text-[16px] md:text-[18px] font-light text-gray-600 font-inter">
              No jargon. No overwhelm. Just full control, even if you’re not a tech expert.
              <span class="font-bold text-black">Built by and for humans. Powered for business.</span>
            </p>
            <button
              class="bg-[#FF6542] hover:bg-[#ff3f1a] text-white font-semibold mt-10 md:mt-16"
              style="width: 155px; height: 51px; padding: 14px 32px; border-radius: 8px;"
            >
              START NOW
            </button>
          </div>

          <!-- Image Section -->
          <div class="w-full lg:w-1/2 flex justify-center">
            <img
              src="/assets/images/control_center.png"
              alt="Dashboard Mockup"
              class="w-full max-w-md sm:max-w-lg h-auto drop-shadow-xl"
            />
          </div>
        </div>
    </template>
  </AppLayout>
  </div>
</template>