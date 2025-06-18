<script setup lang="ts">
import PageHeader from '~/components/PageHeader.vue';

// No logic for now, static page
</script>

<template>

<AppLayout>
    <template #default>
        <div class="bg-[#F6F9FB]">
            <div class="min-h-screen px-8 md:px-20 lg:px-32 flex items-center justify-between flex-col lg:flex-row">
                
            <div class="max-w-xl mb-12 lg:mb-0">
                    <PageHeader
                        title="Control with Simplicity"
                        highlight="Simplicity"
                        highlightColor="cyan"
                    />
                    <p class="mt-10 text-[18px] font-light text-gray-600 mx-auto font-inter mb-4">
                        Skip the cluttered dashboards and cookie-cutter panels. Builtfast gives you a
                        custom-built control center, designed from the ground up for speed, clarity, and ease. Everything in one place and easy to navigate.
                    </p>
                
                    <p class="mt-10 text-[18px] font-light text-gray-600 mx-auto font-inter mb-6">
                        No jargon. No overwhelm. Just full control, even if you’re not a tech expert.
                        <span class="font-bold text-black">Built by and for humans. Powered for business.</span>
                     </p>
                     <button
                        class="bg-[#FF6542] hover:bg-[#ff3f1a] text-white font-semibold mt-32"
                        style="width: 155px; height: 51px; padding: 14px 32px; border-radius: 8px; gap: 10px;"
                    >
                        START NOW
                    </button>
            </div>

            <div class="w-full lg:w-1/2 flex justify-center">
                <img src="/assets/images/control_center.png" alt="Dashboard Mockup" class="max-w-full h-auto drop-shadow-xl" />
            </div>
        </div>
    </div>
    </template>
</AppLayout>
</template>

<style scoped>
</style>
