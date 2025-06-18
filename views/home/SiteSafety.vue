<script setup lang="ts">
import PageHeader from '~/components/PageHeader.vue'
</script>

<template>
  <AppLayout>
    <template #default>
      <div class="bg-white">
        <div class="min-h-screen px-6 sm:px-10 md:px-20 lg:px-32 py-12 flex flex-col lg:flex-row items-center justify-between gap-12">

          <!-- Left Image -->
          <div class="w-full lg:w-1/2 flex justify-center">
            <img
              src="/assets/images/site_safety.png"
              alt="Site Security Preview"
              class="w-full max-w-md sm:max-w-lg h-auto drop-shadow-xl"
            />
          </div>

          <!-- Right Content -->
          <div class="w-full lg:w-1/2">
            <PageHeader
              class="lg:!text-start"
              title="Your site’s safety isn’t an add-on. It’s our baseline."
              highlight="safety"
              highlightColor="red"
            />

            <p class="mt-6 text-[16px] md:text-[18px] font-light text-gray-600 font-inter">
              <span class="font-bold text-black">At BuiltFast, security is built in.</span>
              Every site comes with free SSL, daily backups, and DDoS protection, so your business stays protected without extra fees or surprise charges. We stay ahead of threats, so you can stay focused on growth.
            </p>

            <p class="mt-6 text-[16px] md:text-[18px] font-light text-gray-600 font-inter">
              <span class="font-bold text-black">We stay ahead of the bad guys, so you don’t have to.</span>
            </p>
          </div>
        </div>
      </div>
    </template>
  </AppLayout>
</template>