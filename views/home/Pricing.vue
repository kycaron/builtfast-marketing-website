<template>
    <PageHeader 
        title="Simple, Transparent Pricing" 
        highlight="Transparent"
        subtitle="Our hosting plans give you the speed, simplicity, and support you need."/>
    <div>
        <section class="py-16">
            <!-- Card Layout -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">

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
                <div class="relative">
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
            <p class="mt-8 text-sm text-gray-500 flex items-center justify-center gap-1">
                <Icon icon="mdi:alert-circle-outline" class="w-4 h-4 text-teal-500" />
                    All plans include no questions asked 30-day money-back guarantee.
            </p>
        </section>
    </div>
</template>