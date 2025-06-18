<script setup>
import AppLayout from '~/layout/AppLayout.vue';
import PricingCard from '~/components/PricingCard.vue';

</script>
<template>
 <div class="bg-[#F6F9FB]">
    <AppLayout>
      <template #default>
          <PageHeader
              title="Simple, Transparent Pricing"
              highlight="Transparent"
              highlightColor="cyan"
              subtitle="Our hosting plans give you the speed, simplicity, and support you need."/>
          <div>
            <section class="py-16">
              <!-- Card Layout -->
              <div class="flex flex-col justify-center lg:flex-row lg:space-x-6 space-y-6 lg:space-y-0 justify-center items-center lg:items-start">
  
                <!-- 1. Web Hosting Card -->
                <PricingCard
                    title="Web Hosting"
                    description="Built for growing businesses."
                    price="$4.99"
                    period="/mo"
                    :features="[
                                  '1 Website',
                                  '25 GB SSD storage',
                                  'Free Migration',
                                  'Free SSL certificate',
                                  'Unmetered Bandwidth'
                                  ]"
                    buttonText="VIEW PLANS"
                    buttonLink="#"
                    featureIcon="mdi:check"
  
                    backgroundColor="bg-white"
                    titleColor="text-gray-900"
                    descriptionColor="text-gray-600"
                    priceColor="text-gray-900"
                    periodColor="text-gray-500"
                    mutedTextColor="text-gray-500"
                    featureTextColor="text-gray-700"
                    featureIconColor="text-emerald-500"
                    buttonTextColor="text-white"
                    customButtonBg="#0F172A"
                    customBorderColor="border-gray-200"
                />
  
                <!-- 2. VPS Card (Featured, Colored) -->
                <div class="relative flex justify-center lg:justify-start">
                  <!-- Featured Badge -->
                  <span
                      class="absolute top-[-14px] left-1/2 -translate-x-1/2 text-white text-xs font-semibold py-1 px-3 rounded-full shadow-md border"
                      style="background-color: #FF6542; border-color: #FF6542;"
                  >
                                  FEATURED
                                  </span>
  
                  <PricingCard
                      title="VPS"
                      description="Built for businesses who need extra performance."
                      price="$7.99"
                      period="/mo"
                      :features="[
                                      '5 Websites',
                                      '25 GB SSD storage',
                                      'Free Migration',
                                      'Free SSL certificate',
                                      'Unmetered Bandwidth'
                                  ]"
                      buttonText="VIEW PLANS"
                      buttonLink="#"
                      featureIcon="mdi:check"
                      backgroundColor="bg-white"
                      titleColor="text-gray-900"
                      descriptionColor="text-gray-600"
                      priceColor="text-gray-900"
                      periodColor="text-gray-500"
                      mutedTextColor="text-gray-500"
                      featureTextColor="text-gray-700"
                      featureIconColor="text-emerald-500"
                      buttonTextColor="text-white"
                      customButtonBg="#1DC9D8"
                      customBorderColor="#FF6542"
                  />
                </div>
                <!-- 3. Managed WordPress Card -->
              <PricingCard
                  title="Managed WordPress"
                  description="Built for WordPress optimization."
                  price="$13.00"
                  period="/mo"
                  :features="[
                                '1 Website',
                                '50,000 visits monthly',
                                '25GB NVMe Storage',
                                'Free SSL certificate',
                                'Custom Control Panel'
                                ]"
                  buttonText="VIEW PLANS"
                  buttonLink="#"
                  featureIcon="mdi:check"

                  backgroundColor="bg-white"
                  titleColor="text-gray-900"
                  descriptionColor="text-gray-600"
                  priceColor="text-gray-900"
                  periodColor="text-gray-500"
                  mutedTextColor="text-gray-500"
                  featureTextColor="text-gray-700"
                  featureIconColor="text-emerald-500"
                  buttonTextColor="text-white"
                  customButtonBg="#0F172A"
                  customBorderColor="border-gray-200"
                  buttonBgColor="bg-gray-900"
                  buttonHoverBgColor="hover:bg-gray-800"
              />
            </div>

            <!-- Bottom Note -->
            <p class="mt-20 lg:mt-[80px] mx-auto lg:w-full w-10/12 text-sm text-center text-gray-500 flex items-center justify-center lg:gap-[12px]">
              <Icon icon="mdi:alert-circle-outline" class="size-5 text-teal-500" />
              <span>
                All plans include no questions asked 30-day money-back guarantee.
              </span>
            </p>
          </section>
    
      </div>
    </template>
  </AppLayout>
  </div>
</template>